#### Parser Content
```Java
{
Name = s-sep-mobile-alert-3
  Conditions = [ """"type":"Network"""" , """current_risk_warnings""", """health_status""", """mdm_status""", """"current_health_warnings""" ]
  Fields = ${SymantecParserTemplates.s-sep-mobile-alert.Fields}[
    """"severity":\s*"({alert_severity}[^"]+)".+?"id":\s*({alert_id}\d+)""",
    """"type":\s*"({alert_type}[^"]+)""",
  ]
}
```