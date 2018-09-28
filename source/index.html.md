---
title: BOC API Reference

language_tabs: # must be one of https://git.io/vQNgJ
  - shell : nodejs
  - ruby : swift
  - javascript
  

toc_footers:
  - <a href='support@greylabs.in'>Sign Up for a Developer Key</a>
  - <a href='https://beacon.greylabs.in'>Documentation Powered by Slate</a>

includes:
  - errors

search: true
---
# Introduction

# Super Admin BOC

It is an account that has complete access to all the available information and services provided by the BOC to all the registered schools.

> To authorize, use this code:

```shell
var http = require("http");

var options = {
  "method": "POST",
  "hostname": [
    "52",
    "66",
    "58",
    "94"
  ],
  "port": "4000",
  "path": [
    "user",
    "driver",
    "Login",
    ""
  ],
  "headers": {
    "Cache-Control": "no-cache",
    "Postman-Token": "4636de98-a62e-4735-b3cd-133cd925c161"
  }
};

var req = http.request(options, function (res) {
  var chunks = [];

  res.on("data", function (chunk) {
    chunks.push(chunk);
  });

  res.on("end", function () {
    var body = Buffer.concat(chunks);
    console.log(body.toString());
  });
});

req.end();
```

```ruby
import Foundation

let headers = [
  "Cache-Control": "no-cache",
  "Postman-Token": "0532a5eb-07c4-4726-b388-ed18dad2353c"
]

let request = NSMutableURLRequest(url: NSURL(string: "http://52.66.58.94:4000/user/driver/Login/")! as URL,
                                        cachePolicy: .useProtocolCachePolicy,
                                    timeoutInterval: 10.0)
request.httpMethod = "POST"
request.allHTTPHeaderFields = headers

let session = URLSession.shared
let dataTask = session.dataTask(with: request as URLRequest, completionHandler: { (data, response, error) -> Void in
  if (error != nil) {
    print(error)
  } else {
    let httpResponse = response as? HTTPURLResponse
    print(httpResponse)
  }
})

dataTask.resume()

```

```javascript
[ var settings = {
  "async": true,
  "crossDomain": true,
  "url": "http://52.66.58.94:4000/user/driver/Login/",
  "method": "POST",
  "headers": {
    "Cache-Control": "no-cache",
    "Postman-Token": "da57f14d-1c4c-4803-bf4e-a41116562eca"
  }
}

$.ajax(settings).done(function (response) {
  console.log(response);
});]
```

> Make sure to replace `meowmeowmeow` with your API key.

Kittn uses API keys to allow access to the API. You can register a new Kittn API key at our [developer portal](http://52.66.58.94:4000/user/driver/Login/).

Kittn expects for the API key to be included in all API requests to the server in a header that looks like the following:

`Authorization: http://52.66.58.94:4000/user/driver/Login/`

<aside class="notice">
You must replace <code>meowmeowmeow</code> with your personal API key.
</aside>

## Analytics

## School
### School(s) List
Here, a list of all the registered schools name is available. You can add new schools Add or edit the existing information about these schools.
### Add School
Here, While adding the school for the first time, you can [click on] ("https://boc.greylabs.in/superadmin#/app/admin/addOrUpdateSchool") the following information must be entered.

### View Childs

### View Routes
### View Buses
### View Drivers
### Edit School
### Fliter By


## Children
### Children List
### Edit Children
### Delete Children
### Filter By
### Search By
### Search


## Parents
### Parents List
### Block
### Search


## Routes
### Routes List
### Add Routes
### Edit Routes
### Delete Routes
### Fliter By School Name
### Search By
### Search


## Request(s)
### Request List
### Edit Request
### Delete Request
### Fliter By School Name
### Search By
### Search

## Driver

### Drivers List
### Add Driver
### Edit Driver
### Driver Compliance
### Delete Driver
### Fliter By School Name
### Search By
### Search

## Buses
### Buses List
### Edit Buses
### Delete Buses
### Fliter By School Name
### Search By
### Search

## Help
### Super Admin Help
### School Admin Help
### Driver App Help
### Parent App Help

# School Admin BOC

## Analytics

## School
### School List
### View Childs.
### View Routes.
### View Buses.
### View Drivers.
### Edit School.

## Children
### Add Children
### Upload CSV File
### Download Sample File
### Children List
### Edit Children
### Delete Children
### Search By
### Search

## Routes
### Route List
### Add Route
### Edit Route
### Delete Route
### Search By
### Search

## Request(s)
### Request(s) List
### Edit Request
### Delete Request
### Search By
### Search

## Driver
### Drivers List
### Add Driver
### Edit Driver
### Driver Compliance
### Delete Driver
### Search By
### Search

## Buses
### Bus List
### Add Bus
### Edit Bus
### Delete Bus
### Search By
### Search

## Help
### School Admin Help
### Driver App Help
### Parent App Help

> To authorize, use this code:

```ruby
require 'kittn'

api = Kittn::APIClient.authorize!('meowmeowmeow')
```

```python
import kittn

api = kittn.authorize('meowmeowmeow')
```

```shell
# With shell, you can just pass the correct header with each request
curl "api_endpoint_here"
  -H "Authorization: meowmeowmeow"
```

```javascript
const kittn = require('kittn');

let api = kittn.authorize('meowmeowmeow');
```

> Make sure to replace `meowmeowmeow` with your API key.

Kittn uses API keys to allow access to the API. You can register a new Kittn API key at our [developer portal](http://example.com/developers).

Kittn expects for the API key to be included in all API requests to the server in a header that looks like the following:

`Authorization: meowmeowmeow`

<aside class="notice">
You must replace <code>meowmeowmeow</code> with your personal API key.
</aside>


# Driver App BOC

## Login

For a driver to start using the Beacon Driver app, the driver should :

*a. Have registered with the Beacon BOC.*

*b. Created a profile with their mobile number and a password.*

> To authorize, use this code:

```shell
var http = require("http");

var options = {
  "method": "POST",
  "hostname": [
    "52",
    "66",
    "58",
    "94"
  ],
  "port": "4000",
  "path": [
    "user",
    "driver",
    "Login",
    ""
  ],
  "headers": {
    "Cache-Control": "no-cache",
    "Postman-Token": "4636de98-a62e-4735-b3cd-133cd925c161"
  }
};

var req = http.request(options, function (res) {
  var chunks = [];

  res.on("data", function (chunk) {
    chunks.push(chunk);
  });

  res.on("end", function () {
    var body = Buffer.concat(chunks);
    console.log(body.toString());
  });
});

req.end();
```

```ruby
import Foundation

let headers = [
  "Cache-Control": "no-cache",
  "Postman-Token": "0532a5eb-07c4-4726-b388-ed18dad2353c"
]

let request = NSMutableURLRequest(url: NSURL(string: "http://52.66.58.94:4000/user/driver/Login/")! as URL,
                                        cachePolicy: .useProtocolCachePolicy,
                                    timeoutInterval: 10.0)
request.httpMethod = "POST"
request.allHTTPHeaderFields = headers

let session = URLSession.shared
let dataTask = session.dataTask(with: request as URLRequest, completionHandler: { (data, response, error) -> Void in
  if (error != nil) {
    print(error)
  } else {
    let httpResponse = response as? HTTPURLResponse
    print(httpResponse)
  }
})

dataTask.resume()

```

```javascript
 var settings = {
  "async": true,
  "crossDomain": true,
  "url": "http://52.66.58.94:4000/user/driver/Login/",
  "method": "POST",
  "headers": {
    "Cache-Control": "no-cache",
    "Postman-Token": "da57f14d-1c4c-4803-bf4e-a41116562eca"
  }
}

$.ajax(settings).done(function (response) {
  console.log(response);
});
```

Request:

Method : Post

Url : http://52.66.58.94:4000/user/driver/Login/

Key | Value
---------------- | ----------------
Phone | 8180873363
Password | 123456
OsVersion | 7.0
DeviceID | 56282e7a7d0b9c43
DeviceModel | Micromax Micromax Q437
gcmld | ftkv-Y0PmxE:APA91bFiuNVh35452kjRXbayoXVX4M0xMxSo1OdFuD94eYGuHiUl1c6Ix1r2zNANfZK3A7o3BxQdp8kA-TVo9r0JYx4eN4QP_lOn_EECOWsuc6hvG7e1QHYXp395qEIquHl7oP0cmUi6
DeviceType | Android

Response :

Response Condition | Response Json

> The above command returns JSON structured like this:

```json
    "driver": {
        "_id": "5b850d9a0a458c40ab513e56",
        "fullName": "Ajay Android",
        "modifiedOn": "2018-09-28T12:07:52.024Z",
        "password": "",
        "schoolOrBranch": {
            "_id": "5ac21271b7275c3a6b2c010c",
            "emergencyContactNumber": "9860369199",
            "verifyString": "$2a$08$makaogp8hshraTWtxyXlkuoS.D7XswyeTY4cjmE6NKve5Ky8OEOti",
            "mainBranch": "5ac21271b7275c3a6b2c010d",
            "mobile": "9860369199",
            "firstName": "Praveen Prasad",
            "schoolType": "SCHOOL",
            "schoolRegYear": null,
            "schoolRegNo": "CV-1",
            "schoolName": "City Vista",
            "__v": 0,
            "isEmailVerified": true,
            "createdOn": "2018-04-02T11:22:26.055Z",
            "role": "branchAdmin",
            "address": {
                "LonLat": [
                    73.945672,
                    18.565381
                ],
                "addressLine1": "pavan reddy pg",
                "landMark": "EON IT Park",
                "city": "Pune",
                "state": "Maharashtra",
                "pinCode": "411014",
                "addressLine2": "EON IT Park"
            },
            "local": {
                "password": "$2a$08$yfsFEhYBOk1edu/pqJwfoOBL8z.nH8uIVBf1z2ewGUwbsPV/NT9GC",
                "email": "nikash@greylabs.in"
            }
        },
        "phone": "8180873363",
        "employeeId": "AJ3363",
        "gender": "",
        "dob": null,
        "lastName": "Android",
        "firstName": "Ajay",
        "__v": 6,
        "createdOn": "2018-08-28T08:53:46.781Z",
        "deviceDetails": [
            {
                "_id": "5b9f82dd868f466ad0a94cec",
                "osVersion": "7.0",
                "deviceId": "56282e7a7d0b9c43",
                "deviceModel": "Micromax Micromax Q437",
                "gcmId": "ftkv-Y0PmxE:APA91bFiuNVh35452kjRXbayoXVX4M0xMxSo1OdFuD94eYGuHiUl1c6Ix1r2zNANfZK3A7o3BxQdp8kA-TVo9r0JYx4eN4QP_lOn_EECOWsuc6hvG7e1QHYXp395qEIquHl7oP0cmUi6",
                "deviceType": "Android",
                "isVerified": false,
                "otp": ""
            },
            {
                "_id": "5ba20d9f7453284fe46a311d",
                "osVersion": "7.0",
                "deviceId": "b2805bfb7f400060",
                "deviceModel": "motorola Moto G (4)",
                "gcmId": "dTjlIBVN7g8:APA91bFuA5hZhzbblMcBKb1KeuqRAIBSnP8oHnR43CI8iDwKiErPv0vbbwrWMm6I6SBaKxUphJCgAqX7DiiUVxnHAy9cPDEcgjThom1ttSo3yXKkoPPRYaTKp6rwryuYPVb0nwlw3dlt",
                "deviceType": "Android",
                "isVerified": false,
                "otp": null
            },
            {
                "_id": "5babdeec7453284fe46a3a20",
                "osVersion": "6.0",
                "deviceId": "3be0e9d34a217e1e",
                "deviceModel": "unknown Android SDK built for x86",
                "gcmId": "e9FV2smzhRw:APA91bGFcirtSG59I6VGqsKwjXqMGOim08gtkwi464ThejNShFo25yA4HjMK95O8ZcztyPjG4AF-FbO4ThPHOTXjGNA6rFXonRycyBYf_sEf1tH-sDLOPxIHm-yEzuiKtx7roPnzB12b",
                "deviceType": "Android",
                "isVerified": false,
                "otp": null
            }
        ],
        "status": "Active",
        "role": "Driver",
        "HTdriverid": null
    },
    "statusMessage": "Login Success",
    "status": "Success"
```




## Trips
### To Be Completed
#### Start Trip

### Completed

## Reload.

## Sidebar
### Report Emergency
### Help
### Chenge Password
### Logout

## Emergency Contact 


# Parents App BOC
## Login
## Home
### Track Bus
### Notification

## Sidebar
### Home
### Your Children
### Dashboard
### Change Mobile
### Notification
### Settings
### Emergency Contact
### FAQs
### Logout