#### Parser Content
```Java
{
Name = huawei-firewall
  Vendor = Huawei
  Product = Enterprise Network Firewall
  Lms = Direct
  DataType = "network-connection"
  TimeFormat = "yyyy/MM/dd HH:mm:ss"
  Conditions = ["""rule-name=""" , """vsys=""" , """destination-ip""" , """POLICY/""" , """/POLICY"""]
  Fields = [
    """time=({time}\d\d\d\d\/\d+\/\d+\s*\d\d:\d\d:\d\d)"""
    """\s({host}[^\s]+)\s%""",
    """%*\d*POLICY\/\d\/POLICY({outcome}\w+)""",
    """protocol=({protocol}[^,]+)""",
    """source-ip=({src_ip}[^,]+)""",
    """source-port=({src_port}[^,]+)""",
    """destination-ip=({dest_ip}[^,]+)""",
    """destination-port=({dest_port}[^,]+)""",
    """rule-name=({rule}[^.]+)"""
  ]
}

${HUAWEIParserTemplates.huawei-ids}{
  Name = huawei-ids
  Conditions = ["""SignName=""" , """SignId=""" , """Os=""" ,  """IPS/"""]
}
```