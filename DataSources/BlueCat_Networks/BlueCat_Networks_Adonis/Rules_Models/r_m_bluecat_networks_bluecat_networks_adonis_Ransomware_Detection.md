Vendor: BlueCat Networks
========================
### Product: [BlueCat Networks Adonis](../ds_bluecat_networks_bluecat_networks_adonis.md)
### Use-Case: [Ransomware Detection](../../../../UseCases/uc_ransomware_detection.md)

| Rules | Models | MITRE TTPs | Event Types | Parsers |
|:-----:|:------:|:----------:|:-----------:|:-------:|
|   2   |   1    |     2      |      1      |    1    |

| Event Type | Rules                                                                                                                                                                                                                                                                                     | Models |
| ---------- | ----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- | ------ |
| dns-query  | <b>T1071.004 - Application Layer Protocol: DNS</b><br> ↳ <b>A-DNS-MALDOM-QUERY</b>: DNS query for blacklisted domain from this asset<br><br><b>T1568.002 - Dynamic Resolution: Domain Generation Algorithms</b><br> ↳ <b>A-DNS-DGADOM-QUERY</b>: DNS query for DGA domain from this asset |        |