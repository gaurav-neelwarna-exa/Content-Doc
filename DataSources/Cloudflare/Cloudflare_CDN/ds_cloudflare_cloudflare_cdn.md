Vendor: Cloudflare
==================
Product: Cloudflare CDN
-----------------------
| Rules | Models | MITRE TTPs | Event Types | Parsers |
|:-----:|:------:|:----------:|:-----------:|:-------:|
|   9   |   6    |     2      |      1      |    1    |

|                               Use-Case                               | Event Types/Parsers                                                                                        | MITRE TTP                                                                     | Content                                                                                                                   |
|:--------------------------------------------------------------------:| ---------------------------------------------------------------------------------------------------------- | ----------------------------------------------------------------------------- | ------------------------------------------------------------------------------------------------------------------------- |
|     [Lateral Movement](../../../UseCases/uc_lateral_movement.md)     |  network-alert<br> ↳ [cloudflare-network-alert-2](Parsers/parserContent_cloudflare-network-alert-2.md)<br> | T1027.005 - Obfuscated Files or Information: Indicator Removal from Tools<br> | [<ul><li>5 Rules</li></ul><ul><li>4 Models</li></ul>](Rules_Models/r_m_cloudflare_cloudflare_cdn_Lateral_Movement.md)     |
|    [Malware Detection](../../../UseCases/uc_malware_detection.md)    |  network-alert<br> ↳ [cloudflare-network-alert-2](Parsers/parserContent_cloudflare-network-alert-2.md)<br> | T1204 - User Execution<br>                                                    | [<ul><li>4 Rules</li></ul><ul><li>2 Models</li></ul>](Rules_Models/r_m_cloudflare_cloudflare_cdn_Malware_Detection.md)    |
| [Ransomware Detection](../../../UseCases/uc_ransomware_detection.md) |  network-alert<br> ↳ [cloudflare-network-alert-2](Parsers/parserContent_cloudflare-network-alert-2.md)<br> | T1204 - User Execution<br>                                                    | [<ul><li>4 Rules</li></ul><ul><li>2 Models</li></ul>](Rules_Models/r_m_cloudflare_cloudflare_cdn_Ransomware_Detection.md) |

ATT&CK Matrix for Enterprise
----------------------------
| Initial Access | Execution                                                           | Persistence | Privilege Escalation | Defense Evasion                                                                                                                                                                                            | Credential Access | Discovery | Lateral Movement | Collection | Command and Control | Exfiltration | Impact |
| -------------- | ------------------------------------------------------------------- | ----------- | -------------------- | ---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- | ----------------- | --------- | ---------------- | ---------- | ------------------- | ------------ | ------ |
|                | [User Execution](https://attack.mitre.org/techniques/T1204)<br><br> |             |                      | [Obfuscated Files or Information: Indicator Removal from Tools](https://attack.mitre.org/techniques/T1027/005)<br><br>[Obfuscated Files or Information](https://attack.mitre.org/techniques/T1027)<br><br> |                   |           |                  |            |                     |              |        |