---
description: "Automatically generated file. DO NOT MODIFY"
---

```csharp

var graphClient = new GraphServiceClient(requestAdapter);

var requestBody = new Microsoft.Graph.Beta.Admin.Windows.Updates.UpdatableAssets.Item.MicrosoftGraphWindowsUpdatesAddMembersById.AddMembersByIdPostRequestBody
{
	Ids = new List<string>
	{
		"String",
		"String",
		"String",
	},
	MemberEntityType = "#microsoft.graph.windowsUpdates.azureADDevice",
};
await graphClient.Admin.Windows.Updates.UpdatableAssets["{updatableAsset-id}"].MicrosoftGraphWindowsUpdatesAddMembersById.PostAsync(requestBody);


```