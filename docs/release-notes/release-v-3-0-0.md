---
layout: default
title: Release v3.0.0
parent: Release Notes
nav_order: 1
---

# Release v3.0.0 - Improvements
{: .no_toc }
{: .d-inline-block }

New release
{: .label .label-purple }

---
## Table of contents
{: .no_toc .text-delta }

1. TOC
{:toc}

---

## Features table

---

| Feature(s)         | Change(s)            | Type(s)    |
|:----------------|:---------------------|:----------:|
| Embedded Fonts  | Delete the code and useless resources on Android and iOS, and the **Texts.xaml**, **Icons.xaml** files from the **“Styles”** folder. <br> <br> The “Resources” folder will house all the fonts, images and SVG files. <br> <br> All fonts were registered to class **“AssemblyInfo.cs”**. | **Break**{: .label .label-green } <br> <br> **New**{: .label } |
| There will be no support for UWP. | Xamarin.Forms ≥ v4.5.530 ≤ v4.6.0.800 uses **Embedded Fonts**, in **UWP it is not entirely feasible for Font Icons**. | **Deprecated**{: .label .label-red } |
| Xamarin.Forms        | v4.6.0.800      | **Updated**{: .label .label-yellow }   |
| Xamarin.Forms.Visual.Material          |  v4.6.0.800 | **Updated**{: .label .label-yellow }  |
| Xamarin.Essentials           | v1.5.3.2 | **Updated**{: .label .label-yellow }  |
| Com.Airbnb.Xamarin.Forms.Lottie           | v3.0.3 | ---  |
| Refractored.MvvmHelpers           | v1.6.2 | **Updated**{: .label .label-yellow }  |
| SkiaSharp.Views.Forms           | v1.68.3 | **Updated**{: .label .label-yellow }  |
| Xamarin.FFImageLoading.Forms           | v2.4.11.982 | ---  |
| Xamarin.FFImageLoading.Svg.Forms           | v2.4.11.982 | ---  |
| Xamarin.FFImageLoading.Transformations           | v2.4.11.982 | ---  |
| Xamarin.Forms.PancakeView           | v1.4.2 | **Updated**{: .label .label-yellow }  |

---

## Comparisons with old version

---

| MonettelliUIKIT v3.0.0 | MonettelliUIKIT v2.0.0 | 
|:----------------------:|:----------------------:|
|   <a href="https://raw.githubusercontent.com/MonettelliUIKIT/monettelliuikit.github.io/master/assets/images/v3_0_0_comparison_v2_0_0.png" data-fancybox><img src="https://raw.githubusercontent.com/MonettelliUIKIT/monettelliuikit.github.io/master/assets/images/v3_0_0_comparison_v2_0_0.png" /></a> |   <a href="https://raw.githubusercontent.com/MonettelliUIKIT/monettelliuikit.github.io/master/assets/images/v2_0_0_comparison_v3_0_0.png" data-fancybox><img src="https://raw.githubusercontent.com/MonettelliUIKIT/monettelliuikit.github.io/master/assets/images/v2_0_0_comparison_v3_0_0.png" /></a>

---

## Download this version

[MonettelliUIKIT v3.0.0](https://github.com/danielmonettelli/MonettelliUIKIT/releases/tag/release-3.0.0){: .btn .btn-purple }