---
title: "Create azureADDevice"
description: "Create a new azureADDevice object."
author: "**TODO: Provide Github Name. See [topic-level metadata reference](https://msgo.azurewebsites.net/add/document/guidelines/metadata.html#topic-level-metadata)**"
localization_priority: Normal
ms.prod: "**TODO: Add MS prod. See [topic-level metadata reference](https://msgo.azurewebsites.net/add/document/guidelines/metadata.html#topic-level-metadata)**"
doc_type: apiPageType
---

# Create azureADDevice
Namespace: microsoft.graph.windowsUpdates

[!INCLUDE [beta-disclaimer](../../includes/beta-disclaimer.md)]

Create a new [azureADDevice](../resources/windowsupdates-azureaddevice.md) object.

## Permissions
One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).

|Permission type|Permissions (from least to most privileged)|
|:---|:---|
|Delegated (work or school account)|**TODO: Provide applicable permissions.**|
|Delegated (personal Microsoft account)|**TODO: Provide applicable permissions.**|
|Application|**TODO: Provide applicable permissions.**|

## HTTP request

<!-- {
  "blockType": "ignored"
}
-->
``` http
POST /admin/windows/updates/updatableAssets
```

## Request headers
|Name|Description|
|:---|:---|
|Authorization|Bearer {token}. Required.|
|Content-Type|application/json. Required.|

## Request body
In the request body, supply a JSON representation of the [azureADDevice](../resources/windowsupdates-azureaddevice.md) object.

The following table shows the properties that are required when you create the [azureADDevice](../resources/windowsupdates-azureaddevice.md).

|Property|Type|Description|
|:---|:---|:---|
|id|String|The Azure AD identifier for the device.|


## Response

If successful, this method returns a `201 Created` response code and an [azureADDevice](../resources/windowsupdates-azureaddevice.md) object in the response body.

## Examples

### Request
<!-- {
  "blockType": "request",
  "name": "create_azureaddevice_from_"
}
-->
``` http
POST https://graph.microsoft.com/beta/admin/windows/updates/updatableAssets
Content-Type: application/json
Content-length: 313

{
  "@odata.type": "#microsoft.graph.windowsUpdates.azureADDevice",
  "id": "983f03cd-03cd-983f-cd03-3f98cd033f98"
}
```


### Response
**Note:** The response object shown here might be shortened for readability.
<!-- {
  "blockType": "response",
  "truncated": true,
  "@odata.type": "microsoft.graph.windowsUpdates.azureADDevice"
}
-->
``` http
HTTP/1.1 201 Created
Content-Type: application/json

{
  "@odata.type": "#microsoft.graph.windowsUpdates.azureADDevice",
  "id": "983f03cd-03cd-983f-cd03-3f98cd033f98",
  "errors": [
    {
      "@odata.type": "microsoft.graph.windowsUpdates.azureADDeviceRegistrationError"
    }
  ],
  "enrollments": [
    {
      "@odata.type": "microsoft.graph.windowsUpdates.updateManagementEnrollment"
    }
  ]
}
```

