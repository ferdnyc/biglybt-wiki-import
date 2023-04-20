<div id="mw-page-base" class="noprint">

</div>

<div id="mw-head-base" class="noprint">

</div>

<div id="content" class="mw-body" role="main">

<span id="top"></span>

<div class="mw-indicators">

</div>

# Auto Speed

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

<div
style="border:#0a0 1px solid;background-color:#ffc0c0;padding:0px 3px;margin-top:10px;">

**Note: You should avoid using the old Auto Speed plugin, as it has been
replaced by the built-in features.** If you still have the plugin
installed, please uninstall it.

</div>

  

## <span id="Built-in_Auto-Speed" class="mw-headline">Built-in Auto-Speed</span><span class="mw-editsection"><span class="mw-editsection-bracket">\[</span>[edit](/web/20170911212105/http://wiki.vuze.com/mediawiki/index.php?title=Auto_Speed&action=edit&section=1 "Edit section: Built-in Auto-Speed")<span class="mw-editsection-bracket">\]</span></span>

The built-in Auto-speed feature attempts to match Azureus' upload speed
with your network connection's current traffic to avoid overloading it.
Auto-Speed settings are located at [Options \> Transfer \>
Auto-Speed](/web/20170911212105/http://wiki.vuze.com/w/UG_Options#Auto-Speed "UG Options")
in Vuze's options.

If Auto-Speed is enabled, the current speed limits is shown in brackets
on the Status bar, and an asterisk '\*' indicates that Auto-Speed is
active. In the following example, there is 91K = 91 kB/s in brackets as
the upload limit, and the current upload speed is 91.0 kB/s. (In the
example there is also a fixed 1050K limit for download speed.)

<a href="/web/20170911212105/http://wiki.vuze.com/w/File:Vuze43ShareRatioIndicator.png" class="image"><img src="/web/20170911212105im_/http://wiki.vuze.com/mediawiki/images/0/0c/Vuze43ShareRatioIndicator.png" width="619" height="103" alt="Vuze43ShareRatioIndicator.png" /></a>

  
Azureus contains currently two built-in Auto-speed logics: 'Classic' and
'Beta'

### <span id="Auto-Speed_Classic" class="mw-headline">Auto-Speed Classic</span><span class="mw-editsection"><span class="mw-editsection-bracket">\[</span>[edit](/web/20170911212105/http://wiki.vuze.com/mediawiki/index.php?title=Auto_Speed&action=edit&section=2 "Edit section: Auto-Speed Classic")<span class="mw-editsection-bracket">\]</span></span>

It works by selecting a number of other Azureus instances from the
Distributed Database as ping targets. It then periodically pings these
to obtain an average latency for your connection. In order to baseline
these pings Azureus needs a period during which little network activity
occurs. If this doesn't happen naturally within a period after startup
it will temporarily force the upload limit to a very low value to obtain
the baseline (it may repeat this at other times when the ping targets
change)

Once a baseline ping time is available, auto-speed adjusts the upload
speed based on the observed difference between the current ping time and
the baseline.

There are many different types of connection with very different
characteristics. Unfortunately auto-speed is currently not clever enough
to optimise its behaviour for all scenarios automatically so you may
need to adjust its parameters to maximise its effectiveness. To do this
you need to change the 'Mode' to 'Advanced' in the options.

The three main parameters of interest are the increase/decrease amounts
and the 'choking ping'. The first two affect how quickly auto-speed
changes Azureus' upload setting in response to ping latency changes. The
third is the latency that Azureus will consider as an absolute indicator
of choking (although it also considers an additional factor based on the
measured baseline ping time). By setting a rather low latency limit, you
can make Azureus very responsive to network congestion.

### <span id="Auto-Speed_Beta" class="mw-headline">Auto-Speed Beta</span><span class="mw-editsection"><span class="mw-editsection-bracket">\[</span>[edit](/web/20170911212105/http://wiki.vuze.com/mediawiki/index.php?title=Auto_Speed&action=edit&section=3 "Edit section: Auto-Speed Beta")<span class="mw-editsection-bracket">\]</span></span>

Documentation about the alternative [Auto-Speed
Beta](/web/20170911212105/http://wiki.vuze.com/w/Auto_Speed_Beta "Auto Speed Beta")
functionality.

</div>

<div class="printfooter">

Retrieved from
"[http://wiki.vuze.com/mediawiki/index.php?title=Auto_Speed&oldid=13481](https://web.archive.org/web/20170911212105/http://wiki.vuze.com/mediawiki/index.php?title=Auto_Speed&oldid=13481)"

</div>

<div id="catlinks" class="catlinks" mw="interface">

<div id="mw-normal-catlinks" class="mw-normal-catlinks">

[Categories](/web/20170911212105/http://wiki.vuze.com/w/Special:Categories "Special:Categories"):

-   [Technical
    Information](/web/20170911212105/http://wiki.vuze.com/w/Category:Technical_Information "Category:Technical Information")
-   [Documentation](/web/20170911212105/http://wiki.vuze.com/w/Category:Documentation "Category:Documentation")

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
    id="pt-anontalk">[Talk](/web/20170911212105/http://wiki.vuze.com/w/Special:MyTalk "Discussion about edits from this IP address [n]")</span>
-   <span
    id="pt-anoncontribs">[Contributions](/web/20170911212105/http://wiki.vuze.com/w/Special:MyContributions "A list of edits made from this IP address [y]")</span>
-   <span id="pt-createaccount">[Create
    account](/web/20170911212105/http://wiki.vuze.com/mediawiki/index.php?title=Special:CreateAccount&returnto=Auto+Speed "You are encouraged to create an account and log in; however, it is not mandatory")</span>
-   <span id="pt-login">[Log
    in](/web/20170911212105/http://wiki.vuze.com/mediawiki/index.php?title=Special:UserLogin&returnto=Auto+Speed "You are encouraged to log in; however, it is not mandatory [o]")</span>

</div>

<div id="left-navigation">

<div id="p-namespaces" class="vectorTabs" role="navigation"
aria-labelledby="p-namespaces-label">

### Namespaces

-   <span
    id="ca-nstab-main">[Page](/web/20170911212105/http://wiki.vuze.com/w/Auto_Speed "View the content page [c]")</span>
-   <span
    id="ca-talk">[Discussion](/web/20170911212105/http://wiki.vuze.com/mediawiki/index.php?title=Talk:Auto_Speed&action=edit&redlink=1 "Discussion about the content page [t]")</span>

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
    id="ca-view">[Read](/web/20170911212105/http://wiki.vuze.com/w/Auto_Speed)</span>
-   <span
    id="ca-edit">[Edit](/web/20170911212105/http://wiki.vuze.com/mediawiki/index.php?title=Auto_Speed&action=edit "Edit this page [e]")</span>
-   <span id="ca-history">[View
    history](/web/20170911212105/http://wiki.vuze.com/mediawiki/index.php?title=Auto_Speed&action=history "Past revisions of this page [h]")</span>

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

<a href="/web/20170911212105/http://wiki.vuze.com/w/Main_Page" class="mw-wiki-logo" title="Visit the main page"></a>

</div>

<div id="p-" class="portal" role="navigation"
aria-labelledby="p--label">

### 

<div class="body">

-   <span id="n-Download-Vuze-Now">[Download Vuze
    Now](https://web.archive.org/web/20170911212105/http://www.vuze.com/download)</span>

</div>

</div>

<div id="p-navigation" class="portal" role="navigation"
aria-labelledby="p-navigation-label">

### Navigation

<div class="body">

-   <span id="n-mainpage-description">[Main
    page](/web/20170911212105/http://wiki.vuze.com/w/Main_Page "Visit the main page [z]")</span>
-   <span id="n-recentchanges">[Recent
    changes](/web/20170911212105/http://wiki.vuze.com/w/Special:RecentChanges "A list of recent changes in the wiki [r]")</span>
-   <span id="n-randompage">[Random
    page](/web/20170911212105/http://wiki.vuze.com/w/Special:Random "Load a random page [x]")</span>
-   <span
    id="n-help">[Help](https://web.archive.org/web/20170911212105/https://www.mediawiki.org/wiki/Special:MyLanguage/Help:Contents "The place to find out")</span>

</div>

</div>

<div id="p-tb" class="portal" role="navigation"
aria-labelledby="p-tb-label">

### Tools

<div class="body">

-   <span id="t-whatlinkshere">[What links
    here](/web/20170911212105/http://wiki.vuze.com/w/Special:WhatLinksHere/Auto_Speed "A list of all wiki pages that link here [j]")</span>
-   <span id="t-recentchangeslinked">[Related
    changes](/web/20170911212105/http://wiki.vuze.com/w/Special:RecentChangesLinked/Auto_Speed "Recent changes in pages linked from this page [k]")</span>
-   <span id="t-specialpages">[Special
    pages](/web/20170911212105/http://wiki.vuze.com/w/Special:SpecialPages "A list of all special pages [q]")</span>
-   <span id="t-print">[Printable
    version](/web/20170911212105/http://wiki.vuze.com/mediawiki/index.php?title=Auto_Speed&printable=yes "Printable version of this page [p]")</span>
-   <span id="t-permalink">[Permanent
    link](/web/20170911212105/http://wiki.vuze.com/mediawiki/index.php?title=Auto_Speed&oldid=13481 "Permanent link to this revision of the page")</span>
-   <span id="t-info">[Page
    information](/web/20170911212105/http://wiki.vuze.com/mediawiki/index.php?title=Auto_Speed&action=info "More information about this page")</span>

</div>

</div>

</div>

</div>

<div id="footer" role="contentinfo">

-   <span id="footer-info-lastmod">This page was last modified on 5 May
    2012, at 07:08.</span>
-   <span id="footer-info-viewcount">This page has been accessed 23,570
    times.</span>

<!-- -->

-   <span id="footer-places-about">[About
    VuzeWiki](/web/20170911212105/http://wiki.vuze.com/w/VuzeWiki:About "VuzeWiki:About")</span>
-   <span
    id="footer-places-mobileview"><a href="https://web.archive.org/web/20170911212105/http://wiki.vuze.com/mediawiki/index.php?title=Auto_Speed&amp;mobileaction=toggle_view_mobile" class="noprint stopMobileRedirectToggle">Mobile view</a></span>

<!-- -->

-   <span
    id="footer-poweredbyico">[<img src="/web/20170911212105im_/http://wiki.vuze.com/mediawiki/resources/assets/poweredby_mediawiki_88x31.png" srcset="/web/20170911212105im_/http://wiki.vuze.com/mediawiki/resources/assets/poweredby_mediawiki_132x47.png 1.5x, /web/20170911212105im_/http://wiki.vuze.com/mediawiki/resources/assets/poweredby_mediawiki_176x62.png 2x" width="88" height="31" alt="Powered by MediaWiki" />](//web.archive.org/web/20170911212105/http://www.mediawiki.org/)</span>
-   <span id="footer-analyticsystemsico">Any use of Vuze® and Vuze+™
    that violates the rights of any person or entity is not allowed.
    [More](https://web.archive.org/web/20170911212105/http://vuze.com/corp/legal.php)</span>

<div style="clear:both">

</div>

</div>
