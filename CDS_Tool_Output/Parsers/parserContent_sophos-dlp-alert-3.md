#### Parser Content
```Java
{
Name = sophos-dlp-alert-3
  Vendor = Sophos
  Product = Sophos Endpoint Protection
  Lms = Direct
  DataType = "dlp-alert"
  TimeFormat = "yyyy-MM-dd'T'HH:mm:ss.SSSZ"
  Conditions = [ """"Event::Endpoint::WindowsFirewall::Blocked"""" ]
  Fields = [
    """exabeam_host=([^=]+@\s*)?({host}[^\s]+)""",
    """"location":"({host}[\w\-.]+)"""",
    """"rt":\s*"({time}\d\d\d\d\-\d\d\-\d\dT\d\d:\d\d:\d\d\.\d\d\dZ)""",
    """"name":\s*"({alert_name}[^:"]+)(:\s({target}[^"]+))?"""",
    """"name":\s*"({additional_info}[^"]+)""",
    """"type":\s*"({alert_type}[^"]+)""",
    """"dhost":\s*"({src_host}[^"]+)""",
    """"severity":\s*"({alert_severity}[^"]+)""",
    """"(suser|source)":\s*"(n\/a|(({domain}[^\\"]+)\\+)?({user_fullname}[^\\\(\)\s",]+\s+[^\\\(\)",]+))"""",
    """"(suser|source)":\s*"(n\/a|({user_lastname}[^",\s]+),\s*({user_firstname}[^,"\s]+))""",
    """"(suser|source)":\s*"(n\/a|(([^\\\s"]*\s+[^\\"]*|({domain}[^\\"]+))\\+)?({user}[^\\\s"]+))"""",
    """"source_info":\s*\{[^\}]*?"ip":\s*"({src_ip}[A-Fa-f:\d.]+)""",
    """"id":\s*"({alert_id}[^"]+)""",
  ]
}
```