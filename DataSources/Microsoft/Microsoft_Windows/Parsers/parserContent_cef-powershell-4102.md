#### Parser Content
```Java
{
Name = cef-powershell-4102
  Vendor = Microsoft
  Product = Microsoft Windows
  Lms = Splunk
  DataType = "process-created"
  TimeFormat = "yyyy-MM-dd'T'HH:mm:ss"
  Conditions = [ """CEF: """, """|Microsoft|PowerShell|""", """|Microsoft-Windows-PowerShell:4102|""" ]
  Fields = [
    """({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\d)""",
    """\sduser=(SYSTEM|({user}[^\s]+))\s""",
    """\sahost=({host}[^\s]+)\s""",
    """\sad.ProcessID=({pid}[^\s]+)\s""",
    """\|Microsoft-Windows-PowerShell:4102\|({additional_info}[^|]+)\|""",
  ]
}
```