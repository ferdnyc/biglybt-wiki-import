<div id="mw-page-base" class="noprint">

</div>

<div id="mw-head-base" class="noprint">

</div>

<div id="content" class="mw-body" role="main">

<span id="top"></span>

<div class="mw-indicators">

</div>

# HTTP Seeding

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

HTTP seeding allows content to be delivered via the HTTP protocol.

Through HTTP Seeding (or ***webseeding***), the torrent creator can
specify a ***fallback http:// based url*** from which peers may download
pieces, thus allowing a standard HTTP server to be used for seeding
torrents. This is only useful if you are the original creator however,
and you actually must have a web server serving up the file.

Unless you are an advanced bittorrent user serving up your own torrents,
you should leave this setting ***unchecked*** (the default).

Two forms of seeding are currently defined, the original
<a href="https://web.archive.org/web/20201205001645/http://bittornado.com/docs/webseed-spec.txt" class="external text">webseed</a>
specification and the
<a href="https://web.archive.org/web/20201205001645/http://www.getright.com/seedtorrent.html" class="external text">getright</a>
specification, both of which are supported.

See the
<a href="https://web.archive.org/web/20201205001645/http://wiki.theory.org/BitTorrentSpecification#WebSeeding" class="external text">BitTorrent Specification</a>
for details.

## <span id="webseed" class="mw-headline">webseed</span><span class="mw-editsection"><span class="mw-editsection-bracket">\[</span>[edit](/web/20201205001645/http://wiki.vuze.com/mediawiki/index.php?title=HTTP_Seeding&action=edit&section=1 "Edit section: webseed")<span class="mw-editsection-bracket">\]</span></span>

Content is addressed via a URL of the form

` <url>/webseed?info_hash=<hash>&piece=<piece_number>[&ranges=...]`

## <span id="getright" class="mw-headline">getright</span><span class="mw-editsection"><span class="mw-editsection-bracket">\[</span>[edit](/web/20201205001645/http://wiki.vuze.com/mediawiki/index.php?title=HTTP_Seeding&action=edit&section=2 "Edit section: getright")<span class="mw-editsection-bracket">\]</span></span>

Content is addressed by file name and HTTP range commands used to access
subranges.

For simple torrents with a single file the HTTP seed URL is that of the
file itself.

For multi-file torrents the HTTP seed URL is that of the 'folder' that
contains the files in the torrent.

## <span id="Vuze_as_an_HTTP_Seed" class="mw-headline">Vuze as an HTTP Seed</span><span class="mw-editsection"><span class="mw-editsection-bracket">\[</span>[edit](/web/20201205001645/http://wiki.vuze.com/mediawiki/index.php?title=HTTP_Seeding&action=edit&section=3 "Edit section: Vuze as an HTTP Seed")<span class="mw-editsection-bracket">\]</span></span>

Vuze can itself act as an HTTP seed if you enable the HTTP seeding via
Tools->Options->Connection - see the HTTP section on that page.

When you do this Vuze will start an HTTP server on the specified port
and respond to 'getright' style requests using a file name structure of

<div style="text-align:right; margin-bottom:-37px;">

Copy to Clipboard

</div>

```
http://<host>:<port>/files/<info_hash>/<file_component>[/<file_component>...]
```

info_hash and file_component values are URLEncoded with the ISO-8859-1
character set. UTF-8 is not used as the torrent file format does not
define the character set of file names and therefore a byte encoding is
required.

For example, for the Vuze 'how to video' torrent with hash
'2BD2EDB7226FF7B8C9E32FC0C071356DAAC30EFA' and file name
'Turn_on_device_playback_and_add_devices\[azprefix01750490\].mov'
seeding on Vuze with an IP address of 127.0.0.1 and HTTP seeding port
configured to be port 8080 the HTTP seed URL would be

<div style="text-align:right; margin-bottom:-37px;">

Copy to Clipboard

</div>

```
http://127.0.0.1:8080/files/%2B%D2%ED%B7%22o%F7%B8%C9%E3%2F%C0%C0q5m%AA%C3%0E%FA/Turn_on_device_playback_and_add_devices[azprefix01750490].mov
```

This allows you to create torrents and then seed them over HTTP as well
as via the bittorrent protocol.

</div>

<div class="printfooter">

Retrieved from
"[http://wiki.vuze.com/mediawiki/index.php?title=HTTP_Seeding&oldid=15381](https://web.archive.org/web/20201205001645/http://wiki.vuze.com/mediawiki/index.php?title=HTTP_Seeding&oldid=15381)"

</div>

<div id="catlinks" class="catlinks" mw="interface">

<div id="mw-normal-catlinks" class="mw-normal-catlinks">

[Category](/web/20201205001645/http://wiki.vuze.com/w/Special:Categories "Special:Categories"):

-   [Technical
    Information](/web/20201205001645/http://wiki.vuze.com/w/Category:Technical_Information "Category:Technical Information")

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
    id="pt-anontalk">[Talk](/web/20201205001645/http://wiki.vuze.com/w/Special:MyTalk "Discussion about edits from this IP address [n]")</span>
-   <span
    id="pt-anoncontribs">[Contributions](/web/20201205001645/http://wiki.vuze.com/w/Special:MyContributions "A list of edits made from this IP address [y]")</span>
-   <span id="pt-createaccount">[Create
    account](/web/20201205001645/http://wiki.vuze.com/mediawiki/index.php?title=Special:CreateAccount&returnto=HTTP+Seeding "You are encouraged to create an account and log in; however, it is not mandatory")</span>
-   <span id="pt-login">[Log
    in](/web/20201205001645/http://wiki.vuze.com/mediawiki/index.php?title=Special:UserLogin&returnto=HTTP+Seeding "You are encouraged to log in; however, it is not mandatory [o]")</span>

</div>

<div id="left-navigation">

<div id="p-namespaces" class="vectorTabs" role="navigation"
aria-labelledby="p-namespaces-label">

### Namespaces

-   <span
    id="ca-nstab-main">[Page](/web/20201205001645/http://wiki.vuze.com/w/HTTP_Seeding "View the content page [c]")</span>
-   <span
    id="ca-talk">[Discussion](/web/20201205001645/http://wiki.vuze.com/w/Talk:HTTP_Seeding "Discussion about the content page [t]")</span>

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
    id="ca-view">[Read](/web/20201205001645/http://wiki.vuze.com/w/HTTP_Seeding)</span>
-   <span
    id="ca-edit">[Edit](/web/20201205001645/http://wiki.vuze.com/mediawiki/index.php?title=HTTP_Seeding&action=edit "Edit this page [e]")</span>
-   <span id="ca-history">[View
    history](/web/20201205001645/http://wiki.vuze.com/mediawiki/index.php?title=HTTP_Seeding&action=history "Past revisions of this page [h]")</span>

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

<a href="/web/20201205001645/http://wiki.vuze.com/w/Main_Page" class="mw-wiki-logo" title="Visit the main page"></a>

</div>

<div id="p-" class="portal" role="navigation"
aria-labelledby="p--label">

### 

<div class="body">

-   <span id="n-Download-Vuze-Now">[Download Vuze
    Now](https://web.archive.org/web/20201205001645/http://www.vuze.com/download)</span>

</div>

</div>

<div id="p-navigation" class="portal" role="navigation"
aria-labelledby="p-navigation-label">

### Navigation

<div class="body">

-   <span id="n-mainpage-description">[Main
    page](/web/20201205001645/http://wiki.vuze.com/w/Main_Page "Visit the main page [z]")</span>
-   <span id="n-recentchanges">[Recent
    changes](/web/20201205001645/http://wiki.vuze.com/w/Special:RecentChanges "A list of recent changes in the wiki [r]")</span>
-   <span id="n-randompage">[Random
    page](/web/20201205001645/http://wiki.vuze.com/w/Special:Random "Load a random page [x]")</span>
-   <span
    id="n-help">[Help](https://web.archive.org/web/20201205001645/https://www.mediawiki.org/wiki/Special:MyLanguage/Help:Contents "The place to find out")</span>

</div>

</div>

<div id="p-tb" class="portal" role="navigation"
aria-labelledby="p-tb-label">

### Tools

<div class="body">

-   <span id="t-whatlinkshere">[What links
    here](/web/20201205001645/http://wiki.vuze.com/w/Special:WhatLinksHere/HTTP_Seeding "A list of all wiki pages that link here [j]")</span>
-   <span id="t-recentchangeslinked">[Related
    changes](/web/20201205001645/http://wiki.vuze.com/w/Special:RecentChangesLinked/HTTP_Seeding "Recent changes in pages linked from this page [k]")</span>
-   <span id="t-specialpages">[Special
    pages](/web/20201205001645/http://wiki.vuze.com/w/Special:SpecialPages "A list of all special pages [q]")</span>
-   <span id="t-print">[Printable
    version](/web/20201205001645/http://wiki.vuze.com/mediawiki/index.php?title=HTTP_Seeding&printable=yes "Printable version of this page [p]")</span>
-   <span id="t-permalink">[Permanent
    link](/web/20201205001645/http://wiki.vuze.com/mediawiki/index.php?title=HTTP_Seeding&oldid=15381 "Permanent link to this revision of the page")</span>
-   <span id="t-info">[Page
    information](/web/20201205001645/http://wiki.vuze.com/mediawiki/index.php?title=HTTP_Seeding&action=info "More information about this page")</span>

</div>

</div>

</div>

</div>

<div id="footer" role="contentinfo">

-   <span id="footer-info-lastmod">This page was last modified on 16
    November 2013, at 00:05.</span>
-   <span id="footer-info-viewcount">This page has been accessed 106,085
    times.</span>

<!-- -->

-   <span id="footer-places-about">[About
    VuzeWiki](/web/20201205001645/http://wiki.vuze.com/w/VuzeWiki:About "VuzeWiki:About")</span>
-   <span
    id="footer-places-mobileview"><a href="https://web.archive.org/web/20201205001645/http://wiki.vuze.com/mediawiki/index.php?title=HTTP_Seeding&amp;mobileaction=toggle_view_mobile" class="noprint stopMobileRedirectToggle">Mobile view</a></span>

<!-- -->

-   <span
    id="footer-poweredbyico">[<img src="/web/20201205001645im_/http://wiki.vuze.com/mediawiki/resources/assets/poweredby_mediawiki_88x31.png" srcset="/web/20201205001645im_/http://wiki.vuze.com/mediawiki/resources/assets/poweredby_mediawiki_132x47.png 1.5x, /web/20201205001645im_/http://wiki.vuze.com/mediawiki/resources/assets/poweredby_mediawiki_176x62.png 2x" width="88" height="31" alt="Powered by MediaWiki" />](//web.archive.org/web/20201205001645/http://www.mediawiki.org/)</span>
-   <span id="footer-analyticsystemsico">Any use of Vuze® and Vuze+™
    that violates the rights of any person or entity is not allowed.
    [More](https://web.archive.org/web/20201205001645/http://vuze.com/corp/legal.php)</span>

<div style="clear:both">

</div>

</div>
