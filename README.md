---
page_type: sample
languages:
- nodejs
- javascript
products:
- azure
- azure-app-service
description: "This sample demonstrates a tiny Hello World Node.js app for Azure App Service."
---

# Node.js Hello World

This sample demonstrates a tiny Hello World node.js app for [App Service Web App](https://docs.microsoft.com/azure/app-service-web).  
and deployed this app into azure web app service using azure pipelines

## Microsoft Entra ID authentication

This app now validates Microsoft Entra ID access tokens for API requests.

Required environment variables:

- `AZURE_AD_TENANT_ID`: Your Azure AD tenant ID, or `common` for multi-tenant apps.
- `AZURE_AD_CLIENT_ID`: The Application (client) ID of the registered app in Microsoft Entra ID.

Requests to `/api`, `/api/me`, and all `/api/accounts` endpoints require a bearer token in the `Authorization` header.

Example request:

```bash
curl -H "Authorization: Bearer <access_token>" http://localhost:3000/api
```

To get a token, register an application in Microsoft Entra ID and request an access token for the application ID URI or client ID.

## Contributing

This project has adopted the [Microsoft Open Source Code of Conduct](https://opensource.microsoft.com/codeofconduct/). For more information see the [Code of Conduct FAQ](https://opensource.microsoft.com/codeofconduct/faq/) or contact [opencode@microsoft.com](mailto:opencode@microsoft.com) with any additional questions or comments.
