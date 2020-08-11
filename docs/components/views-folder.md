---
layout: default
title: Views Folder
parent: Components
nav_order: 6
---

# Views Folder
{: .no_toc }
They are XAML files whose base class is mostly a "ContentPage", in it we can add layouts, controls, etc.

---
**SOLUTION**
{: .label .label-green }

- The different interfaces that MonettelliUIKIT requires are tested on all three platforms, being `responsive is a priority`.

---

<a href="https://raw.githubusercontent.com/MonettelliUIKIT/monettelliuikit.github.io/master/assets/images/ResponsiveMode.png" data-fancybox><img src="https://raw.githubusercontent.com/MonettelliUIKIT/monettelliuikit.github.io/master/assets/images/ResponsiveMode.png" /></a>

---
**SOLUTION**
{: .label .label-green }

- All the interfaces, although they are separated in different folders, `the x:Class will simulate that they are only in the Views folder`, this helps to implement a single namespace in AppShell.xaml.

---

 {: #xml}
Interfaces with direct paths to views folder Code Example

```xml
<ContentPage
    x:Class="XF_MonettelliUIKIT.Views.DefaultPage">

       <ContentPage.Resources>
        <ResourceDictionary Source="Styles.xaml" />
       </ContentPage.Resources>

        <!-- ... -->

</ContentPage>
```

---
**SOLUTION**
{: .label .label-green }

- The `Styles.xaml` file is linked in each Views folder, this will make it not mixed with the other styles and only available for the interfaces it requires.

---

---
**CASE**
{: .label .label-yellow }

- When we have two styles with similar FontSize but with different TextColor or FontFamily, `the abbreviation ends in a number that indicates the priority`, this case can be seen in the following code.

---

 {: #xml}
Styles.xaml case and path Code Example

```xml
<?xml version="1.0" encoding="utf-8" ?>
<ResourceDictionary
    x:Class="XF_MonettelliUIKIT.Views.PreviewApp.Styles"
    xmlns="http://xamarin.com/schemas/2014/forms"
    xmlns:x="http://schemas.microsoft.com/winfx/2009/xaml"
    xmlns:d="http://xamarin.com/schemas/2014/forms/design"
    xmlns:mc="http://schemas.openxmlformats.org/markup-compatibility/2006"
    mc:Ignorable="d">

    <Style
        x:Key="TxtTitle_1"
        TargetType="Label">
        <Setter Property="TextColor" Value="{DynamicResource colSec}" />
        <Setter Property="FontSize" Value="{StaticResource TxtSizeTit_18}" />
        <Setter Property="FontFamily" Value="SourceSansPro_Bold" />
    </Style>

    <Style
        x:Key="TxtTitle_2"
        TargetType="Label">
        <Setter Property="TextColor" Value="{DynamicResource colQua}" />
        <Setter Property="FontSize" Value="{StaticResource TxtSizeTit_18}" />
        <Setter Property="FontFamily" Value="SourceSansPro_Bold" />
    </Style>

    <!-- ... -->

</ResourceDictionary>
```
