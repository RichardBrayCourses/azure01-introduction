# Azure Full-Stack Cloud Development

# Initial Setup

To get started you will need the following software installed:

- Google Chrome
- Node.js
- git (including the Git Credential Manager)
- Visual Studio Code
- Azure Command Line Interface (Azure CLI)
- Azure Bicep CLI
- .NET SDK
- Entity Framework Core CLI tools
- pnpm (package manager)

The course uses Azure SQL Database Serverless with Entity Framework Core migrations, so you do not need to install:

- PostgreSQL or pgAdmin
- Redgate Flyway
- Docker

For now, let's focus on the core tools above.

## Mac Setup

### Step 1 - install Homebrew

Visit:

https://brew.sh

and follow the installation instructions.

### Step 2 - update your shell startup file

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

### Step 3 - install software

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

### Step 4 - configure git

```bash
git-credential-manager configure
git config --global user.name "Your Name"
git config --global user.email "you@example.com"
```

## Windows Setup

```powershell
Set-ExecutionPolicy -Scope CurrentUser -ExecutionPolicy RemoteSigned

winget install Google.Chrome
winget install Git.Git
winget install OpenJS.NodeJS
winget install Microsoft.VisualStudioCode
winget install Microsoft.AzureCLI
az bicep install
winget install Microsoft.DotNet.SDK.8
```

Then:

```powershell
npm install -g pnpm
dotnet tool install --global dotnet-ef
```

Configure git:

```powershell
git-credential-manager configure
git config --global user.name "Your Name"
git config --global user.email "you@example.com"
```

# Azure Login

Login using your Microsoft account:

```bash
az login
```

Verify your account:

```bash
az account show
```

# Resource Groups

Create a resource group:

```bash
az group create --name course-dev --location uksouth
```

# First Deployment

Before deploying, verify Bicep is available:

```bash
az bicep version
```

```bash
az deployment group create \
  --resource-group course-dev \
  --template-file main.bicep
```

# Learning Objectives

At the end of this section you should be able to:

- Install Azure development tools
- Login to Azure using Azure CLI
- Verify .NET and Entity Framework Core tooling
- Understand subscriptions
- Understand resource groups
- Deploy infrastructure using Bicep
- Delete Azure resources
