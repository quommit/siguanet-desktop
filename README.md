siguanet-desktop
================

[SIGUANET](https://github.com/labgeo/siguanet-dbsetup) desktop application for Windows that provides a set of query, reporting, mapping and administration tools, including a hierarchically organized interface to [*siguanet_quest*](https://github.com/labgeo/siguanet_quest) PostgreSQL extension.

## What's SIGUANET?
[SIGUANET](https://github.com/labgeo/siguanet-dbsetup) is a free software project that aims to share the University of Alicante's corporate built asset management technology ([SIGUA](http://www.sigua.ua.es)) with the developers community.
In this sense, [SIGUANET](https://github.com/labgeo/siguanet-dbsetup) will hopefully be useful for other universities and academic organizations.

## What's siguanet-desktop
It's a Winforms .NET application written in C# which provides users with a uniform environment for accessing a [SIGUANET](https://github.com/labgeo/siguanet-dbsetup) geodatabase in an intuitive manner.
*siguanet-desktop* features:
* Configuration tools for tailoring the user interface for different profiles.
* *Quest* module: a [*siguanet_quest*](https://github.com/labgeo/siguanet_quest) PostgreSQL extension client which allows executing spatially aggregated reports using a simple treeview interface.
* *TreeMAP* control: a map viewer offering detail views of [*siguanet_quest*](https://github.com/labgeo/siguanet_quest) query results with predefined PDF map outputs.
* A SOAP client which generates the proxy assembly at run time.
* *DbSync* module: a rule based bridge and session management interface for regular data transfer from a corporate ORACLE database to the [SIGUANET](https://github.com/labgeo/siguanet-dbsetup) database.
* A simple SQL execution interface.
* A set of useful utilities for application administrators.

### Operating System requirements
*siguanet-desktop* has been successfully run on Windows XP (SP3) and Windows 7 boxes

### Framework requirements
*siguanet-desktop* is built on .NET framework 2.0.

### Binary dependencies
All external support assemblies are included in the `lib/` folder, namely:
* Npgsql2 data provider for PostgreSQL
* NetTopologySuite 1.7 spatial analysis library
* PdfSharp 0.9 PDF generation library
* Thinktecture 1.6 dynamic proxy generation library

### Database requirements
A working [SIGUANET](https://github.com/labgeo/siguanet-dbsetup) database is needed which meets the following requirements:
* PostgreSQL 9.2 or greater
* PostGIS 2.0 or greater
* [*siguanet_quest*](https://github.com/labgeo/siguanet_quest) 1.0 extension
* Oracle Instant Client and the corresponding TNSNAMES.ora configuration file are needed for running the *DbSync* module.

## How to build and deploy
You can manually build  *siguanet-desktop* using SharpDevelop 2.2 and the provided `SIGUANETDesktop/SIGUANETDesktop.sln` solution file. If you want to distribute *siguanet-desktop* for general use inside your organization, please have a look at the [project's Wiki](https://github.com/labgeo/siguanet-desktop/wiki) for information on configuration files and add-ins you should include in your build and detailed instructions on other required remote resources. For a typical setup (that targeted to a non system administrator who won't be using the *DbSync* module), *siguanet-desktop* can be deployed as a bundle of binaries and configuration files suitable for simple XCOPY install on Windows systems where .NET framework 2.0 is already installed.
