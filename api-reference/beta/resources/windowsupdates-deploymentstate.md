---
title: "deploymentState resource type"
description: "**TODO: Add Description**"
author: "**TODO: Provide Github Name. See [topic-level metadata reference](https://msgo.azurewebsites.net/add/document/guidelines/metadata.html#topic-level-metadata)**"
localization_priority: Normal
ms.prod: "**TODO: Add MS prod. See [topic-level metadata reference](https://msgo.azurewebsites.net/add/document/guidelines/metadata.html#topic-level-metadata)**"
doc_type: resourcePageType
---

# deploymentState resource type

Namespace: microsoft.graph.windowsUpdates

[!INCLUDE [beta-disclaimer](../../includes/beta-disclaimer.md)]

Describes and controls the current state of a deployment.

## Properties
|Property|Type|Description|
|:---|:---|:---|
|effectiveSinceDateTime|String (DateTimeOffset)|Date on which the current state became effective. Read-only.|
|reasons|[deploymentStateReason](../resources/windowsupdates-deploymentstatereason.md) collection|Specifies the reasons the deployment has its state value. Read-only.|
|requestedValue|String (requestedDeploymentStateValue)|Specifies the requested state of the deployment. Possible values are: `none`, `paused`, `archived`.|
|value|String (deploymentStateValue)|Specifies the state of the deployment. Read-only. Possible values are: `scheduled`, `offering`, `paused`, `faulted`, `archived`.|

## Relationships
None.

## JSON representation
The following is a JSON representation of the resource.
<!-- {
  "blockType": "resource",
  "@odata.type": "microsoft.graph.windowsUpdates.deploymentState"
}
-->
``` json
{
  "@odata.type": "#microsoft.graph.windowsUpdates.deploymentState",
  "value": "String",
  "reasons": [
    {
      "@odata.type": "microsoft.graph.windowsUpdates.deploymentStateReason"
    }
  ],
  "requestedValue": "String",
  "effectiveSinceDate": "String (timestamp)"
}
```

