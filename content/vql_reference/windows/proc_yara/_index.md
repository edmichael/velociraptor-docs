---
title: proc_yara
index: true
noTitle: true
no_edit: true
---



<div class="vql_item"></div>


## proc_yara
<span class='vql_type pull-right page-header'>Plugin</span>



<div class="vqlargs"></div>

Arg | Description | Type
----|-------------|-----
rules|Yara rules|string (required)
pid|The pid to scan|int (required)
context|Return this many bytes either side of a hit|int
key|If set use this key to cache the  yara rules.|string

### Description

Scan processes using yara rules.

This plugin uses yara's own engine to scan process memory for the signatures.

{{% notice note %}}

Process memory access depends on having the [SeDebugPrivilege](https://support.microsoft.com/en-au/help/131065/how-to-obtain-a-handle-to-any-process-with-sedebugprivilege) which depends on how Velociraptor was started. Even when running as System, some processes are not accessible.

{{% /notice %}}


