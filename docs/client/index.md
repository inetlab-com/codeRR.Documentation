Client library documentation
============

The client libraries are only used to detect unhandled exceptions and to allow you to manually report exceptions.
They also collect context information and make sure that the error report is uploaded properly.

You also need to either [install codeRR Community Edition](../server/installation.md) or create an account in [codeRR Live](https://coderrapp.com/live/).

# Getting started

Our [Getting started](gettingstarted.md) shows how you install and configure the client libraries and how you can report exceptions and attach custom context collections (like including method arguments or view models).

# Extending

Learn how you can create your own context collections are build your own client library.

[Extending](extending/)

# Integration libraries

We currently have integrations for the following .NET libraries:

Name | Description
--- | -----
[codeRR.client](libraries/core/index.md) | Our reporting library, allows you to manually report exceptions.
[codeRR.client.aspnet](libraries/aspnet/index.md) | Generic ASP.NET library. Catches all unhandled exceptions and report them. Collects information about the HTTP request, session data etc. Allows you to easily create custom error pages for different HTTP error codes.
[codeRR.client.aspnet.mvc5](libraries/aspnet-mvc5/index.md) | ASP.NET MVC5 specific library. Does the same as the ASP.NET library, but do also collect specific MVC5 information like route data, ViewBag etc. Also allows you to customize your error pages by just creating them in the correct folder.
codeRR.client.aspnet.webapi2 | ASP.NET WebApi2 integration. Tracks exceptions, failed authentication attempts, invalid POSTs and other cool stuff.
codeRR.client.aspnetcore.mvc | Core MVC integration. Tracks exceptions, failed authentication attempts, invalid POSTs and other cool stuff.
codeRR.client.wcf | Catches unhandled exceptions in the WCF pipeline. Collects WCF specific information like the inbound WCF message that failed to be processed.
[codeRR.client.log4net](libraries/log4net/index.md) | Reports all exceptions that you log, including the error message that you wrote.
[codeRR.client.winforms](libraries/winforms/) | Reports all unhandled exceptions. Can take screen shots and collect the state of all open forms.
codeRR.client.WPF | Reports all unhandled exceptions. Can take screen shots and collect the state of all open forms.

If your favorite library isn't listed, you can either create your own or use the core library (`codeRR.client`) to report exceptions