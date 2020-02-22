# BMSCore 1.1.0

[![Join the chat at https://gitter.im/BMSCore/community](https://badges.gitter.im/Join%20Chat.svg)](https://gitter.im/BMSCore/community?utm_source=badge&utm_medium=badge&utm_campaign=pr-badge&utm_content=badge)

![BMSCore Logotype](http://github.com/SDOSPY/BMSCore/blob/master/BMSCore_github_icon_64x64.png)

## Introduction

BMSCore is the Framework, open source and cross-platform to create modules and extensions for the Business Management Suite (BMS) based on ASP.NET Core. It is built using the best and most modern tools and languages (Visual Studio 2019, C#, etc). Join our team!

BMSCore allows you to build your web applications from the different independent reusable modules or extensions. Each of these modules or extensions may consist of one or more ASP.NET Core projects and each of these projects may include everything you want as any other ASP.NET Core project. Controllers, view components, views (added as resources and/or precompiled), static content (added as resources) are resolved automatically. These projects may be then added to the web application in two ways: as direct dependencies in project.json (as source code or NuGet packages) or by copying compiled DLLs to the Extensions folder. BMSCore supports both of these options out of the box and at the same time.

Furthermore, any project of the BMSCore-based web application is able to get the implementations or instances of some given type from all the projects (optionally using the predicates for assemblies filtering).

BMSCore consists of one general packages and two optional basic extensions.

### General Packages

BMSCore general package is:

* BMSCore.Infrastructure

#### BMSCore.Infrastructure

This package describes such basic shared things as IExtension interface and its abstract implementation – ExtensionBase class. Also it contains ExtensionManager class – the central element in the BMSCore types discovering mechanism. Most of the modules or extensions need this package as dependency.

### Basic Extensions

BMSCore basic extensions are:

* BMSCore.Data;
* BMSCore.Mvc.

#### BMSCore.Data

By default, BMSCore doesn’t know anything about data and storage, but you can use BMSCore.Data extension to have unified approach to working with data and single storage context among all the extensions. Currently it supports Microsoft SQL Server, PostgreSql and SQLite, but it is very easy to add another storage support.

#### BMSCore.Mvc

By default, BMSCore web applications are not MVC ones. MVC support is provided for them by BMSCore.Mvc extension. This extension initializes MVC, makes it possible to use controllers, view components, views (added as resources and/or precompiled), static content (added as resources) from other extensions etc.

You can find more information using the links at the bottom of this page.

## Getting Started

All you need to do to have modular and extendable web application is:

* implement BMSCore.Infrastructure.IExtension interface in each of your extensions (optional);
* tell main web application about the extensions.

### Samples

Please take a look at our samples on GitHub:

* [Full-featured BMSCore 1.1.0 framework sample web application](https://github.com/SDOSPY/BMSCore-Sample)
* [BMSCore Framework 1.1.0 Sample Simplest Web Application](https://github.com/SDOSPY/BMSCore-Sample-Simplest)
* [BMSCore Framework 1.1.0 Sample MVC Web Application](https://github.com/SDOSPY/BMSCore-Sample-MVC)
* [BMSCore Framework 1.1.0 Sample Web Application That Uses a Database](https://github.com/SDOSPY/BMSCore-Sample-Data)
* [BMSCore Framework 1.1.0 Sample Web Application with Modular UI](https://github.com/SDOSPY/BMSCore-Sample-ModularUI)

You can also download our [ready to use full-featured sample](http://www.sdospy.com/BMS/BMSCore/files/BMSCore-sample-1.1.0.zip). It contains everything you need to run BMSCore-based web application from Visual Studio 2019, including SQLite database with the test data.

### Tutorials

We have written [several tutorials](http://www.sdospy.com/BMS/BMSCore/docs/en/getting_started/index.html) to help you start developing your BMSCore-based web applications.

## Development and Debug

You have to have direct references to your extension projects in the host application project.json file in order to be able to debug that projects. After the extension is finished, you can use it as DLL files without need to have explicit references to its projects.

## Links

Website:		[http://www.sdospy.com/BMS/BMSCore/](http://www.sdospy.com/BMS/BMSCore/) (under construction)

Docs:			[http://www.sdospy.com/BMS/BMSCore/docs](http://www.sdospy.com/BMS/BMSCore/docs/) (under construction)

Source Code:	[https://github.com/SDOSPY/BMSCore/](https://github.com/SDOSPY/BMSCore)
