---
layout: default
title: App-xaml
parent: Components
nav_order: 5
---

# App-xaml
{: .no_toc }
This Application type xaml file is the nexus of the "Clean UI Style Architecture" with Shell and views, therefore, to link them, a resource dictionary is added, in this case the source is LightTheme.xaml.

---
**SOLUTION**
{: .label .label-green }

- To take advantage of the `Xaml Intellisense` it is necessary to add a resource dictionary instead of a namespace, since it is the way to see the styles you want to inject into a control.

---

 {: #xml}
App-xaml structure Code Example

```xml
<?xml version="1.0" encoding="utf-8" ?>
<Application
    x:Class="XF_MonettelliUIKIT.App"
    xmlns="http://xamarin.com/schemas/2014/forms"
    xmlns:x="http://schemas.microsoft.com/winfx/2009/xaml"
    xmlns:d="http://xamarin.com/schemas/2014/forms/design"
    xmlns:mc="http://schemas.openxmlformats.org/markup-compatibility/2006"
    xmlns:theme="clr-namespace:XF_MonettelliUIKIT.Themes"
    mc:Ignorable="d">

    <Application.Resources>
        <!-- With "theme" namespace intellisense does not work -->
        <!--<theme:LightTheme />-->
        
        <!-- With "ResourceDictionary" intellisense if it works -->
        <ResourceDictionary Source="/Themes/LightTheme.xaml"/>
    </Application.Resources>

</Application>
```
