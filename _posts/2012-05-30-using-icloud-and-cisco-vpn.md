---

date: 2012-05-30 20:36:42+00:00
layout: post
title: Using iCloud and Cisco VPN
tags:
- cisco anyconnect icloud vpn
---

[UBC uses Cisco](http://www.it.ubc.ca/service-catalogue/internet-and-telephone/network-management/myvpn/setup-documents/myvpn-setup-mac-os)'s VPN solution for accessing the network off-campus [1]. For a long time I skipped using it because 1) it conflicted with iCloud and 2) it required a constantly active app icon in the Dock. Well, 1) is partially resolved, so I can again use it, begrudgingly.

The problem was that if you had iCloud active (using the preference pane), when the Cisco "myVPN" client started it would not find the VPN server. It turns out that this is due to only two iCloud services, Back to My Mac and Find My Mac, which you can disable. Once those are unchecked (see image), the Cisco client should be able to detect the server and get online.

[![Image](http://fink08.files.wordpress.com/2012/05/screen-shot-2012-05-30-at-13-24-50.png?w=487)](http://fink08.files.wordpress.com/2012/05/screen-shot-2012-05-30-at-13-24-50.png)

Since I only use iCloud for data and calendaring right now, this is acceptable, although I suppose losing my laptop might make me change my mind. You can check out this [Apple support discussion](https://discussions.apple.com/thread/3633238?start=0&tstart=0) for more lurid details.

1. Actually, you need to VPN if you are accessing printers or local directories on-campus as well.
