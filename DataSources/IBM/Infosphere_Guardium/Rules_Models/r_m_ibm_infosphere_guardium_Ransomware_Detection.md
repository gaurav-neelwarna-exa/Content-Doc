Vendor: IBM
===========
### Product: [Infosphere Guardium](../ds_ibm_infosphere_guardium.md)
### Use-Case: [Ransomware Detection](../../../../UseCases/uc_ransomware_detection.md)

| Rules | Models | MITRE TTPs | Event Types | Parsers |
|:-----:|:------:|:----------:|:-----------:|:-------:|
|   2   |   1    |     1      |      4      |    4    |

| Event Type     | Rules                                                                                                                                                                                                                                      | Models                                                                          |
| -------------- | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------- |
| database-alert | <b>T1204 - User Execution</b><br> ↳ <b>EPA-TEMP-DIRECTORY-F</b>: First execution of this process from a temporary directory on this asset<br> ↳ <b>EPA-TEMP-DIRECTORY-A</b>: Abnormal execution of this process from a temporary directory |  • <b>A-EPA-UP-TEMP</b>: Processes executed from TEMP directories on this asset |