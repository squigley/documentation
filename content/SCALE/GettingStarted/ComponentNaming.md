---
title: "Component Naming"
weight: 60
---

{{< toc >}}

TreuNAS SCALE incorporates all the major TrueNAS CORE storage and sharing features with a web interface based on Debian GNU/Linux.  Because SCALE shares the same UI as the FreeBSD-based TrueNAS CORE, users will notice there are similarities. However, SCALE does incorporate some differences, primarily in component naming.

## Disks

TrueNAS Core utilizes a numerical listing of drives in a system.

![ComponentNamingDrivesCore](/images/SCALE/ComponentNamingDrivesCore.png "TrueNAS Core Drive Listing")

TrueNAS SCALE uses a lettered format for drive identification.  

![ComponentNamingDrivesSCALE](/images/SCALE/ComponentNamingDrivesSCALE.png "TrueNAS SCALE Drive Listing")

{{< hint info >}}
 
SCALE still labels NVMe drives with a numeric value.
{{< /hint >}}

## Interfaces

TrueNAS CORE utilizes driver information and enumeration to assign an interface name.

![ComponentNamingInterfacesCore](/images/SCALE/ComponentNamingInterfacesCore.png "TrueNAS CORE Interface Listing")

TrueNAS SCALE uses PCI location to assign an interface name.

![ComponentNamingInterfacesSCALE](/images/SCALE/ComponentNamingInterfacesSCALE.png "TrueNAS SCALE Interface Listing")
