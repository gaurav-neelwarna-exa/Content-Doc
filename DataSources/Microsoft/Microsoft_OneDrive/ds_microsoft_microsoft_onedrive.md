Vendor: Microsoft
=================
Product: Microsoft OneDrive
---------------------------
| Rules | Models | MITRE TTPs | Event Types | Parsers |
|:-----:|:------:|:----------:|:-----------:|:-------:|
|   4   |   3    |     2      |      1      |    1    |

|                                  Use-Case                                  | Event Types/Parsers                                                                                    | MITRE TTP                                                          | Content                                                                                                                         |
|:--------------------------------------------------------------------------:| ------------------------------------------------------------------------------------------------------ | ------------------------------------------------------------------ | ------------------------------------------------------------------------------------------------------------------------------- |
| [Compromised Credentials](../../../UseCases/uc_compromised_credentials.md) |  file-read<br> ↳ [cef-onedrive-file-activity](Parsers/parserContent_cef-onedrive-file-activity.md)<br> | T1078 - Valid Accounts<br>T1083 - File and Directory Discovery<br> | [<ul><li>3 Rules</li></ul><ul><li>2 Models</li></ul>](Rules_Models/r_m_microsoft_microsoft_onedrive_Compromised_Credentials.md) |
|       [Data Exfiltration](../../../UseCases/uc_data_exfiltration.md)       |  file-read<br> ↳ [cef-onedrive-file-activity](Parsers/parserContent_cef-onedrive-file-activity.md)<br> | T1083 - File and Directory Discovery<br>                           | [<ul><li>3 Rules</li></ul><ul><li>3 Models</li></ul>](Rules_Models/r_m_microsoft_microsoft_onedrive_Data_Exfiltration.md)       |

ATT&CK Matrix for Enterprise
----------------------------
| Initial Access                                                      | Execution | Persistence                                                         | Privilege Escalation                                                | Defense Evasion                                                     | Credential Access | Discovery                                                                         | Lateral Movement | Collection | Command and Control | Exfiltration | Impact |
| ------------------------------------------------------------------- | --------- | ------------------------------------------------------------------- | ------------------------------------------------------------------- | ------------------------------------------------------------------- | ----------------- | --------------------------------------------------------------------------------- | ---------------- | ---------- | ------------------- | ------------ | ------ |
| [Valid Accounts](https://attack.mitre.org/techniques/T1078)<br><br> |           | [Valid Accounts](https://attack.mitre.org/techniques/T1078)<br><br> | [Valid Accounts](https://attack.mitre.org/techniques/T1078)<br><br> | [Valid Accounts](https://attack.mitre.org/techniques/T1078)<br><br> |                   | [File and Directory Discovery](https://attack.mitre.org/techniques/T1083)<br><br> |                  |            |                     |              |        |