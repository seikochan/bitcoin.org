---
layout: base
lang: en
id: developer-guide
title: "Developer Guide - Bitcoin"
---

[transaction malleability]: #term-transaction-malleability

# End-User Guide

<p class="summary">Find detailed information about the Bitcoin protocol and related specifications.</p>

<div markdown="1" id="toc" class="toc"><div markdown="1">

* Table of contents
{:toc}

</div></div>


<!--#md#<div markdown="1" class="toccontent">#md#-->

<p style="padding:10px;background-color:rgb(255, 242, 202);"><b>Contribute</b>: This document is still being written; if you find a mistake, please
<a href="https://github.com/saivann/bitcoin.org/issues">open an issue</a>. If you want to write or edit a section, please read and comment on our <a href="https://bitcointalk.org/index.php?topic=511876">forum thread</a> or sign up for our <a href="https://groups.google.com/forum/?hl=en#!forum/bitcoin-documentation">mailing list</a>. This live preview is temporary and should eventually be merged on bitcoin.org .</p>

**Note**: Some strings are shortened or wrapped: "[...]" indicates extra data was removed, and lines ending in a single backslash "\\" are continued below.


## Viewing Hidden Files/Folders

### Windows 7

### Windows 8

### Linux
1. Navigate to the directory/folder you would like to display the contents of.
2. Use the command 'ls -al' to list all files or folders, including hidden ones.  
{% highlight bash lineos %}
[username@localhost ~]$ cd .bitcoin/
[username@localhost .bitcoin]$ ls
[username@localhost ~]$ ls
Documents    Pictures    Videos    Downloads  Music    Desktop                
[username@localhost ~]$ ls -al
total 288
drwx--x--x. 44 username username  4096 Apr 18 10:23 .
drwxr-xr-x.  7 root      root       4096 Apr 13 11:35 ..
-rw-------.  1 username username 12937 Apr 18 10:22 .bash_history
-rw-r--r--.  1 username username    18 Aug  9  2013 .bash_logout
-rw-r--r--.  1 username username   193 Feb 15 17:16 .bash_profile
-rw-r--r--.  1 username username   291 Feb 15 17:19 .bashrc
drwxrwxr-x.  4 username username  4096 Apr  4 15:14 bin
drwxrwxr-x.  5 username username  4096 Mar 21 15:06 .bitcoin
drwxr-xr-x.  2 username username  4096 Mar 25 16:59 Desktop
drwxr-xr-x.  3 username username  4096 Mar 25 17:12 Documents
drwxr-xr-x.  7 username username  4096 Apr 16 12:04 Downloads
drwxr-xr-x.  2 username username  4096 Jan 20 18:02 Music
drwxr-xr-x.  6 username username  4096 Apr 13 13:07 Pictures
drwxr-xr-x.  2 username username  4096 Mar 26 08:27 .vim
-rw-------.  1 username username  7362 Apr 13 14:17 .viminfo
{% endhighlight %}


### Mac OSX

## Viewing File Extensions

### Windows 7
1. Open Windows Explorer.
2. If you do not see a menu bar ("File", "Edit", "View", etc), press the 'alt' button.  
![file-ext-win7-1](/img/end-user/file-extensions-win7/alt-menu-bar.png)  

3. Click on 'Tools' -> 'Folder Options'.  
![file-ext-win7-1](/img/end-user/file-extensions-win7/tools.png)

4. You should now see the popup 'Folder Options' window.  
![file-ext-win7-1](/img/end-user/file-extensions-win7/folder-options.png)

5. Click on the 'View' tab.
6. Uncheck 'Hide extensions for known file types.'
7. Click the 'Apply' button, then 'OK' button.  
![file-ext-win7-1](/img/end-user/file-extensions-win7/view-settings.png)

### Windows 8
1. Open Windows Explorer.
2. Click the 'View' tab.   
![file-ext-win7-1](/img/end-user/file-extensions-win8/view.png)  

3. Click on 'Options' -> 'Change folder and search options'  
![file-ext-win7-1](/img/end-user/file-extensions-win8/options.png)

4. You should now see the popup 'Folder Options' window.  
5. Click the 'View' tab.   
![file-ext-win7-1](/img/end-user/file-extensions-win8/folder-options.png)

6. Uncheck 'Hide extensions for known file types.'
7. Click the 'Apply' button, then 'OK' button.    
![file-ext-win7-1](/img/end-user/file-extensions-win8/unhide-extensions.png)


### Linux
On linux systems, extensions are usually not hidden to begin with.

1. Navigate to the directory/folder you would like to display the contents of.
2. Use the command 'ls' to list all files or folders.  This will list them with their file extensions as well.

{% highlight bash lineos %}
[username@localhost ~]$ cd .bitcoin/
[username@localhost .bitcoin]$ ls
bitcoin.conf  blocks  chainstate  __db.001  __db.002  
__db.003  db.log  debug.log  peers.dat  testnet3  wallet.dat
{% endhighlight %}


### Mac OSX


## Locating Important Files 

### Bitcoin-qt  

#### Windows 8
1. Open the run window by pressing 'Windows' + r.
2. Type in '%APPDATA%'.  
![file-ext-win7-1](/img/end-user/bitcoin-qt-win8/run-window.png)

3. Once you hit enter or press 'OK', you should see the following Appdata Roaming window.  
4. Open the 'Bitcoin' directory.  
![file-ext-win7-1](/img/end-user/bitcoin-qt-win8/appdata.png)

5.  This is where you will find all the data that is held by your wallet.  
![file-ext-win7-1](/img/end-user/bitcoin-qt-win8/bitcoin.png)

6.  The only important file you need to backup and keep secure, is the wallet.dat file as shown below.  (If you cannot see the .dat extention, refer to the __[file extension][view-file-extentions]__ section)  
![file-ext-win7-1](/img/end-user/bitcoin-qt-win8/wallet.png)

#### Windows 7
1. Open the run window by:
 1. 'Windows' + r   OR
 2.  click the start button and type in 'run' into the search bar.

#### Linux

#### Mac OSX

### Electrum

#### Windows 8
1. Open the run window by pressing 'Windows' + r.
2. Type in '%APPDATA%'.  
![file-ext-win7-1](/img/end-user/electrum-win8/run-window.png)

3. Once you hit enter or press 'OK', you should see the following Appdata Roaming window.  
4. Open the 'Electrum' directory.  
![file-ext-win7-1](/img/end-user/electrum-win8/appdata-window.png)

5.  This is where you will find all the data that is held by your wallet.  
![file-ext-win7-1](/img/end-user/electrum-win8/electrum-window.png)

6.  The only important file you need to backup and keep secure, is the default_wallet file as shown below.  
![file-ext-win7-1](/img/end-user/electrum-win8/wallet.png)

#### Windows 7
1. Open the run window by:
 1. 'Windows' + r   OR
 2.  click the start button and type in 'run' into the search bar.

#### Linux

#### Mac OSX


<!-- Links to terms used in this document (case-insensitive alphabetic order)
---- * Link text is case insensitive in markdown so [Block Chain] and
----   [block chain] are equivalent
---- * If nothing uses one of the below reference links, the reference
----   link must be commented out or it will appear in the rendered page
-->
[view-file-extentions]: #viewing-file-extensions

<script>updateToc();</script>
