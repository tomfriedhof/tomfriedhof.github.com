--- 
created: 1195151243
title: Polycom 501 Contact Directory
layout: post
excerpt: I finally found the format of the directory.xml file for my Polycom 501 IP phone after searching the web for about a half hour looking for it.  Where better place to keep the format than in the <a href="/files/PolycomAdminGuide167.pdf">Polycom Admin Guide</a>.  I found an entry on <a href="http://www.voip-info.org/wiki/index.php?page=Polycom+Soundpoint+IP+501">voip-info.org</a>, but it didn't mention all the XML elements I could use.  So being the curious guy that I am, I had to know all the options available to me.
tags: [asterisk, trixbox]
---
<br />
<img class="float-left" src="/files/d_209.jpg" width="250" height="178" />
<p>
I finally found the format of the directory.xml file for my Polycom 501 IP phone after searching the web for about a half hour looking for it.  Where better place to keep the format than in the <a href="/files/PolycomAdminGuide167.pdf">Polycom Admin Guide</a>.  I found an entry on <a href="http://www.voip-info.org/wiki/index.php?page=Polycom+Soundpoint+IP+501">voip-info.org</a>, but it didn't mention all the XML elements I could use.  So being the curious guy that I am, I had to know all the options available to me.
</p>
<p>
I'm reposting the doc page here so google can index it, and if I forget and need a reminder of what the XML elements are Google might lead me back here.
</p>
<p>
 <!--break-->
</p>
<p>
 
</p>
<p style="font: normal normal normal 15px/normal Helvetica; margin: 0px">
3.1.17.1  Local Contact Directory File Format<span style="font: normal normal normal 12px/normal Helvetica"> </span>
</p>
<p style="font: normal normal normal 12px/normal Times; margin: 0px">
An example local contact directory is shown.  Look to the table for an explanation of 
</p>
<p style="font: normal normal normal 12px/normal Times; margin: 0px">
each element.<span style="font: normal normal normal 12px/normal Helvetica"> </span>
</p>
<p style="font: normal normal normal 12px/normal Times; margin: 0px">
 
</p>
<p style="font: normal normal normal 11px/normal Helvetica; margin: 0px">
Local Contact Directory File example:<span style="font: normal normal normal 12px/normal Helvetica"> </span>
</p>
<p style="font: normal normal normal 12px/normal Helvetica; margin: 0px">
&lt;?xml version=&quot;1.0&quot; encoding=&quot;UTF-8&quot; standalone=&quot;yes&quot; ?&gt;  
</p>
<p style="font: normal normal normal 12px/normal Helvetica; margin: 0px">
&lt;directory&gt; 
</p>
<p style="font: normal normal normal 12px/normal Helvetica; margin: 0px">
      &lt;item_list&gt; 
</p>
<p style="font: normal normal normal 12px/normal Helvetica; margin: 0px">
          &lt;item&gt; 
</p>
<p style="font: normal normal normal 12px/normal Helvetica; margin: 0px">
              &lt;ln&gt;Doe&lt;/ln&gt;  
</p>
<p style="font: normal normal normal 12px/normal Helvetica; margin: 0px">
              &lt;fn&gt;John&lt;/fn&gt;  
</p>
<p style="font: normal normal normal 12px/normal Helvetica; margin: 0px">
              &lt;ct&gt;1001&lt;/ct&gt;  
</p>
<p style="font: normal normal normal 12px/normal Helvetica; margin: 0px">
              &lt;sd&gt;1&lt;/sd&gt;  
</p>
<p style="font: normal normal normal 12px/normal Helvetica; margin: 0px">
              &lt;rt&gt;1&lt;/rt&gt;  
</p>
<p style="font: normal normal normal 12px/normal Helvetica; margin: 0px">
              &lt;dc /&gt;  
</p>
<p style="font: normal normal normal 12px/normal Helvetica; margin: 0px">
              &lt;ad&gt;0&lt;/ad&gt;  
</p>
<p style="font: normal normal normal 12px/normal Helvetica; margin: 0px">
              &lt;ar&gt;0&lt;/ar&gt;  ;/p&gt;
</p>
<p style="font: normal normal normal 12px/normal Helvetica; margin: 0px">
              &lt;bw&gt;0&lt;/bw&gt;  
</p>
<p style="font: normal normal normal 12px/normal Helvetica; margin: 0px">
              &lt;bb&gt;0&lt;/bb&gt;  
</p>
<p style="font: normal normal normal 12px/normal Helvetica; margin: 0px">
          &lt;/item&gt; 
</p>
<p style="font: normal normal normal 12px/normal Helvetica; margin: 0px">
          • • • 
</p>
<p style="font: normal normal normal 12px/normal Helvetica; margin: 0px">
      &lt;/item_list&gt; 
</p>
<p style="font: normal normal normal 12px/normal Helvetica; margin: 0px">
&lt;/directory&gt; 
</p>
<p style="font: normal normal normal 12px/normal Times; margin: 0px">
 
</p>
<p style="font: normal normal normal 12px/normal Times; margin: 0px">
fn - First Name
</p>
<p style="font: normal normal normal 12px/normal Times; margin: 0px">
ln - Last Name
</p>
<p style="font: normal normal normal 12px/normal Times; margin: 0px">
ct - Contact
</p>
<p style="font: normal normal normal 12px/normal Times; margin: 0px">
sd - Speed Dial
</p>
<p style="font: normal normal normal 12px/normal Times; margin: 0px">
rt - Ring Type
</p>
<p style="font: normal normal normal 12px/normal Times; margin: 0px">
dc - Divert Contact
</p>
<p style="font: normal normal normal 12px/normal Times; margin: 0px">
ad - Auto Divert
</p>
<p style="font: normal normal normal 12px/normal Times; margin: 0px">
ar - Auto Reject
</p>
<p style="font: normal normal normal 12px/normal Times; margin: 0px">
bw - Buddy Watching
</p>
<p style="font: normal normal normal 12px/normal Times; margin: 0px">
bb - Buddy Block
</p>
<p style="font: normal normal normal 12px/normal Times; margin: 0px">
 
</p>
<p style="font: normal normal normal 12px/normal Times; margin: 0px">
 
</p>
<p style="font: normal normal normal 12px/normal Times; margin: 0px">
You can also download the Admin Manual Here. Page 31.
</p>
<p>
 
</p>
