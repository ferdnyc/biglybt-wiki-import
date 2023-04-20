<div id="mw-page-base" class="noprint">

</div>

<div id="mw-head-base" class="noprint">

</div>

<div id="content" class="mw-body" role="main">

<span id="top"></span>

<div class="mw-indicators">

</div>

# Speed Test FAQ

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

  

<div id="toc" class="toc">

<div id="toctitle">

## Contents

</div>

-   [<span class="tocnumber">1</span> <span
    class="toctext">Introduction</span>](#Introduction)
    -   [<span class="tocnumber">1.1</span> <span
        class="toctext">Running</span>](#Running)
    -   [<span class="tocnumber">1.2</span> <span class="toctext">How it
        works</span>](#How_it_works)
    -   [<span class="tocnumber">1.3</span> <span
        class="toctext">FAQ</span>](#FAQ)
    -   [<span class="tocnumber">1.4</span> <span
        class="toctext">ERRORS</span>](#ERRORS)

</div>

# <span id="Introduction" class="mw-headline">Introduction</span><span class="mw-editsection"><span class="mw-editsection-bracket">\[</span>[edit](/web/20170331115624/http://wiki.vuze.com/mediawiki/index.php?title=Speed_Test_FAQ&action=edit&section=1 "Edit section: Introduction")<span class="mw-editsection-bracket">\]</span></span>

The Speed Test service can be used for the following:

-   Determine the bit torrent protocol upload and download rates.
-   Determine if your ISP is limiting the BitTorrent protocol and if a
    light encryption can get around it.
-   Set the input parameters needed for the AutoSpeed beta.

## <span id="Running" class="mw-headline">Running</span><span class="mw-editsection"><span class="mw-editsection-bracket">\[</span>[edit](/web/20170331115624/http://wiki.vuze.com/mediawiki/index.php?title=Speed_Test_FAQ&action=edit&section=2 "Edit section: Running")<span class="mw-editsection-bracket">\]</span></span>

Start a Speed Test from the "**Tool**" menu item. It will be under the
Advanced tab for version 3.0 users. The panel below will appear.

  

<a href="/web/20170331115624/http://wiki.vuze.com/w/File:WikiSpeedTestPanel1.PNG" class="image"><img src="/web/20170331115624im_/http://wiki.vuze.com/mediawiki/images/2/2d/WikiSpeedTestPanel1.PNG" width="498" height="429" alt="WikiSpeedTestPanel1.PNG" /></a>

  

-   **Vuze speed test**: from the drop down menu, select either an
    upload or a download test.
-   **Press to test with encryption**: select either a standard
    unencrypted protocol, or use of light encryption.
-   Click **Run** to start the test.

<!-- -->

-   The **progress bar** indicates how much of the test has been
    completed. It measures the median rate for 20 seconds once it has
    reached a peak. But if the test is taking too long, it will abort
    after 60 seconds.

<!-- -->

-   You can **abort** a test at any time once it starts.

<!-- -->

-   The text box at the bottom updates once per second with the measured
    rates, and displays any error messages if they occur.

<!-- -->

-   The Speed Test panel requires an upload test to be done first before
    advancing to the second panel. Plan on doing just an upload test, or
    doing both an upload and download test.

<!-- -->

-   After running desired tests, use the **Next** button to advance to
    the second panel.

  
**The Second Panel:**

  
<a href="/web/20170331115624/http://wiki.vuze.com/w/File:WikiSpeedTestPanel2.PNG" class="image"><img src="/web/20170331115624im_/http://wiki.vuze.com/mediawiki/images/6/6e/WikiSpeedTestPanel2.PNG" width="497" height="430" alt="WikiSpeedTestPanel2.PNG" /></a>

  
Speed Test results are used by the AutoSpeed beta. The second panel
allows you to accept the Speed Test results, or over-ride the setting
with your own result.

-   The bytes/sec column indicates the recommended values based on the
    speed test result.
-   The bits/sec column displays what a US ISP would quote.
-   The confidence level column allows you to set how confident you are
    in the settings. See [Auto Speed
    Beta](/web/20170331115624/http://wiki.vuze.com/w/Auto_Speed_Beta "Auto Speed Beta")
    for a discussion of settings.
-   You need to click **Apply** to make the settings active.

  
**The Third (last) Panel:**

  
<a href="/web/20170331115624/http://wiki.vuze.com/w/File:WikiSpeedTestPanel3.PNG" class="image"><img src="/web/20170331115624im_/http://wiki.vuze.com/mediawiki/images/f/fd/WikiSpeedTestPanel3.PNG" width="498" height="430" alt="WikiSpeedTestPanel3.PNG" /></a>

  
This page indicates the settings used by the Vuze AutoSpeed. Click
**Finish** when done.

## <span id="How_it_works" class="mw-headline">How it works</span><span class="mw-editsection"><span class="mw-editsection-bracket">\[</span>[edit](/web/20170331115624/http://wiki.vuze.com/mediawiki/index.php?title=Speed_Test_FAQ&action=edit&section=3 "Edit section: How it works")<span class="mw-editsection-bracket">\]</span></span>

When you click **Run**,

-   the client contacts the auto-speed beta servers.
-   the servers send a challenge to determine if the request is from
    Vuze client.
-   the servers schedule a slot on a server. A slot should usually be
    available (scheduling could require up to 30 seconds).
-   When a testing slot is scheduled, your client will send a test-id to
    the server and get back a torrent file for the test.
-   The client at this point stops all running torrents, and limits
    anything which could interfere with the testing.
-   Once the torrent is started it will take a few seconds to ramp up to
    full speed.
-   After reaching the max speed for this network it will measure that
    speed for the next 20 seconds and use the median measured value as
    its result. Expect the result to vary by about 10% from the true
    value. The server also will limit all tests to 500 kbytes/sec to
    keep server side bandwidth reasonable.
-   This result is then used an input to the second panel with gives
    recommended values for the AutoSpeed beta.

## <span id="FAQ" class="mw-headline">FAQ</span><span class="mw-editsection"><span class="mw-editsection-bracket">\[</span>[edit](/web/20170331115624/http://wiki.vuze.com/mediawiki/index.php?title=Speed_Test_FAQ&action=edit&section=4 "Edit section: FAQ")<span class="mw-editsection-bracket">\]</span></span>

Q: The ISP says my linespeed is 4.5 Mbits/sec, but Speed Test only
measures 500 kbps?

A: The first thing to understand is that in the US, ISPs quote **bits**
per second, but Vuze is measuring **bytes** per second. Multiply bytes
per second by 8x to convert to bits per second. The second thing to
consider is the Speed Test servers limit all tests to 500 kbytes/sec to
keep the bandwidth use reasonable.

------------------------------------------------------------------------

Q: What if I see a higher speed running with encryption than without?

A: Some ISPs have limited the bit torrent protocol in the past. It is
possible that you might be using one of them. The encryption used with
SpeedTest is a light encryption, so even this test might still be
limited. Please see this page if you think your ISP is limiting the bit
torrent protocol.

## <span id="ERRORS" class="mw-headline">ERRORS</span><span class="mw-editsection"><span class="mw-editsection-bracket">\[</span>[edit](/web/20170331115624/http://wiki.vuze.com/mediawiki/index.php?title=Speed_Test_FAQ&action=edit&section=5 "Edit section: ERRORS")<span class="mw-editsection-bracket">\]</span></span>

Q: What if I see these errors (but everything else seems to be working)?

*Test failed: Test aborted: Could not download from any of the peers as
never unchoked by them*

*Test failed: Test aborted: Could not upload to any of the peers -
insufficient upload slots?*

A: Check if your ISP is on the [bad ISP
list](/web/20170331115624/http://wiki.vuze.com/w/Bad_ISPs "Bad ISPs").
Try using the encrypted test.

</div>

<div class="printfooter">

Retrieved from
"[http://wiki.vuze.com/mediawiki/index.php?title=Speed_Test_FAQ&oldid=9842](https://web.archive.org/web/20170331115624/http://wiki.vuze.com/mediawiki/index.php?title=Speed_Test_FAQ&oldid=9842)"

</div>

<div id="catlinks" class="catlinks" mw="interface">

<div id="mw-normal-catlinks" class="mw-normal-catlinks">

[Category](/web/20170331115624/http://wiki.vuze.com/w/Special:Categories "Special:Categories"):

-   [Documentation](/web/20170331115624/http://wiki.vuze.com/w/Category:Documentation "Category:Documentation")

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
    id="pt-anontalk">[Talk](/web/20170331115624/http://wiki.vuze.com/w/Special:MyTalk "Discussion about edits from this IP address [n]")</span>
-   <span
    id="pt-anoncontribs">[Contributions](/web/20170331115624/http://wiki.vuze.com/w/Special:MyContributions "A list of edits made from this IP address [y]")</span>
-   <span id="pt-createaccount">[Create
    account](/web/20170331115624/http://wiki.vuze.com/mediawiki/index.php?title=Special:CreateAccount&returnto=Speed+Test+FAQ "You are encouraged to create an account and log in; however, it is not mandatory")</span>
-   <span id="pt-login">[Log
    in](/web/20170331115624/http://wiki.vuze.com/mediawiki/index.php?title=Special:UserLogin&returnto=Speed+Test+FAQ "You are encouraged to log in; however, it is not mandatory [o]")</span>

</div>

<div id="left-navigation">

<div id="p-namespaces" class="vectorTabs" role="navigation"
aria-labelledby="p-namespaces-label">

### Namespaces

-   <span
    id="ca-nstab-main">[Page](/web/20170331115624/http://wiki.vuze.com/w/Speed_Test_FAQ "View the content page [c]")</span>
-   <span
    id="ca-talk">[Discussion](/web/20170331115624/http://wiki.vuze.com/mediawiki/index.php?title=Talk:Speed_Test_FAQ&action=edit&redlink=1 "Discussion about the content page [t]")</span>

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
    id="ca-view">[Read](/web/20170331115624/http://wiki.vuze.com/w/Speed_Test_FAQ)</span>
-   <span
    id="ca-edit">[Edit](/web/20170331115624/http://wiki.vuze.com/mediawiki/index.php?title=Speed_Test_FAQ&action=edit "Edit this page [e]")</span>
-   <span id="ca-history">[View
    history](/web/20170331115624/http://wiki.vuze.com/mediawiki/index.php?title=Speed_Test_FAQ&action=history "Past revisions of this page [h]")</span>

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

<a href="/web/20170331115624/http://wiki.vuze.com/w/Main_Page" class="mw-wiki-logo" title="Visit the main page"></a>

</div>

<div id="p-" class="portal" role="navigation"
aria-labelledby="p--label">

### 

<div class="body">

-   <span id="n-Download-Vuze-Now">[Download Vuze
    Now](https://web.archive.org/web/20170331115624/http://www.vuze.com/download)</span>

</div>

</div>

<div id="p-navigation" class="portal" role="navigation"
aria-labelledby="p-navigation-label">

### Navigation

<div class="body">

-   <span id="n-mainpage-description">[Main
    page](/web/20170331115624/http://wiki.vuze.com/w/Main_Page "Visit the main page [z]")</span>
-   <span id="n-recentchanges">[Recent
    changes](/web/20170331115624/http://wiki.vuze.com/w/Special:RecentChanges "A list of recent changes in the wiki [r]")</span>
-   <span id="n-randompage">[Random
    page](/web/20170331115624/http://wiki.vuze.com/w/Special:Random "Load a random page [x]")</span>
-   <span
    id="n-help">[Help](https://web.archive.org/web/20170331115624/https://www.mediawiki.org/wiki/Special:MyLanguage/Help:Contents "The place to find out")</span>

</div>

</div>

<div id="p-tb" class="portal" role="navigation"
aria-labelledby="p-tb-label">

### Tools

<div class="body">

-   <span id="t-whatlinkshere">[What links
    here](/web/20170331115624/http://wiki.vuze.com/w/Special:WhatLinksHere/Speed_Test_FAQ "A list of all wiki pages that link here [j]")</span>
-   <span id="t-recentchangeslinked">[Related
    changes](/web/20170331115624/http://wiki.vuze.com/w/Special:RecentChangesLinked/Speed_Test_FAQ "Recent changes in pages linked from this page [k]")</span>
-   <span id="t-specialpages">[Special
    pages](/web/20170331115624/http://wiki.vuze.com/w/Special:SpecialPages "A list of all special pages [q]")</span>
-   <span id="t-print">[Printable
    version](/web/20170331115624/http://wiki.vuze.com/mediawiki/index.php?title=Speed_Test_FAQ&printable=yes "Printable version of this page [p]")</span>
-   <span id="t-permalink">[Permanent
    link](/web/20170331115624/http://wiki.vuze.com/mediawiki/index.php?title=Speed_Test_FAQ&oldid=9842 "Permanent link to this revision of the page")</span>
-   <span id="t-info">[Page
    information](/web/20170331115624/http://wiki.vuze.com/mediawiki/index.php?title=Speed_Test_FAQ&action=info "More information about this page")</span>

</div>

</div>

</div>

</div>

<div id="footer" role="contentinfo">

-   <span id="footer-info-lastmod">This page was last modified on 17
    November 2010, at 23:39.</span>
-   <span id="footer-info-viewcount">This page has been accessed 6,686
    times.</span>

<!-- -->

-   <span id="footer-places-about">[About
    VuzeWiki](/web/20170331115624/http://wiki.vuze.com/w/VuzeWiki:About "VuzeWiki:About")</span>
-   <span
    id="footer-places-mobileview"><a href="https://web.archive.org/web/20170331115624/http://wiki.vuze.com/mediawiki/index.php?title=Speed_Test_FAQ&amp;mobileaction=toggle_view_mobile" class="noprint stopMobileRedirectToggle">Mobile view</a></span>

<!-- -->

-   <span
    id="footer-poweredbyico">[<img src="/web/20170331115624im_/http://wiki.vuze.com/mediawiki/resources/assets/poweredby_mediawiki_88x31.png" srcset="/web/20170331115624im_/http://wiki.vuze.com/mediawiki/resources/assets/poweredby_mediawiki_132x47.png 1.5x, /web/20170331115624im_/http://wiki.vuze.com/mediawiki/resources/assets/poweredby_mediawiki_176x62.png 2x" width="88" height="31" alt="Powered by MediaWiki" />](//web.archive.org/web/20170331115624/http://www.mediawiki.org/)</span>
-   <span id="footer-analyticsystemsico">Any use of Vuze® and Vuze+™
    that violates the rights of any person or entity is not allowed.
    [More](https://web.archive.org/web/20170331115624/http://vuze.com/corp/legal.php)</span>

<div style="clear:both">

</div>

</div>
