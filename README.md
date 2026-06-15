# Azure Full-Stack Cloud Development

# Initial Setup

To get started you will need the following software installed:

- Google Chrome
- Node.js
- git (including the Git Credential Manager)
- Visual Studio Code
- Azure Command Line Interface (Azure CLI)
- pnpm (package manager)

Later on in the course we will also use:

- PostgreSQL tools (pgAdmin)
- Redgate Flyway (database versioning)
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
```

Then:

```powershell
npm install -g pnpm
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

# Bicep

Verify Bicep is available:

```bash
az bicep version
```

# First Deployment

```bash
az deployment group create \
  --resource-group course-dev \
  --template-file main.bicep
```

# Learning Objectives

At the end of this section you should be able to:

- Install Azure development tools
- Login to Azure using Azure CLI
- Understand subscriptions
- Understand resource groups
- Deploy infrastructure using Bicep
- Delete Azure resources
