<div id="mw-page-base" class="noprint">

</div>

<div id="mw-head-base" class="noprint">

</div>

<div id="content" class="mw-body" role="main">

<span id="top"></span>

<div class="mw-indicators">

</div>

# Vuze disappears

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
-   [<span class="tocnumber">2</span> <span class="toctext">Known
    Causes</span>](#Known_Causes)
    -   [<span class="tocnumber">2.1</span> <span class="toctext">SWT
        Browser Issues</span>](#SWT_Browser_Issues)
-   [<span class="tocnumber">3</span> <span class="toctext">Debug
    Procedure</span>](#Debug_Procedure)

</div>

## <span id="Introduction" class="mw-headline">Introduction</span><span class="mw-editsection"><span class="mw-editsection-bracket">\[</span>[edit](/web/20190715182507/http://wiki.vuze.com/mediawiki/index.php?title=Vuze_disappears&action=edit&section=1 "Edit section: Introduction")<span class="mw-editsection-bracket">\]</span></span>

If you have received the error message "Vuze did not shutdown tidily"
after you intentionally turned your computer off, you might read [the
article about possible reasons for that
message](/web/20190715182507/http://wiki.vuze.com/w/Vuze_did_not_shutdown_tidily "Vuze did not shutdown tidily").

The current article is more focused on the case, where Vuze disappears
in the middle of your computer session.

If you find that Vuze keeps crashing, it may be because something is
wrong with Vuze, or something external is making it crash. Look at the
suggestions below first to see if any of the below applications are
causing Vuze to crash. Otherwise, you can search and post in the
<a href="https://web.archive.org/web/20190715182507/http://forum.vuze.com/forum.jspa?forumID=3" class="external text">forum</a>
(attaching the debug logs will also be useful).

## <span id="Known_Causes" class="mw-headline">Known Causes</span><span class="mw-editsection"><span class="mw-editsection-bracket">\[</span>[edit](/web/20190715182507/http://wiki.vuze.com/mediawiki/index.php?title=Vuze_disappears&action=edit&section=2 "Edit section: Known Causes")<span class="mw-editsection-bracket">\]</span></span>

-   Embedded web browser bugs triggered by html content within Vuze. One
    thing to try is disabling adverts within Vuze by doing the following

<!-- -->

-   Open the options dialog via the Tools menu 'Options...' item
-   Click on the 'Plugins' entry in the tree on the left to show the
    plugin list on the right
-   Locate the 'Promo View' line and **uncheck** the 'Load at Startup'
    box:

<a href="/web/20190715182507/http://wiki.vuze.com/w/File:PromoViewOff.png" class="image"><img src="/web/20190715182507im_/http://wiki.vuze.com/mediawiki/images/4/45/PromoViewOff.png" width="535" height="128" alt="PromoViewOff.png" /></a>

-   Restart Vuze

<!-- -->

-   Outdated old
    [Java](/web/20190715182507/http://wiki.vuze.com/w/Java "Java")
    version.
    <a href="https://web.archive.org/web/20190715182507/http://www.java.com/en/download/installed.jsp?detect=jre&amp;try=1" class="external text">Update your java</a>
    to the current version (Java 7 update 40 also referred to as
    1.7.0_40 or OpenJDK 7u40, as of September 2013). Please note that
    Sun Java 6.x is no longer supported by Sun/Oracle. An update to Java
    7 (or higher, when available) is recommended.
-   Internet Explorer 5, 6 or 7. Old versions may not be fully
    compatible with current Vuze features. Use
    <a href="https://web.archive.org/web/20190715182507/http://windowsupdate.microsoft.com/" class="external text">WindowsUpdate</a>
    to update to Internet Explorer 8 or to the recently released
    Internet Explorer 9.

<!-- -->

-   Note: Please note that in Windows environment Vuze uses Internet
    Explorer components to display the search results and other web-like
    content despite the browser that you use for normal web browsing.
    So, even if you use Firefox or Chrome for surfing the web, Internet
    Explorer plays a role inside Vuze.

<!-- -->

-   Additional note: Also check your Internet Explorer's "proxy
    settings". There have been reports that some viruses have changed
    the IE proxy settings (in "Internet Options" of Windows) and that
    might also explain why some content is not shown.

<!-- -->

-   Safari 3 or other old versions. Update to current version (5.1.10 as
    of September 2013) at
    <a href="https://web.archive.org/web/20190715182507/http://support.apple.com/downloads/#safari" class="external free">http://support.apple.com/downloads/#safari</a>
-   Zone Alarm - old versions, see [Zone
    Alarm](/web/20190715182507/http://wiki.vuze.com/w/Zone_Alarm "Zone Alarm")
    and update to current version
-   Other DLL specific problems listed below:

<!-- -->

-   **AxShlex.dll** : Alcohol 120%
    *Latest:* Java 1.6.0 Update 4 solved this issue (and many others it
    seems) - please update to the latest Java 7 from
    <a href="https://web.archive.org/web/20190715182507/http://www.java.com/" class="external free">http://www.java.com</a>
    *Note:* Alcohol 120% is especially troublesome in combination with
    Java 1.6.0 Update 1. There are several ways to fix the issue:
    -   rename/delete AxShlex.dll that it doesn't get loaded (alcohol
        itself will continue to work)
    -   don't download torrents that contain files which are associated
        with alcohol 120%, such as *.MDS* files
    -   remove all ?Shell Extensions" within the Alcohol settings panel
        by going to (File > Options > Virtual Drive > Shell Extensions
        subitem), then click on 'Remove All'.
    -   uninstall Alcohol 120%
    -   downgrade to a previous java version (NOT recommended due to
        security issues, plus this might not work in all cases)
    -   run Vuze with the flag -Xcheck:jni - this traps the native
        floating point error causing the crash but has performance
        overheads
-   **BfLLR.dll** : Bigfoot Killer LSP (see Killer Gaming website)
-   **D3DIM700.DLL** : Microsoft DirectX 3D - upgrade to latest Java
    (see
    <a href="https://web.archive.org/web/20190715182507/http://bugs.sun.com/bugdatabase/view_bug.do?bug_id=6275887" class="external text">Java bug 6275887</a>).
    Also
    <a href="https://web.archive.org/web/20190715182507/http://www.microsoft.com/directx/" class="external text">update Microsoft DirectX components</a>.
-   **Flash.ocx** : Adobe Flash player, which is used for displaying
    Vuze media browsing experienece through embedded IE components.
    <a href="https://web.archive.org/web/20190715182507/http://get.adobe.com/flashplayer/" class="external text">Update Flash player</a>
    and check through
    <a href="https://web.archive.org/web/20190715182507/http://windowsupdate.microsoft.com/" class="external text">WindowsUpdate</a>
    that your browser (IE?) is fully updated.
-   **FPServiceProvider.dll** : FoxyProxy Video Add-on
-   **ForceInterfaceLSP.dll** : HMA! Pro VPN. See forum discussion:
    <a href="https://web.archive.org/web/20190715182507/http://forum.vuze.com/thread.jspa?threadID=96014" class="external free">http://forum.vuze.com/thread.jspa?threadID=96014</a>
-   **gapsp.dll** : Juniper Networks Neoteris client
-   **HMIPCore.dll** : HideMyIP
-   **iFW_Xfilter.dll**: iolo Firewall
-   **imon.dll** : configure NOD32 firewall properly
-   **InjHook12.dll** : Torrent Ratio Keeper
    (<a href="https://web.archive.org/web/20190715182507/http://www.torrentratiokeeper.c0m/" class="external free">http://www.torrentratiokeeper.c0m</a>)
-   **jvm.dll** or **ntdll.dll**: raise the issue with Sun (
    <a href="https://web.archive.org/web/20190715182507/http://bugs.sun.com/bugdatabase/index.jsp" class="external free">http://bugs.sun.com/bugdatabase/index.jsp</a>
    )
-   **libxul.so**: Linux systems may require Xulrunner components to be
    installed separately with Firefox 4. See [this
    article](/web/20190715182507/http://wiki.vuze.com/w/There_was_a_problem_loading_this_page#Linux "There was a problem loading this page").
-   **mclsp.dll** : McAfee - uninstall the privacy service
-   **mshtml.dll**: part of Microsoft IE (in your Windows), which Vuze
    uses for displaying web content. Check that IE is properly updated.
-   **MxAVLsp.dll** : VCom Fix-It Utilities
-   **netdog.dll** : Armor2net personal firewall
-   **niphk.dll**: you might have to uninstall Norman Anti-virus
    completely.
-   **nl_lsp.dll** : NetLimiter - uninstall
-   **nvappfilter.dll**: please uninstall the NVIDIA Firewall and/or
    make Vuze run with only one cpu.
    -   (To make Vuze run only on one cpu, open the Task Manager (press
        ctrl-alt-del) and select the Processes tab. Right-click
        *azureus.exe* and click *set affinity*. Then uncheck all but one
        of the cpus (it shouldn't matter which). Click ok.)
-   **nvLsp.dll** : NVIDIA nTune / ForceWare
-   **radhslib.dll** : Naomi internet filter from Radiant
-   **sarah.dll** : FRITZ! Application Layer Firewall
-   **SBLSP.dll** : SPEEDBit Video Accelerator
-   **SDHook32.dll** : Spybot - search & destroy
-   **Sendori.dll** : See
    <a href="https://web.archive.org/web/20190715182507/http://www.sendori.com/consumer_problem.html" class="external free">http://www.sendori.com/consumer_problem.html</a>
-   **urlmon.dll**: part of Microsoft IE (in your Windows), which Vuze
    uses for displaying web content. Check that IE is properly updated.
-   **vlsp.dll** : Venturi firewall or V-ONE SmartPass software (or
    possibly also Nvidia Network Access Manager)
-   **Winsflt.dll** : PureSight Internet Content Filter

*Note for developers:* The .dlls listed here don't necessarily cause the
crashes, they're just indicators for the presence of problematic
applications.

### <span id="SWT_Browser_Issues" class="mw-headline">SWT Browser Issues</span><span class="mw-editsection"><span class="mw-editsection-bracket">\[</span>[edit](/web/20190715182507/http://wiki.vuze.com/mediawiki/index.php?title=Vuze_disappears&action=edit&section=3 "Edit section: SWT Browser Issues")<span class="mw-editsection-bracket">\]</span></span>

With the 5.6.0.0 update a number of **Windows** users have been
experiencing Vuze crashes (particularly on startup) that can be traced
back the browser used to display web-based views in the client. On
Windows this is always Internet Explorer (regardless of what you may
have configured within Windows itself as your default browser).

Logic was added at version 5.6.1.0 to analyse crash dumps for evidence
of them being caused by an internal browser error. If so then use of the
internal browser within Vuze is automatically disabled. Normally you
would join the
[Beta_Program](/web/20190715182507/http://wiki.vuze.com/w/Beta_Program "Beta Program")
to install the latest updates but if Vuze crashes on startup you won't
be able to do this - please manually install the update from
<a href="https://web.archive.org/web/20190715182507/http://dev.vuze.com/" class="external free">http://dev.vuze.com/</a>

Once on the latest beta Vuze should automatically disable the internal
browser and hopefully run successfully. If not please try manually
disabling the browser by creating some [Configuration
Presets](/web/20190715182507/http://wiki.vuze.com/w/Configuration_directory#Configuration_Presets "Configuration directory").
You will need to enter the following into the presets file:

<div style="text-align:right; margin-bottom:-37px;">

Copy to Clipboard

</div>

```
browser.internal.disable=bool:true
```

**To re-enable the internal browser when Vuze is running do the
following:**

-   Ensure your user 'Mode' is set to 'Advanced': Tools->Options->Mode
-   Go to Tools->Options->Interface->Display, look for the 'Internal
    Browser' section towards the bottom and deselect the 'disable
    internal browser' checkbox.

<div style="text-align:right; margin-bottom:-37px;">

Copy to Clipboard

</div>

```
No restart is required for this to take affect for new views (restart required to reset existing ones)
```

## <span id="Debug_Procedure" class="mw-headline">Debug Procedure</span><span class="mw-editsection"><span class="mw-editsection-bracket">\[</span>[edit](/web/20190715182507/http://wiki.vuze.com/mediawiki/index.php?title=Vuze_disappears&action=edit&section=4 "Edit section: Debug Procedure")<span class="mw-editsection-bracket">\]</span></span>

If you want to file a [bug
report](/web/20190715182507/http://wiki.vuze.com/w/Bug_reporting "Bug reporting")
please include the hs_err_pid\<nnn>.log file.

1.  Check **hs_err_pid\<nnn>.log** files, these may be in the Vuze
    program directory or in %user%\\local\\temp. These files are created
    by java system as java crash logs. It is possible that it will help
    you identifying the cause of the crash.
    The key part is looking for the java/DLL call stack thread leading
    to the crash. There should be something like:
    JRE version: 6.0_15-b03
    Java VM: Java HotSpot(TM) Client VM (14.1-b02 mixed mode, sharing
    windows-x86 )
    **Problematic frame:**
    **C Flash.ocx+0x54377**
    In the example's case the crash is caused by Adobe Flash player
    (used for displaying Vuze media browsing experienece through
    embedded IE components.)
2.  **Identify the failing DLL**. Consider removing the problematic
    application to see if that would help.

See
[Submit_Debug](/web/20190715182507/http://wiki.vuze.com/w/Submit_Debug "Submit Debug")

</div>

<div class="printfooter">

Retrieved from
"[http://wiki.vuze.com/mediawiki/index.php?title=Vuze_disappears&oldid=16701](https://web.archive.org/web/20190715182507/http://wiki.vuze.com/mediawiki/index.php?title=Vuze_disappears&oldid=16701)"

</div>

<div id="catlinks" class="catlinks" mw="interface">

<div id="mw-normal-catlinks" class="mw-normal-catlinks">

[Category](/web/20190715182507/http://wiki.vuze.com/w/Special:Categories "Special:Categories"):

-   [Troubleshooting](/web/20190715182507/http://wiki.vuze.com/w/Category:Troubleshooting "Category:Troubleshooting")

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
    id="pt-anontalk">[Talk](/web/20190715182507/http://wiki.vuze.com/w/Special:MyTalk "Discussion about edits from this IP address [n]")</span>
-   <span
    id="pt-anoncontribs">[Contributions](/web/20190715182507/http://wiki.vuze.com/w/Special:MyContributions "A list of edits made from this IP address [y]")</span>
-   <span id="pt-createaccount">[Create
    account](/web/20190715182507/http://wiki.vuze.com/mediawiki/index.php?title=Special:CreateAccount&returnto=Vuze+disappears "You are encouraged to create an account and log in; however, it is not mandatory")</span>
-   <span id="pt-login">[Log
    in](/web/20190715182507/http://wiki.vuze.com/mediawiki/index.php?title=Special:UserLogin&returnto=Vuze+disappears "You are encouraged to log in; however, it is not mandatory [o]")</span>

</div>

<div id="left-navigation">

<div id="p-namespaces" class="vectorTabs" role="navigation"
aria-labelledby="p-namespaces-label">

### Namespaces

-   <span
    id="ca-nstab-main">[Page](/web/20190715182507/http://wiki.vuze.com/w/Vuze_disappears "View the content page [c]")</span>
-   <span
    id="ca-talk">[Discussion](/web/20190715182507/http://wiki.vuze.com/w/Talk:Vuze_disappears "Discussion about the content page [t]")</span>

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
    id="ca-view">[Read](/web/20190715182507/http://wiki.vuze.com/w/Vuze_disappears)</span>
-   <span
    id="ca-edit">[Edit](/web/20190715182507/http://wiki.vuze.com/mediawiki/index.php?title=Vuze_disappears&action=edit "Edit this page [e]")</span>
-   <span id="ca-history">[View
    history](/web/20190715182507/http://wiki.vuze.com/mediawiki/index.php?title=Vuze_disappears&action=history "Past revisions of this page [h]")</span>

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

<a href="/web/20190715182507/http://wiki.vuze.com/w/Main_Page" class="mw-wiki-logo" title="Visit the main page"></a>

</div>

<div id="p-" class="portal" role="navigation"
aria-labelledby="p--label">

### 

<div class="body">

-   <span id="n-Download-Vuze-Now">[Download Vuze
    Now](https://web.archive.org/web/20190715182507/http://www.vuze.com/download)</span>

</div>

</div>

<div id="p-navigation" class="portal" role="navigation"
aria-labelledby="p-navigation-label">

### Navigation

<div class="body">

-   <span id="n-mainpage-description">[Main
    page](/web/20190715182507/http://wiki.vuze.com/w/Main_Page "Visit the main page [z]")</span>
-   <span id="n-recentchanges">[Recent
    changes](/web/20190715182507/http://wiki.vuze.com/w/Special:RecentChanges "A list of recent changes in the wiki [r]")</span>
-   <span id="n-randompage">[Random
    page](/web/20190715182507/http://wiki.vuze.com/w/Special:Random "Load a random page [x]")</span>
-   <span
    id="n-help">[Help](https://web.archive.org/web/20190715182507/https://www.mediawiki.org/wiki/Special:MyLanguage/Help:Contents "The place to find out")</span>

</div>

</div>

<div id="p-tb" class="portal" role="navigation"
aria-labelledby="p-tb-label">

### Tools

<div class="body">

-   <span id="t-whatlinkshere">[What links
    here](/web/20190715182507/http://wiki.vuze.com/w/Special:WhatLinksHere/Vuze_disappears "A list of all wiki pages that link here [j]")</span>
-   <span id="t-recentchangeslinked">[Related
    changes](/web/20190715182507/http://wiki.vuze.com/w/Special:RecentChangesLinked/Vuze_disappears "Recent changes in pages linked from this page [k]")</span>
-   <span id="t-specialpages">[Special
    pages](/web/20190715182507/http://wiki.vuze.com/w/Special:SpecialPages "A list of all special pages [q]")</span>
-   <span id="t-print">[Printable
    version](/web/20190715182507/http://wiki.vuze.com/mediawiki/index.php?title=Vuze_disappears&printable=yes "Printable version of this page [p]")</span>
-   <span id="t-permalink">[Permanent
    link](/web/20190715182507/http://wiki.vuze.com/mediawiki/index.php?title=Vuze_disappears&oldid=16701 "Permanent link to this revision of the page")</span>
-   <span id="t-info">[Page
    information](/web/20190715182507/http://wiki.vuze.com/mediawiki/index.php?title=Vuze_disappears&action=info "More information about this page")</span>

</div>

</div>

</div>

</div>

<div id="footer" role="contentinfo">

-   <span id="footer-info-lastmod">This page was last modified on 31
    August 2015, at 23:28.</span>
-   <span id="footer-info-viewcount">This page has been accessed 201,902
    times.</span>

<!-- -->

-   <span id="footer-places-about">[About
    VuzeWiki](/web/20190715182507/http://wiki.vuze.com/w/VuzeWiki:About "VuzeWiki:About")</span>
-   <span
    id="footer-places-mobileview"><a href="https://web.archive.org/web/20190715182507/http://wiki.vuze.com/mediawiki/index.php?title=Vuze_disappears&amp;mobileaction=toggle_view_mobile" class="noprint stopMobileRedirectToggle">Mobile view</a></span>

<!-- -->

-   <span
    id="footer-poweredbyico">[<img src="/web/20190715182507im_/http://wiki.vuze.com/mediawiki/resources/assets/poweredby_mediawiki_88x31.png" srcset="/web/20190715182507im_/http://wiki.vuze.com/mediawiki/resources/assets/poweredby_mediawiki_132x47.png 1.5x, /web/20190715182507im_/http://wiki.vuze.com/mediawiki/resources/assets/poweredby_mediawiki_176x62.png 2x" width="88" height="31" alt="Powered by MediaWiki" />](//web.archive.org/web/20190715182507/http://www.mediawiki.org/)</span>
-   <span id="footer-analyticsystemsico">Any use of Vuze® and Vuze+™
    that violates the rights of any person or entity is not allowed.
    [More](https://web.archive.org/web/20190715182507/http://vuze.com/corp/legal.php)</span>

<div style="clear:both">

</div>

</div>
