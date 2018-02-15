---
title: Public API for appointman v1.0.ALPHA
language_tabs:
  - shell: Shell
  - http: HTTP
  - javascript: JavaScript
  - javascript--nodejs: Node.JS
  - ruby: Ruby
  - python: Python
  - java: Java
toc_footers: []
includes: []
search: true
highlight_theme: darkula
headingLevel: 2


---


<h1 id="Public-API-for-appointman">Public API for appointman v1.0.ALPHA</h1>


> Scroll down for code samples, example requests and responses. Select a language for code samples from the tabs above or the mobile navigation menu.


A Rest Service api for appointman.<br />Authentication is done by oauth2.<br/> <br /> Please read the oauth2 authentication documentation https://www.appointman.net/v1/docs/authentication


Base URLs:


* <a href="//localhost:7080/">//localhost:7080/</a>


<a href="https://www.appointman.net/agb/">Terms of service</a>
Email: <a href="mailto:support@appointman.net">APPOINTMAN UG (haftungsbeschränkt)</a> Web: <a href="https://www.appointman.net">APPOINTMAN UG (haftungsbeschränkt)</a> 


# Authentication


* API Key (AUTHORIZATION)
    - Parameter Name: **AUTHORIZATION**, in: header. 


<h1 id="Public-API-for-appointman-Contract-Service">Contract Service</h1>


Endpoint for Contract Management


## getContractsUsingGET


<a id="opIdgetContractsUsingGET"></a>


> Code samples


```shell
# You can also use wget
curl -X GET //localhost:7080//api/v1/contracts/active/{customerId} \
  -H 'Accept: */*'


```


```http
GET //localhost:7080//api/v1/contracts/active/{customerId} HTTP/1.1
Host: null


Accept: */*


```


```javascript
var headers = {
  'Accept':'*/*'


};


$.ajax({
  url: '//localhost:7080//api/v1/contracts/active/{customerId}',
  method: 'get',


  headers: headers,
  success: function(data) {
    console.log(JSON.stringify(data));
  }
})


```


```javascript--nodejs
const request = require('node-fetch');


const headers = {
  'Accept':'*/*'


};


fetch('//localhost:7080//api/v1/contracts/active/{customerId}',
{
  method: 'GET',


  headers: headers
})
.then(function(res) {
    return res.json();
}).then(function(body) {
    console.log(body);
});


```


```ruby
require 'rest-client'
require 'json'


headers = {
  'Accept' => '*/*'
}


result = RestClient.get '//localhost:7080//api/v1/contracts/active/{customerId}',
  params: {
  }, headers: headers


p JSON.parse(result)


```


```python
import requests
headers = {
  'Accept': '*/*'
}


r = requests.get('//localhost:7080//api/v1/contracts/active/{customerId}', params={


}, headers = headers)


print r.json()


```


```java
URL obj = new URL("//localhost:7080//api/v1/contracts/active/{customerId}");
HttpURLConnection con = (HttpURLConnection) obj.openConnection();
con.setRequestMethod("GET");
int responseCode = con.getResponseCode();
BufferedReader in = new BufferedReader(
    new InputStreamReader(con.getInputStream()));
String inputLine;
StringBuffer response = new StringBuffer();
while ((inputLine = in.readLine()) != null) {
    response.append(inputLine);
}
in.close();
System.out.println(response.toString());


```


`GET /api/v1/contracts/active/{customerId}`


*Returns contracts for a customer*


Returns a complete list of customer contracts.


<h3 id="getContractsUsingGET-parameters">Parameters</h3>


|Parameter|In|Type|Required|Description|
|---|---|---|---|---|
|customerId|path|string|true|customerId|


> Example responses


<h3 id="getContractsUsingGET-responses">Responses</h3>


|Status|Meaning|Description|Schema|
|---|---|---|---|
|200|[OK](https://tools.ietf.org/html/rfc7231#section-6.3.1)|Successful retrieval of customers|Inline|
|401|[Unauthorized](https://tools.ietf.org/html/rfc7235#section-3.1)|Unauthorized|None|
|403|[Forbidden](https://tools.ietf.org/html/rfc7231#section-6.5.3)|Access forbidden|None|
|404|[Not Found](https://tools.ietf.org/html/rfc7231#section-6.5.4)|Customer not found|None|
|500|[Internal Server Error](https://tools.ietf.org/html/rfc7231#section-6.6.1)|Internal server error|None|


<h3 id="getContractsUsingGET-responseschema">Response Schema</h3>


Status Code **200**


|Name|Type|Required|Description|
|---|---|---|---|
|*anonymous*|[[Contract](#schemacontract)]|false|No description|
|» Contract|[Contract](#schemacontract)|false|No description|
|»» contractEnd|integer(int64)|false|No description|
|»» contractNumber|string|false|No description|
|»» contractStart|integer(int64)|false|No description|
|»» id|string|false|No description|
|»» maxBookingsInFuture|integer(int64)|false|No description|
|»» maxBookingsPerDay|integer(int64)|false|No description|
|»» notes|string|false|No description|
|»» terminated|boolean|false|No description|
|»» type|string|false|No description|


<aside class="warning">
To perform this operation, you must be authenticated by means of one of the following methods:
AUTHORIZATION ( Scopes: read )
</aside>


## getTerminatedContractsUsingGET


<a id="opIdgetTerminatedContractsUsingGET"></a>


> Code samples


```shell
# You can also use wget
curl -X GET //localhost:7080//api/v1/contracts/terminated/{customerId} \
  -H 'Accept: */*'


```


```http
GET //localhost:7080//api/v1/contracts/terminated/{customerId} HTTP/1.1
Host: null


Accept: */*


```


```javascript
var headers = {
  'Accept':'*/*'


};


$.ajax({
  url: '//localhost:7080//api/v1/contracts/terminated/{customerId}',
  method: 'get',


  headers: headers,
  success: function(data) {
    console.log(JSON.stringify(data));
  }
})


```


```javascript--nodejs
const request = require('node-fetch');


const headers = {
  'Accept':'*/*'


};


fetch('//localhost:7080//api/v1/contracts/terminated/{customerId}',
{
  method: 'GET',


  headers: headers
})
.then(function(res) {
    return res.json();
}).then(function(body) {
    console.log(body);
});


```


```ruby
require 'rest-client'
require 'json'


headers = {
  'Accept' => '*/*'
}


result = RestClient.get '//localhost:7080//api/v1/contracts/terminated/{customerId}',
  params: {
  }, headers: headers


p JSON.parse(result)


```


```python
import requests
headers = {
  'Accept': '*/*'
}


r = requests.get('//localhost:7080//api/v1/contracts/terminated/{customerId}', params={


}, headers = headers)


print r.json()


```


```java
URL obj = new URL("//localhost:7080//api/v1/contracts/terminated/{customerId}");
HttpURLConnection con = (HttpURLConnection) obj.openConnection();
con.setRequestMethod("GET");
int responseCode = con.getResponseCode();
BufferedReader in = new BufferedReader(
    new InputStreamReader(con.getInputStream()));
String inputLine;
StringBuffer response = new StringBuffer();
while ((inputLine = in.readLine()) != null) {
    response.append(inputLine);
}
in.close();
System.out.println(response.toString());


```


`GET /api/v1/contracts/terminated/{customerId}`


*Returns contracts for a customer*


Returns a complete list of customer contracts.


<h3 id="getTerminatedContractsUsingGET-parameters">Parameters</h3>


|Parameter|In|Type|Required|Description|
|---|---|---|---|---|
|customerId|path|string|true|customerId|


> Example responses


<h3 id="getTerminatedContractsUsingGET-responses">Responses</h3>


|Status|Meaning|Description|Schema|
|---|---|---|---|
|200|[OK](https://tools.ietf.org/html/rfc7231#section-6.3.1)|Successful retrieval of customers|Inline|
|401|[Unauthorized](https://tools.ietf.org/html/rfc7235#section-3.1)|Unauthorized|None|
|403|[Forbidden](https://tools.ietf.org/html/rfc7231#section-6.5.3)|Access forbidden|None|
|404|[Not Found](https://tools.ietf.org/html/rfc7231#section-6.5.4)|Customer not found|None|
|500|[Internal Server Error](https://tools.ietf.org/html/rfc7231#section-6.6.1)|Internal server error|None|


<h3 id="getTerminatedContractsUsingGET-responseschema">Response Schema</h3>


Status Code **200**


|Name|Type|Required|Description|
|---|---|---|---|
|*anonymous*|[[Contract](#schemacontract)]|false|No description|
|» Contract|[Contract](#schemacontract)|false|No description|
|»» contractEnd|integer(int64)|false|No description|
|»» contractNumber|string|false|No description|
|»» contractStart|integer(int64)|false|No description|
|»» id|string|false|No description|
|»» maxBookingsInFuture|integer(int64)|false|No description|
|»» maxBookingsPerDay|integer(int64)|false|No description|
|»» notes|string|false|No description|
|»» terminated|boolean|false|No description|
|»» type|string|false|No description|


<aside class="warning">
To perform this operation, you must be authenticated by means of one of the following methods:
AUTHORIZATION ( Scopes: read )
</aside>


<h1 id="Public-API-for-appointman-Customer-Service">Customer Service</h1>


Endpoint for Customer Management


## getCustomerUsingGET


<a id="opIdgetCustomerUsingGET"></a>


> Code samples


```shell
# You can also use wget
curl -X GET //localhost:7080//api/v1/customers/all?limit=0?offset=0 \
  -H 'Accept: */*'


```


```http
GET //localhost:7080//api/v1/customers/all?limit=0?offset=0 HTTP/1.1
Host: null


Accept: */*


```


```javascript
var headers = {
  'Accept':'*/*'


};


$.ajax({
  url: '//localhost:7080//api/v1/customers/all',
  method: 'get',
  data: '?limit=0?offset=0',
  headers: headers,
  success: function(data) {
    console.log(JSON.stringify(data));
  }
})


```


```javascript--nodejs
const request = require('node-fetch');


const headers = {
  'Accept':'*/*'


};


fetch('//localhost:7080//api/v1/customers/all?limit=0?offset=0',
{
  method: 'GET',


  headers: headers
})
.then(function(res) {
    return res.json();
}).then(function(body) {
    console.log(body);
});


```


```ruby
require 'rest-client'
require 'json'


headers = {
  'Accept' => '*/*'
}


result = RestClient.get '//localhost:7080//api/v1/customers/all',
  params: {
  'limit' => 'integer(int32)',
'offset' => 'integer(int32)'
}, headers: headers


p JSON.parse(result)


```


```python
import requests
headers = {
  'Accept': '*/*'
}


r = requests.get('//localhost:7080//api/v1/customers/all', params={
  'limit': '0',  'offset': '0'
}, headers = headers)


print r.json()


```


```java
URL obj = new URL("//localhost:7080//api/v1/customers/all?limit=0?offset=0");
HttpURLConnection con = (HttpURLConnection) obj.openConnection();
con.setRequestMethod("GET");
int responseCode = con.getResponseCode();
BufferedReader in = new BufferedReader(
    new InputStreamReader(con.getInputStream()));
String inputLine;
StringBuffer response = new StringBuffer();
while ((inputLine = in.readLine()) != null) {
    response.append(inputLine);
}
in.close();
System.out.println(response.toString());


```


`GET /api/v1/customers/all`


*Returns customers*


Returns a complete list of customers.


<h3 id="getCustomerUsingGET-parameters">Parameters</h3>


|Parameter|In|Type|Required|Description|
|---|---|---|---|---|
|limit|query|integer(int32)|true|limit|
|offset|query|integer(int32)|true|offset|


> Example responses


<h3 id="getCustomerUsingGET-responses">Responses</h3>


|Status|Meaning|Description|Schema|
|---|---|---|---|
|200|[OK](https://tools.ietf.org/html/rfc7231#section-6.3.1)|Successful retrieval of customers|Inline|
|401|[Unauthorized](https://tools.ietf.org/html/rfc7235#section-3.1)|Unauthorized|None|
|403|[Forbidden](https://tools.ietf.org/html/rfc7231#section-6.5.3)|Forbidden|None|
|404|[Not Found](https://tools.ietf.org/html/rfc7231#section-6.5.4)|Not Found|None|
|500|[Internal Server Error](https://tools.ietf.org/html/rfc7231#section-6.6.1)|Internal server error|None|


<h3 id="getCustomerUsingGET-responseschema">Response Schema</h3>


Status Code **200**


|Name|Type|Required|Description|
|---|---|---|---|
|*anonymous*|[[Customer](#schemacustomer)]|false|No description|
|» Customer|[Customer](#schemacustomer)|false|No description|
|»» id|string|false|Unique id of the customer|
|»» title|string|false|Title like Dr.|
|»» firstname|string|false|The firstname of the customer|
|»» lastname|string|false|The lastname of the customer|
|»» email|string|false|The email address of the customer|
|»» birthday|integer(int64)|false|The birthday of the customer (timestamp in ms)|
|»» phone|string|false|The phone number of the customer|
|»» mobile|string|false|The mobile phone number of the customer|
|»» address|string|false|The private address of the customer|
|»» notes|string|false|Some notes about the customer|


<aside class="warning">
To perform this operation, you must be authenticated by means of one of the following methods:
AUTHORIZATION ( Scopes: read )
</aside>


<h1 id="Public-API-for-appointman-Group-Service">Group Service</h1>


Endpoint for Group Management


## addGroupToContractUsingPUT


<a id="opIdaddGroupToContractUsingPUT"></a>


> Code samples


```shell
# You can also use wget
curl -X PUT //localhost:7080//api/v1/groups/add/{contractId} \
  -H 'Accept: */*'


```


```http
PUT //localhost:7080//api/v1/groups/add/{contractId} HTTP/1.1
Host: null


Accept: */*


```


```javascript
var headers = {
  'Accept':'*/*'


};


$.ajax({
  url: '//localhost:7080//api/v1/groups/add/{contractId}',
  method: 'put',


  headers: headers,
  success: function(data) {
    console.log(JSON.stringify(data));
  }
})


```


```javascript--nodejs
const request = require('node-fetch');


const headers = {
  'Accept':'*/*'


};


fetch('//localhost:7080//api/v1/groups/add/{contractId}',
{
  method: 'PUT',


  headers: headers
})
.then(function(res) {
    return res.json();
}).then(function(body) {
    console.log(body);
});


```


```ruby
require 'rest-client'
require 'json'


headers = {
  'Accept' => '*/*'
}


result = RestClient.put '//localhost:7080//api/v1/groups/add/{contractId}',
  params: {
  }, headers: headers


p JSON.parse(result)


```


```python
import requests
headers = {
  'Accept': '*/*'
}


r = requests.put('//localhost:7080//api/v1/groups/add/{contractId}', params={


}, headers = headers)


print r.json()


```


```java
URL obj = new URL("//localhost:7080//api/v1/groups/add/{contractId}");
HttpURLConnection con = (HttpURLConnection) obj.openConnection();
con.setRequestMethod("PUT");
int responseCode = con.getResponseCode();
BufferedReader in = new BufferedReader(
    new InputStreamReader(con.getInputStream()));
String inputLine;
StringBuffer response = new StringBuffer();
while ((inputLine = in.readLine()) != null) {
    response.append(inputLine);
}
in.close();
System.out.println(response.toString());


```


`PUT /api/v1/groups/add/{contractId}`


*Returns groups*


Returns a complete list of groups.


<h3 id="addGroupToContractUsingPUT-parameters">Parameters</h3>


|Parameter|In|Type|Required|Description|
|---|---|---|---|---|
|name|query|string|false|No description|
|contractId|path|string|true|contractId|


> Example responses


<h3 id="addGroupToContractUsingPUT-responses">Responses</h3>


|Status|Meaning|Description|Schema|
|---|---|---|---|
|200|[OK](https://tools.ietf.org/html/rfc7231#section-6.3.1)|Successful retrieval of lessons|Inline|
|201|[Created](https://tools.ietf.org/html/rfc7231#section-6.3.2)|Created|None|
|401|[Unauthorized](https://tools.ietf.org/html/rfc7235#section-3.1)|Unauthorized|None|
|403|[Forbidden](https://tools.ietf.org/html/rfc7231#section-6.5.3)|Forbidden|None|
|404|[Not Found](https://tools.ietf.org/html/rfc7231#section-6.5.4)|Not Found|None|
|500|[Internal Server Error](https://tools.ietf.org/html/rfc7231#section-6.6.1)|Internal server error|None|


<h3 id="addGroupToContractUsingPUT-responseschema">Response Schema</h3>


Status Code **200**


|Name|Type|Required|Description|
|---|---|---|---|
|*anonymous*|[[Group](#schemagroup)]|false|No description|
|» Group|[Group](#schemagroup)|false|No description|
|»» name|string|false|No description|


<aside class="warning">
To perform this operation, you must be authenticated by means of one of the following methods:
AUTHORIZATION ( Scopes: read )
</aside>


## getGroupsUsingGET


<a id="opIdgetGroupsUsingGET"></a>


> Code samples


```shell
# You can also use wget
curl -X GET //localhost:7080//api/v1/groups/all \
  -H 'Accept: */*'


```


```http
GET //localhost:7080//api/v1/groups/all HTTP/1.1
Host: null


Accept: */*


```


```javascript
var headers = {
  'Accept':'*/*'


};


$.ajax({
  url: '//localhost:7080//api/v1/groups/all',
  method: 'get',


  headers: headers,
  success: function(data) {
    console.log(JSON.stringify(data));
  }
})


```


```javascript--nodejs
const request = require('node-fetch');


const headers = {
  'Accept':'*/*'


};


fetch('//localhost:7080//api/v1/groups/all',
{
  method: 'GET',


  headers: headers
})
.then(function(res) {
    return res.json();
}).then(function(body) {
    console.log(body);
});


```


```ruby
require 'rest-client'
require 'json'


headers = {
  'Accept' => '*/*'
}


result = RestClient.get '//localhost:7080//api/v1/groups/all',
  params: {
  }, headers: headers


p JSON.parse(result)


```


```python
import requests
headers = {
  'Accept': '*/*'
}


r = requests.get('//localhost:7080//api/v1/groups/all', params={


}, headers = headers)


print r.json()


```


```java
URL obj = new URL("//localhost:7080//api/v1/groups/all");
HttpURLConnection con = (HttpURLConnection) obj.openConnection();
con.setRequestMethod("GET");
int responseCode = con.getResponseCode();
BufferedReader in = new BufferedReader(
    new InputStreamReader(con.getInputStream()));
String inputLine;
StringBuffer response = new StringBuffer();
while ((inputLine = in.readLine()) != null) {
    response.append(inputLine);
}
in.close();
System.out.println(response.toString());


```


`GET /api/v1/groups/all`


*Returns groups*


Returns a complete list of groups.


> Example responses


<h3 id="getGroupsUsingGET-responses">Responses</h3>


|Status|Meaning|Description|Schema|
|---|---|---|---|
|200|[OK](https://tools.ietf.org/html/rfc7231#section-6.3.1)|Successful retrieval of lessons|Inline|
|401|[Unauthorized](https://tools.ietf.org/html/rfc7235#section-3.1)|Unauthorized|None|
|403|[Forbidden](https://tools.ietf.org/html/rfc7231#section-6.5.3)|Forbidden|None|
|404|[Not Found](https://tools.ietf.org/html/rfc7231#section-6.5.4)|Not Found|None|
|500|[Internal Server Error](https://tools.ietf.org/html/rfc7231#section-6.6.1)|Internal server error|None|


<h3 id="getGroupsUsingGET-responseschema">Response Schema</h3>


Status Code **200**


|Name|Type|Required|Description|
|---|---|---|---|
|*anonymous*|[[Group](#schemagroup)]|false|No description|
|» Group|[Group](#schemagroup)|false|No description|
|»» name|string|false|No description|


<aside class="warning">
To perform this operation, you must be authenticated by means of one of the following methods:
AUTHORIZATION ( Scopes: read )
</aside>


## removeGroupFromContractUsingPUT


<a id="opIdremoveGroupFromContractUsingPUT"></a>


> Code samples


```shell
# You can also use wget
curl -X PUT //localhost:7080//api/v1/groups/remove/{contractId} \
  -H 'Accept: */*'


```


```http
PUT //localhost:7080//api/v1/groups/remove/{contractId} HTTP/1.1
Host: null


Accept: */*


```


```javascript
var headers = {
  'Accept':'*/*'


};


$.ajax({
  url: '//localhost:7080//api/v1/groups/remove/{contractId}',
  method: 'put',


  headers: headers,
  success: function(data) {
    console.log(JSON.stringify(data));
  }
})


```


```javascript--nodejs
const request = require('node-fetch');


const headers = {
  'Accept':'*/*'


};


fetch('//localhost:7080//api/v1/groups/remove/{contractId}',
{
  method: 'PUT',


  headers: headers
})
.then(function(res) {
    return res.json();
}).then(function(body) {
    console.log(body);
});


```


```ruby
require 'rest-client'
require 'json'


headers = {
  'Accept' => '*/*'
}


result = RestClient.put '//localhost:7080//api/v1/groups/remove/{contractId}',
  params: {
  }, headers: headers


p JSON.parse(result)


```


```python
import requests
headers = {
  'Accept': '*/*'
}


r = requests.put('//localhost:7080//api/v1/groups/remove/{contractId}', params={


}, headers = headers)


print r.json()


```


```java
URL obj = new URL("//localhost:7080//api/v1/groups/remove/{contractId}");
HttpURLConnection con = (HttpURLConnection) obj.openConnection();
con.setRequestMethod("PUT");
int responseCode = con.getResponseCode();
BufferedReader in = new BufferedReader(
    new InputStreamReader(con.getInputStream()));
String inputLine;
StringBuffer response = new StringBuffer();
while ((inputLine = in.readLine()) != null) {
    response.append(inputLine);
}
in.close();
System.out.println(response.toString());


```


`PUT /api/v1/groups/remove/{contractId}`


*Returns groups*


Returns a complete list of groups.


<h3 id="removeGroupFromContractUsingPUT-parameters">Parameters</h3>


|Parameter|In|Type|Required|Description|
|---|---|---|---|---|
|name|query|string|false|No description|
|contractId|path|string|true|contractId|


> Example responses


<h3 id="removeGroupFromContractUsingPUT-responses">Responses</h3>


|Status|Meaning|Description|Schema|
|---|---|---|---|
|200|[OK](https://tools.ietf.org/html/rfc7231#section-6.3.1)|Successful retrieval of lessons|Inline|
|201|[Created](https://tools.ietf.org/html/rfc7231#section-6.3.2)|Created|None|
|401|[Unauthorized](https://tools.ietf.org/html/rfc7235#section-3.1)|Unauthorized|None|
|403|[Forbidden](https://tools.ietf.org/html/rfc7231#section-6.5.3)|Forbidden|None|
|404|[Not Found](https://tools.ietf.org/html/rfc7231#section-6.5.4)|Not Found|None|
|500|[Internal Server Error](https://tools.ietf.org/html/rfc7231#section-6.6.1)|Internal server error|None|


<h3 id="removeGroupFromContractUsingPUT-responseschema">Response Schema</h3>


Status Code **200**


|Name|Type|Required|Description|
|---|---|---|---|
|*anonymous*|[[Group](#schemagroup)]|false|No description|
|» Group|[Group](#schemagroup)|false|No description|
|»» name|string|false|No description|


<aside class="warning">
To perform this operation, you must be authenticated by means of one of the following methods:
AUTHORIZATION ( Scopes: read )
</aside>


<h1 id="Public-API-for-appointman-Lesson-Service">Lesson Service</h1>


Endpoint for Lesson Management


## getLessonsUsingGET


<a id="opIdgetLessonsUsingGET"></a>


> Code samples


```shell
# You can also use wget
curl -X GET //localhost:7080//api/v1/lessons/all/{from}/{to} \
  -H 'Content-Type: application/json' \
  -H 'Accept: */*'


```


```http
GET //localhost:7080//api/v1/lessons/all/{from}/{to} HTTP/1.1
Host: null
Content-Type: application/json
Accept: */*


```


```javascript
var headers = {
  'Content-Type':'application/json',
  'Accept':'*/*'


};


$.ajax({
  url: '//localhost:7080//api/v1/lessons/all/{from}/{to}',
  method: 'get',


  headers: headers,
  success: function(data) {
    console.log(JSON.stringify(data));
  }
})


```


```javascript--nodejs
const request = require('node-fetch');
const inputBody = 'string';
const headers = {
  'Content-Type':'application/json',
  'Accept':'*/*'


};


fetch('//localhost:7080//api/v1/lessons/all/{from}/{to}',
{
  method: 'GET',
  body: inputBody,
  headers: headers
})
.then(function(res) {
    return res.json();
}).then(function(body) {
    console.log(body);
});


```


```ruby
require 'rest-client'
require 'json'


headers = {
  'Content-Type' => 'application/json',
  'Accept' => '*/*'
}


result = RestClient.get '//localhost:7080//api/v1/lessons/all/{from}/{to}',
  params: {
  }, headers: headers


p JSON.parse(result)


```


```python
import requests
headers = {
  'Content-Type': 'application/json',
  'Accept': '*/*'
}


r = requests.get('//localhost:7080//api/v1/lessons/all/{from}/{to}', params={


}, headers = headers)


print r.json()


```


```java
URL obj = new URL("//localhost:7080//api/v1/lessons/all/{from}/{to}");
HttpURLConnection con = (HttpURLConnection) obj.openConnection();
con.setRequestMethod("GET");
int responseCode = con.getResponseCode();
BufferedReader in = new BufferedReader(
    new InputStreamReader(con.getInputStream()));
String inputLine;
StringBuffer response = new StringBuffer();
while ((inputLine = in.readLine()) != null) {
    response.append(inputLine);
}
in.close();
System.out.println(response.toString());


```


`GET /api/v1/lessons/all/{from}/{to}`


*Returns lessons*


Returns a complete list of lessons.


> Body parameter


```json
"string"
```


<h3 id="getLessonsUsingGET-parameters">Parameters</h3>


|Parameter|In|Type|Required|Description|
|---|---|---|---|---|
|from|path|integer(int64)|true|from|
|to|path|integer(int64)|true|to|
|body|body|string|false|contractId|


> Example responses


<h3 id="getLessonsUsingGET-responses">Responses</h3>


|Status|Meaning|Description|Schema|
|---|---|---|---|
|200|[OK](https://tools.ietf.org/html/rfc7231#section-6.3.1)|Successful retrieval of lessons|Inline|
|401|[Unauthorized](https://tools.ietf.org/html/rfc7235#section-3.1)|Unauthorized|None|
|403|[Forbidden](https://tools.ietf.org/html/rfc7231#section-6.5.3)|Access forbidden|None|
|404|[Not Found](https://tools.ietf.org/html/rfc7231#section-6.5.4)|Not Found|None|
|500|[Internal Server Error](https://tools.ietf.org/html/rfc7231#section-6.6.1)|Internal server error|None|


<h3 id="getLessonsUsingGET-responseschema">Response Schema</h3>


Status Code **200**


|Name|Type|Required|Description|
|---|---|---|---|
|*anonymous*|[[Lesson](#schemalesson)]|false|No description|
|» Lesson|[Lesson](#schemalesson)|false|No description|
|»» cancelMessage|string|false|No description|
|»» canceled|boolean|false|No description|
|»» courseId|string|false|No description|
|»» date|integer(int64)|false|No description|
|»» description|string|false|No description|
|»» id|string|false|No description|
|»» name|string|false|No description|
|»» participants|[[Participant](#schemaparticipant)]|false|No description|
|»»» Participant|[Participant](#schemaparticipant)|false|No description|
|»»»» contractId|string|false|No description|
|»»»» lead|boolean|false|No description|
|»»»» leadId|string|false|No description|
|»»»» name|string|false|No description|
|»»»» ticketId|string|false|No description|


<aside class="warning">
To perform this operation, you must be authenticated by means of one of the following methods:
AUTHORIZATION ( Scopes: read )
</aside>


<h1 id="Public-API-for-appointman-oauth-user-controller">oauth-user-controller</h1>


Oauth User Controller


## loginUsingGET


<a id="opIdloginUsingGET"></a>


> Code samples


```shell
# You can also use wget
curl -X GET //localhost:7080//login \
  -H 'Accept: */*'


```


```http
GET //localhost:7080//login HTTP/1.1
Host: null


Accept: */*


```


```javascript
var headers = {
  'Accept':'*/*'


};


$.ajax({
  url: '//localhost:7080//login',
  method: 'get',


  headers: headers,
  success: function(data) {
    console.log(JSON.stringify(data));
  }
})


```


```javascript--nodejs
const request = require('node-fetch');


const headers = {
  'Accept':'*/*'


};


fetch('//localhost:7080//login',
{
  method: 'GET',


  headers: headers
})
.then(function(res) {
    return res.json();
}).then(function(body) {
    console.log(body);
});


```


```ruby
require 'rest-client'
require 'json'


headers = {
  'Accept' => '*/*'
}


result = RestClient.get '//localhost:7080//login',
  params: {
  }, headers: headers


p JSON.parse(result)


```


```python
import requests
headers = {
  'Accept': '*/*'
}


r = requests.get('//localhost:7080//login', params={


}, headers = headers)


print r.json()


```


```java
URL obj = new URL("//localhost:7080//login");
HttpURLConnection con = (HttpURLConnection) obj.openConnection();
con.setRequestMethod("GET");
int responseCode = con.getResponseCode();
BufferedReader in = new BufferedReader(
    new InputStreamReader(con.getInputStream()));
String inputLine;
StringBuffer response = new StringBuffer();
while ((inputLine = in.readLine()) != null) {
    response.append(inputLine);
}
in.close();
System.out.println(response.toString());


```


`GET /login`


*login*


<h3 id="loginUsingGET-parameters">Parameters</h3>


|Parameter|In|Type|Required|Description|
|---|---|---|---|---|
|error|query|string|false|error|
|logout|query|string|false|logout|


> Example responses


<h3 id="loginUsingGET-responses">Responses</h3>


|Status|Meaning|Description|Schema|
|---|---|---|---|
|200|[OK](https://tools.ietf.org/html/rfc7231#section-6.3.1)|OK|string|
|401|[Unauthorized](https://tools.ietf.org/html/rfc7235#section-3.1)|Unauthorized|None|
|403|[Forbidden](https://tools.ietf.org/html/rfc7231#section-6.5.3)|Forbidden|None|
|404|[Not Found](https://tools.ietf.org/html/rfc7231#section-6.5.4)|Not Found|None|


<aside class="success">
This operation does not require authentication
</aside>


<h1 id="Public-API-for-appointman-authorization-endpoint">authorization-endpoint</h1>


Authorization Endpoint


## authorizeUsingGET


<a id="opIdauthorizeUsingGET"></a>


> Code samples


```shell
# You can also use wget
curl -X GET //localhost:7080//oauth/authorize?parameters=string \
  -H 'Accept: */*'


```


```http
GET //localhost:7080//oauth/authorize?parameters=string HTTP/1.1
Host: null


Accept: */*


```


```javascript
var headers = {
  'Accept':'*/*'


};


$.ajax({
  url: '//localhost:7080//oauth/authorize',
  method: 'get',
  data: '?parameters=string',
  headers: headers,
  success: function(data) {
    console.log(JSON.stringify(data));
  }
})


```


```javascript--nodejs
const request = require('node-fetch');


const headers = {
  'Accept':'*/*'


};


fetch('//localhost:7080//oauth/authorize?parameters=string',
{
  method: 'GET',


  headers: headers
})
.then(function(res) {
    return res.json();
}).then(function(body) {
    console.log(body);
});


```


```ruby
require 'rest-client'
require 'json'


headers = {
  'Accept' => '*/*'
}


result = RestClient.get '//localhost:7080//oauth/authorize',
  params: {
  'parameters' => 'string'
}, headers: headers


p JSON.parse(result)


```


```python
import requests
headers = {
  'Accept': '*/*'
}


r = requests.get('//localhost:7080//oauth/authorize', params={
  'parameters': 'string'
}, headers = headers)


print r.json()


```


```java
URL obj = new URL("//localhost:7080//oauth/authorize?parameters=string");
HttpURLConnection con = (HttpURLConnection) obj.openConnection();
con.setRequestMethod("GET");
int responseCode = con.getResponseCode();
BufferedReader in = new BufferedReader(
    new InputStreamReader(con.getInputStream()));
String inputLine;
StringBuffer response = new StringBuffer();
while ((inputLine = in.readLine()) != null) {
    response.append(inputLine);
}
in.close();
System.out.println(response.toString());


```


`GET /oauth/authorize`


*authorize*


<h3 id="authorizeUsingGET-parameters">Parameters</h3>


|Parameter|In|Type|Required|Description|
|---|---|---|---|---|
|model|query|undefined|false|model|
|parameters|query|string|true|parameters|


> Example responses


<h3 id="authorizeUsingGET-responses">Responses</h3>


|Status|Meaning|Description|Schema|
|---|---|---|---|
|200|[OK](https://tools.ietf.org/html/rfc7231#section-6.3.1)|OK|[ModelAndView](#schemamodelandview)|
|401|[Unauthorized](https://tools.ietf.org/html/rfc7235#section-3.1)|Unauthorized|None|
|403|[Forbidden](https://tools.ietf.org/html/rfc7231#section-6.5.3)|Forbidden|None|
|404|[Not Found](https://tools.ietf.org/html/rfc7231#section-6.5.4)|Not Found|None|


<aside class="success">
This operation does not require authentication
</aside>


## authorizeUsingHEAD


<a id="opIdauthorizeUsingHEAD"></a>


> Code samples


```shell
# You can also use wget
curl -X HEAD //localhost:7080//oauth/authorize?parameters=string \
  -H 'Accept: */*'


```


```http
HEAD //localhost:7080//oauth/authorize?parameters=string HTTP/1.1
Host: null


Accept: */*


```


```javascript
var headers = {
  'Accept':'*/*'


};


$.ajax({
  url: '//localhost:7080//oauth/authorize',
  method: 'head',
  data: '?parameters=string',
  headers: headers,
  success: function(data) {
    console.log(JSON.stringify(data));
  }
})


```


```javascript--nodejs
const request = require('node-fetch');


const headers = {
  'Accept':'*/*'


};


fetch('//localhost:7080//oauth/authorize?parameters=string',
{
  method: 'HEAD',


  headers: headers
})
.then(function(res) {
    return res.json();
}).then(function(body) {
    console.log(body);
});


```


```ruby
require 'rest-client'
require 'json'


headers = {
  'Accept' => '*/*'
}


result = RestClient.head '//localhost:7080//oauth/authorize',
  params: {
  'parameters' => 'string'
}, headers: headers


p JSON.parse(result)


```


```python
import requests
headers = {
  'Accept': '*/*'
}


r = requests.head('//localhost:7080//oauth/authorize', params={
  'parameters': 'string'
}, headers = headers)


print r.json()


```


```java
URL obj = new URL("//localhost:7080//oauth/authorize?parameters=string");
HttpURLConnection con = (HttpURLConnection) obj.openConnection();
con.setRequestMethod("HEAD");
int responseCode = con.getResponseCode();
BufferedReader in = new BufferedReader(
    new InputStreamReader(con.getInputStream()));
String inputLine;
StringBuffer response = new StringBuffer();
while ((inputLine = in.readLine()) != null) {
    response.append(inputLine);
}
in.close();
System.out.println(response.toString());


```


`HEAD /oauth/authorize`


*authorize*


<h3 id="authorizeUsingHEAD-parameters">Parameters</h3>


|Parameter|In|Type|Required|Description|
|---|---|---|---|---|
|model|query|undefined|false|model|
|parameters|query|string|true|parameters|


> Example responses


<h3 id="authorizeUsingHEAD-responses">Responses</h3>


|Status|Meaning|Description|Schema|
|---|---|---|---|
|200|[OK](https://tools.ietf.org/html/rfc7231#section-6.3.1)|OK|[ModelAndView](#schemamodelandview)|
|204|[No Content](https://tools.ietf.org/html/rfc7231#section-6.3.5)|No Content|None|
|401|[Unauthorized](https://tools.ietf.org/html/rfc7235#section-3.1)|Unauthorized|None|
|403|[Forbidden](https://tools.ietf.org/html/rfc7231#section-6.5.3)|Forbidden|None|


<aside class="success">
This operation does not require authentication
</aside>


## approveOrDenyUsingPOST


<a id="opIdapproveOrDenyUsingPOST"></a>


> Code samples


```shell
# You can also use wget
curl -X POST //localhost:7080//oauth/authorize?approvalParameters=string?user_oauth_approval=string \
  -H 'Accept: */*'


```


```http
POST //localhost:7080//oauth/authorize?approvalParameters=string?user_oauth_approval=string HTTP/1.1
Host: null


Accept: */*


```


```javascript
var headers = {
  'Accept':'*/*'


};


$.ajax({
  url: '//localhost:7080//oauth/authorize',
  method: 'post',
  data: '?approvalParameters=string?user_oauth_approval=string',
  headers: headers,
  success: function(data) {
    console.log(JSON.stringify(data));
  }
})


```


```javascript--nodejs
const request = require('node-fetch');


const headers = {
  'Accept':'*/*'


};


fetch('//localhost:7080//oauth/authorize?approvalParameters=string?user_oauth_approval=string',
{
  method: 'POST',


  headers: headers
})
.then(function(res) {
    return res.json();
}).then(function(body) {
    console.log(body);
});


```


```ruby
require 'rest-client'
require 'json'


headers = {
  'Accept' => '*/*'
}


result = RestClient.post '//localhost:7080//oauth/authorize',
  params: {
  'approvalParameters' => 'string',
'user_oauth_approval' => 'string'
}, headers: headers


p JSON.parse(result)


```


```python
import requests
headers = {
  'Accept': '*/*'
}


r = requests.post('//localhost:7080//oauth/authorize', params={
  'approvalParameters': 'string',  'user_oauth_approval': 'string'
}, headers = headers)


print r.json()


```


```java
URL obj = new URL("//localhost:7080//oauth/authorize?approvalParameters=string?user_oauth_approval=string");
HttpURLConnection con = (HttpURLConnection) obj.openConnection();
con.setRequestMethod("POST");
int responseCode = con.getResponseCode();
BufferedReader in = new BufferedReader(
    new InputStreamReader(con.getInputStream()));
String inputLine;
StringBuffer response = new StringBuffer();
while ((inputLine = in.readLine()) != null) {
    response.append(inputLine);
}
in.close();
System.out.println(response.toString());


```


`POST /oauth/authorize`


*approveOrDeny*


<h3 id="approveOrDenyUsingPOST-parameters">Parameters</h3>


|Parameter|In|Type|Required|Description|
|---|---|---|---|---|
|approvalParameters|query|string|true|approvalParameters|
|model|query|undefined|false|model|
|user_oauth_approval|query|string|true|No description|


> Example responses


<h3 id="approveOrDenyUsingPOST-responses">Responses</h3>


|Status|Meaning|Description|Schema|
|---|---|---|---|
|200|[OK](https://tools.ietf.org/html/rfc7231#section-6.3.1)|OK|[View](#schemaview)|
|201|[Created](https://tools.ietf.org/html/rfc7231#section-6.3.2)|Created|None|
|401|[Unauthorized](https://tools.ietf.org/html/rfc7235#section-3.1)|Unauthorized|None|
|403|[Forbidden](https://tools.ietf.org/html/rfc7231#section-6.5.3)|Forbidden|None|
|404|[Not Found](https://tools.ietf.org/html/rfc7231#section-6.5.4)|Not Found|None|


<aside class="success">
This operation does not require authentication
</aside>


## authorizeUsingPUT


<a id="opIdauthorizeUsingPUT"></a>


> Code samples


```shell
# You can also use wget
curl -X PUT //localhost:7080//oauth/authorize?parameters=string \
  -H 'Accept: */*'


```


```http
PUT //localhost:7080//oauth/authorize?parameters=string HTTP/1.1
Host: null


Accept: */*


```


```javascript
var headers = {
  'Accept':'*/*'


};


$.ajax({
  url: '//localhost:7080//oauth/authorize',
  method: 'put',
  data: '?parameters=string',
  headers: headers,
  success: function(data) {
    console.log(JSON.stringify(data));
  }
})


```


```javascript--nodejs
const request = require('node-fetch');


const headers = {
  'Accept':'*/*'


};


fetch('//localhost:7080//oauth/authorize?parameters=string',
{
  method: 'PUT',


  headers: headers
})
.then(function(res) {
    return res.json();
}).then(function(body) {
    console.log(body);
});


```


```ruby
require 'rest-client'
require 'json'


headers = {
  'Accept' => '*/*'
}


result = RestClient.put '//localhost:7080//oauth/authorize',
  params: {
  'parameters' => 'string'
}, headers: headers


p JSON.parse(result)


```


```python
import requests
headers = {
  'Accept': '*/*'
}


r = requests.put('//localhost:7080//oauth/authorize', params={
  'parameters': 'string'
}, headers = headers)


print r.json()


```


```java
URL obj = new URL("//localhost:7080//oauth/authorize?parameters=string");
HttpURLConnection con = (HttpURLConnection) obj.openConnection();
con.setRequestMethod("PUT");
int responseCode = con.getResponseCode();
BufferedReader in = new BufferedReader(
    new InputStreamReader(con.getInputStream()));
String inputLine;
StringBuffer response = new StringBuffer();
while ((inputLine = in.readLine()) != null) {
    response.append(inputLine);
}
in.close();
System.out.println(response.toString());


```


`PUT /oauth/authorize`


*authorize*


<h3 id="authorizeUsingPUT-parameters">Parameters</h3>


|Parameter|In|Type|Required|Description|
|---|---|---|---|---|
|model|query|undefined|false|model|
|parameters|query|string|true|parameters|


> Example responses


<h3 id="authorizeUsingPUT-responses">Responses</h3>


|Status|Meaning|Description|Schema|
|---|---|---|---|
|200|[OK](https://tools.ietf.org/html/rfc7231#section-6.3.1)|OK|[ModelAndView](#schemamodelandview)|
|201|[Created](https://tools.ietf.org/html/rfc7231#section-6.3.2)|Created|None|
|401|[Unauthorized](https://tools.ietf.org/html/rfc7235#section-3.1)|Unauthorized|None|
|403|[Forbidden](https://tools.ietf.org/html/rfc7231#section-6.5.3)|Forbidden|None|
|404|[Not Found](https://tools.ietf.org/html/rfc7231#section-6.5.4)|Not Found|None|


<aside class="success">
This operation does not require authentication
</aside>


## authorizeUsingDELETE


<a id="opIdauthorizeUsingDELETE"></a>


> Code samples


```shell
# You can also use wget
curl -X DELETE //localhost:7080//oauth/authorize?parameters=string \
  -H 'Accept: */*'


```


```http
DELETE //localhost:7080//oauth/authorize?parameters=string HTTP/1.1
Host: null


Accept: */*


```


```javascript
var headers = {
  'Accept':'*/*'


};


$.ajax({
  url: '//localhost:7080//oauth/authorize',
  method: 'delete',
  data: '?parameters=string',
  headers: headers,
  success: function(data) {
    console.log(JSON.stringify(data));
  }
})


```


```javascript--nodejs
const request = require('node-fetch');


const headers = {
  'Accept':'*/*'


};


fetch('//localhost:7080//oauth/authorize?parameters=string',
{
  method: 'DELETE',


  headers: headers
})
.then(function(res) {
    return res.json();
}).then(function(body) {
    console.log(body);
});


```


```ruby
require 'rest-client'
require 'json'


headers = {
  'Accept' => '*/*'
}


result = RestClient.delete '//localhost:7080//oauth/authorize',
  params: {
  'parameters' => 'string'
}, headers: headers


p JSON.parse(result)


```


```python
import requests
headers = {
  'Accept': '*/*'
}


r = requests.delete('//localhost:7080//oauth/authorize', params={
  'parameters': 'string'
}, headers = headers)


print r.json()


```


```java
URL obj = new URL("//localhost:7080//oauth/authorize?parameters=string");
HttpURLConnection con = (HttpURLConnection) obj.openConnection();
con.setRequestMethod("DELETE");
int responseCode = con.getResponseCode();
BufferedReader in = new BufferedReader(
    new InputStreamReader(con.getInputStream()));
String inputLine;
StringBuffer response = new StringBuffer();
while ((inputLine = in.readLine()) != null) {
    response.append(inputLine);
}
in.close();
System.out.println(response.toString());


```


`DELETE /oauth/authorize`


*authorize*


<h3 id="authorizeUsingDELETE-parameters">Parameters</h3>


|Parameter|In|Type|Required|Description|
|---|---|---|---|---|
|model|query|undefined|false|model|
|parameters|query|string|true|parameters|


> Example responses


<h3 id="authorizeUsingDELETE-responses">Responses</h3>


|Status|Meaning|Description|Schema|
|---|---|---|---|
|200|[OK](https://tools.ietf.org/html/rfc7231#section-6.3.1)|OK|[ModelAndView](#schemamodelandview)|
|204|[No Content](https://tools.ietf.org/html/rfc7231#section-6.3.5)|No Content|None|
|401|[Unauthorized](https://tools.ietf.org/html/rfc7235#section-3.1)|Unauthorized|None|
|403|[Forbidden](https://tools.ietf.org/html/rfc7231#section-6.5.3)|Forbidden|None|


<aside class="success">
This operation does not require authentication
</aside>


## authorizeUsingOPTIONS


<a id="opIdauthorizeUsingOPTIONS"></a>


> Code samples


```shell
# You can also use wget
curl -X OPTIONS //localhost:7080//oauth/authorize?parameters=string \
  -H 'Accept: */*'


```


```http
OPTIONS //localhost:7080//oauth/authorize?parameters=string HTTP/1.1
Host: null


Accept: */*


```


```javascript
var headers = {
  'Accept':'*/*'


};


$.ajax({
  url: '//localhost:7080//oauth/authorize',
  method: 'options',
  data: '?parameters=string',
  headers: headers,
  success: function(data) {
    console.log(JSON.stringify(data));
  }
})


```


```javascript--nodejs
const request = require('node-fetch');


const headers = {
  'Accept':'*/*'


};


fetch('//localhost:7080//oauth/authorize?parameters=string',
{
  method: 'OPTIONS',


  headers: headers
})
.then(function(res) {
    return res.json();
}).then(function(body) {
    console.log(body);
});


```


```ruby
require 'rest-client'
require 'json'


headers = {
  'Accept' => '*/*'
}


result = RestClient.options '//localhost:7080//oauth/authorize',
  params: {
  'parameters' => 'string'
}, headers: headers


p JSON.parse(result)


```


```python
import requests
headers = {
  'Accept': '*/*'
}


r = requests.options('//localhost:7080//oauth/authorize', params={
  'parameters': 'string'
}, headers = headers)


print r.json()


```


```java
URL obj = new URL("//localhost:7080//oauth/authorize?parameters=string");
HttpURLConnection con = (HttpURLConnection) obj.openConnection();
con.setRequestMethod("OPTIONS");
int responseCode = con.getResponseCode();
BufferedReader in = new BufferedReader(
    new InputStreamReader(con.getInputStream()));
String inputLine;
StringBuffer response = new StringBuffer();
while ((inputLine = in.readLine()) != null) {
    response.append(inputLine);
}
in.close();
System.out.println(response.toString());


```


`OPTIONS /oauth/authorize`


*authorize*


<h3 id="authorizeUsingOPTIONS-parameters">Parameters</h3>


|Parameter|In|Type|Required|Description|
|---|---|---|---|---|
|model|query|undefined|false|model|
|parameters|query|string|true|parameters|


> Example responses


<h3 id="authorizeUsingOPTIONS-responses">Responses</h3>


|Status|Meaning|Description|Schema|
|---|---|---|---|
|200|[OK](https://tools.ietf.org/html/rfc7231#section-6.3.1)|OK|[ModelAndView](#schemamodelandview)|
|204|[No Content](https://tools.ietf.org/html/rfc7231#section-6.3.5)|No Content|None|
|401|[Unauthorized](https://tools.ietf.org/html/rfc7235#section-3.1)|Unauthorized|None|
|403|[Forbidden](https://tools.ietf.org/html/rfc7231#section-6.5.3)|Forbidden|None|


<aside class="success">
This operation does not require authentication
</aside>


## authorizeUsingPATCH


<a id="opIdauthorizeUsingPATCH"></a>


> Code samples


```shell
# You can also use wget
curl -X PATCH //localhost:7080//oauth/authorize?parameters=string \
  -H 'Accept: */*'


```


```http
PATCH //localhost:7080//oauth/authorize?parameters=string HTTP/1.1
Host: null


Accept: */*


```


```javascript
var headers = {
  'Accept':'*/*'


};


$.ajax({
  url: '//localhost:7080//oauth/authorize',
  method: 'patch',
  data: '?parameters=string',
  headers: headers,
  success: function(data) {
    console.log(JSON.stringify(data));
  }
})


```


```javascript--nodejs
const request = require('node-fetch');


const headers = {
  'Accept':'*/*'


};


fetch('//localhost:7080//oauth/authorize?parameters=string',
{
  method: 'PATCH',


  headers: headers
})
.then(function(res) {
    return res.json();
}).then(function(body) {
    console.log(body);
});


```


```ruby
require 'rest-client'
require 'json'


headers = {
  'Accept' => '*/*'
}


result = RestClient.patch '//localhost:7080//oauth/authorize',
  params: {
  'parameters' => 'string'
}, headers: headers


p JSON.parse(result)


```


```python
import requests
headers = {
  'Accept': '*/*'
}


r = requests.patch('//localhost:7080//oauth/authorize', params={
  'parameters': 'string'
}, headers = headers)


print r.json()


```


```java
URL obj = new URL("//localhost:7080//oauth/authorize?parameters=string");
HttpURLConnection con = (HttpURLConnection) obj.openConnection();
con.setRequestMethod("PATCH");
int responseCode = con.getResponseCode();
BufferedReader in = new BufferedReader(
    new InputStreamReader(con.getInputStream()));
String inputLine;
StringBuffer response = new StringBuffer();
while ((inputLine = in.readLine()) != null) {
    response.append(inputLine);
}
in.close();
System.out.println(response.toString());


```


`PATCH /oauth/authorize`


*authorize*


<h3 id="authorizeUsingPATCH-parameters">Parameters</h3>


|Parameter|In|Type|Required|Description|
|---|---|---|---|---|
|model|query|undefined|false|model|
|parameters|query|string|true|parameters|


> Example responses


<h3 id="authorizeUsingPATCH-responses">Responses</h3>


|Status|Meaning|Description|Schema|
|---|---|---|---|
|200|[OK](https://tools.ietf.org/html/rfc7231#section-6.3.1)|OK|[ModelAndView](#schemamodelandview)|
|204|[No Content](https://tools.ietf.org/html/rfc7231#section-6.3.5)|No Content|None|
|401|[Unauthorized](https://tools.ietf.org/html/rfc7235#section-3.1)|Unauthorized|None|
|403|[Forbidden](https://tools.ietf.org/html/rfc7231#section-6.5.3)|Forbidden|None|


<aside class="success">
This operation does not require authentication
</aside>


<h1 id="Public-API-for-appointman-check-token-endpoint">check-token-endpoint</h1>


Check Token Endpoint


## checkTokenUsingGET


<a id="opIdcheckTokenUsingGET"></a>


> Code samples


```shell
# You can also use wget
curl -X GET //localhost:7080//oauth/check_token?token=string \
  -H 'Accept: */*'


```


```http
GET //localhost:7080//oauth/check_token?token=string HTTP/1.1
Host: null


Accept: */*


```


```javascript
var headers = {
  'Accept':'*/*'


};


$.ajax({
  url: '//localhost:7080//oauth/check_token',
  method: 'get',
  data: '?token=string',
  headers: headers,
  success: function(data) {
    console.log(JSON.stringify(data));
  }
})


```


```javascript--nodejs
const request = require('node-fetch');


const headers = {
  'Accept':'*/*'


};


fetch('//localhost:7080//oauth/check_token?token=string',
{
  method: 'GET',


  headers: headers
})
.then(function(res) {
    return res.json();
}).then(function(body) {
    console.log(body);
});


```


```ruby
require 'rest-client'
require 'json'


headers = {
  'Accept' => '*/*'
}


result = RestClient.get '//localhost:7080//oauth/check_token',
  params: {
  'token' => 'string'
}, headers: headers


p JSON.parse(result)


```


```python
import requests
headers = {
  'Accept': '*/*'
}


r = requests.get('//localhost:7080//oauth/check_token', params={
  'token': 'string'
}, headers = headers)


print r.json()


```


```java
URL obj = new URL("//localhost:7080//oauth/check_token?token=string");
HttpURLConnection con = (HttpURLConnection) obj.openConnection();
con.setRequestMethod("GET");
int responseCode = con.getResponseCode();
BufferedReader in = new BufferedReader(
    new InputStreamReader(con.getInputStream()));
String inputLine;
StringBuffer response = new StringBuffer();
while ((inputLine = in.readLine()) != null) {
    response.append(inputLine);
}
in.close();
System.out.println(response.toString());


```


`GET /oauth/check_token`


*checkToken*


<h3 id="checkTokenUsingGET-parameters">Parameters</h3>


|Parameter|In|Type|Required|Description|
|---|---|---|---|---|
|token|query|string|true|token|


> Example responses


<h3 id="checkTokenUsingGET-responses">Responses</h3>


|Status|Meaning|Description|Schema|
|---|---|---|---|
|200|[OK](https://tools.ietf.org/html/rfc7231#section-6.3.1)|OK|Inline|
|401|[Unauthorized](https://tools.ietf.org/html/rfc7235#section-3.1)|Unauthorized|None|
|403|[Forbidden](https://tools.ietf.org/html/rfc7231#section-6.5.3)|Forbidden|None|
|404|[Not Found](https://tools.ietf.org/html/rfc7231#section-6.5.4)|Not Found|None|


<h3 id="checkTokenUsingGET-responseschema">Response Schema</h3>


Status Code **200**


|Name|Type|Required|Description|
|---|---|---|---|


<aside class="success">
This operation does not require authentication
</aside>


## checkTokenUsingHEAD


<a id="opIdcheckTokenUsingHEAD"></a>


> Code samples


```shell
# You can also use wget
curl -X HEAD //localhost:7080//oauth/check_token?token=string \
  -H 'Accept: */*'


```


```http
HEAD //localhost:7080//oauth/check_token?token=string HTTP/1.1
Host: null


Accept: */*


```


```javascript
var headers = {
  'Accept':'*/*'


};


$.ajax({
  url: '//localhost:7080//oauth/check_token',
  method: 'head',
  data: '?token=string',
  headers: headers,
  success: function(data) {
    console.log(JSON.stringify(data));
  }
})


```


```javascript--nodejs
const request = require('node-fetch');


const headers = {
  'Accept':'*/*'


};


fetch('//localhost:7080//oauth/check_token?token=string',
{
  method: 'HEAD',


  headers: headers
})
.then(function(res) {
    return res.json();
}).then(function(body) {
    console.log(body);
});


```


```ruby
require 'rest-client'
require 'json'


headers = {
  'Accept' => '*/*'
}


result = RestClient.head '//localhost:7080//oauth/check_token',
  params: {
  'token' => 'string'
}, headers: headers


p JSON.parse(result)


```


```python
import requests
headers = {
  'Accept': '*/*'
}


r = requests.head('//localhost:7080//oauth/check_token', params={
  'token': 'string'
}, headers = headers)


print r.json()


```


```java
URL obj = new URL("//localhost:7080//oauth/check_token?token=string");
HttpURLConnection con = (HttpURLConnection) obj.openConnection();
con.setRequestMethod("HEAD");
int responseCode = con.getResponseCode();
BufferedReader in = new BufferedReader(
    new InputStreamReader(con.getInputStream()));
String inputLine;
StringBuffer response = new StringBuffer();
while ((inputLine = in.readLine()) != null) {
    response.append(inputLine);
}
in.close();
System.out.println(response.toString());


```


`HEAD /oauth/check_token`


*checkToken*


<h3 id="checkTokenUsingHEAD-parameters">Parameters</h3>


|Parameter|In|Type|Required|Description|
|---|---|---|---|---|
|token|query|string|true|token|


> Example responses


<h3 id="checkTokenUsingHEAD-responses">Responses</h3>


|Status|Meaning|Description|Schema|
|---|---|---|---|
|200|[OK](https://tools.ietf.org/html/rfc7231#section-6.3.1)|OK|Inline|
|204|[No Content](https://tools.ietf.org/html/rfc7231#section-6.3.5)|No Content|None|
|401|[Unauthorized](https://tools.ietf.org/html/rfc7235#section-3.1)|Unauthorized|None|
|403|[Forbidden](https://tools.ietf.org/html/rfc7231#section-6.5.3)|Forbidden|None|


<h3 id="checkTokenUsingHEAD-responseschema">Response Schema</h3>


Status Code **200**


|Name|Type|Required|Description|
|---|---|---|---|


<aside class="success">
This operation does not require authentication
</aside>


## checkTokenUsingPOST


<a id="opIdcheckTokenUsingPOST"></a>


> Code samples


```shell
# You can also use wget
curl -X POST //localhost:7080//oauth/check_token?token=string \
  -H 'Accept: */*'


```


```http
POST //localhost:7080//oauth/check_token?token=string HTTP/1.1
Host: null


Accept: */*


```


```javascript
var headers = {
  'Accept':'*/*'


};


$.ajax({
  url: '//localhost:7080//oauth/check_token',
  method: 'post',
  data: '?token=string',
  headers: headers,
  success: function(data) {
    console.log(JSON.stringify(data));
  }
})


```


```javascript--nodejs
const request = require('node-fetch');


const headers = {
  'Accept':'*/*'


};


fetch('//localhost:7080//oauth/check_token?token=string',
{
  method: 'POST',


  headers: headers
})
.then(function(res) {
    return res.json();
}).then(function(body) {
    console.log(body);
});


```


```ruby
require 'rest-client'
require 'json'


headers = {
  'Accept' => '*/*'
}


result = RestClient.post '//localhost:7080//oauth/check_token',
  params: {
  'token' => 'string'
}, headers: headers


p JSON.parse(result)


```


```python
import requests
headers = {
  'Accept': '*/*'
}


r = requests.post('//localhost:7080//oauth/check_token', params={
  'token': 'string'
}, headers = headers)


print r.json()


```


```java
URL obj = new URL("//localhost:7080//oauth/check_token?token=string");
HttpURLConnection con = (HttpURLConnection) obj.openConnection();
con.setRequestMethod("POST");
int responseCode = con.getResponseCode();
BufferedReader in = new BufferedReader(
    new InputStreamReader(con.getInputStream()));
String inputLine;
StringBuffer response = new StringBuffer();
while ((inputLine = in.readLine()) != null) {
    response.append(inputLine);
}
in.close();
System.out.println(response.toString());


```


`POST /oauth/check_token`


*checkToken*


<h3 id="checkTokenUsingPOST-parameters">Parameters</h3>


|Parameter|In|Type|Required|Description|
|---|---|---|---|---|
|token|query|string|true|token|


> Example responses


<h3 id="checkTokenUsingPOST-responses">Responses</h3>


|Status|Meaning|Description|Schema|
|---|---|---|---|
|200|[OK](https://tools.ietf.org/html/rfc7231#section-6.3.1)|OK|Inline|
|201|[Created](https://tools.ietf.org/html/rfc7231#section-6.3.2)|Created|None|
|401|[Unauthorized](https://tools.ietf.org/html/rfc7235#section-3.1)|Unauthorized|None|
|403|[Forbidden](https://tools.ietf.org/html/rfc7231#section-6.5.3)|Forbidden|None|
|404|[Not Found](https://tools.ietf.org/html/rfc7231#section-6.5.4)|Not Found|None|


<h3 id="checkTokenUsingPOST-responseschema">Response Schema</h3>


Status Code **200**


|Name|Type|Required|Description|
|---|---|---|---|


<aside class="success">
This operation does not require authentication
</aside>


## checkTokenUsingPUT


<a id="opIdcheckTokenUsingPUT"></a>


> Code samples


```shell
# You can also use wget
curl -X PUT //localhost:7080//oauth/check_token?token=string \
  -H 'Accept: */*'


```


```http
PUT //localhost:7080//oauth/check_token?token=string HTTP/1.1
Host: null


Accept: */*


```


```javascript
var headers = {
  'Accept':'*/*'


};


$.ajax({
  url: '//localhost:7080//oauth/check_token',
  method: 'put',
  data: '?token=string',
  headers: headers,
  success: function(data) {
    console.log(JSON.stringify(data));
  }
})


```


```javascript--nodejs
const request = require('node-fetch');


const headers = {
  'Accept':'*/*'


};


fetch('//localhost:7080//oauth/check_token?token=string',
{
  method: 'PUT',


  headers: headers
})
.then(function(res) {
    return res.json();
}).then(function(body) {
    console.log(body);
});


```


```ruby
require 'rest-client'
require 'json'


headers = {
  'Accept' => '*/*'
}


result = RestClient.put '//localhost:7080//oauth/check_token',
  params: {
  'token' => 'string'
}, headers: headers


p JSON.parse(result)


```


```python
import requests
headers = {
  'Accept': '*/*'
}


r = requests.put('//localhost:7080//oauth/check_token', params={
  'token': 'string'
}, headers = headers)


print r.json()


```


```java
URL obj = new URL("//localhost:7080//oauth/check_token?token=string");
HttpURLConnection con = (HttpURLConnection) obj.openConnection();
con.setRequestMethod("PUT");
int responseCode = con.getResponseCode();
BufferedReader in = new BufferedReader(
    new InputStreamReader(con.getInputStream()));
String inputLine;
StringBuffer response = new StringBuffer();
while ((inputLine = in.readLine()) != null) {
    response.append(inputLine);
}
in.close();
System.out.println(response.toString());


```


`PUT /oauth/check_token`


*checkToken*


<h3 id="checkTokenUsingPUT-parameters">Parameters</h3>


|Parameter|In|Type|Required|Description|
|---|---|---|---|---|
|token|query|string|true|token|


> Example responses


<h3 id="checkTokenUsingPUT-responses">Responses</h3>


|Status|Meaning|Description|Schema|
|---|---|---|---|
|200|[OK](https://tools.ietf.org/html/rfc7231#section-6.3.1)|OK|Inline|
|201|[Created](https://tools.ietf.org/html/rfc7231#section-6.3.2)|Created|None|
|401|[Unauthorized](https://tools.ietf.org/html/rfc7235#section-3.1)|Unauthorized|None|
|403|[Forbidden](https://tools.ietf.org/html/rfc7231#section-6.5.3)|Forbidden|None|
|404|[Not Found](https://tools.ietf.org/html/rfc7231#section-6.5.4)|Not Found|None|


<h3 id="checkTokenUsingPUT-responseschema">Response Schema</h3>


Status Code **200**


|Name|Type|Required|Description|
|---|---|---|---|


<aside class="success">
This operation does not require authentication
</aside>


## checkTokenUsingDELETE


<a id="opIdcheckTokenUsingDELETE"></a>


> Code samples


```shell
# You can also use wget
curl -X DELETE //localhost:7080//oauth/check_token?token=string \
  -H 'Accept: */*'


```


```http
DELETE //localhost:7080//oauth/check_token?token=string HTTP/1.1
Host: null


Accept: */*


```


```javascript
var headers = {
  'Accept':'*/*'


};


$.ajax({
  url: '//localhost:7080//oauth/check_token',
  method: 'delete',
  data: '?token=string',
  headers: headers,
  success: function(data) {
    console.log(JSON.stringify(data));
  }
})


```


```javascript--nodejs
const request = require('node-fetch');


const headers = {
  'Accept':'*/*'


};


fetch('//localhost:7080//oauth/check_token?token=string',
{
  method: 'DELETE',


  headers: headers
})
.then(function(res) {
    return res.json();
}).then(function(body) {
    console.log(body);
});


```


```ruby
require 'rest-client'
require 'json'


headers = {
  'Accept' => '*/*'
}


result = RestClient.delete '//localhost:7080//oauth/check_token',
  params: {
  'token' => 'string'
}, headers: headers


p JSON.parse(result)


```


```python
import requests
headers = {
  'Accept': '*/*'
}


r = requests.delete('//localhost:7080//oauth/check_token', params={
  'token': 'string'
}, headers = headers)


print r.json()


```


```java
URL obj = new URL("//localhost:7080//oauth/check_token?token=string");
HttpURLConnection con = (HttpURLConnection) obj.openConnection();
con.setRequestMethod("DELETE");
int responseCode = con.getResponseCode();
BufferedReader in = new BufferedReader(
    new InputStreamReader(con.getInputStream()));
String inputLine;
StringBuffer response = new StringBuffer();
while ((inputLine = in.readLine()) != null) {
    response.append(inputLine);
}
in.close();
System.out.println(response.toString());


```


`DELETE /oauth/check_token`


*checkToken*


<h3 id="checkTokenUsingDELETE-parameters">Parameters</h3>


|Parameter|In|Type|Required|Description|
|---|---|---|---|---|
|token|query|string|true|token|


> Example responses


<h3 id="checkTokenUsingDELETE-responses">Responses</h3>


|Status|Meaning|Description|Schema|
|---|---|---|---|
|200|[OK](https://tools.ietf.org/html/rfc7231#section-6.3.1)|OK|Inline|
|204|[No Content](https://tools.ietf.org/html/rfc7231#section-6.3.5)|No Content|None|
|401|[Unauthorized](https://tools.ietf.org/html/rfc7235#section-3.1)|Unauthorized|None|
|403|[Forbidden](https://tools.ietf.org/html/rfc7231#section-6.5.3)|Forbidden|None|


<h3 id="checkTokenUsingDELETE-responseschema">Response Schema</h3>


Status Code **200**


|Name|Type|Required|Description|
|---|---|---|---|


<aside class="success">
This operation does not require authentication
</aside>


## checkTokenUsingOPTIONS


<a id="opIdcheckTokenUsingOPTIONS"></a>


> Code samples


```shell
# You can also use wget
curl -X OPTIONS //localhost:7080//oauth/check_token?token=string \
  -H 'Accept: */*'


```


```http
OPTIONS //localhost:7080//oauth/check_token?token=string HTTP/1.1
Host: null


Accept: */*


```


```javascript
var headers = {
  'Accept':'*/*'


};


$.ajax({
  url: '//localhost:7080//oauth/check_token',
  method: 'options',
  data: '?token=string',
  headers: headers,
  success: function(data) {
    console.log(JSON.stringify(data));
  }
})


```


```javascript--nodejs
const request = require('node-fetch');


const headers = {
  'Accept':'*/*'


};


fetch('//localhost:7080//oauth/check_token?token=string',
{
  method: 'OPTIONS',


  headers: headers
})
.then(function(res) {
    return res.json();
}).then(function(body) {
    console.log(body);
});


```


```ruby
require 'rest-client'
require 'json'


headers = {
  'Accept' => '*/*'
}


result = RestClient.options '//localhost:7080//oauth/check_token',
  params: {
  'token' => 'string'
}, headers: headers


p JSON.parse(result)


```


```python
import requests
headers = {
  'Accept': '*/*'
}


r = requests.options('//localhost:7080//oauth/check_token', params={
  'token': 'string'
}, headers = headers)


print r.json()


```


```java
URL obj = new URL("//localhost:7080//oauth/check_token?token=string");
HttpURLConnection con = (HttpURLConnection) obj.openConnection();
con.setRequestMethod("OPTIONS");
int responseCode = con.getResponseCode();
BufferedReader in = new BufferedReader(
    new InputStreamReader(con.getInputStream()));
String inputLine;
StringBuffer response = new StringBuffer();
while ((inputLine = in.readLine()) != null) {
    response.append(inputLine);
}
in.close();
System.out.println(response.toString());


```


`OPTIONS /oauth/check_token`


*checkToken*


<h3 id="checkTokenUsingOPTIONS-parameters">Parameters</h3>


|Parameter|In|Type|Required|Description|
|---|---|---|---|---|
|token|query|string|true|token|


> Example responses


<h3 id="checkTokenUsingOPTIONS-responses">Responses</h3>


|Status|Meaning|Description|Schema|
|---|---|---|---|
|200|[OK](https://tools.ietf.org/html/rfc7231#section-6.3.1)|OK|Inline|
|204|[No Content](https://tools.ietf.org/html/rfc7231#section-6.3.5)|No Content|None|
|401|[Unauthorized](https://tools.ietf.org/html/rfc7235#section-3.1)|Unauthorized|None|
|403|[Forbidden](https://tools.ietf.org/html/rfc7231#section-6.5.3)|Forbidden|None|


<h3 id="checkTokenUsingOPTIONS-responseschema">Response Schema</h3>


Status Code **200**


|Name|Type|Required|Description|
|---|---|---|---|


<aside class="success">
This operation does not require authentication
</aside>


## checkTokenUsingPATCH


<a id="opIdcheckTokenUsingPATCH"></a>


> Code samples


```shell
# You can also use wget
curl -X PATCH //localhost:7080//oauth/check_token?token=string \
  -H 'Accept: */*'


```


```http
PATCH //localhost:7080//oauth/check_token?token=string HTTP/1.1
Host: null


Accept: */*


```


```javascript
var headers = {
  'Accept':'*/*'


};


$.ajax({
  url: '//localhost:7080//oauth/check_token',
  method: 'patch',
  data: '?token=string',
  headers: headers,
  success: function(data) {
    console.log(JSON.stringify(data));
  }
})


```


```javascript--nodejs
const request = require('node-fetch');


const headers = {
  'Accept':'*/*'


};


fetch('//localhost:7080//oauth/check_token?token=string',
{
  method: 'PATCH',


  headers: headers
})
.then(function(res) {
    return res.json();
}).then(function(body) {
    console.log(body);
});


```


```ruby
require 'rest-client'
require 'json'


headers = {
  'Accept' => '*/*'
}


result = RestClient.patch '//localhost:7080//oauth/check_token',
  params: {
  'token' => 'string'
}, headers: headers


p JSON.parse(result)


```


```python
import requests
headers = {
  'Accept': '*/*'
}


r = requests.patch('//localhost:7080//oauth/check_token', params={
  'token': 'string'
}, headers = headers)


print r.json()


```


```java
URL obj = new URL("//localhost:7080//oauth/check_token?token=string");
HttpURLConnection con = (HttpURLConnection) obj.openConnection();
con.setRequestMethod("PATCH");
int responseCode = con.getResponseCode();
BufferedReader in = new BufferedReader(
    new InputStreamReader(con.getInputStream()));
String inputLine;
StringBuffer response = new StringBuffer();
while ((inputLine = in.readLine()) != null) {
    response.append(inputLine);
}
in.close();
System.out.println(response.toString());


```


`PATCH /oauth/check_token`


*checkToken*


<h3 id="checkTokenUsingPATCH-parameters">Parameters</h3>


|Parameter|In|Type|Required|Description|
|---|---|---|---|---|
|token|query|string|true|token|


> Example responses


<h3 id="checkTokenUsingPATCH-responses">Responses</h3>


|Status|Meaning|Description|Schema|
|---|---|---|---|
|200|[OK](https://tools.ietf.org/html/rfc7231#section-6.3.1)|OK|Inline|
|204|[No Content](https://tools.ietf.org/html/rfc7231#section-6.3.5)|No Content|None|
|401|[Unauthorized](https://tools.ietf.org/html/rfc7235#section-3.1)|Unauthorized|None|
|403|[Forbidden](https://tools.ietf.org/html/rfc7231#section-6.5.3)|Forbidden|None|


<h3 id="checkTokenUsingPATCH-responseschema">Response Schema</h3>


Status Code **200**


|Name|Type|Required|Description|
|---|---|---|---|


<aside class="success">
This operation does not require authentication
</aside>


<h1 id="Public-API-for-appointman-whitelabel-approval-endpoint">whitelabel-approval-endpoint</h1>


Whitelabel Approval Endpoint


## getAccessConfirmationUsingGET


<a id="opIdgetAccessConfirmationUsingGET"></a>


> Code samples


```shell
# You can also use wget
curl -X GET //localhost:7080//oauth/confirm_access \
  -H 'Accept: */*'


```


```http
GET //localhost:7080//oauth/confirm_access HTTP/1.1
Host: null


Accept: */*


```


```javascript
var headers = {
  'Accept':'*/*'


};


$.ajax({
  url: '//localhost:7080//oauth/confirm_access',
  method: 'get',


  headers: headers,
  success: function(data) {
    console.log(JSON.stringify(data));
  }
})


```


```javascript--nodejs
const request = require('node-fetch');


const headers = {
  'Accept':'*/*'


};


fetch('//localhost:7080//oauth/confirm_access',
{
  method: 'GET',


  headers: headers
})
.then(function(res) {
    return res.json();
}).then(function(body) {
    console.log(body);
});


```


```ruby
require 'rest-client'
require 'json'


headers = {
  'Accept' => '*/*'
}


result = RestClient.get '//localhost:7080//oauth/confirm_access',
  params: {
  }, headers: headers


p JSON.parse(result)


```


```python
import requests
headers = {
  'Accept': '*/*'
}


r = requests.get('//localhost:7080//oauth/confirm_access', params={


}, headers = headers)


print r.json()


```


```java
URL obj = new URL("//localhost:7080//oauth/confirm_access");
HttpURLConnection con = (HttpURLConnection) obj.openConnection();
con.setRequestMethod("GET");
int responseCode = con.getResponseCode();
BufferedReader in = new BufferedReader(
    new InputStreamReader(con.getInputStream()));
String inputLine;
StringBuffer response = new StringBuffer();
while ((inputLine = in.readLine()) != null) {
    response.append(inputLine);
}
in.close();
System.out.println(response.toString());


```


`GET /oauth/confirm_access`


*getAccessConfirmation*


<h3 id="getAccessConfirmationUsingGET-parameters">Parameters</h3>


|Parameter|In|Type|Required|Description|
|---|---|---|---|---|
|model|query|undefined|false|model|


> Example responses


<h3 id="getAccessConfirmationUsingGET-responses">Responses</h3>


|Status|Meaning|Description|Schema|
|---|---|---|---|
|200|[OK](https://tools.ietf.org/html/rfc7231#section-6.3.1)|OK|[ModelAndView](#schemamodelandview)|
|401|[Unauthorized](https://tools.ietf.org/html/rfc7235#section-3.1)|Unauthorized|None|
|403|[Forbidden](https://tools.ietf.org/html/rfc7231#section-6.5.3)|Forbidden|None|
|404|[Not Found](https://tools.ietf.org/html/rfc7231#section-6.5.4)|Not Found|None|


<aside class="success">
This operation does not require authentication
</aside>


## getAccessConfirmationUsingHEAD


<a id="opIdgetAccessConfirmationUsingHEAD"></a>


> Code samples


```shell
# You can also use wget
curl -X HEAD //localhost:7080//oauth/confirm_access \
  -H 'Accept: */*'


```


```http
HEAD //localhost:7080//oauth/confirm_access HTTP/1.1
Host: null


Accept: */*


```


```javascript
var headers = {
  'Accept':'*/*'


};


$.ajax({
  url: '//localhost:7080//oauth/confirm_access',
  method: 'head',


  headers: headers,
  success: function(data) {
    console.log(JSON.stringify(data));
  }
})


```


```javascript--nodejs
const request = require('node-fetch');


const headers = {
  'Accept':'*/*'


};


fetch('//localhost:7080//oauth/confirm_access',
{
  method: 'HEAD',


  headers: headers
})
.then(function(res) {
    return res.json();
}).then(function(body) {
    console.log(body);
});


```


```ruby
require 'rest-client'
require 'json'


headers = {
  'Accept' => '*/*'
}


result = RestClient.head '//localhost:7080//oauth/confirm_access',
  params: {
  }, headers: headers


p JSON.parse(result)


```


```python
import requests
headers = {
  'Accept': '*/*'
}


r = requests.head('//localhost:7080//oauth/confirm_access', params={


}, headers = headers)


print r.json()


```


```java
URL obj = new URL("//localhost:7080//oauth/confirm_access");
HttpURLConnection con = (HttpURLConnection) obj.openConnection();
con.setRequestMethod("HEAD");
int responseCode = con.getResponseCode();
BufferedReader in = new BufferedReader(
    new InputStreamReader(con.getInputStream()));
String inputLine;
StringBuffer response = new StringBuffer();
while ((inputLine = in.readLine()) != null) {
    response.append(inputLine);
}
in.close();
System.out.println(response.toString());


```


`HEAD /oauth/confirm_access`


*getAccessConfirmation*


<h3 id="getAccessConfirmationUsingHEAD-parameters">Parameters</h3>


|Parameter|In|Type|Required|Description|
|---|---|---|---|---|
|model|query|undefined|false|model|


> Example responses


<h3 id="getAccessConfirmationUsingHEAD-responses">Responses</h3>


|Status|Meaning|Description|Schema|
|---|---|---|---|
|200|[OK](https://tools.ietf.org/html/rfc7231#section-6.3.1)|OK|[ModelAndView](#schemamodelandview)|
|204|[No Content](https://tools.ietf.org/html/rfc7231#section-6.3.5)|No Content|None|
|401|[Unauthorized](https://tools.ietf.org/html/rfc7235#section-3.1)|Unauthorized|None|
|403|[Forbidden](https://tools.ietf.org/html/rfc7231#section-6.5.3)|Forbidden|None|


<aside class="success">
This operation does not require authentication
</aside>


## getAccessConfirmationUsingPOST


<a id="opIdgetAccessConfirmationUsingPOST"></a>


> Code samples


```shell
# You can also use wget
curl -X POST //localhost:7080//oauth/confirm_access \
  -H 'Accept: */*'


```


```http
POST //localhost:7080//oauth/confirm_access HTTP/1.1
Host: null


Accept: */*


```


```javascript
var headers = {
  'Accept':'*/*'


};


$.ajax({
  url: '//localhost:7080//oauth/confirm_access',
  method: 'post',


  headers: headers,
  success: function(data) {
    console.log(JSON.stringify(data));
  }
})


```


```javascript--nodejs
const request = require('node-fetch');


const headers = {
  'Accept':'*/*'


};


fetch('//localhost:7080//oauth/confirm_access',
{
  method: 'POST',


  headers: headers
})
.then(function(res) {
    return res.json();
}).then(function(body) {
    console.log(body);
});


```


```ruby
require 'rest-client'
require 'json'


headers = {
  'Accept' => '*/*'
}


result = RestClient.post '//localhost:7080//oauth/confirm_access',
  params: {
  }, headers: headers


p JSON.parse(result)


```


```python
import requests
headers = {
  'Accept': '*/*'
}


r = requests.post('//localhost:7080//oauth/confirm_access', params={


}, headers = headers)


print r.json()


```


```java
URL obj = new URL("//localhost:7080//oauth/confirm_access");
HttpURLConnection con = (HttpURLConnection) obj.openConnection();
con.setRequestMethod("POST");
int responseCode = con.getResponseCode();
BufferedReader in = new BufferedReader(
    new InputStreamReader(con.getInputStream()));
String inputLine;
StringBuffer response = new StringBuffer();
while ((inputLine = in.readLine()) != null) {
    response.append(inputLine);
}
in.close();
System.out.println(response.toString());


```


`POST /oauth/confirm_access`


*getAccessConfirmation*


<h3 id="getAccessConfirmationUsingPOST-parameters">Parameters</h3>


|Parameter|In|Type|Required|Description|
|---|---|---|---|---|
|model|query|undefined|false|model|


> Example responses


<h3 id="getAccessConfirmationUsingPOST-responses">Responses</h3>


|Status|Meaning|Description|Schema|
|---|---|---|---|
|200|[OK](https://tools.ietf.org/html/rfc7231#section-6.3.1)|OK|[ModelAndView](#schemamodelandview)|
|201|[Created](https://tools.ietf.org/html/rfc7231#section-6.3.2)|Created|None|
|401|[Unauthorized](https://tools.ietf.org/html/rfc7235#section-3.1)|Unauthorized|None|
|403|[Forbidden](https://tools.ietf.org/html/rfc7231#section-6.5.3)|Forbidden|None|
|404|[Not Found](https://tools.ietf.org/html/rfc7231#section-6.5.4)|Not Found|None|


<aside class="success">
This operation does not require authentication
</aside>


## getAccessConfirmationUsingPUT


<a id="opIdgetAccessConfirmationUsingPUT"></a>


> Code samples


```shell
# You can also use wget
curl -X PUT //localhost:7080//oauth/confirm_access \
  -H 'Accept: */*'


```


```http
PUT //localhost:7080//oauth/confirm_access HTTP/1.1
Host: null


Accept: */*


```


```javascript
var headers = {
  'Accept':'*/*'


};


$.ajax({
  url: '//localhost:7080//oauth/confirm_access',
  method: 'put',


  headers: headers,
  success: function(data) {
    console.log(JSON.stringify(data));
  }
})


```


```javascript--nodejs
const request = require('node-fetch');


const headers = {
  'Accept':'*/*'


};


fetch('//localhost:7080//oauth/confirm_access',
{
  method: 'PUT',


  headers: headers
})
.then(function(res) {
    return res.json();
}).then(function(body) {
    console.log(body);
});


```


```ruby
require 'rest-client'
require 'json'


headers = {
  'Accept' => '*/*'
}


result = RestClient.put '//localhost:7080//oauth/confirm_access',
  params: {
  }, headers: headers


p JSON.parse(result)


```


```python
import requests
headers = {
  'Accept': '*/*'
}


r = requests.put('//localhost:7080//oauth/confirm_access', params={


}, headers = headers)


print r.json()


```


```java
URL obj = new URL("//localhost:7080//oauth/confirm_access");
HttpURLConnection con = (HttpURLConnection) obj.openConnection();
con.setRequestMethod("PUT");
int responseCode = con.getResponseCode();
BufferedReader in = new BufferedReader(
    new InputStreamReader(con.getInputStream()));
String inputLine;
StringBuffer response = new StringBuffer();
while ((inputLine = in.readLine()) != null) {
    response.append(inputLine);
}
in.close();
System.out.println(response.toString());


```


`PUT /oauth/confirm_access`


*getAccessConfirmation*


<h3 id="getAccessConfirmationUsingPUT-parameters">Parameters</h3>


|Parameter|In|Type|Required|Description|
|---|---|---|---|---|
|model|query|undefined|false|model|


> Example responses


<h3 id="getAccessConfirmationUsingPUT-responses">Responses</h3>


|Status|Meaning|Description|Schema|
|---|---|---|---|
|200|[OK](https://tools.ietf.org/html/rfc7231#section-6.3.1)|OK|[ModelAndView](#schemamodelandview)|
|201|[Created](https://tools.ietf.org/html/rfc7231#section-6.3.2)|Created|None|
|401|[Unauthorized](https://tools.ietf.org/html/rfc7235#section-3.1)|Unauthorized|None|
|403|[Forbidden](https://tools.ietf.org/html/rfc7231#section-6.5.3)|Forbidden|None|
|404|[Not Found](https://tools.ietf.org/html/rfc7231#section-6.5.4)|Not Found|None|


<aside class="success">
This operation does not require authentication
</aside>


## getAccessConfirmationUsingDELETE


<a id="opIdgetAccessConfirmationUsingDELETE"></a>


> Code samples


```shell
# You can also use wget
curl -X DELETE //localhost:7080//oauth/confirm_access \
  -H 'Accept: */*'


```


```http
DELETE //localhost:7080//oauth/confirm_access HTTP/1.1
Host: null


Accept: */*


```


```javascript
var headers = {
  'Accept':'*/*'


};


$.ajax({
  url: '//localhost:7080//oauth/confirm_access',
  method: 'delete',


  headers: headers,
  success: function(data) {
    console.log(JSON.stringify(data));
  }
})


```


```javascript--nodejs
const request = require('node-fetch');


const headers = {
  'Accept':'*/*'


};


fetch('//localhost:7080//oauth/confirm_access',
{
  method: 'DELETE',


  headers: headers
})
.then(function(res) {
    return res.json();
}).then(function(body) {
    console.log(body);
});


```


```ruby
require 'rest-client'
require 'json'


headers = {
  'Accept' => '*/*'
}


result = RestClient.delete '//localhost:7080//oauth/confirm_access',
  params: {
  }, headers: headers


p JSON.parse(result)


```


```python
import requests
headers = {
  'Accept': '*/*'
}


r = requests.delete('//localhost:7080//oauth/confirm_access', params={


}, headers = headers)


print r.json()


```


```java
URL obj = new URL("//localhost:7080//oauth/confirm_access");
HttpURLConnection con = (HttpURLConnection) obj.openConnection();
con.setRequestMethod("DELETE");
int responseCode = con.getResponseCode();
BufferedReader in = new BufferedReader(
    new InputStreamReader(con.getInputStream()));
String inputLine;
StringBuffer response = new StringBuffer();
while ((inputLine = in.readLine()) != null) {
    response.append(inputLine);
}
in.close();
System.out.println(response.toString());


```


`DELETE /oauth/confirm_access`


*getAccessConfirmation*


<h3 id="getAccessConfirmationUsingDELETE-parameters">Parameters</h3>


|Parameter|In|Type|Required|Description|
|---|---|---|---|---|
|model|query|undefined|false|model|


> Example responses


<h3 id="getAccessConfirmationUsingDELETE-responses">Responses</h3>


|Status|Meaning|Description|Schema|
|---|---|---|---|
|200|[OK](https://tools.ietf.org/html/rfc7231#section-6.3.1)|OK|[ModelAndView](#schemamodelandview)|
|204|[No Content](https://tools.ietf.org/html/rfc7231#section-6.3.5)|No Content|None|
|401|[Unauthorized](https://tools.ietf.org/html/rfc7235#section-3.1)|Unauthorized|None|
|403|[Forbidden](https://tools.ietf.org/html/rfc7231#section-6.5.3)|Forbidden|None|


<aside class="success">
This operation does not require authentication
</aside>


## getAccessConfirmationUsingOPTIONS


<a id="opIdgetAccessConfirmationUsingOPTIONS"></a>


> Code samples


```shell
# You can also use wget
curl -X OPTIONS //localhost:7080//oauth/confirm_access \
  -H 'Accept: */*'


```


```http
OPTIONS //localhost:7080//oauth/confirm_access HTTP/1.1
Host: null


Accept: */*


```


```javascript
var headers = {
  'Accept':'*/*'


};


$.ajax({
  url: '//localhost:7080//oauth/confirm_access',
  method: 'options',


  headers: headers,
  success: function(data) {
    console.log(JSON.stringify(data));
  }
})


```


```javascript--nodejs
const request = require('node-fetch');


const headers = {
  'Accept':'*/*'


};


fetch('//localhost:7080//oauth/confirm_access',
{
  method: 'OPTIONS',


  headers: headers
})
.then(function(res) {
    return res.json();
}).then(function(body) {
    console.log(body);
});


```


```ruby
require 'rest-client'
require 'json'


headers = {
  'Accept' => '*/*'
}


result = RestClient.options '//localhost:7080//oauth/confirm_access',
  params: {
  }, headers: headers


p JSON.parse(result)


```


```python
import requests
headers = {
  'Accept': '*/*'
}


r = requests.options('//localhost:7080//oauth/confirm_access', params={


}, headers = headers)


print r.json()


```


```java
URL obj = new URL("//localhost:7080//oauth/confirm_access");
HttpURLConnection con = (HttpURLConnection) obj.openConnection();
con.setRequestMethod("OPTIONS");
int responseCode = con.getResponseCode();
BufferedReader in = new BufferedReader(
    new InputStreamReader(con.getInputStream()));
String inputLine;
StringBuffer response = new StringBuffer();
while ((inputLine = in.readLine()) != null) {
    response.append(inputLine);
}
in.close();
System.out.println(response.toString());


```


`OPTIONS /oauth/confirm_access`


*getAccessConfirmation*


<h3 id="getAccessConfirmationUsingOPTIONS-parameters">Parameters</h3>


|Parameter|In|Type|Required|Description|
|---|---|---|---|---|
|model|query|undefined|false|model|


> Example responses


<h3 id="getAccessConfirmationUsingOPTIONS-responses">Responses</h3>


|Status|Meaning|Description|Schema|
|---|---|---|---|
|200|[OK](https://tools.ietf.org/html/rfc7231#section-6.3.1)|OK|[ModelAndView](#schemamodelandview)|
|204|[No Content](https://tools.ietf.org/html/rfc7231#section-6.3.5)|No Content|None|
|401|[Unauthorized](https://tools.ietf.org/html/rfc7235#section-3.1)|Unauthorized|None|
|403|[Forbidden](https://tools.ietf.org/html/rfc7231#section-6.5.3)|Forbidden|None|


<aside class="success">
This operation does not require authentication
</aside>


## getAccessConfirmationUsingPATCH


<a id="opIdgetAccessConfirmationUsingPATCH"></a>


> Code samples


```shell
# You can also use wget
curl -X PATCH //localhost:7080//oauth/confirm_access \
  -H 'Accept: */*'


```


```http
PATCH //localhost:7080//oauth/confirm_access HTTP/1.1
Host: null


Accept: */*


```


```javascript
var headers = {
  'Accept':'*/*'


};


$.ajax({
  url: '//localhost:7080//oauth/confirm_access',
  method: 'patch',


  headers: headers,
  success: function(data) {
    console.log(JSON.stringify(data));
  }
})


```


```javascript--nodejs
const request = require('node-fetch');


const headers = {
  'Accept':'*/*'


};


fetch('//localhost:7080//oauth/confirm_access',
{
  method: 'PATCH',


  headers: headers
})
.then(function(res) {
    return res.json();
}).then(function(body) {
    console.log(body);
});


```


```ruby
require 'rest-client'
require 'json'


headers = {
  'Accept' => '*/*'
}


result = RestClient.patch '//localhost:7080//oauth/confirm_access',
  params: {
  }, headers: headers


p JSON.parse(result)


```


```python
import requests
headers = {
  'Accept': '*/*'
}


r = requests.patch('//localhost:7080//oauth/confirm_access', params={


}, headers = headers)


print r.json()


```


```java
URL obj = new URL("//localhost:7080//oauth/confirm_access");
HttpURLConnection con = (HttpURLConnection) obj.openConnection();
con.setRequestMethod("PATCH");
int responseCode = con.getResponseCode();
BufferedReader in = new BufferedReader(
    new InputStreamReader(con.getInputStream()));
String inputLine;
StringBuffer response = new StringBuffer();
while ((inputLine = in.readLine()) != null) {
    response.append(inputLine);
}
in.close();
System.out.println(response.toString());


```


`PATCH /oauth/confirm_access`


*getAccessConfirmation*


<h3 id="getAccessConfirmationUsingPATCH-parameters">Parameters</h3>


|Parameter|In|Type|Required|Description|
|---|---|---|---|---|
|model|query|undefined|false|model|


> Example responses


<h3 id="getAccessConfirmationUsingPATCH-responses">Responses</h3>


|Status|Meaning|Description|Schema|
|---|---|---|---|
|200|[OK](https://tools.ietf.org/html/rfc7231#section-6.3.1)|OK|[ModelAndView](#schemamodelandview)|
|204|[No Content](https://tools.ietf.org/html/rfc7231#section-6.3.5)|No Content|None|
|401|[Unauthorized](https://tools.ietf.org/html/rfc7235#section-3.1)|Unauthorized|None|
|403|[Forbidden](https://tools.ietf.org/html/rfc7231#section-6.5.3)|Forbidden|None|


<aside class="success">
This operation does not require authentication
</aside>


<h1 id="Public-API-for-appointman-whitelabel-error-endpoint">whitelabel-error-endpoint</h1>


Whitelabel Error Endpoint


## handleErrorUsingGET


<a id="opIdhandleErrorUsingGET"></a>


> Code samples


```shell
# You can also use wget
curl -X GET //localhost:7080//oauth/error \
  -H 'Accept: */*'


```


```http
GET //localhost:7080//oauth/error HTTP/1.1
Host: null


Accept: */*


```


```javascript
var headers = {
  'Accept':'*/*'


};


$.ajax({
  url: '//localhost:7080//oauth/error',
  method: 'get',


  headers: headers,
  success: function(data) {
    console.log(JSON.stringify(data));
  }
})


```


```javascript--nodejs
const request = require('node-fetch');


const headers = {
  'Accept':'*/*'


};


fetch('//localhost:7080//oauth/error',
{
  method: 'GET',


  headers: headers
})
.then(function(res) {
    return res.json();
}).then(function(body) {
    console.log(body);
});


```


```ruby
require 'rest-client'
require 'json'


headers = {
  'Accept' => '*/*'
}


result = RestClient.get '//localhost:7080//oauth/error',
  params: {
  }, headers: headers


p JSON.parse(result)


```


```python
import requests
headers = {
  'Accept': '*/*'
}


r = requests.get('//localhost:7080//oauth/error', params={


}, headers = headers)


print r.json()


```


```java
URL obj = new URL("//localhost:7080//oauth/error");
HttpURLConnection con = (HttpURLConnection) obj.openConnection();
con.setRequestMethod("GET");
int responseCode = con.getResponseCode();
BufferedReader in = new BufferedReader(
    new InputStreamReader(con.getInputStream()));
String inputLine;
StringBuffer response = new StringBuffer();
while ((inputLine = in.readLine()) != null) {
    response.append(inputLine);
}
in.close();
System.out.println(response.toString());


```


`GET /oauth/error`


*handleError*


> Example responses


<h3 id="handleErrorUsingGET-responses">Responses</h3>


|Status|Meaning|Description|Schema|
|---|---|---|---|
|200|[OK](https://tools.ietf.org/html/rfc7231#section-6.3.1)|OK|[ModelAndView](#schemamodelandview)|
|401|[Unauthorized](https://tools.ietf.org/html/rfc7235#section-3.1)|Unauthorized|None|
|403|[Forbidden](https://tools.ietf.org/html/rfc7231#section-6.5.3)|Forbidden|None|
|404|[Not Found](https://tools.ietf.org/html/rfc7231#section-6.5.4)|Not Found|None|


<aside class="success">
This operation does not require authentication
</aside>


## handleErrorUsingHEAD


<a id="opIdhandleErrorUsingHEAD"></a>


> Code samples


```shell
# You can also use wget
curl -X HEAD //localhost:7080//oauth/error \
  -H 'Accept: */*'


```


```http
HEAD //localhost:7080//oauth/error HTTP/1.1
Host: null


Accept: */*


```


```javascript
var headers = {
  'Accept':'*/*'


};


$.ajax({
  url: '//localhost:7080//oauth/error',
  method: 'head',


  headers: headers,
  success: function(data) {
    console.log(JSON.stringify(data));
  }
})


```


```javascript--nodejs
const request = require('node-fetch');


const headers = {
  'Accept':'*/*'


};


fetch('//localhost:7080//oauth/error',
{
  method: 'HEAD',


  headers: headers
})
.then(function(res) {
    return res.json();
}).then(function(body) {
    console.log(body);
});


```


```ruby
require 'rest-client'
require 'json'


headers = {
  'Accept' => '*/*'
}


result = RestClient.head '//localhost:7080//oauth/error',
  params: {
  }, headers: headers


p JSON.parse(result)


```


```python
import requests
headers = {
  'Accept': '*/*'
}


r = requests.head('//localhost:7080//oauth/error', params={


}, headers = headers)


print r.json()


```


```java
URL obj = new URL("//localhost:7080//oauth/error");
HttpURLConnection con = (HttpURLConnection) obj.openConnection();
con.setRequestMethod("HEAD");
int responseCode = con.getResponseCode();
BufferedReader in = new BufferedReader(
    new InputStreamReader(con.getInputStream()));
String inputLine;
StringBuffer response = new StringBuffer();
while ((inputLine = in.readLine()) != null) {
    response.append(inputLine);
}
in.close();
System.out.println(response.toString());


```


`HEAD /oauth/error`


*handleError*


> Example responses


<h3 id="handleErrorUsingHEAD-responses">Responses</h3>


|Status|Meaning|Description|Schema|
|---|---|---|---|
|200|[OK](https://tools.ietf.org/html/rfc7231#section-6.3.1)|OK|[ModelAndView](#schemamodelandview)|
|204|[No Content](https://tools.ietf.org/html/rfc7231#section-6.3.5)|No Content|None|
|401|[Unauthorized](https://tools.ietf.org/html/rfc7235#section-3.1)|Unauthorized|None|
|403|[Forbidden](https://tools.ietf.org/html/rfc7231#section-6.5.3)|Forbidden|None|


<aside class="success">
This operation does not require authentication
</aside>


## handleErrorUsingPOST


<a id="opIdhandleErrorUsingPOST"></a>


> Code samples


```shell
# You can also use wget
curl -X POST //localhost:7080//oauth/error \
  -H 'Accept: */*'


```


```http
POST //localhost:7080//oauth/error HTTP/1.1
Host: null


Accept: */*


```


```javascript
var headers = {
  'Accept':'*/*'


};


$.ajax({
  url: '//localhost:7080//oauth/error',
  method: 'post',


  headers: headers,
  success: function(data) {
    console.log(JSON.stringify(data));
  }
})


```


```javascript--nodejs
const request = require('node-fetch');


const headers = {
  'Accept':'*/*'


};


fetch('//localhost:7080//oauth/error',
{
  method: 'POST',


  headers: headers
})
.then(function(res) {
    return res.json();
}).then(function(body) {
    console.log(body);
});


```


```ruby
require 'rest-client'
require 'json'


headers = {
  'Accept' => '*/*'
}


result = RestClient.post '//localhost:7080//oauth/error',
  params: {
  }, headers: headers


p JSON.parse(result)


```


```python
import requests
headers = {
  'Accept': '*/*'
}


r = requests.post('//localhost:7080//oauth/error', params={


}, headers = headers)


print r.json()


```


```java
URL obj = new URL("//localhost:7080//oauth/error");
HttpURLConnection con = (HttpURLConnection) obj.openConnection();
con.setRequestMethod("POST");
int responseCode = con.getResponseCode();
BufferedReader in = new BufferedReader(
    new InputStreamReader(con.getInputStream()));
String inputLine;
StringBuffer response = new StringBuffer();
while ((inputLine = in.readLine()) != null) {
    response.append(inputLine);
}
in.close();
System.out.println(response.toString());


```


`POST /oauth/error`


*handleError*


> Example responses


<h3 id="handleErrorUsingPOST-responses">Responses</h3>


|Status|Meaning|Description|Schema|
|---|---|---|---|
|200|[OK](https://tools.ietf.org/html/rfc7231#section-6.3.1)|OK|[ModelAndView](#schemamodelandview)|
|201|[Created](https://tools.ietf.org/html/rfc7231#section-6.3.2)|Created|None|
|401|[Unauthorized](https://tools.ietf.org/html/rfc7235#section-3.1)|Unauthorized|None|
|403|[Forbidden](https://tools.ietf.org/html/rfc7231#section-6.5.3)|Forbidden|None|
|404|[Not Found](https://tools.ietf.org/html/rfc7231#section-6.5.4)|Not Found|None|


<aside class="success">
This operation does not require authentication
</aside>


## handleErrorUsingPUT


<a id="opIdhandleErrorUsingPUT"></a>


> Code samples


```shell
# You can also use wget
curl -X PUT //localhost:7080//oauth/error \
  -H 'Accept: */*'


```


```http
PUT //localhost:7080//oauth/error HTTP/1.1
Host: null


Accept: */*


```


```javascript
var headers = {
  'Accept':'*/*'


};


$.ajax({
  url: '//localhost:7080//oauth/error',
  method: 'put',


  headers: headers,
  success: function(data) {
    console.log(JSON.stringify(data));
  }
})


```


```javascript--nodejs
const request = require('node-fetch');


const headers = {
  'Accept':'*/*'


};


fetch('//localhost:7080//oauth/error',
{
  method: 'PUT',


  headers: headers
})
.then(function(res) {
    return res.json();
}).then(function(body) {
    console.log(body);
});


```


```ruby
require 'rest-client'
require 'json'


headers = {
  'Accept' => '*/*'
}


result = RestClient.put '//localhost:7080//oauth/error',
  params: {
  }, headers: headers


p JSON.parse(result)


```


```python
import requests
headers = {
  'Accept': '*/*'
}


r = requests.put('//localhost:7080//oauth/error', params={


}, headers = headers)


print r.json()


```


```java
URL obj = new URL("//localhost:7080//oauth/error");
HttpURLConnection con = (HttpURLConnection) obj.openConnection();
con.setRequestMethod("PUT");
int responseCode = con.getResponseCode();
BufferedReader in = new BufferedReader(
    new InputStreamReader(con.getInputStream()));
String inputLine;
StringBuffer response = new StringBuffer();
while ((inputLine = in.readLine()) != null) {
    response.append(inputLine);
}
in.close();
System.out.println(response.toString());


```


`PUT /oauth/error`


*handleError*


> Example responses


<h3 id="handleErrorUsingPUT-responses">Responses</h3>


|Status|Meaning|Description|Schema|
|---|---|---|---|
|200|[OK](https://tools.ietf.org/html/rfc7231#section-6.3.1)|OK|[ModelAndView](#schemamodelandview)|
|201|[Created](https://tools.ietf.org/html/rfc7231#section-6.3.2)|Created|None|
|401|[Unauthorized](https://tools.ietf.org/html/rfc7235#section-3.1)|Unauthorized|None|
|403|[Forbidden](https://tools.ietf.org/html/rfc7231#section-6.5.3)|Forbidden|None|
|404|[Not Found](https://tools.ietf.org/html/rfc7231#section-6.5.4)|Not Found|None|


<aside class="success">
This operation does not require authentication
</aside>


## handleErrorUsingDELETE


<a id="opIdhandleErrorUsingDELETE"></a>


> Code samples


```shell
# You can also use wget
curl -X DELETE //localhost:7080//oauth/error \
  -H 'Accept: */*'


```


```http
DELETE //localhost:7080//oauth/error HTTP/1.1
Host: null


Accept: */*


```


```javascript
var headers = {
  'Accept':'*/*'


};


$.ajax({
  url: '//localhost:7080//oauth/error',
  method: 'delete',


  headers: headers,
  success: function(data) {
    console.log(JSON.stringify(data));
  }
})


```


```javascript--nodejs
const request = require('node-fetch');


const headers = {
  'Accept':'*/*'


};


fetch('//localhost:7080//oauth/error',
{
  method: 'DELETE',


  headers: headers
})
.then(function(res) {
    return res.json();
}).then(function(body) {
    console.log(body);
});


```


```ruby
require 'rest-client'
require 'json'


headers = {
  'Accept' => '*/*'
}


result = RestClient.delete '//localhost:7080//oauth/error',
  params: {
  }, headers: headers


p JSON.parse(result)


```


```python
import requests
headers = {
  'Accept': '*/*'
}


r = requests.delete('//localhost:7080//oauth/error', params={


}, headers = headers)


print r.json()


```


```java
URL obj = new URL("//localhost:7080//oauth/error");
HttpURLConnection con = (HttpURLConnection) obj.openConnection();
con.setRequestMethod("DELETE");
int responseCode = con.getResponseCode();
BufferedReader in = new BufferedReader(
    new InputStreamReader(con.getInputStream()));
String inputLine;
StringBuffer response = new StringBuffer();
while ((inputLine = in.readLine()) != null) {
    response.append(inputLine);
}
in.close();
System.out.println(response.toString());


```


`DELETE /oauth/error`


*handleError*


> Example responses


<h3 id="handleErrorUsingDELETE-responses">Responses</h3>


|Status|Meaning|Description|Schema|
|---|---|---|---|
|200|[OK](https://tools.ietf.org/html/rfc7231#section-6.3.1)|OK|[ModelAndView](#schemamodelandview)|
|204|[No Content](https://tools.ietf.org/html/rfc7231#section-6.3.5)|No Content|None|
|401|[Unauthorized](https://tools.ietf.org/html/rfc7235#section-3.1)|Unauthorized|None|
|403|[Forbidden](https://tools.ietf.org/html/rfc7231#section-6.5.3)|Forbidden|None|


<aside class="success">
This operation does not require authentication
</aside>


## handleErrorUsingOPTIONS


<a id="opIdhandleErrorUsingOPTIONS"></a>


> Code samples


```shell
# You can also use wget
curl -X OPTIONS //localhost:7080//oauth/error \
  -H 'Accept: */*'


```


```http
OPTIONS //localhost:7080//oauth/error HTTP/1.1
Host: null


Accept: */*


```


```javascript
var headers = {
  'Accept':'*/*'


};


$.ajax({
  url: '//localhost:7080//oauth/error',
  method: 'options',


  headers: headers,
  success: function(data) {
    console.log(JSON.stringify(data));
  }
})


```


```javascript--nodejs
const request = require('node-fetch');


const headers = {
  'Accept':'*/*'


};


fetch('//localhost:7080//oauth/error',
{
  method: 'OPTIONS',


  headers: headers
})
.then(function(res) {
    return res.json();
}).then(function(body) {
    console.log(body);
});


```


```ruby
require 'rest-client'
require 'json'


headers = {
  'Accept' => '*/*'
}


result = RestClient.options '//localhost:7080//oauth/error',
  params: {
  }, headers: headers


p JSON.parse(result)


```


```python
import requests
headers = {
  'Accept': '*/*'
}


r = requests.options('//localhost:7080//oauth/error', params={


}, headers = headers)


print r.json()


```


```java
URL obj = new URL("//localhost:7080//oauth/error");
HttpURLConnection con = (HttpURLConnection) obj.openConnection();
con.setRequestMethod("OPTIONS");
int responseCode = con.getResponseCode();
BufferedReader in = new BufferedReader(
    new InputStreamReader(con.getInputStream()));
String inputLine;
StringBuffer response = new StringBuffer();
while ((inputLine = in.readLine()) != null) {
    response.append(inputLine);
}
in.close();
System.out.println(response.toString());


```


`OPTIONS /oauth/error`


*handleError*


> Example responses


<h3 id="handleErrorUsingOPTIONS-responses">Responses</h3>


|Status|Meaning|Description|Schema|
|---|---|---|---|
|200|[OK](https://tools.ietf.org/html/rfc7231#section-6.3.1)|OK|[ModelAndView](#schemamodelandview)|
|204|[No Content](https://tools.ietf.org/html/rfc7231#section-6.3.5)|No Content|None|
|401|[Unauthorized](https://tools.ietf.org/html/rfc7235#section-3.1)|Unauthorized|None|
|403|[Forbidden](https://tools.ietf.org/html/rfc7231#section-6.5.3)|Forbidden|None|


<aside class="success">
This operation does not require authentication
</aside>


## handleErrorUsingPATCH


<a id="opIdhandleErrorUsingPATCH"></a>


> Code samples


```shell
# You can also use wget
curl -X PATCH //localhost:7080//oauth/error \
  -H 'Accept: */*'


```


```http
PATCH //localhost:7080//oauth/error HTTP/1.1
Host: null


Accept: */*


```


```javascript
var headers = {
  'Accept':'*/*'


};


$.ajax({
  url: '//localhost:7080//oauth/error',
  method: 'patch',


  headers: headers,
  success: function(data) {
    console.log(JSON.stringify(data));
  }
})


```


```javascript--nodejs
const request = require('node-fetch');


const headers = {
  'Accept':'*/*'


};


fetch('//localhost:7080//oauth/error',
{
  method: 'PATCH',


  headers: headers
})
.then(function(res) {
    return res.json();
}).then(function(body) {
    console.log(body);
});


```


```ruby
require 'rest-client'
require 'json'


headers = {
  'Accept' => '*/*'
}


result = RestClient.patch '//localhost:7080//oauth/error',
  params: {
  }, headers: headers


p JSON.parse(result)


```


```python
import requests
headers = {
  'Accept': '*/*'
}


r = requests.patch('//localhost:7080//oauth/error', params={


}, headers = headers)


print r.json()


```


```java
URL obj = new URL("//localhost:7080//oauth/error");
HttpURLConnection con = (HttpURLConnection) obj.openConnection();
con.setRequestMethod("PATCH");
int responseCode = con.getResponseCode();
BufferedReader in = new BufferedReader(
    new InputStreamReader(con.getInputStream()));
String inputLine;
StringBuffer response = new StringBuffer();
while ((inputLine = in.readLine()) != null) {
    response.append(inputLine);
}
in.close();
System.out.println(response.toString());


```


`PATCH /oauth/error`


*handleError*


> Example responses


<h3 id="handleErrorUsingPATCH-responses">Responses</h3>


|Status|Meaning|Description|Schema|
|---|---|---|---|
|200|[OK](https://tools.ietf.org/html/rfc7231#section-6.3.1)|OK|[ModelAndView](#schemamodelandview)|
|204|[No Content](https://tools.ietf.org/html/rfc7231#section-6.3.5)|No Content|None|
|401|[Unauthorized](https://tools.ietf.org/html/rfc7235#section-3.1)|Unauthorized|None|
|403|[Forbidden](https://tools.ietf.org/html/rfc7231#section-6.5.3)|Forbidden|None|


<aside class="success">
This operation does not require authentication
</aside>


<h1 id="Public-API-for-appointman-token-endpoint">token-endpoint</h1>


Token Endpoint


## getAccessTokenUsingGET


<a id="opIdgetAccessTokenUsingGET"></a>


> Code samples


```shell
# You can also use wget
curl -X GET //localhost:7080//oauth/token?parameters=string \
  -H 'Accept: */*'


```


```http
GET //localhost:7080//oauth/token?parameters=string HTTP/1.1
Host: null


Accept: */*


```


```javascript
var headers = {
  'Accept':'*/*'


};


$.ajax({
  url: '//localhost:7080//oauth/token',
  method: 'get',
  data: '?parameters=string',
  headers: headers,
  success: function(data) {
    console.log(JSON.stringify(data));
  }
})


```


```javascript--nodejs
const request = require('node-fetch');


const headers = {
  'Accept':'*/*'


};


fetch('//localhost:7080//oauth/token?parameters=string',
{
  method: 'GET',


  headers: headers
})
.then(function(res) {
    return res.json();
}).then(function(body) {
    console.log(body);
});


```


```ruby
require 'rest-client'
require 'json'


headers = {
  'Accept' => '*/*'
}


result = RestClient.get '//localhost:7080//oauth/token',
  params: {
  'parameters' => 'string'
}, headers: headers


p JSON.parse(result)


```


```python
import requests
headers = {
  'Accept': '*/*'
}


r = requests.get('//localhost:7080//oauth/token', params={
  'parameters': 'string'
}, headers = headers)


print r.json()


```


```java
URL obj = new URL("//localhost:7080//oauth/token?parameters=string");
HttpURLConnection con = (HttpURLConnection) obj.openConnection();
con.setRequestMethod("GET");
int responseCode = con.getResponseCode();
BufferedReader in = new BufferedReader(
    new InputStreamReader(con.getInputStream()));
String inputLine;
StringBuffer response = new StringBuffer();
while ((inputLine = in.readLine()) != null) {
    response.append(inputLine);
}
in.close();
System.out.println(response.toString());


```


`GET /oauth/token`


*getAccessToken*


<h3 id="getAccessTokenUsingGET-parameters">Parameters</h3>


|Parameter|In|Type|Required|Description|
|---|---|---|---|---|
|parameters|query|string|true|parameters|


> Example responses


<h3 id="getAccessTokenUsingGET-responses">Responses</h3>


|Status|Meaning|Description|Schema|
|---|---|---|---|
|200|[OK](https://tools.ietf.org/html/rfc7231#section-6.3.1)|OK|[OAuth2AccessToken](#schemaoauth2accesstoken)|
|401|[Unauthorized](https://tools.ietf.org/html/rfc7235#section-3.1)|Unauthorized|None|
|403|[Forbidden](https://tools.ietf.org/html/rfc7231#section-6.5.3)|Forbidden|None|
|404|[Not Found](https://tools.ietf.org/html/rfc7231#section-6.5.4)|Not Found|None|


<aside class="success">
This operation does not require authentication
</aside>


## postAccessTokenUsingPOST


<a id="opIdpostAccessTokenUsingPOST"></a>


> Code samples


```shell
# You can also use wget
curl -X POST //localhost:7080//oauth/token?parameters=string \
  -H 'Accept: */*'


```


```http
POST //localhost:7080//oauth/token?parameters=string HTTP/1.1
Host: null


Accept: */*


```


```javascript
var headers = {
  'Accept':'*/*'


};


$.ajax({
  url: '//localhost:7080//oauth/token',
  method: 'post',
  data: '?parameters=string',
  headers: headers,
  success: function(data) {
    console.log(JSON.stringify(data));
  }
})


```


```javascript--nodejs
const request = require('node-fetch');


const headers = {
  'Accept':'*/*'


};


fetch('//localhost:7080//oauth/token?parameters=string',
{
  method: 'POST',


  headers: headers
})
.then(function(res) {
    return res.json();
}).then(function(body) {
    console.log(body);
});


```


```ruby
require 'rest-client'
require 'json'


headers = {
  'Accept' => '*/*'
}


result = RestClient.post '//localhost:7080//oauth/token',
  params: {
  'parameters' => 'string'
}, headers: headers


p JSON.parse(result)


```


```python
import requests
headers = {
  'Accept': '*/*'
}


r = requests.post('//localhost:7080//oauth/token', params={
  'parameters': 'string'
}, headers = headers)


print r.json()


```


```java
URL obj = new URL("//localhost:7080//oauth/token?parameters=string");
HttpURLConnection con = (HttpURLConnection) obj.openConnection();
con.setRequestMethod("POST");
int responseCode = con.getResponseCode();
BufferedReader in = new BufferedReader(
    new InputStreamReader(con.getInputStream()));
String inputLine;
StringBuffer response = new StringBuffer();
while ((inputLine = in.readLine()) != null) {
    response.append(inputLine);
}
in.close();
System.out.println(response.toString());


```


`POST /oauth/token`


*postAccessToken*


<h3 id="postAccessTokenUsingPOST-parameters">Parameters</h3>


|Parameter|In|Type|Required|Description|
|---|---|---|---|---|
|parameters|query|string|true|parameters|


> Example responses


<h3 id="postAccessTokenUsingPOST-responses">Responses</h3>


|Status|Meaning|Description|Schema|
|---|---|---|---|
|200|[OK](https://tools.ietf.org/html/rfc7231#section-6.3.1)|OK|[OAuth2AccessToken](#schemaoauth2accesstoken)|
|201|[Created](https://tools.ietf.org/html/rfc7231#section-6.3.2)|Created|None|
|401|[Unauthorized](https://tools.ietf.org/html/rfc7235#section-3.1)|Unauthorized|None|
|403|[Forbidden](https://tools.ietf.org/html/rfc7231#section-6.5.3)|Forbidden|None|
|404|[Not Found](https://tools.ietf.org/html/rfc7231#section-6.5.4)|Not Found|None|


<aside class="success">
This operation does not require authentication
</aside>


# Schemas


<h2 id="tocScontract">Contract</h2>


<a id="schemacontract"></a>


```json
{
  "contractEnd": 0,
  "contractNumber": "string",
  "contractStart": 0,
  "id": "string",
  "maxBookingsInFuture": 0,
  "maxBookingsPerDay": 0,
  "notes": "string",
  "terminated": true,
  "type": "string"
}
```


### Properties


|Name|Type|Required|Description|
|---|---|---|---|
|contractEnd|integer(int64)|false|No description|
|contractNumber|string|false|No description|
|contractStart|integer(int64)|false|No description|
|id|string|false|No description|
|maxBookingsInFuture|integer(int64)|false|No description|
|maxBookingsPerDay|integer(int64)|false|No description|
|notes|string|false|No description|
|terminated|boolean|false|No description|
|type|string|false|No description|


<h2 id="tocScustomer">Customer</h2>


<a id="schemacustomer"></a>


```json
{
  "id": "string",
  "title": "string",
  "firstname": "string",
  "lastname": "string",
  "email": "string",
  "birthday": 0,
  "phone": "string",
  "mobile": "string",
  "address": "string",
  "notes": "string"
}
```


### Properties


|Name|Type|Required|Description|
|---|---|---|---|
|id|string|false|Unique id of the customer|
|title|string|false|Title like Dr.|
|firstname|string|false|The firstname of the customer|
|lastname|string|false|The lastname of the customer|
|email|string|false|The email address of the customer|
|birthday|integer(int64)|false|The birthday of the customer (timestamp in ms)|
|phone|string|false|The phone number of the customer|
|mobile|string|false|The mobile phone number of the customer|
|address|string|false|The private address of the customer|
|notes|string|false|Some notes about the customer|


<h2 id="tocSgroup">Group</h2>


<a id="schemagroup"></a>


```json
{
  "name": "string"
}
```


### Properties


|Name|Type|Required|Description|
|---|---|---|---|
|name|string|false|No description|


<h2 id="tocSlesson">Lesson</h2>


<a id="schemalesson"></a>


```json
{
  "cancelMessage": "string",
  "canceled": true,
  "courseId": "string",
  "date": 0,
  "description": "string",
  "id": "string",
  "name": "string",
  "participants": [
    {
      "contractId": "string",
      "lead": true,
      "leadId": "string",
      "name": "string",
      "ticketId": "string"
    }
  ]
}
```


### Properties


|Name|Type|Required|Description|
|---|---|---|---|
|cancelMessage|string|false|No description|
|canceled|boolean|false|No description|
|courseId|string|false|No description|
|date|integer(int64)|false|No description|
|description|string|false|No description|
|id|string|false|No description|
|name|string|false|No description|
|participants|[[Participant](#schemaparticipant)]|false|No description|


<h2 id="tocSmodelandview">ModelAndView</h2>


<a id="schemamodelandview"></a>


```json
{
  "empty": true,
  "model": {},
  "modelMap": {
    "property1": {},
    "property2": {}
  },
  "reference": true,
  "status": "100",
  "view": {
    "contentType": "string"
  },
  "viewName": "string"
}
```


### Properties


|Name|Type|Required|Description|
|---|---|---|---|
|empty|boolean|false|No description|
|model|object|false|No description|
|modelMap|object|false|No description|
|» **additionalProperties**|object|false|No description|
|reference|boolean|false|No description|
|status|string|false|No description|
|view|[View](#schemaview)|false|No description|
|viewName|string|false|No description|


#### Enumerated Values


|Property|Value|
|---|---|
|status|100|
|status|101|
|status|102|
|status|103|
|status|200|
|status|201|
|status|202|
|status|203|
|status|204|
|status|205|
|status|206|
|status|207|
|status|208|
|status|226|
|status|300|
|status|301|
|status|302|
|status|303|
|status|304|
|status|305|
|status|307|
|status|308|
|status|400|
|status|401|
|status|402|
|status|403|
|status|404|
|status|405|
|status|406|
|status|407|
|status|408|
|status|409|
|status|410|
|status|411|
|status|412|
|status|413|
|status|414|
|status|415|
|status|416|
|status|417|
|status|418|
|status|419|
|status|420|
|status|421|
|status|422|
|status|423|
|status|424|
|status|426|
|status|428|
|status|429|
|status|431|
|status|451|
|status|500|
|status|501|
|status|502|
|status|503|
|status|504|
|status|505|
|status|506|
|status|507|
|status|508|
|status|509|
|status|510|
|status|511|


<h2 id="tocSoauth2accesstoken">OAuth2AccessToken</h2>


<a id="schemaoauth2accesstoken"></a>


```json
{
  "additionalInformation": {},
  "expiration": "2018-02-15T22:31:59Z",
  "expired": true,
  "expiresIn": 0,
  "refreshToken": {
    "value": "string"
  },
  "scope": [
    "string"
  ],
  "tokenType": "string",
  "value": "string"
}
```


### Properties


|Name|Type|Required|Description|
|---|---|---|---|
|additionalInformation|object|false|No description|
|expiration|string(date-time)|false|No description|
|expired|boolean|false|No description|
|expiresIn|integer(int32)|false|No description|
|refreshToken|[OAuth2RefreshToken](#schemaoauth2refreshtoken)|false|No description|
|scope|[string]|false|No description|
|tokenType|string|false|No description|
|value|string|false|No description|


<h2 id="tocSoauth2refreshtoken">OAuth2RefreshToken</h2>


<a id="schemaoauth2refreshtoken"></a>


```json
{
  "value": "string"
}
```


### Properties


|Name|Type|Required|Description|
|---|---|---|---|
|value|string|false|No description|


<h2 id="tocSparticipant">Participant</h2>


<a id="schemaparticipant"></a>


```json
{
  "contractId": "string",
  "lead": true,
  "leadId": "string",
  "name": "string",
  "ticketId": "string"
}
```


### Properties


|Name|Type|Required|Description|
|---|---|---|---|
|contractId|string|false|No description|
|lead|boolean|false|No description|
|leadId|string|false|No description|
|name|string|false|No description|
|ticketId|string|false|No description|


<h2 id="tocSview">View</h2>


<a id="schemaview"></a>


```json
{
  "contentType": "string"
}
```


### Properties


|Name|Type|Required|Description|
|---|---|---|---|
|contentType|string|false|No description|


