Vendor: Microsoft
=================
Product: NetApp
---------------
|                                 Use-Case                                  | Activity Types                                | Event Types/Parsers                                                                                                                                                                     | MITRE TTP                                                          | Content                   |
|:-------------------------------------------------------------------------:| --------------------------------------------- | --------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- | ------------------------------------------------------------------ | ------------------------- |
| [Compromised Credentials](../UseCases/usecase_compromised_credentials.md) | - Critical System Activity<br>- File Activity |  file-alert<br> -- [s-xml-4656-netapp](../Parsers/parserContent_s-xml-4656-netapp.md)<br><br> file-delete<br> -- [s-xml-4660-netapp](../Parsers/parserContent_s-xml-4660-netapp.md)<br> | T1078 - Valid Accounts<br>T1083 - File and Directory Discovery<br> |  - 3 Rules<br> - 2 Models |
|       [Data Exfiltration](../UseCases/usecase_data_exfiltration.md)       | - File Activity                               |  file-alert<br> -- [s-xml-4656-netapp](../Parsers/parserContent_s-xml-4656-netapp.md)<br><br> file-delete<br> -- [s-xml-4660-netapp](../Parsers/parserContent_s-xml-4660-netapp.md)<br> | T1083 - File and Directory Discovery<br>                           |  - 3 Rules<br> - 3 Models |
|       [Malware Detection](../UseCases/usecase_malware_detection.md)       | - Endpoint Activity<br>- File Activity        |  file-alert<br> -- [s-xml-4656-netapp](../Parsers/parserContent_s-xml-4656-netapp.md)<br><br> file-delete<br> -- [s-xml-4660-netapp](../Parsers/parserContent_s-xml-4660-netapp.md)<br> | T1204 - User Execution<br>                                         |  - 3 Rules<br> - 1 Models |
|    [Ransomware Detection](../UseCases/usecase_ransomware_detection.md)    | - Endpoint Activity<br>- File Activity        |  file-alert<br> -- [s-xml-4656-netapp](../Parsers/parserContent_s-xml-4656-netapp.md)<br><br> file-delete<br> -- [s-xml-4660-netapp](../Parsers/parserContent_s-xml-4660-netapp.md)<br> | T1204 - User Execution<br>                                         |  - 3 Rules<br> - 1 Models |

ATT&CK Matrix for Enterprise
----------------------------
| Initial Access                                                      | Execution                                                           | Persistence                                                         | Privilage escalation                                                | Defense evasion                                                     | Credential Access | Discovery                                                                         | Lateral Movement | Collection | Command and Control | Exfiltration | Impact |
| ------------------------------------------------------------------- | ------------------------------------------------------------------- | ------------------------------------------------------------------- | ------------------------------------------------------------------- | ------------------------------------------------------------------- | ----------------- | --------------------------------------------------------------------------------- | ---------------- | ---------- | ------------------- | ------------ | ------ |
| [Valid Accounts](https://attack.mitre.org/techniques/T1078)<br><br> | [User Execution](https://attack.mitre.org/techniques/T1204)<br><br> | [Valid Accounts](https://attack.mitre.org/techniques/T1078)<br><br> | [Valid Accounts](https://attack.mitre.org/techniques/T1078)<br><br> | [Valid Accounts](https://attack.mitre.org/techniques/T1078)<br><br> |                   | [File and Directory Discovery](https://attack.mitre.org/techniques/T1083)<br><br> |                  |            |                     |              |        |