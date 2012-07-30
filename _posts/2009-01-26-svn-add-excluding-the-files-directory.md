--- 
created: 1233039318
title: svn add - excluding the files directory
layout: post
excerpt: I use bash script that I found on <a href="http://gotdrupal.com/videos/svn-filtering">GotDrupal</a> for adding and removing files from svn using a regular expression.  I normally use the command for simple tasks, like the ones shown in the video on GotDrupal, but today I used a regular expression that took me a few minutes to get working.
---
I use bash script that I found on <a href="http://gotdrupal.com/videos/svn-filtering">GotDrupal</a> for adding and removing files from svn using a regular expression.  I normally use the command for simple tasks, like the ones shown in the video on GotDrupal, but today I used a regular expression that took me a few minutes to get working.

I wanted to add everything in my local development environment to the svn repository except for the files directory.  The first thing I did was add my Drupal install non recursively, then with my handy svngrep command added the rest of the directories, except for the files directory.

<code>
svn add -N drupal
cd drupal
svngrep '^\?.*[^( files$)].*$' add
</code>
