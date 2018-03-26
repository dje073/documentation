---
title: json &raquo; storeValue(json,jsonpath,var)
parent: json
tags: command json jsonpath
comments: true
---
{% include _breadcrumb_command.html %}

### Description
This command stores the value of the matching element (or the first matching element) in `json` in `var`.  The matching
criteria is described in `jsonpath`.


### Parameters
- **json** - the JSON document or file
- **jsonpath** \- the path to describe the JSON element (or the first element) in question
- **var** - the variable name to store the matching value (or the first matching one)


### Example
**Book Store Data in JSON**<br/>
![bookStoreData](image/bookStoreData.png)

**Script**:<br/>
![script](image/storeValue_01.png)

**Result**:<br/>
![output](image/storeValue_02.png)
