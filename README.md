# 🚀 Démo DevDay 2025 – FluentUI Blazor

Dans cette présentation, nous allons découvrir comment utiliser FluentUI Blazor v5 pour créer une petite application de démonstration avec quelques composants essentiels. L’objectif est de montrer la simplicité d’intégration et la puissance des composants **FluentUI** dans un projet Blazor moderne.

## ⚙️ Étapes d’installation

1. Créer un nouveau projet Blazor

```bash
dotnet new blazor -n DevDay25 --empty
```

1. Add this nuget.config file to the root of your project.

Add this nuget.config file to the root of your project. During the development phase of v5, the package is placed in this NuGet feed. You must check the Preview box to view it in your package manager.

```xml
<?xml version="1.0" encoding="utf-8"?>
<configuration>
  <packageSources>
    <clear />
    <add key="nuget" value="https://api.nuget.org/v3/index.json" />
    <add key="dotnet9" value="https://pkgs.dev.azure.com/dnceng/public/_packaging/dotnet9/nuget/v3/index.json" />
  </packageSources>
</configuration>
```

1. Ajouter le package NuGet FluentUI Blazor

Use the NuGet Package Manager or run the following command in your terminal:

```bash
dotnet add package Microsoft.FluentUI.AspNetCore.Components --prerelease
dotnet add package Microsoft.FluentUI.AspNetCore.Components.Icons
```

1. Add Imports

In your _Imports.razor file, include:

```razor
@using Microsoft.FluentUI.AspNetCore.Components
@using Icons = Microsoft.FluentUI.AspNetCore.Components.Icons
```

1. Configurer les services FluentUI

In your `Program.cs`, register the Fluent UI services:

```razor
// Register Fluent UI services
builder.Services.AddFluentUIComponents();
```

In `MainLayout.razor` or your main layout component, add this component at the end of your page:

```razor
@* Add all FluentUI Blazor Providers *@
<FluentProviders />
```
