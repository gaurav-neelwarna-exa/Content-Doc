#### Parser Content
```Java
{
Name = unix-failed-logon-7
  Vendor = Unix
  Product = Unix
  Lms = Direct
  DataType = "failed-logon"
  TimeFormat = "yyyy-MM-dd HH:mm:ss"
  Conditions = [ """Disconnecting: Too many authentication failures for""" ]
  Fields = [
    """exabeam_time=({time}\d\d\d\d-\d\d-\d\d \d\d:\d\d:\d\d)""",
    """({host}[\w.\-]+)\s+sshd\[""",
    """({event_name}Too many authentication failures for ({user}\S+))""",
  ]
}
```