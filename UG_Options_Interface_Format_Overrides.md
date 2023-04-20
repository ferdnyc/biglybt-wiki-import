<div id="mw-page-base" class="noprint">

</div>

<div id="mw-head-base" class="noprint">

</div>

<div id="content" class="mw-body" role="main">

<span id="top"></span>

# <span dir="auto">UG Options Interface Format Overrides</span>

<div id="bodyContent" class="mw-body-content">

<div id="siteSub">

From VuzeWiki

</div>

<div id="contentSub">

</div>

<div id="jump-to-nav" class="mw-jump">

Jump to: [navigation](#mw-navigation), [search](#p-search)

</div>

<div id="mw-content-text" class="mw-content-ltr" lang="en" dir="ltr">

Custom formatting is available for some user interface components such
as rate display.

To allow flexibility and extensibility the format overrides are
specified using a series of lines of the form

    <component name> : <format specification>

Component names currently defined are

    title.rate    Rate format for the main Vuze window title (when enabled)
    column.size   Column size formatting in library views (5621_B04+)

Format specifications define how the component's value is displayed.
They are made up of a number of parameters separated by commas:

    format_specification: <format_parameters> (, <format_parameters>)*

    format_parameters: <format_parameter> (; <format_parameter>)*

    format_parameter: 
        units=<unit> (&<unit>)+
            [;hide=(y|n)] [;short=(y|n)] [;rate=(y|n)]
        format=<format_pattern>
            [;round=(up|down|halfup|halfdown)]

    format_pattern: see link below

    unit: b|k|m|g|t

Format patters are described here:
<a href="https://web.archive.org/web/20150924224503/http://java.sun.com/docs/books/tutorial/i18n/format/decimalFormat.html" class="external free">http://java.sun.com/docs/books/tutorial/i18n/format/decimalFormat.html</a>

For example, to change the rate display used for the main Vuze window
(and hence task-bar information) to just use kilobytes, hide the rate
unit and show two decimal places

    title.rate: units=k;hide=y, format=0.00

To show column sizes in MB with 3 decimal places and rounded up

    column.size: units=m, format=0.000;round=up

</div>

<div class="printfooter">

Retrieved from
"[http://wiki.vuze.com/mediawiki/index.php?title=UG_Options_Interface_Format_Overrides&oldid=16682](https://web.archive.org/web/20150924224503/http://wiki.vuze.com/mediawiki/index.php?title=UG_Options_Interface_Format_Overrides&oldid=16682)"

</div>

<div id="catlinks" class="catlinks catlinks-allhidden">

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

-   <span id="pt-createaccount">[Create
    account](/web/20150924224503/http://wiki.vuze.com/mediawiki/index.php?title=Special:UserLogin&returnto=UG+Options+Interface+Format+Overrides&type=signup)</span>
-   <span id="pt-login">[Log
    in](/web/20150924224503/http://wiki.vuze.com/mediawiki/index.php?title=Special:UserLogin&returnto=UG+Options+Interface+Format+Overrides "You are encouraged to log in; however, it is not mandatory [o]")</span>

</div>

<div id="left-navigation">

<div id="p-namespaces" class="vectorTabs" role="navigation"
aria-labelledby="p-namespaces-label">

### Namespaces

-   <span
    id="ca-nstab-main">[Page](/web/20150924224503/http://wiki.vuze.com/w/UG_Options_Interface_Format_Overrides "View the content page [c]")</span>
-   <span
    id="ca-talk">[Discussion](/web/20150924224503/http://wiki.vuze.com/mediawiki/index.php?title=Talk:UG_Options_Interface_Format_Overrides&action=edit&redlink=1 "Discussion about the content page [t]")</span>

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
    id="ca-view">[Read](/web/20150924224503/http://wiki.vuze.com/w/UG_Options_Interface_Format_Overrides)</span>
-   <span id="ca-viewsource">[View
    source](/web/20150924224503/http://wiki.vuze.com/mediawiki/index.php?title=UG_Options_Interface_Format_Overrides&action=edit "This page is protected.
    You can view its source [e]")</span>
-   <span id="ca-history">[View
    history](/web/20150924224503/http://wiki.vuze.com/mediawiki/index.php?title=UG_Options_Interface_Format_Overrides&action=history "Past revisions of this page [h]")</span>

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

[](/web/20150924224503/http://wiki.vuze.com/w/Main_Page "Visit the main page")

</div>

<div id="p-" class="portal" role="navigation"
aria-labelledby="p--label">

### 

<div class="body">

-   <span id="n-Download-Vuze-Now">[Download Vuze
    Now](https://web.archive.org/web/20150924224503/http://www.vuze.com/download)</span>

</div>

</div>

<div id="p-navigation" class="portal" role="navigation"
aria-labelledby="p-navigation-label">

### Navigation

<div class="body">

-   <span id="n-mainpage-description">[Main
    page](/web/20150924224503/http://wiki.vuze.com/w/Main_Page "Visit the main page [z]")</span>
-   <span id="n-recentchanges">[Recent
    changes](/web/20150924224503/http://wiki.vuze.com/w/Special:RecentChanges "A list of recent changes in the wiki [r]")</span>
-   <span id="n-randompage">[Random
    page](/web/20150924224503/http://wiki.vuze.com/w/Special:Random "Load a random page [x]")</span>
-   <span
    id="n-help">[Help](https://web.archive.org/web/20150924224503/https://www.mediawiki.org/wiki/Special:MyLanguage/Help:Contents "The place to find out")</span>

</div>

</div>

<div id="p-tb" class="portal" role="navigation"
aria-labelledby="p-tb-label">

### Tools

<div class="body">

-   <span id="t-whatlinkshere">[What links
    here](/web/20150924224503/http://wiki.vuze.com/w/Special:WhatLinksHere/UG_Options_Interface_Format_Overrides "A list of all wiki pages that link here [j]")</span>
-   <span id="t-recentchangeslinked">[Related
    changes](/web/20150924224503/http://wiki.vuze.com/w/Special:RecentChangesLinked/UG_Options_Interface_Format_Overrides "Recent changes in pages linked from this page [k]")</span>
-   <span id="t-specialpages">[Special
    pages](/web/20150924224503/http://wiki.vuze.com/w/Special:SpecialPages "A list of all special pages [q]")</span>
-   <span id="t-print">[Printable
    version](/web/20150924224503/http://wiki.vuze.com/mediawiki/index.php?title=UG_Options_Interface_Format_Overrides&printable=yes "Printable version of this page [p]")</span>
-   <span id="t-permalink">[Permanent
    link](/web/20150924224503/http://wiki.vuze.com/mediawiki/index.php?title=UG_Options_Interface_Format_Overrides&oldid=16682 "Permanent link to this revision of the page")</span>
-   <span id="t-info">[Page
    information](/web/20150924224503/http://wiki.vuze.com/mediawiki/index.php?title=UG_Options_Interface_Format_Overrides&action=info)</span>

</div>

</div>

</div>

</div>

<div id="footer" role="contentinfo">

-   <span id="footer-info-lastmod">This page was last modified on 20
    August 2015, at 15:59.</span>
-   <span id="footer-info-viewcount">This page has been accessed 626
    times.</span>

<!-- -->

-   <span id="footer-places-about">[About
    VuzeWiki](/web/20150924224503/http://wiki.vuze.com/w/VuzeWiki:About "VuzeWiki:About")</span>
-   <span
    id="footer-places-mobileview"><a href="https://web.archive.org/web/20150924224503/http://wiki.vuze.com/mediawiki/index.php?title=UG_Options_Interface_Format_Overrides&amp;mobileaction=toggle_view_mobile" class="noprint stopMobileRedirectToggle">Mobile view</a></span>

<!-- -->

-   <span
    id="footer-poweredbyico">[<img src="/web/20150924224503im_/http://wiki.vuze.com/mediawiki/resources/assets/poweredby_mediawiki_88x31.png" width="88" height="31" alt="Powered by MediaWiki" />](//web.archive.org/web/20150924224503/http://www.mediawiki.org/)</span>
-   <span id="footer-analyticsystemsico">Any use of Vuze® and Vuze+™
    that violates the rights of any person or entity is not allowed.
    [More](https://web.archive.org/web/20150924224503/http://vuze.com/corp/legal.php)</span>

<div style="clear:both">

</div>

</div>
