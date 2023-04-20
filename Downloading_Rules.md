<div id="mw-page-base" class="noprint">

</div>

<div id="mw-head-base" class="noprint">

</div>

<div id="content" class="mw-body" role="main">

<span id="top"></span>

<div class="mw-indicators">

</div>

# Downloading Rules

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

Downloading rules can be used to automatically determine a torrent's
position in the download queue. You can control downloading rules from
[Options](/web/20171031042237/http://wiki.vuze.com/w/UG_Options "UG Options")
\>
[Queue](/web/20171031042237/http://wiki.vuze.com/w/UG_Options#Queue_options "UG Options")
\>
[Downloading](/web/20171031042237/http://wiki.vuze.com/w/UG_Options#Downloading "UG Options").

If you have more than one torrent downloading then they are assigned
positions in the download queue. Normally a new torrent will be added to
the bottom of the queue although this can be changed when adding a
torrent in the options dialog.

You can also re-organize the download queue by dragging and dropping
torrents as required, or by right-clicking and selecting the
'reposition' option.

The maximum number of active downloads is defined in the general
[Queue](/web/20171031042237/http://wiki.vuze.com/w/UG_Options#Queue_options "UG Options")
options - if you have more than this number of downloads the remainder
will wait in a queued state until a slot becomes available (there are
also options that permit stalled downloads not to be counted as active,
so you may see extra downloads active in this case)

There are three options for ordering the downloads:

### <span id="Order_Based" class="mw-headline">Order Based</span><span class="mw-editsection"><span class="mw-editsection-bracket">\[</span>[edit](/web/20171031042237/http://wiki.vuze.com/mediawiki/index.php?title=Downloading_Rules&action=edit&section=1 "Edit section: Order Based")<span class="mw-editsection-bracket">\]</span></span>

This is the default, download priority is based on the order that you
manually set for the downloads.

### <span id="Seed_Count_Based" class="mw-headline">Seed Count Based</span><span class="mw-editsection"><span class="mw-editsection-bracket">\[</span>[edit](/web/20171031042237/http://wiki.vuze.com/mediawiki/index.php?title=Downloading_Rules&action=edit&section=2 "Edit section: Seed Count Based")<span class="mw-editsection-bracket">\]</span></span>

Since 5711_B04 there has been the option to automatically order the
downloads based on the number of seeds (and peers if seed counts are
equal) that each download has.

### <span id="Speed_Based" class="mw-headline">Speed Based</span><span class="mw-editsection"><span class="mw-editsection-bracket">\[</span>[edit](/web/20171031042237/http://wiki.vuze.com/mediawiki/index.php?title=Downloading_Rules&action=edit&section=3 "Edit section: Speed Based")<span class="mw-editsection-bracket">\]</span></span>

For the rules to be effective it is important that you set a global
download limit within Vuze - right click on the download speed indicator
on bottom right of the status bar or go to Tools->Options->Transfer to
set this. If you don't know your download limit run a speed test. The
reason this is important is that when a limit is in place Vuze can
easily determine if your download speed is optimized and therefore that
there is no point in attempting further adjustment. The adjustment
process requires that the potential download speed of downloads be
tested - this can cause a transitory decrease in overall download rate.

It is only worth enabling this option if you have a number of incomplete
downloads in a queued state.

The following options influence behavior:

-   Download speed evaluation period: the number of seconds that a
    download will be allowed to run for at the top of the queue to
    assess its potential download speed
-   Re-evaluate downloads: the number of minutes to wait before
    re-evaluating a download's potential speed. Enter zero to disable
    this.

<span class="small">Read the [Azureus
FAQ](/web/20171031042237/http://wiki.vuze.com/w/Azureus_FAQ "Azureus FAQ")</span>

</div>

<div class="printfooter">

Retrieved from
"[http://wiki.vuze.com/mediawiki/index.php?title=Downloading_Rules&oldid=17204](https://web.archive.org/web/20171031042237/http://wiki.vuze.com/mediawiki/index.php?title=Downloading_Rules&oldid=17204)"

</div>

<div id="catlinks" class="catlinks" mw="interface">

<div id="mw-normal-catlinks" class="mw-normal-catlinks">

[Categories](/web/20171031042237/http://wiki.vuze.com/w/Special:Categories "Special:Categories"):

-   [Technical
    Information](/web/20171031042237/http://wiki.vuze.com/w/Category:Technical_Information "Category:Technical Information")
-   [User
    Guide](/web/20171031042237/http://wiki.vuze.com/w/Category:User_Guide "Category:User Guide")

</div>

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

-   <span id="pt-anonuserpage">Not logged in</span>
-   <span
    id="pt-anontalk">[Talk](/web/20171031042237/http://wiki.vuze.com/w/Special:MyTalk "Discussion about edits from this IP address [n]")</span>
-   <span
    id="pt-anoncontribs">[Contributions](/web/20171031042237/http://wiki.vuze.com/w/Special:MyContributions "A list of edits made from this IP address [y]")</span>
-   <span id="pt-createaccount">[Create
    account](/web/20171031042237/http://wiki.vuze.com/mediawiki/index.php?title=Special:CreateAccount&returnto=Downloading+Rules "You are encouraged to create an account and log in; however, it is not mandatory")</span>
-   <span id="pt-login">[Log
    in](/web/20171031042237/http://wiki.vuze.com/mediawiki/index.php?title=Special:UserLogin&returnto=Downloading+Rules "You are encouraged to log in; however, it is not mandatory [o]")</span>

</div>

<div id="left-navigation">

<div id="p-namespaces" class="vectorTabs" role="navigation"
aria-labelledby="p-namespaces-label">

### Namespaces

-   <span
    id="ca-nstab-main">[Page](/web/20171031042237/http://wiki.vuze.com/w/Downloading_Rules "View the content page [c]")</span>
-   <span
    id="ca-talk">[Discussion](/web/20171031042237/http://wiki.vuze.com/mediawiki/index.php?title=Talk:Downloading_Rules&action=edit&redlink=1 "Discussion about the content page [t]")</span>

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
    id="ca-view">[Read](/web/20171031042237/http://wiki.vuze.com/w/Downloading_Rules)</span>
-   <span
    id="ca-edit">[Edit](/web/20171031042237/http://wiki.vuze.com/mediawiki/index.php?title=Downloading_Rules&action=edit "Edit this page [e]")</span>
-   <span id="ca-history">[View
    history](/web/20171031042237/http://wiki.vuze.com/mediawiki/index.php?title=Downloading_Rules&action=history "Past revisions of this page [h]")</span>

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

<a href="/web/20171031042237/http://wiki.vuze.com/w/Main_Page" class="mw-wiki-logo" title="Visit the main page"></a>

</div>

<div id="p-" class="portal" role="navigation"
aria-labelledby="p--label">

### 

<div class="body">

-   <span id="n-Download-Vuze-Now">[Download Vuze
    Now](https://web.archive.org/web/20171031042237/http://www.vuze.com/download)</span>

</div>

</div>

<div id="p-navigation" class="portal" role="navigation"
aria-labelledby="p-navigation-label">

### Navigation

<div class="body">

-   <span id="n-mainpage-description">[Main
    page](/web/20171031042237/http://wiki.vuze.com/w/Main_Page "Visit the main page [z]")</span>
-   <span id="n-recentchanges">[Recent
    changes](/web/20171031042237/http://wiki.vuze.com/w/Special:RecentChanges "A list of recent changes in the wiki [r]")</span>
-   <span id="n-randompage">[Random
    page](/web/20171031042237/http://wiki.vuze.com/w/Special:Random "Load a random page [x]")</span>
-   <span
    id="n-help">[Help](https://web.archive.org/web/20171031042237/https://www.mediawiki.org/wiki/Special:MyLanguage/Help:Contents "The place to find out")</span>

</div>

</div>

<div id="p-tb" class="portal" role="navigation"
aria-labelledby="p-tb-label">

### Tools

<div class="body">

-   <span id="t-whatlinkshere">[What links
    here](/web/20171031042237/http://wiki.vuze.com/w/Special:WhatLinksHere/Downloading_Rules "A list of all wiki pages that link here [j]")</span>
-   <span id="t-recentchangeslinked">[Related
    changes](/web/20171031042237/http://wiki.vuze.com/w/Special:RecentChangesLinked/Downloading_Rules "Recent changes in pages linked from this page [k]")</span>
-   <span id="t-specialpages">[Special
    pages](/web/20171031042237/http://wiki.vuze.com/w/Special:SpecialPages "A list of all special pages [q]")</span>
-   <span id="t-print">[Printable
    version](/web/20171031042237/http://wiki.vuze.com/mediawiki/index.php?title=Downloading_Rules&printable=yes "Printable version of this page [p]")</span>
-   <span id="t-permalink">[Permanent
    link](/web/20171031042237/http://wiki.vuze.com/mediawiki/index.php?title=Downloading_Rules&oldid=17204 "Permanent link to this revision of the page")</span>
-   <span id="t-info">[Page
    information](/web/20171031042237/http://wiki.vuze.com/mediawiki/index.php?title=Downloading_Rules&action=info "More information about this page")</span>

</div>

</div>

</div>

</div>

<div id="footer" role="contentinfo">

-   <span id="footer-info-lastmod">This page was last modified on 2
    March 2016, at 23:53.</span>
-   <span id="footer-info-viewcount">This page has been accessed 16,518
    times.</span>

<!-- -->

-   <span id="footer-places-about">[About
    VuzeWiki](/web/20171031042237/http://wiki.vuze.com/w/VuzeWiki:About "VuzeWiki:About")</span>
-   <span
    id="footer-places-mobileview"><a href="https://web.archive.org/web/20171031042237/http://wiki.vuze.com/mediawiki/index.php?title=Downloading_Rules&amp;mobileaction=toggle_view_mobile" class="noprint stopMobileRedirectToggle">Mobile view</a></span>

<!-- -->

-   <span
    id="footer-poweredbyico">[<img src="/web/20171031042237im_/http://wiki.vuze.com/mediawiki/resources/assets/poweredby_mediawiki_88x31.png" srcset="/web/20171031042237im_/http://wiki.vuze.com/mediawiki/resources/assets/poweredby_mediawiki_132x47.png 1.5x, /web/20171031042237im_/http://wiki.vuze.com/mediawiki/resources/assets/poweredby_mediawiki_176x62.png 2x" width="88" height="31" alt="Powered by MediaWiki" />](//web.archive.org/web/20171031042237/http://www.mediawiki.org/)</span>
-   <span id="footer-analyticsystemsico">Any use of Vuze® and Vuze+™
    that violates the rights of any person or entity is not allowed.
    [More](https://web.archive.org/web/20171031042237/http://vuze.com/corp/legal.php)</span>

<div style="clear:both">

</div>

</div>
