---
title: Interoperability Warnings
ms.date: 11/04/2016
ms.topic: reference
f1_keywords:
  - "vs.codeanalysis.Interoperabilityrules"
helpviewer_keywords:
  - "managed code analysis warnings, interoperability warnings"
  - "interoperability warnings"
  - "warnings, interoperability"
ms.assetid: 95de6eb3-40c4-4063-9f59-25cb70e3b2b3
author: gewarren
ms.author: gewarren
manager: jillfra
ms.workload:
  - "multiple"
---
# Interoperability Warnings

Interoperability warnings support interaction with COM clients.

## In This Section

| Rule | Description |
| - | - |
| [CA1400: P/Invoke entry points should exist](../code-quality/ca1400.md) | A public or protected method is marked by using the System.Runtime.InteropServices.DllImportAttribute attribute. Either the unmanaged library could not be located or the method could not be matched to a function in the library. |
| [CA1401: P/Invokes should not be visible](../code-quality/ca1401.md) | A public or protected method in a public type has the System.Runtime.InteropServices.DllImportAttribute attribute (also implemented by the Declare keyword in Visual Basic). Such methods should not be exposed. |
| [CA1402: Avoid overloads in COM visible interfaces](../code-quality/ca1402.md) | When overloaded methods are exposed to COM clients, only the first method overload retains its name. Subsequent overloads are uniquely renamed by appending to the name an underscore character (_) and an integer that corresponds to the order of declaration of the overload. |
| [CA1403: Auto layout types should not be COM visible](../code-quality/ca1403.md) | A COM-visible value type is marked by using the System.Runtime.InteropServices.StructLayoutAttribute attribute set to LayoutKind.Auto. The layout of these types can change between .NET versions, which will break COM clients that expect a specific layout. |
| [CA1404: Call GetLastError immediately after P/Invoke](../code-quality/ca1404.md) | A call is made to the Marshal.GetLastWin32Error method or the equivalent [!INCLUDE[TLA2#tla_win32](../code-quality/includes/tla2sharptla_win32_md.md)] GetLastError function, and the immediately previous call is not to a platform invoke method. |
| [CA1405: COM visible type base types should be COM visible](../code-quality/ca1405.md) | A COM-visible type derives from a type that is not COM-visible. |
| [CA1406: Avoid Int64 arguments for Visual Basic 6 clients](../code-quality/ca1406.md) | Visual Basic 6 COM clients cannot access 64-bit integers. |
| [CA1407: Avoid static members in COM visible types](../code-quality/ca1407.md) | COM does not support static methods. |
| [CA1408: Do not use AutoDual ClassInterfaceType](../code-quality/ca1408.md) | Types that use a dual interface enable clients to bind to a specific interface layout. Any changes in a future version to the layout of the type or any base types will break COM clients that bind to the interface. By default, if the ClassInterfaceAttribute attribute is not specified, a dispatch-only interface is used. |
| [CA1409: Com visible types should be creatable](../code-quality/ca1409.md) | A reference type that is specifically marked as visible to COM contains a public parameterized constructor but does not contain a public default (parameterless) constructor. A type without a public default constructor is not creatable by COM clients. |
| [CA1410: COM registration methods should be matched](../code-quality/ca1410.md) | A type declares a method that is marked by using the <xref:System.Runtime.InteropServices.ComRegisterFunctionAttribute?displayProperty=fullName> attribute but does not declare a method that is marked by using the <xref:System.Runtime.InteropServices.ComUnregisterFunctionAttribute?displayProperty=fullName> attribute, or vice versa. |
| [CA1411: COM registration methods should not be visible](../code-quality/ca1411.md) | A method that is marked by using the System.Runtime.InteropServices.ComRegisterFunctionAttribute attribute or the System.Runtime.InteropServices.ComUnregisterFunctionAttribute attribute is externally visible. |
| [CA1412: Mark ComSource Interfaces as IDispatch](../code-quality/ca1412.md) | A type is marked by using the System.Runtime.InteropServices.ComSourceInterfacesAttribute attribute, and at least one of the specified interfaces is not marked by using the System.Runtime.InteropServices.InterfaceTypeAttribute attribute set to ComInterfaceType.InterfaceIsIDispatch. |
| [CA1413: Avoid non-public fields in COM visible value types](../code-quality/ca1413.md) | Nonpublic instance fields of COM-visible value types are visible to COM clients. Review the content of the fields for information that should not be exposed, or that will have unintended design or security effects. |
| [CA1414: Mark boolean P/Invoke arguments with MarshalAs](../code-quality/ca1414.md) | The Boolean data type has multiple representations in unmanaged code. |
| [CA1415: Declare P/Invokes correctly](../code-quality/ca1415.md) | This rule looks for platform invoke method declarations that target [!INCLUDE[TLA2#tla_win32](../code-quality/includes/tla2sharptla_win32_md.md)] functions that have a pointer to an OVERLAPPED structure parameter and the corresponding managed parameter is not a pointer to a <xref:System.Threading.NativeOverlapped?displayProperty=fullName> structure. |
