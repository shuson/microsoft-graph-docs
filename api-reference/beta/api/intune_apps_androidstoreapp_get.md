﻿# Get androidStoreApp

> **Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.

Read properties and relationships of the [androidStoreApp](../resources/intune_apps_androidstoreapp.md) object.
### Prerequisites
One of the following **scopes** is required to execute this API:

*DeviceManagementApps.ReadWrite.All; DeviceManagementApps.Read.All*
### HTTP Request
<!-- {
  "blockType": "ignored"
}
-->
```http
GET /deviceAppManagement/mobileApps/{mobileAppId}
GET /deviceAppManagement/mobileApps/{mobileAppId}/userStatuses/{userAppInstallStatusId}/app/
GET /deviceAppManagement/mobileApps/{mobileAppId}/deviceStatuses/{mobileAppInstallStatusId}/app/
GET /deviceAppManagement/mobileApps/{mobileAppId}/groupAssignments/{mobileAppGroupAssignmentId}/app/
```

### Optional query parameters
This method supports the [OData Query Parameters](http://graph.microsoft.io/docs/overview/query_parameters) to help customize the response.
### Request headers
|Header|Value|
|---|---|
|Authorization|Bearer &lt;token&gt; Required.|
|Accept|application/json|

### Request body
Do not supply a request body for this method.

### Response
If successful, this method returns a `200 OK` response code and [androidStoreApp](../resources/intune_apps_androidstoreapp.md) object in the response body.

### Example
##### Request
Here is an example of the request.
```http
GET https://graph.microsoft.com/beta/deviceAppManagement/mobileApps/{mobileAppId}
```

##### Response
Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.
```http
HTTP/1.1 200 OK
Content-Type: application/json
Content-Length: 1437

{
  "value": {
    "@odata.type": "#microsoft.graph.androidStoreApp",
    "id": "1f2b7654-7654-1f2b-5476-2b1f54762b1f",
    "displayName": "Display Name value",
    "description": "Description value",
    "publisher": "Publisher value",
    "largeIcon": {
      "@odata.type": "microsoft.graph.mimeContent",
      "type": "Type value",
      "value": "dmFsdWU="
    },
    "createdDateTime": "2017-01-01T00:02:43.5775965-08:00",
    "lastModifiedDateTime": "2017-01-01T00:00:35.1329464-08:00",
    "isFeatured": true,
    "privacyInformationUrl": "https://example.com/privacyInformationUrl/",
    "informationUrl": "https://example.com/informationUrl/",
    "owner": "Owner value",
    "developer": "Developer value",
    "notes": "Notes value",
    "uploadState": 11,
    "installSummary": {
      "@odata.type": "microsoft.graph.mobileAppInstallSummary",
      "installedDeviceCount": 4,
      "failedDeviceCount": 1,
      "notInstalledDeviceCount": 7,
      "installedUserCount": 2,
      "failedUserCount": 15,
      "notInstalledUserCount": 5
    },
    "appStoreUrl": "https://example.com/appStoreUrl/",
    "minimumSupportedOperatingSystem": {
      "@odata.type": "microsoft.graph.androidMinimumOperatingSystem",
      "v4_0": true,
      "v4_0_3": true,
      "v4_1": true,
      "v4_2": true,
      "v4_3": true,
      "v4_4": true,
      "v5_0": true,
      "v5_1": true
    }
  }
}
```


