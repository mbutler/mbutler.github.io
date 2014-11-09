---
title: Restrict a user to a specific directory
author: Matthew Butler
layout: post
permalink: /restrict-a-user-to-a-specific-directory-in-ubuntu
categories:
  - Uncategorized
---
Once in a while, as system administrator, you&#8217;ll want to create a user that only has access to a specific directory and its subdirectories.  Here&#8217;s how you do it&#8230; in Ubuntu 9.04+ (the packaged ssh is out-of-date in earlier versions).

**Create a new user.**

So to create a user named jsmith we&#8217;d type this as root or with sudo

<div class="codesnip-container" >
  useradd jsmith
</div>

then add a password

<div class="codesnip-container" >
  passwd jsmith
</div>

We&#8217;ll pretend you already have a site set up with them at /srv/www/jsmithsite.com with a subdirectory called public_html. We&#8217;ll assume this is a virtual host and you have other sites configured in your /srv/www directory which you don&#8217;t want them to have access to.

Edit the /etc/passwd file. Find the line with the user (in this case jsmith) and add an absolute path to their directory. You&#8217;ll probably want to change /home/jsmith to /srv/www/jsmithsite.com. Keep their shell /bin/sh unless you want to lock them out completely, in which case you can change it to /bin/false.

**Configure OpenSSH**

Edit your /etc/ssh/sshd_config file, making sure the following line is present. If your system&#8217;s file has a line that begins with &#8220;Subsystem sftp&#8221; modify it to resemble the following:

<div class="codesnip-container" >
  Subsystem sftp internal-sftp
</div>

Continue to add the following block to the end of the file:

<div class="codesnip-container" >
  Match group filetransfer<br /> ChrootDirectory %h<br /> X11Forwarding no<br /> AllowTcpForwarding no<br /> ForceCommand internal-sftp
</div>

Restart OpenSSH:

<div class="codesnip-container" >
  /etc/init.d/ssh restart
</div>

**Modify User Accounts**

Create a group for the users who will only have SFTP access:

<div class="codesnip-container" >
  addgroup filetransfer
</div>

Next, you&#8217;ll need to modify the user accounts that you wish to restrict to using only SFTP. Issue the following commands for each account, substituting the appropriate username. Please keep in mind that this will prevent these users from being able to log into a remote shell session. If you don&#8217;t want to restrict your existing users, you may add new user accounts for file transfer purposes using the adduser command.

<div class="codesnip-container" >
  usermod -G filetransfer jsmith<br /> chown root:root /srv/www/jsmithsite.com<br /> chmod 755 /srv/www/jsmithsite.com
</div>

After issuing these commands, the affected users won&#8217;t be able to create files in their home directories as these directories will be owned by the root user. If you already created the public_html directory you can skip this step, otherwise create them like this:

<div class="codesnip-container" >
  cd /srv/www/jsmithsite.com<br /> mkdir docs public_html<br /> chown jsmith:jsmith *
</div>

Your users should now be able to log into their accounts via SFTP and transfer files to and from the directories located beneath their home directories, but they shouldn&#8217;t be able to see the rest of the server&#8217;s filesystem.

+++++++++++++++++  
The user will need read/execute rights to execute any command (ls, login shell, etc), so you can&#8217;t easily take all rights away.

Usually it&#8217;s enough to make sure they can&#8217;t mess with the home directories of other users. To do this, put the user into a new group (like &#8220;untrusted&#8221;), chown his home directory and revoke the group and other rights on all home directories: chmod go-rwx /home/*/

If that is not enough, create a chroot jail. This is basically a mini Linux where nothing outside a certain directory (the jail) is visible (or accessible). Jailkit might help you to set this up.  
+++++++++++++++++++

disclaimer: A good chunk of this was borrowed from [here][1]

 [1]: http://library.linode.com/networking/security-guides/linux-sftp-jail