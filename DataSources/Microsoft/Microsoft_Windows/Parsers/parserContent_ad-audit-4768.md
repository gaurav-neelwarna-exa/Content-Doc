#### Parser Content
```Java
{
Name = ad-audit-4768
  Vendor = Microsoft
  Product = Microsoft Windows
  Lms = Direct
  DataType = "windows-4768"
  TimeFormat = "epoch_sec"
  Conditions = [ """ADAuditPlus""", """EVENT_NUMBER = 4768""" ]
  Fields = [
    """exabeam_host=([^=]+@\s*)?({host}[\w\-.]+)""",
    """TIME_GENERATED\s*=\s*({time}\d+)""",
    """({host}[\w\-.]+) ADAuditPlus""",
    """USERNAME\s*=\s*({user}[^\s\]@]+)\s*\]""",
    """USERNAME\s*=\s*({user_email}[^\s\]@]+@[^\s\]@]+)\s*\]""",
    """CLIENT_IP_ADDRESS\s*=\s*({dest_ip}[A-Fa-f:\d.]+)""",
    """DOMAIN\s*=\s*({domain}[^\\\/\]]+?)\s*\]""",
    """RECORD_NUMBER\s*=\s*({record_id}\d+)""",
    """EVENT_NUMBER\s*=\s*({event_code}\d+)""",
    """USER_SID\s*=\s*\%?\{?({user_sid}[^\}\s\]]+)""",
    """ERROR_CODE\s*=\s*({result_code}[^\s]+)""",
    """EVENT_TYPE_TEXT\s*=\s*({outcome}.+?)\s*\]""",
    """LOGON_SERVICE\s*=\s*(null|-|({service_name}[^\s\]]+))""",
    """TICKET_OPTIONS\s*=\s*(null|-|({ticket_options}[^\s\]]+))""",
    """TICKET_ENCRYPTION_TYPE\s*=\s*(null|-|({ticket_encryption_type}[^\s\]]+))""",
  ]
}
```