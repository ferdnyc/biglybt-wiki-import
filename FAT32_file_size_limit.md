<div id="mw-page-base" class="noprint">

</div>

<div id="mw-head-base" class="noprint">

</div>

<div id="content" class="mw-body" role="main">

<span id="top"></span>

<div class="mw-indicators">

</div>

# FAT32 file size limit

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

## <span id="FAT32_file_size_limit:_4_GB" class="mw-headline">FAT32 file size limit: 4 GB</span>

FAT32 (or the even older FAT16) is the file system used in older MS-DOS
and Windows systems. It has been replaced by NTFS in the newest Windows
operating systems, and Vista and Windows 7 do not even install into a
FAT32 drive. NTFS is more reliable and offers better security and
protection against data loss.

FAT32 is typically still the default file system in external hard disks,
and it was also widely used by major PC manufacturers with pre-installed
Windows XP systems.

FAT32 has several limitations and drawbacks compared to NTFS. From
bittorrent usage perspective, **the limitation of the maximum file size
of 4 Gigabytes is the most important one**. Information from Microsoft:
<a href="https://web.archive.org/web/20180603130558/http://support.microsoft.com/default.aspx?scid=kb;en-us;314463" class="external text">Limitations of the FAT32 File System in Windows XP</a>

It is not possible to have a larger than 4 GB file on a disk with FAT32
file system. If you try to download a torrent where at least one file
has a size over 4 GB, Vuze will complain to you that "**there is not
enough space on the disk**" and will not create the file (as the OS
prevents the creation).

Check your drive's properties for its file system type: FAT32 or NTFS

<a href="/web/20180603130558/http://wiki.vuze.com/w/File:FileSystemType.png" class="image"><img src="/web/20180603130558im_/http://wiki.vuze.com/mediawiki/images/b/b5/FileSystemType.png" width="367" height="493" alt="FileSystemType.png" /></a>

## <span id="Convert_a_FAT32_volume_to_an_NTFS_file_system" class="mw-headline">Convert a FAT32 volume to an NTFS file system</span>

<div
style="color: #aa0000; background: #eeeeee;border: 3px solid red; padding: 1em; margin: auto; width: 65%;">

Note: Although the chance of corruption or data loss during the
conversion is minimal, we recommend that you perform a backup of the
data on the volume that you want to convert before you start the
conversion.

</div>

  
Windows XP, Vista and Windows 7 contain a command-line tool
**"convert"** for converting an existing FAT32 disk to NTFS without need
for formatting or any data loss. Microsoft gives instructions for that:
<a href="https://web.archive.org/web/20180603130558/http://support.microsoft.com/kb/307881" class="external text">How to convert a FAT16 volume or a FAT32 volume to an NTFS file system in Windows XP</a>

To convert an existing FAT32 volume to NTFS, follow these steps as
described in the referenced Microsoft knowledgebase article:

-   Click Start, point to All Programs, point to Accessories, and then
    click Command Prompt.
-   At the command prompt, type the following, where drive letter is the
    drive that you want to convert:

*convert drive letter: /fs:ntfs*

For example, type the following command to convert drive E to NTFS:

*convert e: /fs:ntfs*

Note If the operating system is on the drive that you are converting,
you will be prompted to schedule the task when you restart the computer
because the conversion cannot be completed while the operating system is
running. When you are prompted, click YES.

-   When you receive the following message at the command prompt, type
    the volume label of the drive that you are converting, and then
    press ENTER:

*The type of the file system is FAT.*

*Enter the current volume label for drive drive letter*

-   When the conversion to NTFS is complete, you receive the following
    message at the command prompt:

*Conversion complete*

-   Quit the command prompt.

  

<span class="small">Read the [Azureus
FAQ](/web/20180603130558/http://wiki.vuze.com/w/Azureus_FAQ "Azureus FAQ")</span>

</div>

<div class="printfooter">

Retrieved from
"[http://wiki.vuze.com/mediawiki/index.php?title=FAT32_file_size_limit&oldid=11669](https://web.archive.org/web/20180603130558/http://wiki.vuze.com/mediawiki/index.php?title=FAT32_file_size_limit&oldid=11669)"

</div>

<div id="catlinks" class="catlinks" mw="interface">

<div id="mw-normal-catlinks" class="mw-normal-catlinks">

[Category](/web/20180603130558/http://wiki.vuze.com/w/Special:Categories "Special:Categories"):

-   [Troubleshooting](/web/20180603130558/http://wiki.vuze.com/w/Category:Troubleshooting "Category:Troubleshooting")

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
    id="pt-anontalk">[Talk](/web/20180603130558/http://wiki.vuze.com/w/Special:MyTalk "Discussion about edits from this IP address [n]")</span>
-   <span
    id="pt-anoncontribs">[Contributions](/web/20180603130558/http://wiki.vuze.com/w/Special:MyContributions "A list of edits made from this IP address [y]")</span>
-   <span id="pt-createaccount">[Create
    account](/web/20180603130558/http://wiki.vuze.com/mediawiki/index.php?title=Special:CreateAccount&returnto=FAT32+file+size+limit "You are encouraged to create an account and log in; however, it is not mandatory")</span>
-   <span id="pt-login">[Log
    in](/web/20180603130558/http://wiki.vuze.com/mediawiki/index.php?title=Special:UserLogin&returnto=FAT32+file+size+limit "You are encouraged to log in; however, it is not mandatory [o]")</span>

</div>

<div id="left-navigation">

<div id="p-namespaces" class="vectorTabs" role="navigation"
aria-labelledby="p-namespaces-label">

### Namespaces

-   <span
    id="ca-nstab-main">[Page](/web/20180603130558/http://wiki.vuze.com/w/FAT32_file_size_limit "View the content page [c]")</span>
-   <span
    id="ca-talk">[Discussion](/web/20180603130558/http://wiki.vuze.com/w/Talk:FAT32_file_size_limit "Discussion about the content page [t]")</span>

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
    id="ca-view">[Read](/web/20180603130558/http://wiki.vuze.com/w/FAT32_file_size_limit)</span>
-   <span id="ca-viewsource">[View
    source](/web/20180603130558/http://wiki.vuze.com/mediawiki/index.php?title=FAT32_file_size_limit&action=edit "This page is protected.
    You can view its source [e]")</span>
-   <span id="ca-history">[View
    history](/web/20180603130558/http://wiki.vuze.com/mediawiki/index.php?title=FAT32_file_size_limit&action=history "Past revisions of this page [h]")</span>

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

<a href="/web/20180603130558/http://wiki.vuze.com/w/Main_Page" class="mw-wiki-logo" title="Visit the main page"></a>

</div>

<div id="p-" class="portal" role="navigation"
aria-labelledby="p--label">

### 

<div class="body">

-   <span id="n-Download-Vuze-Now">[Download Vuze
    Now](https://web.archive.org/web/20180603130558/http://www.vuze.com/download)</span>

</div>

</div>

<div id="p-navigation" class="portal" role="navigation"
aria-labelledby="p-navigation-label">

### Navigation

<div class="body">

-   <span id="n-mainpage-description">[Main
    page](/web/20180603130558/http://wiki.vuze.com/w/Main_Page "Visit the main page [z]")</span>
-   <span id="n-recentchanges">[Recent
    changes](/web/20180603130558/http://wiki.vuze.com/w/Special:RecentChanges "A list of recent changes in the wiki [r]")</span>
-   <span id="n-randompage">[Random
    page](/web/20180603130558/http://wiki.vuze.com/w/Special:Random "Load a random page [x]")</span>
-   <span
    id="n-help">[Help](https://web.archive.org/web/20180603130558/https://www.mediawiki.org/wiki/Special:MyLanguage/Help:Contents "The place to find out")</span>

</div>

</div>

<div id="p-tb" class="portal" role="navigation"
aria-labelledby="p-tb-label">

### Tools

<div class="body">

-   <span id="t-whatlinkshere">[What links
    here](/web/20180603130558/http://wiki.vuze.com/w/Special:WhatLinksHere/FAT32_file_size_limit "A list of all wiki pages that link here [j]")</span>
-   <span id="t-recentchangeslinked">[Related
    changes](/web/20180603130558/http://wiki.vuze.com/w/Special:RecentChangesLinked/FAT32_file_size_limit "Recent changes in pages linked from this page [k]")</span>
-   <span id="t-specialpages">[Special
    pages](/web/20180603130558/http://wiki.vuze.com/w/Special:SpecialPages "A list of all special pages [q]")</span>
-   <span id="t-print">[Printable
    version](/web/20180603130558/http://wiki.vuze.com/mediawiki/index.php?title=FAT32_file_size_limit&printable=yes "Printable version of this page [p]")</span>
-   <span id="t-permalink">[Permanent
    link](/web/20180603130558/http://wiki.vuze.com/mediawiki/index.php?title=FAT32_file_size_limit&oldid=11669 "Permanent link to this revision of the page")</span>
-   <span id="t-info">[Page
    information](/web/20180603130558/http://wiki.vuze.com/mediawiki/index.php?title=FAT32_file_size_limit&action=info "More information about this page")</span>

</div>

</div>

</div>

</div>

<div id="footer" role="contentinfo">

-   <span id="footer-info-lastmod">This page was last modified on 29
    November 2011, at 14:57.</span>
-   <span id="footer-info-viewcount">This page has been accessed 59,265
    times.</span>

<!-- -->

-   <span id="footer-places-about">[About
    VuzeWiki](/web/20180603130558/http://wiki.vuze.com/w/VuzeWiki:About "VuzeWiki:About")</span>
-   <span
    id="footer-places-mobileview"><a href="https://web.archive.org/web/20180603130558/http://wiki.vuze.com/mediawiki/index.php?title=FAT32_file_size_limit&amp;mobileaction=toggle_view_mobile" class="noprint stopMobileRedirectToggle">Mobile view</a></span>

<!-- -->

-   <span
    id="footer-poweredbyico">[<img src="/web/20180603130558im_/http://wiki.vuze.com/mediawiki/resources/assets/poweredby_mediawiki_88x31.png" srcset="/web/20180603130558im_/http://wiki.vuze.com/mediawiki/resources/assets/poweredby_mediawiki_132x47.png 1.5x, /web/20180603130558im_/http://wiki.vuze.com/mediawiki/resources/assets/poweredby_mediawiki_176x62.png 2x" width="88" height="31" alt="Powered by MediaWiki" />](//web.archive.org/web/20180603130558/http://www.mediawiki.org/)</span>
-   <span id="footer-analyticsystemsico">Any use of Vuze® and Vuze+™
    that violates the rights of any person or entity is not allowed.
    [More](https://web.archive.org/web/20180603130558/http://vuze.com/corp/legal.php)</span>

<div style="clear:both">

</div>

</div>
