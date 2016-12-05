---
title: \ SetPPPrefix Preprocessor Directive
author: windows-driver-content
description: \ SetPPPrefix Preprocessor Directive
MS-HAID:
- 'gplfiles\_a9230076-94f8-4554-94ce-841758821e9d.xml'
- 'print.\_setppprefix\_preprocessor\_directive'
MSHAttr:
- 'PreferredSiteName:MSDN'
- 'PreferredLib:/library/windows/hardware'
ms.assetid: 3520aa66-1090-40db-9c9f-cfba0e6e2bee
keywords: ["preprocessor directives WDK GDL , keywords", "keywords WDK GDL", "reserved keywords WDK", "SetPPPrefix directive WDK GDL"]
---

# \#SetPPPrefix Preprocessor Directive


```
#SetPPPrefix: prefix
```

The \#SetPPPrefix directive makes the *prefix* value the current preprocessor prefix. *prefix* can be any token value and is required.

You can define the same prefix more than once. The prefix is user-selectable because it allows directives to be unambiguously distinguished from any existing not-to-be-processed data. The following code example shows how to change a prefix if a normal GDL entry contains a value that might be confused with an actual directive.

```
*%  assume current prefix is #
#SetPPPrefix: #Temp#
#Temp#Ifdef:  WINNT_60
*InfoMessage: "Use the Preprocessor Directive
#PreCompiled to make your GDL file sharable."
#Temp#Endif:  WINNT_60
#Temp#UndefinePrefix
*%  now back to normal # prefix.
```

 

 


--------------------
[Send comments about this topic to Microsoft](mailto:wsddocfb@microsoft.com?subject=Documentation%20feedback%20%5Bprint\print%5D:%20#SetPPPrefix%20Preprocessor%20Directive%20%20RELEASE:%20%289/1/2016%29&body=%0A%0APRIVACY%20STATEMENT%0A%0AWe%20use%20your%20feedback%20to%20improve%20the%20documentation.%20We%20don't%20use%20your%20email%20address%20for%20any%20other%20purpose,%20and%20we'll%20remove%20your%20email%20address%20from%20our%20system%20after%20the%20issue%20that%20you're%20reporting%20is%20fixed.%20While%20we're%20working%20to%20fix%20this%20issue,%20we%20might%20send%20you%20an%20email%20message%20to%20ask%20for%20more%20info.%20Later,%20we%20might%20also%20send%20you%20an%20email%20message%20to%20let%20you%20know%20that%20we've%20addressed%20your%20feedback.%0A%0AFor%20more%20info%20about%20Microsoft's%20privacy%20policy,%20see%20http://privacy.microsoft.com/default.aspx. "Send comments about this topic to Microsoft")

