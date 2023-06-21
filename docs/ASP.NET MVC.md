# ASP.NET MVC & .NET Core

## Contents

- [ASP.NET MVC \& .NET Core](#aspnet-mvc--net-core)
  - [Contents](#contents)
  - [ASP.NET MVC - Basics](#aspnet-mvc---basics)
    - [What is ASP.NET MVC? Explain MVC Life cycle.](#what-is-aspnet-mvc-explain-mvc-life-cycle)
    - [What are the advantages of MVC over Web Forms?](#what-are-the-advantages-of-mvc-over-web-forms)
    - [What are the different return types of a controller Action method?](#what-are-the-different-return-types-of-a-controller-action-method)
    - [What are Filters and their types in MVC?](#what-are-filters-and-their-types-in-mvc)
    - [What is Authentication and Authorization in ASP.NET MVC?](#what-is-authentication-and-authorization-in-aspnet-mvc)
    - [What are the types of Authentication in ASP.NET MVC?](#what-are-the-types-of-authentication-in-aspnet-mvc)
    - [What is Output Caching in MVC? How to implement it?](#what-is-output-caching-in-mvc-how-to-implement-it)
    - [What is Routing in MVC?](#what-is-routing-in-mvc)
    - [Explain Attribute Based Routing in MVC?](#explain-attribute-based-routing-in-mvc)
    - [In which assembly is the MVC Framework defined?](#in-which-assembly-is-the-mvc-framework-defined)
  - [ASP.NET MVC - Routing, Controllers, Views and Razor](#aspnet-mvc---routing-controllers-views-and-razor)
    - [What is the difference between `ViewData`, `ViewBag` \& `TempData`?](#what-is-the-difference-between-viewdata-viewbag--tempdata)
    - [How can we pass the data from Controller to View in MVC?](#how-can-we-pass-the-data-from-controller-to-view-in-mvc)
    - [What is Partial View?](#what-is-partial-view)
    - [What are Areas in MVC?](#what-are-areas-in-mvc)
    - [How we can register the area in ASP.NET MVC?](#how-we-can-register-the-area-in-aspnet-mvc)
    - [Explain the concept of MVC Scaffolding?](#explain-the-concept-of-mvc-scaffolding)
    - [What is Bundling and Minification in MVC?](#what-is-bundling-and-minification-in-mvc)
    - [Is it possible to share a View across multiple Controllers?](#is-it-possible-to-share-a-view-across-multiple-controllers)
    - [What is route in MVC? What is default route in MVC?](#what-is-route-in-mvc-what-is-default-route-in-mvc)
    - [Where are the routing rules defined in an ASP.NET MVC application?](#where-are-the-routing-rules-defined-in-an-aspnet-mvc-application)
    - [Differences between Razor and ASPX View Engine in MVC?](#differences-between-razor-and-aspx-view-engine-in-mvc)
    - [What are the main Razor Syntax rules?](#what-are-the-main-razor-syntax-rules)
    - [Explain the need of Display Mode in MVC?](#explain-the-need-of-display-mode-in-mvc)
    - [What is Route Constraints in MVC?](#what-is-route-constraints-in-mvc)
    - [What are the folders in MVC Application Solutions?](#what-are-the-folders-in-mvc-application-solutions)
    - [What is ViewStart?](#what-is-viewstart)
    - [Explain RenderSection in MVC?](#explain-rendersection-in-mvc)
    - [What is the significance of NonActionAttribute?](#what-is-the-significance-of-nonactionattribute)
    - [How route table is created in ASP.NET MVC?](#how-route-table-is-created-in-aspnet-mvc)
    - [ASP.NET MVC application, makes use of settings at 2 places for routing to work correctly. What are these 2 places?](#aspnet-mvc-application-makes-use-of-settings-at-2-places-for-routing-to-work-correctly-what-are-these-2-places)
    - [What is the use of the following default route?](#what-is-the-use-of-the-following-default-route)
    - [What is the difference between adding routes, to a WebForms application and to an MVC application?](#what-is-the-difference-between-adding-routes-to-a-webforms-application-and-to-an-mvc-application)
    - [Which filter executes first in an ASP.NET MVC application?](#which-filter-executes-first-in-an-aspnet-mvc-application)
    - [What are the levels at which filters can be applied in an ASP.NET MVC application?](#what-are-the-levels-at-which-filters-can-be-applied-in-an-aspnet-mvc-application)
    - [Is it possible to create a custom filter?](#is-it-possible-to-create-a-custom-filter)
    - [What filters are executed in the end?](#what-filters-are-executed-in-the-end)
    - [Is it possible to cancel filter execution?](#is-it-possible-to-cancel-filter-execution)
    - [What type of filter does `OutputCacheAttribute` class represents?](#what-type-of-filter-does-outputcacheattribute-class-represents)
    - [What are the 2 popular ASP.NET MVC view engines?](#what-are-the-2-popular-aspnet-mvc-view-engines)
    - [What symbol would you use to denote, the start of a code block in Razor views?](#what-symbol-would-you-use-to-denote-the-start-of-a-code-block-in-razor-views)
    - [What symbol would you use to denote, the start of a code block in ASPX views?](#what-symbol-would-you-use-to-denote-the-start-of-a-code-block-in-aspx-views)
    - [What are sections?](#what-are-sections)
    - [What are the file extensions for razor views?](#what-are-the-file-extensions-for-razor-views)
    - [How do you specify comments using razor syntax?](#how-do-you-specify-comments-using-razor-syntax)
    - [Is it possible to combine ASP.NET webforms and asp.MVC and develop a single web application?](#is-it-possible-to-combine-aspnet-webforms-and-aspmvc-and-develop-a-single-web-application)
    - [What is the use of viewmodel in MVC?](#what-is-the-use-of-viewmodel-in-mvc)
    - [Explain bundle.config in MVC4?](#explain-bundleconfig-in-mvc4)
    - [Does `TempData` hold the data for other request in ASP.NET MVC?](#does-tempdata-hold-the-data-for-other-request-in-aspnet-mvc)
    - [Explain peek method in `TempData` in ASP.NET MVC?](#explain-peek-method-in-tempdata-in-aspnet-mvc)
    - [What are child actions in ASP.NET MVC?](#what-are-child-actions-in-aspnet-mvc)
    - [Can i use razor code in javascript in ASP.NET MVC?](#can-i-use-razor-code-in-javascript-in-aspnet-mvc)
    - [How can i return string result from action in ASP.NET MVC?](#how-can-i-return-string-result-from-action-in-aspnet-mvc)
    - [How to return the json from action method in ASP.NET MVC?](#how-to-return-the-json-from-action-method-in-aspnet-mvc)
    - [Give an example for authorization filters in an ASP.NET MVC application?](#give-an-example-for-authorization-filters-in-an-aspnet-mvc-application)
  - [ASP.NET MVC - Validation, Security, Authentication \& More](#aspnet-mvc---validation-security-authentication--more)
    - [How Validation works in MVC? What is Data Annotation?](#how-validation-works-in-mvc-what-is-data-annotation)
    - [How to implement Security in web applications in MVC?](#how-to-implement-security-in-web-applications-in-mvc)
    - [What is validation summary in MVC?](#what-is-validation-summary-in-mvc)
    - [How do you implement forms authentication in MVC?](#how-do-you-implement-forms-authentication-in-mvc)
    - [What are the methods of handling an error in MVC?](#what-are-the-methods-of-handling-an-error-in-mvc)
    - [How can we done custom error page in MVC?](#how-can-we-done-custom-error-page-in-mvc)
    - [What is server side validation in MVC?](#what-is-server-side-validation-in-mvc)
    - [What is the use of remote validation in MVC?](#what-is-the-use-of-remote-validation-in-mvc)
    - [How we can handle the exception at controller level in ASP.NET MVC?](#how-we-can-handle-the-exception-at-controller-level-in-aspnet-mvc)
    - [Explain the tools used for unit testing in ASP.NET MVC?](#explain-the-tools-used-for-unit-testing-in-aspnet-mvc)
    - [What is data annotation validator attributes in MVC?](#what-is-data-annotation-validator-attributes-in-mvc)
    - [What are the exception filters in MVC?](#what-are-the-exception-filters-in-mvc)
    - [Which approach provides better support for test driven development – ASP.NET MVC or ASP.NET webforms?](#which-approach-provides-better-support-for-test-driven-development--aspnet-mvc-or-aspnet-webforms)
  - [ASP.NET Core - Basics](#aspnet-core---basics)
    - [What is XSRF or CSRF? How to prevent cross-site request forgery (XSRF/CSRF) attacks in ASP.NET Core?](#what-is-xsrf-or-csrf-how-to-prevent-cross-site-request-forgery-xsrfcsrf-attacks-in-aspnet-core)
    - [Explain session and state management in ASP.NET Core.](#explain-session-and-state-management-in-aspnet-core)
    - [How to access httpcontext in ASP.NET Core?](#how-to-access-httpcontext-in-aspnet-core)
    - [Explain the caching and response caching in ASP.NET Core.](#explain-the-caching-and-response-caching-in-aspnet-core)
    - [What is the options pattern in ASP.NET Core?](#what-is-the-options-pattern-in-aspnet-core)
    - [How to use multiple environments in ASP.NET Core?](#how-to-use-multiple-environments-in-aspnet-core)
    - [How ASP.NET Core serve static files?](#how-aspnet-core-serve-static-files)
    - [Explain session and state management in ASP.NET Core?](#explain-session-and-state-management-in-aspnet-core-1)
    - [Can ASP.NET application be run in docker containers?](#can-aspnet-application-be-run-in-docker-containers)
    - [Explain the caching or response caching in ASP.NET Core?](#explain-the-caching-or-response-caching-in-aspnet-core)
    - [How to handle errors in ASP.NET Core?](#how-to-handle-errors-in-aspnet-core)
    - [What are Razor pages in .NET Core?](#what-are-razor-pages-in-net-core)
    - [What is host in ASP.NET Core?](#what-is-host-in-aspnet-core)
    - [Describe the generic host and web host?](#describe-the-generic-host-and-web-host)
    - [Describe the servers in ASP.NET Core?](#describe-the-servers-in-aspnet-core)
    - [How configuration works in ASP.NET Core?](#how-configuration-works-in-aspnet-core)
  - [ASP.NET Core - Routing, Files, CORS \& More](#aspnet-core---routing-files-cors--more)
    - [What is Routing? Explain attribute routing in ASP.NET Core?](#what-is-routing-explain-attribute-routing-in-aspnet-core)
    - [Explain default project structure in ASP.NET Core application?](#explain-default-project-structure-in-aspnet-core-application)
    - [How ASP.NET Core serve static files?](#how-aspnet-core-serve-static-files-1)
    - [What are the roles of Appsettings.Json and Launchsetting.Json file in ASP.NET Core?](#what-are-the-roles-of-appsettingsjson-and-launchsettingjson-file-in-aspnet-core)
    - [What are the various techniques to save configuration settings in ASP.NET Core?](#what-are-the-various-techniques-to-save-configuration-settings-in-aspnet-core)
    - [What is CORS? Why is CORS restriction is required? How to fix CORS error?](#what-is-cors-why-is-cors-restriction-is-required-how-to-fix-cors-error)
    - [How ASP.NET Core Middleware is different from HttpModule?](#how-aspnet-core-middleware-is-different-from-httpmodule)
    - [What are the types of Hosting in ASP.NET Core? What is In process and Out of process hosting?](#what-are-the-types-of-hosting-in-aspnet-core-what-is-in-process-and-out-of-process-hosting)
    - [How to use Dependency Injection in Views in ASP.NET Core?](#how-to-use-dependency-injection-in-views-in-aspnet-core)
    - [What are the types of Service Lifetimes of an object/ instance in ASP.NET Core?](#what-are-the-types-of-service-lifetimes-of-an-object-instance-in-aspnet-core)
    - [What is AddSingleton, AddScoped and AddTransient method?](#what-is-addsingleton-addscoped-and-addtransient-method)
    - [What is Middleware in ASP.NET Core? What is custom middleware?](#what-is-middleware-in-aspnet-core-what-is-custom-middleware)
    - [What is Request Delegate in .NET Core?](#what-is-request-delegate-in-net-core)
    - [What is `Run()`, `Use()` and `Map()` method?](#what-is-run-use-and-map-method)
    - [What is Kestrel? What is the difference between Kestrel and IIS?](#what-is-kestrel-what-is-the-difference-between-kestrel-and-iis)
    - [How to read values from appsettings.json file?](#how-to-read-values-from-appsettingsjson-file)
  - [Additional Resources and References](#additional-resources-and-references)


## ASP.NET MVC - Basics

### What is ASP.NET MVC? Explain MVC Life cycle.

ASP.NET MVC is a web development framework based on the Model-View-Controller (MVC) architectural pattern. It provides a structured way to build dynamic and scalable web applications by separating the concerns of data, presentation, and user interaction.

The MVC life cycle in ASP.NET MVC refers to the sequence of events that occur during the processing of a request and the generation of a response. Here is an overview of the ASP.NET MVC life cycle:

- **Routing:** When a request is made to an ASP.NET MVC application, the Routing module maps the URL to a specific controller and action method based on the defined routes in the application's route configuration.
- **Controller Creation and Initialization:** Once the routing determines the appropriate controller and action method, an instance of the controller is created by the framework. The controller is responsible for handling the request and coordinating the interaction between the model and the view.
- **Model Binding:** In this step, the values from the request, such as form data or query parameters, are bound to the parameters of the action method. The model binder automatically maps the incoming data to the corresponding model properties.
- **Action Execution:** The action method specified by the routing is executed. It performs the necessary logic, such as retrieving data from a database, updating models, or invoking other services. The action method may return different types of results, such as views, JSON, or file downloads.
- **View Rendering:** If the result returned from the action method is a view, the corresponding view template is rendered. The view combines the data from the model with the HTML markup defined in the view template to generate the final HTML response.
- **Response Generation:** The rendered view or other result is converted into an HTTP response, including the appropriate headers and content, which is sent back to the client's browser.

Throughout the life cycle, there are several extension points, such as action filters and view filters, which allow developers to inject additional logic or modify the behavior of the MVC pipeline.

Understanding the MVC life cycle is essential for developers working with ASP.NET MVC as it provides insights into how the request is processed and how to customize the behavior of the framework at each stage.

### What are the advantages of MVC over Web Forms?

MVC (Model-View-Controller) and Web Forms are two different paradigms for building web applications in ASP.NET. Here are the advantages of MVC over Web Forms:

- **Separation of Concerns:** MVC promotes a clear separation of concerns between the different components of the application. The model represents the data and business logic, the view handles the presentation and user interface, and the controller manages the interaction between the model and the view. This separation makes the code more modular, maintainable, and testable.
- **Full Control over Markup:** In MVC, developers have full control over the generated markup, as views are typically created using HTML templates combined with server-side code. This allows for more flexibility in designing the UI and achieving a pixel-perfect layout.
- **Support for Test-Driven Development (TDD):** MVC provides better support for unit testing and test-driven development practices. The separation of concerns and the ability to easily mock dependencies make it easier to write unit tests for individual components of the application, such as controllers and business logic.
- **URL Routing:** MVC has built-in support for URL routing, which allows developers to define custom URL patterns and map them to specific actions. This enables cleaner and more user-friendly URLs, improved search engine optimization (SEO), and easier navigation within the application.
- **Lightweight and Performance:** Compared to Web Forms, MVC is considered to be more lightweight and has better performance characteristics. It does not rely on ViewState and postbacks, which can contribute to overhead and slower page rendering in Web Forms.
- **Flexible Page Flow:** MVC provides more control over the flow of the application by allowing developers to define custom routes and handle requests based on various conditions. This flexibility is beneficial for building complex and dynamic web applications.

While MVC has several advantages over Web Forms, it's important to note that the choice between the two depends on the specific requirements of the project and the preferences of the development team. Both paradigms have their strengths and can be used effectively in different scenarios.

### What are the different return types of a controller Action method?

In ASP.NET MVC, a controller action method can have various return types depending on the desired behavior and the requirements of the application. Here are the common return types used in controller action methods:

- **ViewResult**: Returns a view to be rendered as a response to the client. It can be used to return a specific view or the default view associated with the action.
- **PartialViewResult**: Returns a partial view, which is a reusable portion of a view. Partial views are often used to render common UI elements or components that can be shared across multiple views.
- **RedirectResult**: Redirects the user to a different URL or action method. This is useful for implementing page redirects or navigation to a different part of the application.
- **JsonResult**: Returns a JSON-formatted response, typically used for AJAX requests or when the client expects data in JSON format.
- **ContentResult**: Returns a simple string or raw content as the response. It can be used to return plain text, HTML, XML, or any other content type.
- **FileResult**: Returns a file as the response, allowing users to download or view the file in the browser. This can be used for returning documents, images, or any other file type.
- **HttpNotFoundResult**: Returns a 404 (Not Found) status code to indicate that the requested resource was not found. This is useful for handling invalid URLs or missing data.
- **HttpStatusCodeResult**: Returns a specific HTTP status code with an optional status description. It allows you to customize the status code returned to the client.
- **EmptyResult**: Returns an empty response with no content. It is typically used for actions that perform some processing without returning any data.
- **ActionResult**: This is a base class for various action result types. It provides flexibility to return different result types based on runtime conditions.

These are some of the commonly used return types in ASP.NET MVC controller action methods. The appropriate return type depends on the desired behavior and the data or response expected by the client.

### What are Filters and their types in MVC?

Filters in ASP.NET MVC are components that allow you to implement cross-cutting concerns and add additional behavior to action methods or controllers. They provide a way to encapsulate common functionalities that can be applied globally or selectively to specific controllers or actions. There are several types of filters available in ASP.NET MVC:

- **Authorization Filters**: These filters are used to enforce access control and authentication requirements. They can be used to restrict access to certain actions or controllers based on user roles or permissions.
- **Action Filters**: Action filters are used to perform pre-processing and post-processing logic around action methods. They can intercept and modify the input and output of an action method, as well as execute custom code before and after the action execution.
- **Result Filters**: Result filters are applied to the result of an action method, allowing you to modify or enhance the result before it is returned to the client. They can be used to modify the view or data returned by an action method.
- **Exception Filters**: Exception filters are used to handle and manage exceptions that occur during the execution of an action method. They can be used to log exceptions, display custom error pages, or perform any other desired exception handling logic.
- **Resource Filters**: Resource filters are executed before and after the execution of an action method. They are primarily used to manage resources, such as opening and closing database connections, to ensure proper resource management.

These filters can be applied globally to all controllers or actions, or selectively to specific controllers or actions using attributes. They allow you to modularize and reuse common functionalities across multiple controllers or actions, promoting code reusability and maintainability.

### What is Authentication and Authorization in ASP.NET MVC?

Authentication and authorization are important security concepts in ASP.NET MVC that ensure proper access control and user authentication within an application.

- **Authentication**: Authentication is the process of verifying the identity of a user. It confirms whether the user is who they claim to be. In ASP.NET MVC, authentication involves validating user credentials, such as a username and password, to grant access to protected resources. Common authentication mechanisms in ASP.NET MVC include forms authentication, Windows authentication, and external authentication providers like OAuth or OpenID Connect.
- **Authorization**: Authorization is the process of determining the access rights and permissions of a user. Once a user is authenticated, authorization determines what actions and resources the user is allowed to access based on their assigned roles, permissions, or other authorization rules. ASP.NET MVC provides various authorization mechanisms, such as role-based authorization, attribute-based authorization, and custom authorization rules.

By implementing authentication and authorization in an ASP.NET MVC application, you can ensure that only authenticated and authorized users can access the application's protected resources, helping to secure sensitive information and control access to functionality based on user roles or permissions.

### What are the types of Authentication in ASP.NET MVC?

ASP.NET MVC provides several types of authentication mechanisms to verify the identity of users. These authentication types include:

- **Forms Authentication**: Forms authentication is a cookie-based authentication mechanism where user credentials are validated against a user store, such as a database. Upon successful authentication, a cookie is issued to the client to identify the authenticated user in subsequent requests.
- **Windows Authentication**: Windows authentication relies on the Windows operating system to authenticate users. It allows users to log in with their Windows credentials, such as domain username and password. This authentication method is commonly used in intranet or enterprise applications.
- **External Authentication Providers**: ASP.NET MVC supports external authentication providers like `OAuth` or `OpenID Connect`. These providers allow users to authenticate using their existing accounts from external platforms, such as Google, Facebook, Twitter, or Microsoft accounts.
- **Identity Authentication**: ASP.NET Identity is a membership system that provides a framework for managing user authentication and authorization. It is highly customizable and can be used to implement various authentication mechanisms, including cookie-based authentication, token-based authentication, or two-factor authentication.

The choice of authentication mechanism depends on the specific requirements of the application, the desired user experience, and the level of security needed. ASP.NET MVC offers flexibility in selecting the appropriate authentication type for different scenarios.

### What is Output Caching in MVC? How to implement it?

Output caching is a technique used in ASP.NET MVC to cache the output of a controller action or a partial view. It allows you to store the rendered HTML content in memory or on disk and serve it directly to subsequent requests without re-executing the action or rendering the view.

To implement output caching in MVC, you can use the `OutputCache` attribute at the action or controller level. Here's how you can do it:

- **Action-Level Output Caching**: Apply the `OutputCache` attribute to the specific action method that you want to cache.

   ``` csharp
   [OutputCache(Duration = 3600)] // Cache the output for 1 hour
   public ActionResult Index()
   {
       // Action logic
       return View();
   }
   ```
   
    In the above example, the output of the `Index` action will be cached for 1 hour. Subsequent requests to the same action will be served from the cache without executing the action method.

- **Controller-Level Output Caching**: Apply the `OutputCache` attribute at the controller level to cache the output of all actions within that controller.

    ``` csharp
    [OutputCache(Duration = 3600)] // Cache the output for 1 hour
    public class HomeController : Controller
    {
        // Actions
    }
    ```

    By applying the `OutputCache` attribute at the controller level, all actions within the `HomeController` will be cached for the specified duration.

You can customize the output caching behavior by specifying various parameters in the `OutputCache` attribute, such as cache duration, location, cache profiles, or cache variations based on request parameters.

Output caching is useful when you have static or relatively static content that does not change frequently. It helps improve application performance by reducing the execution time and database queries for repeated requests.

### What is Routing in MVC?

Routing is a mechanism in ASP.NET MVC that maps incoming URLs to specific controller actions. It determines how the application responds to user requests by matching the URL patterns to the corresponding action methods.

In MVC, the routing configuration is typically defined in the `RouteConfig.cs` file located in the `App_Start` folder of the application. The routing system uses a collection of routes to define the URL patterns and the associated controller and action to handle the request.

The routing system follows a hierarchical order to match the incoming URL with the defined routes. It starts from the top of the route collection and continues until it finds a match or reaches the end of the collection.

Here's an example of a basic route configuration:

``` csharp
public class RouteConfig
{
    public static void RegisterRoutes(RouteCollection routes)
    {
        routes.IgnoreRoute("{resource}.axd/{*pathInfo}");

        routes.MapRoute(
            name: "Default",
            url: "{controller}/{action}/{id}",
            defaults: new { controller = "Home", action = "Index", id = UrlParameter.Optional }
        );
    }
}
```

In the above example, the default route is defined with the pattern `{controller}/{action}/{id}`. It specifies that the URL should have a controller name, action name, and an optional `id` parameter. If no values are provided, it defaults to the `Home` controller, `Index` action, and a nullable `id`.

Routing enables clean and SEO-friendly URLs by providing a logical structure to the application's URLs. It allows for better organization of controller actions and helps in creating meaningful and user-friendly URLs.

### Explain Attribute Based Routing in MVC?

Attribute-Based Routing is an approach in ASP.NET MVC that allows defining the routes directly on the controller actions using attributes. It provides a more declarative way of specifying the routing configuration compared to the conventional route registration.

With Attribute-Based Routing, you can define the URL patterns and their associated actions right above the action methods using the `[Route]` attribute. This approach offers more flexibility in defining custom URL patterns and simplifies the route configuration.

Here's an example of Attribute-Based Routing in MVC:

```csharp
public class HomeController : Controller
{
    [Route("home")]
    public ActionResult Index()
    {
        // Action logic
    }

    [Route("products/{id}")]
    public ActionResult ProductDetails(int id)
    {
        // Action logic
    }
}
```

In the above example, the `[Route]` attribute is used to define the URL patterns for the `Index` and `ProductDetails` actions. The `Index` action is associated with the URL pattern home, while the `ProductDetails` action is associated with the pattern `products/{id}`, where `{id}` is a placeholder for the product ID.

To enable Attribute-Based Routing in an MVC application, you need to add the following line of code in the `RouteConfig.cs` file:

```csharp
routes.MapMvcAttributeRoutes();
```

By calling `MapMvcAttributeRoutes()` method, the routing system scans the controllers and their actions for the `[Route]` attribute and adds them to the routing configuration.

Attribute-Based Routing provides a more intuitive and concise way of defining routes directly on the actions, making the routing configuration more readable and maintainable.

### In which assembly is the MVC Framework defined?

The MVC Framework in ASP.NET is defined in the following assembly:

- Assembly Name: `System.Web.Mvc`
- Namespace: `System.Web.Mvc`

The `System.Web.Mvc` assembly contains the core classes, interfaces, and components that make up the MVC framework. It provides the necessary infrastructure to implement the Model-View-Controller pattern in ASP.NET applications.

To use the MVC framework in your application, you need to reference the `System.Web.Mvc` assembly and import the `System.Web.Mvc` namespace in your code files.

You can add a reference to the `System.Web.Mvc` assembly in your project by either manually browsing to the assembly location or using the NuGet package manager to install the `Microsoft.AspNet.Mvc` package, which will automatically add the reference for you.

By referencing the `System.Web.Mvc` assembly, you gain access to all the classes and features provided by the MVC framework, allowing you to build robust and scalable web applications using the MVC architectural pattern.

## ASP.NET MVC - Routing, Controllers, Views and Razor

### What is the difference between `ViewData`, `ViewBag` & `TempData`?

`ViewData`, `ViewBag`, and `TempData` are all mechanisms provided by ASP.NET MVC to pass data from controllers to views. Here's a brief explanation of each:

- **ViewData:** `ViewData` is a dictionary-like object that is used to pass data from a controller to a view. It uses a key-value pair structure, where data is stored in the `ViewData` dictionary using keys as strings. `ViewData` is a dynamic property of the `ViewBase` class, so you can access it directly within your views. However, since it is a dynamic property, you need to be cautious about type casting when accessing the data.
- **ViewBag:** `ViewBag` is another dynamic property that is introduced in ASP.NET MVC 3. It is a wrapper around `ViewData` that provides a more convenient way to pass data between a controller and a view. Instead of using the key-value pair syntax of `ViewData`, `ViewBag` uses the dot notation to access data. For example, `ViewBag.Message = "Hello";`. However, like `ViewData`, `ViewBag` is also a dynamic property, so you need to be careful with type casting.
- **TempData:** `TempData` is a dictionary-like object used to store data temporarily between two consecutive requests. It is commonly used to transfer data between actions, particularly during redirects. `TempData` is useful when you want to persist data for a short duration across requests. It internally uses session state to store the data. Unlike `ViewData` and `ViewBag`, `TempData` is available for the duration of the user session and will be cleared automatically after the next request.

In summary, `ViewData` and `ViewBag` are similar mechanisms for passing data from controllers to views, with `ViewBag` providing a more convenient syntax. `TempData`, on the other hand, is designed to store data temporarily between requests, typically during redirects.

### How can we pass the data from Controller to View in MVC?

In ASP.NET MVC, there are several ways to pass data from a controller to a view. Here are the commonly used methods:

- **Model:** The preferred and recommended way to pass data is by using a strongly-typed model. You can define a model class representing the data you want to pass to the view, and then pass an instance of that model to the view. The view can then access the model properties directly using the `@Model` directive.
- **ViewData:** `ViewData` is a dictionary-like object provided by MVC to pass data from a controller to a view. It uses a key-value pair structure, where you store data in the `ViewData` dictionary using keys as strings. In the controller, you set the data using `ViewData["key"] = value`, and in the view, you access the data using `@ViewData["key"]`.
- **ViewBag:** `ViewBag` is a dynamic property introduced in ASP.NET MVC 3 as a wrapper around `ViewData`. It provides a more convenient way to pass data between a controller and a view. You can assign values to `ViewBag` properties in the controller, such as `ViewBag.Message = "Hello"`, and then access them in the view using `@ViewBag.Message`.
- **TempData:** `TempData` is another dictionary-like object used to store data temporarily between two consecutive requests. It is commonly used to transfer data between actions, especially during redirects. `TempData` is useful when you want to persist data for a short duration across requests. You can set values in `TempData` using `TempData["key"] = value` in the controller, and then retrieve them in the view using `@TempData["key"]`.

These methods provide flexibility in passing data from controllers to views in MVC. The choice of method depends on your specific requirements and preferences.

### What is Partial View?

A partial view in ASP.NET MVC is a reusable portion of a view that can be rendered within another view. It allows you to encapsulate a specific piece of UI or functionality and reuse it across multiple views. Partial views are commonly used for creating reusable components, such as headers, footers, sidebars, or widgets.

Here are some key points about partial views:

- Partial views are similar to regular views but have the `.cshtml` extension and are typically prefixed with an underscore (`_`).
- They can contain HTML markup, server-side code, and can also be strongly-typed by using a model.
- Partial views can be rendered within other views using the `Html.Partial()` or `Html.RenderPartial()` methods.
- They can also be invoked directly as child actions using the `Html.Action()` or `Html.RenderAction()` methods.
- Partial views can be used to break down complex views into smaller, more manageable components, improving code reusability and maintainability.

By using partial views, you can modularize your MVC application and promote code reusability. This can lead to cleaner and more maintainable code, as well as improved developer productivity.

### What are Areas in MVC?

Areas in ASP.NET MVC are a way to organize and separate different functional areas or modules within an MVC application. They provide a means to divide a large application into smaller, more manageable sections, each with its own set of controllers, views, models, and other related components.

Here are some key points about areas in MVC:

- Areas allow you to group related functionality together and keep the codebase organized.
- Each area has its own folder structure, similar to the main MVC application, containing separate folders for controllers, views, and other related files.
- Areas provide a way to handle routing and URL structure specific to that area, allowing for cleaner and more structured URLs.
- Controllers and views within an area can have the same names as those in other areas, providing a logical separation of functionality.
- Areas can also have their own configuration files, such as `AreaRegistration.cs`, where you can define custom routing rules and other configuration settings specific to the area.

Areas are useful when you have distinct functional modules within your application that require separate organization and encapsulation. They promote a more modular and scalable architecture, making it easier to manage and maintain larger MVC applications.

To create an area in an MVC application, you can use the `AddAreaFolder()` method in the `AreaRegistration` class, which is typically located in the `Areas` folder of the application.

By utilizing areas, you can better structure and organize your MVC application, making it easier to manage, navigate, and maintain over time.

### How we can register the area in ASP.NET MVC?

To register an area in an ASP.NET MVC application, you need to perform the following steps:

1. Create a folder named `Areas` in the root directory of your MVC application if it doesn't already exist.
2. Inside the `Areas` folder, create a new folder for your area, such as `Admin` or `Customer`, which will contain the controllers, views, and other related files for that area.
3. Inside the area folder, create a class that inherits from `AreaRegistration` class, typically named `AreaRegistration.cs`.
4. Override the `AreaName` property to specify the name of the area.
5. Override the `RegisterArea` method and define the routing rules specific to the area using the `MapRoute` method.
6. In the `Global.asax.cs` file, inside the `Application_Start` method, add a call to the `AreaRegistration.RegisterAllAreas()` method.

Here's an example of how the code might look like in the `AreaRegistration.cs` file:

```csharp
using System.Web.Mvc;

namespace YourApplication.Areas.Admin
{
    public class AdminAreaRegistration : AreaRegistration
    {
        public override string AreaName => "Admin";

        public override void RegisterArea(AreaRegistrationContext context)
        {
            context.MapRoute(
                "Admin_default",
                "Admin/{controller}/{action}/{id}",
                new { controller = "Home", action = "Index", id = UrlParameter.Optional }
            );
        }
    }
}
```

By following these steps and registering the area, you can define custom routing rules specific to that area and separate the functionality and resources of your MVC application into distinct areas.

Remember to call `AreaRegistration.RegisterAllAreas()` in the `Application_Start` method of your `Global.asax.cs` file to ensure that the areas are properly registered and the routing rules are applied.

Note: The above example assumes that you have an area named `Admin`. You can replace it with the appropriate name of your area.

Once registered, the controllers and views within the area can be accessed using the specified routing pattern, such as `/Admin/Controller/Action`.

### Explain the concept of MVC Scaffolding?

MVC Scaffolding is a code generation framework in ASP.NET MVC that automates the creation of basic CRUD (Create, Read, Update, Delete) operations for models and their corresponding views and controllers. It is a powerful tool that helps developers quickly generate the boilerplate code required for basic database operations.

With MVC Scaffolding, you can generate the following components for a model:

- **Model class**: Represents the data structure of an entity.
- **Controller class**: Handles the user requests and calls appropriate actions to perform CRUD operations.
- **Views**: Include templates for creating, reading, updating, and deleting records.

Scaffolding saves time and effort by automatically generating the repetitive code for basic CRUD operations based on the model's properties and relationships. It uses templates to define the structure and layout of the generated code, which can be customized to meet specific requirements.

To use MVC Scaffolding, you can follow these steps:

1. Install the necessary scaffolding packages, such as `Microsoft.VisualStudio.Web.CodeGeneration.Design` and `Microsoft.EntityFrameworkCore.Design`, using NuGet package manager.
2. Open the Package Manager Console and run the scaffolding command, specifying the model and the desired options. For example, `Scaffold-DbContext` command is used with Entity Framework to generate the model classes and `MVCController` command is used to generate controllers and views.
3. Provide the required information, such as the connection string, model class, and scaffold options when prompted by the scaffolding command.
4. The scaffolding engine will generate the code files based on the provided information, creating the necessary models, controllers, and views.

By leveraging MVC Scaffolding, developers can quickly generate the basic structure of their application, allowing them to focus on implementing the business logic and customizing the generated code as needed.

> Note: Scaffolding is a powerful tool, but it should be used judiciously. It is best suited for generating initial code or prototypes and may require manual modifications to meet complex business requirements.

### What is Bundling and Minification in MVC?

Bundling and minification are techniques used in ASP.NET MVC to improve the performance and efficiency of web applications by reducing the number and size of the requested resources (such as CSS and JavaScript files) sent to the client.

- **Bundling**: Bundling is the process of combining multiple CSS or JavaScript files into a single file. By bundling files, you can reduce the number of HTTP requests made by the client, which can significantly improve page load time. It also simplifies the management and deployment of CSS and JavaScript files.

    To implement bundling in MVC, you can use the `BundleConfig.cs` file in the `App_Start` folder. In this file, you define bundles by specifying the files that should be bundled together. You can also apply transformations like minification or other optimizations to the bundled files.

- **Minification**: Minification is the process of removing unnecessary characters (such as whitespaces, comments, and line breaks) from CSS and JavaScript files without changing their functionality. Minified files are smaller in size and can be delivered to the client more quickly, resulting in faster page load times.

    In MVC, you can enable minification by using a CSS and JavaScript minifier. There are several libraries and tools available, such as `System.Web.Optimization` or third-party libraries like `YUICompressor.NET`, that perform minification as part of the bundling process.

By bundling and minifying CSS and JavaScript files, you can improve the performance of your MVC application by reducing the network overhead and delivering optimized resources to the client.

> Note: It's important to properly test and validate the bundled and minified resources to ensure they function correctly in your application. Also, keep in mind that bundling and minification may affect debugging and troubleshooting, so it's common practice to disable these optimizations during development to facilitate debugging.

### Is it possible to share a View across multiple Controllers?

Yes, it is possible to share a view across multiple controllers in ASP.NET MVC. This can be useful when you have common functionality or a shared UI component that needs to be used in different parts of your application.

One way to achieve this is by using the `PartialView` feature in MVC. A partial view is a reusable view component that can be rendered within other views. By creating a partial view, you can define the shared UI component or functionality once and then include it in multiple views or even across different controllers.

To share a view using partial views:

1. Create a partial view file (e.g., `_SharedView.cshtml`) in the `Views/Shared` folder or any other desired location.
2. Define the HTML markup, Razor syntax, and any necessary model or ViewData required for the shared view component.
3. In the target views or controllers where you want to include the shared view, use the `Html.Partial` or `Html.RenderPartial` helper methods to render the partial view.

   Example:

   ```csharp
   @Html.Partial("_SharedView")
   ```

You can pass a model or additional ViewData to the partial view if needed.

By using partial views, you can encapsulate common UI components or functionality and reuse them across multiple controllers and views in your MVC application. This promotes code reusability, reduces duplication, and simplifies maintenance.

> Note: It's important to consider the context and purpose of the shared view. Ensure that the shared view is applicable and relevant to all the controllers and views that use it, and make sure to handle any necessary data binding or communication between the shared view and the parent view or controller.

### What is route in MVC? What is default route in MVC?

In ASP.NET MVC, a route is a URL pattern that maps to a specific controller action. It defines how incoming requests are processed and routed to the appropriate controller and action method.

The routing system in MVC uses a set of rules defined in the `RouteConfig.cs` file to match the incoming URLs with the corresponding controller and action.

A default route is a predefined route that is used when no specific route matches the incoming request. It serves as a fallback route and is typically defined as the first route in the route configuration.

By convention, the default route in MVC is typically defined as follows:

```csharp
routes.MapRoute(
    name: "Default",
    url: "{controller}/{action}/{id}",
    defaults: new { controller = "Home", action = "Index", id = UrlParameter.Optional }
);
```

This default route configuration maps URLs with the pattern `/{controller}/{action}/{id}` to the corresponding controller and action method. The `id` parameter is optional and can be omitted.

For example, a URL like `/Home/Index` would map to the `Index` action method in the `HomeController`.

You can customize the route configuration based on your application's requirements. Routes can include placeholders for parameters, constraints, and other configuration options to handle different URL patterns and route to different controllers and actions.

The route configuration is typically defined in the `RouteConfig.cs` file within the `App_Start` folder of an MVC project. You can modify the route configuration to match your desired URL patterns and controller-action mappings.

Note that ASP.NET Core MVC has a different way of configuring routes using the `Startup.cs` file, but the concept of routes and default routes remains similar.

By defining routes and the default route in MVC, you can create clean and meaningful URLs that map to specific controller actions and provide a clear and logical structure to your application's routing system.

### Where are the routing rules defined in an ASP.NET MVC application?

In an ASP.NET MVC application, the routing rules are defined in the `RouteConfig.cs` file. This file is typically located in the `App_Start` folder of the project.

The `RouteConfig.cs` file contains a static method called `RegisterRoutes` that is responsible for configuring the routing rules for the application. This method is called during application startup to register the routes.

Inside the `RegisterRoutes` method, you'll find a `RouteCollection` object (`routes`) on which you can define the routing rules using the `MapRoute` method. The `MapRoute` method takes in parameters such as the route name, URL pattern, default values, and constraints to define how the incoming URLs should be mapped to controllers and actions.

Here's an example of a basic routing rule defined in the `RouteConfig.cs` file:

```csharp
public static void RegisterRoutes(RouteCollection routes)
{
    routes.IgnoreRoute("{resource}.axd/{*pathInfo}");

    routes.MapRoute(
        name: "Default",
        url: "{controller}/{action}/{id}",
        defaults: new { controller = "Home", action = "Index", id = UrlParameter.Optional }
    );
}
```

In the example above, the `MapRoute` method is used to define the default route with the pattern `/{controller}/{action}/{id}`. It specifies that if no specific controller and action are specified in the URL, the `HomeController` and `Index` action method will be used as the defaults.

You can customize the routing rules based on your application's requirements. You can define additional routes, specify constraints on route parameters, and handle different URL patterns.

By modifying the `RouteConfig.cs` file, you can define how incoming requests are mapped to the appropriate controllers and actions in your ASP.NET MVC application.

### Differences between Razor and ASPX View Engine in MVC?

Razor and ASPX are two different view engines available in ASP.NET MVC. Here are the key differences between them:

- **Syntax:** Razor view engine uses a compact and expressive syntax with the `.cshtml` file extension, whereas ASPX view engine uses the traditional ASP.NET Web Forms syntax with the `.aspx` file extension.
- **Code Readability:** Razor provides a more readable and natural syntax for writing HTML and server-side code, thanks to its use of @ symbols for code expressions and blocks. ASPX view engine requires explicit opening and closing tags for server-side code using `<% %>`.
- **IntelliSense Support:** Razor view engine provides better IntelliSense support in Visual Studio, allowing for easier code completion and navigation. ASPX view engine has limited IntelliSense capabilities in comparison.
- **Code Execution:** Razor views are compiled into executable code on the server side, resulting in faster execution. ASPX views, on the other hand, use a code-behind model and are compiled at runtime.
- **Inline Expressions:** Razor supports inline expressions using the `@` symbol, making it easier to mix HTML and server-side code within the same file. ASPX uses server tags (`<% %>` or `<%= %>`) for server-side code, which can make the markup less concise.
- **Layouts and Sections:** Both Razor and ASPX view engines support layouts and sections to provide a consistent structure for views. However, the syntax and usage might differ slightly between the two engines.

Overall, Razor view engine is the recommended choice for new ASP.NET MVC projects due to its clean syntax, better code readability, and improved development experience. However, ASPX view engine is still supported for backward compatibility with existing applications or specific requirements.

It's important to note that the choice of view engine is a matter of personal preference and project requirements. You can switch between Razor and ASPX view engines by configuring the appropriate view engine in your ASP.NET MVC application.

### What are the main Razor Syntax rules?

Razor is a markup syntax used in ASP.NET MVC views to combine server-side code with HTML markup. Here are the main syntax rules of Razor:

- **Code Blocks:** Code blocks in Razor are denoted by the `@` symbol. They can be used to include server-side code within the view. For example: `@{ // code here }`.
- **Expressions:** Expressions are used to output values directly into the HTML markup. They are also denoted by the `@` symbol. For example: `@Model.Property`.
- **Conditional Statements:** Razor supports if, else if, and else statements for conditional logic. They can be written using the `@if`, `@else if`, and `@else` keywords. For example:

   ``` csharp
   @if (condition)
   {
       // code here
   }
   else if (condition)
   {
       // code here
   }
   else
   {
       // code here
   }
   ```

- **Loops**: Razor provides syntax for loops such as `for`, `foreach`, and `while`. They can be written using the `@for`, `@foreach`, and `@while` keywords. For example:

    ``` csharp
    @foreach (var item in collection)
    {
        // code here
    }
    ```

- **Partial Views**: Razor allows rendering of partial views within a view. This can be done using the `@Html.Partial` or `@Html.RenderPartial` methods. For example: `@Html.Partial("_PartialViewName")`.
- **Layouts**: Layouts define the overall structure and design of a page. Razor views can use layouts to provide a consistent structure across multiple views. They can be specified using the `@layout` directive at the top of the view. For example: `@layout "_LayoutName"`.

These are some of the main syntax rules of Razor. It's important to follow these rules while writing Razor views to ensure proper integration of server-side code and HTML markup.

### Explain the need of Display Mode in MVC?

In ASP.NET MVC, display mode is used to provide different views for different devices or clients based on their capabilities. It allows you to create multiple versions of a view and serve the appropriate version based on the requesting client's capabilities.

The need for display mode arises from the fact that different devices have different screen sizes, resolutions, and capabilities. For example, a web page designed for a desktop browser may not be suitable for a mobile device with a smaller screen. By using display mode, you can create separate views tailored to specific devices or groups of devices.

Display mode works by associating a set of conditions with a specific view. These conditions can be based on factors such as the user agent, browser capabilities, screen size, or any other custom criteria. When a request is made to a controller action, the display mode engine selects the appropriate view based on the matching conditions.

By using display mode, you can create a responsive and adaptive user interface that delivers an optimal experience to different devices. It helps in improving the usability and accessibility of your application across a variety of devices.

To configure display mode in MVC, you can use the `DisplayModeProvider` class and register display modes in the `Global.asax.cs` file or in the `Startup.cs` file for ASP.NET Core applications. Display modes can be added for different devices like desktop, mobile, tablet, or any other custom device categories.

Overall, the use of display mode in MVC allows you to deliver a tailored user experience based on the device or client accessing your application, improving usability and user satisfaction.

You can copy and paste the above content into an `.md` file or any markdown editor to preserve the formatting.

### What is Route Constraints in MVC?

In ASP.NET MVC, route constraints are used to restrict the values that can be matched by a route parameter. They provide a way to define rules or conditions that must be satisfied for a URL to match a particular route.

Route constraints are specified as a part of the route definition and help in defining the pattern and format of the route parameter. They allow you to ensure that the values provided in the URL meet specific criteria before they are processed by the associated controller action.

Some commonly used route constraints include:

- **int**: Restricts the parameter to be an integer value.
- **bool**: Restricts the parameter to be a boolean value (`true` or `false`).
- **string**: Restricts the parameter to be a non-empty string value.
- **minlength(n)**: Restricts the minimum length of the parameter value to `n` characters.
- **maxlength(n)**: Restricts the maximum length of the parameter value to `n` characters.
- **range(min, max)**: Restricts the parameter to be within a specified range of values.
- **regex(pattern)**: Restricts the parameter to match a regular expression pattern.

Route constraints are specified by enclosing the constraint within curly braces `{}` in the route template. For example, `{id:int}` specifies a constraint that the `id` parameter must be an integer.

By using route constraints, you can enhance the robustness and security of your application by validating the input parameters before they are processed. They help in preventing potential errors or unexpected behavior by ensuring that the values provided in the URL are of the expected type or format.

### What are the folders in MVC Application Solutions?

An MVC (Model-View-Controller) application solution in ASP.NET typically contains several folders that help organize the different parts of the application. Here are some of the commonly used folders in an MVC application:

- **Models**: This folder contains the model classes that represent the data and business logic of the application. Models are responsible for managing data and implementing the application's rules and behavior.
- **Views**: The Views folder holds the user interface components of the application. It includes the `.cshtml` files (or other view file extensions) that define the HTML markup and presentation logic for rendering the application's output to the user.
- **Controllers**: This folder contains the controller classes that handle user requests, perform business logic, and coordinate the interaction between models and views. Controllers receive requests from the user, process them, and return the appropriate response.
- **Areas**: The Areas folder is used when an application is divided into multiple functional areas, each having its own set of models, views, and controllers. Areas provide a way to organize large applications by grouping related functionality together.
- **Content**: The Content folder contains static files such as CSS, images, and client-side scripts that are used to style and enhance the application's user interface.
- **Scripts**: The Scripts folder is typically used to store JavaScript files that provide client-side interactivity and behavior to the application.
- **App_Data**: This folder is used for storing application data files such as databases or other data sources that the application may require.
- **App_Start**: The App_Start folder contains configuration and startup files for the application. It often includes files like `RouteConfig.cs` for configuring the application's routing rules, `BundleConfig.cs` for bundling and minification settings, and other similar startup files.
- **Areas**: If the application uses areas, each area will have its own folder within the Areas folder, containing the corresponding models, views, and controllers for that specific area.

These folders provide a logical structure for organizing the different components of an MVC application and make it easier to navigate and maintain the codebase.

### What is ViewStart?

ViewStart is a special file in ASP.NET MVC that is used to define common layout and configuration settings for multiple views in an application. It is a per-directory file that is automatically executed before rendering any view within that directory and its subdirectories.

The purpose of the ViewStart file is to provide a central place to define settings that are shared across multiple views. Some common uses of the ViewStart file include:

- **Layout Configuration**: The ViewStart file can be used to specify the layout file that should be used as the base layout for all views in that directory. By setting the `Layout` property, you can define a consistent layout structure for all views within the directory.
- **Default Model**: The ViewStart file can also be used to set a default model that should be passed to all views in that directory. This eliminates the need to specify the model explicitly in each individual view.
- **ViewBag Initialization**: If you need to initialize the ViewBag or ViewData with common data that is required by multiple views, you can do so in the ViewStart file. This ensures that the data is available to all views within the directory.

By defining these settings in the ViewStart file, you can avoid repetition and keep your views consistent and DRY (Don't Repeat Yourself).

> It's important to note that the ViewStart file is hierarchical, meaning that you can have multiple ViewStart files in different directories, each providing different settings for its respective views. The settings in a parent ViewStart file are inherited by child directories unless overridden.

### Explain RenderSection in MVC?

RenderSection is a method in ASP.NET MVC that allows you to define named sections within a layout file and then render content into those sections from individual views. It provides a way to dynamically inject content into specific sections of a layout.

Here's how RenderSection works:

1. In the layout file (typically named `_Layout.cshtml`), you define one or more sections using the `@RenderSection` directive. For example, you can have a section for the page title, scripts, stylesheets, etc. Each section is given a unique name.
2. In the individual views, you can then provide content for those sections using the `@section` directive. You specify the same name as the corresponding section in the layout file.
3. When the view is rendered, the content specified in the view's `@section` directive is injected into the corresponding `@RenderSection` directive in the layout file. This allows you to dynamically customize and extend the layout's content based on the specific view being rendered.

RenderSection is particularly useful when you want to have consistent layout structure but also allow flexibility for individual views to inject their own content into specific sections. It promotes separation of concerns and reusability of layout components.

It's important to note that sections are optional, meaning that views can choose not to provide content for certain sections. In such cases, the corresponding `@RenderSection` directive in the layout file will be empty.

### What is the significance of NonActionAttribute?

The `NonActionAttribute` is an attribute in ASP.NET MVC that is used to mark a public method in a controller as a non-action method. Non-action methods are methods that should not be treated as actions and should not be accessible as HTTP endpoints.

When a method in a controller is marked with the `NonActionAttribute`, it tells the MVC framework that the method should not be considered as an action method and should not be callable via a URL. This is useful when you have public methods in a controller that are intended for internal use within the controller or for reuse by other methods, but should not be directly invoked as actions by the routing system.

Here's an example of how the `NonActionAttribute` can be used:

```csharp
public class MyController : Controller
{
    [NonAction]
    public ActionResult InternalMethod()
    {
        // Logic for the internal method
        return View();
    }

    public ActionResult ActionMethod()
    {
        // Call the internal method
        InternalMethod();

        // Logic for the action method
        return View();
    }
}
```

In the above example, the `InternalMethod` is marked with the `NonActionAttribute`, indicating that it should not be treated as an action method. It can be called within the `ActionMethod`, but it cannot be directly accessed as an HTTP endpoint.

The `NonActionAttribute` is helpful in organizing and separating the public action methods from other methods within a controller, making it clear which methods are intended to be called by external clients and which are intended for internal use.

### How route table is created in ASP.NET MVC?

In ASP.NET MVC, the route table is responsible for mapping incoming URLs to the appropriate controller and action method. The route table is created during the application startup and it defines the routing rules for the MVC application.

The route table is typically defined in the `RouteConfig.cs` file, which is located in the `App_Start` folder of the project. This file contains a static `RegisterRoutes` method that is called during application startup to configure the routes.

Here's an example of how a route table can be created and configured in ASP.NET MVC:

```csharp
public class RouteConfig
{
    public static void RegisterRoutes(RouteCollection routes)
    {
        routes.IgnoreRoute("{resource}.axd/{*pathInfo}");

        routes.MapRoute(
            name: "Default",
            url: "{controller}/{action}/{id}",
            defaults: new { controller = "Home", action = "Index", id = UrlParameter.Optional }
        );
    }
}
```

In the above example, the `RegisterRoutes` method is called during application startup to configure the routes. The `routes` parameter is a `RouteCollection` object that allows you to define the routes.

The `MapRoute` method is used to define a route. It takes in parameters such as the route name, URL pattern, and default values for the controller, action, and any additional parameters.

In the example, the default route maps URLs of the format `/{controller}/{action}/{id}` to the appropriate controller and action method. If no controller, action, or id is specified in the URL, the default values specified in the `defaults` parameter will be used.

You can add additional routes by calling the `MapRoute` method multiple times with different URL patterns and default values.

Remember to call the `RegisterRoutes` method in the `Application_Start` method of the `Global.asax.cs` file to ensure that the route table is properly initialized during application startup.

### ASP.NET MVC application, makes use of settings at 2 places for routing to work correctly. What are these 2 places?

In an ASP.NET MVC application, routing is a critical component that maps incoming URLs to the appropriate controller and action method. To ensure routing works correctly, settings are required to be configured in two places:

1. **RouteConfig.cs**: The first place where routing settings are configured is the `RouteConfig.cs` file, typically located in the `App_Start` folder of the project. This file contains a static `RegisterRoutes` method that is called during application startup to configure the routes. Here, you define the routing rules using the `MapRoute` method, specifying the route name, URL pattern, and default values for the controller, action, and any additional parameters.
2. **Web.config**: The second place where routing settings are required is the `Web.config` file, located in the root folder of the project. In the `system.webServer` section of the `Web.config` file, you need to ensure that the `runAllManagedModulesForAllRequests` setting is set to `true`. This setting allows the routing module (`UrlRoutingModule`) to handle all requests and correctly map them to the appropriate controller and action method.

Both these places play a crucial role in ensuring that routing works correctly in an ASP.NET MVC application. The `RouteConfig.cs` file defines the routing rules, while the `Web.config` file ensures that all requests are handled by the routing module.

### What is the use of the following default route?

The default route in an ASP.NET MVC application is a pre-configured route that is used when no specific route matches the incoming URL. It serves as a fallback route and ensures that requests to the root URL or requests that don't match any defined routes are still handled correctly.

The default route is typically defined in the `RouteConfig.cs` file in the `App_Start` folder of the project. By default, the route template is set to `"{controller}/{action}/{id}"`, which means that the URL should follow the pattern of `/{controller}/{action}/{id}`.

Here's the significance of the default route:

- `{controller}`: This segment of the URL is mapped to the name of the controller that will handle the request. For example, if the URL is `/Home/Index`, the `Home` controller will be invoked.
- `{action}`: This segment is mapped to the name of the action method within the controller that will be executed. In the example above, the `Index` action method will be called.
- `{id}`: This optional segment is typically used to pass additional parameters to the action method. It can be any value that you want to pass as an identifier or parameter to the action method.

The default route allows for a clean and intuitive URL structure by mapping segments of the URL to the corresponding controller and action. It is the most commonly used route in an ASP.NET MVC application and provides a consistent and predictable way of handling requests.

### What is the difference between adding routes, to a WebForms application and to an MVC application?

In a WebForms application, the routing mechanism is not natively supported. The URL routing in WebForms is typically achieved by using ASP.NET Routing module, which needs to be configured separately. It allows you to define custom URL patterns and map them to specific ASPX pages or handlers.

On the other hand, MVC applications have routing as a core part of the framework. The routing system is built-in and is responsible for mapping incoming URLs to specific controllers and action methods. In MVC, the routing is convention-based and follows a pattern defined in the `RouteConfig.cs` file.

The major difference between the two approaches is that WebForms routing is more manual and requires explicit configuration, whereas MVC routing is automatic and follows the convention over configuration principle. In MVC, you define the routes using the `MapRoute` method in the `RouteConfig.cs` file, and the framework takes care of handling the routing based on the configured routes.

Additionally, MVC routing provides more flexibility and control over the URL structure and allows for clean and SEO-friendly URLs. It also supports attribute-based routing, which gives you the ability to define routes directly on the controller or action method using attributes.

Overall, adding routes to an MVC application is a more streamlined and integrated process compared to a WebForms application, where routing needs to be configured separately using additional modules or libraries.

### Which filter executes first in an ASP.NET MVC application?

In an ASP.NET MVC application, the filter execution order follows a specific sequence. The filters are executed in the following order:

1. **Authorization Filters:** Authorization filters are the first filters to be executed. They determine whether the current user is authorized to access the requested resource or action method. Examples of authorization filters include `[Authorize]` and `[AllowAnonymous]` attributes.
2. **Action Filters:** Action filters are executed after authorization filters. They are applied before and after the execution of an action method. Examples of action filters include `[HttpPost]`, `[HttpGet]`, `[ValidateAntiForgeryToken]`, and custom action filters defined by the developer.
3. **Result Filters:** Result filters are executed after the action method has been executed and before the result is returned to the client. They can modify the result or perform additional processing. Examples of result filters include `[OutputCache]`, `[ContentResult]`, and custom result filters defined by the developer.
4. **Exception Filters:** Exception filters are executed when an unhandled exception occurs during the execution of the action method or any filter in the pipeline. They handle and process the exception. Examples of exception filters include `[HandleError]` and custom exception filters defined by the developer.

The filter execution order is designed to follow a logical sequence that allows each filter to perform its specific functionality at the appropriate stage of the request processing.

### What are the levels at which filters can be applied in an ASP.NET MVC application?

In an ASP.NET MVC application, filters can be applied at multiple levels to control the behavior and processing of requests. The levels at which filters can be applied are as follows:

1. **Global Level:** Global filters are applied to all requests in an application. They are registered in the `GlobalFilters` collection in the `FilterConfig` class. Global filters are applied to all controllers and action methods unless explicitly overridden at lower levels.
2. **Controller Level:** Controller filters are applied to all action methods within a specific controller. They can be specified using attributes applied to the controller class or by implementing the `IControllerFilter` interface. Controller filters are applied before and after each action method execution.
3. **Action Level:** Action filters are applied to individual action methods. They can be specified using attributes applied to the action method or by implementing the `IActionFilter` interface. Action filters are executed before and after the execution of an action method.
4. **Result Level:** Result filters are applied to the result of an action method. They can be specified using attributes applied to the action method or by implementing the `IResultFilter` interface. Result filters are executed before and after the result is returned to the client.
5. **Exception Level:** Exception filters are applied to handle exceptions that occur during the execution of an action method or any filter in the pipeline. They can be specified using attributes applied to the action method or by implementing the `IExceptionFilter` interface. Exception filters handle and process exceptions.

By applying filters at different levels, you can control the behavior and processing of requests at various stages in the ASP.NET MVC pipeline.

### Is it possible to create a custom filter?

Yes, in ASP.NET MVC, you can create custom filters by implementing one of the available filter interfaces or by deriving from the `FilterAttribute` class.

To create a custom filter, you can follow these steps:

1. Create a new class that implements one of the following filter interfaces based on your requirement:
   - `IAuthorizationFilter`: For creating custom authorization filters.
   - `IActionFilter`: For creating filters that run before and after the execution of an action method.
   - `IResultFilter`: For creating filters that run before and after the execution of the result.
   - `IExceptionFilter`: For creating filters that handle exceptions that occur during the execution of an action method or any filter in the pipeline.
2. Implement the required methods of the chosen interface. For example, if you implement `IActionFilter`, you need to implement `OnActionExecuting` and `OnActionExecuted` methods.
3. Optionally, you can apply the `AttributeUsage` attribute to define the scope and usage of your custom filter.
4. Register your custom filter in the `FilterConfig` class or using attribute-based registration, depending on your preference.

Once your custom filter is implemented and registered, it can be applied at various levels in your ASP.NET MVC application, such as globally, at the controller level, or at the action level.

### What filters are executed in the end?

In an ASP.NET MVC application, the order of execution for filters is as follows:

1. **Authorization Filters**: These filters are executed first in the pipeline, before any other filter or action method. Examples of authorization filters include `AuthorizeAttribute`.
2. **Action Filters**: These filters are executed before and after the execution of an action method. Examples of action filters include `ActionFilterAttribute`.
3. **Result Filters**: These filters are executed before and after the execution of the result, such as rendering a view or returning a JSON response. Examples of result filters include `ResultFilterAttribute`.
4. **Exception Filters**: These filters are executed when an exception occurs during the execution of an action method or any filter in the pipeline. Examples of exception filters include `HandleErrorAttribute`.

By default, the order of execution is determined by the framework. However, you can modify the order of execution by using filter ordering techniques such as setting the `Order` property on filter attributes or implementing the `IOrderedFilter` interface.

### Is it possible to cancel filter execution?

Yes, it is possible to cancel the execution of filters in an ASP.NET MVC application. This can be achieved by using the `ResultExecutingContext` or `ActionExecutingContext` objects provided by the MVC framework.

To cancel the execution of filters, you can set the `Result` property of the `ResultExecutingContext` object to a new `ActionResult` or `null`. Similarly, in the case of action filters, you can set the `Result` property of the `ActionExecutingContext` object to a new `ActionResult` or `null`. This will stop the execution of subsequent filters and the action method.

Here's an example of canceling filter execution in an action filter:

```csharp
public class CustomActionFilterAttribute : ActionFilterAttribute
{
    public override void OnActionExecuting(ActionExecutingContext filterContext)
    {
        // Cancel filter execution and return a custom result
        filterContext.Result = new ContentResult
        {
            Content = "Filter execution canceled.",
            ContentType = "text/plain"
        };
    }
}
```

You can apply this filter to specific action methods or controller classes by decorating them with the `[CustomActionFilter]` attribute.

### What type of filter does `OutputCacheAttribute` class represents?

The `OutputCacheAttribute` class in ASP.NET MVC represents an output caching filter. Output caching is a technique used to cache the output of a controller action or a partial view, allowing subsequent requests to be served directly from the cache without re-executing the action or rendering the view.

By applying the `OutputCacheAttribute` to a controller action or a partial view, you can specify various caching options such as duration, location, and vary-by parameters. This helps in improving the performance of your application by reducing the processing time and server load for repetitive requests.

Here's an example of applying the `OutputCacheAttribute` to a controller action:

```csharp
[OutputCache(Duration = 3600, Location = OutputCacheLocation.Server)]
public ActionResult Index()
{
    // Action logic
    return View();
}
```

In the above example, the `OutputCacheAttribute` is applied to the Index action with a duration of 3600 seconds (1 hour) and the cache is stored on the server.

### What are the 2 popular ASP.NET MVC view engines?

In ASP.NET MVC, there are two popular view engines:

1. **Razor**: Razor is the default view engine introduced in ASP.NET MVC 3 and is widely used. It provides a concise and expressive syntax for creating dynamic views. Razor views are based on a combination of HTML markup and server-side code enclosed in `@` symbols.
2. **Web Forms**: Web Forms view engine is based on the traditional ASP.NET Web Forms technology. It allows you to use the same familiar syntax and controls as in ASP.NET Web Forms for creating views in an MVC application. However, it is less commonly used compared to Razor.

To specify which view engine to use in an ASP.NET MVC application, you can configure it in the `Global.asax.cs` file using the `ViewEngines.Engines` collection. By default, Razor is configured as the primary view engine.

### What symbol would you use to denote, the start of a code block in Razor views?

In Razor views, you use the `@` symbol to denote the start of a code block or to switch to code execution mode. The `@` symbol is followed by C# code or Razor syntax that you want to execute. For example:

``` csharp
<p>Hello, @Model.Name!</p>
```

In the above example, `@Model.Name` is a code block that accesses the `Name` property of the `Model` object.

### What symbol would you use to denote, the start of a code block in ASPX views?

In ASPX views, you use the `<%` symbol to denote the start of a code block. The `<%` symbol is followed by C# code or ASP.NET server-side code that you want to execute. For example:

``` csharp
<p>Hello, <%= Model.Name %></p>
```
In the above example, `<%= Model.Name %>` is a code block that renders the value of the `Name` property of the `Model` object.

### What are sections?



### What are the file extensions for razor views?



### How do you specify comments using razor syntax?



### Is it possible to combine ASP.NET webforms and asp.MVC and develop a single web application?



### What is the use of viewmodel in MVC?



### Explain bundle.config in MVC4?



### Does `TempData` hold the data for other request in ASP.NET MVC?



### Explain peek method in `TempData` in ASP.NET MVC?



### What are child actions in ASP.NET MVC?



### Can i use razor code in javascript in ASP.NET MVC?



### How can i return string result from action in ASP.NET MVC?



### How to return the json from action method in ASP.NET MVC?



### Give an example for authorization filters in an ASP.NET MVC application?



## ASP.NET MVC - Validation, Security, Authentication & More

### How Validation works in MVC? What is Data Annotation?
### How to implement Security in web applications in MVC?
### What is validation summary in MVC?
### How do you implement forms authentication in MVC?
### What are the methods of handling an error in MVC?
### How can we done custom error page in MVC?
### What is server side validation in MVC?
### What is the use of remote validation in MVC?
### How we can handle the exception at controller level in ASP.NET MVC?
### Explain the tools used for unit testing in ASP.NET MVC?
### What is data annotation validator attributes in MVC?
### What are the exception filters in MVC?
### Which approach provides better support for test driven development – ASP.NET MVC or ASP.NET webforms?

## ASP.NET Core - Basics

### What is XSRF or CSRF? How to prevent cross-site request forgery (XSRF/CSRF) attacks in ASP.NET Core?
### Explain session and state management in ASP.NET Core.
### How to access httpcontext in ASP.NET Core?
### Explain the caching and response caching in ASP.NET Core.
### What is the options pattern in ASP.NET Core?
### How to use multiple environments in ASP.NET Core?
### How ASP.NET Core serve static files?
### Explain session and state management in ASP.NET Core?
### Can ASP.NET application be run in docker containers?
### Explain the caching or response caching in ASP.NET Core?
### How to handle errors in ASP.NET Core?
### What are Razor pages in .NET Core?
### What is host in ASP.NET Core?
### Describe the generic host and web host?
### Describe the servers in ASP.NET Core?
### How configuration works in ASP.NET Core?

## ASP.NET Core - Routing, Files, CORS & More

### What is Routing? Explain attribute routing in ASP.NET Core?
### Explain default project structure in ASP.NET Core application?
### How ASP.NET Core serve static files?
### What are the roles of Appsettings.Json and Launchsetting.Json file in ASP.NET Core?
### What are the various techniques to save configuration settings in ASP.NET Core?
### What is CORS? Why is CORS restriction is required? How to fix CORS error?
### How ASP.NET Core Middleware is different from HttpModule?
### What are the types of Hosting in ASP.NET Core? What is In process and Out of process hosting?

### How to use Dependency Injection in Views in ASP.NET Core?

In ASP.NET Core, views can also benefit from Dependency Injection (DI) to resolve dependencies and access services. Here's how you can use DI in views:

1. **Configure Services**: In the ConfigureServices method of your Startup class, register the required services and dependencies using the services parameter. For example:

    ``` csharp
    services.AddTransient<IMyService, MyService>();
    ```

2. **Inject Services into Controllers**: Inject the required services into your controllers using constructor injection. For example:

    ``` csharp
    public class MyController : Controller
    {
        private readonly IMyService _myService;

        public MyController(IMyService myService)
        {
            _myService = myService;
        }

        // Controller actions...
    }
    ```

3. Use `@inject` Directive in Views: To use dependencies in your views, you can utilize the `@inject` directive. Place the directive at the top of your view file to inject the required service. For example:

    ``` csharp
    @inject IMyService MyService
    ```

4. **Access Services in Views**: Once the service is injected into the view, you can access its properties and methods directly. For example:

    ``` csharp
    @{
        var result = MyService.GetData();
    }
    ```

It's worth noting that views in ASP.NET Core should ideally focus on presentation logic rather than complex business logic. If you find the need for extensive logic in views, it's recommended to extract that logic into dedicated classes or view components, which can be more easily tested and maintained using DI.

### What are the types of Service Lifetimes of an object/ instance in ASP.NET Core?

In ASP.NET Core, there are three types of service lifetimes that determine how instances of objects are managed and shared by the Dependency Injection (DI) container:

- **Transient**: A new instance is created every time it is requested. Transient objects are not shared across different components and are typically suitable for lightweight and stateless services. Each time the service is requested, a new instance is provided.
- **Scoped**: An instance is created once per client request or scope. Scoped objects are shared within the same client request or the same scope instance. When a new client request is made or a new scope is created, a new instance is provided.
- **Singleton**: A single instance is created and shared across the entire application. The same instance is provided whenever the service is requested. Singleton objects are shared across all components and are suitable for stateful services that maintain their state throughout the application's lifetime.

The choice of service lifetime depends on the specific requirements of your application. Transient lifetime is typically used for lightweight, stateless services that don't hold any shared state. Scoped lifetime is commonly used for services that need to maintain state within the scope of a client request. Singleton lifetime is used for services that should have a single instance shared across the entire application.

To specify the lifetime of a service when registering it in the DI container, you can use the following methods:

- **AddTransient**: Registers the service as transient.
- **AddScoped**: Registers the service as scoped.
- **AddSingleton**: Registers the service as singleton.

For example:

```csharp
services.AddTransient<IMyService, MyService>();
services.AddScoped<IMyScopedService, MyScopedService>();
services.AddSingleton<IMySingletonService, MySingletonService>();
```

By understanding the different service lifetimes, you can control the lifecycle and sharing of instances in your ASP.NET Core application.

### What is AddSingleton, AddScoped and AddTransient method?

In ASP.NET Core, the AddSingleton, AddScoped, and AddTransient methods are extension methods provided by the `IServiceCollection` interface to register services in the Dependency Injection (DI) container with different lifetimes.

- **AddSingleton**: This method registers a service with the singleton lifetime. It means that only one instance of the service is created and shared across the entire application. The same instance is provided whenever the service is requested. This is useful for services that need to maintain state or be shared across different components.
- **AddScoped**: This method registers a service with the scoped lifetime. It means that an instance of the service is created once per client request or scope. The same instance is shared within the same client request or scope. When a new client request is made or a new scope is created, a new instance is provided. This is useful for services that need to maintain state within the scope of a client request.
- **AddTransient**: This method registers a service with the transient lifetime. It means that a new instance of the service is created every time it is requested. Transient objects are not shared across different components. Each time the service is requested, a new instance is provided. This is useful for lightweight and stateless services.

Here's an example of how these methods can be used:

``` csharp
services.AddSingleton<ISingletonService, MySingletonService>();
services.AddScoped<IScopedService, MyScopedService>();
services.AddTransient<ITransientService, MyTransientService>();
```
In the above example, `ISingletonService` will have a singleton lifetime, `IScopedService` will have a scoped lifetime, and `ITransientService` will have a transient lifetime.

By using these methods to register services, you can control the lifecycle and sharing behavior of the instances in your application's DI container.

### What is Middleware in ASP.NET Core? What is custom middleware?

In ASP.NET Core, middleware is software components that are used to handle requests and responses in the request pipeline. Each middleware component in the pipeline can inspect, modify, or short-circuit the request/response as it flows through the pipeline.

Middleware components are responsible for performing specific tasks such as authentication, logging, routing, error handling, caching, and more. They can be combined and ordered to form a pipeline that defines the processing flow of an incoming request.

Custom middleware refers to middleware components that are created by developers to add custom functionality to the request pipeline. Custom middleware can be used to implement specific business logic, modify request/response headers, handle custom authentication/authorization schemes, or perform any other custom processing required by the application.

To create custom middleware in ASP.NET Core, you need to implement a class that conforms to the `IMiddleware` interface or use the `UseMiddleware` extension method to create inline middleware. Custom middleware can be added to the pipeline using the `app.UseMiddleware` method in the `Configure` method of the `Startup` class.

Here's an example of a custom middleware class that logs request information:

``` csharp
public class RequestLoggingMiddleware : IMiddleware
{
    public async Task InvokeAsync(HttpContext context, RequestDelegate next)
    {
        // Log request information
        LogRequest(context.Request);

        // Call the next middleware in the pipeline
        await next(context);
    }

    private void LogRequest(HttpRequest request)
    {
        // Log request information
        Console.WriteLine($"Request: {request.Method} {request.Path}");
    }
}
```

To use this custom middleware, you can add it to the pipeline in the Configure method of the Startup class:

``` csharp
public void Configure(IApplicationBuilder app)
{
    // Other middleware configurations...

    app.UseMiddleware<RequestLoggingMiddleware>();

    // Other middleware configurations...
}
```

By adding the custom middleware to the pipeline, it will be executed for each incoming request, allowing you to perform the desired custom processing.

### What is Request Delegate in .NET Core?

In ASP.NET Core, a Request Delegate represents a method that can handle an HTTP request. It is a function that takes an HttpContext object as a parameter and returns a Task representing the asynchronous processing of the request.

The Request Delegate is at the heart of the ASP.NET Core request pipeline. The pipeline is a series of components, called middleware, that each have the ability to process an incoming request and optionally pass it to the next middleware in the pipeline. The Request Delegate is the final middleware in the pipeline that handles the request and generates the response.

The Request Delegate can be defined as a lambda expression, an anonymous method, or a named method. It is typically defined in the Configure method of the Startup class in an ASP.NET Core application. The Configure method is responsible for configuring the middleware pipeline and specifying how each middleware component should handle the request.

Here's an example of a Request Delegate defined as a lambda expression:

``` csharp
app.Use(async (context, next) =>
{
    // Handle the request
    // ...

    // Call the next middleware in the pipeline
    await next.Invoke();
});
```

In the example above, the lambda expression takes an `HttpContext` object as the `context` parameter and a `next` delegate that represents the next middleware in the pipeline. It can perform custom request processing logic and optionally call the `next` delegate to pass the request to the next middleware component.

The Request Delegate plays a critical role in ASP.NET Core as it allows developers to define custom request processing logic and control the flow of the middleware pipeline. It provides the flexibility to handle requests, modify the response, perform authentication, logging, and other tasks required for building web applications.

### What is `Run()`, `Use()` and `Map()` method?

In ASP.NET Core, the `Run()`, `Use()`, and `Map()` methods are used to add middleware components to the request pipeline. Each method serves a different purpose in configuring the middleware pipeline.

- **Run() method**: The `Run()` method is used to add a terminal middleware to the pipeline. It is typically used to handle the request and generate a response, without calling any subsequent middleware components. The `Run()` method takes a `RequestDelegate` parameter, which represents the request processing logic for that specific middleware. Here's an example:

  ``` csharp
  app.Run(async (context) =>
  {
      await context.Response.WriteAsync("Hello, World!");
  });
  ```

  In the above example, the `Run()` method adds a middleware that simply writes "Hello, World!" to the response.

- **Use() method**: The `Use()` method is used to add middleware components to the pipeline that can process the request and optionally call the next middleware in the pipeline. It allows for custom request processing logic and enables building a chain of middleware components. Here's an example:

  ``` csharp
  app.Use(async (context, next) =>
  {
      // Perform some logic before calling the next middleware

      await next.Invoke();

      // Perform some logic after the next middleware has completed
  });
  ```
  In the above example, the `Use()` method adds a middleware component that can handle the request and call the next middleware in the pipeline by invoking the next delegate.

- **Map() method**: The `Map()` method is used to branch the request pipeline based on a specific request path. It allows different middleware components to be executed for different URL paths or routes. Here's an example:

  ``` csharp
  app.Map("/api", apiApp =>
  {
      // Add middleware specific to the "/api" path
      apiApp.UseApiMiddleware();
  });
  ```

  In the above example, the `Map()` method is used to create a new branch in the pipeline for requests with the "/api" prefix. The `UseApiMiddleware()` middleware will only be executed for requests that match the specified path.

These methods provide the flexibility to configure the middleware pipeline in ASP.NET Core, allowing developers to define custom request processing logic and control the flow of the application.

### What is Kestrel? What is the difference between Kestrel and IIS?


### How to read values from appsettings.json file?


## Additional Resources and References

- []()
- []()
- []()
- []()
- []()
- []()
- []()
- []()
- []()
- [ChatGPT-3.5](https://openai.com/blog/chatgpt)
