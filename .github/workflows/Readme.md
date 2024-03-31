Prerequites:
Create a Service Principal:

```bash
az ad sp create-for-rbac --name spn-azure-bicep-github --role contributor --scopes /subscriptions/<SUBSCRIPTION_ID> --sdk-auth
---------
output:
---------
{
  "clientId": "1c2b6506-ca7f-4328-b2d5-a205397ce947",
  "clientSecret": "xPk8Q~btWOFh-mDjodrpFB92RxgjT39gJAehlayr",
  "subscriptionId": "e987901a-710f-4edd-b4c6-7c98572d04d5",
  "tenantId": "b96cc57b-d146-48f5-a381-7cf474c23a9e",
  "activeDirectoryEndpointUrl": "https://login.microsoftonline.com",
  "resourceManagerEndpointUrl": "https://management.azure.com/",
  "activeDirectoryGraphResourceId": "https://graph.windows.net/",
  "sqlManagementEndpointUrl": "https://management.core.windows.net:8443/",
  "galleryEndpointUrl": "https://gallery.azure.com/",
  "managementEndpointUrl": "https://management.core.windows.net/"
}
```

More resources:  
https://docs.microsoft.com/en-us/azure/azure-resource-manager/bicep/deploy-github-actions?tabs=CLI
