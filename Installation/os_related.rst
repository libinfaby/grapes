OS Installation and Configuration
+++++++++++++++++++++++++++++++++


OS on Server Machine
====================
**Windows Server 2019 or above** should be mandatorily installed in the server due to scalability and performance reasons. Regular Windows OS has a limit on SQL concurrent connections for file & printer and the limit appears to be 20. Windows Server adjusts the maximum number of user connections automatically as needed up to the maximum value allowable.

.. warning:: Hence, installing Server OS on the server machine is mandatory.

`Download Windows Server 2022 <https://www.microsoft.com/en-us/evalcenter/download-windows-server-2022>`_ 

`Download Windows Server 2019 <https://www.microsoft.com/en-us/evalcenter/evaluate-windows-server-2019>`_


OS on Client Machines
=====================
Windows 10 Ultimate (a bootable USB drive if possible)


Drivers
=======
* Latest Driver Pack (Version: 16 or 17 recommended)
* Check if all device drivers are installed and configured, especially the network drivers


Drive Partitions
================
Minimum 2 drive partitions are mandatory. C partition should have a minimum capacity of 200GB. The other partition should have a minimum capacity of 300GB - 400GB of space

.. note:: This should be done because if in any case, the server needs to be formatted, the Grapes files and databases will remain safe in the other partition.

`Click here to know how to create a new partition <https://support.microsoft.com/en-us/windows/create-and-format-a-hard-disk-partition-bbb8e185-1bda-ecd1-3465-c9728f7d7d2e>`_


Server Name
===========
Change the Server computer name to ``GRAPESSERVER``. This name is suggested as part of standardization. This should be done only if the server is not being used for any other purpose and have exclusively been given for Grapes installation.


Administrator User
==================
Enable 'Administrator' user with password protection. Ensure that you're always logging in to the 'Administrator' user


Windows Update
==============
**Turn off automatic windows updates**. Windows updates might modify/delete certain system files which are required by Grapes softwares. Turning off automatic updates will prevent this.

#. Go to Control Panel > Administrative Tools > Services
#. Scroll down to Windows Update in the resulting list
#. Double click the Windows Update Entry
#. In the resulting dialog, if the service is started, click ``Stop``
#. Set Startup Type to ``Disabled``


IP Address
==========
Disable IPv6 & assign IPv4 address like ``xxx.xxx.x.251`` as part of standardization (e.g. *192.168.1.251* or *192.168.0.251*)

`Click here to know how to disable IPv6 <https://support.nordvpn.com/hc/en-us/articles/19919186892305-How-to-disable-IPv6-on-Windows>`_

`Click here to know how to assign IPv4 <https://learn.microsoft.com/en-us/troubleshoot/windows-server/networking/change-ip-address-network-adapter>`_


Firewall 
========
Turn off Firewall

.. caution:: Must turn on Firewall after installation


`How to turn Firewall on/off <https://support.microsoft.com/en-us/windows/turn-microsoft-defender-firewall-on-or-off-ec0844f7-aebd-0583-67fe-601ecf5d774f>`_


Date, Time and Regional Settings
================================
* Change Time Zone to ``(UTC+05:30) Chennai, Kolkata, Mumbai, New Delhi``
* Change time format to ``dd-MMM-yyyy``
* Set First day of week as ``Sunday``
* Short Time as ``hh:mm tt``
* Long Time as ``hh:mm:ss tt``

Change Date, Time and Regional Settings in **Control Panel > Clock and Region > (Additional Settings)**