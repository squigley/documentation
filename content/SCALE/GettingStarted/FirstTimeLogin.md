---
title: "First Time Login"
weight: 14
---

Now that you have installed and configured TrueNAS SCALE, you can log in to the web interface and begin managing data!

{{< expand "Can I configure TrueNAS SCALE using a CLI?" "v" >}}
After installing TrueNAS, you can configure and use the system through the web interface.

{{< hint warning >}}
**Important:** Use only the web interface to make configuration changes to the system.
{{< /hint >}}

By default, using the command-line interface (CLI) to modify the system **does not modify the settings database**.
The system reverts to the original database settings when it restarts and wipes any user-made command line changes.
TrueNAS automatically creates a number of ways to access the web interface, but you might need to adjust the default settings to better fit the system in your network environment.
{{< /expand >}}

## Web Interface Access

By default, fresh installs of TrueNAS SCALE provide a default address for logging in to the web interface.
To view the web interface IP address or reconfigure web interface access, connect a monitor and keyboard to your TrueNAS system or connect with IPMI for out-of-band system management.

When powering on a TrueNAS system, the system attempts to connect to a DHCP server from all live interfaces and provide access to the web interface.
On networks that support Multicast Domain Name Services (mDNS), the system can use a hostname and domain to access the TrueNAS web interface.
By default, TrueNAS uses the hostname and domain *truenas.local*.
To change the hostname and domain in the web interface, go to **Network** and click *Settings* in the *Global Configuration* window.

To access the web interface using an IP address, use the one that the Console Setup Menu generated after installing SCALE, or use the one you configured in the [Post-install Configuration article]({{< relref "Post-installConfiguration.md" >}}) if you upgraded from CORE.

We recommend a strong login password!
You can reset the root password in the TrueNAS console setup menu or in the web interface by going to **Credentials > Local Users** and editing the `root` user.

## Logging In

On a computer that can access the same network as the TrueNAS system, enter the hostname and domain or IP address in a web browser to connect to the web interface.

![LoginSCALE](/images/SCALE/LoginSCALE.png "TrueNAS SCALE Login Screen")

Enter the `root` username and account password that you created during installation.

{{< expand "Troubleshooting" "v" >}}
If the user interface is not accessible by IP address from a browser, check these things:

* If the browser configuration has proxy settings enabled, disable them and try connecting again.
* If the page does not load, make sure that a `ping` reaches the TrueNAS system IP address. If the IP address is in a private range, you must access it from within that private network.

If the web interface displays but seems unresponsive or incomplete:

* Make sure the browser allows cookies, Javascript, and custom fonts from the TrueNAS system.
* Try a different browser. We recommend Firefox.

If the UI becomes unresponsive after an upgrade or other system operation, clear the site data and refresh the browser (<kbd>Shift</kbd>+<kbd>F5</kbd>).
{{< /expand >}}

## Dashboard

After logging in, you will see the system **Dashboard**.
The dashboard displays basic information about the installed version, systems component usage, and network traffic. For users with compatible TrueNAS
Hardware, clicking the system image will take you to the **System Settings > Enclosure** page. 

![DashboardSCALE](/images/SCALE/DashboardSCALE.png "TrueNAS SCALE Dashboard")

The **Dashboard** provides access to all TrueNAS management options.
The top row has links to outside resources and buttons to control the system.
The left-hand column lets users navigate to the various TrueNAS Configuration screens.

Users can select which widgets appear on the dashboard by clicking *Configure*.

![ConfigureWidgetsSCALE](/images/SCALE/ConfigureWidgetsSCALE.png "Dashboard Configuration")

Buttons in the top row link to iXsystems sites, outside resources, and buttons to control the system.

![TopRowSCALE](/images/SCALE/TopRowSCALE.png "TrueNAS SCALE Dashboard Top Row Icons")

The button next to the iXsystems logo shows [TrueCommand](https://www.truenas.com/truecommand/) connection options.
The next two buttons show information about system processes, like active or previous tasks and any alerts generated by a system condition.
The remaining buttons link to system configuration option or can be used to log out, restart, or shut down the physical system.

### Task Manager

The Task Manager displays all running and failed jobs/processes. 

![TaskManagerSCALE](/images/SCALE/TaskManagerSCALE.png "TrueNAS SCALE Task Manager")

Users can click the *History* button to open the **Jobs** screen. **Jobs** lists all *Successful*, *Active*, and *Failed* jobs. Users can also click *View Logs* next to a failed process to view its log information and its error message.

![TaskManagerHistorySCALE](/images/SCALE/TaskManagerHistorySCALE.png "Task Manager History")

## Storing Data

Now that you can access the TrueNAS web interface and see all the management options, it's time to begin [storing data]({{< relref "/SCALE/Storage/_index.md" >}})!
