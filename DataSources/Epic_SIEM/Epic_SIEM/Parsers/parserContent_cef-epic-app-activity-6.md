#### Parser Content
```Java
{
Name = cef-epic-app-activity-6
  Product = Epic SIEM
  Conditions = [ """CEF:""", """|Epic|Security-SIEM|""", """|IC_SERVICE_AUDIT|""" ]
  Fields = ${EpicParserTemplates.cef-epic-app-activity.Fields} [
    """SERVICENAME=({object}.+?)\s+(\w+=|$)""",
  ]
}
```