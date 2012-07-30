--- 
created: 1226734467
title: Using AppleScript for Automation
layout: post
excerpt: For the couple past months I've been working really hard to streamline my process of <a href="http://www.davidco.com/what_is_gtd.php">Getting Things Done</a> by implementing automation into my workflow. One way I am accomplishing automation is by using <a href="http://www.apple.com/applescript/">AppleScript</a>. With AppleScript I can automate tasks that I would normally have to use my keyboard and mouse to accomplish. Even if the original task only takes me 15 seconds to accomplish, by writing an AppleScript I can turn a 15 second task into a 1 second task by executing a trigger in <a href="http://docs.blacktree.com/quicksilver/overview">Quicksilver</a> that will fire my AppleScript. Not only am I boosting my productivity by saving time to finish a given task, I'm also saving energy by automating mundane work that I really don't want to do any way. A quick way for me to lose momentum and energy in my day is doing mundane, repetitive work.
---
For the couple past months I've been working really hard to streamline my process of <a href="http://www.davidco.com/what_is_gtd.php">Getting Things Done</a> by implementing automation into my workflow. One way I am accomplishing automation is by using <a href="http://www.apple.com/applescript/">AppleScript</a>. With AppleScript I can automate tasks that I would normally have to use my keyboard and mouse to accomplish. Even if the original task only takes me 15 seconds to accomplish, by writing an AppleScript I can turn a 15 second task into a 1 second task by executing a trigger in <a href="http://docs.blacktree.com/quicksilver/overview">Quicksilver</a> that will fire my AppleScript. Not only am I boosting my productivity by saving time to finish a given task, I'm also saving energy by automating mundane work that I really don't want to do any way. A quick way for me to lose momentum and energy in my day is doing mundane, repetitive work.

I'm working on several AppleScripts at the moment to streamline my process. One really simple script I just wrote was archiving an email message in Mail.app. I use <a href="http://www.google.com/a">Google Apps</a> for my two my primary email addresses. I have used Gmails web interface for the past couple years and I have gotten use to using the Gmail shortcut keys in the web interface. To archive a message in Gmail webmail, all I had to to was select a message by hitting &quot;x&quot; on my keyboard and then &quot;y&quot; to move the message out of my inbox. I'm a strong advocate of <a href="http://www.43folders.com/izero">Inbox-Zero</a>, so nothing can stay in my inbox for more then a day (except for weekends of course). Using <a href="http://mail.google.com/support/bin/answer.py?hl=en&answer=6594">Gmail shortcut keys</a> I was able to process my entire inbox rather quickly, while never having to touch my mouse.

I've recently stopped using the Gmail web interface so heavily and setup Mail.app via IMAP to my Google Accounts. I did this so I could take advantage of local features that Mail.app offers me that I can't get from a web interface, the biggest reason being AppleScript capability, second biggest reason being moving mail items to <a href="http://www.omnigroup.com/applications/omnifocus/">OmniFocus</a> quickly. OmniFocus is a topic for another post, so we'll leave that for another day.

The problem with Mail.app is there is no shortcut key for archiving a message in my Inbox. The only way I could get a message out of my inbox in Mail.app into my Gmail archive was to drag the message from the &quot;Inbox&quot; to my &quot;All Mail&quot; folder. Well this would require me to take my hands of my keyboard and use my mouse. That's a huge time waster. I ended up writing a simple AppleScript that moves the file for me. I setup a trigger in Quicksilver to execute the script. Now I can process my inbox in Mail.app without taking my hands away from the keyboard. Below is the code for the AppleScript to archive messages from inbox to Gmail/All mail IMAP folder.

<pre>
(*
	Archive a Gmail Message from Inbox to All Mail
	
	by Tom Friedhof
	
	Copyright © 2008, Tom Friedhof
	
	All rights reserved.
	
	Redistribution and use in source and binary forms, with or without modification, are permitted provided that the following conditions are met:
	
		• Redistributions of source code must retain the above copyright notice, this list of conditions and the following disclaimer.
		
		• Redistributions in binary form must reproduce the above copyright notice, this list of conditions and the following disclaimer in the documentation and/or other materials provided with the distribution.
		
	THIS SOFTWARE IS PROVIDED BY THE COPYRIGHT HOLDERS AND CONTRIBUTORS "AS IS" AND ANY EXPRESS OR IMPLIED WARRANTIES, INCLUDING, BUT NOT LIMITED TO, THE IMPLIED WARRANTIES OF MERCHANTABILITY AND FITNESS FOR A PARTICULAR PURPOSE ARE DISCLAIMED. IN NO EVENT SHALL THE COPYRIGHT OWNER OR CONTRIBUTORS BE LIABLE FOR ANY DIRECT, INDIRECT, INCIDENTAL, SPECIAL, EXEMPLARY, OR CONSEQUENTIAL DAMAGES (INCLUDING, BUT NOT LIMITED TO, PROCUREMENT OF SUBSTITUTE GOODS OR SERVICES; LOSS OF USE, DATA, OR PROFITS; OR BUSINESS INTERRUPTION) HOWEVER CAUSED AND ON ANY THEORY OF LIABILITY, WHETHER IN CONTRACT, STRICT LIABILITY, OR TORT (INCLUDING NEGLIGENCE OR OTHERWISE) ARISING IN ANY WAY OUT OF THE USE OF THIS SOFTWARE, EVEN IF ADVISED OF THE POSSIBILITY OF SUCH DAMAGE.
	
	Version History:
	
		0.1, initial release, 11/14/08
*)

tell application "Mail"
	set theSelectedMessage to selection
	
	-- Make sure a message is selected
	if (count of theSelectedMessage) is equal to 0 then
		display dialog "Select a Message to Archive" buttons "OK"
		return
	end if
	
	-- Mark the messages as read
	repeat with i from 1 to (length of theSelectedMessage)
		set the read status of item i of theSelectedMessage to true
	end repeat
	
	-- Moving the Messages to a All Mail IMAP Folder
	set theMailAccount to account of mailbox of item 1 of theSelectedMessage
	set theMailbox to every mailbox of theMailAccount whose name is "All Mail"
	move the theSelectedMessage to item 1 of theMailbox
	
end tell
</pre>

If you use the script, let me know what you think, and how it can be made better.
