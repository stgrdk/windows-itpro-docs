---
title: Audit directory service access (Windows 10)
description: Determines whether to audit the event of a user accessing an Active Directory object that has its own system access control list (SACL) specified.
ms.assetid: 52F02EED-3CFE-4307-8D06-CF1E27693D09
ms.prod: W10
ms.mktglfcycl: deploy
ms.sitesec: library
author: brianlic-msft
---

# Audit directory service access


**Applies to**

-   Windows 10

\[Some information relates to pre-released product which may be substantially modified before it's commercially released. Microsoft makes no warranties, express or implied, with respect to the information provided here. An app that calls an API introduced in Windows 10 Anniversary SDK Preview Build 14295 cannot be ingested into the Windows Store during the Preview period.\]

Determines whether to audit the event of a user accessing an Active Directory object that has its own system access control list (SACL) specified.

By default, this value is set to no auditing in the Default Domain Controller Group Policy object (GPO), and it remains undefined for workstations and servers where it has no meaning.

If you define this policy setting, you can specify whether to audit successes, audit failures, or not audit the event type at all. Success audits generate an audit entry when a user successfully accesses an Active Directory object that has a SACL specified. Failure audits generate an audit entry when a user unsuccessfully attempts to access an Active Directory object that has a SACL specified. To set this value to **No auditing,** in the **Properties** dialog box for this policy setting, select the **Define these policy settings** check box and clear the **Success** and **Failure** check boxes.

**Note**  
You can set a SACL on an Active Directory object by using the **Security** tab in that object's **Properties** dialog box. This is the same as Audit object access, except that it applies only to Active Directory objects and not to file system and registry objects.

 

**Default:**

-   Success on domain controllers.

-   Undefined for a member server.

## Configure this audit setting


You can configure this security setting under Computer Configuration\\Windows Settings\\Security Settings\\Local Policies\\Audit Policy.

There is only one directory service access event, which is identical to the Object Access security event message 566.

| Directory service access events | Description                            |
|---------------------------------|----------------------------------------|
| 566                             | A generic object operation took place. |

 

## Related topics


[Basic security audit policy settings](basic-security-audit-policy-settings.md)

 

 




