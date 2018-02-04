---
title: Rebuilding Systems from Scratch — a Retrospective
tags: [career, mistake, windows, automation, scripting, sysadmin]
---

In 2017, I started a new job in a different corner of the IT universe than any that I had previously visited. Previously, I had done web development, software testing, "systems engineering," and a few assorted odds-and-ends. Now, I found myself doing systems administration work.

Along with another sysadin (we'll call him "J"), we were tasked with reinstalling and revamping a piece of software which the team was using for Windows client automation called Symantec ITMS. The basic goal was to assuage our senior sysadmin's (we'll call him "E") doubts about the product's configuration (which had grown *very* organically for years, without much direction) by completely rebuilding it from the ground up.

#Introducing the Software

ITMS provides a number of configuration management features, which we needed to (and did) preserve in the new installation. Generally, these features fall into a few categories: gathering of inventory from managed computers (via an agent), automatic detection and remediation of managed software packages, and deployment (i.e., OS install, post-install config) of endpoint systems.

#Understanding the Current Installation

During the planning phase, and during much of our rebuild, the old server was still up and running and we were able to use it as a model. Based on our own observations, plus the information which E shared with us, we began to identify features which we liked as well as features which we wanted to change or remove.

##The Good

* All of the important software packages were already being distributed by software policies, which combined the software itself with logic for installing it and for detecting whether it was already installed.
* A number of useful "tasks" were available which admins could run at will, and which provided effects such as bypassing smart card enforcement and cleaning the Windows Update cache.
* Instructions had been provided which allowed people to get "up to speed" with providing Windows packages.
* The deployment workflow was capable of handling many of the steps which would otherwise need to be done manually in order to install a Windows laptop or desktop.

##The Bad

* The software deployment itself was lacking in that it was housed on an out-of-warranty physical server with no consideration of availability or optimal resource utilization.
* Only one level of access was provided, which retained full control over all features rather than finer-grained control based on realistic needs.
* Numerous manual steps still needed to be done in order to deploy a Windows system, even with the help being provided by the deployment workflow.
* The software policies and associated resources were inconsistently named, were targeted in inconsistent ways, and were all duplicated for production and testing policies.
* Actual policies, filters, tasks, and so on had been scattered throughout their builtin ITMS-provided counterparts, which yielded a disorganized feel.

#
