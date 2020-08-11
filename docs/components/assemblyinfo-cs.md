---
layout: default
title: AssemblyInfo-cs
parent: Components
nav_order: 2
---

# AssemblyInfo-cs
{: .no_toc }
This class contains all registered fonts.

---

**SOLUTION**
{: .label .label-green }

- Thanks to <a href="https://devblogs.microsoft.com/xamarin/embedded-fonts-xamarin-forms/" target="_blank">Embedded Fonts</a> we can make use of the fonts in the main project, with the `Alias` ​​property we can simplify or change the name of the font.

---

{: #csharp}
Monettelli Font Icons Structure Code Example

```csharp
using Xamarin.Forms;
using Xamarin.Forms.Xaml;

[assembly: XamlCompilation(XamlCompilationOptions.Compile)]


#region FontIcons Embedded
// MATERIAL FONT ICONS
[assembly: ExportFont("materialdesignicons-webfont.ttf", Alias = "MaterialFontIcons")]
// CUSTOM FONT ICONS WITH "IconMoon" and "Fontello"
[assembly: ExportFont("monettelliuikitfonticons.ttf", Alias = "MonettelliFontIcons")]
#endregion


#region FontFamily Embedded
#region FONTFAMILY [SourceSansPro]
[assembly: ExportFont("SourceSansPro-Black.ttf", Alias = "SourceSansPro_Black")]
[assembly: ExportFont("SourceSansPro-BlackItalic.ttf", Alias = "SourceSansPro_BlackItalic")]
[assembly: ExportFont("SourceSansPro-Bold.ttf", Alias = "SourceSansPro_Bold")]
[assembly: ExportFont("SourceSansPro-BoldItalic.ttf", Alias = "SourceSansPro_BoldItalic")]
[assembly: ExportFont("SourceSansPro-ExtraLight.ttf", Alias = "SourceSansPro_ExtraLight")]
[assembly: ExportFont("SourceSansPro-ExtraLightItalic.ttf", Alias = "SourceSansPro_ExtraLightItalic")]

#endregion
#region FONTFAMILY [OpenSans]
// ...
#endregion
#region FONTFAMILY [Poppins]
// ...
#endregion
#region FONTFAMILY [BebasNeue]
// ...
#endregion
#endregion
```

---

Using Embedded Fonts in AssemblyInfo.cs Table

| FontFamily Style          | Alias    |
|:---------------|:-----------|
| `[FontFamily]`-`[Style]`.ttf     | `[FontFamily]`_`[Style]`    |  
| SourceSansPro-Black.ttf     | SourceSansPro_Black    |  
