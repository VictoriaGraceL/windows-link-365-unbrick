# Windows 365 Link Unbrick

An independent recovery guide for Windows 365 Link, based on Microsoft documentation and Dieter Kempeneers' walkthrough. Reviewed October 4, 2026.

**Destructive procedure:** USB preparation erases the selected USB drive; recovery erases the Link device. Get authorization from its owner or IT administrator. Keep power connected throughout reimaging.

This guide combines documentation with the author's reported hardware experience: a USB drive showing 7.2 GB capacity and a metal pin to enter UEFI boot settings. Completion of the full recovery has been confirmed.

## Choose a recovery method

If the device works, use Intune Wipe or Company Portal Reset. For enrollment trouble, try OOBE quick settings → About this device → Reset this device. Use bare-metal recovery (BMR) when normal recovery is unavailable.

## 1. Prepare

Have physical access, another Windows PC, a keyboard/display, and a USB drive with enough capacity. The author used a USB drive showing **7.2 GB capacity**. This is a reported setup, not a universal minimum: ensure the extracted recovery files fit on your prepared drive. Microsoft specifies sufficient capacity rather than a fixed size.

Download the **Windows 365 Link** BMR ZIP for your language from [Microsoft's recovery page](https://learn.microsoft.com/en-us/windows-365/link/wipe-reset-windows-365-link#bare-metal-recovery-bmr). Do not substitute a Surface OS image.

## 2. Make the USB

On the working PC:

1. Back up the USB's contents.
2. Search Start for **Recovery Drive** and open it; approve the administrator prompt.
3. Clear **Back up system files to the recovery drive**.
4. Select the correct USB → Next → Create → Finish.
5. Extract the downloaded ZIP. Copy its contents to the USB root, replacing existing files. Do not copy only the ZIP or its enclosing folder.
6. Safely eject the USB.

Microsoft's [USB preparation instructions](https://support.microsoft.com/en-US/surface/drivers-firmware/creating-and-using-a-usb-recovery-drive-for-surface) are referenced by the Link documentation. Recovery Drive handles FAT32 preparation.

## 3. Boot recovery

Insert the prepared USB. During startup or reboot, gently press the recessed button in the hole **beneath the power port on the back of the device** using a metal pin, paper clip, or SIM tool. The author used a metal pin to enter the UEFI boot settings. This opens the firmware menu; select the USB there to start recovery.

In UEFI, open **Boot configuration**. Hold the left mouse button on **USB Storage**, swipe left, then confirm **OK** to boot immediately. This boot-selection procedure comes from [Microsoft's Link firmware guide](https://learn.microsoft.com/en-us/windows-365/link/manage-firmware-settings).

Alternatively, force shutdown with the power button before Windows finishes loading; repeat at least two more times. When WinRE starts, choose **Advanced options → Use device → USB Storage**. Never interrupt an active recovery installation.

## 4. Reimage

1. Choose the keyboard layout.
2. Select **Recover from a drive**.
3. Skip the device BitLocker recovery key as directed for BMR.
4. Choose **Just remove my files** or **Fully clean the drive** according to your organization's requirements.
5. Confirm recovery and allow installation/restarts.
6. Complete setup and reprovision through your organization's Windows 365/Intune workflow.

An ordinary WinRE reset requires a BitLocker key; the BMR flow above has different instructions.


No recovery binaries or automated wipe scripts are included. Windows 365 and Microsoft names belong to their respective owners; this project is not affiliated with Microsoft.
