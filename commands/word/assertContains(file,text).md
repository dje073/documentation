---
layout: default
title: assertContains(file,text)
parent: word
tags: command word password protection
comments: true
---


### Description
This command asserts that the specified Word `file` contains the specified `text`. Note to consider with care that the
text in question might not be a contiguous series of characters. At times additional spaces or tabs (use `(tab)`) might
need to be considered. In addition, this command searches for the presence of `text` in exact case (case-sensitively).


### Parameters
- **file** - the fully qualified path of the target Word document.


### Example


### See Also
- [`assertNotContain(file,text)`](assertNotContain(file,text))
- [`extractText(var,file)`](extractText(var,file))
