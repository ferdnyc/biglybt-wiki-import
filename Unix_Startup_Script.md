<div id="globalWrapper">

<div id="column-content">

<div id="content" class="mw-body-primary" role="main">

<span id="top"></span>

# <span dir="auto">Unix Startup Script</span>

<div id="bodyContent" class="mw-body">

<div id="siteSub">

From VuzeWiki

</div>

<div id="contentSub">

</div>

<div id="jump-to-nav" class="mw-jump">

Jump to: [navigation](#column-one), [search](#searchInput)

</div>

<div id="mw-content-text" class="mw-content-ltr" lang="en" dir="ltr">

  

<table id="toc" class="toc">
<colgroup>
<col style="width: 100%" />
</colgroup>
<tbody>
<tr class="odd">
<td><div id="toctitle">
<h2 id="contents">Contents</h2>
</div>
<ul>
<li><a href="#Linux.2FUnix_Startup_Script"><span class="tocnumber">1</span> <span class="toctext">Linux/Unix Startup Script</span></a>
<ul>
<li><a href="#Introduction"><span class="tocnumber">1.1</span> <span class="toctext">Introduction</span></a></li>
<li><a href="#Manually_updating_your_start_script"><span class="tocnumber">1.2</span> <span class="toctext">Manually updating your start script</span></a></li>
<li><a href="#Note_to_distros"><span class="tocnumber">1.3</span> <span class="toctext">Note to distros</span></a></li>
<li><a href="#The_latest_script"><span class="tocnumber">1.4</span> <span class="toctext">The latest script</span></a></li>
<li><a href="#Changes"><span class="tocnumber">1.5</span> <span class="toctext">Changes</span></a>
<ul>
<li><a href="#VERSION_1"><span class="tocnumber">1.5.1</span> <span class="toctext">VERSION 1</span></a></li>
<li><a href="#VERSION_2"><span class="tocnumber">1.5.2</span> <span class="toctext">VERSION 2</span></a></li>
</ul></li>
</ul></li>
</ul></td>
</tr>
</tbody>
</table>

# <span class="editsection">\[[edit](/web/20131114095333/http://wiki.vuze.com/mediawiki/index.php?title=Unix_Startup_Script&action=edit&section=1 "Edit section: Linux/Unix Startup Script")\]</span> <span id="Linux.2FUnix_Startup_Script" class="mw-headline">Linux/Unix Startup Script</span>

## <span class="editsection">\[[edit](/web/20131114095333/http://wiki.vuze.com/mediawiki/index.php?title=Unix_Startup_Script&action=edit&section=2 "Edit section: Introduction")\]</span> <span id="Introduction" class="mw-headline"> Introduction </span>

From time to time, azureus startup script will need to be changed to
handle new features or to fix existing bugs. Since we can't just
overwrite your old ./azureus script (especially if you modified it or
installed Azureus via a distro), this page is meant to walk you through
what you need to do.

## <span class="editsection">\[[edit](/web/20131114095333/http://wiki.vuze.com/mediawiki/index.php?title=Unix_Startup_Script&action=edit&section=3 "Edit section: Manually updating your start script")\]</span> <span id="Manually_updating_your_start_script" class="mw-headline"> Manually updating your start script </span>

If you downloaded and installed Azureus from SourceForge, Vuze, or
Zudeo, AND you have made no modifications to the startup script, you can
safely replace the new one with the old one. When there is a new startup
script available, you will be informed via a message box. Simply copy
the new one over the old one and re-run azureus.

If you manually edited your azureus script only to set the
JAVA_PROGRAM_DIR or PROGRAM_DIR variables, or to set java runtime
settings, copy or make note of those lines from your edited script.
Then, copy in the new script, edit it and paste those lines back in.

If you've done major changes to the script, the first thing you need to
do is find your existing startup script version. Search the script for
"SCRIPT_VERSION=". If there are no matches, you have version 0. Read the
sections describing the changes between your version and the latest
version to get and idea of what you need to change (and why).

## <span class="editsection">\[[edit](/web/20131114095333/http://wiki.vuze.com/mediawiki/index.php?title=Unix_Startup_Script&action=edit&section=4 "Edit section: Note to distros")\]</span> <span id="Note_to_distros" class="mw-headline"> Note to distros </span>

Please keep your script up to date. While you may not need all the
directory scanning and version verification script code, you may need to
know if you have to set new variables or pass in new parameters. (For
example, Version 1 adds and entry LD_LIBRARY_PATH so that Azureus can
display a browser window)

## <span class="editsection">\[[edit](/web/20131114095333/http://wiki.vuze.com/mediawiki/index.php?title=Unix_Startup_Script&action=edit&section=5 "Edit section: The latest script")\]</span> <span id="The_latest_script" class="mw-headline"> The latest script </span>

<a href="https://web.archive.org/web/20131114095333/http://azureus.cvs.sourceforge.net/*checkout*/azureus/azureus2/org/gudy/azureus2/platform/unix/startupScript" class="external free">http://azureus.cvs.sourceforge.net/*checkout*/azureus/azureus2/org/gudy/azureus2/platform/unix/startupScript</a>

  

## <span class="editsection">\[[edit](/web/20131114095333/http://wiki.vuze.com/mediawiki/index.php?title=Unix_Startup_Script&action=edit&section=6 "Edit section: Changes")\]</span> <span id="Changes" class="mw-headline">Changes</span>

### <span class="editsection">\[[edit](/web/20131114095333/http://wiki.vuze.com/mediawiki/index.php?title=Unix_Startup_Script&action=edit&section=7 "Edit section: VERSION 1")\]</span> <span id="VERSION_1" class="mw-headline">VERSION 1</span>

The primary reason for this change is to allow azureus to insert shell
script commands before and after azureus runs. The initial use of this
is to find where your Gecko Engine/XULRunner is and add it to your
LD_LIBRARY_PATH. The secondary use of this is to allow Azureus to
restart/update via a script action, instead of the older, clunkier way
of trying to run Java over again.

1\) Set SCRIPT_VERSION string

    SCRIPT_VERSION=1

2\) You need to add the following function to your script:

    runJavaOutput()
    {
        ${JAVA_PROGRAM_DIR}java "${JAVA_ARGS}" -cp "${CLASSPATH}" -Djava.library.path="${PROGRAM_DIR}" -Dazureus.install.path="${PROGRAM_DIR}" -Dazureus.script.version="${SCRIPT_VERSION}" -Dazureus.script="$0" ${1} > ~/azScript
        if [ -f ~/azScript ]; then
            chmod +x ~/azScript
            . ~/azScript
            rm ~/azScript
        fi
    }

3\) Just before running azureus (launching java), add the following
line. Note that this should be AFTER you set LD_LIBRARY_PATH (if you do
that)

    runJavaOutput "org.gudy.azureus2.platform.unix.ScriptBeforeStartup";

4\) Add two java system properties when launching azureus:

    -Dazureus.script.version="${SCRIPT_VERSION}" -Dazureus.script="$0"

5\) Just after running azureus, add this line:

    runJavaOutput "org.gudy.azureus2.platform.unix.ScriptAfterShutdown";

### <span class="editsection">\[[edit](/web/20131114095333/http://wiki.vuze.com/mediawiki/index.php?title=Unix_Startup_Script&action=edit&section=8 "Edit section: VERSION 2")\]</span> <span id="VERSION_2" class="mw-headline">VERSION 2</span>

Version 2 passes all the command line arguments to the "runJavaOutput()"
function. This is needed because ScriptBeforeStartup will check to see
if Azureus is running, and if it is, pass the parameters to it.

1\) Set SCRIPT_VERSION string

>     SCRIPT_VERSION=2

2\) Update the runJavaOutput function you created in version 1 to:

>     runJavaOutput()
>     {
>         # assume we can write to the user's home..
>
>         ${JAVA_PROGRAM_DIR}java "${JAVA_ARGS}" \
>             -cp "${CLASSPATH}" \
>             -Djava.library.path="${PROGRAM_DIR}" \
>             -Dazureus.install.path="${PROGRAM_DIR}" \
>             -Dazureus.script="$0" \
>             $JAVA_PROPS \
>             "$@" > ~/azScript
>         if [ -f ~/azScript ]; then
>             chmod +x ~/azScript
>             . ~/azScript
>             rm ~/azScript
>         fi
>     }
>
> (The difference is that ${1} was turned into "$@")

3\) Update the two runJavaOutput calls to:

>     runJavaOutput "org.gudy.azureus2.platform.unix.ScriptBeforeStartup" "$@";
>
> and
>
>     runJavaOutput "org.gudy.azureus2.platform.unix.ScriptAfterShutdown" "$@";
>
> ("$@" was appended to the call)

</div>

<div class="printfooter">

Retrieved from
"[http://wiki.vuze.com/mediawiki/index.php?title=Unix_Startup_Script&oldid=9852](https://web.archive.org/web/20131114095333/http://wiki.vuze.com/mediawiki/index.php?title=Unix_Startup_Script&oldid=9852)"

</div>

<div id="catlinks" class="catlinks">

<div id="mw-normal-catlinks" class="mw-normal-catlinks">

[Category](/web/20131114095333/http://wiki.vuze.com/w/Special:Categories "Special:Categories"):

-   [Technical
    Information](/web/20131114095333/http://wiki.vuze.com/w/Category:Technical_Information "Category:Technical Information")

</div>

</div>

<div class="visualClear">

</div>

</div>

</div>

</div>

<div id="column-one">

## Navigation menu

<div id="p-cactions" class="portlet" role="navigation">

### Views

<div class="pBody">

-   <span
    id="ca-nstab-main">[Page](/web/20131114095333/http://wiki.vuze.com/w/Unix_Startup_Script "View the content page [c]")</span>
-   <span
    id="ca-talk">[Discussion](/web/20131114095333/http://wiki.vuze.com/mediawiki/index.php?title=Talk:Unix_Startup_Script&action=edit&redlink=1 "Discussion about the content page [t]")</span>
-   <span
    id="ca-edit">[Edit](/web/20131114095333/http://wiki.vuze.com/mediawiki/index.php?title=Unix_Startup_Script&action=edit "You can edit this page. Please use the preview button before saving [e]")</span>
-   <span
    id="ca-history">[History](/web/20131114095333/http://wiki.vuze.com/mediawiki/index.php?title=Unix_Startup_Script&action=history "Past revisions of this page [h]")</span>

</div>

</div>

<div id="p-personal" class="portlet" role="navigation">

### Personal tools

<div class="pBody">

-   <span id="pt-createaccount">[Create
    account](/web/20131114095333/http://wiki.vuze.com/mediawiki/index.php?title=Special:UserLogin&returnto=Unix+Startup+Script&type=signup)</span>
-   <span id="pt-login">[Log
    in](/web/20131114095333/http://wiki.vuze.com/mediawiki/index.php?title=Special:UserLogin&returnto=Unix+Startup+Script "You are encouraged to log in; however, it is not mandatory [o]")</span>

</div>

</div>

<div id="p-logo" class="portlet" role="banner">

[](/web/20131114095333/http://wiki.vuze.com/w/Main_Page "Visit the main page")

</div>

<div id="p-" class="generated-sidebar portlet" role="navigation">

### 

<div class="pBody">

-   <span id="n-Download-Vuze-Now">[Download Vuze
    Now](https://web.archive.org/web/20131114095333/http://www.vuze.com/download)</span>

</div>

</div>

<div id="p-navigation" class="generated-sidebar portlet"
role="navigation">

### Navigation

<div class="pBody">

-   <span id="n-mainpage-description">[Main
    page](/web/20131114095333/http://wiki.vuze.com/w/Main_Page "Visit the main page [z]")</span>
-   <span id="n-portal">[Community
    portal](/web/20131114095333/http://wiki.vuze.com/w/VuzeWiki:Community_portal "About the project, what you can do, where to find things")</span>
-   <span id="n-currentevents">[Current
    events](/web/20131114095333/http://wiki.vuze.com/w/VuzeWiki:Current_events "Find background information on current events")</span>
-   <span id="n-recentchanges">[Recent
    changes](/web/20131114095333/http://wiki.vuze.com/w/Special:RecentChanges "A list of recent changes in the wiki [r]")</span>
-   <span id="n-randompage">[Random
    page](/web/20131114095333/http://wiki.vuze.com/w/Special:Random "Load a random page [x]")</span>
-   <span
    id="n-help">[Help](/web/20131114095333/http://wiki.vuze.com/w/Help:Contents "The place to find out")</span>

</div>

</div>

<div id="p-search" class="portlet" role="search">

### Search

<div id="searchBody" class="pBody">

 

</div>

</div>

<div id="p-tb" class="portlet" role="navigation">

### Toolbox

<div class="pBody">

-   <span id="t-whatlinkshere">[What links
    here](/web/20131114095333/http://wiki.vuze.com/w/Special:WhatLinksHere/Unix_Startup_Script "A list of all wiki pages that link here [j]")</span>
-   <span id="t-recentchangeslinked">[Related
    changes](/web/20131114095333/http://wiki.vuze.com/w/Special:RecentChangesLinked/Unix_Startup_Script "Recent changes in pages linked from this page [k]")</span>
-   <span id="t-specialpages">[Special
    pages](/web/20131114095333/http://wiki.vuze.com/w/Special:SpecialPages "A list of all special pages [q]")</span>
-   <span id="t-print">[Printable
    version](/web/20131114095333/http://wiki.vuze.com/mediawiki/index.php?title=Unix_Startup_Script&printable=yes "Printable version of this page [p]")</span>
-   <span id="t-permalink">[Permanent
    link](/web/20131114095333/http://wiki.vuze.com/mediawiki/index.php?title=Unix_Startup_Script&oldid=9852 "Permanent link to this revision of the page")</span>
-   <span id="t-info">[Page
    information](/web/20131114095333/http://wiki.vuze.com/mediawiki/index.php?title=Unix_Startup_Script&action=info)</span>

</div>

</div>

</div>

<div class="visualClear">

</div>

<div id="footer" role="contentinfo">

<div id="f-poweredbyico">

[<img src="/web/20131114095333im_/http://wiki.vuze.com/mediawiki/skins/common/images/poweredby_mediawiki_88x31.png" width="88" height="31" alt="Powered by MediaWiki" />](//web.archive.org/web/20131114095333/http://www.mediawiki.org/)

</div>

-   <span id="lastmod">This page was last modified on 17 November 2010,
    at 23:42.</span>
-   <span id="viewcount">This page has been accessed 5,025 times.</span>
-   <span id="about">[About
    VuzeWiki](/web/20131114095333/http://wiki.vuze.com/w/VuzeWiki:About "VuzeWiki:About")</span>

</div>

</div>
