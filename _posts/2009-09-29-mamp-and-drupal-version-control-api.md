--- 
created: 1254232566
title: MAMP and Drupal Version Control API
layout: post
excerpt: I recently installed the Version Control API Drupal module to give it a test run.  Unfortunately it did not work right out of the box.  I was getting the following error when trying to refresh my svn logs through my sandbox Drupal site running in MAMP
tags: [drupal, mamp, svn, vcs]
---
I recently installed the <a href="http://drupal.org/project/versioncontrol">Version Control AP</a>I Drupal module to give it a test run.  Unfortunately it did not work right out of the box.  I was getting the following error when trying to refresh my svn logs through my sandbox Drupal site running in MAMP:

<code>
dyld: lazy symbol binding failed: Symbol not found: _iconv_open
  Referenced from: /usr/lib/libaprutil-1.0.dylib
  Expected in: /Applications/MAMP/Library/lib/libiconv.2.dylib

dyld: Symbol not found: _iconv_open
  Referenced from: /usr/lib/libaprutil-1.0.dylib
  Expected in: /Applications/MAMP/Library/lib/libiconv.2.dylib
</code>

After some googling for a while, it became apparent that the svn binaries that are installed by XCode Tools just needed to be updated.

Downloading a <a href="http://www.open.collab.net/downloads/apple/download.html">newer version of subversion</a> ended fixing the error.   The new subversion binaries are installed to the following directory:

<code>
/opt/subversion/
</code>

After installing the new binaries, all you need to do is make sure that the svn executable that MAMP is trying to use is the new one.  Just setup a symlink from your current svn binary to the new svn binary and you should be good to go:

<code>
ln -nsf /opt/subversion/bin/svn /usr/bin/svn
</code>

Once that is done check the version of svn to make sure that you're running the new version:

<code>
svn --version
</code>

With the new subversion binaries that should clear up the "dyld: Symbol not found: _iconv_open" errors.  Good Luck!
