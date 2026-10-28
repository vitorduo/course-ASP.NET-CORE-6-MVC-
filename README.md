# Lanches Mac: snack sales website (ASP.NET Core 6 MVC)

Study project: a functional snack sales website ("lanches" means snacks in Portuguese), built with ASP.NET Core 6 MVC while following the Udemy course "ASP.NET Core MVC - Creating a Website from Scratch (.NET 6)". The user interface is in Portuguese.

## Features

Based on the project's commit history and code structure:

- Snack catalogue with categories, a search bar to find snacks by name, and pagination with data filtering
- A view component that shows a snack dropdown in the menu
- Order details pages, backed by a SQL Server database
- Authentication and authorization with ASP.NET Core Identity, including an Access Denied page
- Admin area to manage snacks, categories and orders, with a menu shown only to admin users
- Orders report filtered by period, with PDF export (FastReport)
- Custom Tag Helper (EmailTagHelper) and a contact page

## Tech stack

- C# and ASP.NET Core 6 MVC (net6.0), Razor views, HTML, CSS and JavaScript
- Entity Framework Core 6 (SQL Server provider) with migrations
- ASP.NET Core Identity (Entity Framework Core store)
- FastReport Open Source for PDF reports
- ReflectionIT.Mvc.Paging for pagination

## Project structure

All code is in LanchesMac/LanchesMac:

- Areas/Admin: admin area (controllers and views for snacks, categories, orders and reports)
- Controllers, Views, ViewModels: MVC layers for the public site
- Models, Context, Migrations: domain model, EF Core DbContext and database migrations
- Repositories and Services: data access and application services
- Components and TagHelpers: view components and custom Tag Helpers
- wwwroot: static files (CSS, JavaScript, product images and generated reports)

## Getting started

Requirements: .NET 6 SDK, SQL Server (the default connection string targets a local SQL Server Express instance with Windows authentication) and, optionally, Visual Studio 2022.

1. Clone the repository.
2. In LanchesMac/LanchesMac/appsettings.json, set ConnectionStrings:DefaultConnection to your own SQL Server instance.
3. Create the database from the existing migrations: dotnet ef database update
4. Run the app: dotnet run
5. Product images are read from wwwroot/images/produtos, and generated reports are written to wwwroot/reports.

## Notes

This is a learning project and is not intended for production use. The connection string in the repository points to a local development database and contains no credentials.
