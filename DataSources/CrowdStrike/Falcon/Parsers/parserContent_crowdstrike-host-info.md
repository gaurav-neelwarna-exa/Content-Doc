#### Parser Content
```Java
{
Name = crowdstrike-host-info
    Vendor = CrowdStrike
    Product = Falcon
    Lms = Direct
    DataType = "logon"
    TimeFormat = "epoch"
    Conditions = [ """"event_simpleName":"HostInfo"""", """"aid"""" ]
    Fields = [
      """"timestamp":"({time}\d+)""",
      """"+MachineDn"+:"+CN\\*(=|u003d)?({dest_host}[^,]+)""",   
      """"aid":"({aid}[^"]+)""",
      """"event_simpleName":"({event_code}[^"]+)""",
      """suser=(system|({user}[^\s]+))"""
    ]
    DupFields = [ "dest_host->host" ] 
  }
```