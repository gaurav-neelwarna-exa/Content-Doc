#### Parser Content
```Java
{
Name = cef-salesforce-app-activity-31
  Vendor = Salesforce
  Lms = ArcSight
  DataType = "app-activity"
  TimeFormat = "yyyy-MM-dd'T'HH:mm:ss.SSSZ"
  Conditions = [ """Action\=changedpassword;""", """Sales Cloud""" ]
  Fields = [
    """exabeam_host=([^=]+@\s*)?({host}\S+)""",  
    """CreatedDate\\=({time}\d\d\d\d\-\d\d\-\d\dT\d\d:\d\d:\d\d\.\d\d\dZ)""",
    """CreatedBy\.Username\\=({user_email}[^\s;]+)""",
    """Action\\=({activity}[^;]+)""",
    """duser=({target}[^\\\s]+)""",
    """({app}Sales Cloud)""",
  ]
  DupFields = [ "user_email->user" ]
}
```