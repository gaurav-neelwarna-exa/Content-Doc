#### Parser Content
```Java
{
Name = q-leef-ds-account-disabled
  Vendor = StealthBits
  Lms = QRadar
  DataType = "account-disabled"
  TimeFormat = "yyyy-MM-dd HH:mm:ss"
  Conditions = [  """LEEF:1.0|STEALTHbits|""","""cat=Account disabled""", """AttrOldValue=""", """Success=True""" ]
  Fields = [  
    """\d\d:\d\d:\d\d ({host}[\w\-.]+) LEEF""",
    """devTime=({time}\d\d\d\d\-\d\d\-\d\d \d\d:\d\d:\d\d)""",
    """src=({src_ip}\d{1,3}\.\d{1,3}\.\d{1,3}\.\d{1,3})""",
    """dst=({dest_ip}\d{1,3}\.\d{1,3}\.\d{1,3}\.\d{1,3})""",
    """usrName=(({domain}[^\\]+)\\)?({user}.+?)\s+\w+=""",
    """AffectedObject=(({target_domain}[^\\]+)\\)?({target_user}.+?)\s+\w+=""",
    """OrigServer=([^\\]+\\)?({dest_host}.+?)\s+\w+="""
  ]
    DupFields = [ "dest_host->host" ]
}
```