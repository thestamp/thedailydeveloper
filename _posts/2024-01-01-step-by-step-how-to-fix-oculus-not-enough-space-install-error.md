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

![Oculus Installation Error](/assets/images/step-by-step-how-to-fix-oculus-not-enough-space-install-error/2020-03-08_20-29-01.png)

# The Cause

This error happens when your hard drive is configured as "dynamic disks," that enables certain features for more performance, extendability and reliability. Unfortunately the Oculus setup software didn't account for this.

# The fix in a nutshell

Let's start off by saying that we are **not** reconfiguring your hard drive as "basic" (as most guides out there tell you to do). I don't want to spend hours backing up my data and reinstalling windows just to use VR.

Instead, we are simply creating a disk file (known as a **virtual disk)**, configured as **basic** so that the Oculus software can happily install. This is a feature of Windows 8.1, Windows 10, and above.

# Step by Step

### Part 1 – Create the virtual disk

1. Right click the start button, and click "Disk Management"
   ![Disk Management](/assets/images/step-by-step-how-to-fix-oculus-not-enough-space-install-error/2020-03-08_20-59-01.png)

2. In the Disk Manager, click "Action" and then "Create VHD"
   ![Create VHD Menu](/assets/images/step-by-step-how-to-fix-oculus-not-enough-space-install-error/2020-03-08_20-29-50.png)

3. In the dialog that appears click "Browse" to pick a spot to save the disk
   ![Create VHD Dialog](/assets/images/step-by-step-how-to-fix-oculus-not-enough-space-install-error/2020-03-08_20-31-46-2.png)

4. Navigate the Browse window to C:\Oculus Software (or a spot of your choosing) and enter "OculusDisk" in the File Name
   ![Browse for Location](/assets/images/step-by-step-how-to-fix-oculus-not-enough-space-install-error/2020-03-08_20-31-08.png)

5. Then press OK
   ![Disk Configuration](/assets/images/step-by-step-how-to-fix-oculus-not-enough-space-install-error/2020-03-08_20-31-46-2-1.png)

6. Navigate the Browse window to C:\Oculus Software (or a spot of your choosing) and enter "OculusDisk" in the File Name
   ![Browse Location](/assets/images/step-by-step-how-to-fix-oculus-not-enough-space-install-error/2020-03-08_20-32-16.png)

7. In the Virtual Hard Drive disk space field, enter "20" and select "GB", then press OK  
   ![Disk Space Field](/assets/images/step-by-step-how-to-fix-oculus-not-enough-space-install-error/2020-03-08_20-32-27.png)

### Part 2: Make the Virtual Disk Accessible

8. In that newly created disk area, right click the grey area on the left and click Initialize Disk
   ![Initialize Disk](/assets/images/step-by-step-how-to-fix-oculus-not-enough-space-install-error/2020-03-08_20-32-37.png)

9. Click OK in the dialog that appears
   ![Initialize Disk Dialog](/assets/images/step-by-step-how-to-fix-oculus-not-enough-space-install-error/2020-03-08_20-32-44.png)

10. The dialog should close. Right click the white area of the new disk (under the black bar) and click New Simple Volume
    ![New Simple Volume](/assets/images/step-by-step-how-to-fix-oculus-not-enough-space-install-error/2020-03-08_20-32-51.png)

11. In the **Assign Drive Letter or Path** step, beside **Assign the following drive letter**, click and select "O" in the dropdown and click **Next.**
    ![Assign Drive Letter](/assets/images/step-by-step-how-to-fix-oculus-not-enough-space-install-error/2020-03-08_20-33-07.png)

12. In the **Format Partition** step, beside **Volume Label**, enter "Oculus" in the text field and click **Next.**
    ![Format Partition](/assets/images/step-by-step-how-to-fix-oculus-not-enough-space-install-error/2020-03-08_20-33-26.png)

13. Lastly, click **Finish.**
    ![Finish Volume Creation](/assets/images/step-by-step-how-to-fix-oculus-not-enough-space-install-error/2020-03-08_20-33-31.png)

### Part 3: Installing the Oculus Software

14. Right click the **Start Button** and click **Run**
    ![Run Dialog Access](/assets/images/step-by-step-how-to-fix-oculus-not-enough-space-install-error/2020-03-08_20-34-26.png)

15. In the **Run Dialog**, click **Browse**
    ![Run Dialog](/assets/images/step-by-step-how-to-fix-oculus-not-enough-space-install-error/2020-03-08_21-08-39.png)

16. Browse to the Oculus Installer, and click Open

17. In the File Path text box, press the **spacebar** and add the following text to the end, then press **OK**:
    ```
    /drive=O
    ```

    It should look a bit like this:

    ![Oculus Installer Command](/assets/images/step-by-step-how-to-fix-oculus-not-enough-space-install-error/2020-03-08_20-35-16-2.png)

18. Go through the steps in the Oculus Software installer!

    ![Oculus Installer Screenshots](/assets/images/step-by-step-how-to-fix-oculus-not-enough-space-install-error/2020-03-08_20-35-37.png)
    
    ![Oculus Installer Step 2](/assets/images/step-by-step-how-to-fix-oculus-not-enough-space-install-error/2020-03-08_20-35-40.png)
    
    ![Oculus Installer Step 3](/assets/images/step-by-step-how-to-fix-oculus-not-enough-space-install-error/2020-03-08_20-35-45.png)

**Enjoy Oculus VR! Give me a follow at @TheDailyDev on X!