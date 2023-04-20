<div id="globalWrapper">

<div id="column-content">

<div id="content">

<span id="top"></span>

# Version.azureusplatform.com

<div id="bodyContent">

### From VuzeWiki

<div id="contentSub">

</div>

<div id="jump-to-nav">

Jump to: [navigation](#column-one), [search](#searchInput)

</div>

There are two reasons why Azureus contacts version.azureusplatform.com
(was version.aelitis.com):

1\. To check for updates

You can disable this call via Options->Interface->Start. Unselect "Check
for latest version when Azureus starts" and "Check for latest version
periodically"

2\. To get your external IP address

As of 2.5.0.4, there is still no way of disabling this.

An anonymous version number, random id, and some anonymous stats are
sent to version.aelitis.com on each request. You can disable this option
by turning off the "Allow Azureus to send anonymous version number and
random id while checking for new version" in Options->Interface.

  
As of 2.5.0.4, the following anonymous data is being sent:

-   OS name, version, architecture (for update check)
-   time since last version check
-   Java version, vendor, memory setting
-   plugin list (for plugin update check)
-   SWT version, platform (for SWT update check)
-   main window size (to help us make sure the UI fits within the vast
    majority of window sizes)
-   using PHE only (encryption mode)
-   which interface you are using (Vuze / Vuze Advanced / Azureus 2
    ("Classic") UI)
-   Your
    <a href="https://web.archive.org/web/20120428023257/http://en.wikipedia.org/wiki/Autonomous_System_Number" class="extiw" title="wikipedia:Autonomous System Number">AS and ASN</a>.
    This allows the version check server to return information about
    whether you would benefit from turning on PHE

  
As of 3.0.2.0, the following additional data is being sent:

-   Java runtime version (more detail about what specific JVM is in use)
-   Language setting (to help us determine which languages need
    supporting)

  
As of 3.0.3.6, certain new experimental features may be disabled
remotely if a lot of problems have been reported with it after release:

-   New request limiting behaviour
-   UDP-based reconnection
-   General quick reconnect mechanism
-   Auto-speed mechanism used

  
As of 3.0.4.2, some plugins can now report data back to the server -
currently, this is limited to the following plugins:

-   [ISP Network
    Monitor](/web/20120428023257/http://wiki.vuze.com/w/ISP_Network_Monitor "ISP Network Monitor")

  
As of 4.2.0.6, information previously not sent when the 'don't send
version number and random id' was selected has been changed to always be
sent. This information is purely to allow the version server to
recommend the correct updates to the client - SWT versions depend on os
specific details for example. The following fields are affected:

-   ui - whether Vuze UI or Classic UI - needed to target UI specific
    updates (e.g. to avoid unnecessary updates of users with Classic UI
    when changes that only affect the Vuze UI are made)
-   os, os_version, os_arch: Required to correctly update SWT
-   swt_version: Required to correctly update SWT

<div class="printfooter">

Retrieved from
"[http://wiki.vuze.com/w/Version.azureusplatform.com](https://web.archive.org/web/20120428023257/http://wiki.vuze.com/w/Version.azureusplatform.com)"

</div>

<div id="catlinks" class="catlinks">

<div id="mw-normal-catlinks">

[Category](/web/20120428023257/http://wiki.vuze.com/w/Special:Categories "Special:Categories"):
<span dir="ltr">[Technical
Information](/web/20120428023257/http://wiki.vuze.com/w/Category:Technical_Information "Category:Technical Information")</span>

</div>

</div>

<div class="visualClear">

</div>

</div>

</div>

</div>

<div id="column-one">

<div id="p-cactions" class="portlet">

##### Views

<div class="pBody">

-   <span
    id="ca-nstab-main">[Page](/web/20120428023257/http://wiki.vuze.com/w/Version.azureusplatform.com "View the content page [c]")</span>
-   <span
    id="ca-talk">[Discussion](/web/20120428023257/http://wiki.vuze.com/mediawiki/index.php?title=Talk:Version.azureusplatform.com&action=edit&redlink=1 "Discussion about the content page [t]")</span>
-   <span
    id="ca-edit">[Edit](/web/20120428023257/http://wiki.vuze.com/mediawiki/index.php?title=Version.azureusplatform.com&action=edit "You can edit this page.
    Please use the preview button before saving [e]")</span>
-   <span
    id="ca-history">[History](/web/20120428023257/http://wiki.vuze.com/mediawiki/index.php?title=Version.azureusplatform.com&action=history "Past revisions of this page [h]")</span>

</div>

</div>

<div id="p-personal" class="portlet">

##### Personal tools

<div class="pBody">

-   <span id="pt-login">[Log in / create
    account](/web/20120428023257/http://wiki.vuze.com/mediawiki/index.php?title=Special:UserLogin&returnto=Version.azureusplatform.com "You are encouraged to log in; however, it is not mandatory [o]")</span>

</div>

</div>

<div id="p-logo" class="portlet">

[](/web/20120428023257/http://wiki.vuze.com/w/Main_Page "Visit the main page [z]")

</div>

<div id="p-navigation" class="generated-sidebar portlet">

##### Navigation

<div class="pBody">

-   <span id="n-mainpage-description">[Main
    Page](/web/20120428023257/http://wiki.vuze.com/w/Main_Page)</span>
-   <span id="n-portal">[Community
    portal](/web/20120428023257/http://wiki.vuze.com/w/VuzeWiki:Community_Portal "About the project, what you can do, where to find things")</span>
-   <span id="n-currentevents">[Current
    events](/web/20120428023257/http://wiki.vuze.com/w/VuzeWiki:Current_events "Find background information on current events")</span>
-   <span id="n-recentchanges">[Recent
    changes](/web/20120428023257/http://wiki.vuze.com/w/Special:RecentChanges "The list of recent changes in the wiki [r]")</span>
-   <span id="n-randompage">[Random
    page](/web/20120428023257/http://wiki.vuze.com/w/Special:Random "Load a random page [x]")</span>
-   <span
    id="n-help">[Help](/web/20120428023257/http://wiki.vuze.com/w/Help:Contents "The place to find out")</span>

</div>

</div>

<div id="p-search" class="portlet">

##### Search

<div id="searchBody" class="pBody">

<div>

 

</div>

</div>

</div>

<div id="p-tb" class="portlet">

##### Toolbox

<div class="pBody">

-   <span id="t-whatlinkshere">[What links
    here](/web/20120428023257/http://wiki.vuze.com/w/Special:WhatLinksHere/Version.azureusplatform.com "List of all wiki pages that link here [j]")</span>
-   <span id="t-recentchangeslinked">[Related
    changes](/web/20120428023257/http://wiki.vuze.com/w/Special:RecentChangesLinked/Version.azureusplatform.com "Recent changes in pages linked from this page [k]")</span>
-   <span id="t-specialpages">[Special
    pages](/web/20120428023257/http://wiki.vuze.com/w/Special:SpecialPages "List of all special pages [q]")</span>
-   <span id="t-print">[Printable
    version](/web/20120428023257/http://wiki.vuze.com/mediawiki/index.php?title=Version.azureusplatform.com&printable=yes "Printable version of this page [p]")</span>
-   <span id="t-permalink">[Permanent
    link](/web/20120428023257/http://wiki.vuze.com/mediawiki/index.php?title=Version.azureusplatform.com&oldid=7443 "Permanent link to this revision of the page")</span>

</div>

</div>

</div>

<div class="visualClear">

</div>

<div id="footer">

<div id="f-poweredbyico">

[![Powered by
MediaWiki](/web/20120428023257im_/http://wiki.vuze.com/mediawiki/skins/common/images/poweredby_mediawiki_88x31.png)](https://web.archive.org/web/20120428023257/http://www.mediawiki.org/)

</div>

-   <span id="lastmod">This page was last modified on 6 August 2009, at
    20:00.</span>
-   <span id="viewcount">This page has been accessed 24,700
    times.</span>
-   <span id="privacy">[Privacy
    policy](/web/20120428023257/http://wiki.vuze.com/w/VuzeWiki:Privacy_policy "VuzeWiki:Privacy policy")</span>
-   <span id="about">[About
    VuzeWiki](/web/20120428023257/http://wiki.vuze.com/w/VuzeWiki:About "VuzeWiki:About")</span>
-   <span
    id="disclaimer">[Disclaimers](/web/20120428023257/http://wiki.vuze.com/w/VuzeWiki:General_disclaimer "VuzeWiki:General disclaimer")</span>

</div>

</div>
