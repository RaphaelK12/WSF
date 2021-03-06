[![Codacy Badge](https://api.codacy.com/project/badge/Grade/b9b51d88782a414e89105bd2efe4ca03)](https://app.codacy.com/app/Dirkster99/WSF?utm_source=github.com&utm_medium=referral&utm_content=Dirkster99/WSF&utm_campaign=Badge_Grade_Dashboard)
[![Build status](https://ci.appveyor.com/api/projects/status/i17iks30rv2xh5gg?svg=true)](https://ci.appveyor.com/project/Dirkster99/wsf)
[![Release](https://img.shields.io/github/release/Dirkster99/WSF.svg)](https://github.com/Dirkster99/WSF/releases/latest)
[![NuGet](https://img.shields.io/nuget/dt/Dirkster.WSF.svg)](http://nuget.org/packages/Dirkster.WSF)

![Net4](https://badgen.net/badge/Framework/.Net&nbsp;4/blue) ![NetCore3](https://badgen.net/badge/Framework/NetCore&nbsp;3/blue)

# Windows Shell Foundation (WSF)

<h2><img src="https://github.com/Dirkster99/WSF/blob/master/ProjectIcon.png?raw=true" height="64"/>&nbsp;Overview</h2>

This project implements an open source Windows Shell data provider,
which is necessary to display information related to the Windows system structure
in an Application. This library is the core of a [Metro Breadcrumb control](https://github.com/Dirkster99/bm)
implemented in a different project.

This implementation targets Windows 10 but should also be good for support on Vista and later (Windows 7-8).

Parts of this project were originally developed by <b>Leung Yat Chun Joseph <a href="https://github.com/lycj">lycj</a></b>
in his FileExplorer application originating from CodePlex and <a href="https://www.codeproject.com/Members/Fainx">CodeProject</a>.

The implementation of the Windows Shell Foundation in this WSF project is based on LYCJ's interfaces
but completely refactored in terms of models and classes using [SharpShell](https://github.com/dwmkerr/sharpshell)
as a base of most things that are there.

Finding all children (eg: 'This PC') under the Desktop root is as complicated as this:

```C#
using WSF;
using WSF.IDs;

foreach (var item in Browser.GetChildItems(KF_IID.ID_FOLDERID_Desktop))
{
    Console.WriteLine("Name '{0}' SpecialPathId '{1}' PathFileSystem '{2}'",
        item.Name, item.SpecialPathId, item.PathFileSystem);
}
```

The *Name* attribute is localized (it should be &quot;This PC&quot; in English and &quot;Dieser PC&quot; in German).

More information about the [Windows Shell](https://msdn.microsoft.com/de-de/library/windows/desktop/bb773177.aspx).
