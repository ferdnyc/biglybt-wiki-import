<div id="mw-page-base" class="noprint">

</div>

<div id="mw-head-base" class="noprint">

</div>

<div id="content" class="mw-body" role="main">

<span id="top"></span>

<div class="mw-indicators">

</div>

# Failed Update

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

-   [<span class="tocnumber">1</span> <span class="toctext">Installation
    of at least one component
    failed</span>](#Installation_of_at_least_one_component_failed)
    -   [<span class="tocnumber">1.1</span> <span
        class="toctext">Windows Vista
        notes</span>](#Windows_Vista_notes)
    -   [<span class="tocnumber">1.2</span> <span class="toctext">Mac OS
        X notes</span>](#Mac_OS_X_notes)
    -   [<span class="tocnumber">1.3</span> <span
        class="toctext">Linux/Unix notes</span>](#Linux.2FUnix_notes)

</div>

# <span id="Installation_of_at_least_one_component_failed" class="mw-headline">Installation of at least one component failed</span><span class="mw-editsection"><span class="mw-editsection-bracket">\[</span>[edit](/web/20161228182741/http://wiki.vuze.com/mediawiki/index.php?title=Failed_Update&action=edit&section=1 "Edit section: Installation of at least one component failed")<span class="mw-editsection-bracket">\]</span></span>

In your config directory there will be an "update.log" file which
contains technical logs on the component update. The newest update is at
the bottom of the file, starting with the line "Update Starts:".

The typical reason for a failure is that you do not have rights to write
to folders required for the update.

If the log is of no help to you, you can always send a debug.zip to
support via Help->Generate Debug Info. The debug.zip will contain the
update.log. When e-mailing, please indicate that this was a update
failure so we know where to look :)

## <span id="Windows_Vista_notes" class="mw-headline">Windows Vista notes</span><span class="mw-editsection"><span class="mw-editsection-bracket">\[</span>[edit](/web/20161228182741/http://wiki.vuze.com/mediawiki/index.php?title=Failed_Update&action=edit&section=2 "Edit section: Windows Vista notes")<span class="mw-editsection-bracket">\]</span></span>

If you are having installation problems under Vista, most likely UAC is
active and preventing the installer from writing files to the
directories it requires access to. The simplest solution to this problem
is the following:

1.  Close Azureus completely. (If it is running minimized in the system
    tray, you will have to right click on it there and select "Exit".)
2.  Find a shortcut (icon) to run Azureus from (e.g. on the Desktop,
    Start Menu, Startup folder or Quick Launch bar)
3.  **Right click** on the Azureus shortcut icon and select "Run as
    Administrator". Select "Allow" from the UAC dialogue that pops up.
    This will allow Azureus to have access to write to any folder on
    your disk, in effect temporarily disabling UAC for Azureus.
4.  The installation should proceed normally. Afterwards, close Azureus
    and open it normally.

  
If this does not work for you, proceed with the following methods:

  
Check on your UAC (User Access Control), this could be preventing you to
install updates on your computer.

You can try logging in as the Administrator, give write access to
directories specified in the "update.log" file and follow the steps
below:

1.  Step: Open an Administrator Explorer window  
    1.  Click Start
    2.  Type: explorer
    3.  Right-click Windows Explorer
    4.  Click Run As Administrator  
          
2.  Step: Change security settings  
    1.  Find the folder you need access to from the Administrator
        Explorer window
    2.  Right-click it
    3.  Click Properties
    4.  Click the Security Tab
    5.  Click Edit
    6.  Click Add
    7.  If you are the only one that needs modify access to this file,
        type your user name and press enter. Otherwise, type "Users" and
        press enter.
    8.  Click the checkbox under Allow next to Full Control
    9.  Click OK
    10. Click OK  

*Note:* You will need to repeat Step 2 for every folder that you need
modify access to. This will open an "Administrator" explorer window.
Every action that you take from this window will be executed with full
Administrator permissions.  

If you are still experiencing issues, you can try turning off the UAC
just for the update. However, **Microsoft strongly recommends that you
do not disable User Account Control**. So to turn UAC off, follow these
simple steps:  

1.  1.  Click Start
    2.  Click Control Panel
    3.  Click User Accounts and Family Safety
    4.  Click User Accounts
    5.  Click Turn User Account Control On or Off
    6.  Uncheck the check box
    7.  Click OK

*Note:* You will need to restart your computer for the change to take
effect. This change affects all accounts on the computer, not just

yours.

## <span id="Mac_OS_X_notes" class="mw-headline">Mac OS X notes</span><span class="mw-editsection"><span class="mw-editsection-bracket">\[</span>[edit](/web/20161228182741/http://wiki.vuze.com/mediawiki/index.php?title=Failed_Update&action=edit&section=3 "Edit section: Mac OS X notes")<span class="mw-editsection-bracket">\]</span></span>

If you get an error indicating that, for example,
"/Volumes/Azureus/Azureus.app/Contents/Resources/Java" isn't writable
then you are running Azureus from the wrong location.

You need to stop Azureus, move Azureus.app into "/Applications" and then
restart it from that location.

You need to have administrators rights to write to the /Applications
location.

## <span id="Linux.2FUnix_notes" class="mw-headline">Linux/Unix notes</span><span class="mw-editsection"><span class="mw-editsection-bracket">\[</span>[edit](/web/20161228182741/http://wiki.vuze.com/mediawiki/index.php?title=Failed_Update&action=edit&section=4 "Edit section: Linux/Unix notes")<span class="mw-editsection-bracket">\]</span></span>

Note: If you installed a distro build of Azureus, there's a chance the
update process is broken. The best solution is to download Vuze from
<a href="https://web.archive.org/web/20161228182741/http://azureus.sf.net/" class="external free">http://azureus.sf.net</a>
. Otherwise,

If you installed Azureus 3.0.2.0 or higher, you can also try a manual
update.

1.  Make sure Azureus is not running
2.  Open up a shell
3.  Change to the azureus program dir
4.  Run "./updateAzureus" (If this is your first time using the script,
    you may have to "chmod +x ./updateAzureus"). If you don't have this
    script, you can create one:

<div style="text-align:right; margin-bottom:-37px;">

Copy to Clipboard

</div>

```
sudo java -cp ./plugins/azupdater/Updater.jar org.gudy.azureus2.update.Updater updateonly `pwd` ~/.azureus
```

Assuming you have a ./plugins/azupdater/Updater.jar, this will elevate
your rights and apply any updates that couldn't be done with your normal
user's rights.

</div>

<div class="printfooter">

Retrieved from
"[http://wiki.vuze.com/mediawiki/index.php?title=Failed_Update&oldid=10649](https://web.archive.org/web/20161228182741/http://wiki.vuze.com/mediawiki/index.php?title=Failed_Update&oldid=10649)"

</div>

<div id="catlinks" class="catlinks" mw="interface">

<div id="mw-normal-catlinks" class="mw-normal-catlinks">

[Category](/web/20161228182741/http://wiki.vuze.com/w/Special:Categories "Special:Categories"):

-   [Troubleshooting](/web/20161228182741/http://wiki.vuze.com/w/Category:Troubleshooting "Category:Troubleshooting")

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
    id="pt-anontalk">[Talk](/web/20161228182741/http://wiki.vuze.com/w/Special:MyTalk "Discussion about edits from this IP address [n]")</span>
-   <span
    id="pt-anoncontribs">[Contributions](/web/20161228182741/http://wiki.vuze.com/w/Special:MyContributions "A list of edits made from this IP address [y]")</span>
-   <span id="pt-createaccount">[Create
    account](/web/20161228182741/http://wiki.vuze.com/mediawiki/index.php?title=Special:CreateAccount&returnto=Failed+Update "You are encouraged to create an account and log in; however, it is not mandatory")</span>
-   <span id="pt-login">[Log
    in](/web/20161228182741/http://wiki.vuze.com/mediawiki/index.php?title=Special:UserLogin&returnto=Failed+Update "You are encouraged to log in; however, it is not mandatory [o]")</span>

</div>

<div id="left-navigation">

<div id="p-namespaces" class="vectorTabs" role="navigation"
aria-labelledby="p-namespaces-label">

### Namespaces

-   <span
    id="ca-nstab-main">[Page](/web/20161228182741/http://wiki.vuze.com/w/Failed_Update "View the content page [c]")</span>
-   <span
    id="ca-talk">[Discussion](/web/20161228182741/http://wiki.vuze.com/w/Talk:Failed_Update "Discussion about the content page [t]")</span>

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
    id="ca-view">[Read](/web/20161228182741/http://wiki.vuze.com/w/Failed_Update)</span>
-   <span
    id="ca-edit">[Edit](/web/20161228182741/http://wiki.vuze.com/mediawiki/index.php?title=Failed_Update&action=edit "Edit this page [e]")</span>
-   <span id="ca-history">[View
    history](/web/20161228182741/http://wiki.vuze.com/mediawiki/index.php?title=Failed_Update&action=history "Past revisions of this page [h]")</span>

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

<a href="/web/20161228182741/http://wiki.vuze.com/w/Main_Page" class="mw-wiki-logo" title="Visit the main page"></a>

</div>

<div id="p-" class="portal" role="navigation"
aria-labelledby="p--label">

### 

<div class="body">

-   <span id="n-Download-Vuze-Now">[Download Vuze
    Now](https://web.archive.org/web/20161228182741/http://www.vuze.com/download)</span>

</div>

</div>

<div id="p-navigation" class="portal" role="navigation"
aria-labelledby="p-navigation-label">

### Navigation

<div class="body">

-   <span id="n-mainpage-description">[Main
    page](/web/20161228182741/http://wiki.vuze.com/w/Main_Page "Visit the main page [z]")</span>
-   <span id="n-recentchanges">[Recent
    changes](/web/20161228182741/http://wiki.vuze.com/w/Special:RecentChanges "A list of recent changes in the wiki [r]")</span>
-   <span id="n-randompage">[Random
    page](/web/20161228182741/http://wiki.vuze.com/w/Special:Random "Load a random page [x]")</span>
-   <span
    id="n-help">[Help](https://web.archive.org/web/20161228182741/https://www.mediawiki.org/wiki/Special:MyLanguage/Help:Contents "The place to find out")</span>

</div>

</div>

<div id="p-tb" class="portal" role="navigation"
aria-labelledby="p-tb-label">

### Tools

<div class="body">

-   <span id="t-whatlinkshere">[What links
    here](/web/20161228182741/http://wiki.vuze.com/w/Special:WhatLinksHere/Failed_Update "A list of all wiki pages that link here [j]")</span>
-   <span id="t-recentchangeslinked">[Related
    changes](/web/20161228182741/http://wiki.vuze.com/w/Special:RecentChangesLinked/Failed_Update "Recent changes in pages linked from this page [k]")</span>
-   <span id="t-specialpages">[Special
    pages](/web/20161228182741/http://wiki.vuze.com/w/Special:SpecialPages "A list of all special pages [q]")</span>
-   <span id="t-print">[Printable
    version](/web/20161228182741/http://wiki.vuze.com/mediawiki/index.php?title=Failed_Update&printable=yes "Printable version of this page [p]")</span>
-   <span id="t-permalink">[Permanent
    link](/web/20161228182741/http://wiki.vuze.com/mediawiki/index.php?title=Failed_Update&oldid=10649 "Permanent link to this revision of the page")</span>
-   <span id="t-info">[Page
    information](/web/20161228182741/http://wiki.vuze.com/mediawiki/index.php?title=Failed_Update&action=info "More information about this page")</span>

</div>

</div>

</div>

</div>

<div id="footer" role="contentinfo">

-   <span id="footer-info-lastmod">This page was last modified on 23 May
    2011, at 06:13.</span>
-   <span id="footer-info-viewcount">This page has been accessed 22,096
    times.</span>

<!-- -->

-   <span id="footer-places-about">[About
    VuzeWiki](/web/20161228182741/http://wiki.vuze.com/w/VuzeWiki:About "VuzeWiki:About")</span>
-   <span
    id="footer-places-mobileview"><a href="https://web.archive.org/web/20161228182741/http://wiki.vuze.com/mediawiki/index.php?title=Failed_Update&amp;mobileaction=toggle_view_mobile" class="noprint stopMobileRedirectToggle">Mobile view</a></span>

<!-- -->

-   <span
    id="footer-poweredbyico">[<img src="/web/20161228182741im_/http://wiki.vuze.com/mediawiki/resources/assets/poweredby_mediawiki_88x31.png" srcset="/web/20161228182741im_/http://wiki.vuze.com/mediawiki/resources/assets/poweredby_mediawiki_132x47.png 1.5x, /web/20161228182741im_/http://wiki.vuze.com/mediawiki/resources/assets/poweredby_mediawiki_176x62.png 2x" width="88" height="31" alt="Powered by MediaWiki" />](//web.archive.org/web/20161228182741/http://www.mediawiki.org/)</span>
-   <span id="footer-analyticsystemsico">Any use of Vuze® and Vuze+™
    that violates the rights of any person or entity is not allowed.
    [More](https://web.archive.org/web/20161228182741/http://vuze.com/corp/legal.php)</span>

<div style="clear:both">

</div>

</div>
