---
title: Erker's Review of the Windows 10 install document
tags: [gfdl, win10]
---

This follows Erker's first read through the Win10 install documentation
available [here](https://sites.google.com/a/noaa.gov/oar-gfdl-syswiki/windows-documentation/it-management-suite/deploy-win10).

Automation changes
==================

These are comments which will likely require additional or changed automation
jobs / tasks:

* SMART reporting should be turned on at some point (by admin or script). Some
  of the newer devices apparently ship with it turned *off*.

* Indicate when, exactly, the auto-provisioning is finished. It is difficult
  to tell and very tempting to log into the system before the deployment is
  finished.

* Go into AD CAC zone immediately during deployment, rather than stopping
  through the No-CAC.

* Move System Restore setting (12%, 17%) to a script.

* Disk Cleanup after the entire installation. Otherwise, lots of Windows
  Update pieces will be left over.

Major documentation rework
==========================

These are comments which will probably require rework or rearrangement of the
existing documentation:

* Move computer to No-CAC zone: why is this necessary? And how do I do this if
  there is no computer yet in existence?

* Ensure that the BIOS is upgraded before proceeding with the setup.

* The BIOS settings steps should be written to be a comprehensive explanation
  of how to configure a new computer for Windows 10, not just a delta from a
  properly-configured-for-Windows-7 machine. (e.g., should include steps about
  USB PowerShare, setting the BIOS password).

* Include a demonstration of the Software Portal here, plus add the link.
  Indeed, much of the latter portion of work should be demonstrating the new
  features of Windows 10 to users: SSH, Software Portal, MS Office 2016,
  Microsoft Store apps, Edge features (?), IE11, and so on.

Minor documentation rework
==========================

These are relatively small nitpicks which should be easy to fix in the current
documentation:

* Remove all references to Windows 7. In several months, the move from Win7 to
  Win10 will be irrelevant, and all that will remain is the fact that we are
  installing Win10 machines.

* Don't worry too much about adding pictures for the BIOS setup.

* Windows 200% scaling -- adjust down to something more reasonable.

Enhancements
============

These are comments which Erker specifically stated are low-priority or
nice-to-haves, rather than hard requirements for Monday.

* Find additional knobs / features to tweak / add in the unattend.xml rather
  than depending as much on (e.g.) PowerShell scripts

* For OpenSSH client, try to include the "optional feature" during provisioning
  or, even better, in the unattend.xml. This would require reaching out to
  MS / Windows Update rather than WSUS, which does not recognize the availability

* Use keyboard-based Start Menu invocation when possible. For example, type
  "Activation" in Windows 10 rather than navigating through the menus.
