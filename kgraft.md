---
title: kGraft Live Patching for SLES12
category: Live-Patching
layout: 2017/sheet
tags: [Featured]
updated: 2021-01-06
keywords:
- live Patching
- SLES SAP
- kgraft
- kgr
---
{: .-three-column}

### kgr Tool - query and manipulate kGraft patching status
Display the overall status of kGraft patching (ready or in_progress)
```bash
$ kgr status
## Example output
ready
```
Display the list of loaded kGraft patches
```bash
$ kgr -v patches
## Example Output
kgraft_patch_1_8_5_1
    active: 1
    RPM: kgraft-patch-4_12_14-122_46-default-1-8.5.1.x86_64
    CVE: (none - this is an initial kGraft patch)
    bug fixes and enhancements: (none)
```

List processes that are preventing kGraft patching from finishing. 
By default, only the PIDs are listed
```bash
$ kgr -v blocking
## Example Output
no processes with kgr_in_progress set
```

Show man page
```bash
$ man kgr
```

### How Does kGraft Work?
![](images/kgraft1.png)


### Documentation
{: .-intro}
SUSE Documentation
- [Live Kernel Patching Using kGraft](https://documentation.suse.com/sles/12-SP5/html/SLES-kgraft/index.html) _(suse.com)_
- [Reboot Reloaded: Patching the Linux Kernel Online](https://www.suse.com/c/reboot-reloaded-patching-the-linux-kernel-online/) _(suse.com)_
- [Live Patching Presentation](https://www.suse.com/media/presentation/slelp.pdf) _(suse.com)_
- [Live Patching Data Sheet](https://www.suse.com/media/data-sheet/sle_live_patching_data_sheet.pdf) _(suse.com)_