#### Parser Content
```Java
{
Name = cef-unix-su
  Vendor = Unix
  Lms = ArcSight
  DataType = "unix-account-switch"
  TimeFormat = "epoch"
  Conditions = [ """|Unix|Unix|""", """|session opened|""", """cs1=su """ ]
  Fields = [
    """\srt=({time}\d+)""",
    """\sduser=({user}.+?)\s+\w+=""",
    """\sdst=({dest_ip}\d{1,3}\.\d{1,3}\.\d{1,3}\.\d{1,3})""",
    """\sdhost=({dest_host}[^\s]+)""",
    """session opened for user ({account}.+?) by""",
    """session opened for user.+?by ({user}[^(]+)""",
    """\(uid\\+=({user_uid}\d+)\)""",
    """({event_code}su)"""
  ]
  DupFields = [ "dest_host->host"]
}
```