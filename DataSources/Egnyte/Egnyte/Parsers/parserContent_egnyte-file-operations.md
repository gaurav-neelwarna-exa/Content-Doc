#### Parser Content
```Java
{
Name = egnyte-file-operations
  Vendor = Egnyte
  Product = Egnyte
  Lms = Direct
  DataType = "file-operations"
  IsHVF = true
  TimeFormat = "yyyy-MM-dd'T'HH:mm:ssZ"
  Conditions = [ """"file/folder":"""", """"target_path":"""", """"transaction":"""" ]
  Fields = [
    """exabeam_host=({host}[\w.\-]+)""",
    """"username":"({user_fullname}[^"\(\)]+?)\s*\(\s*({user_email}[^"\(\)]+?)\s*\)""",
    """"file/folder":"({file_path}({file_parent}[^"]*?[\\\/]+)({file_name}[^"\\\/]+?(\.({file_ext}[^"\.\\\/]+))?))\s*"""",
    """"transaction":"({accesses}[^"]+)""",
    """"target_path":"(N/A|({object}[^"]+))""",
    """"time":"({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\dZ)""",
    """"access":"({service}[^"]+)""",
    """"ip_address":"({src_ip}[^"]+)"""
  ]
}
```