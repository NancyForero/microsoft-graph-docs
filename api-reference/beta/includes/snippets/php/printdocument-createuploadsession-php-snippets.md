---
description: "Automatically generated file. DO NOT MODIFY"
---

```php

<?php

// THIS SNIPPET IS A PREVIEW FOR THE KIOTA BASED SDK. NON-PRODUCTION USE ONLY
$graphServiceClient = new GraphServiceClient($requestAdapter);

$requestBody = new CreateUploadSessionPostRequestBody();
$properties = new PrintDocumentUploadProperties();
$properties->setDocumentName('TestFile.pdf');

$properties->setContentType('application/pdf');

$properties->setSize(4533322);


$requestBody->setProperties($properties);


$result = $graphServiceClient->print()->sharesById('printerShare-id')->jobsById('printJob-id')->documentsById('printDocument-id')->createUploadSession()->post($requestBody);


```