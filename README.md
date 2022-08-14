# Table of Contents

- [Table of Contents](#table-of-contents)
  - [Introduction](#introduction)
  - [Prerequisites](#prerequisites)
    - [.NET 6.0](#net-60)
    - [Visual Studio 2022](#visual-studio-2022)
    - [Required Workloads](#required-workloads)
  - [Demo](#demo)
    - [Create a secure ASP.NET Core Web API Application](#create-a-secure-aspnet-core-web-api-application)
  - [Summary](#summary)
  - [Complete Code](#complete-code)
  - [Resources](#resources)

## Introduction

In this episode, we are going to build a secure `ASP.NET Core Web API` application, and deploy it to `Azure`. Then, we are going to build a `.NET Multi-platform App UI (.NET MAUI)` application, and I am going to show you how you can leverage `Microsoft Authentication Library (MSAL)` for `.NET` to get an access token, which we are going to use to call the Web API application.

The `Microsoft Authentication Library (MSAL)` allows you to acquire tokens from the `Microsoft identity platform`, authenticate users, and call secure web APIs not only from .NET, but from multiple platforms such as JavaScript, Java, Python, Android, and iOS.

You can find more information about `MSAL` here [Overview of the Microsoft Authentication Library (MSAL)](https://docs.microsoft.com/en-us/azure/active-directory/develop/msal-overview)

End results will look like this:

![Logs](images/REPLACE_HERE)

Let's get started.

## Prerequisites

The following prerequisites are needed for this demo.

### .NET 6.0

Download the latest version of the .NET 6.0 SDK [here](https://dotnet.microsoft.com/en-us/download).

### Visual Studio 2022

For this demo, we are going to use the latest version of [Visual Studio 2022](https://visualstudio.microsoft.com/vs/community/).

### Required Workloads

In order to build ASP.NET Core Web API applications, the `ASP.NET and web development` workload needs to be installed. In order to build `.NET MAUI` applications, you also need the `.NET Multi-platform App UI development` workload, so if you do not have them installed let's do that now.

![ASP.NET and web development](images/34640f10f2d813f245973ddb81ffa401c7366e96e625b3e59c7c51a78bbb2056.png)  

## Demo

In the following demo we will perform the following actions:

1. Create a secure `ASP.NET Core Web API` application
2. Deploy the `ASP.NET Core Web API` application in Azure
3. Create and configure an `Azure B2C` app registration to provide authentication workflows
4. Create a `.NET MAUI` application
5. Configure our `.NET MAUI` application to authenticate users and get an access token
6. Call our secure `ASP.NET Core Web API` application from our `.NET MAUI` application

As you can see there are many steps in this demo, so let's get to it.

### Create a secure ASP.NET Core Web API Application

![Create a new ASP.NET Core Web API project](images/e735adc8086673e19e0b451f7e5530b1b15d2813ed7cb7baa561628baae02fd6.png)  

![Configure your new project](images/326751c8c729d6f3f4df012ecc1b25e50842d88fb060779a7e0cb65f678013f6.png)  

![Additional information](images/864d4dced70426006a4d89d11602e92413aff3be5a5bfbadac695e02e0268673.png)  

>:point_up: Notice I unchecked `Use controllers (uncheck to use minimal APIs)` to create a minimal API, and checked `Enable OpenAPI support` to include `Swagger`.

You can learn more about minimal APIs here: [Minimal APIs overview](https://docs.microsoft.com/en-us/aspnet/core/fundamentals/minimal-apis?view=aspnetcore-6.0>)

Run the application to make sure the default templates is working.

![Swagger](images/c4e367405fe55e086ab137bceadeb459658f1ae989aa1340a1aa1bc93c361937.png)  

Expand `GET /WeatherForecast`, click on `Try it out`, then on `Execute`.

![WeatherForecast](images/0e3cb4491bc38c9171d5b0d069bd8517ab2655e8b32b379e768869754c66b338.png)  

We get data, so it is working, but it is not secure.

Let's make our `ASP.NET Core Web API` app secure.



## Summary

For more information about the `Microsoft Authentication Library (MSAL)`, check out the links in the resources section below.

## Complete Code

The complete code for this demo can be found in the link below.

- <https://github.com/payini/MsalAuthInMaui>

## Resources

| Resource Title                                          | Url                                                                             |
| ------------------------------------------------------- | ------------------------------------------------------------------------------- |
| The .NET Show with Carl Franklin                        | <https://www.youtube.com/playlist?list=PL8h4jt35t1wgW_PqzZ9USrHvvnk8JMQy_>      |
| Download .NET                                           | <https://dotnet.microsoft.com/en-us/download>                                   |
| Overview of the Microsoft Authentication Library (MSAL) | <https://docs.microsoft.com/en-us/azure/active-directory/develop/msal-overview> |
| Minimal APIs overview                                          | <https://docs.microsoft.com/en-us/aspnet/core/fundamentals/minimal-apis?view=aspnetcore-6.0>                |
