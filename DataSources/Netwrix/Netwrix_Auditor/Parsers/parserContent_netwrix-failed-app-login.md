#### Parser Content
```Java
{
Name = netwrix-failed-app-login
  DataType = "failed-app-login"
  Conditions = [ """CEF:0|Netwrix|""", """|Failed Logon|""" ]
  Fields = ${NetWrixParserTemplates.netwrix-app-activity-2.Fields}[
    """CEF:0\|Netwrix\|(AD FS|Logon Activity|Self-audit)\|[^\|]+\|[^\|]+\|({activity}[^\|]+)\|""",
  ]
}
```