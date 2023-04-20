<div id="mw-page-base" class="noprint">

</div>

<div id="mw-head-base" class="noprint">

</div>

<div id="content" class="mw-body" role="main">

<span id="top"></span>

<div class="mw-indicators">

</div>

# Backup And Restore

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

Since version 4.7.0.3 Vuze has included a backup-and-restore feature for
configuration data (everything that Vuze uses internally to manage
configuration settings, subscriptions, devices etc). This does not
include anything external such as the downloaded data itself, torrents
stored outside of the standard Vuze configuration directory, transcoded
files etc. as these are in general large and require specialist backup.

As such it provides a good mechanism to recover from configuration data
corruption (a rare occurrence but very annoying when it happens) and it
can also be used to migrate configuration data from one location to
another as the restore action will update any absolute paths in the
configuration data.

## <span id="Migrating_Vuze_using_this_feature" class="mw-headline">Migrating Vuze using this feature</span><span class="mw-editsection"><span class="mw-editsection-bracket">\[</span>[edit](/web/20170419125545/http://wiki.vuze.com/mediawiki/index.php?title=Backup_And_Restore&action=edit&section=1 "Edit section: Migrating Vuze using this feature")<span class="mw-editsection-bracket">\]</span></span>

On the original computer use 'backup' to backup the configuration

On the new computer install Vuze as required

On the new computer ensure that the 'Vuze Downloads' directory is
populated with exactly the same files as the original computer (i.e.
either copy them across or mount them identically if on a shared drive)

On the new computer use 'restore' to restore Vuze's configuration from
the one you backed-up.

## <span id="Warning" class="mw-headline">Warning</span><span class="mw-editsection"><span class="mw-editsection-bracket">\[</span>[edit](/web/20170419125545/http://wiki.vuze.com/mediawiki/index.php?title=Backup_And_Restore&action=edit&section=2 "Edit section: Warning")<span class="mw-editsection-bracket">\]</span></span>

**In versions prior to 4.7.2.0 there is a bug whereby if you select the
backup location to be within Vuze's config directory the process gets in
a loop and will recursively use up all your filestore - see
<a href="https://web.archive.org/web/20170419125545/http://forum.vuze.com/thread.jspa?threadID=111723" class="external free">http://forum.vuze.com/thread.jspa?threadID=111723</a>
so don't!!!**

</div>

<div class="printfooter">

Retrieved from
"[http://wiki.vuze.com/mediawiki/index.php?title=Backup_And_Restore&oldid=14735](https://web.archive.org/web/20170419125545/http://wiki.vuze.com/mediawiki/index.php?title=Backup_And_Restore&oldid=14735)"

</div>

<div id="catlinks" class="catlinks catlinks-allhidden" mw="interface">

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
    id="pt-anontalk">[Talk](/web/20170419125545/http://wiki.vuze.com/w/Special:MyTalk "Discussion about edits from this IP address [n]")</span>
-   <span
    id="pt-anoncontribs">[Contributions](/web/20170419125545/http://wiki.vuze.com/w/Special:MyContributions "A list of edits made from this IP address [y]")</span>
-   <span id="pt-createaccount">[Create
    account](/web/20170419125545/http://wiki.vuze.com/mediawiki/index.php?title=Special:CreateAccount&returnto=Backup+And+Restore "You are encouraged to create an account and log in; however, it is not mandatory")</span>
-   <span id="pt-login">[Log
    in](/web/20170419125545/http://wiki.vuze.com/mediawiki/index.php?title=Special:UserLogin&returnto=Backup+And+Restore "You are encouraged to log in; however, it is not mandatory [o]")</span>

</div>

<div id="left-navigation">

<div id="p-namespaces" class="vectorTabs" role="navigation"
aria-labelledby="p-namespaces-label">

### Namespaces

-   <span
    id="ca-nstab-main">[Page](/web/20170419125545/http://wiki.vuze.com/w/Backup_And_Restore "View the content page [c]")</span>
-   <span
    id="ca-talk">[Discussion](/web/20170419125545/http://wiki.vuze.com/mediawiki/index.php?title=Talk:Backup_And_Restore&action=edit&redlink=1 "Discussion about the content page [t]")</span>

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
    id="ca-view">[Read](/web/20170419125545/http://wiki.vuze.com/w/Backup_And_Restore)</span>
-   <span
    id="ca-edit">[Edit](/web/20170419125545/http://wiki.vuze.com/mediawiki/index.php?title=Backup_And_Restore&action=edit "Edit this page [e]")</span>
-   <span id="ca-history">[View
    history](/web/20170419125545/http://wiki.vuze.com/mediawiki/index.php?title=Backup_And_Restore&action=history "Past revisions of this page [h]")</span>

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

<a href="/web/20170419125545/http://wiki.vuze.com/w/Main_Page" class="mw-wiki-logo" title="Visit the main page"></a>

</div>

<div id="p-" class="portal" role="navigation"
aria-labelledby="p--label">

### 

<div class="body">

-   <span id="n-Download-Vuze-Now">[Download Vuze
    Now](https://web.archive.org/web/20170419125545/http://www.vuze.com/download)</span>

</div>

</div>

<div id="p-navigation" class="portal" role="navigation"
aria-labelledby="p-navigation-label">

### Navigation

<div class="body">

-   <span id="n-mainpage-description">[Main
    page](/web/20170419125545/http://wiki.vuze.com/w/Main_Page "Visit the main page [z]")</span>
-   <span id="n-recentchanges">[Recent
    changes](/web/20170419125545/http://wiki.vuze.com/w/Special:RecentChanges "A list of recent changes in the wiki [r]")</span>
-   <span id="n-randompage">[Random
    page](/web/20170419125545/http://wiki.vuze.com/w/Special:Random "Load a random page [x]")</span>
-   <span
    id="n-help">[Help](https://web.archive.org/web/20170419125545/https://www.mediawiki.org/wiki/Special:MyLanguage/Help:Contents "The place to find out")</span>

</div>

</div>

<div id="p-tb" class="portal" role="navigation"
aria-labelledby="p-tb-label">

### Tools

<div class="body">

-   <span id="t-whatlinkshere">[What links
    here](/web/20170419125545/http://wiki.vuze.com/w/Special:WhatLinksHere/Backup_And_Restore "A list of all wiki pages that link here [j]")</span>
-   <span id="t-recentchangeslinked">[Related
    changes](/web/20170419125545/http://wiki.vuze.com/w/Special:RecentChangesLinked/Backup_And_Restore "Recent changes in pages linked from this page [k]")</span>
-   <span id="t-specialpages">[Special
    pages](/web/20170419125545/http://wiki.vuze.com/w/Special:SpecialPages "A list of all special pages [q]")</span>
-   <span id="t-print">[Printable
    version](/web/20170419125545/http://wiki.vuze.com/mediawiki/index.php?title=Backup_And_Restore&printable=yes "Printable version of this page [p]")</span>
-   <span id="t-permalink">[Permanent
    link](/web/20170419125545/http://wiki.vuze.com/mediawiki/index.php?title=Backup_And_Restore&oldid=14735 "Permanent link to this revision of the page")</span>
-   <span id="t-info">[Page
    information](/web/20170419125545/http://wiki.vuze.com/mediawiki/index.php?title=Backup_And_Restore&action=info "More information about this page")</span>

</div>

</div>

</div>

</div>

<div id="footer" role="contentinfo">

-   <span id="footer-info-lastmod">This page was last modified on 20
    September 2012, at 01:10.</span>
-   <span id="footer-info-viewcount">This page has been accessed 7,908
    times.</span>

<!-- -->

-   <span id="footer-places-about">[About
    VuzeWiki](/web/20170419125545/http://wiki.vuze.com/w/VuzeWiki:About "VuzeWiki:About")</span>
-   <span
    id="footer-places-mobileview"><a href="https://web.archive.org/web/20170419125545/http://wiki.vuze.com/mediawiki/index.php?title=Backup_And_Restore&amp;mobileaction=toggle_view_mobile" class="noprint stopMobileRedirectToggle">Mobile view</a></span>

<!-- -->

-   <span
    id="footer-poweredbyico">[<img src="/web/20170419125545im_/http://wiki.vuze.com/mediawiki/resources/assets/poweredby_mediawiki_88x31.png" srcset="/web/20170419125545im_/http://wiki.vuze.com/mediawiki/resources/assets/poweredby_mediawiki_132x47.png 1.5x, /web/20170419125545im_/http://wiki.vuze.com/mediawiki/resources/assets/poweredby_mediawiki_176x62.png 2x" width="88" height="31" alt="Powered by MediaWiki" />](//web.archive.org/web/20170419125545/http://www.mediawiki.org/)</span>
-   <span id="footer-analyticsystemsico">Any use of Vuze® and Vuze+™
    that violates the rights of any person or entity is not allowed.
    [More](https://web.archive.org/web/20170419125545/http://vuze.com/corp/legal.php)</span>

<div style="clear:both">

</div>

</div>
