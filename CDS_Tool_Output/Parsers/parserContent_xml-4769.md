#### Parser Content
```Java
{
Name = xml-4769
    Vendor = Microsoft
    Product = Microsoft Windows
    Lms = ElasticSearch
    DataType = "windows-4769"
    TimeFormat = "yyyy-MM-dd'T'HH:mm:ss"
    Conditions = ["<EventID>4769</EventID>", "<Data Name='ServiceName'>"]
    Fields = [
      """SystemTime=\'({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\d)""",
      """({event_name}A Kerberos service ticket was requested)""",
      """<Computer>({host}[^<]+)</Computer>""",
      """<EventID>({event_code}[^<]+)</EventID>""",
      """<Data Name='Status'>({result_code}[^<]+)</Data>""",
      """<Data Name='ServiceName'>({dest_host}[^<]+\$)</Data>""",
      """<Data Name='ServiceName'>({service_name}[^<]+)</Data>""",
      """<Data Name='TicketOptions'>({ticket_options}[^<]+)</Data>""",
      """<Data Name='TicketEncryptionType'>({ticket_encryption_type}[^<]+)</Data>""",
      """<Data Name='TargetUserName'>(?=\w)({user}[^<@\s]+)</Data>""",
      """<Data Name='TargetUserName'>(?=\w)({user_email}[^<@\s]+@[^<@\s]+)</Data>""",
      """<Data Name='TargetDomainName'>(?=\w)({domain}[^<]+)</Data>""",
      """<Data Name='IpAddress'>(::[\w]+:)?(::1|({src_ip}[a-fA-F:\d.]+))"""
    ]
  }
```