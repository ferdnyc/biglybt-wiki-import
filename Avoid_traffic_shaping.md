<div id="mw-page-base" class="noprint">

</div>

<div id="mw-head-base" class="noprint">

</div>

<div id="content" class="mw-body" role="main">

<span id="top"></span>

<div class="mw-indicators">

</div>

# Avoid traffic shaping

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

*Note:* This is documentation specific to Vuze (Azureus), if you're
looking for the specifications see [Message Stream
Encryption](/web/20210712091909/http://wiki.vuze.com/w/Message_Stream_Encryption "Message Stream Encryption").

<div id="toc" class="toc">

<div id="toctitle">

## Contents

</div>

-   [<span class="tocnumber">1</span> <span class="toctext">General info
    for endusers</span>](#General_info_for_endusers)
-   [<span class="tocnumber">2</span> <span class="toctext">When to turn
    it on</span>](#When_to_turn_it_on)
    -   [<span class="tocnumber">2.1</span> <span class="toctext">The
        settings</span>](#The_settings)
    -   [<span class="tocnumber">2.2</span> <span
        class="toctext">Escalation of the crypto
        settings</span>](#Escalation_of_the_crypto_settings)
-   [<span class="tocnumber">3</span> <span class="toctext">Level
    5</span>](#Level_5)
    -   [<span class="tocnumber">3.1</span> <span
        class="toctext">Possible problems</span>](#Possible_problems)
    -   [<span class="tocnumber">3.2</span> <span
        class="toctext">Private torrents</span>](#Private_torrents)
    -   [<span class="tocnumber">3.3</span> <span
        class="toctext">Alternatives</span>](#Alternatives)
        -   [<span class="tocnumber">3.3.1</span> <span
            class="toctext">Disguising tracker
            traffic</span>](#Disguising_tracker_traffic)
-   [<span class="tocnumber">4</span> <span
    class="toctext">Notes</span>](#Notes)
-   [<span class="tocnumber">5</span> <span class="toctext">See
    also</span>](#See_also)

</div>

## <span id="General_info_for_endusers" class="mw-headline">General info for endusers</span><span class="mw-editsection"><span class="mw-editsection-bracket">\[</span>[edit](/web/20210712091909/http://wiki.vuze.com/mediawiki/index.php?title=Avoid_traffic_shaping&action=edit&section=1 "Edit section: General info for endusers")<span class="mw-editsection-bracket">\]</span></span>

Since more and more users are affected by overly aggressive
<a href="https://web.archive.org/web/20210712091909/http://wiki.vuze.com/" class="extiw" title="wikipedia:Traffic shaping">traffic shaping</a>
Azureus implements this traffic obfuscation feature to allow users to
use their bandwidth properly. Since this only works when a shaped peer
can connect to any peer in the swarm with the crypto header it is
currently not possible to turn this feature off.

This feature does NOT provide anonymity and only very limited
confidentiality, i.e. if somebody is in possession of the correct
infohash he can obtain your IP/Port combination from public sources like
a tracker or from other clients via
[PEX](/web/20210712091909/http://wiki.vuze.com/w/Peer_Exchange "Peer Exchange")
he will be able to connect to you as usual. Only a passive listener
can't determine what you're downloading.

## <span id="When_to_turn_it_on" class="mw-headline">When to turn it on</span><span class="mw-editsection"><span class="mw-editsection-bracket">\[</span>[edit](/web/20210712091909/http://wiki.vuze.com/mediawiki/index.php?title=Avoid_traffic_shaping&action=edit&section=2 "Edit section: When to turn it on")<span class="mw-editsection-bracket">\]</span></span>

Generally this feature will *not* help you with any kind of download
speed or other problems unless

-   you're affected by P2P/BitTorrent traffic shaping or it is
    completely blocked (see [Bad
    ISPs](/web/20210712091909/http://wiki.vuze.com/w/Bad_ISPs "Bad ISPs"))
-   you're on torrents with a large fraction of traffic shaped users
-   you want to hide what protocol you're using from passive
    surveillance (it is not for those who seek anonymity)

*Please note*: You should make sure that you don't violate any rules
(e.g. 'reasonable use' clauses) that are associated with your internet
connection such as the contract with your ISP.

So before you turn this feature on you should verify you have [good
settings](/web/20210712091909/http://wiki.vuze.com/w/Good_settings "Good settings")
and no [NAT
problem](/web/20210712091909/http://wiki.vuze.com/w/NAT_problem "NAT problem").

You might also test with the built-in Mlab speed test in Vuze for your
effective speeds and also for possible traffic
shaping/throttling/blocking activity. Go to [Help menu, select "Speed
test..."](/web/20210712091909/http://wiki.vuze.com/w/UG_Menus#Vuze_Help_Menu "UG Menus")
and run the "General speed test".

### <span id="The_settings" class="mw-headline">The settings</span><span class="mw-editsection"><span class="mw-editsection-bracket">\[</span>[edit](/web/20210712091909/http://wiki.vuze.com/mediawiki/index.php?title=Avoid_traffic_shaping&action=edit&section=3 "Edit section: The settings")<span class="mw-editsection-bracket">\]</span></span>

To enable the encryption you have to switch to intermediate user mode
and go to [*Tools -> Options -> Connection -> Transport
Encryption*](/web/20210712091909/http://wiki.vuze.com/w/UG_Options#Transport_Encryption "UG Options")
and enable the *Require encrypted transport* checkbox.

<a href="/web/20210712091909/http://wiki.vuze.com/w/File:Vuze4310OptionConnectionTransportEncryption.PNG" class="image"><img src="/web/20210712091909im_/http://wiki.vuze.com/mediawiki/images/b/bc/Vuze4310OptionConnectionTransportEncryption.PNG" width="740" height="250" alt="Vuze4310OptionConnectionTransportEncryption.PNG" /></a>

Enabling this feature instructs to establish connections with the crypto
handshake, which will consume more CPU time due to the
<a href="https://web.archive.org/web/20210712091909/http://wiki.vuze.com/" class="extiw" title="wikipedia:D-H">D-H</a>
key exchange. If it is disabled Azureus will only use the obfuscation
header for peers that either require that via PEX/DHT or when a remote
peer initiates a crypto connection.

Further details are controlled by the following settings:

Minimum encryption level  
this will specify the minimal encryption level you will choose when
establish encrypted connections, currently available are

1.  **Plain**: This only uses the obfuscation header and transmits the
    entire payload unencrypted. It's still easy to identify but might be
    enough to confuse simple traffic shapers
2.  **RC4**: This mode uses strong cryptography to obfuscate the traffic
    and is only attackable with very sophisticated and expensive attacks
    but it consumes more CPU time than the *Plain* method.

<!-- -->

Allow non-encrypted outgoing connections if encrypted connection attempt fails <span class="reference"><sup>[2](#fn_2)</sup></span>  
This option ensures compatibility with legacy clients that don't support
the traffic obfuscation but makes it easier for the ISP to identify
users that engage in BitTorrent activity.

Allow non-encrypted incoming connections  
Disabling this option will prevent any peer from connecting to you
unless he uses the obfuscation header. Thus it even prevent peers from
connecting to you when they support encryption but don't know that you
require it. But as stated in the implementation
[specs](/web/20210712091909/http://wiki.vuze.com/w/Message_Stream_Encryption#Notes_about_the_current_Azureus_implementation "Message Stream Encryption")
Azureus'
[PEX](/web/20210712091909/http://wiki.vuze.com/w/Peer_Exchange "Peer Exchange")
and [Distributed
tracker](/web/20210712091909/http://wiki.vuze.com/w/Distributed_tracker "Distributed tracker")
is obfuscation aware and thus tells other peers to use it even when they
default encryption to off.  
Enabling this option may be necessary when the ISP limits ports instead
of single connections.

### <span id="Escalation_of_the_crypto_settings" class="mw-headline">Escalation of the crypto settings</span><span class="mw-editsection"><span class="mw-editsection-bracket">\[</span>[edit](/web/20210712091909/http://wiki.vuze.com/mediawiki/index.php?title=Avoid_traffic_shaping&action=edit&section=4 "Edit section: Escalation of the crypto settings")<span class="mw-editsection-bracket">\]</span></span>

Since different methods of traffic shaping and protocol discovery exist
different levels of shaping avoidance are necessary. The following
configuration options are listed in ascending order.

It's suggested to use one of the first 3 combinations unless there is
evidence that more drastic steps are necessary. If you turn off fallback
for incoming connections we suggest to change the listening port in case
the shaping is done on a per-port basis.

| Level                                                                                                                  | Enabled                                                                                                                  | Method | allow outgoing fallback | allow incoming fallback | advantages                                                                                                                                         | disadvantages                                                                            |
|------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------|--------|-------------------------|-------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------|
| 0                                                                                                                      | No + using a [non-standard port](/web/20210712091909/http://wiki.vuze.com/w/Select_port_for_Vuze "Select port for Vuze") | none   | Yes                     | Yes                     | Doesn't use cryptography unless required by a peer<span class="reference"><sup>[1](#fn_1)</sup></span>; no additional CPU consumption              | Doesn't prevent traffic shaping, unless the provider simply throttles standard P2P ports |
| 1                                                                                                                      | Yes                                                                                                                      | Plain  | Yes                     | Yes                     | Least CPU intensive and most compatible setting to avoid traffic shaping                                                                           | Easy to detect since the payload isn't encrypted                                         |
| 2                                                                                                                      | Yes                                                                                                                      | RC4    | Yes                     | Yes                     | Still maintains maximum compatibility but avoids traffic shaping, at least for outgoing connections                                                | The incoming port used for BT connections may be detected                                |
| 3 <span class="reference"><sup>[2](#fn_2)</sup></span><sup>,</sup><span class="reference"><sup>[3](#fn_3)</sup></span> | Yes                                                                                                                      | RC4    | Yes                     | No                      | Prevents that any classic BT connection to the incoming port is successful and thus makes it harder to identify ports that are used for BT traffic | Limited backwards compatibility                                                          |
| 4 <span class="reference"><sup>[3](#fn_3)</sup></span>                                                                 | Yes                                                                                                                      | RC4    | No                      | No                      | Prevents any classic BT connection and thus makes it harder to identify the entire host as a BT user                                               | No backwards compatibility at all                                                        |
| 5 <span class="reference"><sup>[3](#fn_3)</sup></span>                                                                 | see [Level 5](#Level_5) below                                                                                            |        |                         |                         |                                                                                                                                                    |                                                                                          |

## <span id="Level_5" class="mw-headline">Level 5</span><span class="mw-editsection"><span class="mw-editsection-bracket">\[</span>[edit](/web/20210712091909/http://wiki.vuze.com/mediawiki/index.php?title=Avoid_traffic_shaping&action=edit&section=5 "Edit section: Level 5")<span class="mw-editsection-bracket">\]</span></span>

*Note:* This is level is available from Azureus 3.0.2.3_B05 onwards.

Level 5 is only intended for people who have problems with a specific
traffic shaping method employed by sandvine traffic shaping hardware,
see [Bad
ISPs](/web/20210712091909/http://wiki.vuze.com/w/Bad_ISPs "Bad ISPs") to
discover if this applies to you. The premise of this method is to
minimize the amount of unencrypted information leaked. To enable it
select following settings:

1.  *Tools -> Options -> Connection -> Transport Encryption* ([See
    here](/web/20210712091909/http://wiki.vuze.com/w/UG_Options#Transport_Encryption "UG Options"))
    -   Enable *require encryption*
    -   Select *RC4*
    -   Disable both fallback checkboxes
2.  *Tools -> Options -> Tracker -> Client*
    -   Enable *Do not announce the listening port to the tracker*
    -   Set the peer limit to a low figure, start with 1 or 2
    -   set the *Minimum time between tracker announces* to 900 for
        example
3.  Adjust DHT settings (2 mutually exclusive alternatives):
    -   Disable the DHT:

    Go to *Tools -> Options -> Plugins -> Distributed DB* and uncheck
    *Enable the distributed database*
    -   Try to get more peers via DHT:

    Go to *Tools -> Options -> Plugins -> Distributed Tracker* and
    uncheck *Only track normal torrents\[...\]*
4.  Try to seed a torrent you haven't seeded within the last few hours
    or so before applying these settings

  

### <span id="Possible_problems" class="mw-headline">Possible problems</span><span class="mw-editsection"><span class="mw-editsection-bracket">\[</span>[edit](/web/20210712091909/http://wiki.vuze.com/mediawiki/index.php?title=Avoid_traffic_shaping&action=edit&section=6 "Edit section: Possible problems")<span class="mw-editsection-bracket">\]</span></span>

-   For some of these settings to be available you will have to switch
    to intermediate or higher user mode
-   This might not work on torrents with very few peers because the
    shaping device may grab all necessary data with the first few
    tracker announces
-   These settings will significantly increase the time it takes to join
    a swarm, regardless of downloading or uploading, so you have to be
    patient and/or perform a manual announce a few(!) times until you
    get your first few pex-capable peers. You should also consider that
    [PEX](/web/20210712091909/http://wiki.vuze.com/w/Peer_Exchange "Peer Exchange")
    takes at least a minute, if not longer to gather additional peers.
-   This will not work on private torrents, see below.
-   This solution may not work at all for you! We've had both reports of
    success and failure with the method described above.

### <span id="Private_torrents" class="mw-headline">Private torrents</span><span class="mw-editsection"><span class="mw-editsection-bracket">\[</span>[edit](/web/20210712091909/http://wiki.vuze.com/mediawiki/index.php?title=Avoid_traffic_shaping&action=edit&section=7 "Edit section: Private torrents")<span class="mw-editsection-bracket">\]</span></span>

Since level 5 is highly dependent on
[PEX](/web/20210712091909/http://wiki.vuze.com/w/Peer_Exchange "Peer Exchange")
which is mutually exclusive with [private
torrents](/web/20210712091909/http://wiki.vuze.com/w/Private_torrent "Private torrent")/trackers
this mode cannot be applied to seed or download on private trackers. But
since private trackers are usually community-based it should be easy for
you to request your administrators to add
<a href="https://web.archive.org/web/20210712091909/http://wiki.vuze.com/" class="extiw" title="wikipedia:https">HTTPS</a>-support
to their tracker and thus reduce the information leak to traffic shaping
hardware.

*Note:* Since only users affected by this kind of traffic shaping will
need https-tracker announces and the remaining userbase can use http the
performance impact should be negligible.

### <span id="Alternatives" class="mw-headline">Alternatives</span><span class="mw-editsection"><span class="mw-editsection-bracket">\[</span>[edit](/web/20210712091909/http://wiki.vuze.com/mediawiki/index.php?title=Avoid_traffic_shaping&action=edit&section=8 "Edit section: Alternatives")<span class="mw-editsection-bracket">\]</span></span>

If you are not the initial seed of a torrent and just want to do your
fair share of uploading you can do that while you're still downloading
by dynamically limiting the download speed to a multiple or fraction of
the upload speed, you can do that by using autospeed classic under
*tools -> options -> transfer -> autospeed* and setting an download to
upload speed ratio.

#### <span id="Disguising_tracker_traffic" class="mw-headline">Disguising tracker traffic</span><span class="mw-editsection"><span class="mw-editsection-bracket">\[</span>[edit](/web/20210712091909/http://wiki.vuze.com/mediawiki/index.php?title=Avoid_traffic_shaping&action=edit&section=9 "Edit section: Disguising tracker traffic")<span class="mw-editsection-bracket">\]</span></span>

Another option is to tunnel the tracker over
<a href="https://web.archive.org/web/20210712091909/http://tor.eff.org/" class="external text">TOR</a>
or an SSH-Tunnel via *tracker communication proxying* using SOCKS under
*tools -> options -> connection -> proxy options*. If you do this you
won't have to set any of the above options (limiting peer requests
etc.), but you will have to set your announce IP override to your
external, public IP under *tools -> options -> tracker -> client*.

## <span id="Notes" class="mw-headline">Notes</span><span class="mw-editsection"><span class="mw-editsection-bracket">\[</span>[edit](/web/20210712091909/http://wiki.vuze.com/mediawiki/index.php?title=Avoid_traffic_shaping&action=edit&section=10 "Edit section: Notes")<span class="mw-editsection-bracket">\]</span></span>

-   [Note 1](#fn_1_back): Doesn't work with [private
    torrents](/web/20210712091909/http://wiki.vuze.com/w/Private_torrent "Private torrent")
-   [Note 2](#fn_2_back): Should not be used in combination with the
    [bind to local
    port](/web/20210712091909/http://wiki.vuze.com/w/UG_Options#Advanced_Network_Settings "UG Options")
    feature
-   [Note 3](#fn_3_back): You should change your listening port and
    adjust your [port
    forward](/web/20210712091909/http://wiki.vuze.com/w/Port_forwarding "Port forwarding")
    and/or
    [firewall](/web/20210712091909/http://wiki.vuze.com/w/Firewalling "Firewalling")
    rules after you've disabled incoming fallback connections

## <span id="See_also" class="mw-headline">See also</span><span class="mw-editsection"><span class="mw-editsection-bracket">\[</span>[edit](/web/20210712091909/http://wiki.vuze.com/mediawiki/index.php?title=Avoid_traffic_shaping&action=edit&section=11 "Edit section: See also")<span class="mw-editsection-bracket">\]</span></span>

-   [Message Stream
    Encryption](/web/20210712091909/http://wiki.vuze.com/w/Message_Stream_Encryption "Message Stream Encryption")
-   [Bad
    ISPs](/web/20210712091909/http://wiki.vuze.com/w/Bad_ISPs "Bad ISPs")

</div>

<div class="printfooter">

Retrieved from
"[http://wiki.vuze.com/mediawiki/index.php?title=Avoid_traffic_shaping&oldid=15807](https://web.archive.org/web/20210712091909/http://wiki.vuze.com/mediawiki/index.php?title=Avoid_traffic_shaping&oldid=15807)"

</div>

<div id="catlinks" class="catlinks" mw="interface">

<div id="mw-normal-catlinks" class="mw-normal-catlinks">

[Categories](/web/20210712091909/http://wiki.vuze.com/w/Special:Categories "Special:Categories"):

-   [Documentation](/web/20210712091909/http://wiki.vuze.com/w/Category:Documentation "Category:Documentation")
-   [Troubleshooting](/web/20210712091909/http://wiki.vuze.com/w/Category:Troubleshooting "Category:Troubleshooting")

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
    id="pt-anontalk">[Talk](/web/20210712091909/http://wiki.vuze.com/w/Special:MyTalk "Discussion about edits from this IP address [n]")</span>
-   <span
    id="pt-anoncontribs">[Contributions](/web/20210712091909/http://wiki.vuze.com/w/Special:MyContributions "A list of edits made from this IP address [y]")</span>
-   <span id="pt-createaccount">[Create
    account](/web/20210712091909/http://wiki.vuze.com/mediawiki/index.php?title=Special:CreateAccount&returnto=Avoid+traffic+shaping "You are encouraged to create an account and log in; however, it is not mandatory")</span>
-   <span id="pt-login">[Log
    in](/web/20210712091909/http://wiki.vuze.com/mediawiki/index.php?title=Special:UserLogin&returnto=Avoid+traffic+shaping "You are encouraged to log in; however, it is not mandatory [o]")</span>

</div>

<div id="left-navigation">

<div id="p-namespaces" class="vectorTabs" role="navigation"
aria-labelledby="p-namespaces-label">

### Namespaces

-   <span
    id="ca-nstab-main">[Page](/web/20210712091909/http://wiki.vuze.com/w/Avoid_traffic_shaping "View the content page [c]")</span>
-   <span
    id="ca-talk">[Discussion](/web/20210712091909/http://wiki.vuze.com/mediawiki/index.php?title=Talk:Avoid_traffic_shaping&action=edit&redlink=1 "Discussion about the content page [t]")</span>

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
    id="ca-view">[Read](/web/20210712091909/http://wiki.vuze.com/w/Avoid_traffic_shaping)</span>
-   <span
    id="ca-edit">[Edit](/web/20210712091909/http://wiki.vuze.com/mediawiki/index.php?title=Avoid_traffic_shaping&action=edit "Edit this page [e]")</span>
-   <span id="ca-history">[View
    history](/web/20210712091909/http://wiki.vuze.com/mediawiki/index.php?title=Avoid_traffic_shaping&action=history "Past revisions of this page [h]")</span>

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

<a href="/web/20210712091909/http://wiki.vuze.com/w/Main_Page" class="mw-wiki-logo" title="Visit the main page"></a>

</div>

<div id="p-" class="portal" role="navigation"
aria-labelledby="p--label">

### 

<div class="body">

-   <span id="n-Download-Vuze-Now">[Download Vuze
    Now](https://web.archive.org/web/20210712091909/http://www.vuze.com/download)</span>

</div>

</div>

<div id="p-navigation" class="portal" role="navigation"
aria-labelledby="p-navigation-label">

### Navigation

<div class="body">

-   <span id="n-mainpage-description">[Main
    page](/web/20210712091909/http://wiki.vuze.com/w/Main_Page "Visit the main page [z]")</span>
-   <span id="n-recentchanges">[Recent
    changes](/web/20210712091909/http://wiki.vuze.com/w/Special:RecentChanges "A list of recent changes in the wiki [r]")</span>
-   <span id="n-randompage">[Random
    page](/web/20210712091909/http://wiki.vuze.com/w/Special:Random "Load a random page [x]")</span>
-   <span
    id="n-help">[Help](https://web.archive.org/web/20210712091909/https://www.mediawiki.org/wiki/Special:MyLanguage/Help:Contents "The place to find out")</span>

</div>

</div>

<div id="p-tb" class="portal" role="navigation"
aria-labelledby="p-tb-label">

### Tools

<div class="body">

-   <span id="t-whatlinkshere">[What links
    here](/web/20210712091909/http://wiki.vuze.com/w/Special:WhatLinksHere/Avoid_traffic_shaping "A list of all wiki pages that link here [j]")</span>
-   <span id="t-recentchangeslinked">[Related
    changes](/web/20210712091909/http://wiki.vuze.com/w/Special:RecentChangesLinked/Avoid_traffic_shaping "Recent changes in pages linked from this page [k]")</span>
-   <span id="t-specialpages">[Special
    pages](/web/20210712091909/http://wiki.vuze.com/w/Special:SpecialPages "A list of all special pages [q]")</span>
-   <span id="t-print">[Printable
    version](/web/20210712091909/http://wiki.vuze.com/mediawiki/index.php?title=Avoid_traffic_shaping&printable=yes "Printable version of this page [p]")</span>
-   <span id="t-permalink">[Permanent
    link](/web/20210712091909/http://wiki.vuze.com/mediawiki/index.php?title=Avoid_traffic_shaping&oldid=15807 "Permanent link to this revision of the page")</span>
-   <span id="t-info">[Page
    information](/web/20210712091909/http://wiki.vuze.com/mediawiki/index.php?title=Avoid_traffic_shaping&action=info "More information about this page")</span>

</div>

</div>

</div>

</div>

<div id="footer" role="contentinfo">

-   <span id="footer-info-lastmod">This page was last modified on 26
    February 2014, at 19:14.</span>
-   <span id="footer-info-viewcount">This page has been accessed 163,971
    times.</span>

<!-- -->

-   <span id="footer-places-about">[About
    VuzeWiki](/web/20210712091909/http://wiki.vuze.com/w/VuzeWiki:About "VuzeWiki:About")</span>
-   <span
    id="footer-places-mobileview"><a href="https://web.archive.org/web/20210712091909/http://wiki.vuze.com/mediawiki/index.php?title=Avoid_traffic_shaping&amp;mobileaction=toggle_view_mobile" class="noprint stopMobileRedirectToggle">Mobile view</a></span>

<!-- -->

-   <span
    id="footer-poweredbyico">[<img src="/web/20210712091909im_/http://wiki.vuze.com/mediawiki/resources/assets/poweredby_mediawiki_88x31.png" srcset="/web/20210712091909im_/http://wiki.vuze.com/mediawiki/resources/assets/poweredby_mediawiki_132x47.png 1.5x, /web/20210712091909im_/http://wiki.vuze.com/mediawiki/resources/assets/poweredby_mediawiki_176x62.png 2x" width="88" height="31" alt="Powered by MediaWiki" />](//web.archive.org/web/20210712091909/http://www.mediawiki.org/)</span>
-   <span id="footer-analyticsystemsico">Any use of Vuze® and Vuze+™
    that violates the rights of any person or entity is not allowed.
    [More](https://web.archive.org/web/20210712091909/http://vuze.com/corp/legal.php)</span>

<div style="clear:both">

</div>

</div>
