<div id="mw-page-base" class="noprint">

</div>

<div id="mw-head-base" class="noprint">

</div>

<div id="content" class="mw-body" role="main">

<span id="top"></span>

<div class="mw-indicators">

</div>

# High CPU Usage

<div id="bodyContent" class="mw-body-content">

<div id="siteSub">

From VuzeWiki

</div>

<div id="contentSub">

</div>

<div id="jump-to-nav" class="mw-jump">

Jump to: [navigation](#mw-head), [search](#p-search)

</div>

<div id="mw-content-text" class="mw-content-ltr" lang="en" dir="ltr">

General advice on reducing CPU usage is [available
here](/web/20160514113611/http://wiki.vuze.com/w/Reduce_CPU_usage "Reduce CPU usage").

High CPU usage withing the Vuze process can have many causes:

<div id="toc" class="toc">

<div id="toctitle">

## Contents

</div>

-   [<span class="tocnumber">1</span> <span class="toctext">Normal
    Situations</span>](#Normal_Situations)
-   [<span class="tocnumber">2</span> <span class="toctext">Abnormal
    Vuze Causes</span>](#Abnormal_Vuze_Causes)
-   [<span class="tocnumber">3</span> <span class="toctext">Abnormal
    External Causes</span>](#Abnormal_External_Causes)
-   [<span class="tocnumber">4</span> <span
    class="toctext">Diagnosis</span>](#Diagnosis)

</div>

## <span id="Normal_Situations" class="mw-headline">Normal Situations</span><span class="mw-editsection"><span class="mw-editsection-bracket">\[</span>[edit](/web/20160514113611/http://wiki.vuze.com/mediawiki/index.php?title=High_CPU_Usage&action=edit&section=1 "Edit section: Normal Situations")<span class="mw-editsection-bracket">\]</span></span>

-   Hash Checking

When pieces of a file are downloaded they are checked for correctness by
calculating their unique hash. This takes a small amount of CPU per
piece and if you are downloading quickly this can add up. This process
also occurs when you manually recheck a file via the 'force recheck'
menu option

-   Transcoding

Converting video file formats is CPU intensive, so when you are doing
this you will see high CPU usage. Note that in this case the CPU usage
is registered against the converter application rather than the Vuze
process.

-   Cryptography

In general cryptography (encryption, decryption) is resource intensive.
If you install the
<a href="/web/20160514113611/http://wiki.vuze.com/w/I2P" class="mw-redirect" title="I2P">I2P plugin</a>
then you will see elevated CPU usage as a result of its continual
cryptographic operations.

## <span id="Abnormal_Vuze_Causes" class="mw-headline">Abnormal Vuze Causes</span><span class="mw-editsection"><span class="mw-editsection-bracket">\[</span>[edit](/web/20160514113611/http://wiki.vuze.com/mediawiki/index.php?title=High_CPU_Usage&action=edit&section=2 "Edit section: Abnormal Vuze Causes")<span class="mw-editsection-bracket">\]</span></span>

-   Memory Exhaustion

Vuze runs within a Java virtual machine (JVM) - this uses a garbage
collected 'heap' to store data. The size of the heap is constrained,
more information is [available
here](/web/20160514113611/http://wiki.vuze.com/w/Java_VM_memory_usage "Java VM memory usage").
If you have a lot of active torrents the heap can become full. As this
happens the JVM spends more and more effort trying to make space in the
heap and this in turn causes increased CPU usage.

-   Bug

Occasionally a bug within Vuze might cause a thread to loop (incorrect
locking of access to a HashSet would be a good example of a rarely
triggered situation)

## <span id="Abnormal_External_Causes" class="mw-headline">Abnormal External Causes</span><span class="mw-editsection"><span class="mw-editsection-bracket">\[</span>[edit](/web/20160514113611/http://wiki.vuze.com/mediawiki/index.php?title=High_CPU_Usage&action=edit&section=3 "Edit section: Abnormal External Causes")<span class="mw-editsection-bracket">\]</span></span>

-   Third party applications such as virus scanners often inject their
    components into the Vuze process in order to monitor network
    traffic. If there is a bug in these components, or they have
    performance issues, this will appear to be an issue with the Vuze
    process itself.

<!-- -->

-   ESET Smart Security version 8

See [Known
Issues](/web/20160514113611/http://wiki.vuze.com/w/Known_Issues#ESET_Smart_Security_version_8:_High_CPU_in_Vuze "Known Issues")

## <span id="Diagnosis" class="mw-headline">Diagnosis</span><span class="mw-editsection"><span class="mw-editsection-bracket">\[</span>[edit](/web/20160514113611/http://wiki.vuze.com/mediawiki/index.php?title=High_CPU_Usage&action=edit&section=4 "Edit section: Diagnosis")<span class="mw-editsection-bracket">\]</span></span>

Vuze monitors the various threads within the process and logs details of
the most active thread to rotating log files named thread_1.log and
thread_2.log in the 'logs' folder of the [configuration
folder](/web/20160514113611/http://wiki.vuze.com/w/Configuration_directory "Configuration directory").
An example line from these files is

<div style="text-align:right; margin-bottom:-37px;">

Copy to Clipboard

</div>

```
[21:36:13] Thread state: elapsed=10001,cpu=2790,max=PRUDPPacketHandler:sender(1404/14%),mem:max=253440,tot=66640,free=36124
```

The first 'max=' entry shows the thread name most active in the last 10
seconds (in this case 'PRUDPPacketHandler:sender') followed by the
amount of CPU used (14%). Following this is the current JVM memory
situation. The 'max' value here (253440) gives the maximum size the heap
can grow to in KB. The 'tot' value gives the current total size of the
heap (66640) in KB, so in this case around 250MB is available but only
66MB is in use. The 'free' value indicates how much of the 'tot'
allocated value is actually free for use.

If you have a 'tot' value that has grown to around 'max', and a small
'free' value then you are running low on heap memory.

The above example was from a user with the ESET induced CPU usage issue.

If you are running I2P then you will see threads with names like 'YK
Precalc' and 'Job Queue n/m' as active, this is normal.

If a thread is using a very large amount of CPU (in the case of a bug
perhaps) then the log file will also contain a stack trace of the
offending thread. This can be very useful to the developers to please
report this on the
<a href="https://web.archive.org/web/20160514113611/http://forum.vuze.com/" class="external text">forums</a>
if you see it.

</div>

<div class="printfooter">

Retrieved from
"[http://wiki.vuze.com/mediawiki/index.php?title=High_CPU_Usage&oldid=16432](https://web.archive.org/web/20160514113611/http://wiki.vuze.com/mediawiki/index.php?title=High_CPU_Usage&oldid=16432)"

</div>

<div id="catlinks" class="catlinks catlinks-allhidden">

</div>

<div class="visualClear">

</div>

</div>

</div>

<div id="mw-navigation">

## Navigation menu

<div id="mw-head">

<div id="p-personal" role="navigation"
aria-labelledby="p-personal-label">

### Personal tools

-   <span id="pt-createaccount">[Create
    account](/web/20160514113611/http://wiki.vuze.com/mediawiki/index.php?title=Special:UserLogin&returnto=High+CPU+Usage&type=signup "You are encouraged to create an account and log in; however, it is not mandatory")</span>
-   <span id="pt-login">[Log
    in](/web/20160514113611/http://wiki.vuze.com/mediawiki/index.php?title=Special:UserLogin&returnto=High+CPU+Usage "You are encouraged to log in; however, it is not mandatory [o]")</span>

</div>

<div id="left-navigation">

<div id="p-namespaces" class="vectorTabs" role="navigation"
aria-labelledby="p-namespaces-label">

### Namespaces

-   <span
    id="ca-nstab-main">[Page](/web/20160514113611/http://wiki.vuze.com/w/High_CPU_Usage "View the content page [c]")</span>
-   <span
    id="ca-talk">[Discussion](/web/20160514113611/http://wiki.vuze.com/mediawiki/index.php?title=Talk:High_CPU_Usage&action=edit&redlink=1 "Discussion about the content page [t]")</span>

</div>

<div id="p-variants" class="vectorMenu emptyPortlet" role="navigation"
aria-labelledby="p-variants-label">

### Variants[](#)

<div class="menu">

</div>

</div>

</div>

<div id="right-navigation">

<div id="p-views" class="vectorTabs" role="navigation"
aria-labelledby="p-views-label">

### Views

-   <span
    id="ca-view">[Read](/web/20160514113611/http://wiki.vuze.com/w/High_CPU_Usage)</span>
-   <span
    id="ca-edit">[Edit](/web/20160514113611/http://wiki.vuze.com/mediawiki/index.php?title=High_CPU_Usage&action=edit "Edit this page [e]")</span>
-   <span id="ca-history">[View
    history](/web/20160514113611/http://wiki.vuze.com/mediawiki/index.php?title=High_CPU_Usage&action=history "Past revisions of this page [h]")</span>

</div>

<div id="p-cactions" class="vectorMenu emptyPortlet" role="navigation"
aria-labelledby="p-cactions-label">

### More[](#)

<div class="menu">

</div>

</div>

<div id="p-search" role="search">

### Search

<div id="simpleSearch">

</div>

</div>

</div>

</div>

<div id="mw-panel">

<div id="p-logo" role="banner">

<a href="/web/20160514113611/http://wiki.vuze.com/w/Main_Page" class="mw-wiki-logo" title="Visit the main page"></a>

</div>

<div id="p-" class="portal" role="navigation"
aria-labelledby="p--label">

### 

<div class="body">

-   <span id="n-Download-Vuze-Now">[Download Vuze
    Now](https://web.archive.org/web/20160514113611/http://www.vuze.com/download)</span>

</div>

</div>

<div id="p-navigation" class="portal" role="navigation"
aria-labelledby="p-navigation-label">

### Navigation

<div class="body">

-   <span id="n-mainpage-description">[Main
    page](/web/20160514113611/http://wiki.vuze.com/w/Main_Page "Visit the main page [z]")</span>
-   <span id="n-recentchanges">[Recent
    changes](/web/20160514113611/http://wiki.vuze.com/w/Special:RecentChanges "A list of recent changes in the wiki [r]")</span>
-   <span id="n-randompage">[Random
    page](/web/20160514113611/http://wiki.vuze.com/w/Special:Random "Load a random page [x]")</span>
-   <span
    id="n-help">[Help](https://web.archive.org/web/20160514113611/https://www.mediawiki.org/wiki/Special:MyLanguage/Help:Contents "The place to find out")</span>

</div>

</div>

<div id="p-tb" class="portal" role="navigation"
aria-labelledby="p-tb-label">

### Tools

<div class="body">

-   <span id="t-whatlinkshere">[What links
    here](/web/20160514113611/http://wiki.vuze.com/w/Special:WhatLinksHere/High_CPU_Usage "A list of all wiki pages that link here [j]")</span>
-   <span id="t-recentchangeslinked">[Related
    changes](/web/20160514113611/http://wiki.vuze.com/w/Special:RecentChangesLinked/High_CPU_Usage "Recent changes in pages linked from this page [k]")</span>
-   <span id="t-specialpages">[Special
    pages](/web/20160514113611/http://wiki.vuze.com/w/Special:SpecialPages "A list of all special pages [q]")</span>
-   <span id="t-print">[Printable
    version](/web/20160514113611/http://wiki.vuze.com/mediawiki/index.php?title=High_CPU_Usage&printable=yes "Printable version of this page [p]")</span>
-   <span id="t-permalink">[Permanent
    link](/web/20160514113611/http://wiki.vuze.com/mediawiki/index.php?title=High_CPU_Usage&oldid=16432 "Permanent link to this revision of the page")</span>
-   <span id="t-info">[Page
    information](/web/20160514113611/http://wiki.vuze.com/mediawiki/index.php?title=High_CPU_Usage&action=info "More information about this page")</span>

</div>

</div>

</div>

</div>

<div id="footer" role="contentinfo">

-   <span id="footer-info-lastmod">This page was last modified on 22
    January 2015, at 18:48.</span>
-   <span id="footer-info-viewcount">This page has been accessed 2,893
    times.</span>

<!-- -->

-   <span id="footer-places-about">[About
    VuzeWiki](/web/20160514113611/http://wiki.vuze.com/w/VuzeWiki:About "VuzeWiki:About")</span>
-   <span
    id="footer-places-mobileview"><a href="https://web.archive.org/web/20160514113611/http://wiki.vuze.com/mediawiki/index.php?title=High_CPU_Usage&amp;mobileaction=toggle_view_mobile" class="noprint stopMobileRedirectToggle">Mobile view</a></span>

<!-- -->

-   <span
    id="footer-poweredbyico">[<img src="/web/20160514113611im_/http://wiki.vuze.com/mediawiki/resources/assets/poweredby_mediawiki_88x31.png" srcset="/web/20160514113611im_/http://wiki.vuze.com/mediawiki/resources/assets/poweredby_mediawiki_132x47.png 1.5x, /web/20160514113611im_/http://wiki.vuze.com/mediawiki/resources/assets/poweredby_mediawiki_176x62.png 2x" width="88" height="31" alt="Powered by MediaWiki" />](//web.archive.org/web/20160514113611/http://www.mediawiki.org/)</span>
-   <span id="footer-analyticsystemsico">Any use of Vuze® and Vuze+™
    that violates the rights of any person or entity is not allowed.
    [More](https://web.archive.org/web/20160514113611/http://vuze.com/corp/legal.php)</span>

<div style="clear:both">

</div>

</div>
