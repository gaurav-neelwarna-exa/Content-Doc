#### Parser Content
```Java
{
Name = fortinet-network-alert-1
  Vendor = Fortinet
  Product = Fortinet UTM
  Lms = Direct
  DataType = "network-alert"
  TimeFormat = "yyyy-MM-dd' time='HH:mm:ss"
  Conditions = [ """subtype="ips"""", """action=""", """service=""", """hostname=""" ]
  Fields = [
    """\Wdate=({time}\d\d\d\d-\d\d-\d\d time\=\d\d:\d\d:\d\d)""",
    """\Wdevname="?({host}[^"]+?)"?(\s+\w+=|\s*$)""",
    """\Wprofile="({alert_type}[^"]+)"""",
    """\Wsrcip=({src_ip}[a-fA-F\d.:]+)""",
    """\Wdstip=({dest_ip}[a-fA-F\d.:]+)""",
    """\Wseverity="?({alert_severity}\w+)""",
    """\Wsrcport=({src_port}\d+)""",
    """\Wdstport=({dest_port}\d+)""",
    """\Wservice="?({protocol}\w+)""",
    """\Wuser="({user}[^"]+)"""",
    """\Wattack="({alert_name}[^"]+)"""",
    """\Wmsg="({additional_info}[^"]+)"""",
    """\Waction="({action}[^"]+)"""",
  ]
}
```