<div id="mw-page-base" class="noprint">

</div>

<div id="mw-head-base" class="noprint">

</div>

<div id="content" class="mw-body" role="main">

<span id="top"></span>

<div class="mw-indicators">

</div>

# NAT problem

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

  

## <span id="Quick_outline" class="mw-headline">Quick outline</span><span class="mw-editsection"><span class="mw-editsection-bracket">\[</span>[edit](/web/20210422050047/http://wiki.vuze.com/mediawiki/index.php?title=NAT_problem&action=edit&section=1 "Edit section: Quick outline")<span class="mw-editsection-bracket">\]</span></span>

To fix a
[NAT](/web/20210422050047/http://wiki.vuze.com/w/What_is_NAT "What is NAT")
issue, you have to consider multiple factors that can cause it. Here's a
quick outline of what you have to do; for more detailed explanations and
instructions have a look at the [next chapter](#Detailed_guideline).

  
There are several causes of reachability problems:

-   Routers/Broadband modems
    a\) Devices without
    [UPnP](/web/20210422050047/http://wiki.vuze.com/w/UPnP "UPnP") or
    [NAT-PMP](/web/20210422050047/http://wiki.vuze.com/w/NATPMP "NATPMP")
    1.  you have to set your PC to a [static
        IP](/web/20210422050047/http://wiki.vuze.com/w/Static_IP "Static IP")
        (i.e. don't use DHCP) or use your router's MAC-address binding
        to allocate a specific IP to your network card
    2.  log into your router (if you don't know its address read the
        manual or determine the gateway address, which should be the
        address of your router)
    3.  Setup [port
        forwarding](/web/20210422050047/http://wiki.vuze.com/w/Port_forwarding "Port forwarding")
        by setting up rules to forward Vuze' listening ports (UDP *and*
        TCP) as external ports to the IP of your computer and the same
        ports on your computer.
        *Note:* The exact wording is different for each router, thus it
        might be called port forwarding, opening pinholes through the
        firewall, NAT rules, virtual server or something else.
    4.  Turn off UPnP in Vuze in Tools > Options > Plugins > UPnP, since
        it may confuse some routers that do not support or correctly
        support UPnP.

    b\) Devices with UPnP/NAT-PMP
    Just enable the UPnP/NAT-PMP plugin under tools -> options ->
    plugins -> UPnP and set it to report everything to get some
    feedback, once it works you can turn the messages off again. Sadly
    some routers that claim to support UPnP don't interoperate with Vuze
    correctly, if that's the case have a look at point a).
-   Software firewalls and antivirus software including firewalls:
    -   If the firewall is port based you have to allow incoming
        connections to the UDP and TCP ports used by Vuze (tools ->
        options -> connection)
    -   For application-based firewalls you have to allow Vuze.exe (or
        javaw.exe) to access the internet *and* accept incoming
        connections
    -   Some firewalls have a generic setting to prevent incoming (WAN)
        connections, this should be disabled too

## <span id="Detailed_guideline" class="mw-headline">Detailed guideline</span><span class="mw-editsection"><span class="mw-editsection-bracket">\[</span>[edit](/web/20210422050047/http://wiki.vuze.com/mediawiki/index.php?title=NAT_problem&action=edit&section=2 "Edit section: Detailed guideline")<span class="mw-editsection-bracket">\]</span></span>

<div id="toc" class="toc">

<div id="toctitle">

## Contents

</div>

-   [<span class="tocnumber">1</span> <span class="toctext">Quick
    outline</span>](#Quick_outline)
-   [<span class="tocnumber">2</span> <span class="toctext">Detailed
    guideline</span>](#Detailed_guideline)
-   [<span class="tocnumber">3</span> <span class="toctext">Understand
    what a NAT problem is</span>](#Understand_what_a_NAT_problem_is)
-   [<span class="tocnumber">4</span> <span class="toctext">Fix your NAT
    problem</span>](#Fix_your_NAT_problem)
    -   [<span class="tocnumber">4.1</span> <span
        class="toctext">Routers And NAT Enabled Broadband
        Modems</span>](#Routers_And_NAT_Enabled_Broadband_Modems)
        -   [<span class="tocnumber">4.1.1</span> <span
            class="toctext">Port Forwarding Through The
            Router</span>](#Port_Forwarding_Through_The_Router)
        -   [<span class="tocnumber">4.1.2</span> <span
            class="toctext">Port forwarding with two
            routers</span>](#Port_forwarding_with_two_routers)
        -   [<span class="tocnumber">4.1.3</span> <span
            class="toctext">Port Forwarding through Windows XP Internet
            Connection
            Sharing</span>](#Port_Forwarding_through_Windows_XP_Internet_Connection_Sharing)
        -   [<span class="tocnumber">4.1.4</span> <span
            class="toctext">Port Forwarding on Linux, specifically
            Ubuntu</span>](#Port_Forwarding_on_Linux.2C_specifically_Ubuntu)
    -   [<span class="tocnumber">4.2</span> <span class="toctext">VPNs
        and Windows Routing and Remote
        Access</span>](#VPNs_and_Windows_Routing_and_Remote_Access)
        -   [<span class="tocnumber">4.2.1</span> <span
            class="toctext">VPNs</span>](#VPNs)
        -   [<span class="tocnumber">4.2.2</span> <span
            class="toctext">Windows Routing and Remote
            Access</span>](#Windows_Routing_and_Remote_Access)
    -   [<span class="tocnumber">4.3</span> <span
        class="toctext">Software Firewalls</span>](#Software_Firewalls)
    -   [<span class="tocnumber">4.4</span> <span
        class="toctext">Anti-virus
        Programs</span>](#Anti-virus_Programs)
    -   [<span class="tocnumber">4.5</span> <span
        class="toctext">Mobile/3G/satellite
        connections</span>](#Mobile.2F3G.2Fsatellite_connections)
    -   [<span class="tocnumber">4.6</span> <span class="toctext">Final
        Thoughts</span>](#Final_Thoughts)
-   [<span class="tocnumber">5</span> <span
    class="toctext">Conclusion</span>](#Conclusion)
    -   [<span class="tocnumber">5.1</span> <span class="toctext">STILL
        Not Working?</span>](#STILL_Not_Working.3F)

</div>

  

  

  

<div id="fix">

## <span id="Understand_what_a_NAT_problem_is" class="mw-headline">Understand what a NAT problem is</span><span class="mw-editsection"><span class="mw-editsection-bracket">\[</span>[edit](/web/20210422050047/http://wiki.vuze.com/mediawiki/index.php?title=NAT_problem&action=edit&section=3 "Edit section: Understand what a NAT problem is")<span class="mw-editsection-bracket">\]</span></span>

Basically, a **N**etwork **A**ddress **T**ranslation problem is caused
by a router not being able to do what it's supposed to; it is not
correctly re-directing data it has received from the outside world to a
computer that is connected to it (the one running Vuze in this case).  

Can this page assist you to resolve the NAT issue? That entirely depends
on several factors. Every computer out there is set up slightly
differently - different makes/models of modems and/or routers, different
software firewalls, different antivirus programs, receiving service from
different providers - these are all factors that must be considered when
attempting to solve a NAT error. We'll attempt to approach a NAT problem
broadly so as to encompass and help as many users as possible. Below
we'll cover some basic terminology and acronyms before you actually give
it a shot.  

1.  **ISP**: Internet Service Provider
2.  **Router**: A device that forwards data packets along networks. A
    router is connected to at least two networks, commonly two LANs
    (Local Area Networks), WANs (Wide Area Network), WLANs (Wireless
    LAN), or a LAN and its ISP?s network. Routers are located at
    gateways, the places where two or more networks connect. Routers use
    headers and forwarding tables to determine the best path for
    forwarding the packets, and they use protocols such as TCP/UDP to
    communicate with each other and configure the best route between any
    two hosts.
3.  **IP Address**: Internet Protocol Address. This is a unique string
    of numbers that identifies a computer or server on the Internet.
    These numbers are normally shown in groups separated by periods
    (example: 216.239.57.99 is Google's IP address).
    -   Public IP Address: An address that is given to you by your
        service provider when you connect to them. The majority of users
        have a *dynamic* public IP address (this can change every time a
        connection is established).
    -   Private IP Address: An address that can be assigned by a router
        or your Operating System for your connection to a LAN, WAN, or
        WLAN. The world will never see this address and can be made
        *static* (this will never change once set up correctly).
4.  **DHCP**: Dynamic Host Configuration Protocol. Used for assigning
    dynamic IP addresses to devices on a network. With dynamic
    addressing, a device can have a different IP address every time it
    connects to the network. DHCP also supports a mix of static and
    dynamic IP addresses.
    -   DHCP Pool/Range: The available addresses a router is instructed
        to use when automatically assigning IP addresses to devices.
        Example: LinkSys routers almost all default with a *starting* IP
        address of 192.168.1.100 with 50 available users, effectively
        making the range 192.168.1.100 - 192.168.1.149
5.  **MAC Address**: Media Access Control Address (sometimes referred to
    as a device's *physical address*). MAC addresses are a unique code
    assigned to most forms of networking hardware (for example:
    A0:99:E3:76:BE:01). The address is *permanently* assigned to the
    hardware (network cards/wireless adapters/routers) to act as a
    security feature for limiting access on closed networks. This is
    extremely useful when securing a wireless network.
    -   MAC Address Binding: An option on some routers to bind a MAC
        address to an IP address on a closed LAN or WAN network. When
        available, this method can be used to create a static IP address
        for port forwarding purposes.
6.  **UPnP**: Universal Plug 'n Play. A technological stab at attempting
    to make networking devices a simple task. This has been met by mixed
    reviews and levels of effectiveness by manufacturers and consumers.
    Your network hardware and Operating System may or may not properly
    employ this technology.
7.  **Port Forwarding**: The act of forwarding a network port from one
    machine to another. One use of this technique can allow an external
    user to reach a port on a private IP address (inside a LAN) from the
    outside via a NAT-enabled router.
8.  **Port Triggering**: This allows computers behind a NAT-enabled
    router access to a special server or use a special application on
    the Internet using a specified port number. While similar to port
    forwarding, it is *not* recommended for usage with bittorrents due
    to the timing discrepencies involved with a port constantly being
    told to open with so many connections being generated. It has more
    functions for gaming servers.
9.  **DMZ**: The De-Militarized Zone. When this option is enabled in a
    router, the computer is now *outside* of the internal/protected
    network. Since a DMZ'd computer will be open to allow public access
    to services, it is considered extremely insecure and dangerous. Do
    **NOT** use DMZ in lieu of port forwarding.

## <span id="Fix_your_NAT_problem" class="mw-headline">Fix your NAT problem</span><span class="mw-editsection"><span class="mw-editsection-bracket">\[</span>[edit](/web/20210422050047/http://wiki.vuze.com/mediawiki/index.php?title=NAT_problem&action=edit&section=4 "Edit section: Fix your NAT problem")<span class="mw-editsection-bracket">\]</span></span>

So you really have a
[NAT](/web/20210422050047/http://wiki.vuze.com/w/What_is_NAT "What is NAT")
problem and never get green smilies *and* you are not using one of those
<a href="/web/20210422050047/http://wiki.vuze.com/w/Internet_service_providers_that_do_not_like_file_sharing" class="mw-redirect" title="Internet service providers that do not like file sharing">Internet service providers that do not like file sharing</a>?
OK, read on.  

-   *Please Note:* If you are using file sharing where you have **no
    access to the router** (corporate or campus network, public WLAN
    from a cyber-cafe or a neighbor, or a housing development where
    everyone shares the connection), you must contact the network
    administrator.

You want to select a port that will forward incoming data to your
computer's IP address using the port of choice, and ensure that software
firewalls and antivirus programs do not interfere. If you skimmed the
above passages, you may be confused by the following procedures. You
should read the entire page before proceeding.  

If you know you own a router, continue reading this page in its intended
order.  

If you own a router and you are absolutely positive it properly supports
UPnP, enable UPnP in Vuze (Tools->Options->Plugins->UPnP) and try the
nat/firewall test again. If this doesn't work, skip down to the Software
Firewall section.

If you are unsure as to whether or not you own a router (some broadband
modems have routers with NAT features built-in), consult your ISP or see
your modems manual.

-   A simple test for Windows operating system users is to use ipconfig
    (win2K/XP) or winipcfg (win9X/ME). Go to Start>Run (or hold the
    Windows key and hit "r"), and type in the command "cmd /k ipconfig"
    or "winipcfg.exe" without the quotes, then press the Enter key. If
    the Default Gateway starts with 10.\*.\*.\*, 172.\*.\*.\* or
    192.\*.\*.\*, then it is very likely that there is a router
    involved.

<a href="/web/20210422050047/http://wiki.vuze.com/w/File:IpConfig.png" class="image"><img src="/web/20210422050047im_/http://wiki.vuze.com/mediawiki/images/1/19/IpConfig.png" width="669" height="194" alt="IpConfig.png" /></a>

-   Apple Mac 8.x/9.x: Pull down the Apple menu, select Control Panels.
    Open the control panel TCP/IP. Look for the line Router address.
-   Apple Mac OS X: use either of the following methods:
    -   Pull down the Apple menu, select System Preferences, click
        Network. In the pull-down Show: select the network interface in
        use. Click tab TCP/IP and look for the line Router.
        -   Leopard (10.5.x): Apple menu > System Preferences > Network.
            From list on the left select your connection (Ethernet,
            AirPort, etc.), which is probably already selected. Click
            "Advanced" button and from there the TCP/IP tab. The
            "Router" line will have an IP address listed if you are
            connected through a router.
    -   Open a Terminal window, type the command ipconfig getoption en0
        router (where en0 is the name of the interface in use)

If you are positive you do not own a router or a broadband modem with
NAT features, please skip down to the Software Firewall section.

### <span id="Routers_And_NAT_Enabled_Broadband_Modems" class="mw-headline">Routers And NAT Enabled Broadband Modems</span><span class="mw-editsection"><span class="mw-editsection-bracket">\[</span>[edit](/web/20210422050047/http://wiki.vuze.com/mediawiki/index.php?title=NAT_problem&action=edit&section=5 "Edit section: Routers And NAT Enabled Broadband Modems")<span class="mw-editsection-bracket">\]</span></span>

1.  Ensure you are using a port number that is not already reserved by a
    computer process or PC on your network, or that is possibly being
    blacklisted/throttled by your ISP. (Avoid 6881-6999. Anything from
    49160-65534 is fine)
2.  Create a static IP address for the computer that is running Vuze.
    -   Log into your router's configuration table. This is normally
        done by typing the router's Gateway Address into your browser's
        URL edit box and pressing the Enter key. You should be prompted
        for a username/password before proceeding. If you don't know the
        information, consult your owner's manual or ISP if it originated
        from them. (Note: some devices require utilizing Telnet for
        access and forwarding; the steps will be left out here due to
        their uniqueness. Again, refer to the owner's manual for the
        correct procedure).
    -   If your router supports MAC address binding, do so save/apply
        your changes, and skip down to the "Port Forwarding Through The
        Router" section.
    -   If your router does *not* use MAC address binding, disable or
        limit the DHCP range in the router, then create a static IP
        address for your computer that is OUTSIDE the router's DHCP
        server's IP pool/range (example: the DHCP range is
        192.168.1.100 - 192.168.1.149 .. you would select 192.168.1.200
        as your new static IP address). Here is a
        <a href="https://web.archive.org/web/20210422050047/http://www.portforward.com/networking/staticip.htm" class="external text">static IP guide</a>
        for individual Operating Systems. Once this step completed, your
        connection to your router will be temporarily broken and then
        reconnected a few moments later - this is to be expected. At
        this point, you should restart both your router *and*
        computer(s) on your LAN (some routers do not release the
        previous login and will interefere with the actual port
        forwarding step detailed further below).
        -   Once your computer and router are restarted, use ipconfig or
            winipcfg to ensure the new static IP address is being used
            and continue reading the instructions on this page.

#### <span id="Port_Forwarding_Through_The_Router" class="mw-headline">Port Forwarding Through The Router</span><span class="mw-editsection"><span class="mw-editsection-bracket">\[</span>[edit](/web/20210422050047/http://wiki.vuze.com/mediawiki/index.php?title=NAT_problem&action=edit&section=6 "Edit section: Port Forwarding Through The Router")<span class="mw-editsection-bracket">\]</span></span>

At this point you should now have a static internal/private IP address
for the computer that is running Vuze. Log into your router's
configuration table so that we may actually port forward. Depending on
the device's manufacturer and the model itself, the "place" where you
*do* the forwarding will differ: NAT, NATP, Custom Services, and Virtual
Server are the most commonly named sections, though it's entirely
feasible yours is named something else, but the fundamental procedure
for creating a port forwarding rule is more or less the same and
self-explanatory.  

You may be lucky and find a step-by-step guide for this procedure at
<a href="https://web.archive.org/web/20210422050047/http://www.portforward.com/routers.htm" class="external free">http://www.portforward.com/routers.htm</a>
. They have an excellent list of home routers and modems and configuring
advice for them. They have a browseable
<a href="https://web.archive.org/web/20210422050047/http://portforward.com/english/routers/port_forwarding/routerindex.htm" class="external text">list of routers/modems</a>,
from which

1.  you can select your router
2.  jump over the advertisement page. (In top-right corner: Click here
    to skip this advertisement...)
3.  arrive to the application page, where Vuze is listed (and also
    'Azureus', the old name for Vuze)
4.  select Vuze there and follow the advice about configuring your
    router.

Typically a forwarding rule for a router contains at least these
elements:

-   The Rule will need a unique Service Name or a Number to identify it.
-   The Rule will need to know what port number to have forwarded to it.
    -   If the option asks for a range, simply input the same number for
        From and To (example: From: 56912 To: 56912).
-   The Rule will need to know which protocol to use for that port. Use
    both TCP and UDP.
    -   Vuze requires the TCP protocol for "regular" incoming data
        transmissions.
    -   Vuze (2.3.0.0 and newer) requires the UDP protocol to be enabled
        for
        [DHT](/web/20210422050047/http://wiki.vuze.com/w/Distributed_hash_table "Distributed hash table")
        to function properly.
        -   If the router does not ask for one protocol or the other, it
            should be safe to assume it defaults to using both.
        -   If the router only allows you to choose one protocol or the
            other, then you will need to create two rules for that port
            (use a different Service Name or Number), one for each
            protocol.
    -   The Rule will need to know which IP address to forward to. You
        will, of course, use the static IP address you have already
        assigned yourself.
-   The Rule will need to be enabled, and then saved/applied.

Example:

<a href="/web/20210422050047/http://wiki.vuze.com/w/File:TypicalPortForwardingSetup.png" class="image"><img src="/web/20210422050047im_/http://wiki.vuze.com/mediawiki/images/e/e4/TypicalPortForwardingSetup.png" width="678" height="469" alt="TypicalPortForwardingSetup.png" /></a>

#### <span id="Port_forwarding_with_two_routers" class="mw-headline">Port forwarding with two routers</span><span class="mw-editsection"><span class="mw-editsection-bracket">\[</span>[edit](/web/20210422050047/http://wiki.vuze.com/mediawiki/index.php?title=NAT_problem&action=edit&section=7 "Edit section: Port forwarding with two routers")<span class="mw-editsection-bracket">\]</span></span>

If you have both a smart NATting modem and a NATting router/basestation,
or two NAT routers, you may need to configure port forwarding in both of
them.

You need to set port forwarding at each router all the way from "public
internet" upto your PC, always **setting the forward to the next device
inwards** (from smart modem to router, and from router to PC). See an
explanation here:
<a href="https://web.archive.org/web/20210422050047/http://www.portforward.com/help/doublerouterportforwarding.htm" class="external free">http://www.portforward.com/help/doublerouterportforwarding.htm</a>

If you have not port forwarded from your modem to your router, it will
be pointless to port forward from the router to your computer as the TCP
traffic from Vuze will never even make it past the modem to the router.

A clear sign of the need for double router port forwarding is if your
router has a private IP address also on its WAN/ADSL/internet side
(whatever it is called in router status/config screens). "Private" IP
address ranges are 10.x.x.x, 172.x.x.x and 192.168.x.x, and IP addresses
inside those areas are different from other addresses, as they can not
be reached from outside without port forwarding.

<a href="/web/20210422050047/http://wiki.vuze.com/w/File:DoubleRouterPortForwarding.png" class="image"><img src="/web/20210422050047im_/http://wiki.vuze.com/mediawiki/images/6/6c/DoubleRouterPortForwarding.png" width="750" height="400" alt="DoubleRouterPortForwarding.png" /></a>

#### <span id="Port_Forwarding_through_Windows_XP_Internet_Connection_Sharing" class="mw-headline">Port Forwarding through Windows XP Internet Connection Sharing</span><span class="mw-editsection"><span class="mw-editsection-bracket">\[</span>[edit](/web/20210422050047/http://wiki.vuze.com/mediawiki/index.php?title=NAT_problem&action=edit&section=8 "Edit section: Port Forwarding through Windows XP Internet Connection Sharing")<span class="mw-editsection-bracket">\]</span></span>

Is your Vuze client running on a computer behind Windows XP ICS? ICS is
a bad excuse for a router in quite a lot of ways but it can be
configured to forward services (read: ports) to other machines in the
local network.

To do it:

-   On the ICS computer, open Control Panel\|Network Connections.
-   Right click on your Internet Connection (eg, Local Area Connection
    X - that accommodates your dial-up/broadband modem connection) and
    click Properties.
-   In the "Local Area Connection X Properties" dialog, go to the
    Advanced tab.
-   Now click the Settings... button in the Internet Connection Sharing
    group.
-   You get the Advanced Settings dialog and a list of services.
-   Click the Add... button to display the Service Settings dialog.
-   For "Description of service:", type in something to remind you that
    this is for Vuze' Distributed DB, eg., Vuze DistDB-T.
-   In the "Name or IP address ..." field, type in the local network
    name of the computer that is running Vuze, eg., livingroom.
-   In the "External Port ..." and "Internal Port ..." fields type in
    the port number you have configured your Vuze to use (the port
    number in Vuze' Tools\|Options\|Connection).
-   Choose TCP (should be default) and click the Ok button and you are
    done. You now have the DistDB-T service in your Advanced Settings
    dialog.
-   You need UDP access to the port as well, so you have to repeat the
    above steps to add a UDP service. Just change the service name (eg.,
    Vuze DistDB-U) and remember to choose UDP instead of TCP this time.

You could follow the "Make sure you really *have* a NAT problem" advice
to check if you've done it right, but, really, the more enjoyable test
is looking in "My Torrents" to see your smileys start to turn green as
soon as you have closed the Advanced Settings dialog.

#### <span id="Port_Forwarding_on_Linux.2C_specifically_Ubuntu" class="mw-headline">Port Forwarding on Linux, specifically Ubuntu</span><span class="mw-editsection"><span class="mw-editsection-bracket">\[</span>[edit](/web/20210422050047/http://wiki.vuze.com/mediawiki/index.php?title=NAT_problem&action=edit&section=9 "Edit section: Port Forwarding on Linux, specifically Ubuntu")<span class="mw-editsection-bracket">\]</span></span>

Firstly the earlier notes on port forwarding for your router apply as
before. Computers running Ubuntu, by default, come with all the ports
locked down and you need to open the ports in ubuntu by using the
iptables command. Other flavours of linux behave similarly

The commands below can be entered in a root terminal session to open the
ports (TCP and UDP)

*iptables -I INPUT -p tcp --dport \<your_port_number> -j ACCEPT  
* *iptables -I INPUT -p udp --dport \<your_port_number> -j ACCEPT*

*\<your_port_number>* is the port number you have used for port
forwarding (Avoid 6881-6999, any from 49125-65535 is fine)

Once you've established the port is open you need to make the change
persist through a reboot; edit file /etc/rc.local and add the lines
below:

<div style="text-align:right; margin-bottom:-37px;">

Copy to Clipboard

</div>

```
sleep 220
/sbin/iptables -I INPUT -p tcp --dport <your_port_number> -j ACCEPT
/sbin/iptables -I INPUT -p udp --dport <your_port_number> -j ACCEPT
```

The *sleep 220* is there to make the script wait a few minutes to allow
subsequent firewall configuration scripts to run. 220 seconds is a large
value and you may choose to configure a lower value. The key is that the
opening of the Vuze port is not countermanded by the firewall
initialisation which runs later.

Your configuration change will now persist through reboots. Further info
on the startup process
<a href="https://web.archive.org/web/20210422050047/https://help.ubuntu.com/community/UbuntuBootupHowto" class="external text">in this ubuntu howto</a>

Futher
<a href="https://web.archive.org/web/20210422050047/http://www.ubuntu.com/support/free" class="external text">Ubuntu Support here</a>

### <span id="VPNs_and_Windows_Routing_and_Remote_Access" class="mw-headline">VPNs and Windows Routing and Remote Access</span><span class="mw-editsection"><span class="mw-editsection-bracket">\[</span>[edit](/web/20210422050047/http://wiki.vuze.com/mediawiki/index.php?title=NAT_problem&action=edit&section=10 "Edit section: VPNs and Windows Routing and Remote Access")<span class="mw-editsection-bracket">\]</span></span>

#### <span id="VPNs" class="mw-headline">VPNs</span><span class="mw-editsection"><span class="mw-editsection-bracket">\[</span>[edit](/web/20210422050047/http://wiki.vuze.com/mediawiki/index.php?title=NAT_problem&action=edit&section=11 "Edit section: VPNs")<span class="mw-editsection-bracket">\]</span></span>

If you are connected to a
<a href="https://web.archive.org/web/20210422050047/http://en.wikipedia.org/wiki/Vpn" class="external text">VPN</a>
(Virtual Private Network) and getting a NAT error when trying to run
Vuze, it is most likely due to all of your internet traffic being routed
through the remote network you are connected to. It is possible to
configure the remote network to allow the traffic through, but given the
added overhead of a VPN, it is better to run Vuze when not connected to
the VPN. Vuze will run better and your downloads will be faster.

If you have no choice and must be connected to a VPN, then you must
contact the network administrator of the remote network you connect to,
and discuss allowing the Vuze port through the VPN to your PC.

**Note:** If you're using Check Point SecuRemote Client, it will give
you NAT problems even when you're NOT connected to any remote networks.

**Note:** If you're using the Cisco Systems VPN Client, you must disable
the Stateful Firewall under Options. (It is disabled if the checkmark
next to Stateful Firewall does not appear.)

To avoid the problems, go to network settings and temporarily disable
it, before starting Vuze. Or, if you have two network adapters, simply
run the VPN client on one, and Vuze on the other.

#### <span id="Windows_Routing_and_Remote_Access" class="mw-headline">Windows Routing and Remote Access</span><span class="mw-editsection"><span class="mw-editsection-bracket">\[</span>[edit](/web/20210422050047/http://wiki.vuze.com/mediawiki/index.php?title=NAT_problem&action=edit&section=12 "Edit section: Windows Routing and Remote Access")<span class="mw-editsection-bracket">\]</span></span>

Microsoft Windows 2000 and XP contain a service for supporting VPNs,
that can cause NAT issues in Vuze if enabled. Even if you don't connect
to a VPN, but this service is enabled, it can cause problems. If you're
sure you don't use VPN connections, then it's safe to assume you don't
need the Routing and Remote Access service enabled.

To disable the Routing and Remote Access service in Windows

1.  Go to the Windows Control Panel (In Windows XP, switch to Classic
    View if not already.)
2.  Open the Administrative Tools
3.  Open Services
4.  Find the Routing and Remote Access service, and double-click it.
5.  If the server status is 'stopped', then it is not running and it is
    not your problem.
6.  If the server status is 'started', then use the stop button to stop
    the service, and see if your NAT problem changes.

If this fixes your NAT problem, and the Routing and Remote Access
Service's startup type is set to Automatic, change it to Manual or
disabled to prevent it from running upon next reboot.

### <span id="Software_Firewalls" class="mw-headline">Software Firewalls</span><span class="mw-editsection"><span class="mw-editsection-bracket">\[</span>[edit](/web/20210422050047/http://wiki.vuze.com/mediawiki/index.php?title=NAT_problem&action=edit&section=13 "Edit section: Software Firewalls")<span class="mw-editsection-bracket">\]</span></span>

*Main article:
[Firewalling](/web/20210422050047/http://wiki.vuze.com/w/Firewalling "Firewalling")*

Just like the wide array of routers available to consumers, so too is
the list of software firewalls, and each has different features and
capabilities. Because of this huge variance, we will again attempt to
approach this as broadly as possible. A software firewall can offer the
same protection that a router can and it can mimic the symptoms of a NAT
error. So why should you use both? A router can only protect you from
incoming data on certain ports - a good software firewall can monitor
outbound traffic too. Consider this an added layer of security.

For those that use a software firewall on their PC, the following
information applies to everyone who hopes to fix their NAT error.

-   You should never have more than one software firewall installed and
    in use at any given time (analogy: two drivers wanting control of a
    steering wheel).
-   In order for Vuze to run correctly, access/permission must be
    allowed.
    -   If your software firewall has options for a security level,
        reduce it from "high" to "medium" if it isn't already there.
    -   If you are using Vuze 2.3.0.4 or older, your software firewall
        must allow "javaw.exe" accesss/permission.
    -   If you are using the current batch of Vuze Betas or a newer
        stable version after it is released, you will need to allow
        "Vuze.exe" instead.

Below is a listing of some of today's common software firewalls guides
that should help. Additional information on how to open your firewall
with some programs and Operating Systems here:
[Firewalling](/web/20210422050047/http://wiki.vuze.com/w/Firewalling "Firewalling")  

-   <span class="small">For XP SP1/SP2 firewall at
    <a href="https://web.archive.org/web/20210422050047/http://support.microsoft.com/default.aspx?scid=kb;en-us;283673" class="external free">http://support.microsoft.com/default.aspx?scid=kb;en-us;283673</a></span>
-   <span class="small">For Microsoft ISA 2004 Firewall
    <a href="https://web.archive.org/web/20210422050047/http://vuze.aelitis.com/wiki/index.php/Router_configuration#Microsoft.27s_ISA_Server_2004" class="external free">http://Vuze.aelitis.com/wiki/index.php/Router_configuration#Microsoft.27s_ISA_Server_2004</a></span>
-   <span class="small">For F-Secure
    <a href="https://web.archive.org/web/20210422050047/http://firewalling.com/personalfirewalls/f-secure/f-secure.htm" class="external free">http://firewalling.com/personalfirewalls/f-secure/f-secure.htm</a></span>
-   <span class="small">For McAfee V6.0 Firewall Plus
    <a href="https://web.archive.org/web/20210422050047/http://firewalling.com/personalfirewalls/McAfeeV6.0FirewallPlus.htm" class="external free">http://firewalling.com/personalfirewalls/McAfeeV6.0FirewallPlus.htm</a></span>
-   <span class="small">For Norton Personal Firewall 2004
    <a href="https://web.archive.org/web/20210422050047/http://firewalling.com/personalfirewalls/nortonpersonalfirewall.htm" class="external free">http://firewalling.com/personalfirewalls/nortonpersonalfirewall.htm</a></span>
-   <span class="small">For Norton Internet Security 2005
    <a href="https://web.archive.org/web/20210422050047/http://firewalling.com/personalfirewalls/nortoninternetsecurity2005.htm" class="external free">http://firewalling.com/personalfirewalls/nortoninternetsecurity2005.htm</a></span>
-   <span class="small">For Sygate Personal Firewall Pro
    <a href="https://web.archive.org/web/20210422050047/http://firewalling.com/personalfirewalls/sygatepersonalfirewallpro.htm" class="external free">http://firewalling.com/personalfirewalls/sygatepersonalfirewallpro.htm</a></span>
-   <span class="small">For ZoneAlarm Pro
    <a href="https://web.archive.org/web/20210422050047/http://firewalling.com/personalfirewalls/ZoneAlarmPro.htm" class="external free">http://firewalling.com/personalfirewalls/ZoneAlarmPro.htm</a></span>
-   <span class="small">Trend Micro PC-cillin Internet Security 2006
    Firewall
    <a href="https://web.archive.org/web/20210422050047/http://kb.trendmicro.com/solutions/search/main/search/solutionDetail.asp?solutionID=26628" class="external free">http://kb.trendmicro.com/solutions/search/main/search/solutionDetail.asp?solutionID=26628</a></span>

Also, confirm whether or not your motherboard is based on the NF4
(nVidia nForce 4 chipset). Many of these new motherboards come with
onboard firewalls that are enabled at the time the drivers are
installed.

### <span id="Anti-virus_Programs" class="mw-headline">Anti-virus Programs</span><span class="mw-editsection"><span class="mw-editsection-bracket">\[</span>[edit](/web/20210422050047/http://wiki.vuze.com/mediawiki/index.php?title=NAT_problem&action=edit&section=14 "Edit section: Anti-virus Programs")<span class="mw-editsection-bracket">\]</span></span>

Some anti-virus programs are extremely sensitive to incoming data and
will report "false positives" when used in conjunction with file sharing
applications (though this is no reason to completely remove your
anti-virus software). Instead, you should use Google and see if other
users have encountered such reports. Other anti-virus programs can at
times contribute to a NAT error. At the time this is being written, only
one stands out, and others will be added if/when they've been confirmed.

1.  Norton AntiVirus 2005 and 2006 employ "internet worm protection" by
    default and should be either disabled or made an exception. Ideally,
    it would be best to make an exception for Vuze' communications.

Open Norton AntiVirus 2005 - Click "Options"-- Click "Internet Worm
Protection"--- Make sure "Enable Internet Worm Protection recommended"
is checked.--- Click "Trojan Rules"---- Uncheck "Unused Windows Services
Block", (all the way at the bottom of the list)----"OK"---"OK"

goto general rules within the internet worm protection,add a new rule,
you need to permit your Incoming TCP Listen
Port(tools-options-connection)

### <span id="Mobile.2F3G.2Fsatellite_connections" class="mw-headline">Mobile/3G/satellite connections</span><span class="mw-editsection"><span class="mw-editsection-bracket">\[</span>[edit](/web/20210422050047/http://wiki.vuze.com/mediawiki/index.php?title=NAT_problem&action=edit&section=15 "Edit section: Mobile/3G/satellite connections")<span class="mw-editsection-bracket">\]</span></span>

Very often the various mobile internet connections, either through
3G/mobile dongles or satellite dishes, have been limited by the ISPs
network architecture to only have private IP addresses.

If your "outermost" device, e.g. the 3G modem, has a private IP address
(10.x.x.x, 172.16-31.x.x and 192.168.x.x) in its config/status screens
as WAN/internet address, then it has been given by ISP's network and
there isn't much you can do. As you have no config access to ISPs
routers, you might have to live with the yellow smileys and the NAT
problem.

-   Note: Vuze NAT test will not find this out, as it will always show
    the first real public IP address it reaches. In the case of mobile
    dongles with private addresses, the shown IP address is probably a
    router somewhere at the ISP.

### <span id="Final_Thoughts" class="mw-headline">Final Thoughts</span><span class="mw-editsection"><span class="mw-editsection-bracket">\[</span>[edit](/web/20210422050047/http://wiki.vuze.com/mediawiki/index.php?title=NAT_problem&action=edit&section=16 "Edit section: Final Thoughts")<span class="mw-editsection-bracket">\]</span></span>

We have seen many Vuze users mistakenly enable or disable an option in
Vuze without knowing what they do. While exploring your client is
encouraged, some of these options may have adverse effects. Two things
of note:

1.  In Options->Connection->Advanced Network Settings, **the "bind to
    local IP address box" should be left empty.** This is **NOT** the
    same thing as the "MAC address binding" or creating a "static IP
    address". This should only be used by experienced users, and those
    that have more than one network adapter in their computer. Be sure
    to press Save after clearing this box if you accidentally used it.
2.  On the other hand - some people have actually reported success by
    enabling this option. You may want to try it as a last resort
    (though if it doesn't solve the problem, then remember to remove
    it).
3.  Oftentimes, users will leave UPnP enabled in Vuze (it is on by
    default.. Tools->Options->Plugins->UPnP), and simply disabling this
    may help clear things up when all the above steps in this guide have
    been taken. Be sure to press Save after disabling UPnP.

## <span id="Conclusion" class="mw-headline">Conclusion</span><span class="mw-editsection"><span class="mw-editsection-bracket">\[</span>[edit](/web/20210422050047/http://wiki.vuze.com/mediawiki/index.php?title=NAT_problem&action=edit&section=17 "Edit section: Conclusion")<span class="mw-editsection-bracket">\]</span></span>

This page's purpose should help the vast majority of those who have
encountered a NAT error while using Vuze with a "typical" setup. There
are other circumstances, though, that require further investigation.
More help sections will be added to this guide in time.

1.  Some computer owners may not realize there are *two* NAT enabled
    devices on their network (modem/router AND router).
2.  Some users may not have a routing device at all, but instead, are
    using ICS (Internet Connection Sharing) and not properly port
    mapping to other machines.

### <span id="STILL_Not_Working.3F" class="mw-headline">STILL Not Working?</span><span class="mw-editsection"><span class="mw-editsection-bracket">\[</span>[edit](/web/20210422050047/http://wiki.vuze.com/mediawiki/index.php?title=NAT_problem&action=edit&section=18 "Edit section: STILL Not Working?")<span class="mw-editsection-bracket">\]</span></span>

Come to the
<a href="https://web.archive.org/web/20210422050047/http://forum.vuze.com/forum.jspa?forumID=102" class="external text">Vuze forums</a>
and ask for assistance there. Be patient. Be prepared to answer these
questions:

-   What is your Operating System?
-   What is your Java Version?
-   What is the *exact* make/model/revision is your router? (if you use
    one)
-   Does the router employ UPnP and MAC binding?
-   What is the *exact* make/model/revision of your broadband modem?
-   What software firewall(s) do you use?
-   What anti-virus program do you use?
-   Which (if any) of the above steps have you already attempted and
    with what level of success?

  
**Special case: Only private IP addresses**

If your ISP is using NAT itself, it may be impossible to get the
NAT/Firewall test to work because it is being cut off at your ISP. Some
ISPs (especially mobile/cellular/3G service providers) use
<a href="https://web.archive.org/web/20210422050047/http://wiki.vuze.com/" class="extiw" title="wikipedia:carrier grade NAT">carrier grade NAT</a>,
meaning they only give users private IP address from those private
ranges and then users are most likely doomed to live with yellow faces.
(Note: Vuze NAT test will not find this out, as it will always show the
first real public IP address it reaches.) If your "outermost" device has
a private IP address (10.x.x.x, 172.x.x.x and 192.168.x.x) in its
config/status screens as its outer WAN/internet address, then it has
been given by ISP's network and there isn't much you can do.

<span class="small">Read the
<a href="/web/20210422050047/http://wiki.vuze.com/mediawiki/index.php?title=Vuze_FAQ&amp;action=edit&amp;redlink=1" class="new" title="Vuze FAQ (page does not exist)">Vuze FAQ</a></span>

</div>

</div>

<div class="printfooter">

Retrieved from
"[http://wiki.vuze.com/mediawiki/index.php?title=NAT_problem&oldid=15797](https://web.archive.org/web/20210422050047/http://wiki.vuze.com/mediawiki/index.php?title=NAT_problem&oldid=15797)"

</div>

<div id="catlinks" class="catlinks" mw="interface">

<div id="mw-normal-catlinks" class="mw-normal-catlinks">

[Categories](/web/20210422050047/http://wiki.vuze.com/w/Special:Categories "Special:Categories"):

-   [NAT and
    firewalling](/web/20210422050047/http://wiki.vuze.com/w/Category:NAT_and_firewalling "Category:NAT and firewalling")
-   [Documentation](/web/20210422050047/http://wiki.vuze.com/w/Category:Documentation "Category:Documentation")
-   [Troubleshooting](/web/20210422050047/http://wiki.vuze.com/w/Category:Troubleshooting "Category:Troubleshooting")

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
    id="pt-anontalk">[Talk](/web/20210422050047/http://wiki.vuze.com/w/Special:MyTalk "Discussion about edits from this IP address [n]")</span>
-   <span
    id="pt-anoncontribs">[Contributions](/web/20210422050047/http://wiki.vuze.com/w/Special:MyContributions "A list of edits made from this IP address [y]")</span>
-   <span id="pt-createaccount">[Create
    account](/web/20210422050047/http://wiki.vuze.com/mediawiki/index.php?title=Special:CreateAccount&returnto=NAT+problem "You are encouraged to create an account and log in; however, it is not mandatory")</span>
-   <span id="pt-login">[Log
    in](/web/20210422050047/http://wiki.vuze.com/mediawiki/index.php?title=Special:UserLogin&returnto=NAT+problem "You are encouraged to log in; however, it is not mandatory [o]")</span>

</div>

<div id="left-navigation">

<div id="p-namespaces" class="vectorTabs" role="navigation"
aria-labelledby="p-namespaces-label">

### Namespaces

-   <span
    id="ca-nstab-main">[Page](/web/20210422050047/http://wiki.vuze.com/w/NAT_problem "View the content page [c]")</span>
-   <span
    id="ca-talk">[Discussion](/web/20210422050047/http://wiki.vuze.com/w/Talk:NAT_problem "Discussion about the content page [t]")</span>

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
    id="ca-view">[Read](/web/20210422050047/http://wiki.vuze.com/w/NAT_problem)</span>
-   <span
    id="ca-edit">[Edit](/web/20210422050047/http://wiki.vuze.com/mediawiki/index.php?title=NAT_problem&action=edit "Edit this page [e]")</span>
-   <span id="ca-history">[View
    history](/web/20210422050047/http://wiki.vuze.com/mediawiki/index.php?title=NAT_problem&action=history "Past revisions of this page [h]")</span>

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

<a href="/web/20210422050047/http://wiki.vuze.com/w/Main_Page" class="mw-wiki-logo" title="Visit the main page"></a>

</div>

<div id="p-" class="portal" role="navigation"
aria-labelledby="p--label">

### 

<div class="body">

-   <span id="n-Download-Vuze-Now">[Download Vuze
    Now](https://web.archive.org/web/20210422050047/http://www.vuze.com/download)</span>

</div>

</div>

<div id="p-navigation" class="portal" role="navigation"
aria-labelledby="p-navigation-label">

### Navigation

<div class="body">

-   <span id="n-mainpage-description">[Main
    page](/web/20210422050047/http://wiki.vuze.com/w/Main_Page "Visit the main page [z]")</span>
-   <span id="n-recentchanges">[Recent
    changes](/web/20210422050047/http://wiki.vuze.com/w/Special:RecentChanges "A list of recent changes in the wiki [r]")</span>
-   <span id="n-randompage">[Random
    page](/web/20210422050047/http://wiki.vuze.com/w/Special:Random "Load a random page [x]")</span>
-   <span
    id="n-help">[Help](https://web.archive.org/web/20210422050047/https://www.mediawiki.org/wiki/Special:MyLanguage/Help:Contents "The place to find out")</span>

</div>

</div>

<div id="p-tb" class="portal" role="navigation"
aria-labelledby="p-tb-label">

### Tools

<div class="body">

-   <span id="t-whatlinkshere">[What links
    here](/web/20210422050047/http://wiki.vuze.com/w/Special:WhatLinksHere/NAT_problem "A list of all wiki pages that link here [j]")</span>
-   <span id="t-recentchangeslinked">[Related
    changes](/web/20210422050047/http://wiki.vuze.com/w/Special:RecentChangesLinked/NAT_problem "Recent changes in pages linked from this page [k]")</span>
-   <span id="t-specialpages">[Special
    pages](/web/20210422050047/http://wiki.vuze.com/w/Special:SpecialPages "A list of all special pages [q]")</span>
-   <span id="t-print">[Printable
    version](/web/20210422050047/http://wiki.vuze.com/mediawiki/index.php?title=NAT_problem&printable=yes "Printable version of this page [p]")</span>
-   <span id="t-permalink">[Permanent
    link](/web/20210422050047/http://wiki.vuze.com/mediawiki/index.php?title=NAT_problem&oldid=15797 "Permanent link to this revision of the page")</span>
-   <span id="t-info">[Page
    information](/web/20210422050047/http://wiki.vuze.com/mediawiki/index.php?title=NAT_problem&action=info "More information about this page")</span>

</div>

</div>

</div>

</div>

<div id="footer" role="contentinfo">

-   <span id="footer-info-lastmod">This page was last modified on 26
    February 2014, at 19:14.</span>
-   <span id="footer-info-viewcount">This page has been accessed 616,258
    times.</span>

<!-- -->

-   <span id="footer-places-about">[About
    VuzeWiki](/web/20210422050047/http://wiki.vuze.com/w/VuzeWiki:About "VuzeWiki:About")</span>
-   <span
    id="footer-places-mobileview"><a href="https://web.archive.org/web/20210422050047/http://wiki.vuze.com/mediawiki/index.php?title=NAT_problem&amp;mobileaction=toggle_view_mobile" class="noprint stopMobileRedirectToggle">Mobile view</a></span>

<!-- -->

-   <span
    id="footer-poweredbyico">[<img src="/web/20210422050047im_/http://wiki.vuze.com/mediawiki/resources/assets/poweredby_mediawiki_88x31.png" srcset="/web/20210422050047im_/http://wiki.vuze.com/mediawiki/resources/assets/poweredby_mediawiki_132x47.png 1.5x, /web/20210422050047im_/http://wiki.vuze.com/mediawiki/resources/assets/poweredby_mediawiki_176x62.png 2x" width="88" height="31" alt="Powered by MediaWiki" />](//web.archive.org/web/20210422050047/http://www.mediawiki.org/)</span>
-   <span id="footer-analyticsystemsico">Any use of Vuze® and Vuze+™
    that violates the rights of any person or entity is not allowed.
    [More](https://web.archive.org/web/20210422050047/http://vuze.com/corp/legal.php)</span>

<div style="clear:both">

</div>

</div>
