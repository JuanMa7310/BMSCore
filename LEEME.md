# BMSCore 1.1.0

[![Únase al chat en https://gitter.im/BMSCore/communityfont](https://badges.gitter.im/Join%20Chat.svg)](https://gitter.im/BMSCore/community?utm_source=insignia&utm_medium=insignia&utm_campaign=insignia-pr&utm_content=insignia)

![Logotipo BMSCore](http://github.com/SDOSPY/BMSCore/blob/master/BMSCore_github_icon_64x64.png)

## Introducción

BMSCore es el Framework, código abierto y multiplataforma para crear módulos y extensiones para Business Management Suite (BMS) basado en ASP.NET Core. Está construido con las mejores y más modernas herramientas y lenguajes (Visual Studio 2019, C#, etc.). ¡Unete a nuestro equipo!

BMSCore le permite construir sus aplicaciones web a partir de los diferentes módulos o extensiones reutilizables independientes. Cada uno de estos módulos o extensiones puede consistir en uno o más proyectos de ASP.NET Core y cada uno de estos proyectos puede incluir todo lo que desee como cualquier otro proyecto de ASP.NET Core. Los controladores, los componentes de vista, las vistas (agregadas como recursos y / o precompiladas), el contenido estático (agregado como recursos) se resuelven automáticamente. Estos proyectos se pueden agregar a la aplicación web de dos maneras: como dependencias directas en project.json (como código fuente o paquetes NuGet) o copiando archivos DLL compilados en la carpeta Extensiones. BMSCore admite estas dos opciones de forma inmediata y al mismo tiempo.

Además, cualquier proyecto de la aplicación web basada en BMSCore puede obtener implementaciones o instancias de algún tipo dado de todos los proyectos (opcionalmente usando los predicados para el filtrado de ensamblados).

BMSCore consta de un paquete general y dos extensiones básicas opcionales.

### Paquetes generales

El paquete general de BMSCore es:

* BMSCore.Infrastructure

#### BMSCore.Infrastructure

Este paquete describe cosas compartidas básicas como la interfaz IExtension y su implementación abstracta: la clase ExtensionBase. También contiene la clase ExtensionManager, el elemento central en el mecanismo de descubrimiento de tipos BMSCore. La mayoría de los módulos o extensiones necesitan este paquete como dependencia.

### Extensiones básicas

Las extensiones básicas de BMSCore son:

* BMSCore.Data;
* BMSCore.Mvc.

#### BMSCore.Data

De forma predeterminada, BMSCore no sabe nada sobre datos y almacenamiento, pero puede usar la extensión BMSCore.Data para tener un enfoque unificado para trabajar con datos y contexto de almacenamiento único entre todas las extensiones. Actualmente es compatible con Microsoft SQL Server, PostgreSql y SQLite, pero es muy fácil agregar otro soporte de almacenamiento.

#### BMSCore.Mvc

Por defecto, las aplicaciones web BMSCore no son MVC. La extensión BMSCore.Mvc les proporciona soporte MVC. Esta extensión inicializa MVC, hace posible utilizar controladores, ver componentes, vistas (agregadas como recursos y / o precompiladas), contenido estático (agregado como recursos) de otras extensiones, etc.

Puede encontrar más información utilizando los enlaces al final de esta página.

## Empezando

Todo lo que necesita hacer para tener una aplicación web modular y extensible es:

* implementar la interfaz BMSCore.Infrastructure.IExtension en cada una de sus extensiones (opcional);
* decirle a la aplicación web principal sobre las extensiones.

### Ejemplos

Por favor, eche un vistazo a nuestros ejemplos en GitHub:

* [BMSCore Framework 1.1.0 Aplicación web de ejemplo con todas las funciones](https://github.com/SDOSPY/BMSCore-Sample)
* [BMSCore Framework 1.1.0 Aplicación web de ejemplo más simple](https://github.com/SDOSPY/BMSCore-Sample-Simplest)
* [BMSCore Framework 1.1.0 Aplicación web de ejemplo MVC](https://github.com/SDOSPY/BMSCore-Sample-MVC)
* [BMSCore Framework 1.1.0 Aplicación web de ejemplo que utiliza una base de datos](https://github.com/SDOSPY/BMSCore-Sample-Data)
* [BMSCore Framework 1.1.0 Aplicación web de ejemplo con interfaz de usuario modular](https://github.com/SDOSPY/BMSCore-Sample-ModularUI)

También puede descargar nuestro [ejemplo completo listo para usar](http://www.sdospy.com/BMS/BMSCore/files/BMSCore-sample-1.1.0.zip). Contiene todo lo que necesita para ejecutar la aplicación web basada en BMSCore de Visual Studio 2019, incluida la base de datos SQLite con los datos de prueba.

### Tutoriales

He escrito [varios tutoriales](http://www.sdospy.com/BMS/BMSCore/docs/en/getting_started/index.html) para ayudarlo a comenzar a desarrollar sus aplicaciones web basadas en BMSCore.

## Desarrollo y depuración

Debe tener referencias directas a sus proyectos de extensión en el archivo project.json de la aplicación host para poder depurar esos proyectos. Una vez finalizada la extensión, puede usarla como archivos DLL sin necesidad de tener referencias explícitas a sus proyectos.

## Enlaces

Sitio web:	[http://www.sdospy.com/BMS/BMSCore](http://www.sdospy.com/BMS/BMSCore/) (en construcción)

Documentación:	[http://www.sdospy.com/BMS/BMSCore/docs](http://www.sdospy.com/BMS/BMSCore/docs/) (en construcción)

Código fuente:	[https://github.com/SDOSPY/BMSCore/](https://github.com/SDOSPY/BMSCore)
