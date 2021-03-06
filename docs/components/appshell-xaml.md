---
layout: default
title: AppShell-xaml
parent: Components
nav_order: 7
---

# AppShell-xaml
{: .no_toc }
AppShell seeks to reduce the complexity of creating mobile applications by providing fundamental application architecture features. As a complete visual hierarchy, common browsing experience, URI-based routing, and integrated search management (David Ortinau, Principal Program Manager of Microsoft).

---
{: #xml}
AppShell-xaml structure Code Example

```xml
<?xml version="1.0" encoding="utf-8" ?>
<Shell
    x:Class="XF_MonettelliUIKIT.AppShell"
    xmlns="http://xamarin.com/schemas/2014/forms"
    xmlns:x="http://schemas.microsoft.com/winfx/2009/xaml"
    xmlns:d="http://xamarin.com/schemas/2014/forms/design"
    xmlns:mc="http://schemas.openxmlformats.org/markup-compatibility/2006"
    xmlns:ShellTemplate="clr-namespace:XF_MonettelliUIKIT.Views.ShellTemplates"
    xmlns:view="clr-namespace:XF_MonettelliUIKIT.Views"
    xmlns:FontAwesome="clr-namespace:XF_MonettelliUIKIT.CodeFontIcons;assembly=XF_MonettelliUIKIT"
    Title="MonettelliUIKIT"
    FlyoutBackgroundColor="{DynamicResource colStartBG1}"
    FlyoutIcon="{StaticResource icon_fly_menu}"
    FlyoutBehavior="Flyout"
    FlyoutHeaderBehavior="Fixed"
    FlyoutHeaderTemplate="{DataTemplate ShellTemplate:FlyoutHeaderTemplate}"
    ItemTemplate="{DataTemplate ShellTemplate:FlyoutItemTemplate}"
    MenuItemTemplate="{DataTemplate ShellTemplate:FlyoutMenuItemTemplate}"
    Visual="Default"
    mc:Ignorable="d">


    <!--#region CHANGED FLYOUT ICON-->
    <!--<Shell.FlyoutIcon>
        <FontImageSource
            FontFamily="{StaticResource MaterialFontIcons}"
            Glyph="{x:Static FontAwesome:MaterialFontIcons.FormatListBulletedSquare}"/>
    </Shell.FlyoutIcon>-->
    <!--#endregion-->


    <!--#region SHELL RESOURCES-->
    <Shell.Resources>

        <!--#region SHELL STYLES-->
        <Color x:Key="NavigationPrimary">#9042F1</Color>

        <Style
            x:Key="BaseStyle"
            TargetType="Element">
            <Setter Property="Shell.BackgroundColor" Value="{DynamicResource colBackgroundColor}" />
            <!--  In iOS, this property changes the color of the FlyoutIcon and the selected top tabs  -->
            <Setter Property="Shell.ForegroundColor" Value="{DynamicResource colForegroundColor}" />
            <Setter Property="Shell.TitleColor" Value="{DynamicResource colTitleColor}" />
            <Setter Property="Shell.DisabledColor" Value="White" />
            <!--  In iOS this property changes the color tabs upper not selected  -->
            <Setter Property="Shell.UnselectedColor" Value="{DynamicResource colTabBarUns}" />
            <Setter Property="Shell.TabBarBackgroundColor" Value="{DynamicResource colTabBarBack}" />
            <!--  In UWP this property changes the color tabs  -->
            <Setter Property="Shell.TabBarForegroundColor" Value="{DynamicResource colTabBarTitle}" />
            <Setter Property="Shell.TabBarUnselectedColor" Value="{DynamicResource colTabBarUns}" />
            <Setter Property="Shell.TabBarTitleColor" Value="{DynamicResource colTabBarTitle}" />
        </Style>
        <!--#endregion-->


        <!--#region ADD TabBar FlyoutBehavior is INVISIBLE-->
        <Style
            BasedOn="{StaticResource BaseStyle}"
            TargetType="TabBar"
            ApplyToDerivedTypes="True" />
        <!--#endregion-->

        <!--#region ADD ShellItem FlyoutBehavior is VISIBLE-->
        <Style
            BasedOn="{StaticResource BaseStyle}"
            TargetType="ShellItem"
            ApplyToDerivedTypes="True" />
        <!--#endregion-->

        <!--#region ADD FlyoutItem FlyoutBehavior is VISIBLE-->
        <Style
            BasedOn="{StaticResource BaseStyle}"
            TargetType="FlyoutItem"
            ApplyToDerivedTypes="True" />
        <!--#endregion-->
    </Shell.Resources>
    <!--#endregion-->



    <!--#region TABS SECTOR-->
    <!--  What's new?  -->
    <ShellItem
        Title="What's new?"
        Icon="{StaticResource icon_fly_new}">
        <ShellContent ContentTemplate="{DataTemplate view:ConstructionPage}" />
    </ShellItem>
    <!--#endregion-->


    <!--#region FLYOUT SECTOR-->
    <!--#region Main dashboard-->
    <FlyoutItem
        Title="Main dashboard"
        Icon="{StaticResource icon_fly_maindashboard}"
        FlyoutDisplayOptions="AsSingleItem">
        <!--#region Explore Tab-->
        <Tab
            Title="Explore"
            Icon="{StaticResource icon_tab_monettelliuikit}">
            <ShellContent ContentTemplate="{DataTemplate view:ProfileSport1Page}" />
        </Tab>
        <!--#endregion-->

        <!--#region Top Bar Tab-->
        <Tab
            Title="Top Bar"
            Icon="{StaticResource icon_tab_monettelliuikit}">
            <ShellContent
                Title="Top Bar 1"
                ContentTemplate="{DataTemplate view:DefaultPage}" />
            <ShellContent
                Title="Top Bar 2"
                ContentTemplate="{DataTemplate view:DefaultPage}" />
        </Tab>
        <!--#endregion-->

        <!--#region Simple Tab-->
        <Tab
            Title="Simple"
            Icon="{StaticResource icon_tab_monettelliuikit}">
            <ShellContent ContentTemplate="{DataTemplate view:DefaultPage}" />
        </Tab>
        <!--#endregion-->
    </FlyoutItem>
    <!--#endregion-->


    <!--#region Controls and features-->
    <FlyoutItem
        Title="Controls and features"
        Icon="{StaticResource icon_fly_controlsandfeatures}">
        <ShellContent ContentTemplate="{DataTemplate view:ConstructionPage}" />
    </FlyoutItem>
    <!--#endregion-->


    <!--#region Preview-->
    <FlyoutItem
        Title="Preview"
        Icon="{StaticResource icon_fly_preview}">
        <ShellContent ContentTemplate="{DataTemplate view:ConstructionPage}" />
    </FlyoutItem>
    <!--#endregion-->


    <!--#region All icons-->
    <FlyoutItem
        Title="All icons"
        Icon="{StaticResource icon_fly_allicons}">
        <ShellContent ContentTemplate="{DataTemplate view:ConstructionPage}" />
    </FlyoutItem>
    <!--#endregion-->


    <!--#region Themes-->
    <FlyoutItem
        Title="Themes"
        Icon="{StaticResource icon_fly_themes}">
        <ShellContent ContentTemplate="{DataTemplate view:ThemesPage}" />
    </FlyoutItem>
    <!--#endregion-->


    <!--#region About-->
    <FlyoutItem
        Title="About"
        Icon="{StaticResource icon_fly_about}">
        <ShellContent ContentTemplate="{DataTemplate view:ConstructionPage}" />
    </FlyoutItem>
    <!--#endregion-->
    <!--#endregion-->

</Shell>
```
