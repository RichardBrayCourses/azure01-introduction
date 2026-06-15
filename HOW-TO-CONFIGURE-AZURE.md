# Instructions for configuring Azure CLI

## Login

```bash
az login
```

A browser window will open.

Sign in with your Azure account and subscription.

## Verify configuration

```bash
az account show
az account list
```

Useful checks:

```bash
az account show --query name
az account show --query id
az account show --query tenantId
```
