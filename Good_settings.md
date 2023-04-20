<div id="mw-page-base" class="noprint">

</div>

<div id="mw-head-base" class="noprint">

</div>

<div id="content" class="mw-body" role="main">

<span id="top"></span>

<div class="mw-indicators">

</div>

# Good settings

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

## <span id="Things_to_read_first" class="mw-headline">Things to read first</span><span class="mw-editsection"><span class="mw-editsection-bracket">\[</span>[edit](/web/20210508092340/http://wiki.vuze.com/mediawiki/index.php?title=Good_settings&action=edit&section=1 "Edit section: Things to read first")<span class="mw-editsection-bracket">\]</span></span>

Downloading as fast as your connection allows requires good settings
based on the **upload speed** of your Internet connection. First, fix
your [NAT
problem](/web/20210508092340/http://wiki.vuze.com/w/NAT_problem "NAT problem")
if you *never* see the green smiley
<a href="/web/20210508092340/http://wiki.vuze.com/w/File:HealthOk.gif" class="image"><img src="/web/20210508092340im_/http://wiki.vuze.com/mediawiki/images/3/30/HealthOk.gif" width="15" height="15" alt="HealthOk.gif" /></a>
as [torrent
health](/web/20210508092340/http://wiki.vuze.com/w/Torrent_health "Torrent health")
and do not [Force
Start](/web/20210508092340/http://wiki.vuze.com/w/Force_Start "Force Start")
your torrents. Running another
[P2P](/web/20210508092340/http://wiki.vuze.com/w/This_funny_word#P2P "This funny word")
program while Azureus is running will stall your downloads badly as they
will fight for the same bandwidth.

The following suggestions should work well most of the time. Downloads
of individual torrents also depend on other factors (see
<a href="/web/20210508092340/http://wiki.vuze.com/w/Good_Torrents" class="mw-redirect" title="Good Torrents">Good Torrents</a>).

<div id="toc" class="toc">

<div id="toctitle">

## Contents

</div>

-   [<span class="tocnumber">1</span> <span class="toctext">Things to
    read first</span>](#Things_to_read_first)
-   [<span class="tocnumber">2</span> <span class="toctext">Good
    settings based upload
    speed</span>](#Good_settings_based_upload_speed)
-   [<span class="tocnumber">3</span> <span class="toctext">How to
    determine your upload
    speed</span>](#How_to_determine_your_upload_speed)
-   [<span class="tocnumber">4</span> <span class="toctext">Test
    real-life torrent speed before
    complaining</span>](#Test_real-life_torrent_speed_before_complaining)
-   [<span class="tocnumber">5</span> <span class="toctext">Other things
    to know</span>](#Other_things_to_know)

</div>

## <span id="Good_settings_based_upload_speed" class="mw-headline">Good settings based upload speed</span><span class="mw-editsection"><span class="mw-editsection-bracket">\[</span>[edit](/web/20210508092340/http://wiki.vuze.com/mediawiki/index.php?title=Good_settings&action=edit&section=2 "Edit section: Good settings based upload speed")<span class="mw-editsection-bracket">\]</span></span>

*Note:* Find your upload speed at [next
chapter](#How_to_determine_your_upload_speed).

If the chart below does not list your upload speed, you might use a
calculator page or [get new settings using AzBot](#AzBot).

If you are running several file-sharing programs on the same internet
connection -- on one or more PCs -- you need to split the upload
bandwidth and calculate queue settings accordingly. When in doubt, ask
in the
<a href="/web/20210508092340/http://wiki.vuze.com/w/IRC" class="mw-redirect" title="IRC">IRC</a>
channel.

  
**Attention:** You need to change the User Proficiency Mode ([Mode
options](/web/20210508092340/http://wiki.vuze.com/w/UG_Options#Mode_options "UG Options"))
at least to "Intermediate" to be able to change all settings!

| Option                                                                                                               | Upload speed of internet connection in kbit/s |         |         |         |         |          |          |          |
|----------------------------------------------------------------------------------------------------------------------|-----------------------------------------------|---------|---------|---------|---------|----------|----------|----------|
| **Upload speed** in [kbit/s](/web/20210508092340/http://wiki.vuze.com/w/Data_units "Data units")                     | **128 3G(HSDPA)**                             | **128** | **256** | **512** | **768** | **1024** | **2048** | **5000** |
| *[Options -> Transfer](/web/20210508092340/http://wiki.vuze.com/w/UG_Options#Transfer_options "UG Options") options* |                                               |         |         |         |         |          |          |          |
| kB/s global max. upload speed                                                                                        | 6-11                                          | 12      | 25      | 51      | 76      | 100      | 200      | 400      |
| kB/s global max. download speed                                                                                      | 0                                             | 0       | 0       | 0       | 0       | 0        | 0        | 0        |
| Default max. upload slots per torrent                                                                                | 1-2                                           | 2       | 3       | 5       | 6       | 8        | 10       | 15       |
| Maximum number of connections per torrent                                                                            | 25                                            | 55      | 60      | 80      | 90      | 100      | 100      | 100      |
| Maximum number of connections globally                                                                               | 40                                            | 80      | 130     | 200     | 250     | 300      | 300      | 360      |
| *[Options -> Queue](/web/20210508092340/http://wiki.vuze.com/w/UG_Options#Queue_options "UG Options") options*       |                                               |         |         |         |         |          |          |          |
| max. simultaneous downloads                                                                                          | 1                                             | 1       | 2       | 2       | 2       | 3        | 4        | 4        |
| max. active torrents                                                                                                 | 1                                             | 1       | 2       | 2       | 3       | 4        | 6        | 6        |

See Options -> [Transfer
options](/web/20210508092340/http://wiki.vuze.com/w/UG_Options#Transfer_options "UG Options")
and Options -> [Queue
options](/web/20210508092340/http://wiki.vuze.com/w/UG_Options#Queue_options "UG Options").

In any case, do not let Azureus (or any other program for that matter)
take up the whole upload bandwidth. There needs to be room for overhead
such as acknowledgement signals (ACKs) and resend requests. Downloads
will suffer if these signals cannot be sent.

Set your upload limit to about 80% of the maximum possible. Setting your
upload too low may result in your torrents downloading slower, so it is
about finding a balance between the maximum speed and maintaining a low
enough latency for smooth internet usage.

## <span id="How_to_determine_your_upload_speed" class="mw-headline">How to determine your upload speed</span><span class="mw-editsection"><span class="mw-editsection-bracket">\[</span>[edit](/web/20210508092340/http://wiki.vuze.com/mediawiki/index.php?title=Good_settings&action=edit&section=3 "Edit section: How to determine your upload speed")<span class="mw-editsection-bracket">\]</span></span>

To configure Azureus for optimum performance, you need to know the
**upstream capacity** of your Internet connection, which can be obtained
from your Internet Service Provider (ISP). Advertisements may include
numbers like "1024/256 Kbps"; this represents the maximum bandwidth
available to you. It is the number of kilobits per second ([kbit/s or
Kbps](/web/20210508092340/http://wiki.vuze.com/w/Data_units "Data units"))
you can download/upload with your connection. You may have seen speed
measured in kiloBytes per second as commonly reported by browsers. There
is a difference between the two measures. In all likelihood, you upload
slower than you download.

**ISPs and most speedtests use kilobits/megabits, while Vuze uses
kiloBytes by default**.

1 Byte = 8 bits, 1 kB/s = 8 kbit/s = 8 kb/s. Small and capital 'B's do
matter.

You may visit
<a href="https://web.archive.org/web/20210508092340/http://www.speedtest.net/" class="external free">http://www.speedtest.net</a>
or
<a href="https://web.archive.org/web/20210508092340/http://www.dslreports.com/stest" class="external free">http://www.dslreports.com/stest</a>
or
<a href="https://web.archive.org/web/20210508092340/http://www.adslguide.org.uk/tools/speedtest.asp" class="external free">http://www.adslguide.org.uk/tools/speedtest.asp</a>
for online speed tests. Stop ALL Internet activity on your machine
(including torrents) for a few minutes before running a test. Repeat it
twice to reduce number anomalies. If it's close to one of the listed
upload speeds, use the [chart](#knownspeed). Otherwise, use
[AzBot](#AzBot) or a calculator page.

You can always set [Options ->
Transfer](/web/20210508092340/http://wiki.vuze.com/w/UG_Options#Transfer_options "UG Options")
\> **kB/s global max. upload speed** to 0 -- meaning unlimited -- and
observe what happens. Most likely it will reach your max. upload speed
and then start oscillating, as the too high uploading will cause traffic
jams.

## <span id="Test_real-life_torrent_speed_before_complaining" class="mw-headline">Test real-life torrent speed before complaining</span><span class="mw-editsection"><span class="mw-editsection-bracket">\[</span>[edit](/web/20210508092340/http://wiki.vuze.com/mediawiki/index.php?title=Good_settings&action=edit&section=4 "Edit section: Test real-life torrent speed before complaining")<span class="mw-editsection-bracket">\]</span></span>

If you get green smileys
<a href="/web/20210508092340/http://wiki.vuze.com/w/File:HealthOk.gif" class="image"><img src="/web/20210508092340im_/http://wiki.vuze.com/mediawiki/images/3/30/HealthOk.gif" width="15" height="15" alt="HealthOk.gif" /></a>
as torrents'
"[Health](/web/20210508092340/http://wiki.vuze.com/w/Torrent_health "Torrent health")",
then you know that your basic network settings are ok. However, that
doesn't guarantee speedy transfers.

It is good to understand that

-   **there is no central server** from which you download. Everything
    that users download, is at the same time uploaded by other users
-   **you contact other users** for your downloads
-   respectively, **others should be able to contact you** (NAT & port
    forwarding to be configured)

It is quite possible with a "new" torrent or an one with "small" swarm
(only a few peers), that the missing pieces are not
[available](/web/20210508092340/http://wiki.vuze.com/w/Availability "Availability").
So, it is quite possible that torrent remains active with "downloading"
status, but is not actively downloading anything as there is nobody to
download from.

Before thinking that your configuration is slow, test it with a "known
speedy" torrent. E.g. the following torrent has very high speed:
<a href="https://web.archive.org/web/20210508092340/http://releases.ubuntu.com/12.04/ubuntu-12.04-desktop-i386.iso.torrent" class="external free">http://releases.ubuntu.com/12.04/ubuntu-12.04-desktop-i386.iso.torrent</a>

It is a Ubuntu Linux distribution, which has lots of seeders, and you
should reach your internet connection's maximum speed in most cases
(especially with ADSL/cable home connections). Speeds well over 10
Mbit/s (= 1 MB/s as Vuze sees it) should be reachable. You don't have to
download the 600 MB torrent completely, but you can use it as a test
case for measuring maximum speeds of genuine torrents.

## <span id="Other_things_to_know" class="mw-headline">Other things to know</span><span class="mw-editsection"><span class="mw-editsection-bracket">\[</span>[edit](/web/20210508092340/http://wiki.vuze.com/mediawiki/index.php?title=Good_settings&action=edit&section=5 "Edit section: Other things to know")<span class="mw-editsection-bracket">\]</span></span>

Read about
<a href="/web/20210508092340/http://wiki.vuze.com/w/Good_Torrents" class="mw-redirect" title="Good Torrents">Good Torrents</a>.
(<a href="/web/20210508092340/http://wiki.vuze.com/w/Bad_torrents" class="mw-redirect" title="Bad torrents">Bad torrents</a>
may be fast at first, but you won't finish them.) You may want to
compare your download speed with the [Average Swarm
Speed](/web/20210508092340/http://wiki.vuze.com/w/Average_Swarm_Speed "Average Swarm Speed");
you may be doing better than you think.

<span class="small">Read the [Azureus
FAQ](/web/20210508092340/http://wiki.vuze.com/w/Azureus_FAQ "Azureus FAQ")</span>

</div>

<div class="printfooter">

Retrieved from
"[http://wiki.vuze.com/mediawiki/index.php?title=Good_settings&oldid=15947](https://web.archive.org/web/20210508092340/http://wiki.vuze.com/mediawiki/index.php?title=Good_settings&oldid=15947)"

</div>

<div id="catlinks" class="catlinks" mw="interface">

<div id="mw-normal-catlinks" class="mw-normal-catlinks">

[Categories](/web/20210508092340/http://wiki.vuze.com/w/Special:Categories "Special:Categories"):

-   [Troubleshooting](/web/20210508092340/http://wiki.vuze.com/w/Category:Troubleshooting "Category:Troubleshooting")
-   [Documentation](/web/20210508092340/http://wiki.vuze.com/w/Category:Documentation "Category:Documentation")
-   [User
    Guide](/web/20210508092340/http://wiki.vuze.com/w/Category:User_Guide "Category:User Guide")

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
    id="pt-anontalk">[Talk](/web/20210508092340/http://wiki.vuze.com/w/Special:MyTalk "Discussion about edits from this IP address [n]")</span>
-   <span
    id="pt-anoncontribs">[Contributions](/web/20210508092340/http://wiki.vuze.com/w/Special:MyContributions "A list of edits made from this IP address [y]")</span>
-   <span id="pt-createaccount">[Create
    account](/web/20210508092340/http://wiki.vuze.com/mediawiki/index.php?title=Special:CreateAccount&returnto=Good+settings "You are encouraged to create an account and log in; however, it is not mandatory")</span>
-   <span id="pt-login">[Log
    in](/web/20210508092340/http://wiki.vuze.com/mediawiki/index.php?title=Special:UserLogin&returnto=Good+settings "You are encouraged to log in; however, it is not mandatory [o]")</span>

</div>

<div id="left-navigation">

<div id="p-namespaces" class="vectorTabs" role="navigation"
aria-labelledby="p-namespaces-label">

### Namespaces

-   <span
    id="ca-nstab-main">[Page](/web/20210508092340/http://wiki.vuze.com/w/Good_settings "View the content page [c]")</span>
-   <span
    id="ca-talk">[Discussion](/web/20210508092340/http://wiki.vuze.com/w/Talk:Good_settings "Discussion about the content page [t]")</span>

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
    id="ca-view">[Read](/web/20210508092340/http://wiki.vuze.com/w/Good_settings)</span>
-   <span
    id="ca-edit">[Edit](/web/20210508092340/http://wiki.vuze.com/mediawiki/index.php?title=Good_settings&action=edit "Edit this page [e]")</span>
-   <span id="ca-history">[View
    history](/web/20210508092340/http://wiki.vuze.com/mediawiki/index.php?title=Good_settings&action=history "Past revisions of this page [h]")</span>

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

<a href="/web/20210508092340/http://wiki.vuze.com/w/Main_Page" class="mw-wiki-logo" title="Visit the main page"></a>

</div>

<div id="p-" class="portal" role="navigation"
aria-labelledby="p--label">

### 

<div class="body">

-   <span id="n-Download-Vuze-Now">[Download Vuze
    Now](https://web.archive.org/web/20210508092340/http://www.vuze.com/download)</span>

</div>

</div>

<div id="p-navigation" class="portal" role="navigation"
aria-labelledby="p-navigation-label">

### Navigation

<div class="body">

-   <span id="n-mainpage-description">[Main
    page](/web/20210508092340/http://wiki.vuze.com/w/Main_Page "Visit the main page [z]")</span>
-   <span id="n-recentchanges">[Recent
    changes](/web/20210508092340/http://wiki.vuze.com/w/Special:RecentChanges "A list of recent changes in the wiki [r]")</span>
-   <span id="n-randompage">[Random
    page](/web/20210508092340/http://wiki.vuze.com/w/Special:Random "Load a random page [x]")</span>
-   <span
    id="n-help">[Help](https://web.archive.org/web/20210508092340/https://www.mediawiki.org/wiki/Special:MyLanguage/Help:Contents "The place to find out")</span>

</div>

</div>

<div id="p-tb" class="portal" role="navigation"
aria-labelledby="p-tb-label">

### Tools

<div class="body">

-   <span id="t-whatlinkshere">[What links
    here](/web/20210508092340/http://wiki.vuze.com/w/Special:WhatLinksHere/Good_settings "A list of all wiki pages that link here [j]")</span>
-   <span id="t-recentchangeslinked">[Related
    changes](/web/20210508092340/http://wiki.vuze.com/w/Special:RecentChangesLinked/Good_settings "Recent changes in pages linked from this page [k]")</span>
-   <span id="t-specialpages">[Special
    pages](/web/20210508092340/http://wiki.vuze.com/w/Special:SpecialPages "A list of all special pages [q]")</span>
-   <span id="t-print">[Printable
    version](/web/20210508092340/http://wiki.vuze.com/mediawiki/index.php?title=Good_settings&printable=yes "Printable version of this page [p]")</span>
-   <span id="t-permalink">[Permanent
    link](/web/20210508092340/http://wiki.vuze.com/mediawiki/index.php?title=Good_settings&oldid=15947 "Permanent link to this revision of the page")</span>
-   <span id="t-info">[Page
    information](/web/20210508092340/http://wiki.vuze.com/mediawiki/index.php?title=Good_settings&action=info "More information about this page")</span>

</div>

</div>

</div>

</div>

<div id="footer" role="contentinfo">

-   <span id="footer-info-lastmod">This page was last modified on 19
    March 2014, at 19:47.</span>
-   <span id="footer-info-viewcount">This page has been accessed 411,115
    times.</span>

<!-- -->

-   <span id="footer-places-about">[About
    VuzeWiki](/web/20210508092340/http://wiki.vuze.com/w/VuzeWiki:About "VuzeWiki:About")</span>
-   <span
    id="footer-places-mobileview"><a href="https://web.archive.org/web/20210508092340/http://wiki.vuze.com/mediawiki/index.php?title=Good_settings&amp;mobileaction=toggle_view_mobile" class="noprint stopMobileRedirectToggle">Mobile view</a></span>

<!-- -->

-   <span
    id="footer-poweredbyico">[<img src="/web/20210508092340im_/http://wiki.vuze.com/mediawiki/resources/assets/poweredby_mediawiki_88x31.png" srcset="/web/20210508092340im_/http://wiki.vuze.com/mediawiki/resources/assets/poweredby_mediawiki_132x47.png 1.5x, /web/20210508092340im_/http://wiki.vuze.com/mediawiki/resources/assets/poweredby_mediawiki_176x62.png 2x" width="88" height="31" alt="Powered by MediaWiki" />](//web.archive.org/web/20210508092340/http://www.mediawiki.org/)</span>
-   <span id="footer-analyticsystemsico">Any use of Vuze® and Vuze+™
    that violates the rights of any person or entity is not allowed.
    [More](https://web.archive.org/web/20210508092340/http://vuze.com/corp/legal.php)</span>

<div style="clear:both">

</div>

</div>
