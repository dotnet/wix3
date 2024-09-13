---
title: Using WiX Standard Bootstrapper Application Variables
layout: documentation
after: wixstdba_customize
---
# Using WiX Standard Bootstrapper Application Variables

The WiX Standard Bootstrapper Application offers a set of variables:

* WixBundleFileVersion - gets the file version of the bundle .exe.
* WixStdBALanguageId - gets the language in effect for the WixStdBA user interface.
* RemoveUpgradeRelatedBundle - this variable can be set by a bundle to control the behavior of upgrade-related bundles. Three values are supported:
    * *always* - default, upgrade-related bundles are removed synchronously.
    * *never* - upgrade-related bundles are not removed.
    * *nextSession* - upgrade-related bundles are removed after the next reboot.  WixStdBA will write to the RunOnce registry key, deferring the removal until the next login session.
  
  Because the variable can be set by the bundle, registry searches or public properties passed on the commandline can be used, allowing users to configure upgrade behavior.


