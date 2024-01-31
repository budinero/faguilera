---
# Documentation: https://hugoblox.com/docs/managing-content/

title: "MATLAB Notes"
subtitle: "Notes on tips and problems resolution."
summary: "Notes on tips and problems resolution for MATLAB software"
authors: 
  - admin 
tags: 
  - soft
  - MATLAB
  - Tips
  - Linux
categories: 
  - Software
date: 2024-01-31T09:29:22-03:00
lastmod: 2024-01-31T09:29:22-03:00
featured: false
draft: false

# Featured image
# To use, add an image named `featured.jpg/png` to your page's folder.
# Focal points: Smart, Center, TopLeft, Top, TopRight, Left, Right, BottomLeft, Bottom, BottomRight.
image:
  caption: ""
  focal_point: ""
  preview_only: false

# Projects (optional).
#   Associate this post with one or more of your projects.
#   Simply enter your project's folder or file name without extension.
#   E.g. `projects = ["internal-project"]` references `content/project/deep-learning/index.md`.
#   Otherwise, set `projects = []`.
projects: []
share: true
---

# Installing MATLAB 2022a/2023a on linux

> Tested with _Debian 12 (Bookworm)_ GNU/Linux
 
## Install

#### Error:
```bash
what():  Failed to launch web window with error: Unable to launch the MATLABWindow application. The exit code was: 127
```

#### Solution:

```bash
cd (extracted_iso_path)/bin/glnxa64
mkdir exclude
mv libfreetype.so* exclude/
```

## After install, load plot error
#### Error:
```bash
`com.jogamp.opengl.GLException: X11GLXDrawableFactory`
```

#### Solution:
```
nano (intall_dir)/bin/glnxa64/java.opts
```
Paste `-Djogl.disable.openglarbcontext=1` inside the text file.

## After install, Simulink error
#### Error
```bash
Failed to load bundle #429: .../R2022a/bin/glnxa64/libmwsl_graphical_classes.so
```

#### Solution:
```bash
cd (install_dir)/bin/glnxa64
mkdir exclude 
mv libfreetype.so.6* exclude/
```

## Does not respect default folder settings

#### Problem
Default folder settings is not respected

![Default folder settings](image.png)

#### Solution
Start MATLAB with the following parameter:
```bash
-useStartupFolderPref
```
 
