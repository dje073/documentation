---
layout: default
title: nexial-core 2.5 (2019-08-??)
parent: release
tags: release nexial-core 2.5
comments: true
---

### <a href="https://github.com/nexiality/nexial-core/releases/tag/nexial-core-v2.4_???" class="external-link" target="_nexial_link">Release 2.5</a>
2019-08-??


### General
#### Fixes
- clarify error message when screenshot cannot be taken
- clarify error message when Nexial Expression cannot be properly evaluated due to data error
- reduce duplicated error messages to streamline console logging
- avoid console pause when executing in zero-touch environment (like unit testing or Jenkins)
- capture screenshot image file as `nexial.lastScreenshot` for `desktop` commands
- Fixed variable list indexing issue for the files.
- Fixed exception found when capturing screenshot within a 
  [base &raquo; `repeatUntil(steps,maxWaitMs)`](../commands/base/repeatUntil(steps,maxWaitMs)) loop.
- reduce duplicate 3rd-party libraries.

#### Improvements
- add jenkins env. variables in execution summary
- create alternative screen capture capability in case we can't capture screen via WebDriver of Winium driver
- add `artifact/bin` as part of creating a project structure via `nexial-project` script.


### [System Variables](../systemvars/)


### [Nexial Expression](../expressions)
- [JSON &raquo; `keys(jsonpath)`](../expressions/JSONexpression#keysjsonpath): extract immediate keys of resolved JSON 
  fragment based on `jsonpath`.


### [Flow Control](../flowcontrols)
- [`has file-size`](../flowcontrols/filter#description): now support non-existent file via `has file-size 0` syntax.


### [base commands](../commands/base)
- console output changes/improvements over multiple assert commands. Now FAILed assertion will display multi-line 
  output that should be easier to decipher.


### [csv commands](../commands/csv)


### [desktop commands](../commands/desktop)
- [`typeKeys(os,keystrokes)`](../commands/desktop/typeKeys(os,keystrokes)): fixed the simulation of certain "symbol" 
  keystrokes. This enables the typing of fully qualified file path that contains slashes (`\` or `/`) and colons (`:`).
- ensure Winium driver and `notifu.exe` are not executed in non-Windows environment.
- [`typeKeys(os,keystrokes)`](../commands/desktop/typeKeys(os,keystrokes)): support UPPERCASE typing.
- [`typeKeys(os,keystrokes)`](../commands/desktop/typeKeys(os,keystrokes)): support non-alphanumeric symbol typing.
- [`typeKeys(os,keystrokes)`](../commands/desktop/typeKeys(os,keystrokes)): _EXPERIMENTAL_ speeding up key-typing by
  removing any between-keys delay and waits.
- [`mouseWheel(amount,modifiers,x,y)`](../commands/desktop/mouseWheel(amount,modifiers,x,y)): **NEW** command to 
  simulate mouse wheel movement. `amount` as negative value means to scroll _backwards_.
- [`clickScreen(button,modifiers,x,y)`](../commands/desktop/clickScreen(button,modifiers,x,y)): **NEW** command to
  simulate mouse click based on current screen (not AUT).
- [`clickScreen(button,modifiers,x,y)`](../commands/desktop/clickScreen(button,modifiers,x,y)): support simple 
  "position" words for `x` and `y`.
- [`mouseWheel(amount,modifiers,x,y)`](../commands/desktop/mouseWheel(amount,modifiers,x,y)): support simple "position" 
  words for `x` and `y`.
- [`mouseWheel(amount,modifiers,x,y)`](../commands/desktop/mouseWheel(amount,modifiers,x,y)): restrict to Windows for now.
- [`typeKeys(os,keystrokes)`](../commands/desktop/typeKeys(os,keystrokes)): support the use of `*` for `os`.


### [io commands](../commands/io)


### [image commands](../commands/image)


### [json commands](../commands/json)
- [`storeKeys(json,jsonpath,var)`](../commands/json/storeKeys(json,jsonpath,var)): extract immediate keys of resolved 
  JSON fragment based on `jsonpath`.


### [ws commands](../commands/ws)
- fix URL by replacing special characters (like space and `&`) with the appropriate encoding.


### [web commands](../commands/web)
- [`saveText(var,locator)`](../commands/web/saveText(var,locator)): clarify output message when no text is saved due 
  to invalid or missing locator.
- Selenium-backed error messages are shorten to just the first line when possible to streamline error messages.
- honor [`nexial.delayBrowser`](../systemvars/index#nexial.delayBrowser) between plan steps so that Nexial won't 
  inadvertently load webdriver before necessarily.
- support screen capturing using native approach so that we can capture JavaScript dialog/popup or other native dialogs 
  (such as "Open File" and "Save As"). This is also the screen capturing alternative when the specific WebDriver fails.


### [xml commands](../commands/xml)