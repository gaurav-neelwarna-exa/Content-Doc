#### Parser Content
```Java
{
Name = cef-mcafee-epo-alert-1
  Vendor = McAfee
  Product = McAfee Endpoint Security
  Lms = ArcSight
  DataType = "alert"
  TimeFormat = "epoch"
  Conditions = [ """CEF""", """|McAfee|Rogue System Sensor|""", """|Rogue System|""", """Detected Rogue System""" ]
  Fields = [
    """\Wrt=({time}\d+)""",
    """\Wagt=({host}.+?)\s+(\w+=|$)""",
    """\Wcs6=({additional_info}.+?)\s+(\w+=|$)""",
    """\Wdhost=({dest_host}[\w\-.]+)""",
    """\Wdst=(0.0.0.0|({dest_ip}[A-Fa-f:\d.]+))""",
    """\Wcs4=({os}.+?)\s+(\w+=|$)""",
    """\Wseverity=({alert_severity}.+?)\s+(\w+=|$)""",
    """\WcategoryTechnique=({threat_category}.+?)\s+(\w+=|$)""",
    """CEF:([^\|]*\|){4}({alert_name}[^\|]+)""",
    """CEF:([^\|]*\|){5}({alert_type}[^\|]+)""",
  ]
}
```