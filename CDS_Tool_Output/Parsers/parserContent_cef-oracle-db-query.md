#### Parser Content
```Java
{
Name = cef-oracle-db-query
  Vendor = Oracle
  Lms = ArcSight
  DataType = "database-query"
  IsHVF = true
  TimeFormat = "epoch"
  Conditions = [ """|Oracle|FGA|""", """|SELECT|""" ]
  Fields = [ 
    """exabeam_host=([^=]*@\s*)?({host}[^\s]+)""",
    """\|Oracle\|FGA\|([^\|]*\|){2}({db_operation}[^\|]+)""",
    """\WeventId=({event_id}\d+)""",
    """\Wmsg=\s*({db_query}([^\\=]|(\\\\)*\\=|\\)+)\s+(\w+=|$)""",
    """\Wrt=({time}\d+)""",
    """\Wshost=({src_host}[^\s]+)""",
    """\Wsuser=({user}[^\s]+)""",
    """\Wdhost=({dest_host}[^\s]+)""",
    """\Wduser=({db_user}[^\s]+)""",
    """\Wcs3=({database_name}[^\s]+)"""
  ]
  DupFields = ["db_user->account"]
}
```