---
title: "expeditedQualityUpdateReference resource type"
description: "**TODO: Add Description**"
author: "**TODO: Provide Github Name. See [topic-level metadata reference](https://msgo.azurewebsites.net/add/document/guidelines/metadata.html#topic-level-metadata)**"
localization_priority: Normal
ms.prod: "**TODO: Add MS prod. See [topic-level metadata reference](https://msgo.azurewebsites.net/add/document/guidelines/metadata.html#topic-level-metadata)**"
doc_type: resourcePageType
---

# expeditedQualityUpdateReference resource type

Namespace: microsoft.graph.windowsUpdates

[!INCLUDE [beta-disclaimer](../../includes/beta-disclaimer.md)]

A reference to specific quality update content to expedite. In a deployment, the same softwareUpdateReference could result in devices receiving different update revisions, but the content is considered contextually equivalent for all devices in the deployment.


Inherits from [qualityUpdateReference](../resources/windowsupdates-qualityupdatereference.md).

## Properties
|Property|Type|Description|
|:---|:---|:---|
|classification|qualityUpdateClassification|Specifies the classification of the referenced content. Default value is security. Inherited from [qualityUpdateReference](../resources/windowsupdates-qualityupdatereference.md). Possible values are: `all`, `security`, `nonSecurity`.|
|equivalentContent|equivalentContentOption|Specifies other content to consider as equivalent. Default value is latestSecurity. Possible values are: `none`, `latestSecurity`.|
|releaseDateTime|DateTimeOffset|Specifies a quality update in the given servicingChannel with the given classification by its publish date (i.e. the last update published on the specified date). Any devices with an update that was published prior to the releaseDate will receive an expedited quality update. Inherited from [qualityUpdateReference](../resources/windowsupdates-qualityupdatereference.md)|

## Relationships
None.

## JSON representation
The following is a JSON representation of the resource.
<!-- {
  "blockType": "resource",
  "@odata.type": "microsoft.graph.windowsUpdates.expeditedQualityUpdateReference"
}
-->
``` json
{
  "@odata.type": "#microsoft.graph.windowsUpdates.expeditedQualityUpdateReference",
  "classification": "String",
  "releaseDate": "String (timestamp)",
  "equivalentContent": "String"
}
```

