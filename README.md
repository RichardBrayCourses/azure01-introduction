# Azure Full-Stack Cloud Development

## Course Overview

This course builds a complete cloud-native web application using Microsoft Azure services, infrastructure and development tools.

The application is developed incrementally across the course. Each section adds a practical production feature and shows how frontend applications, ASP.NET Core APIs, Azure SQL databases, authentication, storage, messaging, monitoring and infrastructure automation work together in a real Azure architecture.

## Azure Course Architecture

The course uses technologies commonly found in Azure and Microsoft enterprise environments:

- React, TypeScript, Vite, Tailwind CSS and Shadcn UI for the frontend
- C# and ASP.NET Core Web API for backend HTTP endpoints
- Entity Framework Core for data access and database migrations
- Azure SQL Database Serverless and Microsoft SQL Server for relational data
- Microsoft Entra External ID for authentication
- Azure Blob Storage for uploaded images and files
- Event Grid and Azure Queue Storage for event-driven processing
- Application Insights and Azure Monitor for observability
- Azure Key Vault for secrets and configuration
- Azure Role-Based Access Control for permissions
- Azure DNS, Azure Managed Certificates, Azure Static Web Apps and Azure Front Door for web hosting and delivery
- Bicep for infrastructure as code

## Initial Setup

To get started you will install the core development tools used throughout the course:

- Google Chrome
- Node.js LTS
- Git with Git Credential Manager
- Visual Studio Code
- Azure CLI
- Azure Bicep CLI
- .NET SDK 10 LTS
- Entity Framework Core CLI tools
- pnpm

Node.js is required for the React, TypeScript, Vite, Tailwind CSS and Shadcn UI frontend tooling. The backend is built with C# and ASP.NET Core.

## Mac Setup

### Step 1 - Install Homebrew

Visit:

https://brew.sh

Follow the installation instructions.

### Step 2 - Update Your Shell Startup File

Check which shell you are using:

```bash
echo $SHELL
```

For zsh:

```bash
echo 'eval "$(/opt/homebrew/bin/brew shellenv)"' >> ~/.zprofile
```

For bash:

```bash
echo 'eval "$(/opt/homebrew/bin/brew shellenv)"' >> ~/.bash_profile
```

Restart your terminal after updating the shell startup file.

### Step 3 - Install Software

```bash
brew install --cask google-chrome
brew install git
brew install node
brew install --cask git-credential-manager
brew install --cask visual-studio-code
brew install azure-cli
az bicep install
brew install --cask dotnet-sdk
dotnet tool install --global dotnet-ef
brew install pnpm
```

### Step 4 - Configure Git

```bash
git-credential-manager configure
git config --global user.name "Your Name"
git config --global user.email "you@example.com"
```

## Windows Setup

Open PowerShell as your normal user.

```powershell
Set-ExecutionPolicy -Scope CurrentUser -ExecutionPolicy RemoteSigned

winget install Google.Chrome
winget install Git.Git
winget install OpenJS.NodeJS.LTS
winget install Microsoft.VisualStudioCode
winget install Microsoft.AzureCLI
az bicep install
winget install Microsoft.DotNet.SDK.10
```

Then install pnpm and the Entity Framework Core CLI tools:

```powershell
npm install -g pnpm
dotnet tool install --global dotnet-ef
```

Configure Git:

```powershell
git-credential-manager configure
git config --global user.name "Your Name"
git config --global user.email "you@example.com"
```

## Verify Your Installation

Run these commands to confirm the development tools are available:

```bash
node --version
npm --version
pnpm --version
git --version
az --version
az bicep version
dotnet --version
dotnet ef --version
```

## Azure Login

Login using your Microsoft account:

```bash
az login
```

Verify your active Azure account:

```bash
az account show
```

## Learning Objectives

At the end of this section you should be able to:

- Identify the Azure services used in the course architecture
- Install the frontend, backend and Azure development tools
- Configure Git and Git Credential Manager
- Verify Node.js, pnpm, Azure CLI, Bicep, .NET and Entity Framework Core tooling
- Login to Azure using Azure CLI
