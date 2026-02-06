---
title: "Example Items"
chapter: false
menuTitle: "IV: Example Items"
weight: 50
---
---
It is inevitable that when discussing technology, we will need to use examples. Both in configurations of various components within the technology, as well as when describing concepts and how they interact with the rest the proposed environment.

Whenever possible, we should use examples that reflect what the lab environment will reflect. This can sometimes bring confusion, if trying to explain something specifically outside the scope of the lab. When that is the case, the following should be relied upon as generic names for objects in documentation.

## Domains

When documentation requires fully qualified domain names, use example.com and example.net. These are special use domain names registered for the express purpose of documentation.

## Host names

Host names should be generic, capture the meaning of the device, and deviate from actual host names leveraged in the lab when not referencing the lab.

## IPv4 addresses

Use addresses from and RFC1918 space that is in a separate class from the lab space you are working in. For example, if leveraging 172.16.0.0/16 in the lab environment, use 10.0.0.0/8 or 192.168.0.0/16 space when showing examples outside the lab environment.

## IPv6 addresses

IPv6 has a dedicated prefix to use in documentation efforts. This is the `2001:0DB8::/32` prefix. Use this whenever documentation requires non-specific IPv6 addressing.

## Users

For example users, use free-software mascots, such as Tux (Linux Kernel), Wilber (The GIMP), Geeko (SUSE), Foxkeh (Firefox), Konqi (KDE), or Duke (Java).
