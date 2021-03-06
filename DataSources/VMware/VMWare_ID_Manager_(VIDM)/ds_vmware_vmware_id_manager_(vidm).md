Vendor: VMware
==============
Product: VMWare ID Manager (VIDM)
---------------------------------
| Rules | Models | MITRE TTPs | Event Types | Parsers |
|:-----:|:------:|:----------:|:-----------:|:-------:|
|   5   |   3    |     2      |      1      |    1    |

|                                  Use-Case                                  | Event Types/Parsers                                                                                                       | MITRE TTP                  | Content                                                                                                                            |
|:--------------------------------------------------------------------------:| ------------------------------------------------------------------------------------------------------------------------- | -------------------------- | ---------------------------------------------------------------------------------------------------------------------------------- |
| [Compromised Credentials](../../../UseCases/uc_compromised_credentials.md) |  privileged-object-access<br> ↳ [vmware-id-manager-obj-access](Parsers/parserContent_vmware-id-manager-obj-access.md)<br> | T1078 - Valid Accounts<br> | [<ul><li>1 Rules</li></ul><ul><li>1 Models</li></ul>](Rules_Models/r_m_vmware_vmware_id_manager_(vidm)_Compromised_Credentials.md) |
|       [Malware Detection](../../../UseCases/uc_malware_detection.md)       |  privileged-object-access<br> ↳ [vmware-id-manager-obj-access](Parsers/parserContent_vmware-id-manager-obj-access.md)<br> | T1204 - User Execution<br> | [<ul><li>4 Rules</li></ul><ul><li>2 Models</li></ul>](Rules_Models/r_m_vmware_vmware_id_manager_(vidm)_Malware_Detection.md)       |
|    [Ransomware Detection](../../../UseCases/uc_ransomware_detection.md)    |  privileged-object-access<br> ↳ [vmware-id-manager-obj-access](Parsers/parserContent_vmware-id-manager-obj-access.md)<br> | T1204 - User Execution<br> | [<ul><li>4 Rules</li></ul><ul><li>2 Models</li></ul>](Rules_Models/r_m_vmware_vmware_id_manager_(vidm)_Ransomware_Detection.md)    |

ATT&CK Matrix for Enterprise
----------------------------
| Initial Access                                                      | Execution                                                           | Persistence                                                         | Privilege Escalation                                                | Defense Evasion                                                     | Credential Access | Discovery | Lateral Movement | Collection | Command and Control | Exfiltration | Impact |
| ------------------------------------------------------------------- | ------------------------------------------------------------------- | ------------------------------------------------------------------- | ------------------------------------------------------------------- | ------------------------------------------------------------------- | ----------------- | --------- | ---------------- | ---------- | ------------------- | ------------ | ------ |
| [Valid Accounts](https://attack.mitre.org/techniques/T1078)<br><br> | [User Execution](https://attack.mitre.org/techniques/T1204)<br><br> | [Valid Accounts](https://attack.mitre.org/techniques/T1078)<br><br> | [Valid Accounts](https://attack.mitre.org/techniques/T1078)<br><br> | [Valid Accounts](https://attack.mitre.org/techniques/T1078)<br><br> |                   |           |                  |            |                     |              |        |