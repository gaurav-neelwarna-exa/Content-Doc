#### Parser Content
```Java
{
Name = secureauth-auth-successful
    Vendor = SecureAuth
    Lms = ArcSight
    DataType = "authentication-successful"
    TimeFormat = "epoch"
    Conditions = [ """|SecureAuth|""","""|ID20990|Success|"""]
    Fields = [
        """\srt=({time}\d+)""",
        """\sdvc=({host}\d{1,3}\.\d{1,3}\.\d{1,3}\.\d{1,3})""",
        """\sflexString1=({host}[^\s]+)""",
        """\ssrc=({src_ip}\d{1,3}\.\d{1,3}\.\d{1,3}\.\d{1,3})""",
        """\ssuser=({user}.+?)\s+\w+=""",
        """requestClientApplication=(?:-|({browser}[\w\-]+))""",
        """requestClientApplication=(?:-|({browser}[\w\-]+)\/[\d\._]+)""",
        """requestClientApplication=(?:-|({browser}[^\/]+).+({os}iOS|Android|BlackBerry|iPhone OS|Windows Phone|BeOS|(?:W|w)indows|(?:L|l)inux|(?:M|m)acintosh|(?:D|d)arwin))""",
        """requestClientApplication=(?:-|Mozilla\/.+\(({os}iOS|Android|BlackBerry|Windows Phone|BeOS|(?:X|x)11|(?:W|w)indows|(?:L|l)inux|(?:M|m)acintosh|(?:D|d)arwin).+?({browser}Chrome|Safari|Opera|(?:F|f)irefox|MSIE|Trident))""",
        """requestClientApplication=(?:-|Mozilla\/.+\((?:BeOS|(?:X|x)11|(?:W|w)indows|(?:L|l)inux|(?:M|m)acintosh|(?:D|d)arwin).+Gecko\/\d+\s+({browser}\w+))"""
    ]
  }
```