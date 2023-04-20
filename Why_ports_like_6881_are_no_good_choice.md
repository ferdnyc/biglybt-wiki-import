<div id="mw-page-base" class="noprint">

</div>

<div id="mw-head-base" class="noprint">

</div>

<div id="content" class="mw-body" role="main">

<span id="top"></span>

<div class="mw-indicators">

</div>

# Select port for Vuze

<div id="bodyContent" class="mw-body-content">

<div id="siteSub">

From VuzeWiki

</div>

<div id="contentSub">

<span class="mw-redirectedfrom">(Redirected from [Why ports like 6881
are no good
choice](/web/20190715182127/http://wiki.vuze.com/mediawiki/index.php?title=Why_ports_like_6881_are_no_good_choice&redirect=no "Why ports like 6881 are no good choice"))</span>

</div>

<div id="jump-to-nav" class="mw-jump">

Jump to: [navigation](#mw-head), [search](#p-search)

</div>

<div id="mw-content-text" class="mw-content-ltr" lang="en" dir="ltr">

  

<div id="toc" class="toc">

<div id="toctitle">

## Contents

</div>

-   [<span class="tocnumber">1</span> <span class="toctext">Which port
    should I use for Vuze?</span>](#Which_port_should_I_use_for_Vuze.3F)
    -   [<span class="tocnumber">1.1</span> <span class="toctext">Which
        ports does Vuze use by
        default?</span>](#Which_ports_does_Vuze_use_by_default.3F)
-   [<span class="tocnumber">2</span> <span class="toctext">Why are
    ports blocked/blacklisted and what can I do about
    it?</span>](#Why_are_ports_blocked.2Fblacklisted_and_what_can_I_do_about_it.3F)
    -   [<span class="tocnumber">2.1</span> <span class="toctext">Why is
        port 6881 (or whatever)
        blocked/blacklisted?</span>](#Why_is_port_6881_.28or_whatever.29_blocked.2Fblacklisted.3F)
    -   [<span class="tocnumber">2.2</span> <span class="toctext">So
        what can I do about it if I'm already
        blacklisted?</span>](#So_what_can_I_do_about_it_if_I.27m_already_blacklisted.3F)

</div>

## <span id="Which_port_should_I_use_for_Vuze.3F" class="mw-headline">Which port should I use for Vuze?</span><span class="mw-editsection"><span class="mw-editsection-bracket">\[</span>[edit](/web/20190715182127/http://wiki.vuze.com/mediawiki/index.php?title=Select_port_for_Vuze&action=edit&section=1 "Edit section: Which port should I use for Vuze?")<span class="mw-editsection-bracket">\]</span></span>

[Ports](/web/20190715182127/http://wiki.vuze.com/w/Ports "Ports") are
just logical addresses inside your computer's
<a href="https://web.archive.org/web/20190715182127/http://en.wikipedia.org/wiki/Internet_Protocol_Suite" class="external text">TCP/IP</a>
networking functionality. From technological perspective there is no
difference between ports, so you can select any port **which is not
already used by something else** and then you need to configure your
firewall and router accordingly.

1.  Vuze needs only one port for the main data transfer functionality.
    Choose a port from the **49160–65534** range. If you really need to
    choose a port within the range **1024–49151** make sure you pick an
    "unassigned" port listed at the
    <a href="https://web.archive.org/web/20190715182127/http://www.iana.org/assignments/port-numbers" class="external text">IANA port list</a>
    and which is not already in use by some other application in your
    computer.
    -   **Go to
        <a href="/web/20190715182127/http://wiki.vuze.com/w/Options" class="mw-redirect" title="Options">Options</a> >
        [Connection](/web/20190715182127/http://wiki.vuze.com/w/UG_Options#Connection_options "UG Options")**
        and input the new TCP and UDP listening port that you have
        chosen.
    -   Save the changed options.
2.  Go into your software firewall configuration and make sure that Vuze
    is allowed *outgoing* and *incoming* connections (and if there is
    such an option, enable Vuze to *act as a server*). Possibly the
    firewall is only configured for applications, but it might also
    require port-specific configuration.
3.  **Go into your router configuration**, if any, and forward the port
    you have chosen using the methods as described in [NAT
    problem](/web/20190715182127/http://wiki.vuze.com/w/NAT_problem "NAT problem")
    and [Port
    forwarding](/web/20190715182127/http://wiki.vuze.com/w/Port_forwarding "Port forwarding").
    Remember to **forward that port** not only for TCP but **also for
    UDP protocol**,
    [DHT](/web/20190715182127/http://wiki.vuze.com/w/Distributed_hash_table "Distributed hash table")
    needs that! (If your router is using UPnP, it should update
    automatically.

Note: When using a port above 49152, you always run to a risk that some
other program has randomly grabbed that port before you start Vuze. For
example, with Vista and Windows7 the operating system itself usually
grabs ports 49152-49158 at boot, so you can't use those ports. For
Windows 8.1, the operating system seems to grab ports throughout the
entire numerical range.

In Windows environment, you can check which ports are currently in use
(already reserved by some program) from CMD commandline prompt with the
command **NETSTAT -A** . Or use the command **NETSTAT -A \> FILE**. This
will produce a text file of the results, saved in the directory from
which the command prompt is operating. The text file might be much more
convenient to use, as without it, the screen results may just scroll by.

Select randomly some port number, which **is not shown** in the list.
The command should output the currently used ports with results like:

C:\\Users\\myusername>**netstat -a**

*Proto Local Address Foreign Address State*

*TCP 0.0.0.0:135 P35HN:0 LISTENING*

*TCP 0.0.0.0:445 P35HN:0 LISTENING*

*TCP 0.0.0.0:5357 P35HN:0 LISTENING*

*TCP 0.0.0.0:12110 P35HN:0 LISTENING*

*TCP 0.0.0.0:49152 P35HN:0 LISTENING*

So, lots of free ports to choose from as only a few ports are already
taken...

Once again, the **NETSTAT -A** command shows ports that **you can't
use**. Select randomly a port, **which is not shown** in the list.

### <span id="Which_ports_does_Vuze_use_by_default.3F" class="mw-headline">Which ports does Vuze use by default?</span><span class="mw-editsection"><span class="mw-editsection-bracket">\[</span>[edit](/web/20190715182127/http://wiki.vuze.com/mediawiki/index.php?title=Select_port_for_Vuze&action=edit&section=2 "Edit section: Which ports does Vuze use by default?")<span class="mw-editsection-bracket">\]</span></span>

When you first install Vuze, it selects the "main port" for torrent
downloading/uploding usage by random. As described previously, you can
change that to something else if you like.

Vuze also uses some ports for internal use and/or as defaults for some
functionality:

-   1900 UDP: Used for UPnP?
-   6880 TCP: Vuze uses this port for internal communication. When you
    launch Vuze, it always checks that port for an older instance of
    Vuze being already active. If there is an active Vuze, then the new
    Vuze instance passes the possible torrent name as parameter to the
    old instance already running and then dies. (This happens e.g. when
    you click a "download torrent" link on a web page. A new second Vuze
    instance gets launched by the browser, but it dies after passing the
    argument to the old Vuze.) If there was no active old Vuze, then the
    new Vuze reserves that TCP port and starts "listening" there.
-   6969 TCP: If you enable internal HTTP tracker, this is the default
    port used. You need to port-forward this port in router for full
    connectivity.
-   7000 TCP: Default port for HTTPS tracker. (usually not in use)
-   16680 UDP: Used for the 'LAN peer finder' functionality.
-   45100 TCP: Used for magnet URI handling.
-   49001 UDP: Used for Mainline DHT (if that plugin is installed). You
    need to port-forward this port in router for full connectivity.

## <span id="Why_are_ports_blocked.2Fblacklisted_and_what_can_I_do_about_it.3F" class="mw-headline">Why are ports blocked/blacklisted and what can I do about it?</span><span class="mw-editsection"><span class="mw-editsection-bracket">\[</span>[edit](/web/20190715182127/http://wiki.vuze.com/mediawiki/index.php?title=Select_port_for_Vuze&action=edit&section=3 "Edit section: Why are ports blocked/blacklisted and what can I do about it?")<span class="mw-editsection-bracket">\]</span></span>

<a href="https://web.archive.org/web/20190715182127/http://en.wikipedia.org/wiki/Internet_service_provider" class="external text">ISPs</a>
have been increasingly reducing the available bandwidth for P2P users on
the standard file-sharing [port
ranges](/web/20190715182127/http://wiki.vuze.com/w/Ports "Ports"). You
may find you need to keep changing your port on a regular basis. This is
normal, and a port change should sort you out if this is indeed what is
happening. And please keep in mind that after any port change, and
stopping and restarting any torrent, it may take up to half an hour or
more for the benefits to become noticeable. So please try not to panic
when things do not improve **immediately**. This is normal. :)

If you suspect that your ISP is blocking/throttling bittorrent traffic,
you might check the [Bad ISPs
list](/web/20190715182127/http://wiki.vuze.com/w/Bad_ISPs "Bad ISPs")
and consider ways to [avoid traffic
shaping](/web/20190715182127/http://wiki.vuze.com/w/Avoid_traffic_shaping "Avoid traffic shaping")
e.g. by encryption.

### <span id="Why_is_port_6881_.28or_whatever.29_blocked.2Fblacklisted.3F" class="mw-headline">Why is port 6881 (or whatever) blocked/blacklisted?</span><span class="mw-editsection"><span class="mw-editsection-bracket">\[</span>[edit](/web/20190715182127/http://wiki.vuze.com/mediawiki/index.php?title=Select_port_for_Vuze&action=edit&section=4 "Edit section: Why is port 6881 (or whatever) blocked/blacklisted?")<span class="mw-editsection-bracket">\]</span></span>

To avoid a decreasing [Average Swarm
Speed](/web/20190715182127/http://wiki.vuze.com/w/Average_Swarm_Speed "Average Swarm Speed"),
some
[tracker](/web/20190715182127/http://wiki.vuze.com/w/This_funny_word#Tracker "This funny word")
administrators are banning these often throttled standard
[ports](/web/20190715182127/http://wiki.vuze.com/w/Ports "Ports"). This
includes the standard port range of 6881–6999, which ports were used by
the "original" Bittorrent client program a few years ago.

So what happens is, those trackers reject connections from bittorrent
clients who are listening on any of the ports within those ranges, and
some of those trackers may blacklist those IPs for 48 hours. So the
torrents will show [red health
smileys](/web/20190715182127/http://wiki.vuze.com/w/Torrent_health "Torrent health")<a href="/web/20190715182127/http://wiki.vuze.com/w/File:Ko.gif" class="image"><img src="/web/20190715182127im_/http://wiki.vuze.com/mediawiki/images/9/9e/Ko.gif" width="17" height="17" alt="Ko.gif" /></a>,
and even if you change your listening port, you are unable to connect
because of the 48 hour ban. This kind of ban will often be reported
under the "Tracker Status" of a torrent in its [Details
screen](/web/20190715182127/http://wiki.vuze.com/w/UG_Advanced_Information#General_tab "UG Advanced Information"),
with the blacklisted information.

The same goes for ISPs, who recognize the port 6881 to be used mostly
for bittorrent traffic, and it might be the first port to be blocked if
the ISP starts to block/throttle/shape bittorrent traffic. If you mostly
receive [blue health
smileys](/web/20190715182127/http://wiki.vuze.com/w/Torrent_health "Torrent health")<a href="/web/20190715182127/http://wiki.vuze.com/w/File:No_tracker.gif" class="image"><img src="/web/20190715182127im_/http://wiki.vuze.com/mediawiki/images/c/c1/No_tracker.gif" width="17" height="17" alt="No tracker.gif" /></a>,
you might suspect that to be the reason.

The best advice is to never use ports from the range 6881-6999.

### <span id="So_what_can_I_do_about_it_if_I.27m_already_blacklisted.3F" class="mw-headline">So what can I do about it if I'm already blacklisted?</span><span class="mw-editsection"><span class="mw-editsection-bracket">\[</span>[edit](/web/20190715182127/http://wiki.vuze.com/mediawiki/index.php?title=Select_port_for_Vuze&action=edit&section=5 "Edit section: So what can I do about it if I'm already blacklisted?")<span class="mw-editsection-bracket">\]</span></span>

1.  **Choose a new TCP listening port for Vuze.** The best range to
    choose a new port from is: **49160–65534** If you really need to
    choose a port within the range **1024–49151** make sure you pick an
    "unassigned" port listed at the
    <a href="https://web.archive.org/web/20190715182127/http://www.iana.org/assignments/port-numbers" class="external text">IANA port list</a>.
    Remember that Vuze needs **one** listening port **only**, so please
    choose one port from the above range.
    -   **Go to
        [Options](/web/20190715182127/http://wiki.vuze.com/w/UG_Options "UG Options") >
        [Connection](/web/20190715182127/http://wiki.vuze.com/w/UG_Options#Connection_options "UG Options")**
        and input the new TCP and UDP listening port that you have
        chosen.
    -   **Click "Save"** at the bottom left side of the screen.
2.  **Go into your router and/or firewall**, if any, and forward the
    port you have chosen using the methods as described in [Port
    forwarding](/web/20190715182127/http://wiki.vuze.com/w/Port_forwarding "Port forwarding")
    and [NAT
    problem](/web/20190715182127/http://wiki.vuze.com/w/NAT_problem "NAT problem").
    Remember to **forward that port** not only for TCP but **also for
    UDP protocol**,
    [DHT](/web/20190715182127/http://wiki.vuze.com/w/Distributed_hash_table "Distributed hash table")
    needs that! (If your router is using UPnP, it should update
    automatically.) The "Port xxxx is blacklisted" message from the
    [tracker](/web/20190715182127/http://wiki.vuze.com/w/This_funny_word#Tracker "This funny word")
    should disappear and the torrent will start. If not, check your
    router and firewall, then go on to step 5.
3.  **Stop all your actively running torrents.** (This is *temporary*,
    just until you get the port sorted out. Vuze will remember all the
    peers you were connected to when you start the torrents up again,
    even if the tracker is offline. No need to panic. Please ring a
    friend if you need any extra support during this trying
    experience.) :-)
4.  **Quit Vuze.**
5.  **Wait a few minutes.**
6.  **Run Vuze**
7.  **Go to Help -> NAT/Firewall Test** and do the port test. You will
    see a port tester with your selected port entered in it by default.
    Change the port number, if necessary, and click "test". You will
    then get any one of three results from this:
    1.  **"This port can not be tested because it is already in use"**
        If you get this message, repeat steps 4–8
    2.  **"NAT Error"** If you get this message, please see the [Port
        forwarding](/web/20190715182127/http://wiki.vuze.com/w/Port_forwarding "Port forwarding")
        and [NAT
        problem](/web/20190715182127/http://wiki.vuze.com/w/NAT_problem "NAT problem")
        pages.
    3.  **"OK!"** If you get this message, then you have just done
        everything right, all is groovy, and the world should appear a
        much rosier place to live in. :-)

  

  
<span class="small">Read the [Azureus
FAQ](/web/20190715182127/http://wiki.vuze.com/w/Azureus_FAQ "Azureus FAQ")</span>

</div>

<div class="printfooter">

Retrieved from
"[http://wiki.vuze.com/mediawiki/index.php?title=Select_port_for_Vuze&oldid=16173](https://web.archive.org/web/20190715182127/http://wiki.vuze.com/mediawiki/index.php?title=Select_port_for_Vuze&oldid=16173)"

</div>

<div id="catlinks" class="catlinks" mw="interface">

<div id="mw-normal-catlinks" class="mw-normal-catlinks">

[Categories](/web/20190715182127/http://wiki.vuze.com/w/Special:Categories "Special:Categories"):

-   [NAT and
    firewalling](/web/20190715182127/http://wiki.vuze.com/w/Category:NAT_and_firewalling "Category:NAT and firewalling")
-   [Troubleshooting](/web/20190715182127/http://wiki.vuze.com/w/Category:Troubleshooting "Category:Troubleshooting")
-   [Documentation](/web/20190715182127/http://wiki.vuze.com/w/Category:Documentation "Category:Documentation")

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
    id="pt-anontalk">[Talk](/web/20190715182127/http://wiki.vuze.com/w/Special:MyTalk "Discussion about edits from this IP address [n]")</span>
-   <span
    id="pt-anoncontribs">[Contributions](/web/20190715182127/http://wiki.vuze.com/w/Special:MyContributions "A list of edits made from this IP address [y]")</span>
-   <span id="pt-createaccount">[Create
    account](/web/20190715182127/http://wiki.vuze.com/mediawiki/index.php?title=Special:CreateAccount&returnto=Select+port+for+Vuze "You are encouraged to create an account and log in; however, it is not mandatory")</span>
-   <span id="pt-login">[Log
    in](/web/20190715182127/http://wiki.vuze.com/mediawiki/index.php?title=Special:UserLogin&returnto=Select+port+for+Vuze "You are encouraged to log in; however, it is not mandatory [o]")</span>

</div>

<div id="left-navigation">

<div id="p-namespaces" class="vectorTabs" role="navigation"
aria-labelledby="p-namespaces-label">

### Namespaces

-   <span
    id="ca-nstab-main">[Page](/web/20190715182127/http://wiki.vuze.com/w/Select_port_for_Vuze "View the content page [c]")</span>
-   <span
    id="ca-talk">[Discussion](/web/20190715182127/http://wiki.vuze.com/mediawiki/index.php?title=Talk:Select_port_for_Vuze&action=edit&redlink=1 "Discussion about the content page [t]")</span>

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
    id="ca-view">[Read](/web/20190715182127/http://wiki.vuze.com/w/Select_port_for_Vuze)</span>
-   <span
    id="ca-edit">[Edit](/web/20190715182127/http://wiki.vuze.com/mediawiki/index.php?title=Select_port_for_Vuze&action=edit "Edit this page [e]")</span>
-   <span id="ca-history">[View
    history](/web/20190715182127/http://wiki.vuze.com/mediawiki/index.php?title=Select_port_for_Vuze&action=history "Past revisions of this page [h]")</span>

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

<a href="/web/20190715182127/http://wiki.vuze.com/w/Main_Page" class="mw-wiki-logo" title="Visit the main page"></a>

</div>

<div id="p-" class="portal" role="navigation"
aria-labelledby="p--label">

### 

<div class="body">

-   <span id="n-Download-Vuze-Now">[Download Vuze
    Now](https://web.archive.org/web/20190715182127/http://www.vuze.com/download)</span>

</div>

</div>

<div id="p-navigation" class="portal" role="navigation"
aria-labelledby="p-navigation-label">

### Navigation

<div class="body">

-   <span id="n-mainpage-description">[Main
    page](/web/20190715182127/http://wiki.vuze.com/w/Main_Page "Visit the main page [z]")</span>
-   <span id="n-recentchanges">[Recent
    changes](/web/20190715182127/http://wiki.vuze.com/w/Special:RecentChanges "A list of recent changes in the wiki [r]")</span>
-   <span id="n-randompage">[Random
    page](/web/20190715182127/http://wiki.vuze.com/w/Special:Random "Load a random page [x]")</span>
-   <span
    id="n-help">[Help](https://web.archive.org/web/20190715182127/https://www.mediawiki.org/wiki/Special:MyLanguage/Help:Contents "The place to find out")</span>

</div>

</div>

<div id="p-tb" class="portal" role="navigation"
aria-labelledby="p-tb-label">

### Tools

<div class="body">

-   <span id="t-whatlinkshere">[What links
    here](/web/20190715182127/http://wiki.vuze.com/w/Special:WhatLinksHere/Select_port_for_Vuze "A list of all wiki pages that link here [j]")</span>
-   <span id="t-recentchangeslinked">[Related
    changes](/web/20190715182127/http://wiki.vuze.com/w/Special:RecentChangesLinked/Select_port_for_Vuze "Recent changes in pages linked from this page [k]")</span>
-   <span id="t-specialpages">[Special
    pages](/web/20190715182127/http://wiki.vuze.com/w/Special:SpecialPages "A list of all special pages [q]")</span>
-   <span id="t-print">[Printable
    version](/web/20190715182127/http://wiki.vuze.com/mediawiki/index.php?title=Select_port_for_Vuze&printable=yes "Printable version of this page [p]")</span>
-   <span id="t-permalink">[Permanent
    link](/web/20190715182127/http://wiki.vuze.com/mediawiki/index.php?title=Select_port_for_Vuze&oldid=16173 "Permanent link to this revision of the page")</span>
-   <span id="t-info">[Page
    information](/web/20190715182127/http://wiki.vuze.com/mediawiki/index.php?title=Select_port_for_Vuze&action=info "More information about this page")</span>

</div>

</div>

</div>

</div>

<div id="footer" role="contentinfo">

-   <span id="footer-info-lastmod">This page was last modified on 3
    September 2014, at 19:54.</span>
-   <span id="footer-info-viewcount">This page has been accessed 379,508
    times.</span>

<!-- -->

-   <span id="footer-places-about">[About
    VuzeWiki](/web/20190715182127/http://wiki.vuze.com/w/VuzeWiki:About "VuzeWiki:About")</span>
-   <span
    id="footer-places-mobileview"><a href="https://web.archive.org/web/20190715182127/http://wiki.vuze.com/mediawiki/index.php?title=Select_port_for_Vuze&amp;mobileaction=toggle_view_mobile" class="noprint stopMobileRedirectToggle">Mobile view</a></span>

<!-- -->

-   <span
    id="footer-poweredbyico">[<img src="/web/20190715182127im_/http://wiki.vuze.com/mediawiki/resources/assets/poweredby_mediawiki_88x31.png" srcset="/web/20190715182127im_/http://wiki.vuze.com/mediawiki/resources/assets/poweredby_mediawiki_132x47.png 1.5x, /web/20190715182127im_/http://wiki.vuze.com/mediawiki/resources/assets/poweredby_mediawiki_176x62.png 2x" width="88" height="31" alt="Powered by MediaWiki" />](//web.archive.org/web/20190715182127/http://www.mediawiki.org/)</span>
-   <span id="footer-analyticsystemsico">Any use of Vuze® and Vuze+™
    that violates the rights of any person or entity is not allowed.
    [More](https://web.archive.org/web/20190715182127/http://vuze.com/corp/legal.php)</span>

<div style="clear:both">

</div>

</div>
