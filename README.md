# dotnet-8-dapper-sqlite-crud-api

.NET 8 + VS Code - Ready for setup Unit Testing by xUnit and Code Coverage in ASP.NET Core

# Last updated

- 11-11-2024

# Source code
dotnet-8-dapper-sqlite-crud-api

# .NET Version
.NET 8

# DB
SQLite

# ORM
Dapper

# Development

Create the Initial Migration for SQLite DB - should work for any DB

set ASPNETCORE_ENVIRONMENT=Development

dotnet ef migrations add InitialCreate --context DataContext --output-dir Migrations/SqliteMigrations

# Create the local SQLite DB

dotnet run

# Production

Create a self contained build for production at the remote server / traditionel web hotel

dotnet publish webapi.csproj --configuration Release --runtime win-x86 --self-contained

Upload the build to remote server ( without SQLite DB )

At my remote servers the web.config needs to be without the folowing:

hostingModel="inprocess"

# Create the remote SQLite DB

Now you can create the remote SQLite DB at the remote server by type the url:

remote-host.com/users





