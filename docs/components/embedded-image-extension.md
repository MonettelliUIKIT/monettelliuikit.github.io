---
layout: default
title: Embedded Image Extension
parent: Components
nav_order: 3
---

# Embedded Image Extension
{: .no_toc }
This markup extension adds built-in resources to place images directly into the shared project.

---
## Table of contents
{: .no_toc .text-delta }

1. TOC
{:toc}

---

## Using Embedded Images Video

---
     
 <a data-fancybox href="https://www.youtube.com/watch?v=VVpbklb6vDc">
<img class="card-img-top img-fluid" src="http://img.youtube.com/vi/VVpbklb6vDc/mqdefault.jpg" /> </a>
        
---
 {: #csharp}
Using Embedded Images Code Example

```csharp
using System;
using System.Collections.Generic;
using System.Reflection;
using System.Text;
using Xamarin.Forms;
using Xamarin.Forms.Xaml;

namespace XF_MonettelliUIKIT.MarkupExtension
{

  // You exclude the 'Extension' suffix when using in Xaml markup
  [ContentProperty("Source")]
  public class EmbeddedImageExtension : IMarkupExtension
  {
    public string Source { get; set; }

    public object ProvideValue(IServiceProvider serviceProvider)
    {
      if (Source == null)
      {
        return null;
      }

      // Do your translation lookup here, using whatever method you require
      var imageSource = ImageSource.FromResource(Source, typeof(EmbeddedImageExtension).GetTypeInfo().Assembly);

      return imageSource;
    }
  }

}

```
