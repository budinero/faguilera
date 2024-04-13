---
# Documentation: https://hugoblox.com/docs/managing-content/

title: "MATLAB Notes"
subtitle: "Notes on tips and troubleshooting."
summary: "Notes on tips and troubleshooting for MATLAB software on Linux"
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

# Dark theme problems with MATLAB/Simulink
> Tested with _Debian Trixie_ GNU/Linux / KDE/Plasma / MATLAB 2013a. 

#### Error:
Simulink has a broken color scheme when using dark theme in Linux.

![simulink_dark](simulink_dark.png)

#### Solution:
Simulink uses some Qt libraries, so some configurations can be changed with environment variables. Theme preferences are
defined in the ~/.config folder, thus simple steps can be followed to use MATLAB with its default light theme and system dark theme (using KDE). 

1. Close any MATLAB instance
2. Select a light theme, i.e.
```bash
plasma-apply-colorscheme BreezeClassic
```
3. Make a copy of the .config folder
```bash
cp ~/.config ~/.config_matlab
```
4. Return back to your preferred dark theme
```bash
plasma-apply-colorscheme BreezeDark
```
5. Start MATLAB with the modified .config folder and test.
```bash
export XDG_CONFIG_HOME=~/.config_matlab; matlab
```
6. Configure the desktop MATLAB launcher
![alt text](matlab_launcher.png)

_More info: https://la.mathworks.com/matlabcentral/answers/1848238-simulink-has-broken-color-scheme_

# Can't run MATLAB 2022a/2023a installer

> Tested with _Debian 12 (Bookworm)_ GNU/Linux  

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

# Error when loading any plot

#### Error:
```bash
`com.jogamp.opengl.GLException: X11GLXDrawableFactory`
```

#### Solution:
```
nano (intall_dir)/bin/glnxa64/java.opts
```
Paste `-Djogl.disable.openglarbcontext=1` inside the text file.

# Simulink error "Failed to load bundle..."
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

# MATLAB startup doesn't respect default folder settings

#### Problem
Default folder settings is not respected

![Default folder settings](image.png)

#### Solution
Start MATLAB with the following parameter:
```bash
-useStartupFolderPref
```
 
