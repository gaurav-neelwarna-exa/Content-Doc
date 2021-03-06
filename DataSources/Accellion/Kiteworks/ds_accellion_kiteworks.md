Vendor: Accellion
=================
Product: Kiteworks
------------------
| Rules | Models | MITRE TTPs | Event Types | Parsers |
|:-----:|:------:|:----------:|:-----------:|:-------:|
|  19   |   11   |     3      |      1      |    1    |

|                               Use-Case                               | Event Types/Parsers                                                                    | MITRE TTP                                                                                                      | Content                                                                                                             |
|:--------------------------------------------------------------------:| -------------------------------------------------------------------------------------- | -------------------------------------------------------------------------------------------------------------- | ------------------------------------------------------------------------------------------------------------------- |
|    [Data Exfiltration](../../../UseCases/uc_data_exfiltration.md)    |  dlp-alert<br> ↳ [accelion-dlp-alert](Parsers/parserContent_accelion-dlp-alert.md)<br> | T1020 - Automated Exfiltration<br>T1048 - Exfiltration Over Alternative Protocol<br>T1204 - User Execution<br> | [<ul><li>15 Rules</li></ul><ul><li>9 Models</li></ul>](Rules_Models/r_m_accellion_kiteworks_Data_Exfiltration.md)   |
|    [Malware Detection](../../../UseCases/uc_malware_detection.md)    |  dlp-alert<br> ↳ [accelion-dlp-alert](Parsers/parserContent_accelion-dlp-alert.md)<br> | T1204 - User Execution<br>                                                                                     | [<ul><li>5 Rules</li></ul><ul><li>3 Models</li></ul>](Rules_Models/r_m_accellion_kiteworks_Malware_Detection.md)    |
| [Ransomware Detection](../../../UseCases/uc_ransomware_detection.md) |  dlp-alert<br> ↳ [accelion-dlp-alert](Parsers/parserContent_accelion-dlp-alert.md)<br> | T1204 - User Execution<br>                                                                                     | [<ul><li>5 Rules</li></ul><ul><li>3 Models</li></ul>](Rules_Models/r_m_accellion_kiteworks_Ransomware_Detection.md) |

ATT&CK Matrix for Enterprise
----------------------------
| Initial Access | Execution                                                           | Persistence | Privilege Escalation | Defense Evasion | Credential Access | Discovery | Lateral Movement | Collection | Command and Control | Exfiltration                                                                                                                                                           | Impact |
| -------------- | ------------------------------------------------------------------- | ----------- | -------------------- | --------------- | ----------------- | --------- | ---------------- | ---------- | ------------------- | ---------------------------------------------------------------------------------------------------------------------------------------------------------------------- | ------ |
|                | [User Execution](https://attack.mitre.org/techniques/T1204)<br><br> |             |                      |                 |                   |           |                  |            |                     | [Exfiltration Over Alternative Protocol](https://attack.mitre.org/techniques/T1048)<br><br>[Automated Exfiltration](https://attack.mitre.org/techniques/T1020)<br><br> |        |