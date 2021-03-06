#### Parser Content
```Java
{
Name = s-xml-4656-netapp
   Vendor = Microsoft
   Product = NetApp
   Lms = Splunk
   DataType = "file-operations"
   TimeFormat = "yyyy-MM-dd'T'HH:mm:ss"
   Conditions = [  """<EventID>4656</EventID>""",   """SubjectUserSid""",       """NetApp-Security-Auditing"""    ]
   Fields = [
      """<TimeCreated SystemTime="+({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\d)""",
      """<Computer>([^<>]+?[\\\/]+)?({host}[^<>]+)<\/Computer>""",
      """<EventID>({event_code}[^<]+)<\/EventID>""",
      """<EventName>({alert_name}[^<]+)<\/EventName>""",
      """<Result>({outcome}[^<]+)<\/Result>""",
      """<Data Name="*SubjectIP.+?>({src_ip}[A-Fa-f\d:.]+)<\/Data>""",
      """<Data Name="*SubjectUserSid"*>({user_sid}[^<]+)<\/Data>""",
      """<Data Name="*SubjectDomainName"*>({domain}.+?)<\/Data>""",
      """<Data Name="*SubjectUserName"*>({user}.+?)<\/Data>""",
      """<Data Name="*ObjectServer"*>({object_server}.+?)<\/Data>""",
      """<Data Name="*ObjectType"*>({object_class}.+?)<\/Data>""",
      """<Data Name="*ObjectName"*>({file_path}.+?)<\/Data>""",
      """<Data Name="*ObjectName"*>[^<]+[\\\/]+({file_name}(?:[^<\\\/:]+?)(\.({file_ext}\w+))?|[^\\:<]+)</Data>""",
      """<Data Name="*ObjectName"*>({file_parent}.+?)[\\\/]+(?:[^\\\/]+?)</Data>""",
      """<Data Name="*ProcessName"*>({process}({directory}(?:[^<]+)?[\\\/])?({process_name}[^\\\/"<]+?))</Data>""",
      """<Data Name="*(HandleID|HandleId)"*>({object_id}.+?)<\/Data>""",
      """<Data Name="*DesiredAccess"*>\s*({accesses}.+?)\s*<\/Data>"""
   ]
    DupFields = ["event_name->activity", "object_class-> alert_type"]
}
```