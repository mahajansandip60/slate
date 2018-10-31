---
title: BOC API Reference

language_tabs: # must be one of https://git.io/vQNgJ
  - shell : nodejs
  - ruby : swift
  - javascript
  

toc_footers:
  - <a href='greylabs.in'>Goto Official Web Portal</a>
  - <a href='support@greylabs.in'>Sign Up for a Developer Key</a>
  - <a href='https://beacon.greylabs.in'>Documentation Powered by Slate</a>

includes:
  - errors

search: true
---

# Introduction

**YOUR NEXT-GEN TRANSPORT OPERATIONS & SECURITY SOLUTION**




# Super Admin BOC

<aside class="notice">
BOC is an abbreviation for Beacon Operation Console. It is the centralised portal for managing all the databases with respect to the schools and their students, who are accessing Beacon supported transportation facilities. 
It is an account that has complete access to all the available information and services provided by the BOC to all the registered schools.
</aside>

**URL :** [https://boc.greylabs.in/superadmin#/login](https://boc.greylabs.in/superadmin#/login) 

> To authorize, use this code:

```shell
```

```ruby
```

```javascript
```
## Login

A user can Login into the portal using the provided credentials, this includes an email and a password.

## Sidebar

The BOC has seven modules which are visible in the left-side panel. They are:

## Dashboard

Here, a summary of school's total register driver, total register route's, total register student, total register parent, etc.

## Analytics

## School

This module is a comprehensive module of all the information relevent to all the registered schools. It helps access all the information of a particular in the same location.

### School(s) List

Here, a list of all the registered schools name is available. You can add new schools Add or edit the existing information about these schools.

> To authorize, use this code:

```shell
var qs = require("querystring");
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
    "admin",
    "getAllSchoolsOrSchool",
    ""
  ],
  "headers": {
    "Content-Type": "application/x-www-form-urlencoded",
    "cache-control": "no-cache",
    "Postman-Token": "cbe4d990-f2e5-44cd-afaa-17ca2e781ed5"
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

req.write(qs.stringify({ role: 'branchAdmin', schoolId: '5ac21271b7275c3a6b2c010c' }));
req.end();
```

```ruby
import Foundation

let headers = [
  "Content-Type": "application/x-www-form-urlencoded",
  "cache-control": "no-cache",
  "Postman-Token": "e703063d-59b7-419d-bc3e-b7de7e1aeed1"
]

let postData = NSMutableData(data: "role=branchAdmin".data(using: String.Encoding.utf8)!)
postData.append("&schoolId=5ac21271b7275c3a6b2c010c".data(using: String.Encoding.utf8)!)

let request = NSMutableURLRequest(url: NSURL(string: "http://52.66.58.94:4000/user/admin/getAllSchoolsOrSchool/")! as URL,
                                        cachePolicy: .useProtocolCachePolicy,
                                    timeoutInterval: 10.0)
request.httpMethod = "POST"
request.allHTTPHeaderFields = headers
request.httpBody = postData as Data

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
  "url": "http://52.66.58.94:4000/user/admin/getAllSchoolsOrSchool/",
  "method": "POST",
  "headers": {
    "Content-Type": "application/x-www-form-urlencoded",
    "cache-control": "no-cache",
    "Postman-Token": "7de0d8f2-7ffa-405c-b9e6-d401d3e8a568"
  },
  "data": {
    "role": "branchAdmin",
    "schoolId": "5ac21271b7275c3a6b2c010c"
  }
}

$.ajax(settings).done(function (response) {
  console.log(response);
});
```

**Request**

**Method :** POST.

**URL :** [http://52.66.58.94:4000/user/admin/getAllSchoolsOrSchool/](http://52.66.58.94:4000/user/admin/getAllSchoolsOrSchool/)

**Header :**

Key | Value
--- | ---
Content-Type | application/x-www-form-urlencoded

**Body Parameter :**

Key | Value
--- | ---
role | branchAdmin
schoolId | 5ac21271b7275c3a6b2c010c


> The above command returns JSON structured like this:

```json
{
    "statusMessage": "The available school(s).",
    "status": "Success",
    "schools": {
        "_id": "5ac21271b7275c3a6b2c010c",
        "emergencyContactNumber": "9860369199",
        "verifyString": "$2a$08$makaogp8hshraTWtxyXlkuoS.D7XswyeTY4cjmE6NKve5Ky8OEOti",
        "mainBranch": {
            "_id": "5ac21271b7275c3a6b2c010d",
            "organisationName": "City Vista Org"
        },
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
    "count": 1
}
```


### Add School

Here, While adding the school for the first time, you can click on below url and information must be entered.

> To authorize, use this code:

```shell
var qs = require("querystring");
var http = require("https");

var options = {
  "method": "POST",
  "hostname": [
    "boc",
    "greylabs",
    "in"
  ],
  "path": [
    "superadmin"
  ],
  "headers": {
    "Content-Type": "application/x-www-form-urlencoded",
    "cache-control": "no-cache",
    "Postman-Token": "08c9de23-d49b-4954-bedd-ab3566c8e020"
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

req.write(qs.stringify({ role: 'branchAdmin',
  schoolId: 'all',
  limit: '10',
  skip: '0',
  sortName: 'schoolName',
  sortValue: '-1' }));
req.end();
```

```ruby
import Foundation

let headers = [
  "Content-Type": "application/x-www-form-urlencoded",
  "cache-control": "no-cache",
  "Postman-Token": "d5889b5f-1386-4227-bfce-8bf63058a039"
]

let postData = NSMutableData(data: "role=branchAdmin".data(using: String.Encoding.utf8)!)
postData.append("&schoolId=all".data(using: String.Encoding.utf8)!)
postData.append("&limit=10".data(using: String.Encoding.utf8)!)
postData.append("&skip=0".data(using: String.Encoding.utf8)!)
postData.append("&sortName=schoolName".data(using: String.Encoding.utf8)!)
postData.append("&sortValue=-1".data(using: String.Encoding.utf8)!)

let request = NSMutableURLRequest(url: NSURL(string: "https://boc.greylabs.in/superadmin#/app/admin/addOrUpdateSchool")! as URL,
                                        cachePolicy: .useProtocolCachePolicy,
                                    timeoutInterval: 10.0)
request.httpMethod = "POST"
request.allHTTPHeaderFields = headers
request.httpBody = postData as Data

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
  "url": "https://boc.greylabs.in/superadmin#/app/admin/addOrUpdateSchool",
  "method": "POST",
  "headers": {
    "Content-Type": "application/x-www-form-urlencoded",
    "cache-control": "no-cache",
    "Postman-Token": "62ff8769-5312-46a7-9699-acfdb712a7e2"
  },
  "data": {
    "role": "branchAdmin",
    "schoolId": "all",
    "limit": "10",
    "skip": "0",
    "sortName": "schoolName",
    "sortValue": "-1"
  }
}

$.ajax(settings).done(function (response) {
  console.log(response);
});
```

**Request**

**Method :** POST

**URL :** [http://52.66.58.94:4000/superadmin#/app/admin/addOrUpdateSchool](http://52.66.58.94:4000/superadmin#/app/admin/addOrUpdateSchool)

**Header**

key | value
---- | ----
Content-Type | application/x-www-form-urlencoded

**Body Parameter :**

key | value
---- | ----
role | branchAdmin
schoolId | all
limit | 10
skip | 0
sortName | schoolName
sortValue | -1

> The above command returns JSON structured like this:

```json

```

### View Childs

Here, Super admin click on view childs button, Redirect to All child's information as you selected. 

### View Routes

Here, super admin click on view route button, Redirect to all registred route page as you selected.

### View Buses

Here, super admin click on view buses button, Redirect to all buses information page as you selected.

### View Drivers

Here, super admin click on view drivers button, Redirect to drivers information page.

### Edit School

Here, super admin click on edit school button, Redirect to edit school information page.

### Fliter By

Here, super admin click on filter by Drop Down list to filter by School names.




## Children

This module is a cumulative collection of all the children from all the different schools.

**URL :** [http://52.66.58.94:4000/superadmin#/app/admin/children](http://52.66.58.94:4000/superadmin#/app/admin/children)

### Children List

Here, super admin click on Children menu to get all children's list for all school's.

### View Children Details

Here, Super admin perform action to viwe children details to redirect the child's details page as you selected.

### Edit Children

Here, Super admin perform action on Edit children to redirect the edit child's information as well as Parant info and Route info also.

#### Add New Parent

Super admin perform action on edit children to redirect the edit child's info page, now click on Parent info tab and show you Add New Parent Button. If you want add new parent to selected child's click on Add new parent button and Fill Parent information. 

#### Search existing Parent

Super admin perform action on edit children to redirect the edit child's info page, now click on Parent info tab and show you Add existing Parent Button. If you want add existing parent to selected child's click on Search existing parent button and fill the existing parent mobile number under search box.

### Delete Children

Super admin perform action on Delete children to search children name and click on Delete children button.

### Filter By

There are filter specific School Child's by School Name.

### Search By

Searching for a child based on information in a category is made simpler with this *First Name/Last Name, Roll Number and Class*. 

### Search

Search for a child based on search by category selected as selected. 

## Parents

This module is a cumulative collection of all the parents registered on the BOC.

### Parents List

This is would display a list of all registered parents.

### Action Status

This is woild display a status of given parent *Active or Block*.

### Search

If the parent has already been registered, this method can be used Search directy.

## Routes

This module is a cumulative collection of all the route's registered on the BOC.

### Routes List

Super admin can view information on all the school’s routes.

### Add Routes

Super admin can add the route manually by clicking on Add Route button and Fill the basic route information.

### Edit Routes

Super admin can update the route information by clicking on edit route button and update basic information.

### Delete Routes

Super admin can perform action to delete route on school route's by clicking on Delete route button. 

### Fliter By School Name

There are filter specific School Child's by School Name.

### Search By

Searching for a child based on information in a category is made simpler with this *First Name/Last Name, Roll Number and Class*. 

### Search

Search for a child based on search by category selected as selected. 

## Request(s)

This module is collection of all request made by the parents to the school admin.

### Request List

The Super admin can view the list of pending requests sent by parents.

### Edit Request

Super Admin can click on the edit button to see parent’s requests and approve or reject it.

### Delete Request

Super Admin can click on the Delete button to see parent’s requests has be Deleted.

### Fliter By School Name

There are filter specific School Request by School Name.

### Search By

Searching for a Request based on information in a category is made simpler with this *Requested Childs and Class/Grade*. 

### Search

Search for a Request based on search by category selected as selected. 

## Driver

This is a cummulative collection of all the registered drivers on the BOC.

### Drivers List

The School admin can view the list of the driver’s detail on the driver’s tab.

### Add Driver

Super admin can click on Add Driver button to add the driver’s details including
the driver’s Image. and set the password for him.

### Edit Driver

Super admin can click on Edit Driver button to Update the driver’s details including
the driver’s Image. and set the password for him.

### Driver Compliance

This feature is used to update all required documents of the driver, namely - ID proof, License and Registration Number.

### Delete Driver

Super admin can click on Delete Driver button to Delete the driver’s full details.

### Fliter By School Name

There are filter specific School Driver by School Name.

### Search By

Searching for a Driver based on information in a category is made simpler with this *Driver Name, Phone Number and Employee Id*. 

### Search

Search for a Driver based on search by category selected as selected. 

## Buses

This module is a cumulative record of all the buses registered on the BOC.

### Buses List

Super admin can view the all buses to register school only to click on Bus tab.

### Add Buses

Super admin can click the add bus button and he can fill the bus basic information.

### Edit Buses

Super admin can click the Edit bus button and he can update the bus basic information.

### Delete Buses

Super admin can click on Delete Bus button to delete the all details for selected bus.

### Fliter By School Name

There are filter specific School Buses by School Name.

### Search By

Searching for a Bus based on information in a category is made simpler with this *Bus Name and Bus Registeration number*. 

### Search

Search for a bus based on search by category selected as selected. 

## Help

This module lets the super admin to have a help documents for *Super Admin Help, School Admin Help, Parents App Help and Driver App Help.* to click on Help Module

# School Admin BOC

<aside class="notice">BOC is an abbreviation for Beacon Operation Console. It is the centralised portal for managing all the databases with respect to the schools and their students, who are accessing Beacon supported transportation facilities.</aside>

Portal Address: [https://boc.greylabs.in/#/login.](https://boc.greylabs.in/#/login)

## Login

A user can Login into the portal using the provided credentials, this includes an email and a password.


## Dashboard

  

## School

This module is a comprehensive module of all the information relevent to all the registered schools. It helps access all the information of a particular in the same location.

### School List

This is essential a list of registered schools. School admin are perform verious action on this page like View Child List, Viwe Route's, view Buses, View Driver's and Edit School Information. 

### View Childs.

This is essential a list of all child's. In this page admin are perform veriou action like : Viwe children Details, Edit Children information and Delete Children.

### View Routes.

This is essential a list of all route's assign to School. 

### View Buses.

This is essential a list of all Buses.

### View Drivers.

This is essential a list of all Driver's registered in our school.

### Edit School.




## Children

This module is a cumulative collection of all the children's from all the different schools.

### Children List

This module is a camulative collection of all the children for all schools as you added.

### Add Children

The School admin can add a new child by clicking on *"Add Child"* button and fill in the relevant information. There are three important forms that need to be filled while adding a child, namely: 

*1) Child Information :* This form requires information about the child.

*2) Parent Information :* This form requires information about the parent.

*3) Route Information :* This form requires information about the route.


### Download Sample File

This is an alternative method for adding all the children details. 

Click on *"Download Sample File"* button to download CSV Sample file and put off-line childs information.

### Upload CSV File

All school data can be uploaded in one shot from a single CSV (Comma Separated Values) file.

Click on *"Upload CSV file"* button and select target file and click on Upload button.

### Edit Children

Here, Super admin perform action on Edit children to redirect the edit child's information as well as Parant info and Route info also.

### Delete Children

Super admin perform action on Delete children to search children name and click on Delete children button.

### Search By

Searching for a child based on information in a category is made simpler with this *First Name/Last Name, Roll Number and Class*.

### Search

Search for a child based on search by category selected as selected. 

## Routes
### Route List

This module is a cumulative collection of all the route's registered on the BOC.

### Add Route

School admin can add the route manually by clicking on Add Route button and Fill the basic route information.

### Edit Route

School admin can update the route information by clicking on edit route button and update basic information.

### Delete Route

School admin can perform action to delete route on school route's by clicking on Delete route button.

### Search By

Searching for a child based on information in a category is made simpler with this *First Name/Last Name, Roll Number and Class*.

### Search

Search for a child based on search by category as selected.

## Request(s)

This module is collection of all request made by the parents to the school admin.

### Request(s) List

The School admin can view the list of pending requests sent by parents.

### Edit Request

School Admin can click on the edit button to see parent’s requests and approve or reject it.

### Delete Request

School Admin can click on the Delete button to see parent’s requests has be Deleted.

### Search By

Searching for a Request based on information in a category is made simpler with this *Requested Childs and Class/Grade*. 

### Search

Search for a Request based on search by category selected as selected. 

## Driver

This is a cummulative collection drivers on the BOC.

### Drivers List

This is a cummulative collection list of all the registered drivers on the BOC.

### Add Driver

School admin can click on Add Driver button to add the driver’s details including
the driver’s Image. and set the password for him.

### Edit Driver

School admin can click on Edit Driver button to Update the driver’s details including
the driver’s Image. and set the password for him.

### Driver Compliance

This feature is used to update all required documents of the driver, namely - ID proof, License and Registration Number.

### Delete Driver

School admin can click on Delete Driver button to Delete the driver’s full details.

### Search By

Searching for a Driver based on information in a category is made simpler with this *Driver Name, Phone Number and Employee Id*. 

### Search

Search for a Driver based on search by category selected as selected.

## Buses

This module is a cumulative record of all the buses registered on the BOC.

### Bus List

School admin can view the all buses to register school only to click on Bus tab.

### Add Bus

School admin can click the add bus button and he can fill the bus basic information.

### Edit Bus

School admin can click the Edit bus button and he can update the bus basic information.

### Delete Bus

School admin can click on Delete Bus button to delete the all details for selected bus.

### Search By

Searching for a Bus based on information in a category is made simpler with this *Bus Name and Bus Registeration number*. 

### Search

Search for a bus based on search by category selected as selected.

## Central Live Tracking

This module lets the school admin to have an eagle’s eye view of the tracking of all the buses, one bus at a time.

## Help

This module lets the school admin to have a help documents for:

*1) School Admin Help*

*2) Parents App Help*

*3) Driver App Help*

to click on Help menu.

# Driver App BOC
<aside class="notice">
First and foremost, the driver should be registered on the Beacon BOC. A Drivers’ work on the Beacon Driver app is minimal. Routes created by the School Admin show up on the driver app including pickup/drop locations. All that the driver needs to do is mark child attendance.</aside>

## Login

For a driver to start using the Beacon Driver app, the driver should :

> To authorize, use this code:

```shell
var qs = require("querystring");
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
    "Content-Type": "application/x-www-form-urlencoded",
    "Cache-Control": "no-cache",
    "Postman-Token": "315b1ff1-c719-42f7-b057-e667e3c2b66b"
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

req.write(qs.stringify({ phone: '8180873363',
  password: '123456',
  osVersion: '7.0',
  deviceId: '56282e7a7d0b9c43',
  deviceModel: 'Micromax Micromax Q437',
  gcmId: 'ftkv-Y0PmxE:APA91bFiuNVh35452kjRXbayoXVX4M0xMxSo1OdFuD94eYGuHiUl1c6Ix1r2zNANfZK3A7o3BxQdp8kA-TVo9r0JYx4eN4QP_lOn_EECOWsuc6hvG7e1QHYXp395qEIquHl7oP0cmUi6',
  deviceType: 'Android' }));
req.end();
```

```ruby
import Foundation

let headers = [
  "Content-Type": "application/x-www-form-urlencoded",
  "Cache-Control": "no-cache",
  "Postman-Token": "2506081a-7619-4e82-9e83-6455e037797a"
]

let postData = NSMutableData(data: "phone=8180873363".data(using: String.Encoding.utf8)!)
postData.append("&password=123456".data(using: String.Encoding.utf8)!)
postData.append("&osVersion=7.0".data(using: String.Encoding.utf8)!)
postData.append("&deviceId=56282e7a7d0b9c43".data(using: String.Encoding.utf8)!)
postData.append("&deviceModel=Micromax Micromax Q437".data(using: String.Encoding.utf8)!)
postData.append("&gcmId=ftkv-Y0PmxE:APA91bFiuNVh35452kjRXbayoXVX4M0xMxSo1OdFuD94eYGuHiUl1c6Ix1r2zNANfZK3A7o3BxQdp8kA-TVo9r0JYx4eN4QP_lOn_EECOWsuc6hvG7e1QHYXp395qEIquHl7oP0cmUi6".data(using: String.Encoding.utf8)!)
postData.append("&deviceType=Android".data(using: String.Encoding.utf8)!)

let request = NSMutableURLRequest(url: NSURL(string: "http://52.66.58.94:4000/user/driver/Login/")! as URL,
                                        cachePolicy: .useProtocolCachePolicy,
                                    timeoutInterval: 10.0)
request.httpMethod = "POST"
request.allHTTPHeaderFields = headers
request.httpBody = postData as Data

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
    "Content-Type": "application/x-www-form-urlencoded",
    "Cache-Control": "no-cache",
    "Postman-Token": "7726dd2d-7359-4303-ae0e-97ddd98e3f9d"
  },
  "data": {
    "phone": "8180873363",
    "password": "123456",
    "osVersion": "7.0",
    "deviceId": "56282e7a7d0b9c43",
    "deviceModel": "Micromax Micromax Q437",
    "gcmId": "ftkv-Y0PmxE:APA91bFiuNVh35452kjRXbayoXVX4M0xMxSo1OdFuD94eYGuHiUl1c6Ix1r2zNANfZK3A7o3BxQdp8kA-TVo9r0JYx4eN4QP_lOn_EECOWsuc6hvG7e1QHYXp395qEIquHl7oP0cmUi6",
    "deviceType": "Android"
  }
}
$.ajax(settings).done(function (response) {
  console.log(response);
});
```
```Json

```

*A. Have registered with the Beacon BOC.*

*B. Created a profile with their register mobile number and password.*





**Request Parameter:**

**Method** : Post

**URL** : [http://52.66.58.94:4000/user/driver/Login/](http://52.66.58.94:4000/user/driver/Login/)

Key | Value
---------------- | ----------------
Phone | 8180873363
Password | 123456
OsVersion | 7.0
DeviceID | 56282e7a7d0b9c43
DeviceModel | Micromax Micromax Q437
gcmld | ftkv-Y0PmxE:APA91bFiuNVh35452kjRXbayoXVX4M0xMxSo1OdFuD94eYGuHiUl1c6Ix1r2zNANfZK3A7o3BxQdp8kA-TVo9r0JYx4eN4QP_lOn_EECOWsuc6hvG7e1QHYXp395qEIquHl7oP0cmUi6
DeviceType | Android


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

Once logged in, the driver can see all the trips of the day. On which driver can
see 2 sections.

1) Trip To Be Completed

2) Completed Trip

### 1) Trip To Be Completed

In this section driver can see , Upcoming trips of the day according the time.

> *Trip To Be Completed* To authorize, use this code:

```shell
var qs = require("querystring");
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
    "getDriverUpcomingTrips"
  ],
  "headers": {
    "Content-Type": "application/x-www-form-urlencoded",
    "Cache-Control": "no-cache",
    "Postman-Token": "1caba864-7e2b-49e4-af8d-180ea6d1f24d"
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

req.write(qs.stringify({ driverID: '5b71c616eddcca22bb7630bb' }));
req.end();
```

```ruby
import Foundation

let headers = [
  "Content-Type": "application/x-www-form-urlencoded",
  "Cache-Control": "no-cache",
  "Postman-Token": "531cfd0f-c22e-4087-ba12-82032fcd9b19"
]

let postData = NSMutableData(data: "driverID=5b71c616eddcca22bb7630bb".data(using: String.Encoding.utf8)!)

let request = NSMutableURLRequest(url: NSURL(string: "http://52.66.58.94:4000/user/driver/getDriverUpcomingTrips")! as URL,
                                        cachePolicy: .useProtocolCachePolicy,
                                    timeoutInterval: 10.0)
request.httpMethod = "POST"
request.allHTTPHeaderFields = headers
request.httpBody = postData as Data

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
  "url": "http://52.66.58.94:4000/user/driver/getDriverUpcomingTrips",
  "method": "POST",
  "headers": {
    "Content-Type": "application/x-www-form-urlencoded",
    "Cache-Control": "no-cache",
    "Postman-Token": "9bd1eb14-5db5-477b-a261-5bda1924644d"
  },
  "data": {
    "driverID": "5b71c616eddcca22bb7630bb"
  }
}

$.ajax(settings).done(function (response) {
  console.log(response);
});
```

**Request Parameters:**

Method : Post

Url : [http://52.66.58.94:4000/user/driver/Login/](http://52.66.58.94:4000/user/driver/Login/)

Key | Value
---------------- | ----------------
DriverId | 5b71c616eddcca22bb7630bb
RouteId | 5b0f9621d811d81f2dc6ea79
Type | Pickup

**Response :**

> **Response :** *Trip To Be Completed* command returns JSON structured like this:

```json
  {
    "routes": [],
    "statusMessage": "Found Upcoming Trips",
    "status": "Success"
  } 
```

> **Response :** *When driver id not found or blank in db* command returns JSON structured like this:

```json
{ 
    "statusMessage": "Driver not found", 
    "status": "Failed" 
}
```
> **Response :** *When driver id not found or blank in db* command returns JSON structured like this:

```json
{
    "statusMessage": "Driver not assigned to this trip", 
    "status": "Failed"
}
```

#### Start Trip

*1. The Driver must click Start Button, in to the Beacon Driver app, the driver can
see the locations for the Next Pick-Up.*

> *Start Trip* To authorize, use this code:

```shell
var qs = require("querystring");
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
    "startTrip",
    ""
  ],
  "headers": {
    "Content-Type": "application/x-www-form-urlencoded",
    "cache-control": "no-cache",
    "Postman-Token": "8f550dcd-e2a5-4515-acc1-67de4d5ad5f7"
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

req.write(qs.stringify({ driverID: '5b71c616eddcca22bb7630bb',
  routeID: '5b0f9621d811d81f2dc6ea79',
  'tripStartLocation[]': [ '18.561324', '73.944711' ] }));
req.end();
```

```ruby
let headers = [
  "Content-Type": "application/x-www-form-urlencoded",
  "cache-control": "no-cache",
  "Postman-Token": "a91fd104-f813-4775-b8bb-d5d533ea9298"
]

let postData = NSMutableData(data: "driverID=5b71c616eddcca22bb7630bb".data(using: String.Encoding.utf8)!)
postData.append("&routeID=5b0f9621d811d81f2dc6ea79".data(using: String.Encoding.utf8)!)
postData.append("&tripStartLocation[]=18.561324".data(using: String.Encoding.utf8)!)
postData.append("&tripStartLocation[]=73.944711".data(using: String.Encoding.utf8)!)

let request = NSMutableURLRequest(url: NSURL(string: "http://52.66.58.94:4000/user/driver/startTrip/")! as URL,
                                        cachePolicy: .useProtocolCachePolicy,
                                    timeoutInterval: 10.0)
request.httpMethod = "POST"
request.allHTTPHeaderFields = headers
request.httpBody = postData as Data

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
  "url": "http://52.66.58.94:4000/user/driver/startTrip/",
  "method": "POST",
  "headers": {
    "Content-Type": "application/x-www-form-urlencoded",
    "cache-control": "no-cache",
    "Postman-Token": "92eb7d13-8e0e-4cbb-b0fb-08cea53edb6d"
  },
  "data": {
    "driverID": "5b71c616eddcca22bb7630bb",
    "routeID": "5b0f9621d811d81f2dc6ea79",
    "tripStartLocation[]": [
      "18.561324",
      "73.944711"
    ]
  }
}

$.ajax(settings).done(function (response) {
  console.log(response);
});
```

> **Response :** *Trip To Be Completed* command returns JSON structured like this:

```json

```

**Request Parameters**

**Method** : POST

**Headers**

Key | Value
---------- | ----------
Content-Type | application/x-www-form-urlencoded

**Body**

Key | Value
---------- | ----------
String driverID | 5b71c616eddcca22bb7630bb
String HTdriverID | 
String routeID | 5b0f9621d811d81f2dc6ea79
double[] tripStartLocation | 18.561324

 *2. The Driver must click Start Trip in order to start the trip. When driver clicks on
start trip button parent will get Push notification from the server.*

#### PickUp Trip

During pickup trips, the driver must mark the attendance after each pickup is made and click the Next button. During the pickup when driver mark child as present, then parent will get the push notification that *child has boarded the bus*. And same as for absent if he mark as absent will get also push notification that *child has absent*.

**Request Parameter** 

**Method** : POST.

**URL** : [http://boc.greylabs.in:4000/user/driver/markAttendence](http://boc.greylabs.in:4000/user/driver/markAttendence)

**Header** 

key | Value
---- | ----
Content-Type | application/x-www-form-urlencoded

**Body**

 key | Value
---- | ----
LonLat | [ 73.944711, 18.561324 ]
children | [ { childID: '5b4f01d8f61d3b31ea3334a5', mark: 'Present' } ]
tripID | 5b4f01d8f61d3b31ea333498

> *Pick-Up Trip* To authorize, use this code:

```shell
var qs = require("querystring");
var http = require("http");

var options = {
  "method": "POST",
  "hostname": [
    "boc",
    "greylabs",
    "in"
  ],
  "port": "4000",
  "path": [
    "user",
    "driver",
    "markAttendence"
  ],
  "headers": {
    "Content-Type": "application/x-www-form-urlencoded",
    "cache-control": "no-cache",
    "Postman-Token": "ff5ce148-739e-4c27-a7e0-b357a3faa7e5"
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

req.write(qs.stringify({ LonLat: '[ 73.944711, 18.561324 ]',
  children: '[ { childID: \'5b4f01d8f61d3b31ea3334a5\', mark: \'Present\' } ]',
  tripID: '5b4f01d8f61d3b31ea333498' }));
req.end();
```

```ruby
import Foundation

let headers = [
  "Content-Type": "application/x-www-form-urlencoded",
  "cache-control": "no-cache",
  "Postman-Token": "7b7055a7-0ccf-4609-90d0-fc60104d82ed"
]

let postData = NSMutableData(data: "LonLat=[ 73.944711, 18.561324 ]".data(using: String.Encoding.utf8)!)
postData.append("&children=[ { childID: '5b4f01d8f61d3b31ea3334a5', mark: 'Present' } ]".data(using: String.Encoding.utf8)!)
postData.append("&tripID=5b4f01d8f61d3b31ea333498".data(using: String.Encoding.utf8)!)

let request = NSMutableURLRequest(url: NSURL(string: "http://boc.greylabs.in:4000/user/driver/markAttendence")! as URL,
                                        cachePolicy: .useProtocolCachePolicy,
                                    timeoutInterval: 10.0)
request.httpMethod = "POST"
request.allHTTPHeaderFields = headers
request.httpBody = postData as Data

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
  "url": "http://boc.greylabs.in:4000/user/driver/markAttendence",
  "method": "POST",
  "headers": {
    "Content-Type": "application/x-www-form-urlencoded",
    "cache-control": "no-cache",
    "Postman-Token": "71209265-ca76-48dd-8e2b-3f3cc5f6cd29"
  },
  "data": {
    "LonLat": "[ 73.944711, 18.561324 ]",
    "children": "[ { childID: '5b4f01d8f61d3b31ea3334a5', mark: 'Present' } ]",
    "tripID": "5b4f01d8f61d3b31ea333498"
  }
}

$.ajax(settings).done(function (response) {
  console.log(response);
});
```


#### Drop Trip

Drivers need to mark attendance for all children before starting a trip. During the drop when driver mark child as present, then parent will get the push notification that *child has boarded the bus* And same as for absent if he mark as absent.



#### Report Breakdown

Driver need to click on *MORE* and select *Report Breakdown*, If there is any breakdown in the bus then parents will get the push notification that "child’s Bus has Breakdown". And after click on restart the trip again parent will get the notification that "child’s Bus has Resumed".

#### End The Trip

Once all children have been picked up or dropped, the driver must end the trip using the page that automatically comes up. As driver click the end trip, parent will get the notification that child has reached the school and if drop then child has reached the destination.


### 2) Completed

Completed trips tab show up under the today's all Completed Trips History.


## Sidebar

Driver click on navigation button show up under the sidebar *Report Emergency*, *Help*, *Change Password* and *Logout* menu. 


### Report Emergency

If in running trip any emergency during driver click on navigation button and select *Report Emergency* menu to call the configured emergency number.

> *Report Emergency* To authorize, use this code:

```shell
var qs = require("querystring");
var http = require("http");

var options = {
  "method": "POST",
  "hostname": [
    "boc",
    "greylabs",
    "in"
  ],
  "port": "4000",
  "path": [
    "user",
    "getEmergencyNoForChild",
    ""
  ],
  "headers": {
    "Content-Type": "application/x-www-form-urlencoded",
    "cache-control": "no-cache",
    "Postman-Token": "03ad2edf-735a-4006-b88a-3dffdc513cfb"
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

req.write(qs.stringify({ userID: '5b3e208f89d50b20e406886c',
  parentID: '5b3e208f89d50b20e406886d',
  routeID: '5b3f6ad389d50b20e4068c65',
  type: 'Drop' }));
req.end();
```

```ruby
import Foundation

let headers = [
  "Content-Type": "application/x-www-form-urlencoded",
  "cache-control": "no-cache",
  "Postman-Token": "d353b927-9b24-49eb-bd52-7faf18dbbf96"
]

let postData = NSMutableData(data: "userID=5b3e208f89d50b20e406886c".data(using: String.Encoding.utf8)!)
postData.append("&parentID=5b3e208f89d50b20e406886d".data(using: String.Encoding.utf8)!)
postData.append("&routeID=5b3f6ad389d50b20e4068c65".data(using: String.Encoding.utf8)!)
postData.append("&type=Drop".data(using: String.Encoding.utf8)!)

let request = NSMutableURLRequest(url: NSURL(string: "http://boc.greylabs.in:4000/user/getEmergencyNoForChild/")! as URL,
                                        cachePolicy: .useProtocolCachePolicy,
                                    timeoutInterval: 10.0)
request.httpMethod = "POST"
request.allHTTPHeaderFields = headers
request.httpBody = postData as Data

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
  "url": "http://boc.greylabs.in:4000/user/getEmergencyNoForChild/",
  "method": "POST",
  "headers": {
    "Content-Type": "application/x-www-form-urlencoded",
    "cache-control": "no-cache",
    "Postman-Token": "22cb8a4a-916a-480c-8a68-befb2b543a30"
  },
  "data": {
    "userID": "5b3e208f89d50b20e406886c",
    "parentID": "5b3e208f89d50b20e406886d",
    "routeID": "5b3f6ad389d50b20e4068c65",
    "type": "Drop"
  }
}

$.ajax(settings).done(function (response) {
  console.log(response);
});
```

**Request Method** : POST.

**URL** : [http://boc.greylabs.in:4000/user/getEmergencyNoForChild/](http://boc.greylabs.in:4000/user/getEmergencyNoForChild/)

**Request Headers:**

Key | Value
---- | ------
Content-Type | application/x-www-form-urlencoded

**Request Parameter Body**

Key | Value
---- | ----
userID | 5b3e208f89d50b20e406886c
parentID | 5b3e208f89d50b20e406886d
routeID | 5b3f6ad389d50b20e4068c65
type | Drop.

> **Response :** *when child not found* command returns JSON structured like this:

```json
    { 
      "statusMessage": "Children doesn't exist with the given details", 
      "status": "Failed" 
    }
```

> **Response :** *when child found* command returns JSON structured like this:

```json
{
    "statusMessage": "Children with given parent details",
    "status": "Success",
    "children": []
}
```

### Help

If driver don't known how to use Beacon Driver App during driver click on navigation button and select *Help* menu to see you User Help Documents.

### Chenge Password

Driver want to change current password during driver click on navigation button and select *Change Password* menu to see you change password screen and fill *Current Password*, *New Password* And *Confirm Password* all feilds.

**Request Method :** POST

**Request URL :** [https://boc.greylabs.in/user/driver/changePassword](https://boc.greylabs.in/user/driver/changePassword)

> **Response :** *Change Password* command returns JSON structured like this:

```json
  { 
    "statusMessage": "Unable to find Driver.",
    "status": "Failed" 
  }
```


### Logout

If driver get logOut the app during driver click on navigation button and select *LogOut* menu and see you Logout Pop-Up window and click on "Yes" for logout the application.

## Emergency Contact 

If in running trip any emergency during driver click on *top right corner RED colour call icon* to call the configured emergency number.

> *Report Emergency* To authorize, use this code:

```shell
var qs = require("querystring");
var http = require("http");

var options = {
  "method": "POST",
  "hostname": [
    "boc",
    "greylabs",
    "in"
  ],
  "port": "4000",
  "path": [
    "user",
    "getEmergencyNoForChild",
    ""
  ],
  "headers": {
    "Content-Type": "application/x-www-form-urlencoded",
    "cache-control": "no-cache",
    "Postman-Token": "03ad2edf-735a-4006-b88a-3dffdc513cfb"
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

req.write(qs.stringify({ userID: '5b3e208f89d50b20e406886c',
  parentID: '5b3e208f89d50b20e406886d',
  routeID: '5b3f6ad389d50b20e4068c65',
  type: 'Drop' }));
req.end();
```

```ruby
import Foundation

let headers = [
  "Content-Type": "application/x-www-form-urlencoded",
  "cache-control": "no-cache",
  "Postman-Token": "d353b927-9b24-49eb-bd52-7faf18dbbf96"
]

let postData = NSMutableData(data: "userID=5b3e208f89d50b20e406886c".data(using: String.Encoding.utf8)!)
postData.append("&parentID=5b3e208f89d50b20e406886d".data(using: String.Encoding.utf8)!)
postData.append("&routeID=5b3f6ad389d50b20e4068c65".data(using: String.Encoding.utf8)!)
postData.append("&type=Drop".data(using: String.Encoding.utf8)!)

let request = NSMutableURLRequest(url: NSURL(string: "http://boc.greylabs.in:4000/user/getEmergencyNoForChild/")! as URL,
                                        cachePolicy: .useProtocolCachePolicy,
                                    timeoutInterval: 10.0)
request.httpMethod = "POST"
request.allHTTPHeaderFields = headers
request.httpBody = postData as Data

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
  "url": "http://boc.greylabs.in:4000/user/getEmergencyNoForChild/",
  "method": "POST",
  "headers": {
    "Content-Type": "application/x-www-form-urlencoded",
    "cache-control": "no-cache",
    "Postman-Token": "22cb8a4a-916a-480c-8a68-befb2b543a30"
  },
  "data": {
    "userID": "5b3e208f89d50b20e406886c",
    "parentID": "5b3e208f89d50b20e406886d",
    "routeID": "5b3f6ad389d50b20e4068c65",
    "type": "Drop"
  }
}

$.ajax(settings).done(function (response) {
  console.log(response);
});
```

**Request Method** : POST

**URL** : [http://boc.greylabs.in:4000/user/getEmergencyNoForChild/](http://boc.greylabs.in:4000/user/getEmergencyNoForChild/)

**Request Headers:**

Key | Value
---- | ------
Content-Type | application/x-www-form-urlencoded

**Request Parameter Body**

Key | Value
---- | ----
userID | 5b3e208f89d50b20e406886c
parentID | 5b3e208f89d50b20e406886d
routeID | 5b3f6ad389d50b20e4068c65
type | Drop.

> **Response :** *when child not found* command returns JSON structured like this:

```json
    { 
      "statusMessage": "Children doesn't exist with the given details", 
      "status": "Failed" 
    }
```

> **Response :** *when child found* command returns JSON structured like this:

```json
{
    "statusMessage": "Children with given parent details",
    "status": "Success",
    "children": []
}
```



# Parents App BOC

<aside class="notice">
First and foremost, the parent should be registered on the Beacon BOC. Parents work on the Parent app is live tracking to their child with ETA. This is for Next-Gen safety feature for their child, which will make a more convenient and hassle free for them. </aside>

Parent can download the parent app from playstore for android user [Click Here](http://bit.ly/2Mf7qww) And Applestore for iPhone User [Click Here](https://apple.co/2JAiX8a) .

## Register

For Parents to start using the Beacon Parent app, the Parent should:

1. Parent Have register Mobile Number with the Beacon BOC.

2. Created a profile with their Registered mobile number and set Password.

3. Verify child's and It will redirect to the child tracking screen.

## Login
<aside class="notice">
Parent get Logged-In with their Registered mobile number and password. Once logged in, It will redirect to the child tracking screen and Parents can track their child.</aside>

## Home

<aside class="notice">
In this page, parent can see their child with top signal indication status, In this first two circle shows pickup status and last two circle shows drop off status.</aside>

**Pickup Status**

1. If the "*Bus has not started*" yet then status shows blank.
2. If the "*Bus has started to pick up childs*" yet then status shows first signal indication in Yellow colour.
3. If the "*pick up childs*" yet then status shows first signal indication in Green colour and Secound signal indication in Yellow colour.
4. If the child's has be reached Destination first and secound signal indication are in Green colour.
5. If child's has be "*Absent*" yet then status show first signal indication in Red Colour. 

**Drop Status**

1. If the "*Bus has not started*" yet then status shows blank.
2. If the "*Bus has started to pick up childs*" yet then status shows Third signal indication in Yellow colour.
3. If the "*pick up childs*" yet then status shows Third signal indication in Green colour and Fourth signal indication in Yellow colour.
4. If the child's has be reached Destination Third and Fourth signal indication are in Green colour.
5. If child's has Present in PickUp trip But "*Absent*" in drop trip yet first and secound signal indication are in Green colour and third signal indication in Red Colour.

### Track Bus

 Parent get Track a bus to click on *START TRACKING*  button. In this screen, parent can see their child bus current location with ETA (Distance) and if they tap on that card status, In which they can see the driver info with elapsed, travelled km, speed and driver’s battery percentage. apart from that there is one refresh button right top corner of the screen. There is one home icon and one school icon with location marker which.. 

**depends on the below situation -**

1. If pickup trip, then location marker will be on the home icon, because bus is coming to home for pickup the child, after boarded the child it will change home to school icon.
2. If drop trip, then location marker first show the child current location (school) after child has boarded the bus then it will change school to home.

### Notification

Parent get all notification to click on Home screen *Bell* icon to show you From start to end the trip, Parent will get all the push notification like "*child's bus has start.*",  "*child's has boarded the bus*" etc.

## Sidebar

<aside class="notice">
Parent clicked the Navigetion icon get show you Sidebar, parent gets the as follows options *Home*, *Your children*, *Dashboard*, *Change Mobile Number*, *Notification*, *Settings*, *Emergency Contacts*, *FAQs* and *Logout*.</aside>

### Home

In sidebar menu, Parent get click on *HOME* menu to redirect the screen on *HOME PAGE.*

### Your Children

In sidebar menu, parent get click on *Your Children* menu to redirect the screen on your child's profile screen.

### Dashboard

In sidebar menu, parent get click on *Dashboard* menu to redirect the screen on your child's Completed or Upcoming Pick-up and Drop trip history screen.

### Change Mobile

In sidebar menu, parent can change his mobile number to click on *Change Mobile* menu to redirect the screen on Chenge Mobile Number.

### Notification

In sidebar menu, parent get click on *Notification* menu to redirect the screen on all notification's for Pickup and Drop all trip's

### Settings

In sidebar menu, parent get click on *Setting* menu to redirect the screen on  setting for pickup and drop trip's push notification on/off options.

### Emergency Contact

In sidebar menu, parent get click on *Emergency Contact* menu to redirect the screen on list of School Admin or Bus Admin Contact numbers.

### FAQs
### Logout