#### Parser Content
```Java
{
Name = s-aws-netflow-connection
  Vendor = AWS CloudWatch
  Product = AWS CloudWatch
  Lms = Splunk
  DataType = "netflow-connection"
  TimeFormat = "epoch"
  Conditions = [ """ eni-""", """ ACCEPT OK""", """aws:cloudwatchlogs:vpcflow""" ]
  Fields = [
    """exabeam_host=([^=]+@\s*)?({host}\S+)""",
    """({account_id}\S+) ({interface_id}\S+) ({src_ip}[A-Fa-f:\d.]+) ({dest_ip}[A-Fa-f:\d.]+) ({src_port}\d+) ({dest_port}\d+) ({protocol}\S+) ({packets}\S+) ({bytes}\d+) ({time}\d+) \S+ ({action}\S+) ({outcome}\S+)""",
  ]
}
```