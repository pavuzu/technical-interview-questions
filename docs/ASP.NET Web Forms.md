# ASP.NET Web Forms

## Contents

- [ASP.NET Web Forms](#aspnet-web-forms)
  - [Contents](#contents)
  - [ASP.NET - Fundamentals](#aspnet---fundamentals)
    - [What are the events in Page Life Cycle? In which event are the controls fully loaded?](#what-are-the-events-in-page-life-cycle-in-which-event-are-the-controls-fully-loaded)
    - [What is the difference between Server.Transfer() and Response.Redirect()?](#what-is-the-difference-between-servertransfer-and-responseredirect)
    - [What are the different types of Caching?](#what-are-the-different-types-of-caching)
    - [What are the types of state management?](#what-are-the-types-of-state-management)
    - [Where the ViewState is stored after the page postback?](#where-the-viewstate-is-stored-after-the-page-postback)
    - [What are the different ways to store session state in asp.net?](#what-are-the-different-ways-to-store-session-state-in-aspnet)
    - [What is cookie less session?](#what-is-cookie-less-session)
    - [How to force all the validation controls to run in a page in web forms?](#how-to-force-all-the-validation-controls-to-run-in-a-page-in-web-forms)
    - [What's the use of response.output.write()?](#whats-the-use-of-responseoutputwrite)
    - [In which event of page cycle is the viewstate available?](#in-which-event-of-page-cycle-is-the-viewstate-available)
    - [From which base class all web forms are inherited?](#from-which-base-class-all-web-forms-are-inherited)
    - [Which validator control you use if you need to make sure the values in two different controls matched?](#which-validator-control-you-use-if-you-need-to-make-sure-the-values-in-two-different-controls-matched)
    - [What is viewstate?](#what-is-viewstate)
    - [How long the items in viewstate exists?](#how-long-the-items-in-viewstate-exists)
    - [What are the different validators in asp.net?](#what-are-the-different-validators-in-aspnet)
    - [How you can add an event handler?](#how-you-can-add-an-event-handler)
    - [Which type of caching will be used if we want to cache the portion of a page instead of whole page?](#which-type-of-caching-will-be-used-if-we-want-to-cache-the-portion-of-a-page-instead-of-whole-page)
    - [Can we have a web application running without web.config file?](#can-we-have-a-web-application-running-without-webconfig-file)
    - [Can we add code files of different languages in app\_code folder?](#can-we-add-code-files-of-different-languages-in-app_code-folder)
    - [What is protected configuration?](#what-is-protected-configuration)
    - [Write code to send e-mail from an asp.net application?](#write-code-to-send-e-mail-from-an-aspnet-application)
    - [How can we prevent browser from caching an aspx page?](#how-can-we-prevent-browser-from-caching-an-aspx-page)
    - [What is the good practice to implement validations in aspx page?](#what-is-the-good-practice-to-implement-validations-in-aspx-page)
    - [What are the event handlers that we can have in global.asax file?](#what-are-the-event-handlers-that-we-can-have-in-globalasax-file)
    - [Which protocol is used to call a web service?](#which-protocol-is-used-to-call-a-web-service)
    - [Explain role based security?](#explain-role-based-security)
    - [How can we apply themes to an asp.net application?](#how-can-we-apply-themes-to-an-aspnet-application)
    - [What is redirectpermanent in asp.net?](#what-is-redirectpermanent-in-aspnet)
    - [Explain the working of passport authentication.](#explain-the-working-of-passport-authentication)
    - [What are the advantages of passport authentication?](#what-are-the-advantages-of-passport-authentication)
    - [What are the asp.net security controls?](#what-are-the-aspnet-security-controls)
    - [How do you register javascript for webcontrols ?](#how-do-you-register-javascript-for-webcontrols-)
    - [Differentiate strong typing and weak typing](#differentiate-strong-typing-and-weak-typing)
    - [List all templates of the repeater control.](#list-all-templates-of-the-repeater-control)
    - [List the major built-in objects in asp.net?](#list-the-major-built-in-objects-in-aspnet)
    - [What is the appsettings section in the web.config file?](#what-is-the-appsettings-section-in-the-webconfig-file)
    - [Which namespaces are necessary to create a localized application?](#which-namespaces-are-necessary-to-create-a-localized-application)
    - [What are the different types of cookies in asp.net?](#what-are-the-different-types-of-cookies-in-aspnet)
    - [What is the file extension of web service?](#what-is-the-file-extension-of-web-service)
    - [Is it possible to create web application with both webforms and mvc?](#is-it-possible-to-create-web-application-with-both-webforms-and-mvc)
    - [Can we have multiple web config files for an asp.net application?](#can-we-have-multiple-web-config-files-for-an-aspnet-application)
    - [What is the difference between web config and machine config?](#what-is-the-difference-between-web-config-and-machine-config)
    - [What is cross page posting?](#what-is-cross-page-posting)


## ASP.NET - Fundamentals

### What are the events in Page Life Cycle? In which event are the controls fully loaded?
### What is the difference between Server.Transfer() and Response.Redirect()?
### What are the different types of Caching?
### What are the types of state management?
### Where the ViewState is stored after the page postback?
### What are the different ways to store session state in asp.net?
### What is cookie less session?
### How to force all the validation controls to run in a page in web forms?
### What's the use of response.output.write()?
### In which event of page cycle is the viewstate available?
### From which base class all web forms are inherited?
### Which validator control you use if you need to make sure the values in two different controls matched?
### What is viewstate?
### How long the items in viewstate exists?
### What are the different validators in asp.net?
### How you can add an event handler?
### Which type of caching will be used if we want to cache the portion of a page instead of whole page?
### Can we have a web application running without web.config file?
### Can we add code files of different languages in app_code folder?
### What is protected configuration?
### Write code to send e-mail from an asp.net application?
### How can we prevent browser from caching an aspx page?
### What is the good practice to implement validations in aspx page?
### What are the event handlers that we can have in global.asax file?
### Which protocol is used to call a web service?
### Explain role based security?
### How can we apply themes to an asp.net application?
### What is redirectpermanent in asp.net?
### Explain the working of passport authentication.
### What are the advantages of passport authentication?
### What are the asp.net security controls?
### How do you register javascript for webcontrols ?
### Differentiate strong typing and weak typing
### List all templates of the repeater control.
### List the major built-in objects in asp.net?
### What is the appsettings section in the web.config file?
### Which namespaces are necessary to create a localized application?
### What are the different types of cookies in asp.net?
### What is the file extension of web service?
### Is it possible to create web application with both webforms and mvc?
### Can we have multiple web config files for an asp.net application?
### What is the difference between web config and machine config?
### What is cross page posting?


