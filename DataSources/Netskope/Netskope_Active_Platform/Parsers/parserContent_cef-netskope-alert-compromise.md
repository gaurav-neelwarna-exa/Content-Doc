#### Parser Content
```Java
{
Name = cef-netskope-alert-compromise
  Vendor = Netskope
  Product = Netskope Active Platform
  Lms = Direct
  DataType = "alert"
  TimeFormat = "epoch_sec"
  Conditions = [ """CEF:""", """|Skyformation|""", """"alert_type":"Compromised Credential"""", """destinationServiceName=Netskope""", """|security-threat-detected|""", """"type":"breach"""" ]
 Fields = [
    """exabeam_host=([^=]+@\s*)?({host}\S+)""",
    """"timestamp":({time}\d+)""",
    """"user":"(({user_email}[^@"\s]+@[^@"\s]+)|(({domain}[^"@\\\/\s]+)[\\\/]+)?({user}[^"@\\\/\s]+))"""",
    """"_id":"({alert_id}[^"]+)""",
    """"category":"(n\/a|({threat_category}[^"]+))""",
    """"alert_type"+:"+({alert_name}[^"]+)""",
    """"hostname":"({src_host}[^"]+)""",
    """security-threat-detected\|({alert_severity}\d+)""",
    """"alert_name":"({additional_info}[^"]+)""",
    """"type":"({alert_type}[^"]+)""",
    """"user":"({from_user_at}[^"]+)"""",
    """"matched_username":"({shared_with_at}[^"]+)"""",
    """requestClientApplication=({site_at}[^=]+?)\s+\w+="""
  ]
  DupFields = [ "site_at->app" ]
}
```