# Storage & VNET example template

This template creates a stroage account and a virtual network with three subnets

## Pre-requisits

* An Azure account 
* AZ CLI 2

## How to deploy

### Login

```bash
az login
az account list -o table
az account set -s 'xxxxx'
```

### Create the resource group and deploy

```
az group create --name azdemo --location northeurope
az group deployment create --name azdemo --resource-group azdemo --template-file .\azuredeploy.json
```

### Cleanup

```
az group delete --name azdemo --yes --no-wait
```
### Deploy to Azure
<a href="https://portal.azure.com/#create/Microsoft.Template/uri/https%3A%2F%2Fraw.githubusercontent.com%2Fyooakim%2Farm%2Fmaster%2Fstorage-vnet-example%2Fazuredeploy.json" target="_blank">
    <img src="http://azuredeploy.net/deploybutton.png"/>
</a>
<a href="http://armviz.io/#/?load=https%3A%2F%2Fraw.githubusercontent.com%2Fyooakim%2Farm%2Fmaster%2Fstorage-vnet-example%2Fazuredeploy.json" target="_blank">
    <img src="http://armviz.io/visualizebutton.png"/>
</a>

