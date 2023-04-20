<div id="mw-page-base" class="noprint">

</div>

<div id="mw-head-base" class="noprint">

</div>

<div id="content" class="mw-body" role="main">

<span id="top"></span>

<div class="mw-indicators">

</div>

# Commandline options

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

-   [<span class="tocnumber">1</span> <span class="toctext">Azureus
    Command Line Options</span>](#Azureus_Command_Line_Options)
    -   [<span class="tocnumber">1.1</span> <span
        class="toctext">Options directly passed to
        Azureus</span>](#Options_directly_passed_to_Azureus)
    -   [<span class="tocnumber">1.2</span> <span
        class="toctext">Options passed to the Virtual
        Machine</span>](#Options_passed_to_the_Virtual_Machine)
        -   [<span class="tocnumber">1.2.1</span> <span
            class="toctext">VM Options file (windows
            only)</span>](#VM_Options_file_.28windows_only.29)
        -   [<span class="tocnumber">1.2.2</span> <span
            class="toctext">Startup Options</span>](#Startup_Options)
        -   [<span class="tocnumber">1.2.3</span> <span
            class="toctext">Network Options</span>](#Network_Options)
        -   [<span class="tocnumber">1.2.4</span> <span
            class="toctext">Path Options</span>](#Path_Options)
        -   [<span class="tocnumber">1.2.5</span> <span
            class="toctext">GUI Options</span>](#GUI_Options)
        -   [<span class="tocnumber">1.2.6</span> <span
            class="toctext">Log Options</span>](#Log_Options)
        -   [<span class="tocnumber">1.2.7</span> <span
            class="toctext">Memory Limits</span>](#Memory_Limits)
        -   [<span class="tocnumber">1.2.8</span> <span
            class="toctext">"Safe Mode"
            Options</span>](#.22Safe_Mode.22_Options)
        -   [<span class="tocnumber">1.2.9</span> <span
            class="toctext">Console UI
            Options</span>](#Console_UI_Options)
-   [<span class="tocnumber">2</span> <span class="toctext">Manually
    starting directly with
    Java</span>](#Manually_starting_directly_with_Java)
    -   [<span class="tocnumber">2.1</span> <span
        class="toctext">Windows</span>](#Windows)
-   [<span class="tocnumber">3</span> <span class="toctext">Changing the
    Control Port</span>](#Changing_the_Control_Port)

</div>

## <span id="Azureus_Command_Line_Options" class="mw-headline">Azureus Command Line Options</span><span class="mw-editsection"><span class="mw-editsection-bracket">\[</span>[edit](/web/20210712091909/http://wiki.vuze.com/mediawiki/index.php?title=Commandline_options&action=edit&section=1 "Edit section: Azureus Command Line Options")<span class="mw-editsection-bracket">\]</span></span>

The general syntax is:

*Windows*: Azureus.exe \[-J\<VM argument>\] \[-J\<VM argument>\]
\[azureus argument\] \[azureus argument\]  
*\*nix*: ./azureus \[azureus argument\] \[azureus argument\]

To provide VM arguments under \*nix see [#Options passed to the Virtual
Machine](#Options_passed_to_the_Virtual_Machine)

### <span id="Options_directly_passed_to_Azureus" class="mw-headline">Options directly passed to Azureus</span><span class="mw-editsection"><span class="mw-editsection-bracket">\[</span>[edit](/web/20210712091909/http://wiki.vuze.com/mediawiki/index.php?title=Commandline_options&action=edit&section=2 "Edit section: Options directly passed to Azureus")<span class="mw-editsection-bracket">\]</span></span>

The most important command line option is the option to provide a
torrent location which could be a [Magnet
link](/web/20210712091909/http://wiki.vuze.com/w/Magnet "Magnet"), an
URL that points to a .torrent file or a path/filename. Those parameters
can be attached to the launcher scripts/applications (depending on your
OS)

*Example (Windows):* Azureus.exe "http://example.com/test.torrent"  
*Example (\*nix):* ./azureus "/path/to/the.torrent"  
*Example (\*nix):* ./azureus
"<a href="https://web.archive.org/web/20210712091909/magnet:/?xt=urn:btih:IJBDPDSBT4QZLBIJ6NX7LITSZHZQ7F5I" class="external free">magnet:?xt=urn:btih:IJBDPDSBT4QZLBIJ6NX7LITSZHZQ7F5I</a>"

  
You can also shutdown a running Azureus instance via the command line
parameter **--closedown** or restart via **--restart**:  
*Example (Windows):* Azureus.exe --closedown

On Unix, if you're using Java 1.5, you can send a SIGHUP to your Azureus
instance to shut it down. It will only work on some java
implementations. If you're running Azureus as a non-root user (as you
should), and you are not running any other Java applications, you can
use this command to shut down Azureus: *killall -SIGHUP java*

### <span id="Options_passed_to_the_Virtual_Machine" class="mw-headline">Options passed to the Virtual Machine</span><span class="mw-editsection"><span class="mw-editsection-bracket">\[</span>[edit](/web/20210712091909/http://wiki.vuze.com/mediawiki/index.php?title=Commandline_options&action=edit&section=3 "Edit section: Options passed to the Virtual Machine")<span class="mw-editsection-bracket">\]</span></span>

Besides the direct arguments above, Azureus provides additional
configuration options via the standard -D\<xxx> java mechanism.

Since azureus 2306 windows users can pass these arguments to Azureus.exe
like regular arguments by prefixing them with *-J*  
*Example (Windows, for Azureus 2306 and later):* Azureus.exe
**-J**-Dazureus.skipSWTcheck=1

  
Users of earlier versions or on linux/unix must invoke Azureus manually
or modify the startup script, see
<a href="https://web.archive.org/web/20210712091909/http://azureus.sourceforge.net/howto_win.php" class="external text">windows how-to</a>
and
<a href="https://web.archive.org/web/20210712091909/http://azureus.sourceforge.net/howto_linux.php" class="external text">linux how-to</a>

*Example (windows):* java -cp swt.jar;Azureus2.jar
-Dazureus.skipSWTcheck=1 org.gudy.azureus2.ui.swt.Main  
*Example (\*nix):* java -cp swt.jar:Azureus2.jar -Djava.library.path=./
-Dazureus.skipSWTcheck=1 org.gudy.azureus2.ui.swt.Main  
*Example (macintosh):* Open /Applications/Vuse.app/Contents/Info.plist
and change the Java/VMOptions Value (I.e.: -Xmx256m)

#### <span id="VM_Options_file_.28windows_only.29" class="mw-headline">VM Options file (windows only)</span><span class="mw-editsection"><span class="mw-editsection-bracket">\[</span>[edit](/web/20210712091909/http://wiki.vuze.com/mediawiki/index.php?title=Commandline_options&action=edit&section=4 "Edit section: VM Options file (windows only)")<span class="mw-editsection-bracket">\]</span></span>

-J options specified on the command line won't be preserved over an
Azureus restart. To ensure the options are retained place them into a
file called *Azureus.exe.vmoptions* in the same directory as the
Azureus.exe (usually C:\\Program Files\\Vuze or C:\\Program Files
(x86)\\Vuze).

In this case simply place each command on a separate line in the file,
without the -J. For example

Azureus.exe.vmoptions

<div style="text-align:right; margin-bottom:-37px;">

Copy to Clipboard

</div>

```
   -Dazureus.instance.port=45811
   -Xmx512m
```

will start Vuze listening on port 45811 (instead of the default 6880)
and with a maximum Java memory size of 512MB

#### <span id="Startup_Options" class="mw-headline">Startup Options</span><span class="mw-editsection"><span class="mw-editsection-bracket">\[</span>[edit](/web/20210712091909/http://wiki.vuze.com/mediawiki/index.php?title=Commandline_options&action=edit&section=5 "Edit section: Startup Options")<span class="mw-editsection-bracket">\]</span></span>

-   **-Dazureus.instance.port=\<port number>** This sets the port
    (default is 6880) that Vuze uses to communicate with other instances
    of itself (e.g. when adding a torrent by clicking on a url/magnet in
    a web browser)
-   -Dazureus.instance.lock.disable=1

#### <span id="Network_Options" class="mw-headline">Network Options</span><span class="mw-editsection"><span class="mw-editsection-bracket">\[</span>[edit](/web/20210712091909/http://wiki.vuze.com/mediawiki/index.php?title=Commandline_options&action=edit&section=6 "Edit section: Network Options")<span class="mw-editsection-bracket">\]</span></span>

-   **-Dazureus.lazy.bitfield=1** Always send a faked incomplete
    bitfield, and instead send remaining completed piece info via Have
    messages. Certain ISP (ie Cablevision's Optimum Online) networks
    seem to block peer seeding via "complete" bitfield message
    filtering. You should only use this option if you need to.

#### <span id="Path_Options" class="mw-headline">Path Options</span><span class="mw-editsection"><span class="mw-editsection-bracket">\[</span>[edit](/web/20210712091909/http://wiki.vuze.com/mediawiki/index.php?title=Commandline_options&action=edit&section=7 "Edit section: Path Options")<span class="mw-editsection-bracket">\]</span></span>

-   **-Dazureus.config.path=** Sets the [Configuration
    directory](/web/20210712091909/http://wiki.vuze.com/w/Configuration_directory "Configuration directory")
    Azureus uses for config files and plugins. Default config path is
    OS-dependant: Under unix, this usually is *\~/.azureus/*; under
    Windows, this usually is *%appdata%\\Azureus\\*; Under Mac OS X,
    this usually is *"/Users/\<username>/Library/Application
    Support/Azureus/"*.
    -   combine with **-DMULTI_INSTANCE=true** to open multiple
        instances of Azureus.

    *Note:* opening multiple instances of Azureus is generally a very
    bad idea, except in very special circumstances.  
    The multi-instance flag can be used to disable the instance-checking
    if some other application is [listening on port
    6880](/web/20210712091909/http://wiki.vuze.com/w/Select_port_for_Vuze#Which_ports_Vuze_uses_by_default.3F "Select port for Vuze")
    and prevents Azureus from starting.
-   **-Dazureus.install.path=** sets the install path for Azureus, this
    is useful if you want to override where Azureus places its shared
    plugins.
    *Note:* this settings should be used with care as it can break the
    auto update feature

#### <span id="GUI_Options" class="mw-headline">GUI Options</span><span class="mw-editsection"><span class="mw-editsection-bracket">\[</span>[edit](/web/20210712091909/http://wiki.vuze.com/mediawiki/index.php?title=Commandline_options&action=edit&section=8 "Edit section: GUI Options")<span class="mw-editsection-bracket">\]</span></span>

-   **-Dazureus.skipSWTcheck=1** Skip the SWT version check at startup.
    This is useful for an OS that do not have the latest SWT binaries
    available.

#### <span id="Log_Options" class="mw-headline">Log Options</span><span class="mw-editsection"><span class="mw-editsection-bracket">\[</span>[edit](/web/20210712091909/http://wiki.vuze.com/mediawiki/index.php?title=Commandline_options&action=edit&section=9 "Edit section: Log Options")<span class="mw-editsection-bracket">\]</span></span>

-   **-Dazureus.overridelog=1** Override logging setting, and enable
    logging, file logging, and all options. Log directory will be the
    current directory.
-   **-Dazureus.overridelogdir=\<dirpath>** New as of version 3.1.1.1 -
    if above option is enabled, this parameter will specify where to
    store the log files (instead of the current directory).
-   **-Dazureus.log.stdout=1** Send all log output to standard out /
    console / terminal.
-   **-Dlog.unknown.peerids=1** Log all unknown Peer IDs to a file
    called identification.log in the config path. As of version 3.1.1.1,
    this will now be stored in the log directory, stored in files named
    clientid_x.log and is enabled by default (you can set the value to 0
    to disable it).
-   **-Dazureus.log.dos=1** Log DOS info from Azureus' Tracker to
    dos.log in the user directory.
-   **-Ddiag.logsize=2M** Change the maximum size of the debugging log
    files from the default 256 kB, e.g. to 2 MB.
-   **-Ddebug.swtexec=1** Creates also swt_x.log debug files enabling a
    better debugging of UI events.

#### <span id="Memory_Limits" class="mw-headline">Memory Limits</span><span class="mw-editsection"><span class="mw-editsection-bracket">\[</span>[edit](/web/20210712091909/http://wiki.vuze.com/mediawiki/index.php?title=Commandline_options&action=edit&section=10 "Edit section: Memory Limits")<span class="mw-editsection-bracket">\]</span></span>

-   **-Xmx\<nnn>m** Sets the maximum heap size to *\<nnn>* MiB (might be
    necessary when OutOfMemory errors occur)
-   **-XX:MaxDirectMemorySize=\<nnn>m** Sets the maximum direct memory
    size to *\<nnn>* MiB (Azureus will notify you when this should
    become necessary)
-   see [Reduce memory
    usage](/web/20210712091909/http://wiki.vuze.com/w/Reduce_memory_usage "Reduce memory usage")
    for further details

#### <span id=".22Safe_Mode.22_Options" class="mw-headline">"Safe Mode" Options</span><span class="mw-editsection"><span class="mw-editsection-bracket">\[</span>[edit](/web/20210712091909/http://wiki.vuze.com/mediawiki/index.php?title=Commandline_options&action=edit&section=11 "Edit section: "Safe Mode" Options")<span class="mw-editsection-bracket">\]</span></span>

-   **-Dazureus.safemode=1** Loads Azureus in safe mode - this disables
    the loading of external plugins, loading of downloads, and disables
    other features - this should only be used to change your
    configuration or to generate a debug log when you can't load Azureus
    normally. Available from version 3.1.1.1 onwards.
-   **-Dazureus.disabledownloads=1** Avoid loading the downloads in
    Azureus - any newly added downloads will not be remembered when the
    program is closed. Available from version 3.1.1.1 onwards.
-   **-Dazureus.loadplugins=0** Skips loading of all plugins - you can
    go to the Options -> Plugins page, and click the *Scan for plugins*
    button to then list all the plugins that are available. Available
    from version 3.1.1.1 onwards.

#### <span id="Console_UI_Options" class="mw-headline">Console UI Options</span><span class="mw-editsection"><span class="mw-editsection-bracket">\[</span>[edit](/web/20210712091909/http://wiki.vuze.com/mediawiki/index.php?title=Commandline_options&action=edit&section=12 "Edit section: Console UI Options")<span class="mw-editsection-bracket">\]</span></span>

-   **-Dazureus.console.noisy=on** New in 3.1.1.1. In older versions for
    Azureus, any debug statements and errors from Azureus or any plugins
    were displayed in the console. In 3.1.1.1 and above, this is now
    prevented, and is only displayed if this option is used.

## <span id="Manually_starting_directly_with_Java" class="mw-headline">Manually starting directly with Java</span><span class="mw-editsection"><span class="mw-editsection-bracket">\[</span>[edit](/web/20210712091909/http://wiki.vuze.com/mediawiki/index.php?title=Commandline_options&action=edit&section=13 "Edit section: Manually starting directly with Java")<span class="mw-editsection-bracket">\]</span></span>

### <span id="Windows" class="mw-headline">Windows</span><span class="mw-editsection"><span class="mw-editsection-bracket">\[</span>[edit](/web/20210712091909/http://wiki.vuze.com/mediawiki/index.php?title=Commandline_options&action=edit&section=14 "Edit section: Windows")<span class="mw-editsection-bracket">\]</span></span>

Here's an example command line to start Vuze on a Windows 7 system
running Java 1.6 (or 6 as it is also known)

Open a Command Prompt (DOS Box as it used to be known) - Open the start
menu and type 'cmd' into the search box

```
cd "c:\Program Files (x86)\Vuze"

"c:\Program Files (x86)\Java\jre6\bin\java" -classpath Azureus2.jar;swt.jar org.gudy.azureus2.ui.swt.Main
```

Note that the location of your Java executable (...\\bin\\java above)
will vary depending on where it is installed. Other example locations
are

<div style="text-align:right; margin-bottom:-37px;">

Copy to Clipboard

</div>

```
"c:\Program Files (x86)\Java\jre7\bin\java"
"c:\Program Files (x86)\Java\jre8\bin\java"
"c:\Program Files (x86)\Java\jre9\bin\java"
```

or with the (x86) removed:

<div style="text-align:right; margin-bottom:-37px;">

Copy to Clipboard

</div>

```
"c:\Program Files\Java\jre6\bin\java"
```

etc.

or even just

<div style="text-align:right; margin-bottom:-37px;">

Copy to Clipboard

</div>

```
java -classpath...
```

## <span id="Changing_the_Control_Port" class="mw-headline">Changing the Control Port</span><span class="mw-editsection"><span class="mw-editsection-bracket">\[</span>[edit](/web/20210712091909/http://wiki.vuze.com/mediawiki/index.php?title=Commandline_options&action=edit&section=15 "Edit section: Changing the Control Port")<span class="mw-editsection-bracket">\]</span></span>

Vuze uses a local TCP socket connection to support communication with a
running instance of Vuze - for example, to send it instructions to open
a .torrent file or magnet link.

By default this is port 6880.

If another application happens to use the same port number then this
prevents Vuze from operating correctly. There are two solutions to this
problem, either terminate the other application or change the port that
Vuze uses.

The port can be changed by passing a parameter to Vuze when starting it

<div style="text-align:right; margin-bottom:-37px;">

Copy to Clipboard

</div>

```
   azureus.instance.port=<port_number>
```

The \<port_number> should be selected to be between 1025 and 65535 and
not already in use on your system.

The various ways of doing this are discussed above and there is an
example for how to do it on Windows via the preferred approach of
[modifying the Azureus.exe.vmoptions
file](/web/20210712091909/http://wiki.vuze.com/w/Commandline_options#VM_Options_file_.28windows_only.29 "Commandline options")

Assuming that you picked 38154 as the port to use the options file would
end up looking something like

<div style="text-align:right; margin-bottom:-37px;">

Copy to Clipboard

</div>

```
   -include-options ${APPDATA}\Azureus\java.vmoptions
   -Dazureus.instance.port=38154
```

The first line above is the default entry added by Vuze. If you wanted
to use different ports for different users on your machine then you
would need to make the change to the referenced
${APPDATA}\\Azureus\\java.vmoptions file instead.

</div>

<div class="printfooter">

Retrieved from
"[http://wiki.vuze.com/mediawiki/index.php?title=Commandline_options&oldid=17206](https://web.archive.org/web/20210712091909/http://wiki.vuze.com/mediawiki/index.php?title=Commandline_options&oldid=17206)"

</div>

<div id="catlinks" class="catlinks" mw="interface">

<div id="mw-normal-catlinks" class="mw-normal-catlinks">

[Categories](/web/20210712091909/http://wiki.vuze.com/w/Special:Categories "Special:Categories"):

-   [Documentation](/web/20210712091909/http://wiki.vuze.com/w/Category:Documentation "Category:Documentation")
-   [Technical
    Information](/web/20210712091909/http://wiki.vuze.com/w/Category:Technical_Information "Category:Technical Information")

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
    account](/web/20210712091909/http://wiki.vuze.com/mediawiki/index.php?title=Special:CreateAccount&returnto=Commandline+options "You are encouraged to create an account and log in; however, it is not mandatory")</span>
-   <span id="pt-login">[Log
    in](/web/20210712091909/http://wiki.vuze.com/mediawiki/index.php?title=Special:UserLogin&returnto=Commandline+options "You are encouraged to log in; however, it is not mandatory [o]")</span>

</div>

<div id="left-navigation">

<div id="p-namespaces" class="vectorTabs" role="navigation"
aria-labelledby="p-namespaces-label">

### Namespaces

-   <span
    id="ca-nstab-main">[Page](/web/20210712091909/http://wiki.vuze.com/w/Commandline_options "View the content page [c]")</span>
-   <span
    id="ca-talk">[Discussion](/web/20210712091909/http://wiki.vuze.com/mediawiki/index.php?title=Talk:Commandline_options&action=edit&redlink=1 "Discussion about the content page [t]")</span>

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
    id="ca-view">[Read](/web/20210712091909/http://wiki.vuze.com/w/Commandline_options)</span>
-   <span
    id="ca-edit">[Edit](/web/20210712091909/http://wiki.vuze.com/mediawiki/index.php?title=Commandline_options&action=edit "Edit this page [e]")</span>
-   <span id="ca-history">[View
    history](/web/20210712091909/http://wiki.vuze.com/mediawiki/index.php?title=Commandline_options&action=history "Past revisions of this page [h]")</span>

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
    here](/web/20210712091909/http://wiki.vuze.com/w/Special:WhatLinksHere/Commandline_options "A list of all wiki pages that link here [j]")</span>
-   <span id="t-recentchangeslinked">[Related
    changes](/web/20210712091909/http://wiki.vuze.com/w/Special:RecentChangesLinked/Commandline_options "Recent changes in pages linked from this page [k]")</span>
-   <span id="t-specialpages">[Special
    pages](/web/20210712091909/http://wiki.vuze.com/w/Special:SpecialPages "A list of all special pages [q]")</span>
-   <span id="t-print">[Printable
    version](/web/20210712091909/http://wiki.vuze.com/mediawiki/index.php?title=Commandline_options&printable=yes "Printable version of this page [p]")</span>
-   <span id="t-permalink">[Permanent
    link](/web/20210712091909/http://wiki.vuze.com/mediawiki/index.php?title=Commandline_options&oldid=17206 "Permanent link to this revision of the page")</span>
-   <span id="t-info">[Page
    information](/web/20210712091909/http://wiki.vuze.com/mediawiki/index.php?title=Commandline_options&action=info "More information about this page")</span>

</div>

</div>

</div>

</div>

<div id="footer" role="contentinfo">

-   <span id="footer-info-lastmod">This page was last modified on 5
    March 2016, at 23:07.</span>
-   <span id="footer-info-viewcount">This page has been accessed 173,420
    times.</span>

<!-- -->

-   <span id="footer-places-about">[About
    VuzeWiki](/web/20210712091909/http://wiki.vuze.com/w/VuzeWiki:About "VuzeWiki:About")</span>
-   <span
    id="footer-places-mobileview"><a href="https://web.archive.org/web/20210712091909/http://wiki.vuze.com/mediawiki/index.php?title=Commandline_options&amp;mobileaction=toggle_view_mobile" class="noprint stopMobileRedirectToggle">Mobile view</a></span>

<!-- -->

-   <span
    id="footer-poweredbyico">[<img src="/web/20210712091909im_/http://wiki.vuze.com/mediawiki/resources/assets/poweredby_mediawiki_88x31.png" srcset="/web/20210712091909im_/http://wiki.vuze.com/mediawiki/resources/assets/poweredby_mediawiki_132x47.png 1.5x, /web/20210712091909im_/http://wiki.vuze.com/mediawiki/resources/assets/poweredby_mediawiki_176x62.png 2x" width="88" height="31" alt="Powered by MediaWiki" />](//web.archive.org/web/20210712091909/http://www.mediawiki.org/)</span>
-   <span id="footer-analyticsystemsico">Any use of Vuze® and Vuze+™
    that violates the rights of any person or entity is not allowed.
    [More](https://web.archive.org/web/20210712091909/http://vuze.com/corp/legal.php)</span>

<div style="clear:both">

</div>

</div>
