---
layout: default
title: CodeFontIcons Folder
parent: Components
nav_order: 2
---

# CodeFontIcons Folder
{: .no_toc }
This folder contains the static classes of the SVGs icon rich fonts, MonettelliUIKIT offers two FontIcons, "Material Design Icons" and "Monettelli Font Icons", both open sources with thousands of ready-to-use icons in Tabs, Flyout and Interfaces.

---
## Table of contents
{: .no_toc .text-delta }

1. TOC
{:toc}

---

---
**NOTE**
{: .label .label-blue }

- To use these `Static FontIcons Classes`, add the `Namespace` or the path where it is located, and in the `Glyph` property of `FontImageSource` through `x:Static` we implement an icon ready for use.

---

 {: #xml}
FontAwesome namespace and the logic of using FontIcons Code Example

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

    <!-- ... -->

    <!--#region FontImageSource INTERFACES-->
    <FontImageSource
        x:Key="icon_love"
        FontFamily="MaterialFontIcons"
        Glyph="{x:Static FontAwesome:MaterialFontIcons.Heart}"
        Size="30"
        Color="#EC2143" />
    <!--#endregion-->

    <!-- ... -->

</ResourceDictionary>
```

---

## MaterialFontIcons-cs

Static class of Material Design Icons whose space name is in Icons.xaml.

---
**SOLUTION**
{: .label .label-green }

- `Material Design Icons` has `more than 5000 icons` and two styles, `Line` and `Solid`, that we can combine according to the type of text Font.

---

Material Design Icons Structure Table

| Style          | Variety    | Variant(s) Font                | Nomenclature             |
|:---------------|:-----------|:-------------------------------|:-------------------------|
| Line Style     | Outline    | Regular, Light, ExtraLight...  | `[NameFonticon]Outline`  |  
| Solid Style    | Solid      | Bold, Black, ExtraBold...      | `[NameFontIcon]`         |

---

 {: #csharp}
Material Design Icons Structure Code Example

```csharp
using System;
using System.Collections.Generic;
using System.Text;

namespace XF_MonettelliUIKIT.CodeFontIcons
{
    static class MaterialFontIcons
    {
        public const string SlashForward = "\u000f0000";
        public const string SlashForwardBox = "\u000f0001";
        public const string SwapHorizontalCircle = "\u000f0002";
        public const string SwapHorizontalCircleOutline = "\u000f0003";
        public const string SwapVerticalCircle = "\u000f0004";
        public const string SwapVerticalCircleOutline = "\u000f0005";
        public const string TankerTruck = "\u000f0006";
        public const string TextureBox = "\u000f0007";
        public const string TramSide = "\u000f0008";
        public const string VectorLink = "\u000f0009";
        public const string Numeric10 = "\u000f000a";
        public const string Numeric10BoxMultiple = "\u000f000b";
        public const string Numeric10BoxMultipleOutline = "\u000f000c";
        public const string Numeric10Circle = "\u000f000d";
        public const string Numeric10CircleOutline = "\u000f000e";
        public const string Numeric9Plus = "\u000f000f";
        public const string VectorSquare = "\uf001";
        public const string CreditCard = "\u000f0010";
        public const string CreditCardMultiple = "\u000f0011";

        // more than 5000 FontIcons...
    }
}
```

---

## MonettelliFontIcons-cs

Static class of Monettelli Font Icons clean and ready to use, this rich font was made in <a href="https://www.adobe.com/products/xd.html" target="_blank">AdobeXD</a> and packaged by <a href="https://icomoon.io" target="_blank">IconMoon</a> and <a href="http://fontello.com/" target="_blank">Fontello</a>.

---
**NOTE**
{: .label .label-blue }

- `Monettelli Font Icons` has 8 outline icons and one brand, very soon this pack will bring more icons of different styles.

---

Monettelli Font Icons Structure Table

| Style          | Variety    | Variant(s) Font                | Nomenclature               |
|:---------------|:-----------|:-------------------------------|:---------------------------|
| Line Style     | Outline    | Regular, Light, ExtraLight...  | `[NameFonticon]_Outline`   |  

---

 {: #csharp}
Monettelli Font Icons Structure Code Example

```csharp
using System;
using System.Collections.Generic;
using System.Text;

namespace XF_MonettelliUIKIT.CodeFontIcons
{
    static class MonettelliFontIcons
    {
        public const string icon_brand_monettelliuikit = "\ue800";
        public const string icon_fly_menu = "\ue801";
        public const string icon_fly_rocket_outline = "\ue802";
        public const string icon_fly_view_dashboard_outline = "\ue803";
        public const string icon_fly_xamarin_outline = "\ue804";
        public const string icon_fly_ballot_outline = "\ue805";
        public const string icon_fly_animation_outline = "\ue806";
        public const string icon_fly_palette_outline = "\ue807";
        public const string icon_fly_file_document_outline = "\ue808";

        // Coming soon more FontIcons...
    }
}
```
