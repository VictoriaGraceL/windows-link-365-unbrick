# Troubleshooting

These are documentation-based checks and practical suggestions, not hardware-tested fixes.

| Symptom | Next step |
| --- | --- |
| USB does not appear | Reconnect it directly, try another port, and confirm preparation completed. If available, check UEFI's USB boot setting. |
| Device boots normally from the USB | Kempeneers observed this behavior. Enter UEFI and deliberately select the prepared USB as described in the README. |
| Recover from a drive is missing | Rebuild the USB with Recovery Drive, then copy the extracted Link recovery contents to its root, replacing files. |
| No bootable operating system | Kempeneers identifies this as a BMR use case. Follow the README recovery procedure. |
| UEFI settings are locked | Ask the managing IT team; Link firmware can be managed with SEMM and a UEFI password. |
| Recovery fails repeatedly | Record the exact error and stage. Try freshly prepared media before escalating to IT/Microsoft support. Might be an issue with USB Driver prepared incorrectly. |
| No power or display | Check power, cable, display input, and peripherals. BMR cannot guarantee repair of failed hardware. |
| Setup fails after recovery | Record the enrollment error and contact the tenant's Microsoft support. |

After recovery, remove the USB when installation is finished and verify that the device starts from internal storage. As a practical acceptance check, confirm setup, enrollment, and access to the expected Cloud PC with your IT team.

Do not post passwords, BitLocker keys, tenant identifiers, serial numbers, or unredacted organizational screenshots in public issues.
