---
title: "Get deviceRegistrationPolicy"
description: "Read the properties and relationships of a deviceRegistrationPolicy object."
author: "myra-ramdenbourg"
ms.localizationpriority: medium
ms.prod: "directory-management"
doc_type: apiPageType
---
# Get deviceRegistrationPolicy

Namespace: microsoft.graph

Read the properties and relationships of a [deviceRegistrationPolicy](../resources/deviceregistrationpolicy.md) object. Represents deviceRegistrationPolicy quota restrictions, additional authentication, and authorization policies to register device identities to your organization.

## Permissions
One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).

|Permission type|Permissions (from least to most privileged)|
|:---|:---|
|Delegated (work or school account)| Policy.Read.All, Policy.ReadWrite.DeviceConfiguration|
|Delegated (personal Microsoft account)|Not supported|
|Application|Not supported|

When calling on behalf of a user, the user needs to belong to the following [Azure AD roles](/azure/active-directory/roles/permissions-reference):
+ Global administrator
+ Cloud device administrator
+ Global reader

## HTTP request

<!-- {
  "blockType": "ignored"
}
-->
```http
GET /policies/deviceRegistrationPolicy
```

## Request headers

|Name|Description|
|:---|:---|
|Authorization|Bearer {token}. Required.|

## Request body

Do not supply a request body for this method.

## Response

If successful, this method returns a `200 OK` response code and a [deviceRegistrationPolicy](../resources/deviceregistrationpolicy.md) object in the response body.

## Examples

### Request

<!-- {
  "blockType": "request",
  "name": "get_deviceregistrationpolicy"
}
-->
``` http
GET https://graph.microsoft.com/v1.0/policies/deviceRegistrationPolicy
```

### Response

The following is an example of a response that shows the default settings for the device registration policy.

>**Note:** The response object shown here might be shortened for readability.
<!-- {
  "blockType": "response",
  "truncated": true,
  "@odata.type": "microsoft.graph.deviceRegistrationPolicy"
}
-->
``` http
HTTP/1.1 200 OK
Content-Type: application/json

{
    "@odata.context": "https://graph.microsoft.com/v1.0/$metadata#deviceRegistrationPolicy",
    "id": "deviceRegistrationPolicy",
    "displayName": "Device Registration Policy",
    "description": "Tenant-wide policy that manages intial provisioning controls using quota restrictions, additional authentication and authorization checks",
    "userDeviceQuota": 50,
    "multiFactorAuthConfiguration": "0",
    "azureADRegistration": {
        "appliesTo": "1",
        "isAdminConfigurable": false,
        "allowedUsers": [],
        "allowedGroups": []
    },
    "azureADJoin": {
        "appliesTo": "1",
        "isAdminConfigurable": true,
        "allowedUsers": [],
        "allowedGroups": []
    }
}
```