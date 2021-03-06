#### Parser Content
```Java
{
Name = o365-activity
  Vendor = Microsoft
  Product = Office 365
  Lms = Direct
  DataType = "app-activity"
  TimeFormat = "yyyy-MM-dd'T'HH:mm:ss"
  Conditions = [ """"Workload""", """"ResultStatus""", """"Operation""" ]
  Fields = [
    """"CreationTime\\*"+:[\s\\]*"+({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\d)""",
    """exabeam_host=({host}[^\s]+)""",
    """\Wdvc=({host}\S+)""",
    """\Wdvchost=(Unknown|({host}[\w\-.]+))""",
    """"host\\*"+:[\s\\]*"+({host}[^"\\]+)""",
    """\Wact=({activity}.+?)\s+(\w+=|$)""",
    """"Operation\\*"+:[\s\\]*"+({activity}[^"\\\.]*)""",
    """"eid\\*"+:[\s\\]*"+(SecurityComplianceAlerts|({user_email}[^"@]+?@[^@"]+?)|({user}[^"]+?))\\*"""",
    """"UserId\\*"+:[\s\\]*"+(({domain}[^"\\]+)\\+)?(({user_email}[^\s"@]+@[^\s"@]+)|(SecurityComplianceAlerts|(Unknown|({user}[^"@\\\s]*))))"""",
    """"MailboxOwnerUPN\\*"+:[\s\\]*"+({user_email}[^"@\\]+@[^"@\\]+)""",
    """\ssuser=[^"@=\s]*?@([\.\w+]+\.)?({email_domain}[^\.\s"]+?\.[^\s"\.\\]+)""",
    """"UserId\\*"+:[\s\\]*"+({user_email}[^"\\@]+?@[^"\\\s@]+)""",
    """"UserId\\*"+:[\s\\"]*"+[^"]*?@([\.\w+]+\.)?({email_domain}[^\.\s"]+?\.[^\s"\.>]+)>?\s*"+""",
    """"UserId":"\\*"(?![^@"]+?@[^\s"]+)({domain}[^"\\\/]+)[^"]*?(Unknown|({user}[^"\\\/@\s]+))\\"""",
    """"MailboxOwnerUPN\\*"+:[\s\\]*"+({user_email}[^"\\\s@]+@[^"\\\s@]+)""",
    """"MailboxOwnerUPN\\*"+:[\s\\"]*"+[^"]*?@([\.\w+]+\.)?({email_domain}[^\.\s"]+?\.[^\s"\.>]+)>?\s*"+""",
    """"ResultStatus\\*"+:[\s\\]*"+({outcome}[^"\\]+)""",
    """"(Workload|Application|Client)\\*"+:[\s\\]*"+({app}[^"\\]*)""",
    """requestClientApplication=({app}.+?)\s+(\w+=|$)""",
    """"ObjectId\\*"+:"?[\s\\]*"+(Unknown|Not Available|({object}[^"\\]*))""",
    """"Client\\*"+:[\s\\]*"+({user_agent}[^"]*)""",
    """"UserAgent\\*"+:[\s\\]*"+({user_agent}.*?)\\*"+,""",
    """\{"+Name"+:[\s\\]*"+UserAgent"+,"+Value"+:"+({user_agent}[^"]+)"+\}""",
    """"+Value"+:\s*"+({user_agent}[^"]+)"+,\s*"+Name"+:[\s\\]*"+UserAgent"+\}
```