<div id="mw-page-base" class="noprint">

</div>

<div id="mw-head-base" class="noprint">

</div>

<div id="content" class="mw-body" role="main">

<span id="top"></span>

<div class="mw-indicators">

</div>

# This funny word

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

<div style="float:right;margin-left:8px;">

<div id="toc" class="toc">

<div id="toctitle">

## Contents

</div>

-   [<span class="tocnumber">1</span> <span
    class="toctext">Availability</span>](#Availability)
    -   [<span class="tocnumber">1.1</span> <span class="toctext">What
        does the Availability number tell
        you?</span>](#What_does_the_Availability_number_tell_you.3F)
    -   [<span class="tocnumber">1.2</span> <span
        class="toctext">Important things to
        note</span>](#Important_things_to_note)
-   [<span class="tocnumber">2</span> <span
    class="toctext">Choking</span>](#Choking)
-   [<span class="tocnumber">3</span> <span class="toctext">Data
    units</span>](#Data_units)
-   [<span class="tocnumber">4</span> <span
    class="toctext">DHT</span>](#DHT)
-   [<span class="tocnumber">5</span> <span
    class="toctext">Downloader</span>](#Downloader)
-   [<span class="tocnumber">6</span> <span
    class="toctext">Hash</span>](#Hash)
-   [<span class="tocnumber">7</span> <span
    class="toctext">ISP</span>](#ISP)
-   [<span class="tocnumber">8</span> <span
    class="toctext">Leech</span>](#Leech)
-   [<span class="tocnumber">9</span> <span class="toctext">Magnet
    Link</span>](#Magnet_Link)
-   [<span class="tocnumber">10</span> <span class="toctext">Multiple
    Hash Scrapes</span>](#Multiple_Hash_Scrapes)
-   [<span class="tocnumber">11</span> <span
    class="toctext">NAT</span>](#NAT)
-   [<span class="tocnumber">12</span> <span
    class="toctext">P2P</span>](#P2P)
-   [<span class="tocnumber">13</span> <span
    class="toctext">Peer</span>](#Peer)
-   [<span class="tocnumber">14</span> <span
    class="toctext">Piece</span>](#Piece)
-   [<span class="tocnumber">15</span> <span
    class="toctext">Ports</span>](#Ports)
-   [<span class="tocnumber">16</span> <span
    class="toctext">Scrape</span>](#Scrape)
-   [<span class="tocnumber">17</span> <span
    class="toctext">Seed</span>](#Seed)
-   [<span class="tocnumber">18</span> <span class="toctext">Seeding
    rank</span>](#Seeding_rank)
-   [<span class="tocnumber">19</span> <span class="toctext">Share
    ratio</span>](#Share_ratio)
-   [<span class="tocnumber">20</span> <span
    class="toctext">Snubbing</span>](#Snubbing)
-   [<span class="tocnumber">21</span> <span
    class="toctext">SSL</span>](#SSL)
-   [<span class="tocnumber">22</span> <span
    class="toctext">Superseeding</span>](#Superseeding)
-   [<span class="tocnumber">23</span> <span
    class="toctext">Swarm</span>](#Swarm)
-   [<span class="tocnumber">24</span> <span
    class="toctext">.torrent</span>](#.torrent)
-   [<span class="tocnumber">25</span> <span
    class="toctext">Tracker</span>](#Tracker)
-   [<span class="tocnumber">26</span> <span
    class="toctext">Unchoking</span>](#Unchoking)
-   [<span class="tocnumber">27</span> <span
    class="toctext">UPnP</span>](#UPnP)

</div>

</div>

**Some useful definitions of funny BitTorrent words and terms**

## <span id="Availability" class="mw-headline">Availability</span><span class="mw-editsection"><span class="mw-editsection-bracket">\[</span>[edit](/web/20210427182632/http://wiki.vuze.com/mediawiki/index.php?title=This_funny_word&action=edit&section=1 "Edit section: Availability")<span class="mw-editsection-bracket">\]</span></span>

### <span id="What_does_the_Availability_number_tell_you.3F" class="mw-headline">What does the Availability number tell you?</span><span class="mw-editsection"><span class="mw-editsection-bracket">\[</span>[edit](/web/20210427182632/http://wiki.vuze.com/mediawiki/index.php?title=Availability&action=edit&section=T-1 "Availability")<span class="mw-editsection-bracket">\]</span></span>

**Availability** is a per-torrent score like 0.640 or 37.989. The major
number of the *Availability* tells you how many copies of **the least
available piece** of the torrent you currently see. If the availability
is 1 or more, you see all of the pieces of the file(s). If it is 0, you
do not see the whole file(s). The decimals are most useful when the
Availability is below 1. Lets say availability is 0.652, that means
you're only seeing 65.2% of the file.

-   Availability reflects **your** **current** view to the torrent. It
    changes constantly based on the seeds & peers you are connected to.

Availability has a direct impact on download speed too. If you are
downloading a torrent with good availability, the speed is usually much
higher than in a torrent with only one source (as that the upload speed
of that source will then limit the whole swarm's download speed). You
can also see in the example image that speeds of individual torrents can
vary a lot.

**You can (and should) easily enable the *Availability* column:** just
go to *Library* tab in Vuze (or the *My Torrents* tab in Azureus),
right-click on the header row where the downloading torrents are queued
and choose [*Column
Setup*](/web/20210427182632/http://wiki.vuze.com/w/Column_setup "Column setup").
*Enable* the *Availability* column there and hit *OK*.

Doing this will give you a new column where you can easily spot the
*Availability* of the torrent. This is calculated based on the pieces
available from
[seeds](/web/20210427182632/http://wiki.vuze.com/w/This_funny_word#Seed "This funny word")
and
[peers](/web/20210427182632/http://wiki.vuze.com/w/This_funny_word#Peer "This funny word"),
that you're connected to.

Another option to see the *Availability* is to open the [torrent
details](/web/20210427182632/http://wiki.vuze.com/w/UG_Advanced_Information#General_tab "UG Advanced Information")
via *right-click \> Show Details* or doublecklicking on the torrent in
the *My Torrents* view. The *Availability* is displayed there as a
graphic bar and the Availability number itself on the right end of the
bar.

Availability shown in the Library view:

<a href="/web/20210427182632/http://wiki.vuze.com/w/File:Vuze42Availability.png" class="image"><img src="/web/20210427182632im_/http://wiki.vuze.com/mediawiki/images/4/4d/Vuze42Availability.png" width="590" height="184" alt="Vuze42Availability.png" /></a>

Examples:

-   **0.000** means that the
    [Tracker](/web/20210427182632/http://wiki.vuze.com/w/This_funny_word#Tracker "This funny word")
    is offline or doesn't track this torrent anymore and
    [DHT](/web/20210427182632/http://wiki.vuze.com/w/Distributed_hash_table "Distributed hash table")
    can't help either or there simply are no
    [seeds](/web/20210427182632/http://wiki.vuze.com/w/This_funny_word#Seed "This funny word")
    left (old torrent).
-   **0.249** means there are only parts of the torrent available (in
    this case 24.9%). Try to wait for
    [seeds](/web/20210427182632/http://wiki.vuze.com/w/This_funny_word#Seed "This funny word"),
    you might have to wait a day or so. Or it is very new and in
    [Superseeding](/web/20210427182632/http://wiki.vuze.com/w/This_funny_word#Superseeding "This funny word")
    mode
-   **0.640** and all other peers stuck at nearly the same percentage
    (\~64.0% in that case) means the torrent is either stuck because it
    lacks a seed or there is a very slow seed you're currently not
    connected to. Be patient, that torrent might finish, very slowly.
-   **0.999** (or something below 1 near that) means there is **almost**
    100% of the torrent available. This could be a
    anti-[leech](/web/20210427182632/http://wiki.vuze.com/w/This_funny_word#Leech "This funny word")-protection,
    meaning you just have to wait a few hours or days for it to get 100%
    of it. If you are already trying to get it for 2 weeks or so read
    the [Torrents stop at 99
    percent](/web/20210427182632/http://wiki.vuze.com/w/Torrents_stop_at_99_percent "Torrents stop at 99 percent")
    page.
-   **1.000** means that there is currently 100% of the torrent
    available. You are only able to download this torrent when the
    [seed](/web/20210427182632/http://wiki.vuze.com/w/This_funny_word#Seed "This funny word")
    won't go offline before you got all of it.
-   **1.539** *and* many peers stuck at \~53.9% (check the torrent
    details) means the swarm is either a [bad
    torrent](/web/20210427182632/http://wiki.vuze.com/w/Bad_torrent "Bad torrent")
    or the only
    [seed](/web/20210427182632/http://wiki.vuze.com/w/This_funny_word#Seed "This funny word")
    is very slow and everybody is waiting for new data from him, thus
    you'll reach 53.9% very fast but the remaining 46.1% will take quite
    some time (could be hours or days) while the original uploader
    slowly uploads it to peers.
-   **3.357** means there are some
    [seeds](/web/20210427182632/http://wiki.vuze.com/w/This_funny_word#Seed "This funny word")
    and
    [peers](/web/20210427182632/http://wiki.vuze.com/w/This_funny_word#Peer "This funny word")
    available and as you see at least 3 copies of each piece, you should
    be able to download the complete torrent, even if a seed stops
    seeding.
-   **37.989** means that you are downloading a torrent with a big
    [swarm](/web/20210427182632/http://wiki.vuze.com/w/This_funny_word#Swarm "This funny word").
    You see at least 37 copies of all data. If the [Average Swarm
    Speed](/web/20210427182632/http://wiki.vuze.com/w/Average_Swarm_Speed "Average Swarm Speed")
    is not too low you should be able to download it rather fast (partly
    depending on your upload too).

### <span id="Important_things_to_note" class="mw-headline">Important things to note</span><span class="mw-editsection"><span class="mw-editsection-bracket">\[</span>[edit](/web/20210427182632/http://wiki.vuze.com/mediawiki/index.php?title=Availability&action=edit&section=T-2 "Availability")<span class="mw-editsection-bracket">\]</span></span>

Note that a good (high) Availability does *not* necessarily mean that
it's a
<a href="/web/20210427182632/http://wiki.vuze.com/w/Good_torrents" class="mw-redirect" title="Good torrents">good torrent</a>
(and also read about
<a href="/web/20210427182632/http://wiki.vuze.com/w/Bad_torrents" class="mw-redirect" title="Bad torrents">Bad torrents</a>).
Another important thing is that seeds are NOT necessary to finish a
download since peers can have data to share too, only an Availability
above 1 (not counting cases with superseeds). That Availability \> 1.0
condition can be also reached with several peers having different pieces
of data, so that combined they have all the pieces.

It's perfectly normal not to connect to all
[seeds](/web/20210427182632/http://wiki.vuze.com/w/This_funny_word#Seed "This funny word")
and
[peers](/web/20210427182632/http://wiki.vuze.com/w/This_funny_word#Peer "This funny word")
in a swarm - more important is a good [Average Swarm
Speed](/web/20210427182632/http://wiki.vuze.com/w/Average_Swarm_Speed "Average Swarm Speed").

<span class="small">Read the [Azureus
FAQ](/web/20210427182632/http://wiki.vuze.com/w/Azureus_FAQ "Azureus FAQ")</span>

## <span id="Choking" class="mw-headline">Choking</span><span class="mw-editsection"><span class="mw-editsection-bracket">\[</span>[edit](/web/20210427182632/http://wiki.vuze.com/mediawiki/index.php?title=This_funny_word&action=edit&section=2 "Edit section: Choking")<span class="mw-editsection-bracket">\]</span></span>

-   **Choking:** This is something that is part of the BitTorrent
    protocol, in the network. **Choking is a signal that a
    [peer](/web/20210427182632/http://wiki.vuze.com/w/This_funny_word#Peer "This funny word")
    is not intending to send you any data, until you are unchoked.**
    This could be because the
    [peer](/web/20210427182632/http://wiki.vuze.com/w/This_funny_word#Peer "This funny word")
    is not ready, or not willing to fulfill your requests. When you are
    connected to a
    [peer](/web/20210427182632/http://wiki.vuze.com/w/This_funny_word#Peer "This funny word"),
    the connection contains information on 2 situations, one is choked
    or unchoked, the other is interested or not interested. **Interested
    means, that
    [peer](/web/20210427182632/http://wiki.vuze.com/w/This_funny_word#Peer "This funny word")
    has data that you do not have, and wish to acquire.** New
    connections to peers always begin as choked and not interested.
    Peers will unchoke connected peers who upload fast but are not
    interested. If the fast uploading peers subsequently become
    interested, then the worst uploader gets choked. If you are
    interested in what the
    [peer](/web/20210427182632/http://wiki.vuze.com/w/This_funny_word#Peer "This funny word")
    has, then that
    [peer](/web/20210427182632/http://wiki.vuze.com/w/This_funny_word#Peer "This funny word")'s
    client will calculate whether to send you the data, using
    information such as how fast you are uploading to other peers. When
    you are connected to many peers, you are never going to receive data
    from all of them at once. Sometimes data are sent to you from a
    particular
    [peer](/web/20210427182632/http://wiki.vuze.com/w/This_funny_word#Peer "This funny word"),
    sometimes that
    [peer](/web/20210427182632/http://wiki.vuze.com/w/This_funny_word#Peer "This funny word")
    sends to another
    [peer](/web/20210427182632/http://wiki.vuze.com/w/This_funny_word#Peer "This funny word")
    instead, who may then upload to you. **It is not possible for every
    [peer](/web/20210427182632/http://wiki.vuze.com/w/This_funny_word#Peer "This funny word")
    to share data with every other connected
    [peer](/web/20210427182632/http://wiki.vuze.com/w/This_funny_word#Peer "This funny word")
    at the same time**. The
    <a href="https://web.archive.org/web/20210427182632/http://en.wikipedia.org/wiki/Transmission_Control_Protocol" class="external text">TCP-Protocol</a>
    used in
    [BitTorrent](/web/20210427182632/http://wiki.vuze.com/w/BitTorrent "BitTorrent")
    to connect to other peers gets easily congested, and performs badly
    when sharing data over many connections at once. So **choking is
    used to limit that congestion**, and to help make sharing faster.
    Choking is also used to make sharing fairer to all, by ensuring that
    peers who upload more data faster to others get more data uploaded
    to them. So **the more you upload, the more you can download** from
    other peers. And **the less you upload, the more likely you are to
    be choked.** Also, read the info about
    [unchoking](/web/20210427182632/http://wiki.vuze.com/w/This_funny_word#Unchoking "This funny word").

## <span id="Data_units" class="mw-headline">Data units</span><span class="mw-editsection"><span class="mw-editsection-bracket">\[</span>[edit](/web/20210427182632/http://wiki.vuze.com/mediawiki/index.php?title=This_funny_word&action=edit&section=3 "Edit section: Data units")<span class="mw-editsection-bracket">\]</span></span>

-   **Bandwidth/Site Units**: Confused about Kib/sec, KiB/sec, kB, kb
    and so on? Have a look at the [Data
    units](/web/20210427182632/http://wiki.vuze.com/w/Data_units "Data units")
    page.

  

## <span id="DHT" class="mw-headline">DHT</span><span class="mw-editsection"><span class="mw-editsection-bracket">\[</span>[edit](/web/20210427182632/http://wiki.vuze.com/mediawiki/index.php?title=This_funny_word&action=edit&section=4 "Edit section: DHT")<span class="mw-editsection-bracket">\]</span></span>

-   **[DHT](/web/20210427182632/http://wiki.vuze.com/w/Distributed_hash_table "Distributed hash table"):**
    DHT is the acronym for 'Distributed Hash Table' and is the
    de-centralized tracking system used in Azureus 2.3.0.0 and later.
    The DHT has many uses, including but not limited to, finding peers
    while
    [trackers](/web/20210427182632/http://wiki.vuze.com/w/This_funny_word#Tracker "This funny word")
    are down, hosting completely trackerless torrents, and playing host
    to things like the 'Ratings and Comments' plug-in. You need to open
    the Incoming TCP
    [port](/web/20210427182632/http://wiki.vuze.com/w/Ports "Ports") for
    TCP and UDP traffic to make it work. You'll then get a green dot
    with a user count at the bottom of the Azureus GUI, which should
    display about 400000 users or more. See
    <a href="https://web.archive.org/web/20210427182632/http://en.wikipedia.org/wiki/Distributed_hash_table" class="external free">http://en.wikipedia.org/wiki/Distributed_hash_table</a>
    and
    <a href="https://web.archive.org/web/20210427182632/http://en.wikipedia.org/wiki/Kademlia" class="external free">http://en.wikipedia.org/wiki/Kademlia</a>
    for further technical information.

## <span id="Downloader" class="mw-headline">Downloader</span><span class="mw-editsection"><span class="mw-editsection-bracket">\[</span>[edit](/web/20210427182632/http://wiki.vuze.com/mediawiki/index.php?title=This_funny_word&action=edit&section=5 "Edit section: Downloader")<span class="mw-editsection-bracket">\]</span></span>

-   **Downloader:** a
    [peer](/web/20210427182632/http://wiki.vuze.com/w/This_funny_word#Peer "This funny word")
    in a
    [swarm](/web/20210427182632/http://wiki.vuze.com/w/This_funny_word#Swarm "This funny word")
    who has not finished the whole
    [torrent](/web/20210427182632/http://wiki.vuze.com/w/This_funny_word#.torrent "This funny word"),
    or has not finished all the files that have not been marked as "Do
    Not Download". In
    [BitTorrent](/web/20210427182632/http://wiki.vuze.com/w/BitTorrent "BitTorrent"),
    downloaders also upload to other peers, unless they are
    [leeches](/web/20210427182632/http://wiki.vuze.com/w/This_funny_word#Leech "This funny word").
    When a downloader completes the whole
    [torrent](/web/20210427182632/http://wiki.vuze.com/w/This_funny_word#.torrent "This funny word"),
    they become a
    [seed](/web/20210427182632/http://wiki.vuze.com/w/This_funny_word#Seed "This funny word")
    and then only upload to other peers in the swarm.

## <span id="Hash" class="mw-headline">Hash</span><span class="mw-editsection"><span class="mw-editsection-bracket">\[</span>[edit](/web/20210427182632/http://wiki.vuze.com/mediawiki/index.php?title=This_funny_word&action=edit&section=6 "Edit section: Hash")<span class="mw-editsection-bracket">\]</span></span>

-   **Hash:** the hash is a string of
    <a href="https://web.archive.org/web/20210427182632/http://en.wikipedia.org/wiki/Gobbledegook" class="external text">gobbledegook</a>
    characters in the
    [.torrent](/web/20210427182632/http://wiki.vuze.com/w/This_funny_word#.torrent "This funny word")
    file that the client uses to verify the data that is being
    transferred. It contains information like the file list, sizes,
    pieces, etc. Every piece received is first checked against the hash.
    If it fails verification, the data is discarded and requested again.
    The 'Hash Fails' field in the
    [torrent](/web/20210427182632/http://wiki.vuze.com/w/This_funny_word#.torrent "This funny word")
    General tab shows the number of these hash fails.

## <span id="ISP" class="mw-headline">ISP</span><span class="mw-editsection"><span class="mw-editsection-bracket">\[</span>[edit](/web/20210427182632/http://wiki.vuze.com/mediawiki/index.php?title=This_funny_word&action=edit&section=7 "Edit section: ISP")<span class="mw-editsection-bracket">\]</span></span>

<a href="https://web.archive.org/web/20210427182632/http://en.wikipedia.org/wiki/Internet_service_provider" class="external text">Internet service provider</a>.
Also read about [ISPs that are bad for
BT](/web/20210427182632/http://wiki.vuze.com/w/Bad_ISPs "Bad ISPs").

  

## <span id="Leech" class="mw-headline">Leech</span><span class="mw-editsection"><span class="mw-editsection-bracket">\[</span>[edit](/web/20210427182632/http://wiki.vuze.com/mediawiki/index.php?title=This_funny_word&action=edit&section=8 "Edit section: Leech")<span class="mw-editsection-bracket">\]</span></span>

-   **Leech:** an egoistic person who downloads a file using P2P
    technology, and who does **NOT** share (enough) with others when in
    possession of the complete file, reducing its
    [Availability](/web/20210427182632/http://wiki.vuze.com/w/Availability "Availability").
    Normally in
    [BitTorrent](/web/20210427182632/http://wiki.vuze.com/w/BitTorrent "BitTorrent"),
    it is polite and considerate to leave your connection open long
    after you finish downloading to
    **[seed](/web/20210427182632/http://wiki.vuze.com/w/This_funny_word#Seed "This funny word")** -
    so that other
    **[peers](/web/20210427182632/http://wiki.vuze.com/w/This_funny_word#Peer "This funny word")**
    in the
    **[swarm](/web/20210427182632/http://wiki.vuze.com/w/This_funny_word#Swarm "This funny word")**,
    who do NOT yet have the complete file yet, benefit from you sharing,
    as you did benefit from others sharing when you originally
    downloaded the
    [torrent](/web/20210427182632/http://wiki.vuze.com/w/This_funny_word#.torrent "This funny word").
    [Some share more, some share
    less](/web/20210427182632/http://wiki.vuze.com/w/Ignore_Rules "Ignore Rules"),
    but a leech is somebody who closes their connection as soon as they
    have downloaded the complete file. In the long run, your total
    [Share
    ratio](/web/20210427182632/http://wiki.vuze.com/w/Share_ratio "Share ratio")
    ([Statistics -> Transfers
    Tab](/web/20210427182632/http://wiki.vuze.com/w/UG_Statistics#Transfers_tab "UG Statistics"))
    should always be >1.000!

However, there is another interpretation of the term "leech" as being
any user who has not completed the torrent download (ie anybody who has
a percentage complete lower than 100% on a given torrent). Although Vuze
chooses to refer to these users as "peers" in their client, there are
official places (such as Demonoid) that still use "leech" in this
manner.

## <span id="Magnet_Link" class="mw-headline">Magnet Link</span><span class="mw-editsection"><span class="mw-editsection-bracket">\[</span>[edit](/web/20210427182632/http://wiki.vuze.com/mediawiki/index.php?title=This_funny_word&action=edit&section=9 "Edit section: Magnet Link")<span class="mw-editsection-bracket">\]</span></span>

-   **[Magnet
    Link](/web/20210427182632/http://wiki.vuze.com/w/Magnet "Magnet")**

## <span id="Multiple_Hash_Scrapes" class="mw-headline">Multiple Hash Scrapes</span><span class="mw-editsection"><span class="mw-editsection-bracket">\[</span>[edit](/web/20210427182632/http://wiki.vuze.com/mediawiki/index.php?title=This_funny_word&action=edit&section=10 "Edit section: Multiple Hash Scrapes")<span class="mw-editsection-bracket">\]</span></span>

-   **Multiple Hash Scrapes:** This is when, instead of Azureus scraping
    a
    [tracker](/web/20210427182632/http://wiki.vuze.com/w/This_funny_word#Tracker "This funny word")
    (from which you are running several torrents) separate times for
    each and every loaded
    [torrent](/web/20210427182632/http://wiki.vuze.com/w/This_funny_word#.torrent "This funny word"),
    Azureus can connect to that tracker one single time for *all* the
    loaded .torrents hosted on it. This is a tracker feature. This is a
    feature that is useful if you have more than one active
    [.torrent](/web/20210427182632/http://wiki.vuze.com/w/This_funny_word#.torrent "This funny word")
    which is hosted on the same tracker. Azureus can keep the connection
    to the tracker alive and do multiple scrapes during that single
    connection. This saves bandwidth, both for the tracker, and for you,
    since not so many connections need to be made. However, not all
    trackers support this feature. This is why, you may sometimes see a
    message in the tracker column in the "My Torrents" view, saying
    **Multiple hash scrapes not supported**. There is nothing you can do
    about this, nor is it something to get alarmed about. It simply
    means that Azureus will continue to scrape the tracker in the way it
    always has before, separate times for each
    [torrent](/web/20210427182632/http://wiki.vuze.com/w/This_funny_word#.torrent "This funny word").

  

## <span id="NAT" class="mw-headline">NAT</span><span class="mw-editsection"><span class="mw-editsection-bracket">\[</span>[edit](/web/20210427182632/http://wiki.vuze.com/mediawiki/index.php?title=This_funny_word&action=edit&section=11 "Edit section: NAT")<span class="mw-editsection-bracket">\]</span></span>

-   **NAT:** This is short for Network Address Translation. This means
    that the Network, (which consists of any and all hardware you have
    connected up together, such as your router and your computer) needs
    to Translate the IP address of your router (which has it's own IP
    address) to and from the IP address of your computer (which also has
    it's own, *different* IP address). In simpler terms, it's sort of
    like mail forwarding. The router is there to help protect you from
    what it thinks is unwanted traffic, it is sort of like the Post
    Office. Inside the router, the port forwarding instructions are like
    telling the postman to redirect your mail to a different address. So
    the original address from the outside world (WAN, or Wider Area
    Network) is the IP address of your router, that's what the postman
    sees on the labels of parcels and letters. Then the postman
    redirects your mail according to the instructions you gave, to your
    ACTUAL address, which is the real local IP address of your computer,
    in the LAN (Local Area Network). See below for how to find out what
    the actual IP of your computer is on Mac OS X. So when you get the
    error message **NAT Error**, this means that your router is NOT
    translating the IP address from your computer to and from the
    outside world IP address of your router. And this is why no
    information or downloads can occur until this is sorted out, because
    information can not pass between your computer and the router, and
    thus cannot pass to and from the outside world of the internet.
    Please see [NAT
    problem](/web/20210427182632/http://wiki.vuze.com/w/NAT_problem "NAT problem")
    and
    <a href="/web/20210427182632/http://wiki.vuze.com/w/PortForwarding" class="mw-redirect" title="PortForwarding">PortForwarding</a>
    for more information about this.

## <span id="P2P" class="mw-headline">P2P</span><span class="mw-editsection"><span class="mw-editsection-bracket">\[</span>[edit](/web/20210427182632/http://wiki.vuze.com/mediawiki/index.php?title=This_funny_word&action=edit&section=12 "Edit section: P2P")<span class="mw-editsection-bracket">\]</span></span>

-   **P2P:** is short for **Peer to Peer**, which is a technology to do
    with personal file sharing, which includes the like of BitTorrent,
    Gnutella, eDonkey, etc. Peer to Peer networks differ from other
    file-sharing networks in that there is no single centralized server.

## <span id="Peer" class="mw-headline">Peer</span><span class="mw-editsection"><span class="mw-editsection-bracket">\[</span>[edit](/web/20210427182632/http://wiki.vuze.com/mediawiki/index.php?title=This_funny_word&action=edit&section=13 "Edit section: Peer")<span class="mw-editsection-bracket">\]</span></span>

-   **Peer:** a person who is participating in file sharing. That is, a
    person who is transferring a file using P2P technology. Peers who
    have not already downloaded 100% of the torrent upload to other
    peers and download from them, while
    [seeds](/web/20210427182632/http://wiki.vuze.com/w/This_funny_word#Seed "This funny word")
    just upload to other peers, improving their own [Share
    ratio](/web/20210427182632/http://wiki.vuze.com/w/Share_ratio "Share ratio")
    that way to prevent becoming a
    [leech](/web/20210427182632/http://wiki.vuze.com/w/This_funny_word#Leech "This funny word").

## <span id="Piece" class="mw-headline">Piece</span><span class="mw-editsection"><span class="mw-editsection-bracket">\[</span>[edit](/web/20210427182632/http://wiki.vuze.com/mediawiki/index.php?title=This_funny_word&action=edit&section=14 "Edit section: Piece")<span class="mw-editsection-bracket">\]</span></span>

-   **Piece:** every
    [torrent](/web/20210427182632/http://wiki.vuze.com/w/This_funny_word#.torrent "This funny word")
    is divided up into a bunch of small, equally sized pieces. These
    pieces are then transferred in a generally random order. Different
    pieces are sent to different peers so that each
    [peer](/web/20210427182632/http://wiki.vuze.com/w/This_funny_word#Peer "This funny word")
    will have something the other peers do not, and the potential for
    trading is maximized to the fullest.

  

## <span id="Ports" class="mw-headline">Ports</span><span class="mw-editsection"><span class="mw-editsection-bracket">\[</span>[edit](/web/20210427182632/http://wiki.vuze.com/mediawiki/index.php?title=This_funny_word&action=edit&section=15 "Edit section: Ports")<span class="mw-editsection-bracket">\]</span></span>

You normally have only one physical connection to a network at a time,
but often use it for more than one thing, or logical connection, at a
time. Ports are used to tell the operating system, which logical
connection the received data packets are intended for.

For example, web browsing with Hyper Text Transfer Protocol (HTTP)
usually uses port 80 while File Transfer Protocol (FTP) normally uses
port 21. When you request a webpage, your computer sends a request
packet to port 80 on the server, as it expects the web site's server to
wait for your call at the default port. Port numbers run from 0 to
65535. Some of them are "reserved" for official purposes. You can go to
<a href="https://web.archive.org/web/20210427182632/http://ports.tantalo.net/" class="external free">http://ports.tantalo.net/</a>
, the
<a href="https://web.archive.org/web/20210427182632/http://www.iana.org/assignments/port-numbers" class="external text">official IANA port list</a>
and
<a href="https://web.archive.org/web/20210427182632/http://en.wikipedia.org/wiki/List_of_well_known_ports_(computing)" class="external free">http://en.wikipedia.org/wiki/List_of_well_known_ports_(computing)</a>
to find out more about which ports normally belong to which
protocol/program.

The general advice is to use a randomly selected port between
49160-65534. Please read [this
article](/web/20210427182632/http://wiki.vuze.com/w/Select_port_for_Vuze "Select port for Vuze")
for more information on which ports to use with Azureus.

Originally bittorrent implementations (like Vuze/Azureus) used the port
6881, but as some ISPs started to block that port, Vuze currently
recommends to use some other port and it randomly selects a port for a
new installation. The selected port number itself does not change the
functionality, as long as you configure your own network accordingly.
Read all about [port
forwarding](/web/20210427182632/http://wiki.vuze.com/w/Port_forwarding "Port forwarding").

Information about ports that [Vuze reserves by
default](/web/20210427182632/http://wiki.vuze.com/w/Select_port_for_Vuze#Which_ports_Vuze_uses_by_default.3F "Select port for Vuze").

  
<span class="small">Read the [Azureus
FAQ](/web/20210427182632/http://wiki.vuze.com/w/Azureus_FAQ "Azureus FAQ")</span>

  

## <span id="Scrape" class="mw-headline">Scrape</span><span class="mw-editsection"><span class="mw-editsection-bracket">\[</span>[edit](/web/20210427182632/http://wiki.vuze.com/mediawiki/index.php?title=This_funny_word&action=edit&section=16 "Edit section: Scrape")<span class="mw-editsection-bracket">\]</span></span>

See [Scrape](/web/20210427182632/http://wiki.vuze.com/w/Scrape "Scrape")

## <span id="Seed" class="mw-headline">Seed</span><span class="mw-editsection"><span class="mw-editsection-bracket">\[</span>[edit](/web/20210427182632/http://wiki.vuze.com/mediawiki/index.php?title=This_funny_word&action=edit&section=17 "Edit section: Seed")<span class="mw-editsection-bracket">\]</span></span>

-   **Seed:** a
    [peer](/web/20210427182632/http://wiki.vuze.com/w/This_funny_word#Peer "This funny word")
    who has 100% of the
    [torrent](/web/20210427182632/http://wiki.vuze.com/w/This_funny_word#.torrent "This funny word")
    and is only uploading to other peers. Seed is also used as a verb,
    as in "I'm going to be seeding this file overnight", meaning leave
    open and available for other users to download. Usually, a person
    with the whole file is a 'seed', while someone with a partial amount
    is a
    [peer](/web/20210427182632/http://wiki.vuze.com/w/This_funny_word#Peer "This funny word").
    Remember that **a seed is not a file server**. We're not talking
    about "magic seeds" here, so get any idea like that out of your
    mind. Connecting to more seeds does not necessarily mean that you'll
    finish downloading any faster. If you don't connect to all the seeds
    in a
    [swarm](/web/20210427182632/http://wiki.vuze.com/w/This_funny_word#Swarm "This funny word"),
    or even if you don't connect to any seeds, it does not mean Vuze is
    doing anything wrong. For any random
    [torrent](/web/20210427182632/http://wiki.vuze.com/w/This_funny_word#.torrent "This funny word"),
    you might download faster when connected only to 5 other
    [peers](/web/20210427182632/http://wiki.vuze.com/w/This_funny_word#Peer "This funny word")
    and no seeds than you might with some other random
    [torrent](/web/20210427182632/http://wiki.vuze.com/w/This_funny_word#.torrent "This funny word")
    while connected to 50 seeds and no other
    [peers](/web/20210427182632/http://wiki.vuze.com/w/This_funny_word#Peer "This funny word").
    Seeding torrents improves your [Share
    ratio](/web/20210427182632/http://wiki.vuze.com/w/Share_ratio "Share ratio").

## <span id="Seeding_rank" class="mw-headline">Seeding rank</span><span class="mw-editsection"><span class="mw-editsection-bracket">\[</span>[edit](/web/20210427182632/http://wiki.vuze.com/mediawiki/index.php?title=This_funny_word&action=edit&section=18 "Edit section: Seeding rank")<span class="mw-editsection-bracket">\]</span></span>

-   Seeding rank is a measurement of how urgent seeding of one torrent
    is against others. The higher the number, the more important it is
    for a given torrent to have more seeds, and the higher position it
    gets in the [seeding
    queue](/web/20210427182632/http://wiki.vuze.com/w/Torrents_queued "Torrents queued").
    This is a useful metric for deciding when to terminate seeding
    activity for a particular torrent. Or just use the [Ignore
    Rules](/web/20210427182632/http://wiki.vuze.com/w/Ignore_Rules "Ignore Rules")
    to do that automatically.

## <span id="Share_ratio" class="mw-headline">Share ratio</span><span class="mw-editsection"><span class="mw-editsection-bracket">\[</span>[edit](/web/20210427182632/http://wiki.vuze.com/mediawiki/index.php?title=This_funny_word&action=edit&section=19 "Edit section: Share ratio")<span class="mw-editsection-bracket">\]</span></span>

See [Share
ratio](/web/20210427182632/http://wiki.vuze.com/w/Share_ratio "Share ratio")

## <span id="Snubbing" class="mw-headline">Snubbing</span><span class="mw-editsection"><span class="mw-editsection-bracket">\[</span>[edit](/web/20210427182632/http://wiki.vuze.com/mediawiki/index.php?title=This_funny_word&action=edit&section=20 "Edit section: Snubbing")<span class="mw-editsection-bracket">\]</span></span>

-   **Snubbing:** This is something that any BitTorrent client does to a
    [peer](/web/20210427182632/http://wiki.vuze.com/w/This_funny_word#Peer "This funny word"),
    when that
    [peer](/web/20210427182632/http://wiki.vuze.com/w/This_funny_word#Peer "This funny word")
    tells you he will send you a requested block of data, but then fails
    to do so within a reasonable period of time (60 seconds for
    Azureus). **Snubbing is a way to indicate that a
    [peer](/web/20210427182632/http://wiki.vuze.com/w/This_funny_word#Peer "This funny word")
    is not trusted to fulfill requests for data.** Whereas choking is
    done from the network,
    [snubbing](/web/20210427182632/http://wiki.vuze.com/w/This_funny_word#Snubbing "This funny word")
    is done from the BitTorrent client. **Snubbing happens when a
    [peer](/web/20210427182632/http://wiki.vuze.com/w/This_funny_word#Peer "This funny word")
    promises to send data by unchoking us, but then does not send the
    promised and requested block within 1 minute.** Usually Azureus
    makes multiple requests to any one
    [peer](/web/20210427182632/http://wiki.vuze.com/w/This_funny_word#Peer "This funny word"),
    and queues them up, waiting for them to be fulfilled. When a
    [peer](/web/20210427182632/http://wiki.vuze.com/w/This_funny_word#Peer "This funny word")
    is snubbed, only one request is queued to the snubbed
    [peer](/web/20210427182632/http://wiki.vuze.com/w/This_funny_word#Peer "This funny word")
    at any one time. A peer is unsnubbed if they fulfill the one request
    they're given within 60 seconds. In some conditions, requests are
    not made from snubbed peers at all, such as when a torrent is almost
    complete and there are other unsnubbed peers available to make the
    requests from. The most likely reason for the offending peer is a
    misconfigured client. It may be uploading to too many peers without
    enough upload capacity.

## <span id="SSL" class="mw-headline">SSL</span><span class="mw-editsection"><span class="mw-editsection-bracket">\[</span>[edit](/web/20210427182632/http://wiki.vuze.com/mediawiki/index.php?title=This_funny_word&action=edit&section=21 "Edit section: SSL")<span class="mw-editsection-bracket">\]</span></span>

-   **SSL:** This is short for
    **<a href="https://web.archive.org/web/20210427182632/http://en.wikipedia.org/wiki/Secure_Sockets_Layer" class="external text">Secure Sockets Layer</a>**.
    This is a protocol developed by Netscape Communications. SSL makes
    it possible for encrypted, authenticated (i.e. by username and/or
    password) communication over the internet. It is possible to
    transmit private files this way. SSL is often used in communications
    between web browsers and web servers. For example, when you buy
    something over the internet, and you go to a secure page to enter
    your personal sensitive information such as credit card details, the
    URL beginning with "https" will indicate that this is an SSL
    connection. SSL is also used for people to securely access their
    home machines remotely when they are away from home.

## <span id="Superseeding" class="mw-headline">Superseeding</span><span class="mw-editsection"><span class="mw-editsection-bracket">\[</span>[edit](/web/20210427182632/http://wiki.vuze.com/mediawiki/index.php?title=This_funny_word&action=edit&section=22 "Edit section: Superseeding")<span class="mw-editsection-bracket">\]</span></span>

-   **Superseeding:** a feature that allows seeders who are the *only*
    seed in the swarm to solely seed pieces that are found nowhere else
    in the swarm. It works something like this: the superseeding client
    pretends not to be a seed, but pretends to be a
    [peer](/web/20210427182632/http://wiki.vuze.com/w/This_funny_word#Peer "This funny word")
    with an incomplete file. Then the client shares each piece with one
    [peer](/web/20210427182632/http://wiki.vuze.com/w/This_funny_word#Peer "This funny word")
    only. And that
    [peer](/web/20210427182632/http://wiki.vuze.com/w/This_funny_word#Peer "This funny word")
    can then share that piece with the swarm. This allows the
    superseeding client to maximise the efficiency of the upload by only
    sharing those pieces nobody else has. And because of some other
    things about the behaviour of superseeding, this function does not
    work at all well in swarms with one
    [peer](/web/20210427182632/http://wiki.vuze.com/w/This_funny_word#Peer "This funny word")
    and one seed only. So it is only good when the seeder is the *only*
    seed (usually the original uploader), and there are more than two
    peers. For more information please see [Seeding
    Rules](/web/20210427182632/http://wiki.vuze.com/w/Seeding_Rules "Seeding Rules").

Note: Do not enable super-seeding for a torrent where you are not the
only seed.

Read also: [Super
Seeding](/web/20210427182632/http://wiki.vuze.com/w/Super_Seeding "Super Seeding")

## <span id="Swarm" class="mw-headline">Swarm</span><span class="mw-editsection"><span class="mw-editsection-bracket">\[</span>[edit](/web/20210427182632/http://wiki.vuze.com/mediawiki/index.php?title=This_funny_word&action=edit&section=23 "Edit section: Swarm")<span class="mw-editsection-bracket">\]</span></span>

-   **Swarm:** the group of people,
    [seeds](/web/20210427182632/http://wiki.vuze.com/w/This_funny_word#Seed "This funny word")
    and
    [peers](/web/20210427182632/http://wiki.vuze.com/w/This_funny_word#Peer "This funny word"),
    who are active on a single
    [torrent](/web/20210427182632/http://wiki.vuze.com/w/This_funny_word#.torrent "This funny word").
    **It's perfectly normal NOT to connect to ALL
    [seeds](/web/20210427182632/http://wiki.vuze.com/w/This_funny_word#Seed "This funny word")
    and
    [peers](/web/20210427182632/http://wiki.vuze.com/w/This_funny_word#Peer "This funny word")
    in a swarm!** A good [Average Swarm
    Speed](/web/20210427182632/http://wiki.vuze.com/w/Average_Swarm_Speed "Average Swarm Speed")
    and
    [Availability](/web/20210427182632/http://wiki.vuze.com/w/Availability "Availability")
    are more important. If you see something like **5 (14)** in the
    seeds column it means that you are connected to 5 out of 14 seeds
    that are in the swarm - meaning that the
    [tracker](/web/20210427182632/http://wiki.vuze.com/w/This_funny_word#Tracker "This funny word")
    knows about 9 more seeds. If you see something like **12 (4)** it
    could mean the tracker knows about 4 seeds in the swarm, but thanks
    to
    [DHT](/web/20210427182632/http://wiki.vuze.com/w/Distributed_hash_table "Distributed hash table")
    you did connect to even more!

Please note that the total number of seeds and peers in the swarm is
just the tracker server's current knowledge. It is no absolute truth.
Some of the seeds/peers might already have closed their bittorrent
clients and are thus no longer active. There is a defined time delay
since last contact, after which the the tracker forgets about a
seed/peer.

## <span id=".torrent" class="mw-headline">.torrent</span><span class="mw-editsection"><span class="mw-editsection-bracket">\[</span>[edit](/web/20210427182632/http://wiki.vuze.com/mediawiki/index.php?title=This_funny_word&action=edit&section=24 "Edit section: .torrent")<span class="mw-editsection-bracket">\]</span></span>

-   **.torrent:** (aka. metafile) A .torrent file is a small text file
    that is used to start a torrent download. (A torrent is a set of
    data being shared.) The .torrent file contains information about the
    files included in the torrent, the address to the
    [tracker](/web/20210427182632/http://wiki.vuze.com/w/This_funny_word#Tracker "This funny word")
    server and error correction information.

## <span id="Tracker" class="mw-headline">Tracker</span><span class="mw-editsection"><span class="mw-editsection-bracket">\[</span>[edit](/web/20210427182632/http://wiki.vuze.com/mediawiki/index.php?title=This_funny_word&action=edit&section=25 "Edit section: Tracker")<span class="mw-editsection-bracket">\]</span></span>

-   **Tracker:** a tracker is a special server that contains the
    information needed for peers to connect to other peers. Trackers
    coordinate the
    [BitTorrent](/web/20210427182632/http://wiki.vuze.com/w/BitTorrent "BitTorrent")
    clients, and also keep track of statistics and verification
    information for each
    [torrent](/web/20210427182632/http://wiki.vuze.com/w/This_funny_word#.torrent "This funny word").
    Azureus contains its own built-in tracker, but there are a variety
    of other tracker software packages in use. If the tracker server
    goes down and you try to start a
    [torrent](/web/20210427182632/http://wiki.vuze.com/w/This_funny_word#.torrent "This funny word"),
    you won't be able to connect to the swarm. Usually tracker errors
    are temporary, so Azureus will keep trying to
    [scrape](/web/20210427182632/http://wiki.vuze.com/w/This_funny_word#Scrape "This funny word")/connect
    again until successful or the
    [torrent](/web/20210427182632/http://wiki.vuze.com/w/This_funny_word#.torrent "This funny word")
    is removed. Please do **NOT** use the **Manual Update** button! The
    more you click it, the more this will destabilize the tracker, and
    cause it to go offline for everybody. So for the most part, leave
    the Manual Update button alone. Clicking it won't speed up your
    downloads, [Good
    settings](/web/20210427182632/http://wiki.vuze.com/w/Good_settings "Good settings")
    will.

## <span id="Unchoking" class="mw-headline">Unchoking</span><span class="mw-editsection"><span class="mw-editsection-bracket">\[</span>[edit](/web/20210427182632/http://wiki.vuze.com/mediawiki/index.php?title=This_funny_word&action=edit&section=26 "Edit section: Unchoking")<span class="mw-editsection-bracket">\]</span></span>

-   **Unchoking** is a promise to send data. Unchoking normally happens
    like this:

**When you are downloading**, Azureus will unchoke to the optimal number
of unchokes for your connection, in this order:

1.  The optimum uploaders (who upload at least 256B/s)
2.  Peers you are interested in (unless they are snubbed, or they have
    reached a [Share
    ratio](/web/20210427182632/http://wiki.vuze.com/w/Share_ratio "Share ratio")
    of 1/10, which means that every 1 byte they upload allows them to
    download 10 bytes)
3.  Peers who have globally uploaded you the maximum amount of data

**When you are seeding** you will unchoke in this order:

1.  Peers who have uploaded the most the fastest
2.  Peers who have biggest portion of the file

Here are some points to note about unchoking:

1.  When you are a seed, snubbed peers will never get unchoked
2.  Azureus will not
    [snub](/web/20210427182632/http://wiki.vuze.com/w/This_funny_word#Snubbing "This funny word")
    any
    [peer](/web/20210427182632/http://wiki.vuze.com/w/This_funny_word#Peer "This funny word")
    when you are seeding
3.  Manually
    [snubbing](/web/20210427182632/http://wiki.vuze.com/w/This_funny_word#Snubbing "This funny word")
    someone can be done with a right (contextual) click on a selected
    [peer](/web/20210427182632/http://wiki.vuze.com/w/This_funny_word#Peer "This funny word")
    in the details view
4.  This can let you have some control over which peers you do *not*
    want to send data to.

## <span id="UPnP" class="mw-headline">UPnP</span><span class="mw-editsection"><span class="mw-editsection-bracket">\[</span>[edit](/web/20210427182632/http://wiki.vuze.com/mediawiki/index.php?title=This_funny_word&action=edit&section=27 "Edit section: UPnP")<span class="mw-editsection-bracket">\]</span></span>

See **[UPnP](/web/20210427182632/http://wiki.vuze.com/w/UPnP "UPnP")**

  
<span class="small">Read the [Azureus
FAQ](/web/20210427182632/http://wiki.vuze.com/w/Azureus_FAQ "Azureus FAQ")</span>

</div>

<div class="printfooter">

Retrieved from
"[http://wiki.vuze.com/mediawiki/index.php?title=This_funny_word&oldid=15787](https://web.archive.org/web/20210427182632/http://wiki.vuze.com/mediawiki/index.php?title=This_funny_word&oldid=15787)"

</div>

<div id="catlinks" class="catlinks" mw="interface">

<div id="mw-normal-catlinks" class="mw-normal-catlinks">

[Categories](/web/20210427182632/http://wiki.vuze.com/w/Special:Categories "Special:Categories"):

-   [Definitions](/web/20210427182632/http://wiki.vuze.com/w/Category:Definitions "Category:Definitions")
-   [Documentation](/web/20210427182632/http://wiki.vuze.com/w/Category:Documentation "Category:Documentation")
-   [Troubleshooting](/web/20210427182632/http://wiki.vuze.com/w/Category:Troubleshooting "Category:Troubleshooting")

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
    id="pt-anontalk">[Talk](/web/20210427182632/http://wiki.vuze.com/w/Special:MyTalk "Discussion about edits from this IP address [n]")</span>
-   <span
    id="pt-anoncontribs">[Contributions](/web/20210427182632/http://wiki.vuze.com/w/Special:MyContributions "A list of edits made from this IP address [y]")</span>
-   <span id="pt-createaccount">[Create
    account](/web/20210427182632/http://wiki.vuze.com/mediawiki/index.php?title=Special:CreateAccount&returnto=This+funny+word "You are encouraged to create an account and log in; however, it is not mandatory")</span>
-   <span id="pt-login">[Log
    in](/web/20210427182632/http://wiki.vuze.com/mediawiki/index.php?title=Special:UserLogin&returnto=This+funny+word "You are encouraged to log in; however, it is not mandatory [o]")</span>

</div>

<div id="left-navigation">

<div id="p-namespaces" class="vectorTabs" role="navigation"
aria-labelledby="p-namespaces-label">

### Namespaces

-   <span
    id="ca-nstab-main">[Page](/web/20210427182632/http://wiki.vuze.com/w/This_funny_word "View the content page [c]")</span>
-   <span
    id="ca-talk">[Discussion](/web/20210427182632/http://wiki.vuze.com/w/Talk:This_funny_word "Discussion about the content page [t]")</span>

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
    id="ca-view">[Read](/web/20210427182632/http://wiki.vuze.com/w/This_funny_word)</span>
-   <span
    id="ca-edit">[Edit](/web/20210427182632/http://wiki.vuze.com/mediawiki/index.php?title=This_funny_word&action=edit "Edit this page [e]")</span>
-   <span id="ca-history">[View
    history](/web/20210427182632/http://wiki.vuze.com/mediawiki/index.php?title=This_funny_word&action=history "Past revisions of this page [h]")</span>

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

<a href="/web/20210427182632/http://wiki.vuze.com/w/Main_Page" class="mw-wiki-logo" title="Visit the main page"></a>

</div>

<div id="p-" class="portal" role="navigation"
aria-labelledby="p--label">

### 

<div class="body">

-   <span id="n-Download-Vuze-Now">[Download Vuze
    Now](https://web.archive.org/web/20210427182632/http://www.vuze.com/download)</span>

</div>

</div>

<div id="p-navigation" class="portal" role="navigation"
aria-labelledby="p-navigation-label">

### Navigation

<div class="body">

-   <span id="n-mainpage-description">[Main
    page](/web/20210427182632/http://wiki.vuze.com/w/Main_Page "Visit the main page [z]")</span>
-   <span id="n-recentchanges">[Recent
    changes](/web/20210427182632/http://wiki.vuze.com/w/Special:RecentChanges "A list of recent changes in the wiki [r]")</span>
-   <span id="n-randompage">[Random
    page](/web/20210427182632/http://wiki.vuze.com/w/Special:Random "Load a random page [x]")</span>
-   <span
    id="n-help">[Help](https://web.archive.org/web/20210427182632/https://www.mediawiki.org/wiki/Special:MyLanguage/Help:Contents "The place to find out")</span>

</div>

</div>

<div id="p-tb" class="portal" role="navigation"
aria-labelledby="p-tb-label">

### Tools

<div class="body">

-   <span id="t-whatlinkshere">[What links
    here](/web/20210427182632/http://wiki.vuze.com/w/Special:WhatLinksHere/This_funny_word "A list of all wiki pages that link here [j]")</span>
-   <span id="t-recentchangeslinked">[Related
    changes](/web/20210427182632/http://wiki.vuze.com/w/Special:RecentChangesLinked/This_funny_word "Recent changes in pages linked from this page [k]")</span>
-   <span id="t-specialpages">[Special
    pages](/web/20210427182632/http://wiki.vuze.com/w/Special:SpecialPages "A list of all special pages [q]")</span>
-   <span id="t-print">[Printable
    version](/web/20210427182632/http://wiki.vuze.com/mediawiki/index.php?title=This_funny_word&printable=yes "Printable version of this page [p]")</span>
-   <span id="t-permalink">[Permanent
    link](/web/20210427182632/http://wiki.vuze.com/mediawiki/index.php?title=This_funny_word&oldid=15787 "Permanent link to this revision of the page")</span>
-   <span id="t-info">[Page
    information](/web/20210427182632/http://wiki.vuze.com/mediawiki/index.php?title=This_funny_word&action=info "More information about this page")</span>

</div>

</div>

</div>

</div>

<div id="footer" role="contentinfo">

-   <span id="footer-info-lastmod">This page was last modified on 26
    February 2014, at 19:14.</span>
-   <span id="footer-info-viewcount">This page has been accessed 203,539
    times.</span>

<!-- -->

-   <span id="footer-places-about">[About
    VuzeWiki](/web/20210427182632/http://wiki.vuze.com/w/VuzeWiki:About "VuzeWiki:About")</span>
-   <span
    id="footer-places-mobileview"><a href="https://web.archive.org/web/20210427182632/http://wiki.vuze.com/mediawiki/index.php?title=This_funny_word&amp;mobileaction=toggle_view_mobile" class="noprint stopMobileRedirectToggle">Mobile view</a></span>

<!-- -->

-   <span
    id="footer-poweredbyico">[<img src="/web/20210427182632im_/http://wiki.vuze.com/mediawiki/resources/assets/poweredby_mediawiki_88x31.png" srcset="/web/20210427182632im_/http://wiki.vuze.com/mediawiki/resources/assets/poweredby_mediawiki_132x47.png 1.5x, /web/20210427182632im_/http://wiki.vuze.com/mediawiki/resources/assets/poweredby_mediawiki_176x62.png 2x" width="88" height="31" alt="Powered by MediaWiki" />](//web.archive.org/web/20210427182632/http://www.mediawiki.org/)</span>
-   <span id="footer-analyticsystemsico">Any use of Vuze® and Vuze+™
    that violates the rights of any person or entity is not allowed.
    [More](https://web.archive.org/web/20210427182632/http://vuze.com/corp/legal.php)</span>

<div style="clear:both">

</div>

</div>
