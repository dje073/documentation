---
layout: default
title: nexial-core 2.7 (2019-10-??)
parent: release
tags: release nexial-core 2.7
comments: true
---

### <a href="https://github.com/nexiality/nexial-core/releases/tag/nexial-core-v2.7_0???" class="external-link" target="_nexial_link">Release 2.7</a>
2019-10-??


### General
#### Fixes
- fixed code to support intra-execution changes of `nexial.scriptRef.*` data variables.

#### Improvements
- added checks to ensure that read-only variables aren't overwritten via commands affect data variables


### [Nexial Interactive](../interactive)


### [Built-in Functions](../functions)


### [Nexial Expression](../expressions)
- fix code to support negative number parsing
- [TEXT expression](../expressions/TEXTexpression): code fix to handle escaped delimiter (meaning same character as 
  [`nexial.textDelim`](../systemvars/index#nexial.textDelim))
- [`nexial.expression.resolveUrl`](../systemvars/index#nexial.expression.resolveUrl): change its default value to
  `false` to minimize impact to existing automation. This will impact some (likely small subset) of automation that
  utilize [TEXT expression](../expressions/TEXTexpression) to automate the fetching of HTTP-based resources.
- [TEXT &raquo; `xml`](../expressions/TEXTexpression#xml): **NEW** operation to transform a 
  [TEXT expression](../expressions/TEXTexpression) to a [XML expression](../expressions/XMLexpression).
- [TEXT &raquo; `json`](../expressions/TEXTexpression#json): **NEW** operation to transform a 
  [TEXT expression](../expressions/TEXTexpression) to a [JSON expression](../expressions/JSONexpression).


### [aws.vision commands](../commands/aws.vision)


### [base commands](../commands/base)


### [csv commands](../commands/csv)
- [`compareExtended`](../commands/csv/compareExtended(var,profile,expected,actual)): fix code to support negative 
  number parsing


### [desktop commands](../commands/desktop)


### [external commands](../commands/external)
- [`runProgram(programPathAndParams)`](../commands/external/runProgram(programPathAndParams)): support the execution 
  of sub-shell with parameterized commands (*NIX and Mac only). The parameterized command should be wrapped with single 
  quotes.
- [`runProgramNoWait(programPathAndParams)`](../commands/external/runProgramNoWait(programPathAndParams)): support 
  the execution of sub-shell with parameterized commands (*NIX and Mac only). The parameterized command should be 
  wrapped with single quotes.


### [image commands](../commands/image)


### [json commands](../commands/json)


### [localdb commands](../commands/localdb)


### [ws commands](../commands/ws)


### [web commands](../commands/web)
- [web &raquo; `closeAll`](../commands/web/closeAll()): A **NEW** System variable  
  [`nexial.browser.electron.forceTerminate`](../systemvars/index#nexial.browser.electron.forceTerminate) to forcefully 
  terminate the AUT executable - i.e. the electron application as specified via 
  [`nexial.browser.electron.appLocation`](../systemvars/index#nexial.browser.electron.appLocation) - after the 
  underlying chromedriver shuts down or when [web &raquo; `closeAll`](../commands/web/closeAll()) is invoked.
- [`saveDivsAsCsv(headers,rows,cells,nextPage,file)`](../commands/web/saveDivsAsCsv(headers,rows,cells,nextPage,file)):
  enable the use of `(null)`, `(empty)` or `(blank)` for `headers` and `nextPage` to omit the use of these parameters.
- [`saveTableAsCsv(locator,nextPageLocator,file)`](../commands/web/saveTableAsCsv(locator,nextPageLocator,file)):
  enable the use of `(null)`, `(empty)` or `(blank)` for `nextPage` to omit the use of this parameter.
- [`saveInfiniteDivsAsCsv(config,file)`](../commands/web/saveInfiniteDivsAsCsv(config,file)):
  enable the use of `(null)`, `(empty)` or `(blank)` for `header-cell` to omit the use of this `config`.
- [`saveInfiniteTableAsCsv(config,file)`](../commands/web/saveInfiniteTableAsCsv(config,file)):
  enable the use of `(null)`, `(empty)` or `(blank)` for `header-cell` to omit the use of this `config`.
