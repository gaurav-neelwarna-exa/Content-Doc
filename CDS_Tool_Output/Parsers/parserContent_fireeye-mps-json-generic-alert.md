#### Parser Content
```Java
{
Name = fireeye-mps-json-generic-alert
    Vendor = FireEye
    Product = FireEye Network Security (NX)
    Lms = Splunk
    DataType = "alert"
    TimeFormat = "yyyy-MM-dd HH:mm:ss"
    Conditions = [""""msg": """",""""product": "Web MPS"""",""""alert": {"""]
    Fields = [
            """"appliance": "({host}[^"]+)"""",
            """"src":\s\{\s*(?:"\w+": "[^"]+",\s*)*"ip": "({src_ip}[^"]+)"""",
            """"src":\s\{\s*(?:"\w+": "[^"]+",\s*)*"host": "({src_host}[^"]+)"""",
    """"explanation":\s\{\s*(?:"\w+": "[^"]+",\s*)*"({alert_type}[^"]+)": \{\s*[^\{]+\{\s*(?:"\w+": "[^"]+",\s*)*"name": "({alert_name}[^"]+)"""",
            """"severity": "({alert_severity}[^"]+)"""", 
        """"occurred": "({time}\d{4}-\d{2}-\d{2} \d{2}:\d{2}:\d{2})""",
    """"id": "({alert_id}[^"]+)","""
    ]
    SOAR {
        IncidentType = "malware"
        DupFields = ["time->startedDate", "vendor->source", "rawLog->sourceInfo", "alert_name->malwareName", "alert_id->sourceId", "alert_type->malwareCategory", "alert_severity->sourceSeverity", "src_host->malwareVictimHost"]
        NameTemplate = """FireEye Alert ${alert_name} found"""
        ProjectName = "SOC"
        EntityFields = [
          {EntityType="device", Name="src_address", Fields=["src_ip->ip_address", "src_host->host_name"]}
        ]
  }
}
```