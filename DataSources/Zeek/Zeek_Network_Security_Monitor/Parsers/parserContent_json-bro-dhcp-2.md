#### Parser Content
```Java
{
Name = json-bro-dhcp-2
  Product = Zeek Network Security Monitor
  DataType = "dhcp"
  Conditions = [ """client_addr":""", """"duration":""", """"msg_types":"""]
  Fields = ${BroParserTemplates.json-bro-activity.Fields}[
    """"host_name":"({host}[^"]+)""",
    """"client_addr":"({assigned_ip}\d+.\d+.\d+.\d+)""",
    """"domain":"({domain}[^"]+)""",
    """"duration":({duration}[^\}]+)""",
  ]
}
```