---
layout: post
title:  "Update your windows apps with yum like a utility in windows"
author: Aman
categories: [News,Tutorial]
image: assets/images/winget/winget-cover.svg
comments: true
---

Winget is s a windows package manager that's bundled with modern windows ( such as windows 11). It lets you manage your windows application in the command line.

![]({{ site.baseurl}}/assets/images/winget/winget.png)

It allows us perform various actions such as installing, removing, upgrading apps and much more. 

![]({{ site.baseurl}}/assets/images/winget/winget-upgrade.png)

Here we will be upgrading the apps present in my system. 

```bash
winget upgrade
```

This command to show us the list of available updates and then use the --all parameter to upgrade all apps.

![]({{ site.baseurl}}/assets/images/winget/winget-upgrade-2.png)

*More information regarding the utility can be found [here](https://learn.microsoft.com/en-us/windows/package-manager/). This will help you get familiar with the fairly easy to use utility.*