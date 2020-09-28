#### Parser Content
```Java
{
Name = s-dtex
  Vendor = Dtex
  Product = DTEX InTERCEPT
  Lms = Splunk
  DataType = "dtex"
  IsHVF = true
  TimeFormat = "yyyy-MM-dd'T'HH:mm:ss"
  Conditions = [ "User_Department", "User_Location"]
  Fields = [
    """(?:[^,]*,){8}({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\d)?""",
    """(?:([^",]*,)){10}({activity_details}".+?"|[^,]+),""",
    """(?:[^,]*,){6}({activity}[^,]+)?""",
    """(?:[^,]*,){5}({activity_category}[^,]+)?""",
    """(?:([^",]*,)){10}(".+?"|[^,]*),(?:([^,]*,)){11}(({host_domain}[^\\]+)\\)?({host}[^,]+)?""",
    """(?:([^",]*,)){10}(".+?"|[^,]*),(?:([^,]*,)){13}({os_version}[^,]+)""",
    """(?:([^",]*,)){10}(".+?"|[^,]*),(?:([^,]*,)){15}({os_architecture}[^,]+)""",
    """(?:([^",]*,)){10}(".+?"|[^,]*),(?:([^,]*,)){16}({os_edition}[^,]+)""",
    """(?:([^",]*,)){10}(".+?"|[^,]*),(?:([^,]*,)){17}({os_type}[^,]+)""",
    """(?:([^",]*,)){10}(".+?"|[^,]*),(?:([^,]*,)){2}({domain}[^\\]+)\\({user}[^,]+)?""",
    """(?:([^",]*,)){10}(".+?"|[^,]*),(?:([^,]*,)){35}({bytes}[^,]+)?""",
    """(?:([^",]*,)){10}(".+?"|[^,]*),(?:([^,]*,)){19}({process_name}[^,]+)?""",
    """(?:([^",]*,)){10}(".+?"|[^,]*),(?:([^,]*,)){21}({directory}[^,]+)?""",
    """(?:([^",]*,)){10}(".+?"|[^,]*),(?:([^,]*,)){26}(".+?"|[^,]*),({url}[^,]+)?""",
    """(?:([^",]*,)){10}(".+?"|[^,]*),(?:([^,]*,)){26}(".+?"|[^,]*),(?:([^,]*,)){5}({src_file_dir}[^,]+)?""",
    """(?:([^",]*,)){10}(".+?"|[^,]*),(?:([^,]*,)){26}(".+?"|[^,]*),(?:([^,]*,)){6}({src_file_name}[^,]+)?""",
    """(?:([^",]*,)){10}(".+?"|[^,]*),(?:([^,]*,)){26}(".+?"|[^,]*),(?:([^,]*,)){7}({src_file_ext}[^,]+)?""",
    """(?:([^",]*,)){10}(".+?"|[^,]*),(?:([^,]*,)){26}(".+?"|[^,]*),(?:([^,]*,)){14}({file_parent}[^,]+)?""",
    """(?:([^",]*,)){10}(".+?"|[^,]*),(?:([^,]*,)){26}(".+?"|[^,]*),(?:([^,]*,)){15}({file_name}[^,]+)?""",
    """(?:([^",]*,)){10}(".+?"|[^,]*),(?:([^,]*,)){26}(".+?"|[^,]*),(?:([^,]*,)){16}({file_ext}[^,]+)?"""
  ]
  DupFields = [ "host->dest_host", "activity->accesses", "directory->process_directory" ]
}
```