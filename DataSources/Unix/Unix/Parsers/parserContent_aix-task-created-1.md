#### Parser Content
```Java
{
Name = aix-task-created-1
  Vendor = Unix
  Product = Unix
  Lms = Splunk
  DataType = "task-created"
  TimeFormat = "yyyy-MM-dd HH:mm:ss"
  Conditions = [ """) CMD (""", """ CRON[""", """]: (""" ]
  Fields = [
    """exabeam_host=([^=]+@\s*)?({host}\S+)""",
    """exabeam_time=({time}\d\d\d\d-\d\d-\d\d \d\d:\d\d:\d\d)""",
    """\w+\s+\d+\s+\d\d:\d\d:\d\d\s+({host}[\w\-.]+)""",
    """\(({user}[^\)]+)\) CMD""",
    """\sCMD\s+\(({task_name}[^\s\)]+)""",
    """\sCMD \(\s*({command_line}[^\)]+)\)""",
  ]
}
```