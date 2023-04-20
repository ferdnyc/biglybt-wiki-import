<div id="mw-page-base" class="noprint">

</div>

<div id="mw-head-base" class="noprint">

</div>

<div id="content" class="mw-body" role="main">

<span id="top"></span>

<div class="mw-indicators">

</div>

# UPnP

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

<div id="Part_of_Azureus_UG">

<table data-align="center" data-cellspacing="0" data-cellpadding="7" style="width: 360px; font-size: 100%; border-style: solid; border-color: #DDDDDD; border-width: 1px; margin-top: 1px; margin-bottom: 5px; clear: both; position:relative;">
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td style="text-align: right;" style="width: 35px; height: 32px; vertical-align: middle"><a href="/web/20200709111852/http://wiki.vuze.com/w/File:Azureuslogo3ds.gif" class="image"><img src="/web/20200709111852im_/http://wiki.vuze.com/mediawiki/images/3/3f/Azureuslogo3ds.gif" width="32" height="32" alt="Azureuslogo3ds.gif" /></a></td>
<td>This article is a part of the Azureus User Guide.<br />
See <a href="/web/20200709111852/http://wiki.vuze.com/w/UG_Plugins#UPnP" title="UG Plugins">UG_Plugins#UPnP</a></td>
</tr>
</tbody>
</table>

</div>

[Options](/web/20200709111852/http://wiki.vuze.com/w/UG_Options "UG Options")
\>
[Plugins](/web/20200709111852/http://wiki.vuze.com/w/UG_Options#Plugins_options "UG Options")
\> UPnP

UPnP is short for **Universal Plug and Play** - it is a feature that
works with some compatible routers to open the required
[ports](/web/20200709111852/http://wiki.vuze.com/w/Ports "Ports")
automatically. **If Azureus is crashing often, you should try to disable
UPnP in the options!**

Azureus needs to open a connection for the outside world, through a port
in your router. Currently Azureus randomly selects a port at initial
setup (in any case, do not use the port 6881 any more). Let us use port
55321.

We need to tell your router that all that arrives on port 55321 has to
be directed to your machine. UPnP in Azureus can do that for you,
unless:

-   your router doesn't support UPnP. Some routers, even if they are
    compatible with UPnP, have problems with this. In that case you need
    to dive into your router's manual and look up [port
    forwarding](/web/20200709111852/http://wiki.vuze.com/w/Port_forwarding "Port forwarding").
-   someone else on your LAN is already using the port you want to use
    1.  UPnP: Mapping 'Incoming Peer Data Port (TCP/55321)' failed
    2.  UPnP: Mapping 'incoming peer data port (TCP/55321)' has been
        reserved by 192.168.0.50" - please select a different port.
        Choose **another port** in [Options >
        Connection](/web/20200709111852/http://wiki.vuze.com/w/UG_Options#Connection_options "UG Options") >
        Incoming TCP listen port and save.

**If your ISP disconnects you** every 24 hours so that you have to
reconnect (like German Telekom/T-Online) you should **not use UPnP** but
set up [port
forwarding](/web/20200709111852/http://wiki.vuze.com/w/Port_forwarding "Port forwarding")
yourself.

  
The Universal Plug and Play plugin produces various informative
messages. By default these are all enabled. To disable them go to Tools
\>
[Options](/web/20200709111852/http://wiki.vuze.com/w/UG_Options "UG Options")
\>
[Plugins](/web/20200709111852/http://wiki.vuze.com/w/UG_Options#Plugins_options "UG Options")
and select the UPnP plugin. You can now configure the plugin as you
required. To disable the popups you disable the 3 "report ..."
checkboxes.

The informative messages are on by default so that users know that UPnP
is in action.

**Known router problems:**

-   3Com
    1.  ADSL 11g - early firmware versions (earlier than 2.05) don't
        support UPnP.
-   Linksys
    1.  WRT54G v4(/5?) - doesn't do UDP/TCP on same port properly - use
        different ports for the 'Incoming TCP Listen Port' and DDB. Also
        disable the UDP tracker protocol if needed. User has reported
        that with v5 a hard-reset of the router was needed to get things
        working.
    2.  WAG354G - very slow at releasing port mappings on exit. This
        causes Azureus to appear to hang when quit for several minutes.
        Avoid this by configuring Azureus not to release on exit.
-   Netgear
    1.  DG834 - some earlier firmware versions have buggy UPnP
        implementations - try updating the firmware to see if that
        helps.

**Reporting UPnP problems:**

If you experience UPnP problems, then you should have a look at the log
view for the UPnP plugin (Plugins \> Log Views \> UPnP). The information
there will describe how Azureus has tried to set up the appropriate
connections using UPnP. If you need some help understanding what the
messages mean (when things aren't working), copy the text and post it to
the Azureus forums.

If you are asked to get the full UPnP log, you can do this by going to
the UPnP options, and enable the "Output full debug information to log"
setting. Then restart Azureus - the full UPnP debug information will be
printed in the UPnP log view. This setting is only available in v3.0.0.9
and later.

If you have an earlier version of Azureus which does not have this
setting, then follow these steps:

1.  Enable logging in Azureus.
2.  Enable logging to file - choose to save the output somewhere that
    you'll remember.
3.  Deselect \*everything\* for Information, Warning and Error,
    \*except\* "plug".
4.  Close down Azureus.
5.  Delete any log file that already exists in the save file location.
6.  Start up Azureus.
7.  Wait until Azureus has reported UPnP problems.
8.  Take a copy of the log file saved on disk.

That will contain information about other plugins as well, but it will
contain the full log information about everything the UPnP plugin has
tried to do.

  
<span class="small">Read the [Azureus
FAQ](/web/20200709111852/http://wiki.vuze.com/w/Azureus_FAQ "Azureus FAQ")</span>

</div>

<div class="printfooter">

Retrieved from
"[http://wiki.vuze.com/mediawiki/index.php?title=UPnP&oldid=8221](https://web.archive.org/web/20200709111852/http://wiki.vuze.com/mediawiki/index.php?title=UPnP&oldid=8221)"

</div>

<div id="catlinks" class="catlinks" mw="interface">

<div id="mw-normal-catlinks" class="mw-normal-catlinks">

[Categories](/web/20200709111852/http://wiki.vuze.com/w/Special:Categories "Special:Categories"):

-   [User
    Guide](/web/20200709111852/http://wiki.vuze.com/w/Category:User_Guide "Category:User Guide")
-   [Documentation](/web/20200709111852/http://wiki.vuze.com/w/Category:Documentation "Category:Documentation")

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
    id="pt-anontalk">[Talk](/web/20200709111852/http://wiki.vuze.com/w/Special:MyTalk "Discussion about edits from this IP address [n]")</span>
-   <span
    id="pt-anoncontribs">[Contributions](/web/20200709111852/http://wiki.vuze.com/w/Special:MyContributions "A list of edits made from this IP address [y]")</span>
-   <span id="pt-createaccount">[Create
    account](/web/20200709111852/http://wiki.vuze.com/mediawiki/index.php?title=Special:CreateAccount&returnto=UPnP "You are encouraged to create an account and log in; however, it is not mandatory")</span>
-   <span id="pt-login">[Log
    in](/web/20200709111852/http://wiki.vuze.com/mediawiki/index.php?title=Special:UserLogin&returnto=UPnP "You are encouraged to log in; however, it is not mandatory [o]")</span>

</div>

<div id="left-navigation">

<div id="p-namespaces" class="vectorTabs" role="navigation"
aria-labelledby="p-namespaces-label">

### Namespaces

-   <span
    id="ca-nstab-main">[Page](/web/20200709111852/http://wiki.vuze.com/w/UPnP "View the content page [c]")</span>
-   <span
    id="ca-talk">[Discussion](/web/20200709111852/http://wiki.vuze.com/mediawiki/index.php?title=Talk:UPnP&action=edit&redlink=1 "Discussion about the content page [t]")</span>

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
    id="ca-view">[Read](/web/20200709111852/http://wiki.vuze.com/w/UPnP)</span>
-   <span
    id="ca-edit">[Edit](/web/20200709111852/http://wiki.vuze.com/mediawiki/index.php?title=UPnP&action=edit "Edit this page [e]")</span>
-   <span id="ca-history">[View
    history](/web/20200709111852/http://wiki.vuze.com/mediawiki/index.php?title=UPnP&action=history "Past revisions of this page [h]")</span>

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

<a href="/web/20200709111852/http://wiki.vuze.com/w/Main_Page" class="mw-wiki-logo" title="Visit the main page"></a>

</div>

<div id="p-" class="portal" role="navigation"
aria-labelledby="p--label">

### 

<div class="body">

-   <span id="n-Download-Vuze-Now">[Download Vuze
    Now](https://web.archive.org/web/20200709111852/http://www.vuze.com/download)</span>

</div>

</div>

<div id="p-navigation" class="portal" role="navigation"
aria-labelledby="p-navigation-label">

### Navigation

<div class="body">

-   <span id="n-mainpage-description">[Main
    page](/web/20200709111852/http://wiki.vuze.com/w/Main_Page "Visit the main page [z]")</span>
-   <span id="n-recentchanges">[Recent
    changes](/web/20200709111852/http://wiki.vuze.com/w/Special:RecentChanges "A list of recent changes in the wiki [r]")</span>
-   <span id="n-randompage">[Random
    page](/web/20200709111852/http://wiki.vuze.com/w/Special:Random "Load a random page [x]")</span>
-   <span
    id="n-help">[Help](https://web.archive.org/web/20200709111852/https://www.mediawiki.org/wiki/Special:MyLanguage/Help:Contents "The place to find out")</span>

</div>

</div>

<div id="p-tb" class="portal" role="navigation"
aria-labelledby="p-tb-label">

### Tools

<div class="body">

-   <span id="t-whatlinkshere">[What links
    here](/web/20200709111852/http://wiki.vuze.com/w/Special:WhatLinksHere/UPnP "A list of all wiki pages that link here [j]")</span>
-   <span id="t-recentchangeslinked">[Related
    changes](/web/20200709111852/http://wiki.vuze.com/w/Special:RecentChangesLinked/UPnP "Recent changes in pages linked from this page [k]")</span>
-   <span id="t-specialpages">[Special
    pages](/web/20200709111852/http://wiki.vuze.com/w/Special:SpecialPages "A list of all special pages [q]")</span>
-   <span id="t-print">[Printable
    version](/web/20200709111852/http://wiki.vuze.com/mediawiki/index.php?title=UPnP&printable=yes "Printable version of this page [p]")</span>
-   <span id="t-permalink">[Permanent
    link](/web/20200709111852/http://wiki.vuze.com/mediawiki/index.php?title=UPnP&oldid=8221 "Permanent link to this revision of the page")</span>
-   <span id="t-info">[Page
    information](/web/20200709111852/http://wiki.vuze.com/mediawiki/index.php?title=UPnP&action=info "More information about this page")</span>

</div>

</div>

</div>

</div>

<div id="footer" role="contentinfo">

-   <span id="footer-info-lastmod">This page was last modified on 6
    March 2010, at 14:40.</span>
-   <span id="footer-info-viewcount">This page has been accessed 47,571
    times.</span>

<!-- -->

-   <span id="footer-places-about">[About
    VuzeWiki](/web/20200709111852/http://wiki.vuze.com/w/VuzeWiki:About "VuzeWiki:About")</span>
-   <span
    id="footer-places-mobileview"><a href="https://web.archive.org/web/20200709111852/http://wiki.vuze.com/mediawiki/index.php?title=UPnP&amp;mobileaction=toggle_view_mobile" class="noprint stopMobileRedirectToggle">Mobile view</a></span>

<!-- -->

-   <span
    id="footer-poweredbyico">[<img src="/web/20200709111852im_/http://wiki.vuze.com/mediawiki/resources/assets/poweredby_mediawiki_88x31.png" srcset="/web/20200709111852im_/http://wiki.vuze.com/mediawiki/resources/assets/poweredby_mediawiki_132x47.png 1.5x, /web/20200709111852im_/http://wiki.vuze.com/mediawiki/resources/assets/poweredby_mediawiki_176x62.png 2x" width="88" height="31" alt="Powered by MediaWiki" />](//web.archive.org/web/20200709111852/http://www.mediawiki.org/)</span>
-   <span id="footer-analyticsystemsico">Any use of Vuze® and Vuze+™
    that violates the rights of any person or entity is not allowed.
    [More](https://web.archive.org/web/20200709111852/http://vuze.com/corp/legal.php)</span>

<div style="clear:both">

</div>

</div>
