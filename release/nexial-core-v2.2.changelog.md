---
layout: default
title: nexial-core 2.2 (2019-05-??)
parent: release
tags: release nexial-core 2.2
comments: true
---

### <a href="https://github.com/nexiality/nexial-core/releases/tag/nexial-core-2.2" class="external-link" target="_nexial_link">Release 2.2</a>
2019-05-??


### General
#### Fixes
 
#### Improvements


### Project Inspector


### System Variables


### Nexial Expression
- fix the storage of large decimal numbers when using `[NUMBER(...) => ...]` expression. The previous scientific 
  representation has been replaced with plain numeric representation.
- [`CSV(...) => sortAscending`](../expressions/CSVexpression#sortascendingcolumn) and 
  [`CSV(...) => sortDescending`](../expressions/CSVexpression#sortdescendingcolumn) now supports both numeric and 
  textual sorting, depending on the target column data.


### [base commands](../commands/base)


### [csv commands](../commands/csv)
- [CSV &raquo; `toExcel`](../commands/csv/toExcel): **NEW** command to export CSV content into new/existing Excel file.


### [desktop commands](../commands/desktop)


### [io commands](../commands/io)


### [rdbms commands](../commands/rdbms)


### [number commands](../commands/number)


### [web commands](../commands/web)
- [`assertElementsPresent(prefix)`](../commands/web/assertElementsPresent(prefix)): improved logging.


### [xml commands](../commands/xml)