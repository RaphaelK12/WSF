
[![Release](https://img.shields.io/github/release/Dirkster99/WSF.svg)](https://github.com/Dirkster99/WSF/releases/latest)
[![NuGet](https://img.shields.io/nuget/dt/Dirkster.WSF.svg)](http://nuget.org/packages/Dirkster.WSF)

# Windows Shell Foundation (WSF)

<h1><img src="https://github.com/Dirkster99/WSF/blob/master/ProjectIcon.png?raw=true" height="64"/>&nbsp;Overview</h1>

This project implements an open source Windows Shell data provider,
which is necessary to display information related to the Windows system structure
in an Application.

This implementation targets Windows 10 but should also be good for support on Vista and later (Windows 7-8).

Parts of this project were originally developed by <b>Leung Yat Chun Joseph <a href="https://github.com/lycj">lycj</a></b>
in his FileExplorer application originating from CodePlex and <a href="https://www.codeproject.com/Members/Fainx">CodeProject</a>.

The implementation of the Windows Shell Foundation in this WSF project is based on LYCJ's interfaces
but completely refactored in terms of models and classes using [SharpShell](https://github.com/dwmkerr/sharpshell)
as a base of most things that are there.

More information about the [Windows Shell](https://msdn.microsoft.com/de-de/library/windows/desktop/bb773177.aspx).
