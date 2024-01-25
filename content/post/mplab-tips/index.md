---
title: MPLAB
subtitle: Tips and problems resolution.

# Summary for listings and search engines
summary: Tips and problems resolution using Microchip MPLAB IDE software.

# Link this post with a project
projects: []

# Date published
date:  '2024-01-25T18:42:51.000-03:00'

# Date updated
#lastmod: '2020-12-13T00:00:00Z'

# Is this an unpublished draft?
draft: false

# Show this page in the Featured widget?
featured: yes

# Featured image
# Place an image named `featured.jpg/png` in this page's folder and customize its options here.
image:
  caption: 'Image credit: [**Unsplash**](https://unsplash.com/photos/CpkOjOcXdUY)'
  focal_point: ''
  placement: 2
  preview_only: false

authors:
  - admin 

tags:
  - soft
  - MPLAB

categories:
  - Software 

share: true
---
 

## Problem: Unrecognized VM option 'UseConcMarkSweepGC'
 > Found in v6.15

Program doen't start, showin the following message:
```bash
Unrecognized VM option 'UseConcMarkSweepGC'
Error: Could not create the Java Virtual Machine.
Error: A fatal exception has occurred. Program will exit.
```

#### Solution
Force a previous java version. You may use the java version included with MPLAB with the `--jdkhome`option. Example
```bash
mplab_ide --jdkhome /usr/local/microchip/mplabx/v6.15/sys/java/zulu8.64.0.19-ca-fx-jre8.0.345-linux_x64
```

Add this command to your `MPLAB.desktop` file.

[Comment](https://x.com/budinero_/status/1750646477095940453?s=20)