Vendor: IBM
===========
Product: IBM DB2
----------------
| Rules | Models | MITRE TTPs | Event Types | Parsers |
|:-----:|:------:|:----------:|:-----------:|:-------:|
|  78   |   40   |     14     |      4      |    4    |

|                                  Use-Case                                  | Event Types/Parsers                                                                                                                                                                                                                                                                                                                                                                                                                                                                      | MITRE TTP                                                                                                                                                                                                                                                                                                                                                                                                                                                      | Content                                                                                                          |
|:--------------------------------------------------------------------------:| ---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- | -------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- | ---------------------------------------------------------------------------------------------------------------- |
| [Compromised Credentials](../../../UseCases/uc_compromised_credentials.md) |  authentication-failed<br> ↳ [cef-db2-auth-failed](Parsers/parserContent_cef-db2-auth-failed.md)<br><br> file-read<br> ↳ [cef-db2-file-read](Parsers/parserContent_cef-db2-file-read.md)<br><br> remote-logon<br> ↳ [cef-db2-remote-logon](Parsers/parserContent_cef-db2-remote-logon.md)<br><br> security-alert<br> ↳ [cef-db2-security-alert](Parsers/parserContent_cef-db2-security-alert.md)<br> ↳ [cef-db2-security-alert-2](Parsers/parserContent_cef-db2-security-alert-2.md)<br> | T1021 - Remote Services<br>T1027.005 - Obfuscated Files or Information: Indicator Removal from Tools<br>T1059.001 - Command and Scripting Interperter: PowerShell<br>T1078 - Valid Accounts<br>T1083 - File and Directory Discovery<br>T1133 - External Remote Services<br>T1550 - Use Alternate Authentication Material<br>T1550.002 - Use Alternate Authentication Material: Pass the Hash<br>T1558.003 - Steal or Forge Kerberos Tickets: Kerberoasting<br> | [<ul><li>51 Rules</li></ul><ul><li>26 Models</li></ul>](Rules_Models/r_m_ibm_ibm_db2_Compromised_Credentials.md) |
|       [Data Exfiltration](../../../UseCases/uc_data_exfiltration.md)       |  authentication-failed<br> ↳ [cef-db2-auth-failed](Parsers/parserContent_cef-db2-auth-failed.md)<br><br> file-read<br> ↳ [cef-db2-file-read](Parsers/parserContent_cef-db2-file-read.md)<br><br> remote-logon<br> ↳ [cef-db2-remote-logon](Parsers/parserContent_cef-db2-remote-logon.md)<br><br> security-alert<br> ↳ [cef-db2-security-alert](Parsers/parserContent_cef-db2-security-alert.md)<br> ↳ [cef-db2-security-alert-2](Parsers/parserContent_cef-db2-security-alert-2.md)<br> | T1083 - File and Directory Discovery<br>                                                                                                                                                                                                                                                                                                                                                                                                                       | [<ul><li>3 Rules</li></ul><ul><li>3 Models</li></ul>](Rules_Models/r_m_ibm_ibm_db2_Data_Exfiltration.md)         |
|        [Lateral Movement](../../../UseCases/uc_lateral_movement.md)        |  authentication-failed<br> ↳ [cef-db2-auth-failed](Parsers/parserContent_cef-db2-auth-failed.md)<br><br> file-read<br> ↳ [cef-db2-file-read](Parsers/parserContent_cef-db2-file-read.md)<br><br> remote-logon<br> ↳ [cef-db2-remote-logon](Parsers/parserContent_cef-db2-remote-logon.md)<br><br> security-alert<br> ↳ [cef-db2-security-alert](Parsers/parserContent_cef-db2-security-alert.md)<br> ↳ [cef-db2-security-alert-2](Parsers/parserContent_cef-db2-security-alert-2.md)<br> | T1018 - Remote System Discovery<br>T1021 - Remote Services<br>T1078 - Valid Accounts<br>T1078.003 - Valid Accounts: Local Accounts<br>T1133 - External Remote Services<br>T1550 - Use Alternate Authentication Material<br>T1558.003 - Steal or Forge Kerberos Tickets: Kerberoasting<br>                                                                                                                                                                      | [<ul><li>22 Rules</li></ul><ul><li>14 Models</li></ul>](Rules_Models/r_m_ibm_ibm_db2_Lateral_Movement.md)        |
|       [Malware Detection](../../../UseCases/uc_malware_detection.md)       |  authentication-failed<br> ↳ [cef-db2-auth-failed](Parsers/parserContent_cef-db2-auth-failed.md)<br><br> file-read<br> ↳ [cef-db2-file-read](Parsers/parserContent_cef-db2-file-read.md)<br><br> remote-logon<br> ↳ [cef-db2-remote-logon](Parsers/parserContent_cef-db2-remote-logon.md)<br><br> security-alert<br> ↳ [cef-db2-security-alert](Parsers/parserContent_cef-db2-security-alert.md)<br> ↳ [cef-db2-security-alert-2](Parsers/parserContent_cef-db2-security-alert-2.md)<br> | T1027.005 - Obfuscated Files or Information: Indicator Removal from Tools<br>T1059.001 - Command and Scripting Interperter: PowerShell<br>T1078 - Valid Accounts<br>T1090.003 - Proxy: Multi-hop Proxy<br>T1204 - User Execution<br>                                                                                                                                                                                                                           | [<ul><li>13 Rules</li></ul><ul><li>4 Models</li></ul>](Rules_Models/r_m_ibm_ibm_db2_Malware_Detection.md)        |
|     [Privileged Activity](../../../UseCases/uc_privileged_activity.md)     |  authentication-failed<br> ↳ [cef-db2-auth-failed](Parsers/parserContent_cef-db2-auth-failed.md)<br><br> file-read<br> ↳ [cef-db2-file-read](Parsers/parserContent_cef-db2-file-read.md)<br><br> remote-logon<br> ↳ [cef-db2-remote-logon](Parsers/parserContent_cef-db2-remote-logon.md)<br><br> security-alert<br> ↳ [cef-db2-security-alert](Parsers/parserContent_cef-db2-security-alert.md)<br> ↳ [cef-db2-security-alert-2](Parsers/parserContent_cef-db2-security-alert-2.md)<br> | T1068 - Exploitation for Privilege Escalation<br>T1078 - Valid Accounts<br>                                                                                                                                                                                                                                                                                                                                                                                    | [<ul><li>2 Rules</li></ul><ul><li>1 Models</li></ul>](Rules_Models/r_m_ibm_ibm_db2_Privileged_Activity.md)       |
|    [Ransomware Detection](../../../UseCases/uc_ransomware_detection.md)    |  authentication-failed<br> ↳ [cef-db2-auth-failed](Parsers/parserContent_cef-db2-auth-failed.md)<br><br> file-read<br> ↳ [cef-db2-file-read](Parsers/parserContent_cef-db2-file-read.md)<br><br> remote-logon<br> ↳ [cef-db2-remote-logon](Parsers/parserContent_cef-db2-remote-logon.md)<br><br> security-alert<br> ↳ [cef-db2-security-alert](Parsers/parserContent_cef-db2-security-alert.md)<br> ↳ [cef-db2-security-alert-2](Parsers/parserContent_cef-db2-security-alert-2.md)<br> | T1027.005 - Obfuscated Files or Information: Indicator Removal from Tools<br>T1059.001 - Command and Scripting Interperter: PowerShell<br>T1078 - Valid Accounts<br>T1090.003 - Proxy: Multi-hop Proxy<br>T1204 - User Execution<br>                                                                                                                                                                                                                           | [<ul><li>13 Rules</li></ul><ul><li>4 Models</li></ul>](Rules_Models/r_m_ibm_ibm_db2_Ransomware_Detection.md)     |

ATT&CK Matrix for Enterprise
----------------------------
| Initial Access                                                                                                                                   | Execution                                                                                                                                                                                                                                                       | Persistence                                                                                                                                      | Privilege Escalation                                                                                                                                          | Defense Evasion                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                             | Credential Access                                                                                                                                                                           | Discovery                                                                                                                                                     | Lateral Movement                                                                                                                                               | Collection | Command and Control                                                                                                                       | Exfiltration | Impact |
| ------------------------------------------------------------------------------------------------------------------------------------------------ | --------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- | ------------------------------------------------------------------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------------------------------------------------------------------------------- | --------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- | ------------------------------------------------------------------------------------------------------------------------------------------------------------- | -------------------------------------------------------------------------------------------------------------------------------------------------------------- | ---------- | ----------------------------------------------------------------------------------------------------------------------------------------- | ------------ | ------ |
| [External Remote Services](https://attack.mitre.org/techniques/T1133)<br><br>[Valid Accounts](https://attack.mitre.org/techniques/T1078)<br><br> | [Command and Scripting Interperter](https://attack.mitre.org/techniques/T1059)<br><br>[User Execution](https://attack.mitre.org/techniques/T1204)<br><br>[Command and Scripting Interperter: PowerShell](https://attack.mitre.org/techniques/T1059/001)<br><br> | [External Remote Services](https://attack.mitre.org/techniques/T1133)<br><br>[Valid Accounts](https://attack.mitre.org/techniques/T1078)<br><br> | [Valid Accounts](https://attack.mitre.org/techniques/T1078)<br><br>[Exploitation for Privilege Escalation](https://attack.mitre.org/techniques/T1068)<br><br> | [Obfuscated Files or Information: Indicator Removal from Tools](https://attack.mitre.org/techniques/T1027/005)<br><br>[Valid Accounts](https://attack.mitre.org/techniques/T1078)<br><br>[Use Alternate Authentication Material](https://attack.mitre.org/techniques/T1550)<br><br>[Use Alternate Authentication Material: Pass the Hash](https://attack.mitre.org/techniques/T1550/002)<br><br>[Obfuscated Files or Information](https://attack.mitre.org/techniques/T1027)<br><br>[Valid Accounts: Local Accounts](https://attack.mitre.org/techniques/T1078/003)<br><br> | [Steal or Forge Kerberos Tickets](https://attack.mitre.org/techniques/T1558)<br><br>[Steal or Forge Kerberos Tickets: Kerberoasting](https://attack.mitre.org/techniques/T1558/003)<br><br> | [File and Directory Discovery](https://attack.mitre.org/techniques/T1083)<br><br>[Remote System Discovery](https://attack.mitre.org/techniques/T1018)<br><br> | [Remote Services](https://attack.mitre.org/techniques/T1021)<br><br>[Use Alternate Authentication Material](https://attack.mitre.org/techniques/T1550)<br><br> |            | [Proxy: Multi-hop Proxy](https://attack.mitre.org/techniques/T1090/003)<br><br>[Proxy](https://attack.mitre.org/techniques/T1090)<br><br> |              |        |