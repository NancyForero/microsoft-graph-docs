---
description: "Automatically generated file. DO NOT MODIFY"
---

```csharp

var graphClient = new GraphServiceClient(requestAdapter);

var requestBody = new Microsoft.Graph.Beta.Print.Shares.Item.Jobs.Item.Documents.Item.CreateUploadSession.CreateUploadSessionPostRequestBody
{
	Properties = new PrintDocumentUploadProperties
	{
		DocumentName = "TestFile.pdf",
		ContentType = "application/pdf",
		Size = 4533322L,
	},
};
var result = await graphClient.Print.Shares["{printerShare-id}"].Jobs["{printJob-id}"].Documents["{printDocument-id}"].CreateUploadSession.PostAsync(requestBody);


```