#### Parser Content
```Java
{
Name = mcafee-network-alert
  Vendor = McAfee
  Product = McAfee Network Security Platform (IPS)
  DataType = network-alert
  Lms = Splunk
  TimeFormat = "yyyy-MM-dd HH:mm:ss"
  Conditions = ["""threat_source_ip_address""" , """McAfee Host Intrusion Prevention"""]
  Fields = [
    """"event_generated_time":"({time}\d\d\d\d-\d\d-\d\d\s\d\d:\d\d:\d\d)""",
    """"action_taken":"({outcome}[^"]+)"""", 
    """"detecting_product_ipv4_address":"({host}[^"]+)"""",
    """"detecting_product_host_name":"({host}[^"]+)"""",
    """"threat_source_ip_address":"({src_ip}[^"]+)"""",
    """"threat_target_ip_address":"({dest_ip}[^"]+)"""",
    """"threat_source_user_name":"({domain}[^\\]+)\\+({user}[^"]+)"""",
    """"threat_severity":"({alert_severity}[^"]+)"""",
    """"threat_source_process_name":"\w+:\\+([^\\"]+\\+)+({process_name}[^"]+)"""",
    """"signature_name_host_ips":"({alert_name}[^"]+)"""",
    """"event_description":"({alert_type}[^"]+)"""",
    """"threat_source_host_name":"({src_host}[^"]+)"""",
    """"event_category":"({alert_type}[^"]+)"""",
    """"threat_target_host_name":"({dest_host}[^"]+)"""",
    """"threat_type":"({additional_info}[^"]+)""""
  ]
}

{
  Name = cef-mcafee-dlp-email-alert
  Vendor = McAfee
  Product = McAfee Email Protection
  Lms = ArcSight
  DataType = "dlp-email-alert"
  TimeFormat = "epoch"
  Conditions = [ """CEF:""", """|McAfee|Secure Internet Gateway|""", """|smtp:Email Delivered|""" ]
  Fields = [
    """CEF:([^\|]*\|){4}({alert_name}[^\|]+)""",
    """\Wrt=({time}\d+)""",
    """\Wdvchost=({host}[\w\-.]+)""",
    """\WeventId=({alert_id}\d+)""",
    """\Wact=({outcome}.+?)\s+([\w\\]+=|$)""",
    """\Wshost=({src_host}[\w\-.]+)""",
    """\Wsrc=({src_ip}[A-Fa-f:\d.]+)""",
    """\WFrom\\=<({sender}[^\s>]+)""",
    """\WFrom\\=<[^@]+@({external_domain_sender}[^\s>]+)""",
    """\Wsize=({bytes}\d+)""",
    """\Wto\\=<({recipients}[^>]+)""",
    """\Wto\\=<({recipient}[^\s>,;]+)""",
    """\Wto\\=<[^@]+@({external_domain_recipient}[^\s>]+)""",
    """\Wsubject\\='({subject}[^']+)""",
    """\Wattachment\(s\)\\='(|({attachments}[^']+))'""",
    """\Wattachment\(s\)\\='(|({attachment}[^,']+)),""",
  ]
  DupFields = [ "alert_name->alert_type" ]
}
```