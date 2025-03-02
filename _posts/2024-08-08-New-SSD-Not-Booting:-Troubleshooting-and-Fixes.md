# New SSD Not Booting? Here’s How to Fix It

### Problem Summary

You just installed a new SSD to replace your old HDD, but your PC is showing the error: “No boot device found, press any key to reboot.” Even though the BIOS detects the SSD, the system refuses to boot. Let’s go over the possible causes and solutions.

---

### Understanding the Issue

A brand-new SSD comes completely blank, meaning it has no operating system installed. When your PC tries to boot, it looks for an OS but doesn't find one, resulting in the “No boot device found” error.

---

### Solutions

#### 1. Install a Fresh Copy of Windows

If you haven’t installed an operating system on the new SSD yet, follow these steps:

##### Create a Bootable USB Drive

- Download the Windows Media Creation Tool (or Windows 11 if applicable).
- Use the tool to create a bootable USB drive with Windows installation files.

##### Boot from the USB Drive

- Insert the USB drive into your PC.
- Restart and enter the BIOS (usually by pressing F2, F12, DEL, or ESC at startup).
- Set the USB drive as the primary boot device.
- Save and exit the BIOS.

##### Install Windows

- Follow the on-screen instructions to install Windows on your new SSD.

---

#### 2. Clone Your Old HDD to the New SSD

If you want to transfer everything from your old HDD, you’ll need to clone it:

##### Reinstall Your Old HDD (if possible) alongside the new SSD

- Use cloning software like Macrium Reflect, EaseUS Todo Backup, or Clonezilla.
- Use the software to clone your HDD to the SSD.

##### Remove the Old HDD After Cloning

- After cloning, remove the old HDD from your PC.

##### Set SSD as Boot Drive in BIOS

- Restart your PC and enter BIOS.
- Ensure the SSD is set as the primary boot drive.

---

#### 3. Check Boot Mode (UEFI vs. Legacy)

If you still get the error:

- Enter BIOS and check Boot Mode settings.
- If Windows was installed in **UEFI** mode, make sure Secure Boot is enabled and the SSD is set to **GPT**.
- If Windows was installed in **Legacy** mode, ensure the SSD is formatted as **MBR**.

---

#### 4. Double-Check Connections

Ensure that the cables are properly connected:

- Check the **SATA** cable and power cable.
- Try using a different SATA port on your motherboard.
- If using an **M.2 SSD**, confirm it's securely installed in the correct slot.

---

### Conclusion

If your SSD is not booting, it’s likely because there’s no operating system installed. The quickest solution is to install Windows using a bootable USB. If you want to keep all your files and settings, you’ll need to clone your HDD to your SSD. If problems persist, checking your BIOS settings and drive connections can help resolve boot issues.

---

**Have any questions? Let us know in the comments!**

---

**Keywords**: SSD not booting, no boot device found, Windows installation, HDD to SSD migration, bootable USB, cloning HDD to SSD
