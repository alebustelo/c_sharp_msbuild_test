# c_sharp_msbuild_test
Test to use msbuild with Jenkins

## Build

Need the Microsoft VS C# Build Tools installed. Then run the following command which will generate an executable file that can be run directly.

Using the C# compiler
```
csc Helloworld.cs
Helloworld.exe
```

Using MSBuild
```
msbuild helloworld.csproj -t:Build -verbosity:detailed
```