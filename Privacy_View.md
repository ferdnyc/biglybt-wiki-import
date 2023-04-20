<div id="mw-page-base" class="noprint">

</div>

<div id="mw-head-base" class="noprint">

</div>

<div id="content" class="mw-body" role="main">

<span id="top"></span>

<div class="mw-indicators">

</div>

# Privacy View

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

The Privacy View was introduced in Vuze 5.6.1.3 to gather together the
various settings that control the privacy aspects of a download.

<div id="toc" class="toc">

<div id="toctitle">

## Contents

</div>

-   [<span class="tocnumber">1</span> <span
    class="toctext">Introduction</span>](#Introduction)
-   [<span class="tocnumber">2</span> <span class="toctext">Privacy
    Level</span>](#Privacy_Level)
-   [<span class="tocnumber">3</span> <span
    class="toctext">Networks</span>](#Networks)
    -   [<span class="tocnumber">3.1</span> <span class="toctext">Public
        Internet</span>](#Public_Internet)
    -   [<span class="tocnumber">3.2</span> <span
        class="toctext">I2P</span>](#I2P)
    -   [<span class="tocnumber">3.3</span> <span
        class="toctext">Tor</span>](#Tor)
-   [<span class="tocnumber">4</span> <span class="toctext">I2P Peer
    Lookup</span>](#I2P_Peer_Lookup)
-   [<span class="tocnumber">5</span> <span class="toctext">Changing
    Network Selection</span>](#Changing_Network_Selection)
-   [<span class="tocnumber">6</span> <span class="toctext">Other
    Settings</span>](#Other_Settings)
    -   [<span class="tocnumber">6.1</span> <span class="toctext">Peer
        Sources</span>](#Peer_Sources)
    -   [<span class="tocnumber">6.2</span> <span class="toctext">IP
        Filter</span>](#IP_Filter)
    -   [<span class="tocnumber">6.3</span> <span
        class="toctext">VPN/Proxies</span>](#VPN.2FProxies)

</div>

## <span id="Introduction" class="mw-headline">Introduction</span>

The Privacy View can be selected via the sub-tabs section in the Library
view:

<a href="/web/20200117223417/http://wiki.vuze.com/w/File:Privacy_View.png" class="image"><img src="/web/20200117223417im_/http://wiki.vuze.com/mediawiki/images/1/1c/Privacy_View.png" width="838" height="517" alt="Privacy View.png" /></a>

If you are interested in controlling the networks that a download uses
then make sure you read and understand the 'changing network selection'
section below - one particular consequence of this is that you will want
to either set the enabled networks in the 'torrent options dialog', when
adding the download, or ensure that you add the torrent in a 'stopped'
state (there is a 'privacy' button in the options dialog to simplify
this). If you add a download in a running state and then adjust network
settings then you will encounter the privacy issues associated with the
change of settings.

If you are not consistently seeing the 'torrent options dialog' when
adding a download then check the setting under

Tools->Options->Files: when opening a torrent, show options dialog

## <span id="Privacy_Level" class="mw-headline">Privacy Level</span>

The 'privacy level' slider allows you to change the networks enabled for
a download in a straight forward fashion - the actual networks can be
explicitly enabled/disabled by the checkboxes to the right of the slider
if desired. Below the slider some information is shown regarding how the
privacy level affects which trackers are active (both direct http(s)/udp
trackers as well as decentralized tracking), how webseeds are affected
and also, when the download is running, which networks connected peers
belong to.

-   Public Only

All download activities will occur over the public internet

-   Public/Anonymous Mixing

If you have installed I2P and are downloading/seeding torrents via the
public internet then running them as a mix between public and I2P is a
great way to help out other users that have a censored public internet.
The 'Public/I2P mix' destination will be used for connections.

While they may be unable to connect to the torrent publicly there is the
opportunity for them to connect anonymously and successfully download.

By using [Peer
Sets](/web/20200117223417/http://wiki.vuze.com/w/Speed_Limit_Scheduler#IP.2FPeer_Sets "Speed Limit Scheduler")
is it also possible to configure things so that, for example,
downloading occurs from both the public and I2P but uploading only
occurs via I2P.

-   Anonymous Only

All download activities will occur over I2P and/or Tor - the 'I2P Only'
destination will be used for connections.

-   Invalid

This denotes the state where no networks are enabled

## <span id="Networks" class="mw-headline">Networks</span>

### <span id="Public_Internet" class="mw-headline">Public Internet</span>

This is the IPv4/IPv6 internet you know and love and use everyday for
updating you Facebook status and watching cat videos. Privacy conscious
users may well use a [VPN or
Proxy](/web/20200117223417/http://wiki.vuze.com/w/Proxies_And_VPNs "Proxies And VPNs")
service to provide a level of privacy - these are centralized services
run by organisations who may log your actions and also likely charge you
for the pleasure.

### <span id="I2P" class="mw-headline">I2P</span>

<a href="/web/20200117223417/http://wiki.vuze.com/w/I2P" class="mw-redirect" title="I2P">I2P</a>
is an anonymous overlay network that is P2P friendly.

-   I2P destinations/addresses

I2P uses anonymous destinations to identify peers. Within Vuze you
actually have multiple separate destinations to separate and decouple
activity. In particular there are two addresses used for torrent
download. One is used for torrents that have both the public and I2P
networks enabled. The other is used for downloads that are purely I2P.

By default Vuze will change your I2P destinations on a weekly basis
(when Vuze starts) - you can change the frequency of this, or force an
explicit change, via the I2P settings.

### <span id="Tor" class="mw-headline">Tor</span>

[Tor](/web/20200117223417/http://wiki.vuze.com/w/Tor_HowTo "Tor HowTo")
is not P2P friendly and as such should only be used for non-bulk
transfer operations such as Trackers and to provide an
alternative/indirect method for accessing the internet to circumvent
censorship.

## <span id="I2P_Peer_Lookup" class="mw-headline">I2P Peer Lookup</span>

The ability to explicitly search for decentralized I2P peers is useful
when you add a public download and want to check to see if it can be
downloaded anonymously as well.

Note that if the peer lookup fails to find any I2P peers this does not
in general mean that it will be impossible to download via I2P as there
may be peers with the download in a queued state that will start seeding
to you once you appear in the swarm. You can always run the download
anonymously for a while (say 30 minutes) and see how things work out. If
no peers appear then you can consider switching to public downloading.

Note that the default bandwidth available for I2P peers is **low**, you
will need to increase this if you want to achieve reasonable anonymous
download rates.

## <span id="Changing_Network_Selection" class="mw-headline">Changing Network Selection</span>

It is important to understand the implications of changing a download's
network selection between one of the public selections and an anonymous
one - doing so can allow an observer to correlate your public and
anonymous activity and therefore de-anonymize you. This is particularly
evident for incomplete downloads as your current download completion
state can be an effective fingerprint.

Consider the bitfield of an example download at a point in time,
viewable on the General tab:

<a href="/web/20200117223417/http://wiki.vuze.com/w/File:Privacy_BitField.png" class="image"><img src="/web/20200117223417im_/http://wiki.vuze.com/mediawiki/images/6/63/Privacy_BitField.png" width="1005" height="31" alt="Privacy BitField.png" /></a>

Say you are downloading via the public internet and your IP address is
1.2.3.4 - other connected peers will see your bitfield against IP
address 1.2.3.4. Now you switch to anonymous downloading (disconnecting
all publicly connected peers) - if you happen to anonymously connect to
one of the peers you were previously connected to they will see pretty
much the same bitfield (with the addition of any subsequent downloaded
pieces) against your anonymous address (e.g.
hjtixkqcqppqplpihh4eztp7gitxo5yyibkngkvfq35eh4ug4zxa.b32.i2p). The peer
can now be fairly confident that the two addresses represent the same
peer (assuming that the swarm has the usual relatively random
distribution of peer completion states).

Likewise, if you are downloading purely anonymously and switch to a
mixed state, this will switch you from using your purely anonymous I2P
address to using your separate 'mixed network' I2P address along with
your public address, thus allowing correlation between all three
addresses.

To mitigate against this you need to carefully consider making such
changes to downloads that have started downloading (prior to actually
starting the download changes can be safely made as no information has
leaked to the swarm). If the download is incomplete then the safest
thing would be to completely remove the download from Vuze (and delete
any existing downloaded files), re-add it with the new network selection
and start over. If the download is complete, and the swarm is active and
has a lot of other seeds, then you may decide that switching networks
presents an acceptable risk.

## <span id="Other_Settings" class="mw-headline">Other Settings</span>

### <span id="Peer_Sources" class="mw-headline">Peer Sources</span>

You can control the ways that peers are located and how connections are
established by using the Peer Sources selection. For example, to disable
'peer exchange' as a means of finding peers uncheck the 'supplied by
another peer' option.

### <span id="IP_Filter" class="mw-headline">IP Filter</span>

If you have setup an overall [IP
filter](/web/20200117223417/http://wiki.vuze.com/w/UG_Options#IP_Filters_options "UG Options")
to filter peers connections based on IP address, this can be
enabled/disabled on a per-download basis.

### <span id="VPN.2FProxies" class="mw-headline">VPN/Proxies</span>

For convenience the globally detected VPN and Proxy status is shown -
this is not currently a download specific view.

</div>

<div class="printfooter">

Retrieved from
"[http://wiki.vuze.com/mediawiki/index.php?title=Privacy_View&oldid=16761](https://web.archive.org/web/20200117223417/http://wiki.vuze.com/mediawiki/index.php?title=Privacy_View&oldid=16761)"

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
    id="pt-anontalk">[Talk](/web/20200117223417/http://wiki.vuze.com/w/Special:MyTalk "Discussion about edits from this IP address [n]")</span>
-   <span
    id="pt-anoncontribs">[Contributions](/web/20200117223417/http://wiki.vuze.com/w/Special:MyContributions "A list of edits made from this IP address [y]")</span>
-   <span id="pt-createaccount">[Create
    account](/web/20200117223417/http://wiki.vuze.com/mediawiki/index.php?title=Special:CreateAccount&returnto=Privacy+View "You are encouraged to create an account and log in; however, it is not mandatory")</span>
-   <span id="pt-login">[Log
    in](/web/20200117223417/http://wiki.vuze.com/mediawiki/index.php?title=Special:UserLogin&returnto=Privacy+View "You are encouraged to log in; however, it is not mandatory [o]")</span>

</div>

<div id="left-navigation">

<div id="p-namespaces" class="vectorTabs" role="navigation"
aria-labelledby="p-namespaces-label">

### Namespaces

-   <span
    id="ca-nstab-main">[Page](/web/20200117223417/http://wiki.vuze.com/w/Privacy_View "View the content page [c]")</span>
-   <span
    id="ca-talk">[Discussion](/web/20200117223417/http://wiki.vuze.com/mediawiki/index.php?title=Talk:Privacy_View&action=edit&redlink=1 "Discussion about the content page [t]")</span>

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
    id="ca-view">[Read](/web/20200117223417/http://wiki.vuze.com/w/Privacy_View)</span>
-   <span id="ca-viewsource">[View
    source](/web/20200117223417/http://wiki.vuze.com/mediawiki/index.php?title=Privacy_View&action=edit "This page is protected.
    You can view its source [e]")</span>
-   <span id="ca-history">[View
    history](/web/20200117223417/http://wiki.vuze.com/mediawiki/index.php?title=Privacy_View&action=history "Past revisions of this page [h]")</span>

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

<a href="/web/20200117223417/http://wiki.vuze.com/w/Main_Page" class="mw-wiki-logo" title="Visit the main page"></a>

</div>

<div id="p-" class="portal" role="navigation"
aria-labelledby="p--label">

### 

<div class="body">

-   <span id="n-Download-Vuze-Now">[Download Vuze
    Now](https://web.archive.org/web/20200117223417/http://www.vuze.com/download)</span>

</div>

</div>

<div id="p-navigation" class="portal" role="navigation"
aria-labelledby="p-navigation-label">

### Navigation

<div class="body">

-   <span id="n-mainpage-description">[Main
    page](/web/20200117223417/http://wiki.vuze.com/w/Main_Page "Visit the main page [z]")</span>
-   <span id="n-recentchanges">[Recent
    changes](/web/20200117223417/http://wiki.vuze.com/w/Special:RecentChanges "A list of recent changes in the wiki [r]")</span>
-   <span id="n-randompage">[Random
    page](/web/20200117223417/http://wiki.vuze.com/w/Special:Random "Load a random page [x]")</span>
-   <span
    id="n-help">[Help](https://web.archive.org/web/20200117223417/https://www.mediawiki.org/wiki/Special:MyLanguage/Help:Contents "The place to find out")</span>

</div>

</div>

<div id="p-tb" class="portal" role="navigation"
aria-labelledby="p-tb-label">

### Tools

<div class="body">

-   <span id="t-whatlinkshere">[What links
    here](/web/20200117223417/http://wiki.vuze.com/w/Special:WhatLinksHere/Privacy_View "A list of all wiki pages that link here [j]")</span>
-   <span id="t-recentchangeslinked">[Related
    changes](/web/20200117223417/http://wiki.vuze.com/w/Special:RecentChangesLinked/Privacy_View "Recent changes in pages linked from this page [k]")</span>
-   <span id="t-specialpages">[Special
    pages](/web/20200117223417/http://wiki.vuze.com/w/Special:SpecialPages "A list of all special pages [q]")</span>
-   <span id="t-print">[Printable
    version](/web/20200117223417/http://wiki.vuze.com/mediawiki/index.php?title=Privacy_View&printable=yes "Printable version of this page [p]")</span>
-   <span id="t-permalink">[Permanent
    link](/web/20200117223417/http://wiki.vuze.com/mediawiki/index.php?title=Privacy_View&oldid=16761 "Permanent link to this revision of the page")</span>
-   <span id="t-info">[Page
    information](/web/20200117223417/http://wiki.vuze.com/mediawiki/index.php?title=Privacy_View&action=info "More information about this page")</span>

</div>

</div>

</div>

</div>

<div id="footer" role="contentinfo">

-   <span id="footer-info-lastmod">This page was last modified on 12
    November 2015, at 23:27.</span>
-   <span id="footer-info-viewcount">This page has been accessed 187,471
    times.</span>

<!-- -->

-   <span id="footer-places-about">[About
    VuzeWiki](/web/20200117223417/http://wiki.vuze.com/w/VuzeWiki:About "VuzeWiki:About")</span>
-   <span
    id="footer-places-mobileview"><a href="https://web.archive.org/web/20200117223417/http://wiki.vuze.com/mediawiki/index.php?title=Privacy_View&amp;mobileaction=toggle_view_mobile" class="noprint stopMobileRedirectToggle">Mobile view</a></span>

<!-- -->

-   <span
    id="footer-poweredbyico">[<img src="/web/20200117223417im_/http://wiki.vuze.com/mediawiki/resources/assets/poweredby_mediawiki_88x31.png" srcset="/web/20200117223417im_/http://wiki.vuze.com/mediawiki/resources/assets/poweredby_mediawiki_132x47.png 1.5x, /web/20200117223417im_/http://wiki.vuze.com/mediawiki/resources/assets/poweredby_mediawiki_176x62.png 2x" width="88" height="31" alt="Powered by MediaWiki" />](//web.archive.org/web/20200117223417/http://www.mediawiki.org/)</span>
-   <span id="footer-analyticsystemsico">Any use of Vuze® and Vuze+™
    that violates the rights of any person or entity is not allowed.
    [More](https://web.archive.org/web/20200117223417/http://vuze.com/corp/legal.php)</span>

<div style="clear:both">

</div>

</div>
