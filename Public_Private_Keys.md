<div id="mw-page-base" class="noprint">

</div>

<div id="mw-head-base" class="noprint">

</div>

<div id="content" class="mw-body" role="main">

<span id="top"></span>

<div id="mw-js-message" style="display:none;">

</div>

# <span dir="auto">Keys</span>

<div id="bodyContent">

<div id="siteSub">

From VuzeWiki

</div>

<div id="contentSub">

(Redirected from [Public Private
Keys](/web/20150301131618/http://wiki.vuze.com/mediawiki/index.php?title=Public_Private_Keys&redirect=no "Public Private Keys"))

</div>

<div id="jump-to-nav" class="mw-jump">

Jump to: [navigation](#mw-navigation), [search](#p-search)

</div>

<div id="mw-content-text" class="mw-content-ltr" lang="en" dir="ltr">

<div id="toc" class="toc">

<div id="toctitle">

## Contents

</div>

-   [<span class="tocnumber">1</span> <span class="toctext">I keep
    getting a pop up box asking for an encryption key
    password?</span>](#I_keep_getting_a_pop_up_box_asking_for_an_encryption_key_password.3F)

</div>

Azureus uses public key cryptography to ensure that communication
between friends/buddies is confidential.

Each Azureus install has a separate key pair - a public key and a
private key.

The private key is only ever stored on the local disk of your machine.

The public key can be communicated to the world at large to allow people
to securely communicate with you.

It is important that the private key is kept securely. To this end it is
stored in an encrypted form itself using a password. The management of
this password can be by the user themselves or automatically by the
client (the default). In both cases the private key never leaves your
machine, it is purely the management of the password required to unlock
it for use that differs.

  

## <span id="I_keep_getting_a_pop_up_box_asking_for_an_encryption_key_password.3F" class="mw-headline">I keep getting a pop up box asking for an encryption key password?</span><span class="mw-editsection"><span class="mw-editsection-bracket">\[</span>[edit](/web/20150301131618/http://wiki.vuze.com/mediawiki/index.php?title=Keys&action=edit&section=1 "Edit section: I keep getting a pop up box asking for an encryption key password?")<span class="mw-editsection-bracket">\]</span></span>

Somehow you've managed to set a password for your private key... Short
of remembering the actual password, you can regenerate a new one:

*Tools - Options - Mode*: select *Advanced*

Then go to the *Security* section, and you should see a *Reset (keys)*
button. Click it and confirm the warning. You might be prompted for a
new password. Once you've recreated the Public/Private keys, exit out of
the client and restart it.

</div>

<div class="printfooter">

Retrieved from
"[http://wiki.vuze.com/mediawiki/index.php?title=Keys&oldid=9554](https://web.archive.org/web/20150301131618/http://wiki.vuze.com/mediawiki/index.php?title=Keys&oldid=9554)"

</div>

<div id="catlinks" class="catlinks">

<div id="mw-normal-catlinks" class="mw-normal-catlinks">

[Category](/web/20150301131618/http://wiki.vuze.com/w/Special:Categories "Special:Categories"):

-   [Technical
    Information](/web/20150301131618/http://wiki.vuze.com/w/Category:Technical_Information "Category:Technical Information")

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

-   <span id="pt-createaccount">[Create
    account](/web/20150301131618/http://wiki.vuze.com/mediawiki/index.php?title=Special:UserLogin&returnto=Keys&type=signup)</span>
-   <span id="pt-login">[Log
    in](/web/20150301131618/http://wiki.vuze.com/mediawiki/index.php?title=Special:UserLogin&returnto=Keys "You are encouraged to log in; however, it is not mandatory [o]")</span>

</div>

<div id="left-navigation">

<div id="p-namespaces" class="vectorTabs" role="navigation"
aria-labelledby="p-namespaces-label">

### Namespaces

-   <span
    id="ca-nstab-main">[Page](/web/20150301131618/http://wiki.vuze.com/w/Keys "View the content page [c]")</span>
-   <span
    id="ca-talk">[Discussion](/web/20150301131618/http://wiki.vuze.com/w/Talk:Keys "Discussion about the content page [t]")</span>

</div>

<div id="p-variants" class="vectorMenu emptyPortlet" role="navigation"
aria-labelledby="p-variants-label">

### 

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
    id="ca-view">[Read](/web/20150301131618/http://wiki.vuze.com/w/Keys)</span>
-   <span
    id="ca-edit">[Edit](/web/20150301131618/http://wiki.vuze.com/mediawiki/index.php?title=Keys&action=edit "You can edit this page. Please use the preview button before saving [e]")</span>
-   <span id="ca-history">[View
    history](/web/20150301131618/http://wiki.vuze.com/mediawiki/index.php?title=Keys&action=history "Past revisions of this page [h]")</span>

</div>

<div id="p-cactions" class="vectorMenu emptyPortlet" role="navigation"
aria-labelledby="p-cactions-label">

### Actions[](#)

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

[](/web/20150301131618/http://wiki.vuze.com/w/Main_Page "Visit the main page")

</div>

<div id="p-" class="portal" role="navigation"
aria-labelledby="p--label">

### 

<div class="body">

-   <span id="n-Download-Vuze-Now">[Download Vuze
    Now](https://web.archive.org/web/20150301131618/http://www.vuze.com/download)</span>

</div>

</div>

<div id="p-navigation" class="portal" role="navigation"
aria-labelledby="p-navigation-label">

### Navigation

<div class="body">

-   <span id="n-mainpage-description">[Main
    page](/web/20150301131618/http://wiki.vuze.com/w/Main_Page "Visit the main page [z]")</span>
-   <span id="n-recentchanges">[Recent
    changes](/web/20150301131618/http://wiki.vuze.com/w/Special:RecentChanges "A list of recent changes in the wiki [r]")</span>
-   <span id="n-randompage">[Random
    page](/web/20150301131618/http://wiki.vuze.com/w/Special:Random "Load a random page [x]")</span>
-   <span
    id="n-help">[Help](https://web.archive.org/web/20150301131618/https://www.mediawiki.org/wiki/Special:MyLanguage/Help:Contents "The place to find out")</span>

</div>

</div>

<div id="p-tb" class="portal" role="navigation"
aria-labelledby="p-tb-label">

### Tools

<div class="body">

-   <span id="t-whatlinkshere">[What links
    here](/web/20150301131618/http://wiki.vuze.com/w/Special:WhatLinksHere/Keys "A list of all wiki pages that link here [j]")</span>
-   <span id="t-recentchangeslinked">[Related
    changes](/web/20150301131618/http://wiki.vuze.com/w/Special:RecentChangesLinked/Keys "Recent changes in pages linked from this page [k]")</span>
-   <span id="t-specialpages">[Special
    pages](/web/20150301131618/http://wiki.vuze.com/w/Special:SpecialPages "A list of all special pages [q]")</span>
-   <span id="t-print">[Printable
    version](/web/20150301131618/http://wiki.vuze.com/mediawiki/index.php?title=Keys&printable=yes "Printable version of this page [p]")</span>
-   <span id="t-permalink">[Permanent
    link](/web/20150301131618/http://wiki.vuze.com/mediawiki/index.php?title=Keys&oldid=9554 "Permanent link to this revision of the page")</span>
-   <span id="t-info">[Page
    information](/web/20150301131618/http://wiki.vuze.com/mediawiki/index.php?title=Keys&action=info)</span>

</div>

</div>

</div>

</div>

<div id="footer" role="contentinfo">

-   <span id="footer-info-lastmod">This page was last modified on 28
    October 2010, at 23:32.</span>
-   <span id="footer-info-viewcount">This page has been accessed 66,754
    times.</span>

<!-- -->

-   <span id="footer-places-about">[About
    VuzeWiki](/web/20150301131618/http://wiki.vuze.com/w/VuzeWiki:About "VuzeWiki:About")</span>

<!-- -->

-   <span
    id="footer-poweredbyico">[<img src="/web/20150301131618im_/http://wiki.vuze.com/mediawiki/skins/common/images/poweredby_mediawiki_88x31.png" width="88" height="31" alt="Powered by MediaWiki" />](//web.archive.org/web/20150301131618/http://www.mediawiki.org/)</span>
-   <span id="footer-analyticsystemsico">Any use of Vuze® and Vuze+™
    that violates the rights of any person or entity is not allowed.
    [More](https://web.archive.org/web/20150301131618/http://vuze.com/corp/legal.php)</span>

<div style="clear:both">

</div>

</div>
