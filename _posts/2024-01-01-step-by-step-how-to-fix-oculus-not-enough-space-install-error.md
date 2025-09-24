---
layout: post
title: "Step by Step: How to Fix Oculus 'Not Enough Space' Install Error"
date: 2024-01-01 12:00:00 -0000
permalink: /step-by-step-how-to-fix-oculus-not-enough-space-install-error/
categories: [VR, Oculus, Windows, Troubleshooting]
tags: [oculus, vr, windows, disk-management, virtual-disk, installation]
excerpt: "Fix the frustrating 'Out of disk space' error when installing Oculus software on Windows, even when you have plenty of space available."
---

Although a leading provider of VR technologies, Oculus is not known for their Windows software prowess. When you install the Oculus app software and you've encountered an "Out of disk space" error when you have enough disk space, look no further. This is how to get around it.

![Oculus Installation Error](/assets/images/step-by-step-how-to-fix-oculus-not-enough-space-install-error/disk-management.png)

## The Cause

This error happens when your hard drive is configured as "dynamic disks," that enables certain features for more performance, extendability and reliability. Unfortunately the Oculus setup software didn't account for this.

![Dynamic Disk Configuration](/assets/images/step-by-step-how-to-fix-oculus-not-enough-space-install-error/create-vhd-dialog.png)

## The fix in a nutshell

Let's start off by saying that we are not reconfiguring your hard drive as "basic" (as most guides out there tell you to do). I don't want to spend hours backing up my data and reinstalling windows just to use VR.

Instead, we are simply creating a disk file (known as a virtual disk), configured as basic so that the Oculus software can happily install. This is a feature of Windows 8.1, Windows 10, and above.

![Virtual Disk Solution](/assets/images/step-by-step-how-to-fix-oculus-not-enough-space-install-error/browse-location.png)

## Step by Step

### Part 1 – Create the virtual disk

Right click the start button, and click "Disk Management"

![Disk Management Access](/assets/images/step-by-step-how-to-fix-oculus-not-enough-space-install-error/disk-size-config.png)

In the Disk Manager, click "Action" and then "Create VHD"

![Create VHD Menu](/assets/images/step-by-step-how-to-fix-oculus-not-enough-space-install-error/initialize-disk.png)

In the dialog that appears click "Browse" to pick a spot to save the disk

Navigate the Browse window to C:\Oculus Software (or a spot of your choosing) and enter "OculusDisk" in the File Name

![Browse for Location](/assets/images/step-by-step-how-to-fix-oculus-not-enough-space-install-error/new-simple-volume.png)

In the Virtual Hard Drive disk space field, enter "20" and select "GB"
Then press OK

![Disk Size Configuration](/assets/images/step-by-step-how-to-fix-oculus-not-enough-space-install-error/volume-wizard.png)

### Part 2: Make the Virtual Disk Accessible

In that newly created disk area, right click the grey area on the left and click Initialize Disk

Click OK in the dialog that appears

![Initialize Disk Dialog](/assets/images/step-by-step-how-to-fix-oculus-not-enough-space-install-error/assign-drive-letter.png)

The dialog should close.
Right click the white area of the new disk (under the black bar) and click New Simple Volume

In the Welcome to the New Simple Volume Wizard dialog, click Next.

![New Simple Volume Wizard](/assets/images/step-by-step-how-to-fix-oculus-not-enough-space-install-error/format-partition.png)

In the Specify Volume Size step, click Next.

In the Assign Drive Letter or Path step, beside Assign the following drive letter, click and select "O" in the dropdown and click Next.

![Assign Drive Letter](/assets/images/step-by-step-how-to-fix-oculus-not-enough-space-install-error/run-dialog.png)

In the Format Partition step, beside Volume Label, enter "Oculus" in the text field and click Next.

Lastly, click Finish.

![Format Partition](/assets/images/step-by-step-how-to-fix-oculus-not-enough-space-install-error/oculus-installer-command.png)

### Part 3: Installing the Oculus Software

Right click the Start Button and click Run

In the Run Dialog, click Browse

Browse to the Oculus Installer, and click Open

In the File Path text box, press the spacebar and add the following text to the end, then press OK:
```
/drive=O
```

It should look a bit like this:

![Oculus Installer Command](/assets/images/step-by-step-how-to-fix-oculus-not-enough-space-install-error/oculus-installer-command.png)

Go through the steps in the Oculus Software installer!

Enjoy Oculus VR! Give me a follow at @TheDailyDev on twitter, or contact me at <a href="https://web.archive.org/web/20210301101200/http://thedailydeveloper.com/hello">http://thedailydeveloper.com/hello</a>