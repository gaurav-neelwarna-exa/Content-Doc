#### Parser Content
```Java
{
Name = sophos-dlp-alert-2
  Vendor = Sophos
  Product = Sophos Endpoint Protection
  Lms = Direct
  DataType = "dlp-alert"
  TimeFormat = "yyyy-MM-dd'T'HH:mm:ss.SSSZ"
  Conditions = [ """"Event::Endpoint::Application::Blocked"""", """"Controlled application blocked: """ ]
  Fields = [
    """exabeam_host=([^=]+@\s*)?({host}[^\s]+)""",
    """"location":"({host}[^"]+)""",
    """"when":"({time}\d\d\d\d\-\d\d\-\d\dT\d\d:\d\d:\d\d\.\d\d\dZ)""",
    """"rt":\s*"({time}\d\d\d\d\-\d\d\-\d\dT\d\d:\d\d:\d\d\.\d\d\dZ)""",
    """"name":\s*"({alert_name}[^:]+):\s({target}[^"]+)""",
    """"name":\s*"({additional_info}[^"]+)""",
    """"type":\s*"({alert_type}[^"]+)""",
    """"dhost":\s*"({src_host}[^"]+)""",
    """"severity":\s*"({alert_severity}[^"]+)""",
    """"suser":\s*"(?:n\/a|({user_fullname}[^"\\,]+))"""",
    """"suser":\s*"({user_lastname}[^",\s]+),\s*({user_firstname}[^,"\s]+)"""",
    """"suser":\s*"(({domain}[^\\",]+)\\+)?({user}[^",\\\/\s]+)"""",
    """"source":"({user_fullname}[^",]+)"""",
    """"source":"({user_lastname}[^",\s]+),\s*({user_firstname}[^,"\s]+)"""",
    """\\"source_info\\"__ip=({src_ip}[A-Fa-f:\d.]+)""",
    """"id":\s*"({alert_id}[^"]+)""",
  ]
  DupFields = [ "host->src_host" ]
}
```