--- 
created: 1190405092
title: Drupal Asterisk module
layout: post
excerpt: A couple weeks ago after I upgraded my home office PBX to <a href="http://www.trixbox.org/">Trixbox 2.2.4</a> I did a search on <a href="http://drupal.org">drupal.org</a> to see if there were any modules for <a href="http://asterisk.org/">Asterisk</a>.  Sure enough I <a href="http://drupal.org/project/asterisk">found one</a> that had been ported from drupal 4.6 by <a href="http://drupal.org/user/22079">Chad Phillips</a>, better known as <a href="http://drupal.org/user/22079">hunmonk</a> in the drupal community.
---
<p>
<img class="float-left" src="/files/Asterisk_logo_7.png" width="300" height="150" />
A couple weeks ago after I upgraded my home office PBX to <a href="http://www.trixbox.org/">Trixbox 2.2.4</a> I did a search on <a href="http://drupal.org">drupal.org</a> to see if there were any modules for <a href="http://asterisk.org/">Asterisk</a>.  Sure enough I <a href="http://drupal.org/project/asterisk">found one</a> that had been ported from drupal 4.6 by <a href="http://drupal.org/user/22079">Chad Phillips</a>, better known as <a href="http://drupal.org/user/22079">hunmonk</a> in the drupal community.
</p>
<p>
If you haven't checked out the module, check out his <a href="http://asterisk.drupal.xcarnated.com/">demo site</a> and get in touch with hunmonk for a live demonstration.  He showed me some pretty cool features in the demonstration, but the one that sold me was the call bridge.  What happens is:
</p>
<ol>
	<li>You enter a phone number on your drupal web site</li>
	<li>Your drupal site will make an <a href="http://en.wikipedia.org/wiki/XML-RPC">XML-RPC</a> request to your asterisk server which doesn't have to be running drupal.</li>
	<li>Your asterisk server places a call to the phone number you configured for your account on your drupal site.</li>
	<li>Once you answer the call that your asterisk server placed, it will start calling the number that you entered on your drupal site.</li>
	<li>When the other end of the phone call picks up, the call is bridged.</li>
</ol>
<p>
<img class="float-right" src="/files/sprint_logo.jpg" width="275" height="144" />This is a pretty sweet deal if you have Sprint or Nextel and a free incoming plan.  Basically you can call anyone without running up your minutes.  What even makes this feature even more cool is that the voip provider I use allows me to caller id spoof.  I have 5 different phone numbers, and with caller id spoofing I can make all my phone lines look like one phone number.  I can be any where in the world and make it appear that I'm calling whoever from my home, or cell, or... you get the idea.
</p>
<p>
The installation instructions for the module are awesome.  Chad really took the time to make sure this module was well documented.  I did run into a few issues with my asterisk configuration to work with the drupal module, but I didn't have to modify anything in the drupal module to get it to work.  Just a couple things in my dial plan.  I'll leave that for another blog post though. 
</p>
