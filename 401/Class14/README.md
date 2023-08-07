## Stephen Walther's Tutorial on ASP.NET MVC Framework Mapping:

Purpose:

This tutorial by Stephen Walther explains how the ASP.NET MVC framework maps browser requests to controller actions using ASP.NET Routing.
ASP.NET Routing:

An essential feature of every ASP.NET MVC application.
Maps incoming browser requests to specific MVC controller actions.
Default Route Table Setup:

When an ASP.NET MVC application is created, it's pre-configured to use ASP.NET Routing.
Routing is enabled in two primary locations:
a. The Web.config file of the application. Four sections here are crucial for routing: system.web.httpModules, system.web.httpHandlers, system.webserver.modules, and system.webserver.handlers.
b. A route table is established in the Global.asax file, which contains event handlers for ASP.NET application lifecycle events. The route table is set up during the Application Start event.
Default Route in Detail:

The Global.asax file creates the default route table during the Application_Start event.
The default route (named "Default") maps:
First URL segment to a controller name.
Second URL segment to a controller action.
Third segment to a parameter named id.
For example, the URL /Home/Index/3 gets mapped to:
Controller: Home
Action: Index
ID: 3
Parameter Defaults:

The default route has predefined values for all three parameters. If not provided:
Controller defaults to "Home".
Action defaults to "Index".
ID defaults to an empty string.
Examples:

Given the URL /Home:
The Index() method of HomeController is called.
If the Index() method expects a string parameter named Id, it's passed an empty string.
If no parameters are expected, the Id is ignored.
If the method has a nullable integer parameter, the method is called without an error.
If the method has a non-nullable integer parameter (and no value is provided), an error occurs.
Given the URL /Home/Index/3:
The Index() method of HomeController is called with an Id parameter having the value 3.
Conclusion:

The tutorial served as an introduction to ASP.NET Routing.

The primary focus was on understanding the default route table in a new ASP.NET MVC application and how it maps URLs to corresponding controller actions.


## Routing in ASP.NET Core

Purpose: Routing matches incoming HTTP requests to endpoints in the app.

Endpoints: These are units of executable request-handling code. They can extract values from URLs for request processing.

Configuration:

Controllers
Razor Pages
SignalR
gRPC Services
Endpoint-enabled middleware (e.g., Health Checks)
Delegates and lambdas
Routing Basics:

All ASP.NET Core templates have routing.
The middleware pipeline in Startup.Configure includes routing.
UseRouting middleware adds route matching.
UseEndpoints middleware adds endpoint execution.
Endpoint Definition:

An endpoint is executable, extensible, selectable, and enumerable.
An endpoint can be matched and executed, e.g., MapGet, MapPost.
ASP.NET Core supports route template features and constraints.
Endpoint Metadata:

Endpoints can have extra data (metadata) attached.
Metadata can be any .NET type and processed by routing-aware middleware.
Routing Concepts:

Endpoints represent units of functionality in terms of routing, authorization, etc.
An endpoint has a RequestDelegate, Metadata collection, routing info (optional), and can be listed from DI.
Endpoint objects are immutable.
Middleware and Routing Interaction:

Middleware can run before UseRouting to influence the request.
Middleware can run between UseRouting and UseEndpoints to inspect metadata and make decisions.
The combination allows configuring policies per endpoint.
Best Practices for Metadata: Define metadata as interfaces or attributes for flexibility and code reuse.

Distinguishing Terminal Middleware and Routing:

Terminal middleware doesn't call the next middleware in the pipeline, effectively terminating the request.
In contrast, routing determines how an incoming URL corresponds to endpoints in the app.