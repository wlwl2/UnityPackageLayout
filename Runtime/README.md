# Runtime Folder

Runtime platform-specific Assets folder. This is only a convention and does not
affect the Asset import pipeline. See Assembly definition and packages to
properly configure runtime assemblies in this folder.

## Assembly definition and packages

You must associate scripts inside a package to an assembly definition file
(.asmdef). Assembly definition files are the Unity equivalent to a C# project in
the .NET ecosystem. You must set explicit references in the assembly definition
file to other assemblies (whether in the same package or in external packages).
See Assembly Definitions for more details.

Use these conventions for naming and storing your assembly definition files to
ensure that the compiled assembly filenames follow the .NET Framework Design
Guidelines:

### Store Editor-specific code under a root editor assembly definition file:

Editor/MyCompany.MyFeature.Editor.asmdef

### Store runtime-specific code under a root runtime assembly definition file:

Runtime/MyCompany.MyFeature.Runtime.asmdef

### Configure related test assemblies for your editor and runtime scripts:

Tests/Editor/MyCompany.MyFeature.Editor.Tests.asmdef

Tests/Runtime/MyCompany.MyFeature.Runtime.Tests.asmdef