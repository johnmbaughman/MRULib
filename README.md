[![Build status](https://ci.appveyor.com/api/projects/status/hs63uymamjh9p34u?svg=true)](https://ci.appveyor.com/project/Dirkster99/mrulib)
[![Release](https://img.shields.io/github/release/Dirkster99/MRULib.svg)](https://github.com/Dirkster99/MRULib/releases/latest)
[![NuGet](https://img.shields.io/nuget/dt/Dirkster.MRULib.svg)](http://nuget.org/packages/Dirkster.MRULib)
<h1><img src="https://github.com/Dirkster99/MRULib/blob/master/ProjectIcon.png?raw=true" height="64"/>&nbsp;Overview</h1>
The MRUib project supplies MVVM/WPF controls that manage a Most Recently Used list of files.
See <a href="https://www.codeproject.com/Articles/1202738/MRU-Most-Recently-Used-WPF-control">CodeProject article</a> for more details.

## Details and Demo Applications
This library Implements a WPF/MVVM Control libray (with backend) that manages a Most Recently Used list of files:
- with saving/loading settings from to XML
- List can be grouped by last access (Pinned, Today, Yesterday, Last Week)
- A recently used files menu entry sorted by last access (without grouping is also supported)
- Pinned entries can be moved up and down in the list
- List entries can be removed based on their age (e.g. Remove all entries older than 1 week)
- Support for Light/Dark theming is build in
- Entries in a ListView (or other constrained size view) can be trimmed using Ellipses '...' characters at the Left, Right, or Center of the text string

![](https://raw.githubusercontent.com/Dirkster99/Docu/master/MruLib/ShowLeftEllipses.png)![](https://raw.githubusercontent.com/Dirkster99/Docu/master/MruLib/ShowCenterEllipses.png)

See `ShowEllipses` dependency property of the:
- [PathTrimmingFileHyperlink](https://github.com/Dirkster99/MRULib/blob/master/source/MRULib/Controls/PathTrimmingFileHyperlink.xaml.cs)
- [PathTrimmingTextBlock](https://github.com/Dirkster99/MRULib/blob/master/source/MRULib/Controls/PathTrimmingTextBlock.cs)

for more details.

There is a demo application and unit test project to demonstrate usage of the control
and document each feature, such as, the ability to configure a minimum and maximum value
that can be used to keep the resulting number of list entries within defined bounds.

## Theming

Load *Light* or *Dark* brush resources in you resource dictionary to take advantage of existing definitions.

```XAML
    <ResourceDictionary.MergedDictionaries>
        <ResourceDictionary Source="/MRULib;component/Themes/DarkBrushes.xaml" />
    </ResourceDictionary.MergedDictionaries>
```

```XAML
    <ResourceDictionary.MergedDictionaries>
        <ResourceDictionary Source="/MRULib;component/Themes/LightBrushes.xaml" />
    </ResourceDictionary.MergedDictionaries>
```

These definitions do not theme all controls used within this library. You should use a standard theming library, such as:
- [MahApps.Metro](https://github.com/MahApps/MahApps.Metro),
- [MLib](https://github.com/Dirkster99/MLib), or
- [MUI](https://github.com/firstfloorsoftware/mui)

to also theme standard elements, such as, button and textblock etc.

This library is the third attempt on the subject. See Codeplex to find the last version of this library:
http://mrulist.codeplex.com/.

Sample Applications:
- [Edi](https://github.com/Dirkster99/Edi) (see screeenshots below)
- [XmlExplorer](https://github.com/Dirkster99/XmlExplorer)

![screenshot](https://github.com/Dirkster99/Docu/blob/master/Edi/StartPage.png?raw=true)
![screenshot](https://github.com/Dirkster99/Docu/blob/master/Edi/MU_MenuItems.png?raw=true)
![screenshot](https://github.com/Dirkster99/Docu/blob/master/Edi/Edi_MRU_ContextMenu.png?raw=true)
