---
layout: default
title: Styles Folder
parent: Components
nav_order: 1
---

# Styles Folder
{: .no_toc }
This folder is the backbone of MonettelliUIKIT, it has 3 XAML files of type "ResourceDictionary" and a main one that merges them.

---
## Table of contents
{: .no_toc .text-delta }

1. TOC
{:toc}

---

## Texts-xaml

This ResourceDictionary establishes ~~the sources of the application through OnPlatform for Android, iOS and UWP, with~~ their respective variants called Bold, ItalicBold, italic, etc.

---
**NOTE**{: .label .label-blue } **Old version**{: .label .label-red }

~~- In the `"FONTSFAMILY" region`, the `x:Key` must start with the variant followed by the name of the font family, this helps to differentiate it from other fonts, `Example: "BoldFont_OpenSans".`~~

---

{: #xml}
"FontsFamily" region Code Example **Old version**{: .label .label-red }

```xml
<?xml version="1.0" encoding="UTF-8" ?>
<?xaml-comp compile="true" ?>
<ResourceDictionary 
    xmlns="http://xamarin.com/schemas/2014/forms"
    xmlns:x="http://schemas.microsoft.com/winfx/2009/xaml"
    xmlns:d="http://xamarin.com/schemas/2014/forms/design"
    xmlns:mc="http://schemas.openxmlformats.org/markup-compatibility/2006"
    mc:Ignorable="d">

    <!--#region FONTSFAMILY [OpenSans]-->
    <!--#region Bold-->
    <OnPlatform x:Key="BoldFont_OpenSans" x:TypeArguments="x:String">
        <On Platform="Android" Value="FontsFamily/OpenSans-Bold.ttf#Open Sans" />
        <On Platform="iOS" Value="OpenSans-Bold" />
        <On Platform="UWP" Value="/Assets/FontsFamily/OpenSans-Bold.ttf#Open Sans" />
    </OnPlatform>
    <!--#endregion-->

    <!--#region BoldItalic-->
    <OnPlatform x:Key="BoldItalicFont_OpenSans" x:TypeArguments="x:String">
        <On Platform="Android" Value="FontsFamily/OpenSans-BoldItalic.ttf#Open Sans" />
        <On Platform="iOS" Value="OpenSans-BoldItalic" />
        <On Platform="UWP" Value="/Assets/FontsFamily/OpenSans-BoldItalic.ttf#Open Sans" />
    </OnPlatform>
    <!--#endregion-->

    <!-- Other variants... -->

</ResourceDictionary>
```

---
Font size is an important issue, and thanks to “Material Design” we can categorize them (see the following table).

---
**NOTE**
{: .label .label-blue }

- In the `"TEXT SIZE [MATERIAL DESIGN]" region`, the `x:Key` starts with "TxtSize" followed by the abbreviation of "Scale Category" with its respective "Size", `Example: "TxtSizeH2_60" (Look at the following table and the sample code).`

---

Material Design Typography Table

| Scale Category | Name           | Variant(s)       | Size    | x:key              |
|:---------------|:---------------|:-----------------|:--------|:-------------------|
| H1             | Headline1      | Light            | 96      | `TxtSizeH1_96`     |
| H2             | Headline2      | Light            | 60      | `TxtSizeH2_60`     |
| H3             | Headline3      | Regular          | 48      | `TxtSizeH3_48`     |
| H4             | Headline4      | Regular          | 34      | `TxtSizeH4_34`     |
| H5             | Headline5      | Regular          | 24      | `TxtSizeH5_24`     |
| H6             | Headline6      | Medium, Bold     | 20      | `TxtSizeH6_20`     |
| Title          | Title          | Medium, Bold     | 18      | `TxtSizeTit_18`    |
| Subtitle 1     | Subtitle 1     | Regular, Bold    | 16      | `TxtSizeSubTit1_16`|
| Subtitle 2     | Subtitle 2     | Medium, Bold     | 14      | `TxtSizeSubTit2_14`|
| Body 1         | Body 1         | Regular          | 16      | `TxtSizeBod1_16`   |
| Body 2         | Body 2         | Regular          | 14      | `TxtSizeBod2_14`   |
| BUTTON         | BUTTON         | Medium, Bold     | 14      | `TxtSizeBtn_14`    |
| Caption        | Caption        | Regular          | 12      | `TxtSizeCap_12`    |
| OVERLINE       | OVERLINE       | Regular          | 10      | `TxtSizeOver_10`   |

---
{: #xml}
"Text Size [Material Design]" region Code Example

```xml
<?xml version="1.0" encoding="UTF-8" ?>
<?xaml-comp compile="true" ?>
<ResourceDictionary 
    xmlns="http://xamarin.com/schemas/2014/forms"
    xmlns:x="http://schemas.microsoft.com/winfx/2009/xaml"
    xmlns:d="http://xamarin.com/schemas/2014/forms/design"
    xmlns:mc="http://schemas.openxmlformats.org/markup-compatibility/2006"
    mc:Ignorable="d">

    <!--#region TEXT SIZE [MATERIAL DESIGN]-->
    <!--  H1-Light  -->
    <x:Double x:Key="TxtSizeH1_96">96</x:Double>
    <!--  H2-Light  -->
    <x:Double x:Key="TxtSizeH2_60">60</x:Double>
    <!--  H3-Regular  -->
    <x:Double x:Key="TxtSizeH3_48">48</x:Double>
    <!--  H4-Regular  -->
    <x:Double x:Key="TxtSizeH4_34">34</x:Double>
    <!--  H5-Regular  -->
    <x:Double x:Key="TxtSizeH5_24">24</x:Double>
    <!--  H6-Medium, (Bold)  -->
    <x:Double x:Key="TxtSizeH6_20">20</x:Double>
    <!--  Title-Medium, (Bold)  -->
    <x:Double x:Key="TxtSizeTit_18">18</x:Double>
    <!--  SubTitle1-Regular, (Bold)  -->
    <x:Double x:Key="TxtSizeSubTit1_16">16</x:Double>
    <!--  SubTitle2-Medium, (Bold)  -->
    <x:Double x:Key="TxtSizeSubTit2_14">14</x:Double>
    <!--  Body1-Regular  -->
    <x:Double x:Key="TxtSizeBod1_16">16</x:Double>
    <!--  Body2-Regular  -->
    <x:Double x:Key="TxtSizeBod2_14">14</x:Double>
    <!--  Button-Medium, (Bold)  -->
    <x:Double x:Key="TxtSizeBtn_14">14</x:Double>
    <!--  Caption-Regular  -->
    <x:Double x:Key="TxtSizeCap_12">12</x:Double>
    <!--  Overline-Regular  -->
    <x:Double x:Key="TxtSizeOver_10">10</x:Double>
    <!--#endregion-->

</ResourceDictionary>
```

---

## Icons-xaml

This ResourceDictionary establishes the "FontIcons" ~~through OnPlatform, their structure can be seen in the following code~~.

---
 {: #xml}
FontIcons by OnPlatform Code Example **Old version**{: .label .label-red }

```xml
<?xml version="1.0" encoding="UTF-8" ?>
<?xaml-comp compile="true" ?>
<ResourceDictionary
    xmlns="http://xamarin.com/schemas/2014/forms"
    xmlns:x="http://schemas.microsoft.com/winfx/2009/xaml"
    xmlns:d="http://xamarin.com/schemas/2014/forms/design"
    xmlns:mc="http://schemas.openxmlformats.org/markup-compatibility/2006"
    xmlns:FontAwesome="clr-namespace:XF_Monettelli.CodeFontIcons;assembly=XF_Monettelli"
    mc:Ignorable="d">

    <!--#region MATERIAL FONT ICONS-->
    <OnPlatform x:Key="MaterialFontIcons" x:TypeArguments="x:String">
        <On Platform="Android"
            Value="FontIcons/materialdesignicons-webfont.ttf#Material Design Icons" />
        <On Platform="iOS"
            Value="Material Design Icons" />
        <On Platform="UWP"
            Value="/Assets/FontIcons/materialdesignicons-webfont.ttf#Material Design Icons" />
    </OnPlatform>
    <!--#endregion-->


    <!--#region CUSTOM FONT ICONS WITH IconMoon and Fontello-->
    <OnPlatform x:Key="MonettelliFontIcons" x:TypeArguments="x:String">
        <On Platform="Android"
            Value="FontIcons/monettelliuikitfonticons.ttf#monettelliuikitfonticons" />
        <On Platform="iOS"
            Value="monettelliuikitfonticons" />
        <On Platform="UWP"
            Value="/Assets/FontIcons/monettelliuikitfonticons.ttf#monettelliuikitfonticons" />
    </OnPlatform>
    <!--#endregion-->

    <!-- FontImageSource region... -->

</ResourceDictionary>
```

---
To use "FontIcons", the "FontImageSource" tag is created, MonettelliUIKIT separates the "Tabs", "Flyout" and "Interfaces" resources for an optimal search.

---
**SOLUTION**
{: .label .label-green }

- In FontImageSource `x:Key` must be clean for Xamarin.Forms developers, the following table shows how to name Tabs, Flyout and interfaces (You can see the result in the example code).

---

Nomenclature of the sectors of FontImageSource

| FontImageSource Sector     | x:Key                    |
|:---------------------------|:-------------------------|
| Tabs                       | `icon_tab_[NameFontIcon]`|    
| Flyout                     | `icon_fly_[NameFontIcon]`|      
| Interfaces                 | `icon_[NameFontIcon]`    | 

---
 {: #xml}
FontImageSource in Tabs, Flyout and Interfaces Code Example

```xml
<?xml version="1.0" encoding="UTF-8" ?>
<?xaml-comp compile="true" ?>
<ResourceDictionary
    xmlns="http://xamarin.com/schemas/2014/forms"
    xmlns:x="http://schemas.microsoft.com/winfx/2009/xaml"
    xmlns:d="http://xamarin.com/schemas/2014/forms/design"
    xmlns:mc="http://schemas.openxmlformats.org/markup-compatibility/2006"
    xmlns:FontAwesome="clr-namespace:XF_MonettelliUIKIT.CodeFontIcons;assembly=XF_MonettelliUIKIT"
    mc:Ignorable="d">
  
    <!--#region FontImageSource TABS-->
    <FontImageSource
        x:Key="icon_tab_monettelliuikit"
        FontFamily="MonettelliFontIcons"
        Glyph="{x:Static FontAwesome:MonettelliFontIcons.icon_brand_monettelliuikit}"
        Size="92"
        Color="{DynamicResource colPrim}" />
    <!--#endregion-->


    <!--#region FontImageSource FLYOUT-->

    <!--#region Flyout Icon-->
    <FontImageSource
        x:Key="icon_fly_menu"
        FontFamily="MonettelliFontIcons"
        Glyph="{x:Static FontAwesome:MonettelliFontIcons.icon_fly_menu}"
        Color="{DynamicResource colQua}" />
    <!--#endregion-->

    <FontImageSource
        x:Key="icon_fly_new"
        FontFamily="MonettelliFontIcons"
        Glyph="{x:Static FontAwesome:MonettelliFontIcons.icon_fly_rocket_outline}"
        Size="30"
        Color="{DynamicResource colQua}" />
    <!--#endregion-->


    <!--#region FontImageSource INTERFACES-->
    <FontImageSource
        x:Key="icon_love"
        FontFamily="MaterialFontIcons"
        Glyph="{x:Static FontAwesome:MaterialFontIcons.Heart}"
        Size="30"
        Color="#EC2143" />
    <!--#endregion-->

</ResourceDictionary>
```

---
**NOTE**
{: .label .label-blue }

- If you want to use different icons, colors and sizes for Android, iOS and UWP, make use of `"OnPlatform"` (see the following example code).

---

 {: #xml}
Changing FontIcons on different platforms Code Example

```xml
<?xml version="1.0" encoding="UTF-8" ?>
<?xaml-comp compile="true" ?>
<ResourceDictionary
    xmlns="http://xamarin.com/schemas/2014/forms"
    xmlns:x="http://schemas.microsoft.com/winfx/2009/xaml"
    xmlns:d="http://xamarin.com/schemas/2014/forms/design"
    xmlns:mc="http://schemas.openxmlformats.org/markup-compatibility/2006"
    xmlns:FontAwesome="clr-namespace:XF_MonettelliUIKIT.CodeFontIcons;assembly=XF_MonettelliUIKIT"
    mc:Ignorable="d">


    <!--#region PLATFORMS OPTIONAL-->
    <!--#region PLATFORMS CHANGE ICONS FONT FOR Glyph-->
    <OnPlatform x:Key="OnStringIcon" x:TypeArguments="x:String">
        <On Platform="Android"
            Value="{x:Static FontAwesome:MaterialFontIcons.AccessPoint}" />
        <On Platform="iOS"
            Value="{x:Static FontAwesome:MaterialFontIcons.Cached}" />
        <On Platform="UWP"
            Value="{x:Static FontAwesome:MaterialFontIcons.AccountCardDetails}" />
    </OnPlatform>
    <!--#endregion-->

    <!--#region PLATFORMS COLOR ICONS FONT-->
    <OnPlatform x:Key="OnColorIcon" x:TypeArguments="Color">
        <On Platform="Android" Value="#17D47E" />
        <On Platform="iOS" Value="#EA29E2" />
        <On Platform="UWP" Value="#8DFF2D" />
    </OnPlatform>
    <!--#endregion-->

    <!--#region PLATFORMS SIZE ICONS FONT-->
    <OnPlatform x:Key="OnSizeIcon" x:TypeArguments="x:Double">
        <On Platform="Android" Value="200" />
        <On Platform="iOS" Value="30" />
        <On Platform="UWP" Value="50" />
    </OnPlatform>
    <!--#endregion-->

    <!--#region PLATFORMS IN FontImageSource-->
    <FontImageSource
        x:Key="OnIconDemo"
        FontFamily="MaterialFontIcons"
        Glyph="{StaticResource OnStringIcon}"
        Size="{StaticResource OnSizeIcon}"
        Color="{StaticResource OnColorIcon}" />
    <!--#endregion-->
    <!--#endregion-->

    <!-- FontImageSource region... -->

</ResourceDictionary>
```

---

## Responsive-xaml

Previously called Spaces.xaml, this ResourceDictionary implements Thickness, and thanks to OnPlatform establishes the breadth of Layouts, following the parameters of Material Design, MonettelliUIKIT expanded into controls that need to inject responsive aspects.

---
**SOLUTION**
{: .label .label-green }

- MonettelliUIKIT was separated into three types of space, `idealSpace`, `mediumSpace` and `bigSpace`, due to the dimensions of each platform.

---

 {: #xml}
Types of Spaces Code Example

```xml
<?xml version="1.0" encoding="UTF-8" ?>
<?xaml-comp compile="true" ?>
<ResourceDictionary
    xmlns="http://xamarin.com/schemas/2014/forms"
    xmlns:x="http://schemas.microsoft.com/winfx/2009/xaml"
    xmlns:d="http://xamarin.com/schemas/2014/forms/design"
    xmlns:mc="http://schemas.openxmlformats.org/markup-compatibility/2006"
    mc:Ignorable="d">

   <!--#region TYPES OF SPACES-->
    <OnPlatform x:Key="idealSpace" x:TypeArguments="Thickness">
        <On Platform="Android" Value="16,0" />
        <On Platform="iOS" Value="18,0" />
        <On Platform="UWP" Value="20,0" />
    </OnPlatform>

    <OnPlatform x:Key="mediumSpace" x:TypeArguments="Thickness">
        <On Platform="Android" Value="20,0" />
        <On Platform="iOS" Value="22,0" />
        <On Platform="UWP" Value="24,0" />
    </OnPlatform>

    <OnPlatform x:Key="bigSpace" x:TypeArguments="Thickness">
        <On Platform="Android" Value="32,0" />
        <On Platform="iOS" Value="34,0" />
        <On Platform="UWP" Value="36,0" />
    </OnPlatform>
    <!--#endregion-->


    <!--#region SPACES Grid-->
    <Style x:Key="GridIdealSpace" TargetType="Grid">
        <Setter Property="Padding" Value="{StaticResource idealSpace}" />
    </Style>

    <Style x:Key="GridMediumSpace" TargetType="Grid">
        <Setter Property="Padding" Value="{StaticResource mediumSpace}" />
    </Style>

    <Style x:Key="GridBigSpace" TargetType="Grid">
        <Setter Property="Padding" Value="{StaticResource bigSpace}" />
    </Style>
    <!--#endregion-->


    <!--#region SPACES StackLayout-->
    <Style x:Key="StackIdealSpace" TargetType="StackLayout">
        <Setter Property="Padding" Value="{StaticResource idealSpace}" />
    </Style>

    <Style x:Key="StackMediumSpace" TargetType="StackLayout">
        <Setter Property="Padding" Value="{StaticResource mediumSpace}" />
    </Style>

    <Style x:Key="StackBigSpace" TargetType="StackLayout">
        <Setter Property="Padding" Value="{StaticResource bigSpace}" />
    </Style>
    <!--#endregion-->

    <!-- ... -->

</ResourceDictionary>
```

---
**NOTE**
{: .label .label-blue }

- `Base Spaces are Global Styles` that influence the entire architecture, depending on the `TargetType` applied.

---

---
**SOLUTION**
{: .label .label-green }

- Layouts and controls have default spaces, so styles have `assigned values ​​of 0.`

---

 {: #xml}
BASE Spaces Code Example

```xml
<?xml version="1.0" encoding="UTF-8" ?>
<?xaml-comp compile="true" ?>
<ResourceDictionary
    xmlns="http://xamarin.com/schemas/2014/forms"
    xmlns:x="http://schemas.microsoft.com/winfx/2009/xaml"
    xmlns:d="http://xamarin.com/schemas/2014/forms/design"
    xmlns:mc="http://schemas.openxmlformats.org/markup-compatibility/2006"
    mc:Ignorable="d">

   <!-- ... -->

   <!--#region SPACES BASE-->
    <Style TargetType="Grid">
        <Setter Property="RowSpacing" Value="0" />
        <Setter Property="ColumnSpacing" Value="0" />
    </Style>

    <Style TargetType="StackLayout">
        <Setter Property="Spacing" Value="0" />
    </Style>

    <Style TargetType="Frame">
        <Setter Property="Padding" Value="0" />
    </Style>
    <!--#endregion-->

    <!-- ... -->

</ResourceDictionary>
```

---
**SOLUTION**
{: .label .label-green }

- `Base Labels are Global Styles` and with the `LineBreakMode` property of `TailTruncation` value there will be no problems when using `small devices`.

---

 {: #xml}
BASE Labels Code Example

```xml
<?xml version="1.0" encoding="UTF-8" ?>
<?xaml-comp compile="true" ?>
<ResourceDictionary
    xmlns="http://xamarin.com/schemas/2014/forms"
    xmlns:x="http://schemas.microsoft.com/winfx/2009/xaml"
    xmlns:d="http://xamarin.com/schemas/2014/forms/design"
    xmlns:mc="http://schemas.openxmlformats.org/markup-compatibility/2006"
    mc:Ignorable="d">

   <!-- ... -->

    <!--#region LABELS BASE-->
    <Style TargetType="Label">
        <Setter Property="LineBreakMode" Value="TailTruncation" />
    </Style>
    <!--#endregion-->

</ResourceDictionary>
```

---

## General-xaml

This ResourceDictionary merges Texts.xaml, Icons.xaml and Responsive.xaml using "MergedDictionaries", thanks to Adam Pedley, it is possible to separate multiple XAML files, and create this cool style architecture.

---
 {: #xml}
Use of MergedDictionaries Code Example

```xml
<?xml version="1.0" encoding="UTF-8" ?>
<?xaml-comp compile="true" ?>
<ResourceDictionary
    xmlns="http://xamarin.com/schemas/2014/forms"
    xmlns:x="http://schemas.microsoft.com/winfx/2009/xaml"
    xmlns:d="http://xamarin.com/schemas/2014/forms/design"
    xmlns:mc="http://schemas.openxmlformats.org/markup-compatibility/2006"
    mc:Ignorable="d">

    <ResourceDictionary.MergedDictionaries>
        <ResourceDictionary Source="Texts.xaml" />
        <ResourceDictionary Source="Icons.xaml" />
        <ResourceDictionary Source="Responsive.xaml" />
    </ResourceDictionary.MergedDictionaries>

</ResourceDictionary>
```
