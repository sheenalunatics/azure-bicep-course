## Deploy Bicep template using Azure CLI

```bash
# create resource group
az group create --name spn-azure-bicep-github --location southeastasia

# preview changes
az deployment group what-if --resource-group spn-azure-bicep-github \
   --template-file webapp-linux.bicep \
   --parameters webAppName='webappbicepx'

# deploy the web app using Bicep
az deployment group create --resource-group spn-azure-bicep-github \
   --template-file webapp-linux.bicep \
   --parameters webAppName='webappbicepx'
```

More templates are available here:
https://github.com/Azure/bicep/blob/main/docs/examples/
