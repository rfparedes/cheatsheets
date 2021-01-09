---
title: KLP (Kernel Live Patching) for SLES15
category: Live-Patching
layout: 2017/sheet
tags: [WIP, Featured]
updated: 2021-01-08
keywords:
- live Patching
- SLES SAP
- klp
- kernel live patching
---
{: .-two-column}
### Documentation
{: .-intro}
SUSE Documentation
- [Live Kernel Patching with KLP](https://documentation.suse.com/sles/15-SP2/single-html/SLES-admin/#cha-klp) _(suse.com)_

### klp Tool - Query kernel live patching status
Display the overall status of Kernel Live Patching (ready or in_progress)
```bash
$ klp status
## Example Output
ready
```
Display the list of loaded KLP patches
```bash
$ klp -v patches
## Example Output
livepatch_1_5_3_2
    active: 1
    RPM: kernel-livepatch-5_3_18-24_34-default-1-5.3.2.x86_64
    CVE: (none - this is an initial kernel live patch)
    bug fixes and enhancements: (none)
```
List processes that are preventing KLP from finishing. 
By default, only the PIDs are listed
```bash
$ klp -v blocking
## Example Output
no threads with klp_in_progress set
```
Show man page
```bash
$ man klp
```