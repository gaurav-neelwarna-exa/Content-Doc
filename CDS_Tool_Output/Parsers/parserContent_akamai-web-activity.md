#### Parser Content
```Java
{
Name = akamai-web-activity
  Vendor = Cloud Akamai
  Product = Cloud Akamai
  Lms = Direct
  DataType = "web-activity"
  IsHVF = true
  TimeFormat = "epoch_sec"
  Conditions = [ """"message":{"""", """"reqHost":"""", """"status":"""", """"reqPath":"""" ]
  Fields = [
    """exabeam_host=([^=]+@\s*)?({host}\S+)""",
    """"start":"({time}\d+)""",
    """"proto":"({protocol}[^"]+)""",
    """"status":"({result_code}\d+)""",
    """"cliIP":"({src_ip}[A-Fa-f:\d.]+)""",
    """"reqPort":"({dest_port}\d+)""",
    """"reqHost":"({web_domain}[^"\s]+)""",
    """"reqHost":"[^"\s]*?({top_domain}[^\/\.\s]+(?i)(\.(com|net|info|edu|org|gov|co|jp|ru|de|ir|it|in|fr|info|pl|nl|es|gr|cz|eu|tv|me|jp|ca|cn|uk|my|cc|id|us|nz|biz|club|io|gg|fi|au|st|tw|asia|sg|ie|li|za))+)""",
    """"reqMethod":"({method}[^"]+)""",
    """"reqPath":"({uri_path}[^"]+)""",
    """"reqQuery":"({uri_query}[^"]+)""",
    """"edgeIP":"({dest_ip}[A-Fa-f:\d.]+)""",
    """"bytes":"({bytes}\d+)""",
  ]
}
```