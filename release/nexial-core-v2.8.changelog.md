---
layout: default
title: nexial-core 2.8 (2019-11-??)
parent: release
tags: release nexial-core 2.8
comments: true
---

### <a href="https://github.com/nexiality/nexial-core/releases/tag/nexial-core-v2.8_????" class="external-link" target="_nexial_link">Release 2.8</a>
2019-11-??


### General
#### Fixes
- [`nexial-project-inspector`](../userguide/BatchFiles#nexial-project-inspector): code fix to consider encrypted data 
  variables. Also minor update to inspector report (HTML).

#### Improvements
- Code change to omit the writing or creation of cells when there isn't data to display. In other words, display 
as much of the actual content as possible in output file.

### [System Variable](../systemvars)


### [Nexial Interactive](../interactive)


### [Built-in Functions](../functions)
- [`$(execution|plan|name)`](../functions/$(execution)#): **NEW** function to reveal the plan file name currently in 
  execution.
- [`$(execution|plan|fullpath)`](../functions/$(execution)#): **NEW** function to reveal the fully qualified path for 
  the plan currently in execution.
- [`$(execution|plan|index)`](../functions/$(execution)#): **NEW** function to reveal the plan step (i.e. row number) 
  of the plan currently in execution.


### [Nexial Expression](../expressions)
- [JSON &raquo; `keys(jsonpath)`](../expressions/JSONexpression#keysjsonpath): code fix to extract JSON keys correctly. 
- [JSON &raquo; `pack`](../expressions/JSONexpression#pack): code fix to enforce JSON beautification after "packing".
- [TEXT &raquo; `extract(beginRegex,endRegex,inclusive)`](../expressions/TEXTexpression#extractbeginregexendregexinclusive): 
  **NEW** operation to extract all instances of text between two regex-based patterns as a LIST expression.


### [base commands](../commands/base)
- [`repeatUntil(steps,maxWaitMs)`](../commands/base/repeatUntil(steps,maxWaitMs)): add console output when exception 
  is thrown.


### [csv commands](../commands/csv)


### [external commands](../commands/external)


### [image commands](../commands/image)
 

### [io commands](../commands/io)


### [json commands](../commands/json)


### [rdbms commands](../commands/rdbms)


### [ws commands](../commands/ws)
- [`nexial.ws.logDetail`](../systemvars/index#nexial.ws.logDetail): set `true` to log the detail for each web service
  call.
- [`nexial.ws.logSummary`](../systemvars/index#nexial.ws.logSummary): set `true` to log the summary of each web service
  call.
- code fix to parse empty cookie in response header.
- added `.ttfb` property to the response of web service call (e.g. ``${response}.ttfb`).
- added `.requestTime` property to the Response of web service call (e.g. `${response}.requestTime`).
- ensure the specified response data variable is cleared out prior to web service call, thus preventing previously 
  derived response to be used.


### [web commands](../commands/web)
- [Browser Performance Metrics](../commands/web/browsermetrics): **NEW** option to create chart.
- [`saveSelectedText(var,locator)`](../commands/web/saveSelectedText(var,locator)): **NEW** command store the text of 
 selected option from `single select or multi-select` element.
- [`saveSelectedValue(var,locator)`](../commands/web/saveSelectedValue(var,locator)): **NEW** command store the value
 (equivalent to the "value" attribute) of selected option from `single select or multi-select` element.
- [`nexial.browser.userData`](../systemvars/index#nexial.browser.userData): **NEW** System variable to specify browser 
  profile directory.