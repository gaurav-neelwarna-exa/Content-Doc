#### Parser Content
```Java
{
Name = s-azura-pri-auth-failed
  Vendor = Azura
  Lms = Splunk
  DataType = "authentication-failed"
  TimeFormat = "epoch"
  Conditions = [ """pfsvc: Failed """, """ auth for """ ]
  Fields = [
    """exabeam_host=([^=]+@\s*)?({host}[^\s]+)""",
    """({host}[\w\.-]+)\s+pfsvc:""",
    """Failed\s+({auth_method}.+?)\s+auth for """,
    """\suser\s+'({user_dn}[^']+)' \(distinguishedName format\)""",
    """\suser\s+'({user}[^']+)'""",
    """Logon failure:\s*({failure_reason}.+?)(\s*\(|$)""",
  ]
}

${MFAParserTemplates.azure-mfa-auth}{
  Name = azure-mfa-auth-successful
  DataType = authentication-successful
  Conditions = [ """|pfsvc|""", """Pfauth succeeded for user""", """Call status:""" ]
}

${MFAParserTemplates.azure-mfa-auth}{
  Name = azure-mfa-auth-failed
  DataType = authentication-failed
  Conditions = [ """|pfsvc|""", """Pfauth failed for user""", """Call status:""" ]
}

{
  Name = cef-sonicwall-vpn-start
  Vendor = Sonicwall
  Lms = ArcSight
  DataType = "vpn-start"
  TimeFormat = "epoch"
  Conditions = [ """|Sonicwall|VPN|""", """|User login successful|"""]
  Fields = [
    """\srt=({time}\d+)""",
    """\sdvc=({host}\S+)""",
    """\sdvchost=({host}\S+)""",
    """\ssrc=({src_ip}\S+)""",
    """\sdst=({dest_ip}\S+)""",
    """\sdhost=({dest_host}\S+)""",
    """\sduser=(|({user}.+?))\s+(\w+=|$)""",
    """\scs5Label=Portal\s.*cs5=({realm}.+?)\s+(\w+=|$)""",
    """\scs5=({realm}.+?)\s+(|\w+=.*)cs5Label=Portal\s""",
  ]
}
```