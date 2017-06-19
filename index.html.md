---
title: API v0.0.1
language_tabs:
  - shell: Shell
  - http: HTTP
  - javascript: JavaScript
  - javascript--nodejs: Node.JS
  - python: Python
  - ruby: Ruby
  - java: Java
toc_footers: []
includes: []
search: true
highlight_theme: darkula
---

# API v0.0.1

> Scroll down for code samples, example requests and responses. Select a language for code samples from the tabs above or the mobile navigation menu.

The Whiplash V2 API.

Base URL = <a href="://staging.whiplashmerch.com/">://staging.whiplashmerch.com/</a>

Email: <a href="mailto:developers@getwhiplash.com">Whiplash Development Team</a>Web: <a href="https://www.getwhiplash.com">Whiplash Development Team</a>

# Authentication



- oAuth2 authentication. 
    - Flow: implicit
    - Authorization URL = [/oauth/token](/oauth/token)

|Scope|Scope Description|
|---|---|
|user_read|read user information, default scope if none is provided|
|user_manage| modify user information|
|app_read|read application information|
|app_manage|read application information|
|app_create_user|create users for the application|



# orders

Operations about orders

## getApiV2OrdersIdOriginator

> Code samples

```shell
# You can also use wget
curl -X get ://staging.whiplashmerch.com/api/v2/orders/{id}/originator \
  -H 'Accept: application/json'

```

```http
GET ://staging.whiplashmerch.com/api/v2/orders/{id}/originator HTTP/1.1
Host: staging.whiplashmerch.com

Accept: application/json

```

```javascript
var headers = {
  'Accept':'application/json'

};

$.ajax({
  url: '://staging.whiplashmerch.com/api/v2/orders/{id}/originator',
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
  'Accept':'application/json'

};

fetch('://staging.whiplashmerch.com/api/v2/orders/{id}/originator',
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
  'Accept' => 'application/json'
}

result = RestClient.get '://staging.whiplashmerch.com/api/v2/orders/{id}/originator', params: {
  }, headers: headers

p JSON.parse(result)
```

```python
import requests
headers = {
  'Accept': 'application/json'
}

r = requests.get('://staging.whiplashmerch.com/api/v2/orders/{id}/originator', params={

}, headers = headers)

print r.json()
```

```java
URL obj = new URL("://staging.whiplashmerch.com/api/v2/orders/{id}/originator");
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

`GET /api/v2/orders/{id}/originator`

*Get the originator for a(n) Order*

Get the originator for a(n) Order

### Parameters

Parameter|In|Type|Required|Description
---|---|---|---|---|
id|path|integer|true|No description


### Responses

Status|Meaning|Description
---|---|---|
200|[OK](https://tools.ietf.org/html/rfc7231#section-6.3.1)|Get the originator for a(n) Order
401|[Unauthorized](https://tools.ietf.org/html/rfc7235#section-3.1)|No description
403|[Forbidden](https://tools.ietf.org/html/rfc7231#section-6.5.3)|No description

> Example responses

```json
{
  "id": 0,
  "originated_id": 0,
  "originated_type": "string",
  "shop_id": 0,
  "provider": "string",
  "original_id": "string",
  "group_id": "string",
  "address_id": "string",
  "active": true,
  "integration_id": 0,
  "last_notified_at": "2017-06-19T15:15:48Z",
  "last_notification_status": "string",
  "distinct_originator_key": "string",
  "created_at": "2017-06-19T15:15:48Z",
  "updated_at": "2017-06-19T15:15:48Z"
}
```
```json
{
  "message": "string"
}
```
```json
{
  "message": "string"
}
```
<aside class="success">
This operation does not require authentication
</aside>

## getApiV2OrdersId

> Code samples

```shell
# You can also use wget
curl -X get ://staging.whiplashmerch.com/api/v2/orders/{id} \
  -H 'X-Customer-Id: string' \
  -H 'X-Shop-Id: string' \
  -H 'Accept: application/json'

```

```http
GET ://staging.whiplashmerch.com/api/v2/orders/{id} HTTP/1.1
Host: staging.whiplashmerch.com

Accept: application/json
X-Customer-Id: string
X-Shop-Id: string

```

```javascript
var headers = {
  'X-Customer-Id':'string',
  'X-Shop-Id':'string',
  'Accept':'application/json'

};

$.ajax({
  url: '://staging.whiplashmerch.com/api/v2/orders/{id}',
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
  'X-Customer-Id':'string',
  'X-Shop-Id':'string',
  'Accept':'application/json'

};

fetch('://staging.whiplashmerch.com/api/v2/orders/{id}',
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
  'X-Customer-Id' => 'string',
  'X-Shop-Id' => 'string',
  'Accept' => 'application/json'
}

result = RestClient.get '://staging.whiplashmerch.com/api/v2/orders/{id}', params: {
  }, headers: headers

p JSON.parse(result)
```

```python
import requests
headers = {
  'X-Customer-Id': 'string',
  'X-Shop-Id': 'string',
  'Accept': 'application/json'
}

r = requests.get('://staging.whiplashmerch.com/api/v2/orders/{id}', params={

}, headers = headers)

print r.json()
```

```java
URL obj = new URL("://staging.whiplashmerch.com/api/v2/orders/{id}");
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

`GET /api/v2/orders/{id}`

*Get an order*

Get an order

### Parameters

Parameter|In|Type|Required|Description
---|---|---|---|---|
id|path|integer|true|No description
X-Customer-Id|header|string|false|The customer associated with this resource.
X-Shop-Id|header|string|false|The shop associated with this resource.


### Responses

Status|Meaning|Description
---|---|---|
200|[OK](https://tools.ietf.org/html/rfc7231#section-6.3.1)|Get an order
401|[Unauthorized](https://tools.ietf.org/html/rfc7235#section-3.1)|No description
403|[Forbidden](https://tools.ietf.org/html/rfc7231#section-6.5.3)|No description

> Example responses

```json
{
  "id": 0,
  "customer_id": 0,
  "first_name": "string",
  "last_name": "string",
  "full_name": "string",
  "billing_company": "string",
  "billing_address_1": "string",
  "billing_address_2": "string",
  "billing_city": "string",
  "billing_state": "string",
  "billing_zip": "string",
  "billing_country": "string",
  "billing_phone": "string",
  "shipping_company": "string",
  "shipping_address_1": "string",
  "shipping_address_2": "string",
  "shipping_city": "string",
  "shipping_state": "string",
  "shipping_zip": "string",
  "shipping_country": "string",
  "shipping_phone": "string",
  "email": "string",
  "ship_actual_cost": 0,
  "shipped_on": "2017-06-19T15:15:48Z",
  "ship_notes": "string",
  "created_at": "2017-06-19T15:15:48Z",
  "updated_at": "2017-06-19T15:15:48Z",
  "shipping_name": "string",
  "shop_shipping_method_price": 0,
  "shipping_confirmation_sent": true,
  "status": 0,
  "previous_status": 0,
  "ship_3rdparty_cost": 0,
  "public_note": "string",
  "gift": true,
  "billed": true,
  "ship_3rdparty_account": "string",
  "ship_3rdparty_zip": "string",
  "ship_3rdparty_country": "string",
  "shop_shipping_method_text": "string",
  "order_batch_id": 0,
  "order_orig": "string",
  "days_in_transit": 0,
  "quote_id": 0,
  "shipping_country_iso2": "string",
  "insure": true,
  "require_signature": true,
  "req_insurance_value": 0,
  "warehouse_id": 0,
  "workable_at": "2017-06-19T15:15:48Z",
  "requested_address": "string",
  "address_verified": true,
  "address_message": "string",
  "return_city": "string",
  "return_state": "string",
  "return_country": "string",
  "return_zip": "string",
  "return_address_1": "string",
  "return_address_2": "string",
  "return_phone": "string",
  "return_email": "string",
  "level1_token": "string",
  "level2_token": "string",
  "return_time_limit": 0,
  "return_address_verified": true,
  "shipping_method_id": 0,
  "skip_street_date": true,
  "shop_warehouse_id": 0,
  "shop_shipping_method_currency": "string",
  "saturday_delivery": true,
  "shop_created_at": "2017-06-19T15:15:48Z",
  "shop_updated_at": "2017-06-19T15:15:48Z",
  "residential": true,
  "skip_address_verification": true,
  "due_at": "2017-06-19T15:15:48Z",
  "do_not_bill": true,
  "return_company": "string",
  "contains_alcohol": true,
  "require_adult_signature": true,
  "order_items": {
    "id": 0,
    "order_id": 0,
    "sku": "string",
    "description": "string",
    "quantity": 0,
    "price": 0,
    "created_at": "2017-06-19T15:15:48Z",
    "updated_at": "2017-06-19T15:15:48Z",
    "unshippable": true,
    "customer_id": 0,
    "item_id": 0,
    "available": true,
    "packed": 0,
    "packaging": true,
    "wholesale_cost": 0,
    "package_id": 0,
    "is_bundle": true,
    "retail_fee": 0,
    "promo": true,
    "quote_item_id": 0,
    "returnable": true,
    "currency": "string",
    "wholesale_fee": 0
  },
  "ship_method": "string",
  "status_name": "string"
}
```
```json
{
  "message": "string"
}
```
```json
{
  "message": "string"
}
```
<aside class="success">
This operation does not require authentication
</aside>

## putApiV2OrdersId

> Code samples

```shell
# You can also use wget
curl -X put ://staging.whiplashmerch.com/api/v2/orders/{id} \
  -H 'X-Customer-Id: string' \
  -H 'X-Shop-Id: string' \
  -H 'Content-Type: application/json' \
  -H 'Accept: application/json'

```

```http
PUT ://staging.whiplashmerch.com/api/v2/orders/{id} HTTP/1.1
Host: staging.whiplashmerch.com
Content-Type: application/json
Accept: application/json
X-Customer-Id: string
X-Shop-Id: string

```

```javascript
var headers = {
  'X-Customer-Id':'string',
  'X-Shop-Id':'string',
  'Content-Type':'application/json',
  'Accept':'application/json'

};

$.ajax({
  url: '://staging.whiplashmerch.com/api/v2/orders/{id}',
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
  'X-Customer-Id':'string',
  'X-Shop-Id':'string',
  'Content-Type':'application/json',
  'Accept':'application/json'

};

fetch('://staging.whiplashmerch.com/api/v2/orders/{id}',
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
  'X-Customer-Id' => 'string',
  'X-Shop-Id' => 'string',
  'Content-Type' => 'application/json',
  'Accept' => 'application/json'
}

result = RestClient.put '://staging.whiplashmerch.com/api/v2/orders/{id}', params: {
  }, headers: headers

p JSON.parse(result)
```

```python
import requests
headers = {
  'X-Customer-Id': 'string',
  'X-Shop-Id': 'string',
  'Content-Type': 'application/json',
  'Accept': 'application/json'
}

r = requests.put('://staging.whiplashmerch.com/api/v2/orders/{id}', params={

}, headers = headers)

print r.json()
```

```java
URL obj = new URL("://staging.whiplashmerch.com/api/v2/orders/{id}");
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

`PUT /api/v2/orders/{id}`

*Update an order*

Update an order

### Parameters

Parameter|In|Type|Required|Description
---|---|---|---|---|
X-Customer-Id|header|string|false|The customer associated with this resource.
X-Shop-Id|header|string|false|The shop associated with this resource.
first_name|formData|string|false|No description
last_name|formData|string|false|No description
full_name|formData|string|false|No description
billing_company|formData|string|false|No description
billing_address_1|formData|string|false|No description
billing_address_2|formData|string|false|No description
billing_city|formData|string|false|No description
billing_state|formData|string|false|No description
billing_zip|formData|string|false|No description
billing_country|formData|string|false|No description
billing_phone|formData|string|false|No description
shipping_company|formData|string|false|No description
shipping_address_1|formData|string|false|No description
shipping_address_2|formData|string|false|No description
shipping_city|formData|string|false|No description
shipping_state|formData|string|false|No description
shipping_zip|formData|string|false|No description
shipping_country|formData|string|false|No description
shipping_phone|formData|string|false|No description
email|formData|string|false|No description
ship_notes|formData|string|false|No description
shipping_name|formData|string|false|No description
shop_shipping_method_price|formData|number|false|No description
ship_3rdparty_cost|formData|number|false|No description
public_note|formData|string|false|No description
gift|formData|boolean|false|No description
ship_3rdparty_account|formData|string|false|No description
ship_3rdparty_zip|formData|string|false|No description
ship_3rdparty_country|formData|string|false|No description
shop_shipping_method_text|formData|string|false|No description
order_orig|formData|string|false|No description
days_in_transit|formData|integer|false|No description
shipping_country_iso2|formData|string|false|No description
insure|formData|boolean|false|No description
require_signature|formData|boolean|false|No description
req_insurance_value|formData|number|false|No description
requested_address|formData|string|false|No description
return_city|formData|string|false|No description
return_state|formData|string|false|No description
return_country|formData|string|false|No description
return_zip|formData|string|false|No description
return_address_1|formData|string|false|No description
return_address_2|formData|string|false|No description
return_phone|formData|string|false|No description
return_email|formData|string|false|No description
level1_token|formData|string|false|No description
level2_token|formData|string|false|No description
return_time_limit|formData|integer|false|No description
shipping_method_id|formData|integer|false|No description
skip_street_date|formData|boolean|false|No description
shop_warehouse_id|formData|integer|false|No description
shop_shipping_method_currency|formData|string|false|No description
saturday_delivery|formData|boolean|false|No description
shop_created_at|formData|string|false|No description
shop_updated_at|formData|string|false|No description
residential|formData|boolean|false|No description
skip_address_verification|formData|boolean|false|No description
due_at|formData|string|false|No description
do_not_bill|formData|boolean|false|No description
return_company|formData|string|false|No description
contains_alcohol|formData|boolean|false|No description
require_adult_signature|formData|boolean|false|No description
id|path|integer|true|No description


### Responses

Status|Meaning|Description
---|---|---|
200|[OK](https://tools.ietf.org/html/rfc7231#section-6.3.1)|Update an order
401|[Unauthorized](https://tools.ietf.org/html/rfc7235#section-3.1)|No description
403|[Forbidden](https://tools.ietf.org/html/rfc7231#section-6.5.3)|No description
422|[Unprocessable Entity](https://tools.ietf.org/html/rfc2518#section-10.3)|No description

> Example responses

```json
{
  "id": 0,
  "customer_id": 0,
  "first_name": "string",
  "last_name": "string",
  "full_name": "string",
  "billing_company": "string",
  "billing_address_1": "string",
  "billing_address_2": "string",
  "billing_city": "string",
  "billing_state": "string",
  "billing_zip": "string",
  "billing_country": "string",
  "billing_phone": "string",
  "shipping_company": "string",
  "shipping_address_1": "string",
  "shipping_address_2": "string",
  "shipping_city": "string",
  "shipping_state": "string",
  "shipping_zip": "string",
  "shipping_country": "string",
  "shipping_phone": "string",
  "email": "string",
  "ship_actual_cost": 0,
  "shipped_on": "2017-06-19T15:15:48Z",
  "ship_notes": "string",
  "created_at": "2017-06-19T15:15:48Z",
  "updated_at": "2017-06-19T15:15:48Z",
  "shipping_name": "string",
  "shop_shipping_method_price": 0,
  "shipping_confirmation_sent": true,
  "status": 0,
  "previous_status": 0,
  "ship_3rdparty_cost": 0,
  "public_note": "string",
  "gift": true,
  "billed": true,
  "ship_3rdparty_account": "string",
  "ship_3rdparty_zip": "string",
  "ship_3rdparty_country": "string",
  "shop_shipping_method_text": "string",
  "order_batch_id": 0,
  "order_orig": "string",
  "days_in_transit": 0,
  "quote_id": 0,
  "shipping_country_iso2": "string",
  "insure": true,
  "require_signature": true,
  "req_insurance_value": 0,
  "warehouse_id": 0,
  "workable_at": "2017-06-19T15:15:48Z",
  "requested_address": "string",
  "address_verified": true,
  "address_message": "string",
  "return_city": "string",
  "return_state": "string",
  "return_country": "string",
  "return_zip": "string",
  "return_address_1": "string",
  "return_address_2": "string",
  "return_phone": "string",
  "return_email": "string",
  "level1_token": "string",
  "level2_token": "string",
  "return_time_limit": 0,
  "return_address_verified": true,
  "shipping_method_id": 0,
  "skip_street_date": true,
  "shop_warehouse_id": 0,
  "shop_shipping_method_currency": "string",
  "saturday_delivery": true,
  "shop_created_at": "2017-06-19T15:15:48Z",
  "shop_updated_at": "2017-06-19T15:15:48Z",
  "residential": true,
  "skip_address_verification": true,
  "due_at": "2017-06-19T15:15:48Z",
  "do_not_bill": true,
  "return_company": "string",
  "contains_alcohol": true,
  "require_adult_signature": true,
  "order_items": {
    "id": 0,
    "order_id": 0,
    "sku": "string",
    "description": "string",
    "quantity": 0,
    "price": 0,
    "created_at": "2017-06-19T15:15:48Z",
    "updated_at": "2017-06-19T15:15:48Z",
    "unshippable": true,
    "customer_id": 0,
    "item_id": 0,
    "available": true,
    "packed": 0,
    "packaging": true,
    "wholesale_cost": 0,
    "package_id": 0,
    "is_bundle": true,
    "retail_fee": 0,
    "promo": true,
    "quote_item_id": 0,
    "returnable": true,
    "currency": "string",
    "wholesale_fee": 0
  },
  "ship_method": "string",
  "status_name": "string"
}
```
```json
{
  "message": "string"
}
```
```json
{
  "message": "string"
}
```
```json
{
  "message": "string"
}
```
<aside class="success">
This operation does not require authentication
</aside>

## getApiV2OrdersIdOrderItems

> Code samples

```shell
# You can also use wget
curl -X get ://staging.whiplashmerch.com/api/v2/orders/{id}/order_items \
  -H 'Accept: application/json'

```

```http
GET ://staging.whiplashmerch.com/api/v2/orders/{id}/order_items HTTP/1.1
Host: staging.whiplashmerch.com

Accept: application/json

```

```javascript
var headers = {
  'Accept':'application/json'

};

$.ajax({
  url: '://staging.whiplashmerch.com/api/v2/orders/{id}/order_items',
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
  'Accept':'application/json'

};

fetch('://staging.whiplashmerch.com/api/v2/orders/{id}/order_items',
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
  'Accept' => 'application/json'
}

result = RestClient.get '://staging.whiplashmerch.com/api/v2/orders/{id}/order_items', params: {
  }, headers: headers

p JSON.parse(result)
```

```python
import requests
headers = {
  'Accept': 'application/json'
}

r = requests.get('://staging.whiplashmerch.com/api/v2/orders/{id}/order_items', params={

}, headers = headers)

print r.json()
```

```java
URL obj = new URL("://staging.whiplashmerch.com/api/v2/orders/{id}/order_items");
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

`GET /api/v2/orders/{id}/order_items`

*Get all order items for an order*

Get all order items for an order

### Parameters

Parameter|In|Type|Required|Description
---|---|---|---|---|
search|query|string|false|JSON search string like {"attribute_eq": "Term"}
page|query|integer|false|Page of results to fetch.
per_page|query|integer|false|Number of results to return per page.
id|path|integer|true|No description


### Responses

Status|Meaning|Description
---|---|---|
200|[OK](https://tools.ietf.org/html/rfc7231#section-6.3.1)|Get all order items for an order
401|[Unauthorized](https://tools.ietf.org/html/rfc7235#section-3.1)|No description
403|[Forbidden](https://tools.ietf.org/html/rfc7231#section-6.5.3)|No description

> Example responses

```json
{
  "id": 0,
  "order_id": 0,
  "sku": "string",
  "description": "string",
  "quantity": 0,
  "price": 0,
  "created_at": "2017-06-19T15:15:48Z",
  "updated_at": "2017-06-19T15:15:48Z",
  "unshippable": true,
  "customer_id": 0,
  "item_id": 0,
  "available": true,
  "packed": 0,
  "packaging": true,
  "wholesale_cost": 0,
  "package_id": 0,
  "is_bundle": true,
  "retail_fee": 0,
  "promo": true,
  "quote_item_id": 0,
  "returnable": true,
  "currency": "string",
  "wholesale_fee": 0
}
```
```json
{
  "message": "string"
}
```
```json
{
  "message": "string"
}
```
<aside class="success">
This operation does not require authentication
</aside>

## getApiV2Orders

> Code samples

```shell
# You can also use wget
curl -X get ://staging.whiplashmerch.com/api/v2/orders \
  -H 'X-Customer-Id: string' \
  -H 'X-Shop-Id: string' \
  -H 'Accept: application/json'

```

```http
GET ://staging.whiplashmerch.com/api/v2/orders HTTP/1.1
Host: staging.whiplashmerch.com

Accept: application/json
X-Customer-Id: string
X-Shop-Id: string

```

```javascript
var headers = {
  'X-Customer-Id':'string',
  'X-Shop-Id':'string',
  'Accept':'application/json'

};

$.ajax({
  url: '://staging.whiplashmerch.com/api/v2/orders',
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
  'X-Customer-Id':'string',
  'X-Shop-Id':'string',
  'Accept':'application/json'

};

fetch('://staging.whiplashmerch.com/api/v2/orders',
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
  'X-Customer-Id' => 'string',
  'X-Shop-Id' => 'string',
  'Accept' => 'application/json'
}

result = RestClient.get '://staging.whiplashmerch.com/api/v2/orders', params: {
  }, headers: headers

p JSON.parse(result)
```

```python
import requests
headers = {
  'X-Customer-Id': 'string',
  'X-Shop-Id': 'string',
  'Accept': 'application/json'
}

r = requests.get('://staging.whiplashmerch.com/api/v2/orders', params={

}, headers = headers)

print r.json()
```

```java
URL obj = new URL("://staging.whiplashmerch.com/api/v2/orders");
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

`GET /api/v2/orders`

*Get all orders*

Get all orders

### Parameters

Parameter|In|Type|Required|Description
---|---|---|---|---|
X-Customer-Id|header|string|false|The customer associated with this resource.
X-Shop-Id|header|string|false|The shop associated with this resource.
search|query|string|false|JSON search string like {"attribute_eq": "Term"}
fields|query|string|false|Comma-separated list of fields to include in the response
page|query|integer|false|Page of results to fetch.
per_page|query|integer|false|Number of results to return per page.


### Responses

Status|Meaning|Description
---|---|---|
200|[OK](https://tools.ietf.org/html/rfc7231#section-6.3.1)|Get all orders
401|[Unauthorized](https://tools.ietf.org/html/rfc7235#section-3.1)|No description
403|[Forbidden](https://tools.ietf.org/html/rfc7231#section-6.5.3)|No description

> Example responses

```json
{
  "id": 0,
  "customer_id": 0,
  "first_name": "string",
  "last_name": "string",
  "full_name": "string",
  "billing_company": "string",
  "billing_address_1": "string",
  "billing_address_2": "string",
  "billing_city": "string",
  "billing_state": "string",
  "billing_zip": "string",
  "billing_country": "string",
  "billing_phone": "string",
  "shipping_company": "string",
  "shipping_address_1": "string",
  "shipping_address_2": "string",
  "shipping_city": "string",
  "shipping_state": "string",
  "shipping_zip": "string",
  "shipping_country": "string",
  "shipping_phone": "string",
  "email": "string",
  "ship_actual_cost": 0,
  "shipped_on": "2017-06-19T15:15:48Z",
  "ship_notes": "string",
  "created_at": "2017-06-19T15:15:48Z",
  "updated_at": "2017-06-19T15:15:48Z",
  "shipping_name": "string",
  "shop_shipping_method_price": 0,
  "shipping_confirmation_sent": true,
  "status": 0,
  "previous_status": 0,
  "ship_3rdparty_cost": 0,
  "public_note": "string",
  "gift": true,
  "billed": true,
  "ship_3rdparty_account": "string",
  "ship_3rdparty_zip": "string",
  "ship_3rdparty_country": "string",
  "shop_shipping_method_text": "string",
  "order_batch_id": 0,
  "order_orig": "string",
  "days_in_transit": 0,
  "quote_id": 0,
  "shipping_country_iso2": "string",
  "insure": true,
  "require_signature": true,
  "req_insurance_value": 0,
  "warehouse_id": 0,
  "workable_at": "2017-06-19T15:15:48Z",
  "requested_address": "string",
  "address_verified": true,
  "address_message": "string",
  "return_city": "string",
  "return_state": "string",
  "return_country": "string",
  "return_zip": "string",
  "return_address_1": "string",
  "return_address_2": "string",
  "return_phone": "string",
  "return_email": "string",
  "level1_token": "string",
  "level2_token": "string",
  "return_time_limit": 0,
  "return_address_verified": true,
  "shipping_method_id": 0,
  "skip_street_date": true,
  "shop_warehouse_id": 0,
  "shop_shipping_method_currency": "string",
  "saturday_delivery": true,
  "shop_created_at": "2017-06-19T15:15:48Z",
  "shop_updated_at": "2017-06-19T15:15:48Z",
  "residential": true,
  "skip_address_verification": true,
  "due_at": "2017-06-19T15:15:48Z",
  "do_not_bill": true,
  "return_company": "string",
  "contains_alcohol": true,
  "require_adult_signature": true,
  "order_items": {
    "id": 0,
    "order_id": 0,
    "sku": "string",
    "description": "string",
    "quantity": 0,
    "price": 0,
    "created_at": "2017-06-19T15:15:48Z",
    "updated_at": "2017-06-19T15:15:48Z",
    "unshippable": true,
    "customer_id": 0,
    "item_id": 0,
    "available": true,
    "packed": 0,
    "packaging": true,
    "wholesale_cost": 0,
    "package_id": 0,
    "is_bundle": true,
    "retail_fee": 0,
    "promo": true,
    "quote_item_id": 0,
    "returnable": true,
    "currency": "string",
    "wholesale_fee": 0
  },
  "ship_method": "string",
  "status_name": "string"
}
```
```json
{
  "message": "string"
}
```
```json
{
  "message": "string"
}
```
<aside class="success">
This operation does not require authentication
</aside>

## postApiV2Orders

> Code samples

```shell
# You can also use wget
curl -X post ://staging.whiplashmerch.com/api/v2/orders \
  -H 'X-Customer-Id: string' \
  -H 'X-Shop-Id: string' \
  -H 'Content-Type: application/json' \
  -H 'Accept: application/json'

```

```http
POST ://staging.whiplashmerch.com/api/v2/orders HTTP/1.1
Host: staging.whiplashmerch.com
Content-Type: application/json
Accept: application/json
X-Customer-Id: string
X-Shop-Id: string

```

```javascript
var headers = {
  'X-Customer-Id':'string',
  'X-Shop-Id':'string',
  'Content-Type':'application/json',
  'Accept':'application/json'

};

$.ajax({
  url: '://staging.whiplashmerch.com/api/v2/orders',
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
  'X-Customer-Id':'string',
  'X-Shop-Id':'string',
  'Content-Type':'application/json',
  'Accept':'application/json'

};

fetch('://staging.whiplashmerch.com/api/v2/orders',
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
  'X-Customer-Id' => 'string',
  'X-Shop-Id' => 'string',
  'Content-Type' => 'application/json',
  'Accept' => 'application/json'
}

result = RestClient.post '://staging.whiplashmerch.com/api/v2/orders', params: {
  }, headers: headers

p JSON.parse(result)
```

```python
import requests
headers = {
  'X-Customer-Id': 'string',
  'X-Shop-Id': 'string',
  'Content-Type': 'application/json',
  'Accept': 'application/json'
}

r = requests.post('://staging.whiplashmerch.com/api/v2/orders', params={

}, headers = headers)

print r.json()
```

```java
URL obj = new URL("://staging.whiplashmerch.com/api/v2/orders");
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

`POST /api/v2/orders`

*Create an order*

Create an order

### Parameters

Parameter|In|Type|Required|Description
---|---|---|---|---|
X-Customer-Id|header|string|false|The customer associated with this resource.
X-Shop-Id|header|string|false|The shop associated with this resource.
first_name|formData|string|false|No description
last_name|formData|string|false|No description
full_name|formData|string|false|No description
billing_company|formData|string|false|No description
billing_address_1|formData|string|false|No description
billing_address_2|formData|string|false|No description
billing_city|formData|string|false|No description
billing_state|formData|string|false|No description
billing_zip|formData|string|false|No description
billing_country|formData|string|false|No description
billing_phone|formData|string|false|No description
shipping_company|formData|string|false|No description
shipping_address_1|formData|string|false|No description
shipping_address_2|formData|string|false|No description
shipping_city|formData|string|false|No description
shipping_state|formData|string|false|No description
shipping_zip|formData|string|false|No description
shipping_country|formData|string|false|No description
shipping_phone|formData|string|false|No description
email|formData|string|false|No description
ship_notes|formData|string|false|No description
shipping_name|formData|string|false|No description
shop_shipping_method_price|formData|number|false|No description
ship_3rdparty_cost|formData|number|false|No description
public_note|formData|string|false|No description
gift|formData|boolean|false|No description
ship_3rdparty_account|formData|string|false|No description
ship_3rdparty_zip|formData|string|false|No description
ship_3rdparty_country|formData|string|false|No description
shop_shipping_method_text|formData|string|false|No description
order_orig|formData|string|false|No description
days_in_transit|formData|integer|false|No description
shipping_country_iso2|formData|string|false|No description
insure|formData|boolean|false|No description
require_signature|formData|boolean|false|No description
req_insurance_value|formData|number|false|No description
requested_address|formData|string|false|No description
return_city|formData|string|false|No description
return_state|formData|string|false|No description
return_country|formData|string|false|No description
return_zip|formData|string|false|No description
return_address_1|formData|string|false|No description
return_address_2|formData|string|false|No description
return_phone|formData|string|false|No description
return_email|formData|string|false|No description
level1_token|formData|string|false|No description
level2_token|formData|string|false|No description
return_time_limit|formData|integer|false|No description
shipping_method_id|formData|integer|false|No description
skip_street_date|formData|boolean|false|No description
shop_warehouse_id|formData|integer|false|No description
shop_shipping_method_currency|formData|string|false|No description
saturday_delivery|formData|boolean|false|No description
shop_created_at|formData|string|false|No description
shop_updated_at|formData|string|false|No description
residential|formData|boolean|false|No description
skip_address_verification|formData|boolean|false|No description
due_at|formData|string|false|No description
do_not_bill|formData|boolean|false|No description
return_company|formData|string|false|No description
contains_alcohol|formData|boolean|false|No description
require_adult_signature|formData|boolean|false|No description
order_items_attributes[quantity]|formData|array[integer]|false|number of this item in Order
order_items_attributes[price]|formData|array[number]|false|price of this item
order_items_attributes[currency]|formData|array[string]|false|currency code for this item
order_items_attributes[originator_id]|formData|array[string]|false|The original id of the order item
order_items_attributes[item_id]|formData|array[integer]|false|No description
order_items_attributes[item_originator_id]|formData|array[string]|false|The original id of the item


### Responses

Status|Meaning|Description
---|---|---|
201|[Created](https://tools.ietf.org/html/rfc7231#section-6.3.2)|Create an order
401|[Unauthorized](https://tools.ietf.org/html/rfc7235#section-3.1)|No description
403|[Forbidden](https://tools.ietf.org/html/rfc7231#section-6.5.3)|No description
409|[Conflict](https://tools.ietf.org/html/rfc7231#section-6.5.8)|No description
422|[Unprocessable Entity](https://tools.ietf.org/html/rfc2518#section-10.3)|No description

> Example responses

```json
{
  "id": 0,
  "customer_id": 0,
  "first_name": "string",
  "last_name": "string",
  "full_name": "string",
  "billing_company": "string",
  "billing_address_1": "string",
  "billing_address_2": "string",
  "billing_city": "string",
  "billing_state": "string",
  "billing_zip": "string",
  "billing_country": "string",
  "billing_phone": "string",
  "shipping_company": "string",
  "shipping_address_1": "string",
  "shipping_address_2": "string",
  "shipping_city": "string",
  "shipping_state": "string",
  "shipping_zip": "string",
  "shipping_country": "string",
  "shipping_phone": "string",
  "email": "string",
  "ship_actual_cost": 0,
  "shipped_on": "2017-06-19T15:15:48Z",
  "ship_notes": "string",
  "created_at": "2017-06-19T15:15:48Z",
  "updated_at": "2017-06-19T15:15:48Z",
  "shipping_name": "string",
  "shop_shipping_method_price": 0,
  "shipping_confirmation_sent": true,
  "status": 0,
  "previous_status": 0,
  "ship_3rdparty_cost": 0,
  "public_note": "string",
  "gift": true,
  "billed": true,
  "ship_3rdparty_account": "string",
  "ship_3rdparty_zip": "string",
  "ship_3rdparty_country": "string",
  "shop_shipping_method_text": "string",
  "order_batch_id": 0,
  "order_orig": "string",
  "days_in_transit": 0,
  "quote_id": 0,
  "shipping_country_iso2": "string",
  "insure": true,
  "require_signature": true,
  "req_insurance_value": 0,
  "warehouse_id": 0,
  "workable_at": "2017-06-19T15:15:48Z",
  "requested_address": "string",
  "address_verified": true,
  "address_message": "string",
  "return_city": "string",
  "return_state": "string",
  "return_country": "string",
  "return_zip": "string",
  "return_address_1": "string",
  "return_address_2": "string",
  "return_phone": "string",
  "return_email": "string",
  "level1_token": "string",
  "level2_token": "string",
  "return_time_limit": 0,
  "return_address_verified": true,
  "shipping_method_id": 0,
  "skip_street_date": true,
  "shop_warehouse_id": 0,
  "shop_shipping_method_currency": "string",
  "saturday_delivery": true,
  "shop_created_at": "2017-06-19T15:15:48Z",
  "shop_updated_at": "2017-06-19T15:15:48Z",
  "residential": true,
  "skip_address_verification": true,
  "due_at": "2017-06-19T15:15:48Z",
  "do_not_bill": true,
  "return_company": "string",
  "contains_alcohol": true,
  "require_adult_signature": true,
  "order_items": {
    "id": 0,
    "order_id": 0,
    "sku": "string",
    "description": "string",
    "quantity": 0,
    "price": 0,
    "created_at": "2017-06-19T15:15:48Z",
    "updated_at": "2017-06-19T15:15:48Z",
    "unshippable": true,
    "customer_id": 0,
    "item_id": 0,
    "available": true,
    "packed": 0,
    "packaging": true,
    "wholesale_cost": 0,
    "package_id": 0,
    "is_bundle": true,
    "retail_fee": 0,
    "promo": true,
    "quote_item_id": 0,
    "returnable": true,
    "currency": "string",
    "wholesale_fee": 0
  },
  "ship_method": "string",
  "status_name": "string"
}
```
```json
{
  "message": "string"
}
```
```json
{
  "message": "string"
}
```
```json
{
  "message": "string"
}
```
```json
{
  "message": "string"
}
```
<aside class="success">
This operation does not require authentication
</aside>

## getApiV2OrdersCount

> Code samples

```shell
# You can also use wget
curl -X get ://staging.whiplashmerch.com/api/v2/orders/count \
  -H 'X-Customer-Id: string' \
  -H 'X-Shop-Id: string' \
  -H 'Accept: application/json'

```

```http
GET ://staging.whiplashmerch.com/api/v2/orders/count HTTP/1.1
Host: staging.whiplashmerch.com

Accept: application/json
X-Customer-Id: string
X-Shop-Id: string

```

```javascript
var headers = {
  'X-Customer-Id':'string',
  'X-Shop-Id':'string',
  'Accept':'application/json'

};

$.ajax({
  url: '://staging.whiplashmerch.com/api/v2/orders/count',
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
  'X-Customer-Id':'string',
  'X-Shop-Id':'string',
  'Accept':'application/json'

};

fetch('://staging.whiplashmerch.com/api/v2/orders/count',
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
  'X-Customer-Id' => 'string',
  'X-Shop-Id' => 'string',
  'Accept' => 'application/json'
}

result = RestClient.get '://staging.whiplashmerch.com/api/v2/orders/count', params: {
  }, headers: headers

p JSON.parse(result)
```

```python
import requests
headers = {
  'X-Customer-Id': 'string',
  'X-Shop-Id': 'string',
  'Accept': 'application/json'
}

r = requests.get('://staging.whiplashmerch.com/api/v2/orders/count', params={

}, headers = headers)

print r.json()
```

```java
URL obj = new URL("://staging.whiplashmerch.com/api/v2/orders/count");
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

`GET /api/v2/orders/count`

*Returns count of orders*

Returns count of orders

### Parameters

Parameter|In|Type|Required|Description
---|---|---|---|---|
X-Customer-Id|header|string|false|The customer associated with this resource.
X-Shop-Id|header|string|false|The shop associated with this resource.
search|query|string|false|JSON search string like {"attribute_eq": "Term"}


### Responses

Status|Meaning|Description
---|---|---|
200|[OK](https://tools.ietf.org/html/rfc7231#section-6.3.1)|Returns count of orders
401|[Unauthorized](https://tools.ietf.org/html/rfc7235#section-3.1)|No description
403|[Forbidden](https://tools.ietf.org/html/rfc7231#section-6.5.3)|No description

> Example responses

```json
{
  "id": 0,
  "customer_id": 0,
  "first_name": "string",
  "last_name": "string",
  "full_name": "string",
  "billing_company": "string",
  "billing_address_1": "string",
  "billing_address_2": "string",
  "billing_city": "string",
  "billing_state": "string",
  "billing_zip": "string",
  "billing_country": "string",
  "billing_phone": "string",
  "shipping_company": "string",
  "shipping_address_1": "string",
  "shipping_address_2": "string",
  "shipping_city": "string",
  "shipping_state": "string",
  "shipping_zip": "string",
  "shipping_country": "string",
  "shipping_phone": "string",
  "email": "string",
  "ship_actual_cost": 0,
  "shipped_on": "2017-06-19T15:15:48Z",
  "ship_notes": "string",
  "created_at": "2017-06-19T15:15:48Z",
  "updated_at": "2017-06-19T15:15:48Z",
  "shipping_name": "string",
  "shop_shipping_method_price": 0,
  "shipping_confirmation_sent": true,
  "status": 0,
  "previous_status": 0,
  "ship_3rdparty_cost": 0,
  "public_note": "string",
  "gift": true,
  "billed": true,
  "ship_3rdparty_account": "string",
  "ship_3rdparty_zip": "string",
  "ship_3rdparty_country": "string",
  "shop_shipping_method_text": "string",
  "order_batch_id": 0,
  "order_orig": "string",
  "days_in_transit": 0,
  "quote_id": 0,
  "shipping_country_iso2": "string",
  "insure": true,
  "require_signature": true,
  "req_insurance_value": 0,
  "warehouse_id": 0,
  "workable_at": "2017-06-19T15:15:48Z",
  "requested_address": "string",
  "address_verified": true,
  "address_message": "string",
  "return_city": "string",
  "return_state": "string",
  "return_country": "string",
  "return_zip": "string",
  "return_address_1": "string",
  "return_address_2": "string",
  "return_phone": "string",
  "return_email": "string",
  "level1_token": "string",
  "level2_token": "string",
  "return_time_limit": 0,
  "return_address_verified": true,
  "shipping_method_id": 0,
  "skip_street_date": true,
  "shop_warehouse_id": 0,
  "shop_shipping_method_currency": "string",
  "saturday_delivery": true,
  "shop_created_at": "2017-06-19T15:15:48Z",
  "shop_updated_at": "2017-06-19T15:15:48Z",
  "residential": true,
  "skip_address_verification": true,
  "due_at": "2017-06-19T15:15:48Z",
  "do_not_bill": true,
  "return_company": "string",
  "contains_alcohol": true,
  "require_adult_signature": true,
  "order_items": {
    "id": 0,
    "order_id": 0,
    "sku": "string",
    "description": "string",
    "quantity": 0,
    "price": 0,
    "created_at": "2017-06-19T15:15:48Z",
    "updated_at": "2017-06-19T15:15:48Z",
    "unshippable": true,
    "customer_id": 0,
    "item_id": 0,
    "available": true,
    "packed": 0,
    "packaging": true,
    "wholesale_cost": 0,
    "package_id": 0,
    "is_bundle": true,
    "retail_fee": 0,
    "promo": true,
    "quote_item_id": 0,
    "returnable": true,
    "currency": "string",
    "wholesale_fee": 0
  },
  "ship_method": "string",
  "status_name": "string"
}
```
```json
{
  "message": "string"
}
```
```json
{
  "message": "string"
}
```
<aside class="success">
This operation does not require authentication
</aside>

## putApiV2OrdersBulkAction

> Code samples

```shell
# You can also use wget
curl -X put ://staging.whiplashmerch.com/api/v2/orders/bulk/{action} \
  -H 'X-Customer-Id: string' \
  -H 'X-Shop-Id: string' \
  -H 'Content-Type: application/json' \
  -H 'Accept: application/json'

```

```http
PUT ://staging.whiplashmerch.com/api/v2/orders/bulk/{action} HTTP/1.1
Host: staging.whiplashmerch.com
Content-Type: application/json
Accept: application/json
X-Customer-Id: string
X-Shop-Id: string

```

```javascript
var headers = {
  'X-Customer-Id':'string',
  'X-Shop-Id':'string',
  'Content-Type':'application/json',
  'Accept':'application/json'

};

$.ajax({
  url: '://staging.whiplashmerch.com/api/v2/orders/bulk/{action}',
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
  'X-Customer-Id':'string',
  'X-Shop-Id':'string',
  'Content-Type':'application/json',
  'Accept':'application/json'

};

fetch('://staging.whiplashmerch.com/api/v2/orders/bulk/{action}',
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
  'X-Customer-Id' => 'string',
  'X-Shop-Id' => 'string',
  'Content-Type' => 'application/json',
  'Accept' => 'application/json'
}

result = RestClient.put '://staging.whiplashmerch.com/api/v2/orders/bulk/{action}', params: {
  }, headers: headers

p JSON.parse(result)
```

```python
import requests
headers = {
  'X-Customer-Id': 'string',
  'X-Shop-Id': 'string',
  'Content-Type': 'application/json',
  'Accept': 'application/json'
}

r = requests.put('://staging.whiplashmerch.com/api/v2/orders/bulk/{action}', params={

}, headers = headers)

print r.json()
```

```java
URL obj = new URL("://staging.whiplashmerch.com/api/v2/orders/bulk/{action}");
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

`PUT /api/v2/orders/bulk/{action}`

*Bulk update orders*

Bulk update orders

### Parameters

Parameter|In|Type|Required|Description
---|---|---|---|---|
X-Customer-Id|header|string|false|The customer associated with this resource.
X-Shop-Id|header|string|false|The shop associated with this resource.
ids|formData|array[integer]|true|IDs of the orders to update
action|path|integer|true|No description


### Responses

Status|Meaning|Description
---|---|---|
200|[OK](https://tools.ietf.org/html/rfc7231#section-6.3.1)|Bulk update orders
401|[Unauthorized](https://tools.ietf.org/html/rfc7235#section-3.1)|No description
403|[Forbidden](https://tools.ietf.org/html/rfc7231#section-6.5.3)|No description
405|[Method Not Allowed](https://tools.ietf.org/html/rfc7231#section-6.5.5)|No description
422|[Unprocessable Entity](https://tools.ietf.org/html/rfc2518#section-10.3)|No description

> Example responses

```json
{
  "id": 0,
  "customer_id": 0,
  "first_name": "string",
  "last_name": "string",
  "full_name": "string",
  "billing_company": "string",
  "billing_address_1": "string",
  "billing_address_2": "string",
  "billing_city": "string",
  "billing_state": "string",
  "billing_zip": "string",
  "billing_country": "string",
  "billing_phone": "string",
  "shipping_company": "string",
  "shipping_address_1": "string",
  "shipping_address_2": "string",
  "shipping_city": "string",
  "shipping_state": "string",
  "shipping_zip": "string",
  "shipping_country": "string",
  "shipping_phone": "string",
  "email": "string",
  "ship_actual_cost": 0,
  "shipped_on": "2017-06-19T15:15:48Z",
  "ship_notes": "string",
  "created_at": "2017-06-19T15:15:48Z",
  "updated_at": "2017-06-19T15:15:48Z",
  "shipping_name": "string",
  "shop_shipping_method_price": 0,
  "shipping_confirmation_sent": true,
  "status": 0,
  "previous_status": 0,
  "ship_3rdparty_cost": 0,
  "public_note": "string",
  "gift": true,
  "billed": true,
  "ship_3rdparty_account": "string",
  "ship_3rdparty_zip": "string",
  "ship_3rdparty_country": "string",
  "shop_shipping_method_text": "string",
  "order_batch_id": 0,
  "order_orig": "string",
  "days_in_transit": 0,
  "quote_id": 0,
  "shipping_country_iso2": "string",
  "insure": true,
  "require_signature": true,
  "req_insurance_value": 0,
  "warehouse_id": 0,
  "workable_at": "2017-06-19T15:15:48Z",
  "requested_address": "string",
  "address_verified": true,
  "address_message": "string",
  "return_city": "string",
  "return_state": "string",
  "return_country": "string",
  "return_zip": "string",
  "return_address_1": "string",
  "return_address_2": "string",
  "return_phone": "string",
  "return_email": "string",
  "level1_token": "string",
  "level2_token": "string",
  "return_time_limit": 0,
  "return_address_verified": true,
  "shipping_method_id": 0,
  "skip_street_date": true,
  "shop_warehouse_id": 0,
  "shop_shipping_method_currency": "string",
  "saturday_delivery": true,
  "shop_created_at": "2017-06-19T15:15:48Z",
  "shop_updated_at": "2017-06-19T15:15:48Z",
  "residential": true,
  "skip_address_verification": true,
  "due_at": "2017-06-19T15:15:48Z",
  "do_not_bill": true,
  "return_company": "string",
  "contains_alcohol": true,
  "require_adult_signature": true,
  "order_items": {
    "id": 0,
    "order_id": 0,
    "sku": "string",
    "description": "string",
    "quantity": 0,
    "price": 0,
    "created_at": "2017-06-19T15:15:48Z",
    "updated_at": "2017-06-19T15:15:48Z",
    "unshippable": true,
    "customer_id": 0,
    "item_id": 0,
    "available": true,
    "packed": 0,
    "packaging": true,
    "wholesale_cost": 0,
    "package_id": 0,
    "is_bundle": true,
    "retail_fee": 0,
    "promo": true,
    "quote_item_id": 0,
    "returnable": true,
    "currency": "string",
    "wholesale_fee": 0
  },
  "ship_method": "string",
  "status_name": "string"
}
```
```json
{
  "message": "string"
}
```
```json
{
  "message": "string"
}
```
```json
{
  "message": "string"
}
```
```json
{
  "message": "string"
}
```
<aside class="success">
This operation does not require authentication
</aside>

## getApiV2OrdersIdPackages

> Code samples

```shell
# You can also use wget
curl -X get ://staging.whiplashmerch.com/api/v2/orders/{id}/packages \
  -H 'X-Customer-Id: string' \
  -H 'X-Shop-Id: string' \
  -H 'Accept: application/json'

```

```http
GET ://staging.whiplashmerch.com/api/v2/orders/{id}/packages HTTP/1.1
Host: staging.whiplashmerch.com

Accept: application/json
X-Customer-Id: string
X-Shop-Id: string

```

```javascript
var headers = {
  'X-Customer-Id':'string',
  'X-Shop-Id':'string',
  'Accept':'application/json'

};

$.ajax({
  url: '://staging.whiplashmerch.com/api/v2/orders/{id}/packages',
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
  'X-Customer-Id':'string',
  'X-Shop-Id':'string',
  'Accept':'application/json'

};

fetch('://staging.whiplashmerch.com/api/v2/orders/{id}/packages',
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
  'X-Customer-Id' => 'string',
  'X-Shop-Id' => 'string',
  'Accept' => 'application/json'
}

result = RestClient.get '://staging.whiplashmerch.com/api/v2/orders/{id}/packages', params: {
  }, headers: headers

p JSON.parse(result)
```

```python
import requests
headers = {
  'X-Customer-Id': 'string',
  'X-Shop-Id': 'string',
  'Accept': 'application/json'
}

r = requests.get('://staging.whiplashmerch.com/api/v2/orders/{id}/packages', params={

}, headers = headers)

print r.json()
```

```java
URL obj = new URL("://staging.whiplashmerch.com/api/v2/orders/{id}/packages");
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

`GET /api/v2/orders/{id}/packages`

*Get the packages associated with an order*

Get the packages associated with an order

### Parameters

Parameter|In|Type|Required|Description
---|---|---|---|---|
X-Customer-Id|header|string|false|The customer associated with this resource.
X-Shop-Id|header|string|false|The shop associated with this resource.
page|query|integer|false|Page of results to fetch.
per_page|query|integer|false|Number of results to return per page.
id|path|integer|true|No description


### Responses

Status|Meaning|Description
---|---|---|
200|[OK](https://tools.ietf.org/html/rfc7231#section-6.3.1)|Get the packages associated with an order
401|[Unauthorized](https://tools.ietf.org/html/rfc7235#section-3.1)|No description
403|[Forbidden](https://tools.ietf.org/html/rfc7231#section-6.5.3)|No description

> Example responses

```json
{
  "id": 0,
  "order_id": 0,
  "pick_fee_actual": 0,
  "pack_fee_actual": 0,
  "packaging_fee_actual": 0,
  "shipped_on": "2017-06-19T15:15:48Z",
  "ship_actual_cost": 0,
  "created_at": "2017-06-19T15:15:48Z",
  "updated_at": "2017-06-19T15:15:48Z",
  "actual_weight": 0,
  "tracking": "string",
  "bill_of_lading": "string"
}
```
```json
{
  "message": "string"
}
```
```json
{
  "message": "string"
}
```
<aside class="success">
This operation does not require authentication
</aside>

## getApiV2OrdersIdMeta

> Code samples

```shell
# You can also use wget
curl -X get ://staging.whiplashmerch.com/api/v2/orders/{id}/meta \
  -H 'X-Customer-Id: string' \
  -H 'X-Shop-Id: string' \
  -H 'Accept: application/json'

```

```http
GET ://staging.whiplashmerch.com/api/v2/orders/{id}/meta HTTP/1.1
Host: staging.whiplashmerch.com

Accept: application/json
X-Customer-Id: string
X-Shop-Id: string

```

```javascript
var headers = {
  'X-Customer-Id':'string',
  'X-Shop-Id':'string',
  'Accept':'application/json'

};

$.ajax({
  url: '://staging.whiplashmerch.com/api/v2/orders/{id}/meta',
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
  'X-Customer-Id':'string',
  'X-Shop-Id':'string',
  'Accept':'application/json'

};

fetch('://staging.whiplashmerch.com/api/v2/orders/{id}/meta',
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
  'X-Customer-Id' => 'string',
  'X-Shop-Id' => 'string',
  'Accept' => 'application/json'
}

result = RestClient.get '://staging.whiplashmerch.com/api/v2/orders/{id}/meta', params: {
  }, headers: headers

p JSON.parse(result)
```

```python
import requests
headers = {
  'X-Customer-Id': 'string',
  'X-Shop-Id': 'string',
  'Accept': 'application/json'
}

r = requests.get('://staging.whiplashmerch.com/api/v2/orders/{id}/meta', params={

}, headers = headers)

print r.json()
```

```java
URL obj = new URL("://staging.whiplashmerch.com/api/v2/orders/{id}/meta");
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

`GET /api/v2/orders/{id}/meta`

*Get the meta info for an order*

Get the meta info for an order

### Parameters

Parameter|In|Type|Required|Description
---|---|---|---|---|
X-Customer-Id|header|string|false|The customer associated with this resource.
X-Shop-Id|header|string|false|The shop associated with this resource.
id|path|integer|true|No description


### Responses

Status|Meaning|Description
---|---|---|
200|[OK](https://tools.ietf.org/html/rfc7231#section-6.3.1)|Get the meta info for an order
401|[Unauthorized](https://tools.ietf.org/html/rfc7235#section-3.1)|No description
403|[Forbidden](https://tools.ietf.org/html/rfc7231#section-6.5.3)|No description

> Example responses

```json
{
  "id": 0,
  "customer_id": 0,
  "first_name": "string",
  "last_name": "string",
  "full_name": "string",
  "billing_company": "string",
  "billing_address_1": "string",
  "billing_address_2": "string",
  "billing_city": "string",
  "billing_state": "string",
  "billing_zip": "string",
  "billing_country": "string",
  "billing_phone": "string",
  "shipping_company": "string",
  "shipping_address_1": "string",
  "shipping_address_2": "string",
  "shipping_city": "string",
  "shipping_state": "string",
  "shipping_zip": "string",
  "shipping_country": "string",
  "shipping_phone": "string",
  "email": "string",
  "ship_actual_cost": 0,
  "shipped_on": "2017-06-19T15:15:48Z",
  "ship_notes": "string",
  "created_at": "2017-06-19T15:15:48Z",
  "updated_at": "2017-06-19T15:15:48Z",
  "shipping_name": "string",
  "shop_shipping_method_price": 0,
  "shipping_confirmation_sent": true,
  "status": 0,
  "previous_status": 0,
  "ship_3rdparty_cost": 0,
  "public_note": "string",
  "gift": true,
  "billed": true,
  "ship_3rdparty_account": "string",
  "ship_3rdparty_zip": "string",
  "ship_3rdparty_country": "string",
  "shop_shipping_method_text": "string",
  "order_batch_id": 0,
  "order_orig": "string",
  "days_in_transit": 0,
  "quote_id": 0,
  "shipping_country_iso2": "string",
  "insure": true,
  "require_signature": true,
  "req_insurance_value": 0,
  "warehouse_id": 0,
  "workable_at": "2017-06-19T15:15:48Z",
  "requested_address": "string",
  "address_verified": true,
  "address_message": "string",
  "return_city": "string",
  "return_state": "string",
  "return_country": "string",
  "return_zip": "string",
  "return_address_1": "string",
  "return_address_2": "string",
  "return_phone": "string",
  "return_email": "string",
  "level1_token": "string",
  "level2_token": "string",
  "return_time_limit": 0,
  "return_address_verified": true,
  "shipping_method_id": 0,
  "skip_street_date": true,
  "shop_warehouse_id": 0,
  "shop_shipping_method_currency": "string",
  "saturday_delivery": true,
  "shop_created_at": "2017-06-19T15:15:48Z",
  "shop_updated_at": "2017-06-19T15:15:48Z",
  "residential": true,
  "skip_address_verification": true,
  "due_at": "2017-06-19T15:15:48Z",
  "do_not_bill": true,
  "return_company": "string",
  "contains_alcohol": true,
  "require_adult_signature": true,
  "order_items": {
    "id": 0,
    "order_id": 0,
    "sku": "string",
    "description": "string",
    "quantity": 0,
    "price": 0,
    "created_at": "2017-06-19T15:15:48Z",
    "updated_at": "2017-06-19T15:15:48Z",
    "unshippable": true,
    "customer_id": 0,
    "item_id": 0,
    "available": true,
    "packed": 0,
    "packaging": true,
    "wholesale_cost": 0,
    "package_id": 0,
    "is_bundle": true,
    "retail_fee": 0,
    "promo": true,
    "quote_item_id": 0,
    "returnable": true,
    "currency": "string",
    "wholesale_fee": 0
  },
  "ship_method": "string",
  "status_name": "string"
}
```
```json
{
  "message": "string"
}
```
```json
{
  "message": "string"
}
```
<aside class="success">
This operation does not require authentication
</aside>

## getApiV2OrdersIdShippingWeight

> Code samples

```shell
# You can also use wget
curl -X get ://staging.whiplashmerch.com/api/v2/orders/{id}/shipping_weight \
  -H 'X-Customer-Id: string' \
  -H 'X-Shop-Id: string' \
  -H 'Accept: application/json'

```

```http
GET ://staging.whiplashmerch.com/api/v2/orders/{id}/shipping_weight HTTP/1.1
Host: staging.whiplashmerch.com

Accept: application/json
X-Customer-Id: string
X-Shop-Id: string

```

```javascript
var headers = {
  'X-Customer-Id':'string',
  'X-Shop-Id':'string',
  'Accept':'application/json'

};

$.ajax({
  url: '://staging.whiplashmerch.com/api/v2/orders/{id}/shipping_weight',
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
  'X-Customer-Id':'string',
  'X-Shop-Id':'string',
  'Accept':'application/json'

};

fetch('://staging.whiplashmerch.com/api/v2/orders/{id}/shipping_weight',
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
  'X-Customer-Id' => 'string',
  'X-Shop-Id' => 'string',
  'Accept' => 'application/json'
}

result = RestClient.get '://staging.whiplashmerch.com/api/v2/orders/{id}/shipping_weight', params: {
  }, headers: headers

p JSON.parse(result)
```

```python
import requests
headers = {
  'X-Customer-Id': 'string',
  'X-Shop-Id': 'string',
  'Accept': 'application/json'
}

r = requests.get('://staging.whiplashmerch.com/api/v2/orders/{id}/shipping_weight', params={

}, headers = headers)

print r.json()
```

```java
URL obj = new URL("://staging.whiplashmerch.com/api/v2/orders/{id}/shipping_weight");
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

`GET /api/v2/orders/{id}/shipping_weight`

*Get the shipping weight for an order*

Get the shipping weight for an order

### Parameters

Parameter|In|Type|Required|Description
---|---|---|---|---|
X-Customer-Id|header|string|false|The customer associated with this resource.
X-Shop-Id|header|string|false|The shop associated with this resource.
id|path|integer|true|No description


### Responses

Status|Meaning|Description
---|---|---|
200|[OK](https://tools.ietf.org/html/rfc7231#section-6.3.1)|Get the shipping weight for an order
401|[Unauthorized](https://tools.ietf.org/html/rfc7235#section-3.1)|No description
403|[Forbidden](https://tools.ietf.org/html/rfc7231#section-6.5.3)|No description

> Example responses

```json
{
  "id": 0,
  "customer_id": 0,
  "first_name": "string",
  "last_name": "string",
  "full_name": "string",
  "billing_company": "string",
  "billing_address_1": "string",
  "billing_address_2": "string",
  "billing_city": "string",
  "billing_state": "string",
  "billing_zip": "string",
  "billing_country": "string",
  "billing_phone": "string",
  "shipping_company": "string",
  "shipping_address_1": "string",
  "shipping_address_2": "string",
  "shipping_city": "string",
  "shipping_state": "string",
  "shipping_zip": "string",
  "shipping_country": "string",
  "shipping_phone": "string",
  "email": "string",
  "ship_actual_cost": 0,
  "shipped_on": "2017-06-19T15:15:48Z",
  "ship_notes": "string",
  "created_at": "2017-06-19T15:15:48Z",
  "updated_at": "2017-06-19T15:15:48Z",
  "shipping_name": "string",
  "shop_shipping_method_price": 0,
  "shipping_confirmation_sent": true,
  "status": 0,
  "previous_status": 0,
  "ship_3rdparty_cost": 0,
  "public_note": "string",
  "gift": true,
  "billed": true,
  "ship_3rdparty_account": "string",
  "ship_3rdparty_zip": "string",
  "ship_3rdparty_country": "string",
  "shop_shipping_method_text": "string",
  "order_batch_id": 0,
  "order_orig": "string",
  "days_in_transit": 0,
  "quote_id": 0,
  "shipping_country_iso2": "string",
  "insure": true,
  "require_signature": true,
  "req_insurance_value": 0,
  "warehouse_id": 0,
  "workable_at": "2017-06-19T15:15:48Z",
  "requested_address": "string",
  "address_verified": true,
  "address_message": "string",
  "return_city": "string",
  "return_state": "string",
  "return_country": "string",
  "return_zip": "string",
  "return_address_1": "string",
  "return_address_2": "string",
  "return_phone": "string",
  "return_email": "string",
  "level1_token": "string",
  "level2_token": "string",
  "return_time_limit": 0,
  "return_address_verified": true,
  "shipping_method_id": 0,
  "skip_street_date": true,
  "shop_warehouse_id": 0,
  "shop_shipping_method_currency": "string",
  "saturday_delivery": true,
  "shop_created_at": "2017-06-19T15:15:48Z",
  "shop_updated_at": "2017-06-19T15:15:48Z",
  "residential": true,
  "skip_address_verification": true,
  "due_at": "2017-06-19T15:15:48Z",
  "do_not_bill": true,
  "return_company": "string",
  "contains_alcohol": true,
  "require_adult_signature": true,
  "order_items": {
    "id": 0,
    "order_id": 0,
    "sku": "string",
    "description": "string",
    "quantity": 0,
    "price": 0,
    "created_at": "2017-06-19T15:15:48Z",
    "updated_at": "2017-06-19T15:15:48Z",
    "unshippable": true,
    "customer_id": 0,
    "item_id": 0,
    "available": true,
    "packed": 0,
    "packaging": true,
    "wholesale_cost": 0,
    "package_id": 0,
    "is_bundle": true,
    "retail_fee": 0,
    "promo": true,
    "quote_item_id": 0,
    "returnable": true,
    "currency": "string",
    "wholesale_fee": 0
  },
  "ship_method": "string",
  "status_name": "string"
}
```
```json
{
  "message": "string"
}
```
```json
{
  "message": "string"
}
```
<aside class="success">
This operation does not require authentication
</aside>

## getApiV2OrdersIdShippingRates

> Code samples

```shell
# You can also use wget
curl -X get ://staging.whiplashmerch.com/api/v2/orders/{id}/shipping_rates \
  -H 'X-Customer-Id: string' \
  -H 'X-Shop-Id: string' \
  -H 'Accept: application/json'

```

```http
GET ://staging.whiplashmerch.com/api/v2/orders/{id}/shipping_rates HTTP/1.1
Host: staging.whiplashmerch.com

Accept: application/json
X-Customer-Id: string
X-Shop-Id: string

```

```javascript
var headers = {
  'X-Customer-Id':'string',
  'X-Shop-Id':'string',
  'Accept':'application/json'

};

$.ajax({
  url: '://staging.whiplashmerch.com/api/v2/orders/{id}/shipping_rates',
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
  'X-Customer-Id':'string',
  'X-Shop-Id':'string',
  'Accept':'application/json'

};

fetch('://staging.whiplashmerch.com/api/v2/orders/{id}/shipping_rates',
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
  'X-Customer-Id' => 'string',
  'X-Shop-Id' => 'string',
  'Accept' => 'application/json'
}

result = RestClient.get '://staging.whiplashmerch.com/api/v2/orders/{id}/shipping_rates', params: {
  }, headers: headers

p JSON.parse(result)
```

```python
import requests
headers = {
  'X-Customer-Id': 'string',
  'X-Shop-Id': 'string',
  'Accept': 'application/json'
}

r = requests.get('://staging.whiplashmerch.com/api/v2/orders/{id}/shipping_rates', params={

}, headers = headers)

print r.json()
```

```java
URL obj = new URL("://staging.whiplashmerch.com/api/v2/orders/{id}/shipping_rates");
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

`GET /api/v2/orders/{id}/shipping_rates`

*List shipping rates for an order*

List shipping rates for an order

### Parameters

Parameter|In|Type|Required|Description
---|---|---|---|---|
X-Customer-Id|header|string|false|The customer associated with this resource.
X-Shop-Id|header|string|false|The shop associated with this resource.
id|path|integer|true|No description


### Responses

Status|Meaning|Description
---|---|---|
200|[OK](https://tools.ietf.org/html/rfc7231#section-6.3.1)|List shipping rates for an order
401|[Unauthorized](https://tools.ietf.org/html/rfc7235#section-3.1)|No description
403|[Forbidden](https://tools.ietf.org/html/rfc7231#section-6.5.3)|No description

> Example responses

```json
{
  "id": 0,
  "customer_id": 0,
  "first_name": "string",
  "last_name": "string",
  "full_name": "string",
  "billing_company": "string",
  "billing_address_1": "string",
  "billing_address_2": "string",
  "billing_city": "string",
  "billing_state": "string",
  "billing_zip": "string",
  "billing_country": "string",
  "billing_phone": "string",
  "shipping_company": "string",
  "shipping_address_1": "string",
  "shipping_address_2": "string",
  "shipping_city": "string",
  "shipping_state": "string",
  "shipping_zip": "string",
  "shipping_country": "string",
  "shipping_phone": "string",
  "email": "string",
  "ship_actual_cost": 0,
  "shipped_on": "2017-06-19T15:15:48Z",
  "ship_notes": "string",
  "created_at": "2017-06-19T15:15:48Z",
  "updated_at": "2017-06-19T15:15:48Z",
  "shipping_name": "string",
  "shop_shipping_method_price": 0,
  "shipping_confirmation_sent": true,
  "status": 0,
  "previous_status": 0,
  "ship_3rdparty_cost": 0,
  "public_note": "string",
  "gift": true,
  "billed": true,
  "ship_3rdparty_account": "string",
  "ship_3rdparty_zip": "string",
  "ship_3rdparty_country": "string",
  "shop_shipping_method_text": "string",
  "order_batch_id": 0,
  "order_orig": "string",
  "days_in_transit": 0,
  "quote_id": 0,
  "shipping_country_iso2": "string",
  "insure": true,
  "require_signature": true,
  "req_insurance_value": 0,
  "warehouse_id": 0,
  "workable_at": "2017-06-19T15:15:48Z",
  "requested_address": "string",
  "address_verified": true,
  "address_message": "string",
  "return_city": "string",
  "return_state": "string",
  "return_country": "string",
  "return_zip": "string",
  "return_address_1": "string",
  "return_address_2": "string",
  "return_phone": "string",
  "return_email": "string",
  "level1_token": "string",
  "level2_token": "string",
  "return_time_limit": 0,
  "return_address_verified": true,
  "shipping_method_id": 0,
  "skip_street_date": true,
  "shop_warehouse_id": 0,
  "shop_shipping_method_currency": "string",
  "saturday_delivery": true,
  "shop_created_at": "2017-06-19T15:15:48Z",
  "shop_updated_at": "2017-06-19T15:15:48Z",
  "residential": true,
  "skip_address_verification": true,
  "due_at": "2017-06-19T15:15:48Z",
  "do_not_bill": true,
  "return_company": "string",
  "contains_alcohol": true,
  "require_adult_signature": true,
  "order_items": {
    "id": 0,
    "order_id": 0,
    "sku": "string",
    "description": "string",
    "quantity": 0,
    "price": 0,
    "created_at": "2017-06-19T15:15:48Z",
    "updated_at": "2017-06-19T15:15:48Z",
    "unshippable": true,
    "customer_id": 0,
    "item_id": 0,
    "available": true,
    "packed": 0,
    "packaging": true,
    "wholesale_cost": 0,
    "package_id": 0,
    "is_bundle": true,
    "retail_fee": 0,
    "promo": true,
    "quote_item_id": 0,
    "returnable": true,
    "currency": "string",
    "wholesale_fee": 0
  },
  "ship_method": "string",
  "status_name": "string"
}
```
```json
{
  "message": "string"
}
```
```json
{
  "message": "string"
}
```
<aside class="success">
This operation does not require authentication
</aside>

## getApiV2OrdersIdEvents

> Code samples

```shell
# You can also use wget
curl -X get ://staging.whiplashmerch.com/api/v2/orders/{id}/events \
  -H 'X-Customer-Id: string' \
  -H 'X-Shop-Id: string' \
  -H 'Accept: application/json'

```

```http
GET ://staging.whiplashmerch.com/api/v2/orders/{id}/events HTTP/1.1
Host: staging.whiplashmerch.com

Accept: application/json
X-Customer-Id: string
X-Shop-Id: string

```

```javascript
var headers = {
  'X-Customer-Id':'string',
  'X-Shop-Id':'string',
  'Accept':'application/json'

};

$.ajax({
  url: '://staging.whiplashmerch.com/api/v2/orders/{id}/events',
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
  'X-Customer-Id':'string',
  'X-Shop-Id':'string',
  'Accept':'application/json'

};

fetch('://staging.whiplashmerch.com/api/v2/orders/{id}/events',
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
  'X-Customer-Id' => 'string',
  'X-Shop-Id' => 'string',
  'Accept' => 'application/json'
}

result = RestClient.get '://staging.whiplashmerch.com/api/v2/orders/{id}/events', params: {
  }, headers: headers

p JSON.parse(result)
```

```python
import requests
headers = {
  'X-Customer-Id': 'string',
  'X-Shop-Id': 'string',
  'Accept': 'application/json'
}

r = requests.get('://staging.whiplashmerch.com/api/v2/orders/{id}/events', params={

}, headers = headers)

print r.json()
```

```java
URL obj = new URL("://staging.whiplashmerch.com/api/v2/orders/{id}/events");
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

`GET /api/v2/orders/{id}/events`

*Get the order history*

Get the order history

### Parameters

Parameter|In|Type|Required|Description
---|---|---|---|---|
X-Customer-Id|header|string|false|The customer associated with this resource.
X-Shop-Id|header|string|false|The shop associated with this resource.
id|path|integer|true|No description


### Responses

Status|Meaning|Description
---|---|---|
200|[OK](https://tools.ietf.org/html/rfc7231#section-6.3.1)|Get the order history
401|[Unauthorized](https://tools.ietf.org/html/rfc7235#section-3.1)|No description
403|[Forbidden](https://tools.ietf.org/html/rfc7231#section-6.5.3)|No description

> Example responses

```json
{
  "id": 0,
  "customer_id": 0,
  "first_name": "string",
  "last_name": "string",
  "full_name": "string",
  "billing_company": "string",
  "billing_address_1": "string",
  "billing_address_2": "string",
  "billing_city": "string",
  "billing_state": "string",
  "billing_zip": "string",
  "billing_country": "string",
  "billing_phone": "string",
  "shipping_company": "string",
  "shipping_address_1": "string",
  "shipping_address_2": "string",
  "shipping_city": "string",
  "shipping_state": "string",
  "shipping_zip": "string",
  "shipping_country": "string",
  "shipping_phone": "string",
  "email": "string",
  "ship_actual_cost": 0,
  "shipped_on": "2017-06-19T15:15:48Z",
  "ship_notes": "string",
  "created_at": "2017-06-19T15:15:48Z",
  "updated_at": "2017-06-19T15:15:48Z",
  "shipping_name": "string",
  "shop_shipping_method_price": 0,
  "shipping_confirmation_sent": true,
  "status": 0,
  "previous_status": 0,
  "ship_3rdparty_cost": 0,
  "public_note": "string",
  "gift": true,
  "billed": true,
  "ship_3rdparty_account": "string",
  "ship_3rdparty_zip": "string",
  "ship_3rdparty_country": "string",
  "shop_shipping_method_text": "string",
  "order_batch_id": 0,
  "order_orig": "string",
  "days_in_transit": 0,
  "quote_id": 0,
  "shipping_country_iso2": "string",
  "insure": true,
  "require_signature": true,
  "req_insurance_value": 0,
  "warehouse_id": 0,
  "workable_at": "2017-06-19T15:15:48Z",
  "requested_address": "string",
  "address_verified": true,
  "address_message": "string",
  "return_city": "string",
  "return_state": "string",
  "return_country": "string",
  "return_zip": "string",
  "return_address_1": "string",
  "return_address_2": "string",
  "return_phone": "string",
  "return_email": "string",
  "level1_token": "string",
  "level2_token": "string",
  "return_time_limit": 0,
  "return_address_verified": true,
  "shipping_method_id": 0,
  "skip_street_date": true,
  "shop_warehouse_id": 0,
  "shop_shipping_method_currency": "string",
  "saturday_delivery": true,
  "shop_created_at": "2017-06-19T15:15:48Z",
  "shop_updated_at": "2017-06-19T15:15:48Z",
  "residential": true,
  "skip_address_verification": true,
  "due_at": "2017-06-19T15:15:48Z",
  "do_not_bill": true,
  "return_company": "string",
  "contains_alcohol": true,
  "require_adult_signature": true,
  "order_items": {
    "id": 0,
    "order_id": 0,
    "sku": "string",
    "description": "string",
    "quantity": 0,
    "price": 0,
    "created_at": "2017-06-19T15:15:48Z",
    "updated_at": "2017-06-19T15:15:48Z",
    "unshippable": true,
    "customer_id": 0,
    "item_id": 0,
    "available": true,
    "packed": 0,
    "packaging": true,
    "wholesale_cost": 0,
    "package_id": 0,
    "is_bundle": true,
    "retail_fee": 0,
    "promo": true,
    "quote_item_id": 0,
    "returnable": true,
    "currency": "string",
    "wholesale_fee": 0
  },
  "ship_method": "string",
  "status_name": "string"
}
```
```json
{
  "message": "string"
}
```
```json
{
  "message": "string"
}
```
<aside class="success">
This operation does not require authentication
</aside>

## putApiV2OrdersIdCallAction

> Code samples

```shell
# You can also use wget
curl -X put ://staging.whiplashmerch.com/api/v2/orders/{id}/call/{action} \
  -H 'X-Customer-Id: string' \
  -H 'X-Shop-Id: string' \
  -H 'Content-Type: application/json' \
  -H 'Accept: application/json'

```

```http
PUT ://staging.whiplashmerch.com/api/v2/orders/{id}/call/{action} HTTP/1.1
Host: staging.whiplashmerch.com
Content-Type: application/json
Accept: application/json
X-Customer-Id: string
X-Shop-Id: string

```

```javascript
var headers = {
  'X-Customer-Id':'string',
  'X-Shop-Id':'string',
  'Content-Type':'application/json',
  'Accept':'application/json'

};

$.ajax({
  url: '://staging.whiplashmerch.com/api/v2/orders/{id}/call/{action}',
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
  'X-Customer-Id':'string',
  'X-Shop-Id':'string',
  'Content-Type':'application/json',
  'Accept':'application/json'

};

fetch('://staging.whiplashmerch.com/api/v2/orders/{id}/call/{action}',
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
  'X-Customer-Id' => 'string',
  'X-Shop-Id' => 'string',
  'Content-Type' => 'application/json',
  'Accept' => 'application/json'
}

result = RestClient.put '://staging.whiplashmerch.com/api/v2/orders/{id}/call/{action}', params: {
  }, headers: headers

p JSON.parse(result)
```

```python
import requests
headers = {
  'X-Customer-Id': 'string',
  'X-Shop-Id': 'string',
  'Content-Type': 'application/json',
  'Accept': 'application/json'
}

r = requests.put('://staging.whiplashmerch.com/api/v2/orders/{id}/call/{action}', params={

}, headers = headers)

print r.json()
```

```java
URL obj = new URL("://staging.whiplashmerch.com/api/v2/orders/{id}/call/{action}");
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

`PUT /api/v2/orders/{id}/call/{action}`

*Perform an action on an order*

Perform an action on an order

### Parameters

Parameter|In|Type|Required|Description
---|---|---|---|---|
X-Customer-Id|header|string|false|The customer associated with this resource.
X-Shop-Id|header|string|false|The shop associated with this resource.
async|formData|boolean|false|Process this action asynchronously
id|path|integer|true|No description
action|path|integer|true|No description


### Responses

Status|Meaning|Description
---|---|---|
200|[OK](https://tools.ietf.org/html/rfc7231#section-6.3.1)|Perform an action on an order
401|[Unauthorized](https://tools.ietf.org/html/rfc7235#section-3.1)|No description
403|[Forbidden](https://tools.ietf.org/html/rfc7231#section-6.5.3)|No description
405|[Method Not Allowed](https://tools.ietf.org/html/rfc7231#section-6.5.5)|No description
422|[Unprocessable Entity](https://tools.ietf.org/html/rfc2518#section-10.3)|No description

> Example responses

```json
{
  "id": 0,
  "customer_id": 0,
  "first_name": "string",
  "last_name": "string",
  "full_name": "string",
  "billing_company": "string",
  "billing_address_1": "string",
  "billing_address_2": "string",
  "billing_city": "string",
  "billing_state": "string",
  "billing_zip": "string",
  "billing_country": "string",
  "billing_phone": "string",
  "shipping_company": "string",
  "shipping_address_1": "string",
  "shipping_address_2": "string",
  "shipping_city": "string",
  "shipping_state": "string",
  "shipping_zip": "string",
  "shipping_country": "string",
  "shipping_phone": "string",
  "email": "string",
  "ship_actual_cost": 0,
  "shipped_on": "2017-06-19T15:15:48Z",
  "ship_notes": "string",
  "created_at": "2017-06-19T15:15:48Z",
  "updated_at": "2017-06-19T15:15:48Z",
  "shipping_name": "string",
  "shop_shipping_method_price": 0,
  "shipping_confirmation_sent": true,
  "status": 0,
  "previous_status": 0,
  "ship_3rdparty_cost": 0,
  "public_note": "string",
  "gift": true,
  "billed": true,
  "ship_3rdparty_account": "string",
  "ship_3rdparty_zip": "string",
  "ship_3rdparty_country": "string",
  "shop_shipping_method_text": "string",
  "order_batch_id": 0,
  "order_orig": "string",
  "days_in_transit": 0,
  "quote_id": 0,
  "shipping_country_iso2": "string",
  "insure": true,
  "require_signature": true,
  "req_insurance_value": 0,
  "warehouse_id": 0,
  "workable_at": "2017-06-19T15:15:48Z",
  "requested_address": "string",
  "address_verified": true,
  "address_message": "string",
  "return_city": "string",
  "return_state": "string",
  "return_country": "string",
  "return_zip": "string",
  "return_address_1": "string",
  "return_address_2": "string",
  "return_phone": "string",
  "return_email": "string",
  "level1_token": "string",
  "level2_token": "string",
  "return_time_limit": 0,
  "return_address_verified": true,
  "shipping_method_id": 0,
  "skip_street_date": true,
  "shop_warehouse_id": 0,
  "shop_shipping_method_currency": "string",
  "saturday_delivery": true,
  "shop_created_at": "2017-06-19T15:15:48Z",
  "shop_updated_at": "2017-06-19T15:15:48Z",
  "residential": true,
  "skip_address_verification": true,
  "due_at": "2017-06-19T15:15:48Z",
  "do_not_bill": true,
  "return_company": "string",
  "contains_alcohol": true,
  "require_adult_signature": true,
  "order_items": {
    "id": 0,
    "order_id": 0,
    "sku": "string",
    "description": "string",
    "quantity": 0,
    "price": 0,
    "created_at": "2017-06-19T15:15:48Z",
    "updated_at": "2017-06-19T15:15:48Z",
    "unshippable": true,
    "customer_id": 0,
    "item_id": 0,
    "available": true,
    "packed": 0,
    "packaging": true,
    "wholesale_cost": 0,
    "package_id": 0,
    "is_bundle": true,
    "retail_fee": 0,
    "promo": true,
    "quote_item_id": 0,
    "returnable": true,
    "currency": "string",
    "wholesale_fee": 0
  },
  "ship_method": "string",
  "status_name": "string"
}
```
```json
{
  "message": "string"
}
```
```json
{
  "message": "string"
}
```
```json
{
  "message": "string"
}
```
```json
{
  "message": "string"
}
```
<aside class="success">
This operation does not require authentication
</aside>

## postApiV2OrdersIdDuplicate

> Code samples

```shell
# You can also use wget
curl -X post ://staging.whiplashmerch.com/api/v2/orders/{id}/duplicate \
  -H 'X-Customer-Id: string' \
  -H 'X-Shop-Id: string' \
  -H 'Content-Type: application/json' \
  -H 'Accept: application/json'

```

```http
POST ://staging.whiplashmerch.com/api/v2/orders/{id}/duplicate HTTP/1.1
Host: staging.whiplashmerch.com
Content-Type: application/json
Accept: application/json
X-Customer-Id: string
X-Shop-Id: string

```

```javascript
var headers = {
  'X-Customer-Id':'string',
  'X-Shop-Id':'string',
  'Content-Type':'application/json',
  'Accept':'application/json'

};

$.ajax({
  url: '://staging.whiplashmerch.com/api/v2/orders/{id}/duplicate',
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
  'X-Customer-Id':'string',
  'X-Shop-Id':'string',
  'Content-Type':'application/json',
  'Accept':'application/json'

};

fetch('://staging.whiplashmerch.com/api/v2/orders/{id}/duplicate',
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
  'X-Customer-Id' => 'string',
  'X-Shop-Id' => 'string',
  'Content-Type' => 'application/json',
  'Accept' => 'application/json'
}

result = RestClient.post '://staging.whiplashmerch.com/api/v2/orders/{id}/duplicate', params: {
  }, headers: headers

p JSON.parse(result)
```

```python
import requests
headers = {
  'X-Customer-Id': 'string',
  'X-Shop-Id': 'string',
  'Content-Type': 'application/json',
  'Accept': 'application/json'
}

r = requests.post('://staging.whiplashmerch.com/api/v2/orders/{id}/duplicate', params={

}, headers = headers)

print r.json()
```

```java
URL obj = new URL("://staging.whiplashmerch.com/api/v2/orders/{id}/duplicate");
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

`POST /api/v2/orders/{id}/duplicate`

*Duplicate an order *

Duplicate an order 

### Parameters

Parameter|In|Type|Required|Description
---|---|---|---|---|
X-Customer-Id|header|string|false|The customer associated with this resource.
X-Shop-Id|header|string|false|The shop associated with this resource.
id|path|integer|true|No description


### Responses

Status|Meaning|Description
---|---|---|
201|[Created](https://tools.ietf.org/html/rfc7231#section-6.3.2)|Duplicate an order
401|[Unauthorized](https://tools.ietf.org/html/rfc7235#section-3.1)|No description
403|[Forbidden](https://tools.ietf.org/html/rfc7231#section-6.5.3)|No description
409|[Conflict](https://tools.ietf.org/html/rfc7231#section-6.5.8)|No description
422|[Unprocessable Entity](https://tools.ietf.org/html/rfc2518#section-10.3)|No description

> Example responses

```json
{
  "id": 0,
  "customer_id": 0,
  "first_name": "string",
  "last_name": "string",
  "full_name": "string",
  "billing_company": "string",
  "billing_address_1": "string",
  "billing_address_2": "string",
  "billing_city": "string",
  "billing_state": "string",
  "billing_zip": "string",
  "billing_country": "string",
  "billing_phone": "string",
  "shipping_company": "string",
  "shipping_address_1": "string",
  "shipping_address_2": "string",
  "shipping_city": "string",
  "shipping_state": "string",
  "shipping_zip": "string",
  "shipping_country": "string",
  "shipping_phone": "string",
  "email": "string",
  "ship_actual_cost": 0,
  "shipped_on": "2017-06-19T15:15:48Z",
  "ship_notes": "string",
  "created_at": "2017-06-19T15:15:48Z",
  "updated_at": "2017-06-19T15:15:48Z",
  "shipping_name": "string",
  "shop_shipping_method_price": 0,
  "shipping_confirmation_sent": true,
  "status": 0,
  "previous_status": 0,
  "ship_3rdparty_cost": 0,
  "public_note": "string",
  "gift": true,
  "billed": true,
  "ship_3rdparty_account": "string",
  "ship_3rdparty_zip": "string",
  "ship_3rdparty_country": "string",
  "shop_shipping_method_text": "string",
  "order_batch_id": 0,
  "order_orig": "string",
  "days_in_transit": 0,
  "quote_id": 0,
  "shipping_country_iso2": "string",
  "insure": true,
  "require_signature": true,
  "req_insurance_value": 0,
  "warehouse_id": 0,
  "workable_at": "2017-06-19T15:15:48Z",
  "requested_address": "string",
  "address_verified": true,
  "address_message": "string",
  "return_city": "string",
  "return_state": "string",
  "return_country": "string",
  "return_zip": "string",
  "return_address_1": "string",
  "return_address_2": "string",
  "return_phone": "string",
  "return_email": "string",
  "level1_token": "string",
  "level2_token": "string",
  "return_time_limit": 0,
  "return_address_verified": true,
  "shipping_method_id": 0,
  "skip_street_date": true,
  "shop_warehouse_id": 0,
  "shop_shipping_method_currency": "string",
  "saturday_delivery": true,
  "shop_created_at": "2017-06-19T15:15:48Z",
  "shop_updated_at": "2017-06-19T15:15:48Z",
  "residential": true,
  "skip_address_verification": true,
  "due_at": "2017-06-19T15:15:48Z",
  "do_not_bill": true,
  "return_company": "string",
  "contains_alcohol": true,
  "require_adult_signature": true,
  "order_items": {
    "id": 0,
    "order_id": 0,
    "sku": "string",
    "description": "string",
    "quantity": 0,
    "price": 0,
    "created_at": "2017-06-19T15:15:48Z",
    "updated_at": "2017-06-19T15:15:48Z",
    "unshippable": true,
    "customer_id": 0,
    "item_id": 0,
    "available": true,
    "packed": 0,
    "packaging": true,
    "wholesale_cost": 0,
    "package_id": 0,
    "is_bundle": true,
    "retail_fee": 0,
    "promo": true,
    "quote_item_id": 0,
    "returnable": true,
    "currency": "string",
    "wholesale_fee": 0
  },
  "ship_method": "string",
  "status_name": "string"
}
```
```json
{
  "message": "string"
}
```
```json
{
  "message": "string"
}
```
```json
{
  "message": "string"
}
```
```json
{
  "message": "string"
}
```
<aside class="success">
This operation does not require authentication
</aside>

## getApiV2OrdersOriginatorOriginatorId

> Code samples

```shell
# You can also use wget
curl -X get ://staging.whiplashmerch.com/api/v2/orders/originator/{originator_id} \
  -H 'X-Customer-Id: string' \
  -H 'X-Shop-Id: string' \
  -H 'Accept: application/json'

```

```http
GET ://staging.whiplashmerch.com/api/v2/orders/originator/{originator_id} HTTP/1.1
Host: staging.whiplashmerch.com

Accept: application/json
X-Customer-Id: string
X-Shop-Id: string

```

```javascript
var headers = {
  'X-Customer-Id':'string',
  'X-Shop-Id':'string',
  'Accept':'application/json'

};

$.ajax({
  url: '://staging.whiplashmerch.com/api/v2/orders/originator/{originator_id}',
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
  'X-Customer-Id':'string',
  'X-Shop-Id':'string',
  'Accept':'application/json'

};

fetch('://staging.whiplashmerch.com/api/v2/orders/originator/{originator_id}',
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
  'X-Customer-Id' => 'string',
  'X-Shop-Id' => 'string',
  'Accept' => 'application/json'
}

result = RestClient.get '://staging.whiplashmerch.com/api/v2/orders/originator/{originator_id}', params: {
  }, headers: headers

p JSON.parse(result)
```

```python
import requests
headers = {
  'X-Customer-Id': 'string',
  'X-Shop-Id': 'string',
  'Accept': 'application/json'
}

r = requests.get('://staging.whiplashmerch.com/api/v2/orders/originator/{originator_id}', params={

}, headers = headers)

print r.json()
```

```java
URL obj = new URL("://staging.whiplashmerch.com/api/v2/orders/originator/{originator_id}");
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

`GET /api/v2/orders/originator/{originator_id}`

*Get an order*

Get an order

### Parameters

Parameter|In|Type|Required|Description
---|---|---|---|---|
originator_id|path|integer|true|No description
X-Customer-Id|header|string|false|The customer associated with this resource.
X-Shop-Id|header|string|false|The shop associated with this resource.


### Responses

Status|Meaning|Description
---|---|---|
200|[OK](https://tools.ietf.org/html/rfc7231#section-6.3.1)|Get an order
401|[Unauthorized](https://tools.ietf.org/html/rfc7235#section-3.1)|No description
403|[Forbidden](https://tools.ietf.org/html/rfc7231#section-6.5.3)|No description

> Example responses

```json
{
  "id": 0,
  "customer_id": 0,
  "first_name": "string",
  "last_name": "string",
  "full_name": "string",
  "billing_company": "string",
  "billing_address_1": "string",
  "billing_address_2": "string",
  "billing_city": "string",
  "billing_state": "string",
  "billing_zip": "string",
  "billing_country": "string",
  "billing_phone": "string",
  "shipping_company": "string",
  "shipping_address_1": "string",
  "shipping_address_2": "string",
  "shipping_city": "string",
  "shipping_state": "string",
  "shipping_zip": "string",
  "shipping_country": "string",
  "shipping_phone": "string",
  "email": "string",
  "ship_actual_cost": 0,
  "shipped_on": "2017-06-19T15:15:48Z",
  "ship_notes": "string",
  "created_at": "2017-06-19T15:15:48Z",
  "updated_at": "2017-06-19T15:15:48Z",
  "shipping_name": "string",
  "shop_shipping_method_price": 0,
  "shipping_confirmation_sent": true,
  "status": 0,
  "previous_status": 0,
  "ship_3rdparty_cost": 0,
  "public_note": "string",
  "gift": true,
  "billed": true,
  "ship_3rdparty_account": "string",
  "ship_3rdparty_zip": "string",
  "ship_3rdparty_country": "string",
  "shop_shipping_method_text": "string",
  "order_batch_id": 0,
  "order_orig": "string",
  "days_in_transit": 0,
  "quote_id": 0,
  "shipping_country_iso2": "string",
  "insure": true,
  "require_signature": true,
  "req_insurance_value": 0,
  "warehouse_id": 0,
  "workable_at": "2017-06-19T15:15:48Z",
  "requested_address": "string",
  "address_verified": true,
  "address_message": "string",
  "return_city": "string",
  "return_state": "string",
  "return_country": "string",
  "return_zip": "string",
  "return_address_1": "string",
  "return_address_2": "string",
  "return_phone": "string",
  "return_email": "string",
  "level1_token": "string",
  "level2_token": "string",
  "return_time_limit": 0,
  "return_address_verified": true,
  "shipping_method_id": 0,
  "skip_street_date": true,
  "shop_warehouse_id": 0,
  "shop_shipping_method_currency": "string",
  "saturday_delivery": true,
  "shop_created_at": "2017-06-19T15:15:48Z",
  "shop_updated_at": "2017-06-19T15:15:48Z",
  "residential": true,
  "skip_address_verification": true,
  "due_at": "2017-06-19T15:15:48Z",
  "do_not_bill": true,
  "return_company": "string",
  "contains_alcohol": true,
  "require_adult_signature": true,
  "order_items": {
    "id": 0,
    "order_id": 0,
    "sku": "string",
    "description": "string",
    "quantity": 0,
    "price": 0,
    "created_at": "2017-06-19T15:15:48Z",
    "updated_at": "2017-06-19T15:15:48Z",
    "unshippable": true,
    "customer_id": 0,
    "item_id": 0,
    "available": true,
    "packed": 0,
    "packaging": true,
    "wholesale_cost": 0,
    "package_id": 0,
    "is_bundle": true,
    "retail_fee": 0,
    "promo": true,
    "quote_item_id": 0,
    "returnable": true,
    "currency": "string",
    "wholesale_fee": 0
  },
  "ship_method": "string",
  "status_name": "string"
}
```
```json
{
  "message": "string"
}
```
```json
{
  "message": "string"
}
```
<aside class="success">
This operation does not require authentication
</aside>

## putApiV2OrdersOriginatorOriginatorId

> Code samples

```shell
# You can also use wget
curl -X put ://staging.whiplashmerch.com/api/v2/orders/originator/{originator_id} \
  -H 'X-Customer-Id: string' \
  -H 'X-Shop-Id: string' \
  -H 'Content-Type: application/json' \
  -H 'Accept: application/json'

```

```http
PUT ://staging.whiplashmerch.com/api/v2/orders/originator/{originator_id} HTTP/1.1
Host: staging.whiplashmerch.com
Content-Type: application/json
Accept: application/json
X-Customer-Id: string
X-Shop-Id: string

```

```javascript
var headers = {
  'X-Customer-Id':'string',
  'X-Shop-Id':'string',
  'Content-Type':'application/json',
  'Accept':'application/json'

};

$.ajax({
  url: '://staging.whiplashmerch.com/api/v2/orders/originator/{originator_id}',
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
  'X-Customer-Id':'string',
  'X-Shop-Id':'string',
  'Content-Type':'application/json',
  'Accept':'application/json'

};

fetch('://staging.whiplashmerch.com/api/v2/orders/originator/{originator_id}',
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
  'X-Customer-Id' => 'string',
  'X-Shop-Id' => 'string',
  'Content-Type' => 'application/json',
  'Accept' => 'application/json'
}

result = RestClient.put '://staging.whiplashmerch.com/api/v2/orders/originator/{originator_id}', params: {
  }, headers: headers

p JSON.parse(result)
```

```python
import requests
headers = {
  'X-Customer-Id': 'string',
  'X-Shop-Id': 'string',
  'Content-Type': 'application/json',
  'Accept': 'application/json'
}

r = requests.put('://staging.whiplashmerch.com/api/v2/orders/originator/{originator_id}', params={

}, headers = headers)

print r.json()
```

```java
URL obj = new URL("://staging.whiplashmerch.com/api/v2/orders/originator/{originator_id}");
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

`PUT /api/v2/orders/originator/{originator_id}`

*Update an order*

Update an order

### Parameters

Parameter|In|Type|Required|Description
---|---|---|---|---|
X-Customer-Id|header|string|false|The customer associated with this resource.
X-Shop-Id|header|string|false|The shop associated with this resource.
first_name|formData|string|false|No description
last_name|formData|string|false|No description
full_name|formData|string|false|No description
billing_company|formData|string|false|No description
billing_address_1|formData|string|false|No description
billing_address_2|formData|string|false|No description
billing_city|formData|string|false|No description
billing_state|formData|string|false|No description
billing_zip|formData|string|false|No description
billing_country|formData|string|false|No description
billing_phone|formData|string|false|No description
shipping_company|formData|string|false|No description
shipping_address_1|formData|string|false|No description
shipping_address_2|formData|string|false|No description
shipping_city|formData|string|false|No description
shipping_state|formData|string|false|No description
shipping_zip|formData|string|false|No description
shipping_country|formData|string|false|No description
shipping_phone|formData|string|false|No description
email|formData|string|false|No description
ship_notes|formData|string|false|No description
shipping_name|formData|string|false|No description
shop_shipping_method_price|formData|number|false|No description
ship_3rdparty_cost|formData|number|false|No description
public_note|formData|string|false|No description
gift|formData|boolean|false|No description
ship_3rdparty_account|formData|string|false|No description
ship_3rdparty_zip|formData|string|false|No description
ship_3rdparty_country|formData|string|false|No description
shop_shipping_method_text|formData|string|false|No description
order_orig|formData|string|false|No description
days_in_transit|formData|integer|false|No description
shipping_country_iso2|formData|string|false|No description
insure|formData|boolean|false|No description
require_signature|formData|boolean|false|No description
req_insurance_value|formData|number|false|No description
requested_address|formData|string|false|No description
return_city|formData|string|false|No description
return_state|formData|string|false|No description
return_country|formData|string|false|No description
return_zip|formData|string|false|No description
return_address_1|formData|string|false|No description
return_address_2|formData|string|false|No description
return_phone|formData|string|false|No description
return_email|formData|string|false|No description
level1_token|formData|string|false|No description
level2_token|formData|string|false|No description
return_time_limit|formData|integer|false|No description
shipping_method_id|formData|integer|false|No description
skip_street_date|formData|boolean|false|No description
shop_warehouse_id|formData|integer|false|No description
shop_shipping_method_currency|formData|string|false|No description
saturday_delivery|formData|boolean|false|No description
shop_created_at|formData|string|false|No description
shop_updated_at|formData|string|false|No description
residential|formData|boolean|false|No description
skip_address_verification|formData|boolean|false|No description
due_at|formData|string|false|No description
do_not_bill|formData|boolean|false|No description
return_company|formData|string|false|No description
contains_alcohol|formData|boolean|false|No description
require_adult_signature|formData|boolean|false|No description
originator_id|path|integer|true|No description


### Responses

Status|Meaning|Description
---|---|---|
200|[OK](https://tools.ietf.org/html/rfc7231#section-6.3.1)|Update an order
401|[Unauthorized](https://tools.ietf.org/html/rfc7235#section-3.1)|No description
403|[Forbidden](https://tools.ietf.org/html/rfc7231#section-6.5.3)|No description
422|[Unprocessable Entity](https://tools.ietf.org/html/rfc2518#section-10.3)|No description

> Example responses

```json
{
  "id": 0,
  "customer_id": 0,
  "first_name": "string",
  "last_name": "string",
  "full_name": "string",
  "billing_company": "string",
  "billing_address_1": "string",
  "billing_address_2": "string",
  "billing_city": "string",
  "billing_state": "string",
  "billing_zip": "string",
  "billing_country": "string",
  "billing_phone": "string",
  "shipping_company": "string",
  "shipping_address_1": "string",
  "shipping_address_2": "string",
  "shipping_city": "string",
  "shipping_state": "string",
  "shipping_zip": "string",
  "shipping_country": "string",
  "shipping_phone": "string",
  "email": "string",
  "ship_actual_cost": 0,
  "shipped_on": "2017-06-19T15:15:48Z",
  "ship_notes": "string",
  "created_at": "2017-06-19T15:15:48Z",
  "updated_at": "2017-06-19T15:15:48Z",
  "shipping_name": "string",
  "shop_shipping_method_price": 0,
  "shipping_confirmation_sent": true,
  "status": 0,
  "previous_status": 0,
  "ship_3rdparty_cost": 0,
  "public_note": "string",
  "gift": true,
  "billed": true,
  "ship_3rdparty_account": "string",
  "ship_3rdparty_zip": "string",
  "ship_3rdparty_country": "string",
  "shop_shipping_method_text": "string",
  "order_batch_id": 0,
  "order_orig": "string",
  "days_in_transit": 0,
  "quote_id": 0,
  "shipping_country_iso2": "string",
  "insure": true,
  "require_signature": true,
  "req_insurance_value": 0,
  "warehouse_id": 0,
  "workable_at": "2017-06-19T15:15:48Z",
  "requested_address": "string",
  "address_verified": true,
  "address_message": "string",
  "return_city": "string",
  "return_state": "string",
  "return_country": "string",
  "return_zip": "string",
  "return_address_1": "string",
  "return_address_2": "string",
  "return_phone": "string",
  "return_email": "string",
  "level1_token": "string",
  "level2_token": "string",
  "return_time_limit": 0,
  "return_address_verified": true,
  "shipping_method_id": 0,
  "skip_street_date": true,
  "shop_warehouse_id": 0,
  "shop_shipping_method_currency": "string",
  "saturday_delivery": true,
  "shop_created_at": "2017-06-19T15:15:48Z",
  "shop_updated_at": "2017-06-19T15:15:48Z",
  "residential": true,
  "skip_address_verification": true,
  "due_at": "2017-06-19T15:15:48Z",
  "do_not_bill": true,
  "return_company": "string",
  "contains_alcohol": true,
  "require_adult_signature": true,
  "order_items": {
    "id": 0,
    "order_id": 0,
    "sku": "string",
    "description": "string",
    "quantity": 0,
    "price": 0,
    "created_at": "2017-06-19T15:15:48Z",
    "updated_at": "2017-06-19T15:15:48Z",
    "unshippable": true,
    "customer_id": 0,
    "item_id": 0,
    "available": true,
    "packed": 0,
    "packaging": true,
    "wholesale_cost": 0,
    "package_id": 0,
    "is_bundle": true,
    "retail_fee": 0,
    "promo": true,
    "quote_item_id": 0,
    "returnable": true,
    "currency": "string",
    "wholesale_fee": 0
  },
  "ship_method": "string",
  "status_name": "string"
}
```
```json
{
  "message": "string"
}
```
```json
{
  "message": "string"
}
```
```json
{
  "message": "string"
}
```
<aside class="success">
This operation does not require authentication
</aside>

## getApiV2OrdersIdMessages

> Code samples

```shell
# You can also use wget
curl -X get ://staging.whiplashmerch.com/api/v2/orders/{id}/messages \
  -H 'Accept: application/json'

```

```http
GET ://staging.whiplashmerch.com/api/v2/orders/{id}/messages HTTP/1.1
Host: staging.whiplashmerch.com

Accept: application/json

```

```javascript
var headers = {
  'Accept':'application/json'

};

$.ajax({
  url: '://staging.whiplashmerch.com/api/v2/orders/{id}/messages',
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
  'Accept':'application/json'

};

fetch('://staging.whiplashmerch.com/api/v2/orders/{id}/messages',
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
  'Accept' => 'application/json'
}

result = RestClient.get '://staging.whiplashmerch.com/api/v2/orders/{id}/messages', params: {
  }, headers: headers

p JSON.parse(result)
```

```python
import requests
headers = {
  'Accept': 'application/json'
}

r = requests.get('://staging.whiplashmerch.com/api/v2/orders/{id}/messages', params={

}, headers = headers)

print r.json()
```

```java
URL obj = new URL("://staging.whiplashmerch.com/api/v2/orders/{id}/messages");
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

`GET /api/v2/orders/{id}/messages`

*Get all messages for a(n) Order*

Get all messages for a(n) Order

### Parameters

Parameter|In|Type|Required|Description
---|---|---|---|---|
search|query|string|false|JSON search string like {"attribute_eq": "Term"}
page|query|integer|false|Page of results to fetch.
per_page|query|integer|false|Number of results to return per page.
id|path|integer|true|No description


### Responses

Status|Meaning|Description
---|---|---|
200|[OK](https://tools.ietf.org/html/rfc7231#section-6.3.1)|Get all messages for a(n) Order
401|[Unauthorized](https://tools.ietf.org/html/rfc7235#section-3.1)|No description
403|[Forbidden](https://tools.ietf.org/html/rfc7231#section-6.5.3)|No description

> Example responses

```json
{
  "id": 0,
  "customer_id": 0,
  "to": "string",
  "from": "string",
  "subject": "string",
  "content": "string",
  "contextuable_id": 0,
  "contextuable_type": "string",
  "created_at": "2017-06-19T15:15:48Z",
  "updated_at": "2017-06-19T15:15:48Z"
}
```
```json
{
  "message": "string"
}
```
```json
{
  "message": "string"
}
```
<aside class="success">
This operation does not require authentication
</aside>

## postApiV2OrdersIdMessages

> Code samples

```shell
# You can also use wget
curl -X post ://staging.whiplashmerch.com/api/v2/orders/{id}/messages \
  -H 'X-Customer-Id: string' \
  -H 'Content-Type: application/json' \
  -H 'Accept: application/json'

```

```http
POST ://staging.whiplashmerch.com/api/v2/orders/{id}/messages HTTP/1.1
Host: staging.whiplashmerch.com
Content-Type: application/json
Accept: application/json
X-Customer-Id: string

```

```javascript
var headers = {
  'X-Customer-Id':'string',
  'Content-Type':'application/json',
  'Accept':'application/json'

};

$.ajax({
  url: '://staging.whiplashmerch.com/api/v2/orders/{id}/messages',
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
  'X-Customer-Id':'string',
  'Content-Type':'application/json',
  'Accept':'application/json'

};

fetch('://staging.whiplashmerch.com/api/v2/orders/{id}/messages',
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
  'X-Customer-Id' => 'string',
  'Content-Type' => 'application/json',
  'Accept' => 'application/json'
}

result = RestClient.post '://staging.whiplashmerch.com/api/v2/orders/{id}/messages', params: {
  }, headers: headers

p JSON.parse(result)
```

```python
import requests
headers = {
  'X-Customer-Id': 'string',
  'Content-Type': 'application/json',
  'Accept': 'application/json'
}

r = requests.post('://staging.whiplashmerch.com/api/v2/orders/{id}/messages', params={

}, headers = headers)

print r.json()
```

```java
URL obj = new URL("://staging.whiplashmerch.com/api/v2/orders/{id}/messages");
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

`POST /api/v2/orders/{id}/messages`

*Create a messages for a(n) Order*

Create a messages for a(n) Order

### Parameters

Parameter|In|Type|Required|Description
---|---|---|---|---|
X-Customer-Id|header|string|false|The customer associated with this resource.
to|formData|string|true|No description
from|formData|string|true|No description
subject|formData|string|true|No description
content|formData|string|true|No description
id|path|integer|true|No description


### Responses

Status|Meaning|Description
---|---|---|
201|[Created](https://tools.ietf.org/html/rfc7231#section-6.3.2)|Create a messages for a(n) Order
401|[Unauthorized](https://tools.ietf.org/html/rfc7235#section-3.1)|No description
403|[Forbidden](https://tools.ietf.org/html/rfc7231#section-6.5.3)|No description
409|[Conflict](https://tools.ietf.org/html/rfc7231#section-6.5.8)|No description
422|[Unprocessable Entity](https://tools.ietf.org/html/rfc2518#section-10.3)|No description

> Example responses

```json
{
  "id": 0,
  "customer_id": 0,
  "to": "string",
  "from": "string",
  "subject": "string",
  "content": "string",
  "contextuable_id": 0,
  "contextuable_type": "string",
  "created_at": "2017-06-19T15:15:48Z",
  "updated_at": "2017-06-19T15:15:48Z"
}
```
```json
{
  "message": "string"
}
```
```json
{
  "message": "string"
}
```
```json
{
  "message": "string"
}
```
```json
{
  "message": "string"
}
```
<aside class="success">
This operation does not require authentication
</aside>

## getApiV2OrdersIdMessagesCount

> Code samples

```shell
# You can also use wget
curl -X get ://staging.whiplashmerch.com/api/v2/orders/{id}/messages/count \
  -H 'Accept: application/json'

```

```http
GET ://staging.whiplashmerch.com/api/v2/orders/{id}/messages/count HTTP/1.1
Host: staging.whiplashmerch.com

Accept: application/json

```

```javascript
var headers = {
  'Accept':'application/json'

};

$.ajax({
  url: '://staging.whiplashmerch.com/api/v2/orders/{id}/messages/count',
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
  'Accept':'application/json'

};

fetch('://staging.whiplashmerch.com/api/v2/orders/{id}/messages/count',
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
  'Accept' => 'application/json'
}

result = RestClient.get '://staging.whiplashmerch.com/api/v2/orders/{id}/messages/count', params: {
  }, headers: headers

p JSON.parse(result)
```

```python
import requests
headers = {
  'Accept': 'application/json'
}

r = requests.get('://staging.whiplashmerch.com/api/v2/orders/{id}/messages/count', params={

}, headers = headers)

print r.json()
```

```java
URL obj = new URL("://staging.whiplashmerch.com/api/v2/orders/{id}/messages/count");
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

`GET /api/v2/orders/{id}/messages/count`

*Returns count of messages for a(n) Order*

Returns count of messages for a(n) Order

### Parameters

Parameter|In|Type|Required|Description
---|---|---|---|---|
search|query|string|false|JSON search string like {"attribute_eq": "Term"}
id|path|integer|true|No description


### Responses

Status|Meaning|Description
---|---|---|
200|[OK](https://tools.ietf.org/html/rfc7231#section-6.3.1)|Returns count of messages for a(n) Order
401|[Unauthorized](https://tools.ietf.org/html/rfc7235#section-3.1)|No description
403|[Forbidden](https://tools.ietf.org/html/rfc7231#section-6.5.3)|No description

> Example responses

```json
{
  "id": 0,
  "customer_id": 0,
  "to": "string",
  "from": "string",
  "subject": "string",
  "content": "string",
  "contextuable_id": 0,
  "contextuable_type": "string",
  "created_at": "2017-06-19T15:15:48Z",
  "updated_at": "2017-06-19T15:15:48Z"
}
```
```json
{
  "message": "string"
}
```
```json
{
  "message": "string"
}
```
<aside class="success">
This operation does not require authentication
</aside>

# order_items

Operations about order_items

## getApiV2OrderItemsIdOriginator

> Code samples

```shell
# You can also use wget
curl -X get ://staging.whiplashmerch.com/api/v2/order_items/{id}/originator \
  -H 'Accept: application/json'

```

```http
GET ://staging.whiplashmerch.com/api/v2/order_items/{id}/originator HTTP/1.1
Host: staging.whiplashmerch.com

Accept: application/json

```

```javascript
var headers = {
  'Accept':'application/json'

};

$.ajax({
  url: '://staging.whiplashmerch.com/api/v2/order_items/{id}/originator',
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
  'Accept':'application/json'

};

fetch('://staging.whiplashmerch.com/api/v2/order_items/{id}/originator',
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
  'Accept' => 'application/json'
}

result = RestClient.get '://staging.whiplashmerch.com/api/v2/order_items/{id}/originator', params: {
  }, headers: headers

p JSON.parse(result)
```

```python
import requests
headers = {
  'Accept': 'application/json'
}

r = requests.get('://staging.whiplashmerch.com/api/v2/order_items/{id}/originator', params={

}, headers = headers)

print r.json()
```

```java
URL obj = new URL("://staging.whiplashmerch.com/api/v2/order_items/{id}/originator");
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

`GET /api/v2/order_items/{id}/originator`

*Get the originator for a(n) OrderItem*

Get the originator for a(n) OrderItem

### Parameters

Parameter|In|Type|Required|Description
---|---|---|---|---|
id|path|integer|true|No description


### Responses

Status|Meaning|Description
---|---|---|
200|[OK](https://tools.ietf.org/html/rfc7231#section-6.3.1)|Get the originator for a(n) OrderItem
401|[Unauthorized](https://tools.ietf.org/html/rfc7235#section-3.1)|No description
403|[Forbidden](https://tools.ietf.org/html/rfc7231#section-6.5.3)|No description

> Example responses

```json
{
  "id": 0,
  "originated_id": 0,
  "originated_type": "string",
  "shop_id": 0,
  "provider": "string",
  "original_id": "string",
  "group_id": "string",
  "address_id": "string",
  "active": true,
  "integration_id": 0,
  "last_notified_at": "2017-06-19T15:15:48Z",
  "last_notification_status": "string",
  "distinct_originator_key": "string",
  "created_at": "2017-06-19T15:15:48Z",
  "updated_at": "2017-06-19T15:15:48Z"
}
```
```json
{
  "message": "string"
}
```
```json
{
  "message": "string"
}
```
<aside class="success">
This operation does not require authentication
</aside>

## getApiV2OrderItemsId

> Code samples

```shell
# You can also use wget
curl -X get ://staging.whiplashmerch.com/api/v2/order_items/{id} \
  -H 'Accept: application/json'

```

```http
GET ://staging.whiplashmerch.com/api/v2/order_items/{id} HTTP/1.1
Host: staging.whiplashmerch.com

Accept: application/json

```

```javascript
var headers = {
  'Accept':'application/json'

};

$.ajax({
  url: '://staging.whiplashmerch.com/api/v2/order_items/{id}',
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
  'Accept':'application/json'

};

fetch('://staging.whiplashmerch.com/api/v2/order_items/{id}',
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
  'Accept' => 'application/json'
}

result = RestClient.get '://staging.whiplashmerch.com/api/v2/order_items/{id}', params: {
  }, headers: headers

p JSON.parse(result)
```

```python
import requests
headers = {
  'Accept': 'application/json'
}

r = requests.get('://staging.whiplashmerch.com/api/v2/order_items/{id}', params={

}, headers = headers)

print r.json()
```

```java
URL obj = new URL("://staging.whiplashmerch.com/api/v2/order_items/{id}");
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

`GET /api/v2/order_items/{id}`

*Get an order item*

Get an order item

### Parameters

Parameter|In|Type|Required|Description
---|---|---|---|---|
page|query|integer|false|Page of results to fetch.
per_page|query|integer|false|Number of results to return per page.
id|path|integer|true|No description


### Responses

Status|Meaning|Description
---|---|---|
200|[OK](https://tools.ietf.org/html/rfc7231#section-6.3.1)|Get an order item
401|[Unauthorized](https://tools.ietf.org/html/rfc7235#section-3.1)|No description
403|[Forbidden](https://tools.ietf.org/html/rfc7231#section-6.5.3)|No description

> Example responses

```json
{
  "id": 0,
  "order_id": 0,
  "sku": "string",
  "description": "string",
  "quantity": 0,
  "price": 0,
  "created_at": "2017-06-19T15:15:48Z",
  "updated_at": "2017-06-19T15:15:48Z",
  "unshippable": true,
  "customer_id": 0,
  "item_id": 0,
  "available": true,
  "packed": 0,
  "packaging": true,
  "wholesale_cost": 0,
  "package_id": 0,
  "is_bundle": true,
  "retail_fee": 0,
  "promo": true,
  "quote_item_id": 0,
  "returnable": true,
  "currency": "string",
  "wholesale_fee": 0
}
```
```json
{
  "message": "string"
}
```
```json
{
  "message": "string"
}
```
<aside class="success">
This operation does not require authentication
</aside>

## putApiV2OrderItemsId

> Code samples

```shell
# You can also use wget
curl -X put ://staging.whiplashmerch.com/api/v2/order_items/{id} \
  -H 'Content-Type: application/json' \
  -H 'Accept: application/json'

```

```http
PUT ://staging.whiplashmerch.com/api/v2/order_items/{id} HTTP/1.1
Host: staging.whiplashmerch.com
Content-Type: application/json
Accept: application/json

```

```javascript
var headers = {
  'Content-Type':'application/json',
  'Accept':'application/json'

};

$.ajax({
  url: '://staging.whiplashmerch.com/api/v2/order_items/{id}',
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
  'Content-Type':'application/json',
  'Accept':'application/json'

};

fetch('://staging.whiplashmerch.com/api/v2/order_items/{id}',
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
  'Content-Type' => 'application/json',
  'Accept' => 'application/json'
}

result = RestClient.put '://staging.whiplashmerch.com/api/v2/order_items/{id}', params: {
  }, headers: headers

p JSON.parse(result)
```

```python
import requests
headers = {
  'Content-Type': 'application/json',
  'Accept': 'application/json'
}

r = requests.put('://staging.whiplashmerch.com/api/v2/order_items/{id}', params={

}, headers = headers)

print r.json()
```

```java
URL obj = new URL("://staging.whiplashmerch.com/api/v2/order_items/{id}");
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

`PUT /api/v2/order_items/{id}`

*Update an order item*

Update an order item

### Parameters

Parameter|In|Type|Required|Description
---|---|---|---|---|
order_id|formData|integer|false|No description
sku|formData|string|false|the SKU of this item
description|formData|string|false|description of this item
quantity|formData|integer|false|number of this item in Order
price|formData|number|false|price of this item
unshippable|formData|boolean|false|is this item unshippable?
customer_id|formData|integer|false|No description
item_id|formData|integer|false|No description
available|formData|boolean|false|is this item available?
packed|formData|integer|false|number of items packed
packaging|formData|boolean|false|is this item packaging?
wholesale_cost|formData|number|false|wholesale cost of the item
package_id|formData|integer|false|No description
is_bundle|formData|boolean|false|is this item a bundle?
retail_fee|formData|number|false|retail fee of this item
promo|formData|boolean|false|is this item a promo?
quote_item_id|formData|integer|false|No description
returnable|formData|boolean|false|is this item returnable?
currency|formData|string|false|currency code for this item
wholesale_fee|formData|number|false|wholesale fee of this item
id|path|integer|true|No description


### Responses

Status|Meaning|Description
---|---|---|
200|[OK](https://tools.ietf.org/html/rfc7231#section-6.3.1)|Update an order item
401|[Unauthorized](https://tools.ietf.org/html/rfc7235#section-3.1)|No description
403|[Forbidden](https://tools.ietf.org/html/rfc7231#section-6.5.3)|No description
422|[Unprocessable Entity](https://tools.ietf.org/html/rfc2518#section-10.3)|No description

> Example responses

```json
{
  "id": 0,
  "order_id": 0,
  "sku": "string",
  "description": "string",
  "quantity": 0,
  "price": 0,
  "created_at": "2017-06-19T15:15:48Z",
  "updated_at": "2017-06-19T15:15:48Z",
  "unshippable": true,
  "customer_id": 0,
  "item_id": 0,
  "available": true,
  "packed": 0,
  "packaging": true,
  "wholesale_cost": 0,
  "package_id": 0,
  "is_bundle": true,
  "retail_fee": 0,
  "promo": true,
  "quote_item_id": 0,
  "returnable": true,
  "currency": "string",
  "wholesale_fee": 0
}
```
```json
{
  "message": "string"
}
```
```json
{
  "message": "string"
}
```
```json
{
  "message": "string"
}
```
<aside class="success">
This operation does not require authentication
</aside>

## deleteApiV2OrderItemsId

> Code samples

```shell
# You can also use wget
curl -X delete ://staging.whiplashmerch.com/api/v2/order_items/{id} \
  -H 'Accept: application/json'

```

```http
DELETE ://staging.whiplashmerch.com/api/v2/order_items/{id} HTTP/1.1
Host: staging.whiplashmerch.com

Accept: application/json

```

```javascript
var headers = {
  'Accept':'application/json'

};

$.ajax({
  url: '://staging.whiplashmerch.com/api/v2/order_items/{id}',
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
  'Accept':'application/json'

};

fetch('://staging.whiplashmerch.com/api/v2/order_items/{id}',
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
  'Accept' => 'application/json'
}

result = RestClient.delete '://staging.whiplashmerch.com/api/v2/order_items/{id}', params: {
  }, headers: headers

p JSON.parse(result)
```

```python
import requests
headers = {
  'Accept': 'application/json'
}

r = requests.delete('://staging.whiplashmerch.com/api/v2/order_items/{id}', params={

}, headers = headers)

print r.json()
```

```java
URL obj = new URL("://staging.whiplashmerch.com/api/v2/order_items/{id}");
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

`DELETE /api/v2/order_items/{id}`

*Destroy an order item*

Destroy an order item

### Parameters

Parameter|In|Type|Required|Description
---|---|---|---|---|
id|path|integer|true|No description


### Responses

Status|Meaning|Description
---|---|---|
200|[OK](https://tools.ietf.org/html/rfc7231#section-6.3.1)|Destroy an order item
401|[Unauthorized](https://tools.ietf.org/html/rfc7235#section-3.1)|No description
403|[Forbidden](https://tools.ietf.org/html/rfc7231#section-6.5.3)|No description
422|[Unprocessable Entity](https://tools.ietf.org/html/rfc2518#section-10.3)|No description

> Example responses

```json
{
  "id": 0,
  "order_id": 0,
  "sku": "string",
  "description": "string",
  "quantity": 0,
  "price": 0,
  "created_at": "2017-06-19T15:15:48Z",
  "updated_at": "2017-06-19T15:15:48Z",
  "unshippable": true,
  "customer_id": 0,
  "item_id": 0,
  "available": true,
  "packed": 0,
  "packaging": true,
  "wholesale_cost": 0,
  "package_id": 0,
  "is_bundle": true,
  "retail_fee": 0,
  "promo": true,
  "quote_item_id": 0,
  "returnable": true,
  "currency": "string",
  "wholesale_fee": 0
}
```
```json
{
  "message": "string"
}
```
```json
{
  "message": "string"
}
```
```json
{
  "message": "string"
}
```
<aside class="success">
This operation does not require authentication
</aside>

## postApiV2OrderItems

> Code samples

```shell
# You can also use wget
curl -X post ://staging.whiplashmerch.com/api/v2/order_items \
  -H 'Content-Type: application/json' \
  -H 'Accept: application/json'

```

```http
POST ://staging.whiplashmerch.com/api/v2/order_items HTTP/1.1
Host: staging.whiplashmerch.com
Content-Type: application/json
Accept: application/json

```

```javascript
var headers = {
  'Content-Type':'application/json',
  'Accept':'application/json'

};

$.ajax({
  url: '://staging.whiplashmerch.com/api/v2/order_items',
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
  'Content-Type':'application/json',
  'Accept':'application/json'

};

fetch('://staging.whiplashmerch.com/api/v2/order_items',
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
  'Content-Type' => 'application/json',
  'Accept' => 'application/json'
}

result = RestClient.post '://staging.whiplashmerch.com/api/v2/order_items', params: {
  }, headers: headers

p JSON.parse(result)
```

```python
import requests
headers = {
  'Content-Type': 'application/json',
  'Accept': 'application/json'
}

r = requests.post('://staging.whiplashmerch.com/api/v2/order_items', params={

}, headers = headers)

print r.json()
```

```java
URL obj = new URL("://staging.whiplashmerch.com/api/v2/order_items");
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

`POST /api/v2/order_items`

*Create an order item*

Create an order item

### Parameters

Parameter|In|Type|Required|Description
---|---|---|---|---|
order_id|formData|integer|false|No description
item_id|formData|integer|false|No description
sku|formData|string|false|the SKU of this item
description|formData|string|false|description of this item
quantity|formData|integer|false|number of this item in Order
price|formData|number|false|price of this item
unshippable|formData|boolean|false|is this item unshippable?
customer_id|formData|integer|false|No description
available|formData|boolean|false|is this item available?
packed|formData|integer|false|number of items packed
packaging|formData|boolean|false|is this item packaging?
wholesale_cost|formData|number|false|wholesale cost of the item
package_id|formData|integer|false|No description
is_bundle|formData|boolean|false|is this item a bundle?
retail_fee|formData|number|false|retail fee of this item
promo|formData|boolean|false|is this item a promo?
quote_item_id|formData|integer|false|No description
returnable|formData|boolean|false|is this item returnable?
currency|formData|string|false|currency code for this item
wholesale_fee|formData|number|false|wholesale fee of this item


### Responses

Status|Meaning|Description
---|---|---|
201|[Created](https://tools.ietf.org/html/rfc7231#section-6.3.2)|Create an order item
401|[Unauthorized](https://tools.ietf.org/html/rfc7235#section-3.1)|No description
403|[Forbidden](https://tools.ietf.org/html/rfc7231#section-6.5.3)|No description
409|[Conflict](https://tools.ietf.org/html/rfc7231#section-6.5.8)|No description
422|[Unprocessable Entity](https://tools.ietf.org/html/rfc2518#section-10.3)|No description

> Example responses

```json
{
  "id": 0,
  "order_id": 0,
  "sku": "string",
  "description": "string",
  "quantity": 0,
  "price": 0,
  "created_at": "2017-06-19T15:15:48Z",
  "updated_at": "2017-06-19T15:15:48Z",
  "unshippable": true,
  "customer_id": 0,
  "item_id": 0,
  "available": true,
  "packed": 0,
  "packaging": true,
  "wholesale_cost": 0,
  "package_id": 0,
  "is_bundle": true,
  "retail_fee": 0,
  "promo": true,
  "quote_item_id": 0,
  "returnable": true,
  "currency": "string",
  "wholesale_fee": 0
}
```
```json
{
  "message": "string"
}
```
```json
{
  "message": "string"
}
```
```json
{
  "message": "string"
}
```
```json
{
  "message": "string"
}
```
<aside class="success">
This operation does not require authentication
</aside>

## getApiV2OrderItemsIdSeparate

> Code samples

```shell
# You can also use wget
curl -X get ://staging.whiplashmerch.com/api/v2/order_items/{id}/separate \
  -H 'Accept: application/json'

```

```http
GET ://staging.whiplashmerch.com/api/v2/order_items/{id}/separate HTTP/1.1
Host: staging.whiplashmerch.com

Accept: application/json

```

```javascript
var headers = {
  'Accept':'application/json'

};

$.ajax({
  url: '://staging.whiplashmerch.com/api/v2/order_items/{id}/separate',
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
  'Accept':'application/json'

};

fetch('://staging.whiplashmerch.com/api/v2/order_items/{id}/separate',
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
  'Accept' => 'application/json'
}

result = RestClient.get '://staging.whiplashmerch.com/api/v2/order_items/{id}/separate', params: {
  }, headers: headers

p JSON.parse(result)
```

```python
import requests
headers = {
  'Accept': 'application/json'
}

r = requests.get('://staging.whiplashmerch.com/api/v2/order_items/{id}/separate', params={

}, headers = headers)

print r.json()
```

```java
URL obj = new URL("://staging.whiplashmerch.com/api/v2/order_items/{id}/separate");
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

`GET /api/v2/order_items/{id}/separate`

*Separate an order item*

Separate an order item

### Parameters

Parameter|In|Type|Required|Description
---|---|---|---|---|
id|path|integer|true|No description


### Responses

Status|Meaning|Description
---|---|---|
200|[OK](https://tools.ietf.org/html/rfc7231#section-6.3.1)|Separate an order item
401|[Unauthorized](https://tools.ietf.org/html/rfc7235#section-3.1)|No description
403|[Forbidden](https://tools.ietf.org/html/rfc7231#section-6.5.3)|No description

> Example responses

```json
{
  "id": 0,
  "order_id": 0,
  "sku": "string",
  "description": "string",
  "quantity": 0,
  "price": 0,
  "created_at": "2017-06-19T15:15:48Z",
  "updated_at": "2017-06-19T15:15:48Z",
  "unshippable": true,
  "customer_id": 0,
  "item_id": 0,
  "available": true,
  "packed": 0,
  "packaging": true,
  "wholesale_cost": 0,
  "package_id": 0,
  "is_bundle": true,
  "retail_fee": 0,
  "promo": true,
  "quote_item_id": 0,
  "returnable": true,
  "currency": "string",
  "wholesale_fee": 0
}
```
```json
{
  "message": "string"
}
```
```json
{
  "message": "string"
}
```
<aside class="success">
This operation does not require authentication
</aside>

# items

Operations about items

## getApiV2ItemsIdOriginators

> Code samples

```shell
# You can also use wget
curl -X get ://staging.whiplashmerch.com/api/v2/items/{id}/originators \
  -H 'Accept: application/json'

```

```http
GET ://staging.whiplashmerch.com/api/v2/items/{id}/originators HTTP/1.1
Host: staging.whiplashmerch.com

Accept: application/json

```

```javascript
var headers = {
  'Accept':'application/json'

};

$.ajax({
  url: '://staging.whiplashmerch.com/api/v2/items/{id}/originators',
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
  'Accept':'application/json'

};

fetch('://staging.whiplashmerch.com/api/v2/items/{id}/originators',
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
  'Accept' => 'application/json'
}

result = RestClient.get '://staging.whiplashmerch.com/api/v2/items/{id}/originators', params: {
  }, headers: headers

p JSON.parse(result)
```

```python
import requests
headers = {
  'Accept': 'application/json'
}

r = requests.get('://staging.whiplashmerch.com/api/v2/items/{id}/originators', params={

}, headers = headers)

print r.json()
```

```java
URL obj = new URL("://staging.whiplashmerch.com/api/v2/items/{id}/originators");
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

`GET /api/v2/items/{id}/originators`

*Get the originators for a(n) Item*

Get the originators for a(n) Item

### Parameters

Parameter|In|Type|Required|Description
---|---|---|---|---|
search|query|string|false|JSON search string like {"attribute_eq": "Term"}
page|query|integer|false|Page of results to fetch.
per_page|query|integer|false|Number of results to return per page.
id|path|integer|true|No description


### Responses

Status|Meaning|Description
---|---|---|
200|[OK](https://tools.ietf.org/html/rfc7231#section-6.3.1)|Get the originators for a(n) Item
401|[Unauthorized](https://tools.ietf.org/html/rfc7235#section-3.1)|No description
403|[Forbidden](https://tools.ietf.org/html/rfc7231#section-6.5.3)|No description

> Example responses

```json
{
  "id": 0,
  "originated_id": 0,
  "originated_type": "string",
  "shop_id": 0,
  "provider": "string",
  "original_id": "string",
  "group_id": "string",
  "address_id": "string",
  "active": true,
  "integration_id": 0,
  "last_notified_at": "2017-06-19T15:15:48Z",
  "last_notification_status": "string",
  "distinct_originator_key": "string",
  "created_at": "2017-06-19T15:15:48Z",
  "updated_at": "2017-06-19T15:15:48Z"
}
```
```json
{
  "message": "string"
}
```
```json
{
  "message": "string"
}
```
<aside class="success">
This operation does not require authentication
</aside>

## postApiV2ItemsIdOriginators

> Code samples

```shell
# You can also use wget
curl -X post ://staging.whiplashmerch.com/api/v2/items/{id}/originators \
  -H 'X-Shop-Id: string' \
  -H 'Content-Type: application/json' \
  -H 'Accept: application/json'

```

```http
POST ://staging.whiplashmerch.com/api/v2/items/{id}/originators HTTP/1.1
Host: staging.whiplashmerch.com
Content-Type: application/json
Accept: application/json
X-Shop-Id: string

```

```javascript
var headers = {
  'X-Shop-Id':'string',
  'Content-Type':'application/json',
  'Accept':'application/json'

};

$.ajax({
  url: '://staging.whiplashmerch.com/api/v2/items/{id}/originators',
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
  'X-Shop-Id':'string',
  'Content-Type':'application/json',
  'Accept':'application/json'

};

fetch('://staging.whiplashmerch.com/api/v2/items/{id}/originators',
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
  'X-Shop-Id' => 'string',
  'Content-Type' => 'application/json',
  'Accept' => 'application/json'
}

result = RestClient.post '://staging.whiplashmerch.com/api/v2/items/{id}/originators', params: {
  }, headers: headers

p JSON.parse(result)
```

```python
import requests
headers = {
  'X-Shop-Id': 'string',
  'Content-Type': 'application/json',
  'Accept': 'application/json'
}

r = requests.post('://staging.whiplashmerch.com/api/v2/items/{id}/originators', params={

}, headers = headers)

print r.json()
```

```java
URL obj = new URL("://staging.whiplashmerch.com/api/v2/items/{id}/originators");
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

`POST /api/v2/items/{id}/originators`

*Create a new Item originator*

Create a new Item originator

### Parameters

Parameter|In|Type|Required|Description
---|---|---|---|---|
X-Shop-Id|header|string|false|The shop associated with this resource.
type|formData|string|false|No description
String|formData|string|false|No description
desc|formData|string|false|No description
the originator original id (from the provider)|formData|string|false|No description
the originator group id|formData|string|false|No description
id|path|integer|true|No description


### Responses

Status|Meaning|Description
---|---|---|
201|[Created](https://tools.ietf.org/html/rfc7231#section-6.3.2)|Create a new Item originator
|Unknown|No description

> Example responses

```json
{
  "id": 0,
  "originated_id": 0,
  "originated_type": "string",
  "shop_id": 0,
  "provider": "string",
  "original_id": "string",
  "group_id": "string",
  "address_id": "string",
  "active": true,
  "integration_id": 0,
  "last_notified_at": "2017-06-19T15:15:48Z",
  "last_notification_status": "string",
  "distinct_originator_key": "string",
  "created_at": "2017-06-19T15:15:48Z",
  "updated_at": "2017-06-19T15:15:48Z"
}
```
```json
{
  "message": "string"
}
```
<aside class="success">
This operation does not require authentication
</aside>

## getApiV2ItemsId

> Code samples

```shell
# You can also use wget
curl -X get ://staging.whiplashmerch.com/api/v2/items/{id} \
  -H 'X-Customer-Id: string' \
  -H 'X-Shop-Id: string' \
  -H 'Accept: application/json'

```

```http
GET ://staging.whiplashmerch.com/api/v2/items/{id} HTTP/1.1
Host: staging.whiplashmerch.com

Accept: application/json
X-Customer-Id: string
X-Shop-Id: string

```

```javascript
var headers = {
  'X-Customer-Id':'string',
  'X-Shop-Id':'string',
  'Accept':'application/json'

};

$.ajax({
  url: '://staging.whiplashmerch.com/api/v2/items/{id}',
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
  'X-Customer-Id':'string',
  'X-Shop-Id':'string',
  'Accept':'application/json'

};

fetch('://staging.whiplashmerch.com/api/v2/items/{id}',
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
  'X-Customer-Id' => 'string',
  'X-Shop-Id' => 'string',
  'Accept' => 'application/json'
}

result = RestClient.get '://staging.whiplashmerch.com/api/v2/items/{id}', params: {
  }, headers: headers

p JSON.parse(result)
```

```python
import requests
headers = {
  'X-Customer-Id': 'string',
  'X-Shop-Id': 'string',
  'Accept': 'application/json'
}

r = requests.get('://staging.whiplashmerch.com/api/v2/items/{id}', params={

}, headers = headers)

print r.json()
```

```java
URL obj = new URL("://staging.whiplashmerch.com/api/v2/items/{id}");
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

`GET /api/v2/items/{id}`

*Get an item*

Get an item

### Parameters

Parameter|In|Type|Required|Description
---|---|---|---|---|
id|path|integer|true|No description
X-Customer-Id|header|string|false|The customer associated with this resource.
X-Shop-Id|header|string|false|The shop associated with this resource.


### Responses

Status|Meaning|Description
---|---|---|
200|[OK](https://tools.ietf.org/html/rfc7231#section-6.3.1)|Get an item
401|[Unauthorized](https://tools.ietf.org/html/rfc7235#section-3.1)|No description
403|[Forbidden](https://tools.ietf.org/html/rfc7231#section-6.5.3)|No description

> Example responses

```json
{
  "id": 0,
  "sku": "string",
  "title": "string",
  "description": "string",
  "original_location": "string",
  "created_at": "2017-06-19T15:15:48Z",
  "updated_at": "2017-06-19T15:15:48Z",
  "customer_id": 0,
  "quantity": 0,
  "weight": 0,
  "available": true,
  "image_file_name": "string",
  "image_content_type": "string",
  "image_file_size": 0,
  "image_updated_at": "2017-06-19T15:15:48Z",
  "image_originator_url": "string",
  "vendor": "string",
  "scancode": "string",
  "price": 0,
  "media_mail": true,
  "packaging": true,
  "length": 0,
  "width": 0,
  "height": 0,
  "active": true,
  "wholesale_cost": 0,
  "is_bundle": true,
  "packaging_type": "string",
  "promo": true,
  "street_date": "2017-06-19T15:15:48Z",
  "category": "string",
  "include_inbound_in_published": true,
  "returnable": true,
  "return_sku_match": "string",
  "return_price_restricted": true,
  "request_serial_number": true,
  "currency": "string",
  "tariff_number": "string",
  "label_format": "string",
  "notify_originator_inventory": 0,
  "name": "string"
}
```
```json
{
  "message": "string"
}
```
```json
{
  "message": "string"
}
```
<aside class="success">
This operation does not require authentication
</aside>

## putApiV2ItemsId

> Code samples

```shell
# You can also use wget
curl -X put ://staging.whiplashmerch.com/api/v2/items/{id} \
  -H 'X-Customer-Id: string' \
  -H 'X-Shop-Id: string' \
  -H 'Content-Type: application/json' \
  -H 'Accept: application/json'

```

```http
PUT ://staging.whiplashmerch.com/api/v2/items/{id} HTTP/1.1
Host: staging.whiplashmerch.com
Content-Type: application/json
Accept: application/json
X-Customer-Id: string
X-Shop-Id: string

```

```javascript
var headers = {
  'X-Customer-Id':'string',
  'X-Shop-Id':'string',
  'Content-Type':'application/json',
  'Accept':'application/json'

};

$.ajax({
  url: '://staging.whiplashmerch.com/api/v2/items/{id}',
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
  'X-Customer-Id':'string',
  'X-Shop-Id':'string',
  'Content-Type':'application/json',
  'Accept':'application/json'

};

fetch('://staging.whiplashmerch.com/api/v2/items/{id}',
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
  'X-Customer-Id' => 'string',
  'X-Shop-Id' => 'string',
  'Content-Type' => 'application/json',
  'Accept' => 'application/json'
}

result = RestClient.put '://staging.whiplashmerch.com/api/v2/items/{id}', params: {
  }, headers: headers

p JSON.parse(result)
```

```python
import requests
headers = {
  'X-Customer-Id': 'string',
  'X-Shop-Id': 'string',
  'Content-Type': 'application/json',
  'Accept': 'application/json'
}

r = requests.put('://staging.whiplashmerch.com/api/v2/items/{id}', params={

}, headers = headers)

print r.json()
```

```java
URL obj = new URL("://staging.whiplashmerch.com/api/v2/items/{id}");
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

`PUT /api/v2/items/{id}`

*Update an item*

Update an item

### Parameters

Parameter|In|Type|Required|Description
---|---|---|---|---|
X-Customer-Id|header|string|false|The customer associated with this resource.
X-Shop-Id|header|string|false|The shop associated with this resource.
sku|formData|string|false|the item SKU number
title|formData|string|false|the item title
description|formData|string|false|the item description
original_location|formData|string|false|the original warehouse location for the item
customer_id|formData|integer|false|the id of the customer the item belongs to
quantity|formData|integer|false|the available quantity of the item
weight|formData|number|false|the weight of the item (in pounds)
available|formData|boolean|false|is the item available?
image_file_name|formData|string|false|the file name for the item image
image_content_type|formData|string|false|the content type for item image
image_file_size|formData|integer|false|the file size for the item image
image_updated_at|formData|string|false|the last update date for the item image
image_originator_url|formData|string|false|the originator url for the item image
vendor|formData|string|false|the item vendor
scancode|formData|string|false|the item scancode
price|formData|number|false|the item price
media_mail|formData|boolean|false|is the item eligible for media mail?
packaging|formData|boolean|false|is the item packaging?
length|formData|number|false|the item length (in inches)
width|formData|number|false|the item width (in inches)
height|formData|number|false|the item height (in inches)
active|formData|boolean|false|is the item active?
wholesale_cost|formData|number|false|the wholesale cost of the item
is_bundle|formData|boolean|false|is the item a bundle?
packaging_type|formData|string|false|the item packaging type
promo|formData|boolean|false|is the item a promo?
street_date|formData|string|false|the item street date
category|formData|string|false|the item category
include_inbound_in_published|formData|boolean|false|include inbound items in published?
returnable|formData|boolean|false|is the item returnable?
return_sku_match|formData|string|false|the item return SKU match
return_price_restricted|formData|boolean|false|is the item return price restricted?
request_serial_number|formData|boolean|false|does the item require a serial number when shipping?
currency|formData|string|false|the item currency
tariff_number|formData|string|false|the item harmonized tariff number (for international shipping)
label_format|formData|string|false|the item postage label format (epl, png, pdf, etc)
notify_originator_inventory|formData|integer|false|notify originator inventory?
name|formData|string|false|the item name and description, formatted nicely
id|path|integer|true|No description


### Responses

Status|Meaning|Description
---|---|---|
200|[OK](https://tools.ietf.org/html/rfc7231#section-6.3.1)|Update an item
401|[Unauthorized](https://tools.ietf.org/html/rfc7235#section-3.1)|No description
403|[Forbidden](https://tools.ietf.org/html/rfc7231#section-6.5.3)|No description
422|[Unprocessable Entity](https://tools.ietf.org/html/rfc2518#section-10.3)|No description

> Example responses

```json
{
  "id": 0,
  "sku": "string",
  "title": "string",
  "description": "string",
  "original_location": "string",
  "created_at": "2017-06-19T15:15:48Z",
  "updated_at": "2017-06-19T15:15:48Z",
  "customer_id": 0,
  "quantity": 0,
  "weight": 0,
  "available": true,
  "image_file_name": "string",
  "image_content_type": "string",
  "image_file_size": 0,
  "image_updated_at": "2017-06-19T15:15:48Z",
  "image_originator_url": "string",
  "vendor": "string",
  "scancode": "string",
  "price": 0,
  "media_mail": true,
  "packaging": true,
  "length": 0,
  "width": 0,
  "height": 0,
  "active": true,
  "wholesale_cost": 0,
  "is_bundle": true,
  "packaging_type": "string",
  "promo": true,
  "street_date": "2017-06-19T15:15:48Z",
  "category": "string",
  "include_inbound_in_published": true,
  "returnable": true,
  "return_sku_match": "string",
  "return_price_restricted": true,
  "request_serial_number": true,
  "currency": "string",
  "tariff_number": "string",
  "label_format": "string",
  "notify_originator_inventory": 0,
  "name": "string"
}
```
```json
{
  "message": "string"
}
```
```json
{
  "message": "string"
}
```
```json
{
  "message": "string"
}
```
<aside class="success">
This operation does not require authentication
</aside>

## deleteApiV2ItemsId

> Code samples

```shell
# You can also use wget
curl -X delete ://staging.whiplashmerch.com/api/v2/items/{id} \
  -H 'X-Customer-Id: string' \
  -H 'X-Shop-Id: string' \
  -H 'Accept: application/json'

```

```http
DELETE ://staging.whiplashmerch.com/api/v2/items/{id} HTTP/1.1
Host: staging.whiplashmerch.com

Accept: application/json
X-Customer-Id: string
X-Shop-Id: string

```

```javascript
var headers = {
  'X-Customer-Id':'string',
  'X-Shop-Id':'string',
  'Accept':'application/json'

};

$.ajax({
  url: '://staging.whiplashmerch.com/api/v2/items/{id}',
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
  'X-Customer-Id':'string',
  'X-Shop-Id':'string',
  'Accept':'application/json'

};

fetch('://staging.whiplashmerch.com/api/v2/items/{id}',
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
  'X-Customer-Id' => 'string',
  'X-Shop-Id' => 'string',
  'Accept' => 'application/json'
}

result = RestClient.delete '://staging.whiplashmerch.com/api/v2/items/{id}', params: {
  }, headers: headers

p JSON.parse(result)
```

```python
import requests
headers = {
  'X-Customer-Id': 'string',
  'X-Shop-Id': 'string',
  'Accept': 'application/json'
}

r = requests.delete('://staging.whiplashmerch.com/api/v2/items/{id}', params={

}, headers = headers)

print r.json()
```

```java
URL obj = new URL("://staging.whiplashmerch.com/api/v2/items/{id}");
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

`DELETE /api/v2/items/{id}`

*Destroy an item*

Destroy an item

### Parameters

Parameter|In|Type|Required|Description
---|---|---|---|---|
id|path|integer|true|No description
X-Customer-Id|header|string|false|The customer associated with this resource.
X-Shop-Id|header|string|false|The shop associated with this resource.


### Responses

Status|Meaning|Description
---|---|---|
200|[OK](https://tools.ietf.org/html/rfc7231#section-6.3.1)|Destroy an item
401|[Unauthorized](https://tools.ietf.org/html/rfc7235#section-3.1)|No description
403|[Forbidden](https://tools.ietf.org/html/rfc7231#section-6.5.3)|No description
422|[Unprocessable Entity](https://tools.ietf.org/html/rfc2518#section-10.3)|No description

> Example responses

```json
{
  "id": 0,
  "sku": "string",
  "title": "string",
  "description": "string",
  "original_location": "string",
  "created_at": "2017-06-19T15:15:48Z",
  "updated_at": "2017-06-19T15:15:48Z",
  "customer_id": 0,
  "quantity": 0,
  "weight": 0,
  "available": true,
  "image_file_name": "string",
  "image_content_type": "string",
  "image_file_size": 0,
  "image_updated_at": "2017-06-19T15:15:48Z",
  "image_originator_url": "string",
  "vendor": "string",
  "scancode": "string",
  "price": 0,
  "media_mail": true,
  "packaging": true,
  "length": 0,
  "width": 0,
  "height": 0,
  "active": true,
  "wholesale_cost": 0,
  "is_bundle": true,
  "packaging_type": "string",
  "promo": true,
  "street_date": "2017-06-19T15:15:48Z",
  "category": "string",
  "include_inbound_in_published": true,
  "returnable": true,
  "return_sku_match": "string",
  "return_price_restricted": true,
  "request_serial_number": true,
  "currency": "string",
  "tariff_number": "string",
  "label_format": "string",
  "notify_originator_inventory": 0,
  "name": "string"
}
```
```json
{
  "message": "string"
}
```
```json
{
  "message": "string"
}
```
```json
{
  "message": "string"
}
```
<aside class="success">
This operation does not require authentication
</aside>

## getApiV2Items

> Code samples

```shell
# You can also use wget
curl -X get ://staging.whiplashmerch.com/api/v2/items \
  -H 'X-Customer-Id: string' \
  -H 'X-Shop-Id: string' \
  -H 'Accept: application/json'

```

```http
GET ://staging.whiplashmerch.com/api/v2/items HTTP/1.1
Host: staging.whiplashmerch.com

Accept: application/json
X-Customer-Id: string
X-Shop-Id: string

```

```javascript
var headers = {
  'X-Customer-Id':'string',
  'X-Shop-Id':'string',
  'Accept':'application/json'

};

$.ajax({
  url: '://staging.whiplashmerch.com/api/v2/items',
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
  'X-Customer-Id':'string',
  'X-Shop-Id':'string',
  'Accept':'application/json'

};

fetch('://staging.whiplashmerch.com/api/v2/items',
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
  'X-Customer-Id' => 'string',
  'X-Shop-Id' => 'string',
  'Accept' => 'application/json'
}

result = RestClient.get '://staging.whiplashmerch.com/api/v2/items', params: {
  }, headers: headers

p JSON.parse(result)
```

```python
import requests
headers = {
  'X-Customer-Id': 'string',
  'X-Shop-Id': 'string',
  'Accept': 'application/json'
}

r = requests.get('://staging.whiplashmerch.com/api/v2/items', params={

}, headers = headers)

print r.json()
```

```java
URL obj = new URL("://staging.whiplashmerch.com/api/v2/items");
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

`GET /api/v2/items`

*Get a list of items *

Get a list of items 

### Parameters

Parameter|In|Type|Required|Description
---|---|---|---|---|
X-Customer-Id|header|string|false|The customer associated with this resource.
X-Shop-Id|header|string|false|The shop associated with this resource.
search|query|string|false|JSON search string like {"attribute_eq": "Term"}
fields|query|string|false|Comma-separated list of fields to include in the response
page|query|integer|false|Page of results to fetch.
per_page|query|integer|false|Number of results to return per page.


### Responses

Status|Meaning|Description
---|---|---|
200|[OK](https://tools.ietf.org/html/rfc7231#section-6.3.1)|Get a list of items
|Unknown|No description

> Example responses

```json
{
  "id": 0,
  "sku": "string",
  "title": "string",
  "description": "string",
  "original_location": "string",
  "created_at": "2017-06-19T15:15:48Z",
  "updated_at": "2017-06-19T15:15:48Z",
  "customer_id": 0,
  "quantity": 0,
  "weight": 0,
  "available": true,
  "image_file_name": "string",
  "image_content_type": "string",
  "image_file_size": 0,
  "image_updated_at": "2017-06-19T15:15:48Z",
  "image_originator_url": "string",
  "vendor": "string",
  "scancode": "string",
  "price": 0,
  "media_mail": true,
  "packaging": true,
  "length": 0,
  "width": 0,
  "height": 0,
  "active": true,
  "wholesale_cost": 0,
  "is_bundle": true,
  "packaging_type": "string",
  "promo": true,
  "street_date": "2017-06-19T15:15:48Z",
  "category": "string",
  "include_inbound_in_published": true,
  "returnable": true,
  "return_sku_match": "string",
  "return_price_restricted": true,
  "request_serial_number": true,
  "currency": "string",
  "tariff_number": "string",
  "label_format": "string",
  "notify_originator_inventory": 0,
  "name": "string"
}
```
```json
{
  "message": "string"
}
```
<aside class="success">
This operation does not require authentication
</aside>

## postApiV2Items

> Code samples

```shell
# You can also use wget
curl -X post ://staging.whiplashmerch.com/api/v2/items \
  -H 'X-Customer-Id: string' \
  -H 'X-Shop-Id: string' \
  -H 'Content-Type: application/json' \
  -H 'Accept: application/json'

```

```http
POST ://staging.whiplashmerch.com/api/v2/items HTTP/1.1
Host: staging.whiplashmerch.com
Content-Type: application/json
Accept: application/json
X-Customer-Id: string
X-Shop-Id: string

```

```javascript
var headers = {
  'X-Customer-Id':'string',
  'X-Shop-Id':'string',
  'Content-Type':'application/json',
  'Accept':'application/json'

};

$.ajax({
  url: '://staging.whiplashmerch.com/api/v2/items',
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
  'X-Customer-Id':'string',
  'X-Shop-Id':'string',
  'Content-Type':'application/json',
  'Accept':'application/json'

};

fetch('://staging.whiplashmerch.com/api/v2/items',
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
  'X-Customer-Id' => 'string',
  'X-Shop-Id' => 'string',
  'Content-Type' => 'application/json',
  'Accept' => 'application/json'
}

result = RestClient.post '://staging.whiplashmerch.com/api/v2/items', params: {
  }, headers: headers

p JSON.parse(result)
```

```python
import requests
headers = {
  'X-Customer-Id': 'string',
  'X-Shop-Id': 'string',
  'Content-Type': 'application/json',
  'Accept': 'application/json'
}

r = requests.post('://staging.whiplashmerch.com/api/v2/items', params={

}, headers = headers)

print r.json()
```

```java
URL obj = new URL("://staging.whiplashmerch.com/api/v2/items");
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

`POST /api/v2/items`

*Create an item*

Create an item

### Parameters

Parameter|In|Type|Required|Description
---|---|---|---|---|
X-Customer-Id|header|string|false|The customer associated with this resource.
X-Shop-Id|header|string|false|The shop associated with this resource.
sku|formData|string|false|the item SKU number
title|formData|string|false|the item title
description|formData|string|false|the item description
original_location|formData|string|false|the original warehouse location for the item
customer_id|formData|integer|false|the id of the customer the item belongs to
quantity|formData|integer|false|the available quantity of the item
weight|formData|number|false|the weight of the item (in pounds)
available|formData|boolean|false|is the item available?
image_file_name|formData|string|false|the file name for the item image
image_content_type|formData|string|false|the content type for item image
image_file_size|formData|integer|false|the file size for the item image
image_updated_at|formData|string|false|the last update date for the item image
image_originator_url|formData|string|false|the originator url for the item image
vendor|formData|string|false|the item vendor
scancode|formData|string|false|the item scancode
price|formData|number|false|the item price
media_mail|formData|boolean|false|is the item eligible for media mail?
packaging|formData|boolean|false|is the item packaging?
length|formData|number|false|the item length (in inches)
width|formData|number|false|the item width (in inches)
height|formData|number|false|the item height (in inches)
active|formData|boolean|false|is the item active?
wholesale_cost|formData|number|false|the wholesale cost of the item
is_bundle|formData|boolean|false|is the item a bundle?
packaging_type|formData|string|false|the item packaging type
promo|formData|boolean|false|is the item a promo?
street_date|formData|string|false|the item street date
category|formData|string|false|the item category
include_inbound_in_published|formData|boolean|false|include inbound items in published?
returnable|formData|boolean|false|is the item returnable?
return_sku_match|formData|string|false|the item return SKU match
return_price_restricted|formData|boolean|false|is the item return price restricted?
request_serial_number|formData|boolean|false|does the item require a serial number when shipping?
currency|formData|string|false|the item currency
tariff_number|formData|string|false|the item harmonized tariff number (for international shipping)
label_format|formData|string|false|the item postage label format (epl, png, pdf, etc)
notify_originator_inventory|formData|integer|false|notify originator inventory?
name|formData|string|false|the item name and description, formatted nicely


### Responses

Status|Meaning|Description
---|---|---|
201|[Created](https://tools.ietf.org/html/rfc7231#section-6.3.2)|Create an item
401|[Unauthorized](https://tools.ietf.org/html/rfc7235#section-3.1)|No description
403|[Forbidden](https://tools.ietf.org/html/rfc7231#section-6.5.3)|No description
409|[Conflict](https://tools.ietf.org/html/rfc7231#section-6.5.8)|No description
422|[Unprocessable Entity](https://tools.ietf.org/html/rfc2518#section-10.3)|No description

> Example responses

```json
{
  "id": 0,
  "sku": "string",
  "title": "string",
  "description": "string",
  "original_location": "string",
  "created_at": "2017-06-19T15:15:48Z",
  "updated_at": "2017-06-19T15:15:48Z",
  "customer_id": 0,
  "quantity": 0,
  "weight": 0,
  "available": true,
  "image_file_name": "string",
  "image_content_type": "string",
  "image_file_size": 0,
  "image_updated_at": "2017-06-19T15:15:48Z",
  "image_originator_url": "string",
  "vendor": "string",
  "scancode": "string",
  "price": 0,
  "media_mail": true,
  "packaging": true,
  "length": 0,
  "width": 0,
  "height": 0,
  "active": true,
  "wholesale_cost": 0,
  "is_bundle": true,
  "packaging_type": "string",
  "promo": true,
  "street_date": "2017-06-19T15:15:48Z",
  "category": "string",
  "include_inbound_in_published": true,
  "returnable": true,
  "return_sku_match": "string",
  "return_price_restricted": true,
  "request_serial_number": true,
  "currency": "string",
  "tariff_number": "string",
  "label_format": "string",
  "notify_originator_inventory": 0,
  "name": "string"
}
```
```json
{
  "message": "string"
}
```
```json
{
  "message": "string"
}
```
```json
{
  "message": "string"
}
```
```json
{
  "message": "string"
}
```
<aside class="success">
This operation does not require authentication
</aside>

## getApiV2ItemsCount

> Code samples

```shell
# You can also use wget
curl -X get ://staging.whiplashmerch.com/api/v2/items/count \
  -H 'X-Customer-Id: string' \
  -H 'X-Shop-Id: string' \
  -H 'Accept: application/json'

```

```http
GET ://staging.whiplashmerch.com/api/v2/items/count HTTP/1.1
Host: staging.whiplashmerch.com

Accept: application/json
X-Customer-Id: string
X-Shop-Id: string

```

```javascript
var headers = {
  'X-Customer-Id':'string',
  'X-Shop-Id':'string',
  'Accept':'application/json'

};

$.ajax({
  url: '://staging.whiplashmerch.com/api/v2/items/count',
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
  'X-Customer-Id':'string',
  'X-Shop-Id':'string',
  'Accept':'application/json'

};

fetch('://staging.whiplashmerch.com/api/v2/items/count',
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
  'X-Customer-Id' => 'string',
  'X-Shop-Id' => 'string',
  'Accept' => 'application/json'
}

result = RestClient.get '://staging.whiplashmerch.com/api/v2/items/count', params: {
  }, headers: headers

p JSON.parse(result)
```

```python
import requests
headers = {
  'X-Customer-Id': 'string',
  'X-Shop-Id': 'string',
  'Accept': 'application/json'
}

r = requests.get('://staging.whiplashmerch.com/api/v2/items/count', params={

}, headers = headers)

print r.json()
```

```java
URL obj = new URL("://staging.whiplashmerch.com/api/v2/items/count");
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

`GET /api/v2/items/count`

*Returns count of items*

Returns count of items

### Parameters

Parameter|In|Type|Required|Description
---|---|---|---|---|
X-Customer-Id|header|string|false|The customer associated with this resource.
X-Shop-Id|header|string|false|The shop associated with this resource.
search|query|string|false|JSON search string like {"attribute_eq": "Term"}


### Responses

Status|Meaning|Description
---|---|---|
200|[OK](https://tools.ietf.org/html/rfc7231#section-6.3.1)|Returns count of items
401|[Unauthorized](https://tools.ietf.org/html/rfc7235#section-3.1)|No description
403|[Forbidden](https://tools.ietf.org/html/rfc7231#section-6.5.3)|No description

> Example responses

```json
{
  "id": 0,
  "sku": "string",
  "title": "string",
  "description": "string",
  "original_location": "string",
  "created_at": "2017-06-19T15:15:48Z",
  "updated_at": "2017-06-19T15:15:48Z",
  "customer_id": 0,
  "quantity": 0,
  "weight": 0,
  "available": true,
  "image_file_name": "string",
  "image_content_type": "string",
  "image_file_size": 0,
  "image_updated_at": "2017-06-19T15:15:48Z",
  "image_originator_url": "string",
  "vendor": "string",
  "scancode": "string",
  "price": 0,
  "media_mail": true,
  "packaging": true,
  "length": 0,
  "width": 0,
  "height": 0,
  "active": true,
  "wholesale_cost": 0,
  "is_bundle": true,
  "packaging_type": "string",
  "promo": true,
  "street_date": "2017-06-19T15:15:48Z",
  "category": "string",
  "include_inbound_in_published": true,
  "returnable": true,
  "return_sku_match": "string",
  "return_price_restricted": true,
  "request_serial_number": true,
  "currency": "string",
  "tariff_number": "string",
  "label_format": "string",
  "notify_originator_inventory": 0,
  "name": "string"
}
```
```json
{
  "message": "string"
}
```
```json
{
  "message": "string"
}
```
<aside class="success">
This operation does not require authentication
</aside>

## getApiV2ItemsIdInbound

> Code samples

```shell
# You can also use wget
curl -X get ://staging.whiplashmerch.com/api/v2/items/{id}/inbound \
  -H 'X-Customer-Id: string' \
  -H 'X-Shop-Id: string' \
  -H 'Accept: application/json'

```

```http
GET ://staging.whiplashmerch.com/api/v2/items/{id}/inbound HTTP/1.1
Host: staging.whiplashmerch.com

Accept: application/json
X-Customer-Id: string
X-Shop-Id: string

```

```javascript
var headers = {
  'X-Customer-Id':'string',
  'X-Shop-Id':'string',
  'Accept':'application/json'

};

$.ajax({
  url: '://staging.whiplashmerch.com/api/v2/items/{id}/inbound',
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
  'X-Customer-Id':'string',
  'X-Shop-Id':'string',
  'Accept':'application/json'

};

fetch('://staging.whiplashmerch.com/api/v2/items/{id}/inbound',
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
  'X-Customer-Id' => 'string',
  'X-Shop-Id' => 'string',
  'Accept' => 'application/json'
}

result = RestClient.get '://staging.whiplashmerch.com/api/v2/items/{id}/inbound', params: {
  }, headers: headers

p JSON.parse(result)
```

```python
import requests
headers = {
  'X-Customer-Id': 'string',
  'X-Shop-Id': 'string',
  'Accept': 'application/json'
}

r = requests.get('://staging.whiplashmerch.com/api/v2/items/{id}/inbound', params={

}, headers = headers)

print r.json()
```

```java
URL obj = new URL("://staging.whiplashmerch.com/api/v2/items/{id}/inbound");
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

`GET /api/v2/items/{id}/inbound`

*Shows all inbound ship notices containing this item*

Shows all inbound ship notices containing this item

### Parameters

Parameter|In|Type|Required|Description
---|---|---|---|---|
id|path|integer|true|No description
X-Customer-Id|header|string|false|The customer associated with this resource.
X-Shop-Id|header|string|false|The shop associated with this resource.


### Responses

Status|Meaning|Description
---|---|---|
200|[OK](https://tools.ietf.org/html/rfc7231#section-6.3.1)|Shows all inbound ship notices containing this item
401|[Unauthorized](https://tools.ietf.org/html/rfc7235#section-3.1)|No description
403|[Forbidden](https://tools.ietf.org/html/rfc7231#section-6.5.3)|No description

> Example responses

```json
{
  "id": 0,
  "sku": "string",
  "title": "string",
  "description": "string",
  "original_location": "string",
  "created_at": "2017-06-19T15:15:48Z",
  "updated_at": "2017-06-19T15:15:48Z",
  "customer_id": 0,
  "quantity": 0,
  "weight": 0,
  "available": true,
  "image_file_name": "string",
  "image_content_type": "string",
  "image_file_size": 0,
  "image_updated_at": "2017-06-19T15:15:48Z",
  "image_originator_url": "string",
  "vendor": "string",
  "scancode": "string",
  "price": 0,
  "media_mail": true,
  "packaging": true,
  "length": 0,
  "width": 0,
  "height": 0,
  "active": true,
  "wholesale_cost": 0,
  "is_bundle": true,
  "packaging_type": "string",
  "promo": true,
  "street_date": "2017-06-19T15:15:48Z",
  "category": "string",
  "include_inbound_in_published": true,
  "returnable": true,
  "return_sku_match": "string",
  "return_price_restricted": true,
  "request_serial_number": true,
  "currency": "string",
  "tariff_number": "string",
  "label_format": "string",
  "notify_originator_inventory": 0,
  "name": "string"
}
```
```json
{
  "message": "string"
}
```
```json
{
  "message": "string"
}
```
<aside class="success">
This operation does not require authentication
</aside>

## getApiV2ItemsIdInBundles

> Code samples

```shell
# You can also use wget
curl -X get ://staging.whiplashmerch.com/api/v2/items/{id}/in_bundles \
  -H 'X-Customer-Id: string' \
  -H 'X-Shop-Id: string' \
  -H 'Accept: application/json'

```

```http
GET ://staging.whiplashmerch.com/api/v2/items/{id}/in_bundles HTTP/1.1
Host: staging.whiplashmerch.com

Accept: application/json
X-Customer-Id: string
X-Shop-Id: string

```

```javascript
var headers = {
  'X-Customer-Id':'string',
  'X-Shop-Id':'string',
  'Accept':'application/json'

};

$.ajax({
  url: '://staging.whiplashmerch.com/api/v2/items/{id}/in_bundles',
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
  'X-Customer-Id':'string',
  'X-Shop-Id':'string',
  'Accept':'application/json'

};

fetch('://staging.whiplashmerch.com/api/v2/items/{id}/in_bundles',
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
  'X-Customer-Id' => 'string',
  'X-Shop-Id' => 'string',
  'Accept' => 'application/json'
}

result = RestClient.get '://staging.whiplashmerch.com/api/v2/items/{id}/in_bundles', params: {
  }, headers: headers

p JSON.parse(result)
```

```python
import requests
headers = {
  'X-Customer-Id': 'string',
  'X-Shop-Id': 'string',
  'Accept': 'application/json'
}

r = requests.get('://staging.whiplashmerch.com/api/v2/items/{id}/in_bundles', params={

}, headers = headers)

print r.json()
```

```java
URL obj = new URL("://staging.whiplashmerch.com/api/v2/items/{id}/in_bundles");
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

`GET /api/v2/items/{id}/in_bundles`

*Shows all instances of this item in bundles*

Shows all instances of this item in bundles

### Parameters

Parameter|In|Type|Required|Description
---|---|---|---|---|
id|path|integer|true|No description
X-Customer-Id|header|string|false|The customer associated with this resource.
X-Shop-Id|header|string|false|The shop associated with this resource.


### Responses

Status|Meaning|Description
---|---|---|
200|[OK](https://tools.ietf.org/html/rfc7231#section-6.3.1)|Shows all instances of this item in bundles
401|[Unauthorized](https://tools.ietf.org/html/rfc7235#section-3.1)|No description
403|[Forbidden](https://tools.ietf.org/html/rfc7231#section-6.5.3)|No description

> Example responses

```json
{
  "id": 0,
  "sku": "string",
  "title": "string",
  "description": "string",
  "original_location": "string",
  "created_at": "2017-06-19T15:15:48Z",
  "updated_at": "2017-06-19T15:15:48Z",
  "customer_id": 0,
  "quantity": 0,
  "weight": 0,
  "available": true,
  "image_file_name": "string",
  "image_content_type": "string",
  "image_file_size": 0,
  "image_updated_at": "2017-06-19T15:15:48Z",
  "image_originator_url": "string",
  "vendor": "string",
  "scancode": "string",
  "price": 0,
  "media_mail": true,
  "packaging": true,
  "length": 0,
  "width": 0,
  "height": 0,
  "active": true,
  "wholesale_cost": 0,
  "is_bundle": true,
  "packaging_type": "string",
  "promo": true,
  "street_date": "2017-06-19T15:15:48Z",
  "category": "string",
  "include_inbound_in_published": true,
  "returnable": true,
  "return_sku_match": "string",
  "return_price_restricted": true,
  "request_serial_number": true,
  "currency": "string",
  "tariff_number": "string",
  "label_format": "string",
  "notify_originator_inventory": 0,
  "name": "string"
}
```
```json
{
  "message": "string"
}
```
```json
{
  "message": "string"
}
```
<aside class="success">
This operation does not require authentication
</aside>

## getApiV2ItemsIdBundleItems

> Code samples

```shell
# You can also use wget
curl -X get ://staging.whiplashmerch.com/api/v2/items/{id}/bundle_items \
  -H 'X-Customer-Id: string' \
  -H 'X-Shop-Id: string' \
  -H 'Accept: application/json'

```

```http
GET ://staging.whiplashmerch.com/api/v2/items/{id}/bundle_items HTTP/1.1
Host: staging.whiplashmerch.com

Accept: application/json
X-Customer-Id: string
X-Shop-Id: string

```

```javascript
var headers = {
  'X-Customer-Id':'string',
  'X-Shop-Id':'string',
  'Accept':'application/json'

};

$.ajax({
  url: '://staging.whiplashmerch.com/api/v2/items/{id}/bundle_items',
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
  'X-Customer-Id':'string',
  'X-Shop-Id':'string',
  'Accept':'application/json'

};

fetch('://staging.whiplashmerch.com/api/v2/items/{id}/bundle_items',
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
  'X-Customer-Id' => 'string',
  'X-Shop-Id' => 'string',
  'Accept' => 'application/json'
}

result = RestClient.get '://staging.whiplashmerch.com/api/v2/items/{id}/bundle_items', params: {
  }, headers: headers

p JSON.parse(result)
```

```python
import requests
headers = {
  'X-Customer-Id': 'string',
  'X-Shop-Id': 'string',
  'Accept': 'application/json'
}

r = requests.get('://staging.whiplashmerch.com/api/v2/items/{id}/bundle_items', params={

}, headers = headers)

print r.json()
```

```java
URL obj = new URL("://staging.whiplashmerch.com/api/v2/items/{id}/bundle_items");
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

`GET /api/v2/items/{id}/bundle_items`

*Shows all bundles containing this item*

Shows all bundles containing this item

### Parameters

Parameter|In|Type|Required|Description
---|---|---|---|---|
id|path|integer|true|No description
X-Customer-Id|header|string|false|The customer associated with this resource.
X-Shop-Id|header|string|false|The shop associated with this resource.


### Responses

Status|Meaning|Description
---|---|---|
200|[OK](https://tools.ietf.org/html/rfc7231#section-6.3.1)|Shows all bundles containing this item
401|[Unauthorized](https://tools.ietf.org/html/rfc7235#section-3.1)|No description
403|[Forbidden](https://tools.ietf.org/html/rfc7231#section-6.5.3)|No description

> Example responses

```json
{
  "id": 0,
  "sku": "string",
  "title": "string",
  "description": "string",
  "original_location": "string",
  "created_at": "2017-06-19T15:15:48Z",
  "updated_at": "2017-06-19T15:15:48Z",
  "customer_id": 0,
  "quantity": 0,
  "weight": 0,
  "available": true,
  "image_file_name": "string",
  "image_content_type": "string",
  "image_file_size": 0,
  "image_updated_at": "2017-06-19T15:15:48Z",
  "image_originator_url": "string",
  "vendor": "string",
  "scancode": "string",
  "price": 0,
  "media_mail": true,
  "packaging": true,
  "length": 0,
  "width": 0,
  "height": 0,
  "active": true,
  "wholesale_cost": 0,
  "is_bundle": true,
  "packaging_type": "string",
  "promo": true,
  "street_date": "2017-06-19T15:15:48Z",
  "category": "string",
  "include_inbound_in_published": true,
  "returnable": true,
  "return_sku_match": "string",
  "return_price_restricted": true,
  "request_serial_number": true,
  "currency": "string",
  "tariff_number": "string",
  "label_format": "string",
  "notify_originator_inventory": 0,
  "name": "string"
}
```
```json
{
  "message": "string"
}
```
```json
{
  "message": "string"
}
```
<aside class="success">
This operation does not require authentication
</aside>

## getApiV2ItemsIdWarehouseQuantities

> Code samples

```shell
# You can also use wget
curl -X get ://staging.whiplashmerch.com/api/v2/items/{id}/warehouse_quantities \
  -H 'X-Customer-Id: string' \
  -H 'X-Shop-Id: string' \
  -H 'Accept: application/json'

```

```http
GET ://staging.whiplashmerch.com/api/v2/items/{id}/warehouse_quantities HTTP/1.1
Host: staging.whiplashmerch.com

Accept: application/json
X-Customer-Id: string
X-Shop-Id: string

```

```javascript
var headers = {
  'X-Customer-Id':'string',
  'X-Shop-Id':'string',
  'Accept':'application/json'

};

$.ajax({
  url: '://staging.whiplashmerch.com/api/v2/items/{id}/warehouse_quantities',
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
  'X-Customer-Id':'string',
  'X-Shop-Id':'string',
  'Accept':'application/json'

};

fetch('://staging.whiplashmerch.com/api/v2/items/{id}/warehouse_quantities',
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
  'X-Customer-Id' => 'string',
  'X-Shop-Id' => 'string',
  'Accept' => 'application/json'
}

result = RestClient.get '://staging.whiplashmerch.com/api/v2/items/{id}/warehouse_quantities', params: {
  }, headers: headers

p JSON.parse(result)
```

```python
import requests
headers = {
  'X-Customer-Id': 'string',
  'X-Shop-Id': 'string',
  'Accept': 'application/json'
}

r = requests.get('://staging.whiplashmerch.com/api/v2/items/{id}/warehouse_quantities', params={

}, headers = headers)

print r.json()
```

```java
URL obj = new URL("://staging.whiplashmerch.com/api/v2/items/{id}/warehouse_quantities");
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

`GET /api/v2/items/{id}/warehouse_quantities`

*Shows the number of this item in the warehouse*

Shows the number of this item in the warehouse

### Parameters

Parameter|In|Type|Required|Description
---|---|---|---|---|
id|path|integer|true|No description
X-Customer-Id|header|string|false|The customer associated with this resource.
X-Shop-Id|header|string|false|The shop associated with this resource.


### Responses

Status|Meaning|Description
---|---|---|
200|[OK](https://tools.ietf.org/html/rfc7231#section-6.3.1)|Shows the number of this item in the warehouse
401|[Unauthorized](https://tools.ietf.org/html/rfc7235#section-3.1)|No description
403|[Forbidden](https://tools.ietf.org/html/rfc7231#section-6.5.3)|No description

> Example responses

```json
{
  "id": 0,
  "sku": "string",
  "title": "string",
  "description": "string",
  "original_location": "string",
  "created_at": "2017-06-19T15:15:48Z",
  "updated_at": "2017-06-19T15:15:48Z",
  "customer_id": 0,
  "quantity": 0,
  "weight": 0,
  "available": true,
  "image_file_name": "string",
  "image_content_type": "string",
  "image_file_size": 0,
  "image_updated_at": "2017-06-19T15:15:48Z",
  "image_originator_url": "string",
  "vendor": "string",
  "scancode": "string",
  "price": 0,
  "media_mail": true,
  "packaging": true,
  "length": 0,
  "width": 0,
  "height": 0,
  "active": true,
  "wholesale_cost": 0,
  "is_bundle": true,
  "packaging_type": "string",
  "promo": true,
  "street_date": "2017-06-19T15:15:48Z",
  "category": "string",
  "include_inbound_in_published": true,
  "returnable": true,
  "return_sku_match": "string",
  "return_price_restricted": true,
  "request_serial_number": true,
  "currency": "string",
  "tariff_number": "string",
  "label_format": "string",
  "notify_originator_inventory": 0,
  "name": "string"
}
```
```json
{
  "message": "string"
}
```
```json
{
  "message": "string"
}
```
<aside class="success">
This operation does not require authentication
</aside>

## getApiV2ItemsOriginatorOriginatorId

> Code samples

```shell
# You can also use wget
curl -X get ://staging.whiplashmerch.com/api/v2/items/originator/{originator_id} \
  -H 'X-Customer-Id: string' \
  -H 'X-Shop-Id: string' \
  -H 'Accept: application/json'

```

```http
GET ://staging.whiplashmerch.com/api/v2/items/originator/{originator_id} HTTP/1.1
Host: staging.whiplashmerch.com

Accept: application/json
X-Customer-Id: string
X-Shop-Id: string

```

```javascript
var headers = {
  'X-Customer-Id':'string',
  'X-Shop-Id':'string',
  'Accept':'application/json'

};

$.ajax({
  url: '://staging.whiplashmerch.com/api/v2/items/originator/{originator_id}',
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
  'X-Customer-Id':'string',
  'X-Shop-Id':'string',
  'Accept':'application/json'

};

fetch('://staging.whiplashmerch.com/api/v2/items/originator/{originator_id}',
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
  'X-Customer-Id' => 'string',
  'X-Shop-Id' => 'string',
  'Accept' => 'application/json'
}

result = RestClient.get '://staging.whiplashmerch.com/api/v2/items/originator/{originator_id}', params: {
  }, headers: headers

p JSON.parse(result)
```

```python
import requests
headers = {
  'X-Customer-Id': 'string',
  'X-Shop-Id': 'string',
  'Accept': 'application/json'
}

r = requests.get('://staging.whiplashmerch.com/api/v2/items/originator/{originator_id}', params={

}, headers = headers)

print r.json()
```

```java
URL obj = new URL("://staging.whiplashmerch.com/api/v2/items/originator/{originator_id}");
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

`GET /api/v2/items/originator/{originator_id}`

*Get an item via its originator id*

Get an item via its originator id

### Parameters

Parameter|In|Type|Required|Description
---|---|---|---|---|
originator_id|path|integer|true|No description
X-Customer-Id|header|string|false|The customer associated with this resource.
X-Shop-Id|header|string|false|The shop associated with this resource.


### Responses

Status|Meaning|Description
---|---|---|
200|[OK](https://tools.ietf.org/html/rfc7231#section-6.3.1)|Get an item via its originator id
401|[Unauthorized](https://tools.ietf.org/html/rfc7235#section-3.1)|No description
403|[Forbidden](https://tools.ietf.org/html/rfc7231#section-6.5.3)|No description

> Example responses

```json
{
  "id": 0,
  "sku": "string",
  "title": "string",
  "description": "string",
  "original_location": "string",
  "created_at": "2017-06-19T15:15:48Z",
  "updated_at": "2017-06-19T15:15:48Z",
  "customer_id": 0,
  "quantity": 0,
  "weight": 0,
  "available": true,
  "image_file_name": "string",
  "image_content_type": "string",
  "image_file_size": 0,
  "image_updated_at": "2017-06-19T15:15:48Z",
  "image_originator_url": "string",
  "vendor": "string",
  "scancode": "string",
  "price": 0,
  "media_mail": true,
  "packaging": true,
  "length": 0,
  "width": 0,
  "height": 0,
  "active": true,
  "wholesale_cost": 0,
  "is_bundle": true,
  "packaging_type": "string",
  "promo": true,
  "street_date": "2017-06-19T15:15:48Z",
  "category": "string",
  "include_inbound_in_published": true,
  "returnable": true,
  "return_sku_match": "string",
  "return_price_restricted": true,
  "request_serial_number": true,
  "currency": "string",
  "tariff_number": "string",
  "label_format": "string",
  "notify_originator_inventory": 0,
  "name": "string"
}
```
```json
{
  "message": "string"
}
```
```json
{
  "message": "string"
}
```
<aside class="success">
This operation does not require authentication
</aside>

## putApiV2ItemsOriginatorOriginatorId

> Code samples

```shell
# You can also use wget
curl -X put ://staging.whiplashmerch.com/api/v2/items/originator/{originator_id} \
  -H 'X-Customer-Id: string' \
  -H 'X-Shop-Id: string' \
  -H 'Content-Type: application/json' \
  -H 'Accept: application/json'

```

```http
PUT ://staging.whiplashmerch.com/api/v2/items/originator/{originator_id} HTTP/1.1
Host: staging.whiplashmerch.com
Content-Type: application/json
Accept: application/json
X-Customer-Id: string
X-Shop-Id: string

```

```javascript
var headers = {
  'X-Customer-Id':'string',
  'X-Shop-Id':'string',
  'Content-Type':'application/json',
  'Accept':'application/json'

};

$.ajax({
  url: '://staging.whiplashmerch.com/api/v2/items/originator/{originator_id}',
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
  'X-Customer-Id':'string',
  'X-Shop-Id':'string',
  'Content-Type':'application/json',
  'Accept':'application/json'

};

fetch('://staging.whiplashmerch.com/api/v2/items/originator/{originator_id}',
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
  'X-Customer-Id' => 'string',
  'X-Shop-Id' => 'string',
  'Content-Type' => 'application/json',
  'Accept' => 'application/json'
}

result = RestClient.put '://staging.whiplashmerch.com/api/v2/items/originator/{originator_id}', params: {
  }, headers: headers

p JSON.parse(result)
```

```python
import requests
headers = {
  'X-Customer-Id': 'string',
  'X-Shop-Id': 'string',
  'Content-Type': 'application/json',
  'Accept': 'application/json'
}

r = requests.put('://staging.whiplashmerch.com/api/v2/items/originator/{originator_id}', params={

}, headers = headers)

print r.json()
```

```java
URL obj = new URL("://staging.whiplashmerch.com/api/v2/items/originator/{originator_id}");
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

`PUT /api/v2/items/originator/{originator_id}`

*Update an item via its originator id*

Update an item via its originator id

### Parameters

Parameter|In|Type|Required|Description
---|---|---|---|---|
X-Customer-Id|header|string|false|The customer associated with this resource.
X-Shop-Id|header|string|false|The shop associated with this resource.
sku|formData|string|false|the item SKU number
title|formData|string|false|the item title
description|formData|string|false|the item description
original_location|formData|string|false|the original warehouse location for the item
customer_id|formData|integer|false|the id of the customer the item belongs to
quantity|formData|integer|false|the available quantity of the item
weight|formData|number|false|the weight of the item (in pounds)
available|formData|boolean|false|is the item available?
image_file_name|formData|string|false|the file name for the item image
image_content_type|formData|string|false|the content type for item image
image_file_size|formData|integer|false|the file size for the item image
image_updated_at|formData|string|false|the last update date for the item image
image_originator_url|formData|string|false|the originator url for the item image
vendor|formData|string|false|the item vendor
scancode|formData|string|false|the item scancode
price|formData|number|false|the item price
media_mail|formData|boolean|false|is the item eligible for media mail?
packaging|formData|boolean|false|is the item packaging?
length|formData|number|false|the item length (in inches)
width|formData|number|false|the item width (in inches)
height|formData|number|false|the item height (in inches)
active|formData|boolean|false|is the item active?
wholesale_cost|formData|number|false|the wholesale cost of the item
is_bundle|formData|boolean|false|is the item a bundle?
packaging_type|formData|string|false|the item packaging type
promo|formData|boolean|false|is the item a promo?
street_date|formData|string|false|the item street date
category|formData|string|false|the item category
include_inbound_in_published|formData|boolean|false|include inbound items in published?
returnable|formData|boolean|false|is the item returnable?
return_sku_match|formData|string|false|the item return SKU match
return_price_restricted|formData|boolean|false|is the item return price restricted?
request_serial_number|formData|boolean|false|does the item require a serial number when shipping?
currency|formData|string|false|the item currency
tariff_number|formData|string|false|the item harmonized tariff number (for international shipping)
label_format|formData|string|false|the item postage label format (epl, png, pdf, etc)
notify_originator_inventory|formData|integer|false|notify originator inventory?
name|formData|string|false|the item name and description, formatted nicely
originator_id|path|integer|true|No description


### Responses

Status|Meaning|Description
---|---|---|
200|[OK](https://tools.ietf.org/html/rfc7231#section-6.3.1)|Update an item via its originator id
401|[Unauthorized](https://tools.ietf.org/html/rfc7235#section-3.1)|No description
403|[Forbidden](https://tools.ietf.org/html/rfc7231#section-6.5.3)|No description
422|[Unprocessable Entity](https://tools.ietf.org/html/rfc2518#section-10.3)|No description

> Example responses

```json
{
  "id": 0,
  "sku": "string",
  "title": "string",
  "description": "string",
  "original_location": "string",
  "created_at": "2017-06-19T15:15:48Z",
  "updated_at": "2017-06-19T15:15:48Z",
  "customer_id": 0,
  "quantity": 0,
  "weight": 0,
  "available": true,
  "image_file_name": "string",
  "image_content_type": "string",
  "image_file_size": 0,
  "image_updated_at": "2017-06-19T15:15:48Z",
  "image_originator_url": "string",
  "vendor": "string",
  "scancode": "string",
  "price": 0,
  "media_mail": true,
  "packaging": true,
  "length": 0,
  "width": 0,
  "height": 0,
  "active": true,
  "wholesale_cost": 0,
  "is_bundle": true,
  "packaging_type": "string",
  "promo": true,
  "street_date": "2017-06-19T15:15:48Z",
  "category": "string",
  "include_inbound_in_published": true,
  "returnable": true,
  "return_sku_match": "string",
  "return_price_restricted": true,
  "request_serial_number": true,
  "currency": "string",
  "tariff_number": "string",
  "label_format": "string",
  "notify_originator_inventory": 0,
  "name": "string"
}
```
```json
{
  "message": "string"
}
```
```json
{
  "message": "string"
}
```
```json
{
  "message": "string"
}
```
<aside class="success">
This operation does not require authentication
</aside>

## deleteApiV2ItemsOriginatorOriginatorId

> Code samples

```shell
# You can also use wget
curl -X delete ://staging.whiplashmerch.com/api/v2/items/originator/{originator_id} \
  -H 'X-Customer-Id: string' \
  -H 'X-Shop-Id: string' \
  -H 'Accept: application/json'

```

```http
DELETE ://staging.whiplashmerch.com/api/v2/items/originator/{originator_id} HTTP/1.1
Host: staging.whiplashmerch.com

Accept: application/json
X-Customer-Id: string
X-Shop-Id: string

```

```javascript
var headers = {
  'X-Customer-Id':'string',
  'X-Shop-Id':'string',
  'Accept':'application/json'

};

$.ajax({
  url: '://staging.whiplashmerch.com/api/v2/items/originator/{originator_id}',
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
  'X-Customer-Id':'string',
  'X-Shop-Id':'string',
  'Accept':'application/json'

};

fetch('://staging.whiplashmerch.com/api/v2/items/originator/{originator_id}',
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
  'X-Customer-Id' => 'string',
  'X-Shop-Id' => 'string',
  'Accept' => 'application/json'
}

result = RestClient.delete '://staging.whiplashmerch.com/api/v2/items/originator/{originator_id}', params: {
  }, headers: headers

p JSON.parse(result)
```

```python
import requests
headers = {
  'X-Customer-Id': 'string',
  'X-Shop-Id': 'string',
  'Accept': 'application/json'
}

r = requests.delete('://staging.whiplashmerch.com/api/v2/items/originator/{originator_id}', params={

}, headers = headers)

print r.json()
```

```java
URL obj = new URL("://staging.whiplashmerch.com/api/v2/items/originator/{originator_id}");
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

`DELETE /api/v2/items/originator/{originator_id}`

*Destroy an item via its originator id*

Destroy an item via its originator id

### Parameters

Parameter|In|Type|Required|Description
---|---|---|---|---|
originator_id|path|integer|true|No description
X-Customer-Id|header|string|false|The customer associated with this resource.
X-Shop-Id|header|string|false|The shop associated with this resource.


### Responses

Status|Meaning|Description
---|---|---|
200|[OK](https://tools.ietf.org/html/rfc7231#section-6.3.1)|Destroy an item via its originator id
401|[Unauthorized](https://tools.ietf.org/html/rfc7235#section-3.1)|No description
403|[Forbidden](https://tools.ietf.org/html/rfc7231#section-6.5.3)|No description
422|[Unprocessable Entity](https://tools.ietf.org/html/rfc2518#section-10.3)|No description

> Example responses

```json
{
  "id": 0,
  "sku": "string",
  "title": "string",
  "description": "string",
  "original_location": "string",
  "created_at": "2017-06-19T15:15:48Z",
  "updated_at": "2017-06-19T15:15:48Z",
  "customer_id": 0,
  "quantity": 0,
  "weight": 0,
  "available": true,
  "image_file_name": "string",
  "image_content_type": "string",
  "image_file_size": 0,
  "image_updated_at": "2017-06-19T15:15:48Z",
  "image_originator_url": "string",
  "vendor": "string",
  "scancode": "string",
  "price": 0,
  "media_mail": true,
  "packaging": true,
  "length": 0,
  "width": 0,
  "height": 0,
  "active": true,
  "wholesale_cost": 0,
  "is_bundle": true,
  "packaging_type": "string",
  "promo": true,
  "street_date": "2017-06-19T15:15:48Z",
  "category": "string",
  "include_inbound_in_published": true,
  "returnable": true,
  "return_sku_match": "string",
  "return_price_restricted": true,
  "request_serial_number": true,
  "currency": "string",
  "tariff_number": "string",
  "label_format": "string",
  "notify_originator_inventory": 0,
  "name": "string"
}
```
```json
{
  "message": "string"
}
```
```json
{
  "message": "string"
}
```
```json
{
  "message": "string"
}
```
<aside class="success">
This operation does not require authentication
</aside>

## getApiV2ItemsOriginatorOriginatorIdInbound

> Code samples

```shell
# You can also use wget
curl -X get ://staging.whiplashmerch.com/api/v2/items/originator/{originator_id}/inbound \
  -H 'X-Customer-Id: string' \
  -H 'X-Shop-Id: string' \
  -H 'Accept: application/json'

```

```http
GET ://staging.whiplashmerch.com/api/v2/items/originator/{originator_id}/inbound HTTP/1.1
Host: staging.whiplashmerch.com

Accept: application/json
X-Customer-Id: string
X-Shop-Id: string

```

```javascript
var headers = {
  'X-Customer-Id':'string',
  'X-Shop-Id':'string',
  'Accept':'application/json'

};

$.ajax({
  url: '://staging.whiplashmerch.com/api/v2/items/originator/{originator_id}/inbound',
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
  'X-Customer-Id':'string',
  'X-Shop-Id':'string',
  'Accept':'application/json'

};

fetch('://staging.whiplashmerch.com/api/v2/items/originator/{originator_id}/inbound',
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
  'X-Customer-Id' => 'string',
  'X-Shop-Id' => 'string',
  'Accept' => 'application/json'
}

result = RestClient.get '://staging.whiplashmerch.com/api/v2/items/originator/{originator_id}/inbound', params: {
  }, headers: headers

p JSON.parse(result)
```

```python
import requests
headers = {
  'X-Customer-Id': 'string',
  'X-Shop-Id': 'string',
  'Accept': 'application/json'
}

r = requests.get('://staging.whiplashmerch.com/api/v2/items/originator/{originator_id}/inbound', params={

}, headers = headers)

print r.json()
```

```java
URL obj = new URL("://staging.whiplashmerch.com/api/v2/items/originator/{originator_id}/inbound");
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

`GET /api/v2/items/originator/{originator_id}/inbound`

*Shows all inbound ship notices containing this item via its originator id*

Shows all inbound ship notices containing this item via its originator id

### Parameters

Parameter|In|Type|Required|Description
---|---|---|---|---|
originator_id|path|integer|true|No description
X-Customer-Id|header|string|false|The customer associated with this resource.
X-Shop-Id|header|string|false|The shop associated with this resource.


### Responses

Status|Meaning|Description
---|---|---|
200|[OK](https://tools.ietf.org/html/rfc7231#section-6.3.1)|Shows all inbound ship notices containing this item via its originator id
401|[Unauthorized](https://tools.ietf.org/html/rfc7235#section-3.1)|No description
403|[Forbidden](https://tools.ietf.org/html/rfc7231#section-6.5.3)|No description

> Example responses

```json
{
  "id": 0,
  "sku": "string",
  "title": "string",
  "description": "string",
  "original_location": "string",
  "created_at": "2017-06-19T15:15:48Z",
  "updated_at": "2017-06-19T15:15:48Z",
  "customer_id": 0,
  "quantity": 0,
  "weight": 0,
  "available": true,
  "image_file_name": "string",
  "image_content_type": "string",
  "image_file_size": 0,
  "image_updated_at": "2017-06-19T15:15:48Z",
  "image_originator_url": "string",
  "vendor": "string",
  "scancode": "string",
  "price": 0,
  "media_mail": true,
  "packaging": true,
  "length": 0,
  "width": 0,
  "height": 0,
  "active": true,
  "wholesale_cost": 0,
  "is_bundle": true,
  "packaging_type": "string",
  "promo": true,
  "street_date": "2017-06-19T15:15:48Z",
  "category": "string",
  "include_inbound_in_published": true,
  "returnable": true,
  "return_sku_match": "string",
  "return_price_restricted": true,
  "request_serial_number": true,
  "currency": "string",
  "tariff_number": "string",
  "label_format": "string",
  "notify_originator_inventory": 0,
  "name": "string"
}
```
```json
{
  "message": "string"
}
```
```json
{
  "message": "string"
}
```
<aside class="success">
This operation does not require authentication
</aside>

## getApiV2ItemsOriginatorOriginatorIdInBundles

> Code samples

```shell
# You can also use wget
curl -X get ://staging.whiplashmerch.com/api/v2/items/originator/{originator_id}/in_bundles \
  -H 'X-Customer-Id: string' \
  -H 'X-Shop-Id: string' \
  -H 'Accept: application/json'

```

```http
GET ://staging.whiplashmerch.com/api/v2/items/originator/{originator_id}/in_bundles HTTP/1.1
Host: staging.whiplashmerch.com

Accept: application/json
X-Customer-Id: string
X-Shop-Id: string

```

```javascript
var headers = {
  'X-Customer-Id':'string',
  'X-Shop-Id':'string',
  'Accept':'application/json'

};

$.ajax({
  url: '://staging.whiplashmerch.com/api/v2/items/originator/{originator_id}/in_bundles',
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
  'X-Customer-Id':'string',
  'X-Shop-Id':'string',
  'Accept':'application/json'

};

fetch('://staging.whiplashmerch.com/api/v2/items/originator/{originator_id}/in_bundles',
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
  'X-Customer-Id' => 'string',
  'X-Shop-Id' => 'string',
  'Accept' => 'application/json'
}

result = RestClient.get '://staging.whiplashmerch.com/api/v2/items/originator/{originator_id}/in_bundles', params: {
  }, headers: headers

p JSON.parse(result)
```

```python
import requests
headers = {
  'X-Customer-Id': 'string',
  'X-Shop-Id': 'string',
  'Accept': 'application/json'
}

r = requests.get('://staging.whiplashmerch.com/api/v2/items/originator/{originator_id}/in_bundles', params={

}, headers = headers)

print r.json()
```

```java
URL obj = new URL("://staging.whiplashmerch.com/api/v2/items/originator/{originator_id}/in_bundles");
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

`GET /api/v2/items/originator/{originator_id}/in_bundles`

*Shows all instances of this item in bundles via its originator id*

Shows all instances of this item in bundles via its originator id

### Parameters

Parameter|In|Type|Required|Description
---|---|---|---|---|
originator_id|path|integer|true|No description
X-Customer-Id|header|string|false|The customer associated with this resource.
X-Shop-Id|header|string|false|The shop associated with this resource.


### Responses

Status|Meaning|Description
---|---|---|
200|[OK](https://tools.ietf.org/html/rfc7231#section-6.3.1)|Shows all instances of this item in bundles via its originator id
401|[Unauthorized](https://tools.ietf.org/html/rfc7235#section-3.1)|No description
403|[Forbidden](https://tools.ietf.org/html/rfc7231#section-6.5.3)|No description

> Example responses

```json
{
  "id": 0,
  "sku": "string",
  "title": "string",
  "description": "string",
  "original_location": "string",
  "created_at": "2017-06-19T15:15:48Z",
  "updated_at": "2017-06-19T15:15:48Z",
  "customer_id": 0,
  "quantity": 0,
  "weight": 0,
  "available": true,
  "image_file_name": "string",
  "image_content_type": "string",
  "image_file_size": 0,
  "image_updated_at": "2017-06-19T15:15:48Z",
  "image_originator_url": "string",
  "vendor": "string",
  "scancode": "string",
  "price": 0,
  "media_mail": true,
  "packaging": true,
  "length": 0,
  "width": 0,
  "height": 0,
  "active": true,
  "wholesale_cost": 0,
  "is_bundle": true,
  "packaging_type": "string",
  "promo": true,
  "street_date": "2017-06-19T15:15:48Z",
  "category": "string",
  "include_inbound_in_published": true,
  "returnable": true,
  "return_sku_match": "string",
  "return_price_restricted": true,
  "request_serial_number": true,
  "currency": "string",
  "tariff_number": "string",
  "label_format": "string",
  "notify_originator_inventory": 0,
  "name": "string"
}
```
```json
{
  "message": "string"
}
```
```json
{
  "message": "string"
}
```
<aside class="success">
This operation does not require authentication
</aside>

## getApiV2ItemsOriginatorOriginatorIdBundleItems

> Code samples

```shell
# You can also use wget
curl -X get ://staging.whiplashmerch.com/api/v2/items/originator/{originator_id}/bundle_items \
  -H 'X-Customer-Id: string' \
  -H 'X-Shop-Id: string' \
  -H 'Accept: application/json'

```

```http
GET ://staging.whiplashmerch.com/api/v2/items/originator/{originator_id}/bundle_items HTTP/1.1
Host: staging.whiplashmerch.com

Accept: application/json
X-Customer-Id: string
X-Shop-Id: string

```

```javascript
var headers = {
  'X-Customer-Id':'string',
  'X-Shop-Id':'string',
  'Accept':'application/json'

};

$.ajax({
  url: '://staging.whiplashmerch.com/api/v2/items/originator/{originator_id}/bundle_items',
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
  'X-Customer-Id':'string',
  'X-Shop-Id':'string',
  'Accept':'application/json'

};

fetch('://staging.whiplashmerch.com/api/v2/items/originator/{originator_id}/bundle_items',
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
  'X-Customer-Id' => 'string',
  'X-Shop-Id' => 'string',
  'Accept' => 'application/json'
}

result = RestClient.get '://staging.whiplashmerch.com/api/v2/items/originator/{originator_id}/bundle_items', params: {
  }, headers: headers

p JSON.parse(result)
```

```python
import requests
headers = {
  'X-Customer-Id': 'string',
  'X-Shop-Id': 'string',
  'Accept': 'application/json'
}

r = requests.get('://staging.whiplashmerch.com/api/v2/items/originator/{originator_id}/bundle_items', params={

}, headers = headers)

print r.json()
```

```java
URL obj = new URL("://staging.whiplashmerch.com/api/v2/items/originator/{originator_id}/bundle_items");
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

`GET /api/v2/items/originator/{originator_id}/bundle_items`

*Shows all bundles containing this item via its originator id*

Shows all bundles containing this item via its originator id

### Parameters

Parameter|In|Type|Required|Description
---|---|---|---|---|
originator_id|path|integer|true|No description
X-Customer-Id|header|string|false|The customer associated with this resource.
X-Shop-Id|header|string|false|The shop associated with this resource.


### Responses

Status|Meaning|Description
---|---|---|
200|[OK](https://tools.ietf.org/html/rfc7231#section-6.3.1)|Shows all bundles containing this item via its originator id
401|[Unauthorized](https://tools.ietf.org/html/rfc7235#section-3.1)|No description
403|[Forbidden](https://tools.ietf.org/html/rfc7231#section-6.5.3)|No description

> Example responses

```json
{
  "id": 0,
  "sku": "string",
  "title": "string",
  "description": "string",
  "original_location": "string",
  "created_at": "2017-06-19T15:15:48Z",
  "updated_at": "2017-06-19T15:15:48Z",
  "customer_id": 0,
  "quantity": 0,
  "weight": 0,
  "available": true,
  "image_file_name": "string",
  "image_content_type": "string",
  "image_file_size": 0,
  "image_updated_at": "2017-06-19T15:15:48Z",
  "image_originator_url": "string",
  "vendor": "string",
  "scancode": "string",
  "price": 0,
  "media_mail": true,
  "packaging": true,
  "length": 0,
  "width": 0,
  "height": 0,
  "active": true,
  "wholesale_cost": 0,
  "is_bundle": true,
  "packaging_type": "string",
  "promo": true,
  "street_date": "2017-06-19T15:15:48Z",
  "category": "string",
  "include_inbound_in_published": true,
  "returnable": true,
  "return_sku_match": "string",
  "return_price_restricted": true,
  "request_serial_number": true,
  "currency": "string",
  "tariff_number": "string",
  "label_format": "string",
  "notify_originator_inventory": 0,
  "name": "string"
}
```
```json
{
  "message": "string"
}
```
```json
{
  "message": "string"
}
```
<aside class="success">
This operation does not require authentication
</aside>

## getApiV2ItemsOriginatorOriginatorIdWarehouseQuantities

> Code samples

```shell
# You can also use wget
curl -X get ://staging.whiplashmerch.com/api/v2/items/originator/{originator_id}/warehouse_quantities \
  -H 'X-Customer-Id: string' \
  -H 'X-Shop-Id: string' \
  -H 'Accept: application/json'

```

```http
GET ://staging.whiplashmerch.com/api/v2/items/originator/{originator_id}/warehouse_quantities HTTP/1.1
Host: staging.whiplashmerch.com

Accept: application/json
X-Customer-Id: string
X-Shop-Id: string

```

```javascript
var headers = {
  'X-Customer-Id':'string',
  'X-Shop-Id':'string',
  'Accept':'application/json'

};

$.ajax({
  url: '://staging.whiplashmerch.com/api/v2/items/originator/{originator_id}/warehouse_quantities',
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
  'X-Customer-Id':'string',
  'X-Shop-Id':'string',
  'Accept':'application/json'

};

fetch('://staging.whiplashmerch.com/api/v2/items/originator/{originator_id}/warehouse_quantities',
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
  'X-Customer-Id' => 'string',
  'X-Shop-Id' => 'string',
  'Accept' => 'application/json'
}

result = RestClient.get '://staging.whiplashmerch.com/api/v2/items/originator/{originator_id}/warehouse_quantities', params: {
  }, headers: headers

p JSON.parse(result)
```

```python
import requests
headers = {
  'X-Customer-Id': 'string',
  'X-Shop-Id': 'string',
  'Accept': 'application/json'
}

r = requests.get('://staging.whiplashmerch.com/api/v2/items/originator/{originator_id}/warehouse_quantities', params={

}, headers = headers)

print r.json()
```

```java
URL obj = new URL("://staging.whiplashmerch.com/api/v2/items/originator/{originator_id}/warehouse_quantities");
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

`GET /api/v2/items/originator/{originator_id}/warehouse_quantities`

*Shows the number of this item in the warehouse via its originator id*

Shows the number of this item in the warehouse via its originator id

### Parameters

Parameter|In|Type|Required|Description
---|---|---|---|---|
originator_id|path|integer|true|No description
X-Customer-Id|header|string|false|The customer associated with this resource.
X-Shop-Id|header|string|false|The shop associated with this resource.


### Responses

Status|Meaning|Description
---|---|---|
200|[OK](https://tools.ietf.org/html/rfc7231#section-6.3.1)|Shows the number of this item in the warehouse via its originator id
401|[Unauthorized](https://tools.ietf.org/html/rfc7235#section-3.1)|No description
403|[Forbidden](https://tools.ietf.org/html/rfc7231#section-6.5.3)|No description

> Example responses

```json
{
  "id": 0,
  "sku": "string",
  "title": "string",
  "description": "string",
  "original_location": "string",
  "created_at": "2017-06-19T15:15:48Z",
  "updated_at": "2017-06-19T15:15:48Z",
  "customer_id": 0,
  "quantity": 0,
  "weight": 0,
  "available": true,
  "image_file_name": "string",
  "image_content_type": "string",
  "image_file_size": 0,
  "image_updated_at": "2017-06-19T15:15:48Z",
  "image_originator_url": "string",
  "vendor": "string",
  "scancode": "string",
  "price": 0,
  "media_mail": true,
  "packaging": true,
  "length": 0,
  "width": 0,
  "height": 0,
  "active": true,
  "wholesale_cost": 0,
  "is_bundle": true,
  "packaging_type": "string",
  "promo": true,
  "street_date": "2017-06-19T15:15:48Z",
  "category": "string",
  "include_inbound_in_published": true,
  "returnable": true,
  "return_sku_match": "string",
  "return_price_restricted": true,
  "request_serial_number": true,
  "currency": "string",
  "tariff_number": "string",
  "label_format": "string",
  "notify_originator_inventory": 0,
  "name": "string"
}
```
```json
{
  "message": "string"
}
```
```json
{
  "message": "string"
}
```
<aside class="success">
This operation does not require authentication
</aside>

## getApiV2ItemsIdTransactions

> Code samples

```shell
# You can also use wget
curl -X get ://staging.whiplashmerch.com/api/v2/items/{id}/transactions \
  -H 'Accept: application/json'

```

```http
GET ://staging.whiplashmerch.com/api/v2/items/{id}/transactions HTTP/1.1
Host: staging.whiplashmerch.com

Accept: application/json

```

```javascript
var headers = {
  'Accept':'application/json'

};

$.ajax({
  url: '://staging.whiplashmerch.com/api/v2/items/{id}/transactions',
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
  'Accept':'application/json'

};

fetch('://staging.whiplashmerch.com/api/v2/items/{id}/transactions',
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
  'Accept' => 'application/json'
}

result = RestClient.get '://staging.whiplashmerch.com/api/v2/items/{id}/transactions', params: {
  }, headers: headers

p JSON.parse(result)
```

```python
import requests
headers = {
  'Accept': 'application/json'
}

r = requests.get('://staging.whiplashmerch.com/api/v2/items/{id}/transactions', params={

}, headers = headers)

print r.json()
```

```java
URL obj = new URL("://staging.whiplashmerch.com/api/v2/items/{id}/transactions");
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

`GET /api/v2/items/{id}/transactions`

*Get all transactions for an item*

Get all transactions for an item

### Parameters

Parameter|In|Type|Required|Description
---|---|---|---|---|
search|query|string|false|JSON search string like {"attribute_eq": "Term"}
page|query|integer|false|Page of results to fetch.
per_page|query|integer|false|Number of results to return per page.
id|path|integer|true|No description


### Responses

Status|Meaning|Description
---|---|---|
200|[OK](https://tools.ietf.org/html/rfc7231#section-6.3.1)|Get all transactions for an item
401|[Unauthorized](https://tools.ietf.org/html/rfc7235#section-3.1)|No description
403|[Forbidden](https://tools.ietf.org/html/rfc7231#section-6.5.3)|No description

> Example responses

```json
{
  "id": 0,
  "item_id": 0,
  "description": "string",
  "quantity": 0,
  "created_at": "2017-06-19T15:15:48Z",
  "updated_at": "2017-06-19T15:15:48Z",
  "change": 0,
  "order_id": 0,
  "shipnotice_id": 0,
  "user_id": 0,
  "rule_id": 0
}
```
```json
{
  "message": "string"
}
```
```json
{
  "message": "string"
}
```
<aside class="success">
This operation does not require authentication
</aside>

## getApiV2ItemsIdTransactionsCount

> Code samples

```shell
# You can also use wget
curl -X get ://staging.whiplashmerch.com/api/v2/items/{id}/transactions/count \
  -H 'Accept: application/json'

```

```http
GET ://staging.whiplashmerch.com/api/v2/items/{id}/transactions/count HTTP/1.1
Host: staging.whiplashmerch.com

Accept: application/json

```

```javascript
var headers = {
  'Accept':'application/json'

};

$.ajax({
  url: '://staging.whiplashmerch.com/api/v2/items/{id}/transactions/count',
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
  'Accept':'application/json'

};

fetch('://staging.whiplashmerch.com/api/v2/items/{id}/transactions/count',
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
  'Accept' => 'application/json'
}

result = RestClient.get '://staging.whiplashmerch.com/api/v2/items/{id}/transactions/count', params: {
  }, headers: headers

p JSON.parse(result)
```

```python
import requests
headers = {
  'Accept': 'application/json'
}

r = requests.get('://staging.whiplashmerch.com/api/v2/items/{id}/transactions/count', params={

}, headers = headers)

print r.json()
```

```java
URL obj = new URL("://staging.whiplashmerch.com/api/v2/items/{id}/transactions/count");
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

`GET /api/v2/items/{id}/transactions/count`

*Returns count of item transactions*

Returns count of item transactions

### Parameters

Parameter|In|Type|Required|Description
---|---|---|---|---|
search|query|string|false|JSON search string like {"attribute_eq": "Term"}
id|path|integer|true|No description


### Responses

Status|Meaning|Description
---|---|---|
200|[OK](https://tools.ietf.org/html/rfc7231#section-6.3.1)|Returns count of item transactions
401|[Unauthorized](https://tools.ietf.org/html/rfc7235#section-3.1)|No description
403|[Forbidden](https://tools.ietf.org/html/rfc7231#section-6.5.3)|No description

> Example responses

```json
{
  "id": 0,
  "item_id": 0,
  "description": "string",
  "quantity": 0,
  "created_at": "2017-06-19T15:15:48Z",
  "updated_at": "2017-06-19T15:15:48Z",
  "change": 0,
  "order_id": 0,
  "shipnotice_id": 0,
  "user_id": 0,
  "rule_id": 0
}
```
```json
{
  "message": "string"
}
```
```json
{
  "message": "string"
}
```
<aside class="success">
This operation does not require authentication
</aside>

# originators

Operations about originators

## putApiV2OriginatorsId

> Code samples

```shell
# You can also use wget
curl -X put ://staging.whiplashmerch.com/api/v2/originators/{id} \
  -H 'X-Customer-Id: string' \
  -H 'X-Shop-Id: string' \
  -H 'Content-Type: application/json' \
  -H 'Accept: application/json'

```

```http
PUT ://staging.whiplashmerch.com/api/v2/originators/{id} HTTP/1.1
Host: staging.whiplashmerch.com
Content-Type: application/json
Accept: application/json
X-Customer-Id: string
X-Shop-Id: string

```

```javascript
var headers = {
  'X-Customer-Id':'string',
  'X-Shop-Id':'string',
  'Content-Type':'application/json',
  'Accept':'application/json'

};

$.ajax({
  url: '://staging.whiplashmerch.com/api/v2/originators/{id}',
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
  'X-Customer-Id':'string',
  'X-Shop-Id':'string',
  'Content-Type':'application/json',
  'Accept':'application/json'

};

fetch('://staging.whiplashmerch.com/api/v2/originators/{id}',
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
  'X-Customer-Id' => 'string',
  'X-Shop-Id' => 'string',
  'Content-Type' => 'application/json',
  'Accept' => 'application/json'
}

result = RestClient.put '://staging.whiplashmerch.com/api/v2/originators/{id}', params: {
  }, headers: headers

p JSON.parse(result)
```

```python
import requests
headers = {
  'X-Customer-Id': 'string',
  'X-Shop-Id': 'string',
  'Content-Type': 'application/json',
  'Accept': 'application/json'
}

r = requests.put('://staging.whiplashmerch.com/api/v2/originators/{id}', params={

}, headers = headers)

print r.json()
```

```java
URL obj = new URL("://staging.whiplashmerch.com/api/v2/originators/{id}");
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

`PUT /api/v2/originators/{id}`

*Update an originator*

Update an originator

### Parameters

Parameter|In|Type|Required|Description
---|---|---|---|---|
X-Customer-Id|header|string|false|The customer associated with this resource.
X-Shop-Id|header|string|false|The shop associated with this resource.
id|path|integer|true|the originator id
originated_id|formData|integer|false|the id of the object created by the originator
originated_type|formData|string|false|the type of object created by the originator
shop_id|formData|integer|false|the originator shop id
provider|formData|string|false|the originator provider (shopify, magento, bandcamp, etc)
original_id|formData|string|false|the originator original id (from the provider)
group_id|formData|string|false|the originator group id
address_id|formData|string|false|the originator address id
active|formData|boolean|false|is the originator active?
integration_id|formData|integer|false|the originator integration id
last_notified_at|formData|string|false|the originator last notified date and time
last_notification_status|formData|string|false|the originator last notification status
distinct_originator_key|formData|string|false|the originator distinct key
created_at|formData|string|false|the originator creation date and time
updated_at|formData|string|false|the originator last update date and time


### Responses

Status|Meaning|Description
---|---|---|
200|[OK](https://tools.ietf.org/html/rfc7231#section-6.3.1)|Update an originator
401|[Unauthorized](https://tools.ietf.org/html/rfc7235#section-3.1)|No description
403|[Forbidden](https://tools.ietf.org/html/rfc7231#section-6.5.3)|No description
422|[Unprocessable Entity](https://tools.ietf.org/html/rfc2518#section-10.3)|No description

> Example responses

```json
{
  "id": 0,
  "originated_id": 0,
  "originated_type": "string",
  "shop_id": 0,
  "provider": "string",
  "original_id": "string",
  "group_id": "string",
  "address_id": "string",
  "active": true,
  "integration_id": 0,
  "last_notified_at": "2017-06-19T15:15:48Z",
  "last_notification_status": "string",
  "distinct_originator_key": "string",
  "created_at": "2017-06-19T15:15:48Z",
  "updated_at": "2017-06-19T15:15:48Z"
}
```
```json
{
  "message": "string"
}
```
```json
{
  "message": "string"
}
```
```json
{
  "message": "string"
}
```
<aside class="success">
This operation does not require authentication
</aside>

# customers

Operations about customers

## getApiV2Customers

> Code samples

```shell
# You can also use wget
curl -X get ://staging.whiplashmerch.com/api/v2/customers \
  -H 'Accept: application/json'

```

```http
GET ://staging.whiplashmerch.com/api/v2/customers HTTP/1.1
Host: staging.whiplashmerch.com

Accept: application/json

```

```javascript
var headers = {
  'Accept':'application/json'

};

$.ajax({
  url: '://staging.whiplashmerch.com/api/v2/customers',
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
  'Accept':'application/json'

};

fetch('://staging.whiplashmerch.com/api/v2/customers',
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
  'Accept' => 'application/json'
}

result = RestClient.get '://staging.whiplashmerch.com/api/v2/customers', params: {
  }, headers: headers

p JSON.parse(result)
```

```python
import requests
headers = {
  'Accept': 'application/json'
}

r = requests.get('://staging.whiplashmerch.com/api/v2/customers', params={

}, headers = headers)

print r.json()
```

```java
URL obj = new URL("://staging.whiplashmerch.com/api/v2/customers");
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

`GET /api/v2/customers`

*Get all customers*

Get all customers

### Parameters

Parameter|In|Type|Required|Description
---|---|---|---|---|
search|query|string|false|JSON search string like {"attribute_eq": "Term"}
fields|query|string|false|Comma-separated list of fields to include in the response


### Responses

Status|Meaning|Description
---|---|---|
200|[OK](https://tools.ietf.org/html/rfc7231#section-6.3.1)|Get all customers
|Unknown|No description

> Example responses

```json
{
  "id": 0,
  "name": "string",
  "created_at": "2017-06-19T15:15:48Z",
  "active": true,
  "auto_merge_gestation": 0,
  "balance": 0,
  "default_warehouse_id": 0,
  "eori_number": "string",
  "estimated_monthly_volume": "string",
  "fedex_account": "string",
  "from_email": "string",
  "instructions": "string",
  "item_scanning_preference": true,
  "label_format": "string",
  "minimum_storage_qty": 0,
  "notes": "string",
  "notify_originator": true,
  "notify_originator_inventory": 0,
  "originator_permissions": true,
  "packing_slip_msg": "string",
  "packingslip_template": "string",
  "partner_id": 0,
  "request_serial_numbers": true,
  "ship_method_preference": 0,
  "shipping_name": "string",
  "ups_account": "string",
  "vat_number": "string",
  "warehouse_fallback": 0,
  "activated_at": "2017-06-19T15:15:48Z",
  "deactivated_at": "2017-06-19T15:15:48Z",
  "authentication_token": "string",
  "auto_merge_skus": true,
  "billing_email": "string",
  "billing_contact_name": "string",
  "billing_company": "string",
  "billing_phone1": "string",
  "billing_phone2": "string",
  "billing_address1": "string",
  "billing_address2": "string",
  "billing_address3": "string",
  "billing_city": "string",
  "billing_state": "string",
  "billing_zip": "string",
  "billing_country": "string",
  "billing_residential": true,
  "items_returnable": true,
  "return_time_limit": 0,
  "return_label_expires_in": 0,
  "return_price_restricted": true,
  "return_sku_match": "string",
  "rma_display_logo": true,
  "rma_footer_content": "string",
  "return_email": "string",
  "return_phone": "string",
  "return_address_1": "string",
  "return_address_2": "string",
  "return_city": "string",
  "return_state": "string",
  "return_zip": "string",
  "return_country": "string",
  "logo_content_type": "string",
  "logo_file_name": "string",
  "logo_file_size": 0,
  "logo_updated_at": "2017-06-19T15:15:48Z",
  "full_logo_url": "string",
  "email_confirmation_from": "string",
  "email_confirmation_name": "string",
  "email_confirmation_msg": "string",
  "email_confirmation_preference": 0,
  "email_confirmation_template": "string"
}
```
```json
{
  "message": "string"
}
```
<aside class="success">
This operation does not require authentication
</aside>

## postApiV2Customers

> Code samples

```shell
# You can also use wget
curl -X post ://staging.whiplashmerch.com/api/v2/customers \
  -H 'Content-Type: application/json' \
  -H 'Accept: application/json'

```

```http
POST ://staging.whiplashmerch.com/api/v2/customers HTTP/1.1
Host: staging.whiplashmerch.com
Content-Type: application/json
Accept: application/json

```

```javascript
var headers = {
  'Content-Type':'application/json',
  'Accept':'application/json'

};

$.ajax({
  url: '://staging.whiplashmerch.com/api/v2/customers',
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
  'Content-Type':'application/json',
  'Accept':'application/json'

};

fetch('://staging.whiplashmerch.com/api/v2/customers',
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
  'Content-Type' => 'application/json',
  'Accept' => 'application/json'
}

result = RestClient.post '://staging.whiplashmerch.com/api/v2/customers', params: {
  }, headers: headers

p JSON.parse(result)
```

```python
import requests
headers = {
  'Content-Type': 'application/json',
  'Accept': 'application/json'
}

r = requests.post('://staging.whiplashmerch.com/api/v2/customers', params={

}, headers = headers)

print r.json()
```

```java
URL obj = new URL("://staging.whiplashmerch.com/api/v2/customers");
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

`POST /api/v2/customers`

*Create a customer*

Create a customer

### Parameters

Parameter|In|Type|Required|Description
---|---|---|---|---|
name|formData|string|false|Customer name.
billing_email|formData|string|false|Customer billing email.
active|formData|boolean|false|Customer active?
auto_merge_gestation|formData|integer|false|Customer auto merge gestation.
balance|formData|number|false|Customer account balance.
default_warehouse_id|formData|integer|false|Customer default warehouse id.
eori_number|formData|string|false|Customer EORI number.
estimated_monthly_volume|formData|string|false|Customer estimated monthly volume.
fedex_account|formData|string|false|Customer FedEx account.
from_email|formData|string|false|Customer from email.
instructions|formData|string|false|Customer instructions.
item_scanning_preference|formData|boolean|false|Customer has item scanning preference?
label_format|formData|string|false|Customer label format.
minimum_storage_qty|formData|number|false|Customer minimum storage quantity.
notes|formData|string|false|Customer notes.
notify_originator|formData|boolean|false|notify originator?
notify_originator_inventory|formData|integer|false|Customer notify originator inventory.
originator_permissions|formData|boolean|false|originator permissions?
packing_slip_msg|formData|string|false|Customer packing slip message.
packingslip_template|formData|string|false|Customer packing slip template.
partner_id|formData|integer|false|Customer partner id.
request_serial_numbers|formData|boolean|false|request serial numbers?
ship_method_preference|formData|integer|false|Customer shipping method preference.
shipping_name|formData|string|false|Customer shipping name.
ups_account|formData|string|false|Customer UPS account.
vat_number|formData|string|false|Customer VAT number.
warehouse_fallback|formData|integer|false|Customer warehouse fallback.
authentication_token|formData|string|false|No description
auto_merge_skus|formData|boolean|false|auto merge SKUs?
billing_contact_name|formData|string|false|Customer billing contact name.
billing_company|formData|string|false|Customer billing company.
billing_phone1|formData|string|false|Customer phone 1.
billing_phone2|formData|string|false|Customer phone 2.
billing_address1|formData|string|false|Customer billing address line 1.
billing_address2|formData|string|false|Customer billing address line 2.
billing_address3|formData|string|false|Customer billing address line 3.
billing_city|formData|string|false|Customer billing city.
billing_state|formData|string|false|Customer billing state.
billing_zip|formData|string|false|Customer billing zip.
billing_country|formData|string|false|Customer billing country.
billing_residential|formData|boolean|false|Customer billing residential?
items_returnable|formData|boolean|false|items returnable by default?
return_time_limit|formData|integer|false|Return time limit.
return_label_expires_in|formData|integer|false|Return label expiration time limit.
return_price_restricted|formData|boolean|false|limit exchange to same value or less?
return_sku_match|formData|string|false|Exchange SKU match policy.
rma_display_logo|formData|boolean|false|display customer logo on returns page?
rma_footer_content|formData|string|false|Return page footer content.
return_email|formData|string|false|Customer return email.
return_phone|formData|string|false|Customer return phone.
return_address_1|formData|string|false|Customer return address line 1.
return_address_2|formData|string|false|Customer return address line 2.
return_city|formData|string|false|Customer return city.
return_state|formData|string|false|Customer return state.
return_zip|formData|string|false|Customer return zip.
return_country|formData|string|false|Customer return country.
logo_content_type|formData|string|false|Customer logo content type.
logo_file_name|formData|string|false|Customer logo file name.
logo_file_size|formData|integer|false|Customer logo file size.
logo_updated_at|formData|string|false|Customer logo updated at.
full_logo_url|formData|string|false|Customer full logo url.
email_confirmation_from|formData|string|false|Customer email confirmation from.
email_confirmation_name|formData|string|false|Customer email confirmation name.
email_confirmation_msg|formData|string|false|Customer email confirmation message.
email_confirmation_preference|formData|integer|false|Customer email confirmation preference.
email_confirmation_template|formData|string|false|Customer email confirmation template.


### Responses

Status|Meaning|Description
---|---|---|
201|[Created](https://tools.ietf.org/html/rfc7231#section-6.3.2)|Create a customer
|Unknown|No description

> Example responses

```json
{
  "id": 0,
  "name": "string",
  "created_at": "2017-06-19T15:15:48Z",
  "active": true,
  "auto_merge_gestation": 0,
  "balance": 0,
  "default_warehouse_id": 0,
  "eori_number": "string",
  "estimated_monthly_volume": "string",
  "fedex_account": "string",
  "from_email": "string",
  "instructions": "string",
  "item_scanning_preference": true,
  "label_format": "string",
  "minimum_storage_qty": 0,
  "notes": "string",
  "notify_originator": true,
  "notify_originator_inventory": 0,
  "originator_permissions": true,
  "packing_slip_msg": "string",
  "packingslip_template": "string",
  "partner_id": 0,
  "request_serial_numbers": true,
  "ship_method_preference": 0,
  "shipping_name": "string",
  "ups_account": "string",
  "vat_number": "string",
  "warehouse_fallback": 0,
  "activated_at": "2017-06-19T15:15:48Z",
  "deactivated_at": "2017-06-19T15:15:48Z",
  "authentication_token": "string",
  "auto_merge_skus": true,
  "billing_email": "string",
  "billing_contact_name": "string",
  "billing_company": "string",
  "billing_phone1": "string",
  "billing_phone2": "string",
  "billing_address1": "string",
  "billing_address2": "string",
  "billing_address3": "string",
  "billing_city": "string",
  "billing_state": "string",
  "billing_zip": "string",
  "billing_country": "string",
  "billing_residential": true,
  "items_returnable": true,
  "return_time_limit": 0,
  "return_label_expires_in": 0,
  "return_price_restricted": true,
  "return_sku_match": "string",
  "rma_display_logo": true,
  "rma_footer_content": "string",
  "return_email": "string",
  "return_phone": "string",
  "return_address_1": "string",
  "return_address_2": "string",
  "return_city": "string",
  "return_state": "string",
  "return_zip": "string",
  "return_country": "string",
  "logo_content_type": "string",
  "logo_file_name": "string",
  "logo_file_size": 0,
  "logo_updated_at": "2017-06-19T15:15:48Z",
  "full_logo_url": "string",
  "email_confirmation_from": "string",
  "email_confirmation_name": "string",
  "email_confirmation_msg": "string",
  "email_confirmation_preference": 0,
  "email_confirmation_template": "string"
}
```
```json
{
  "message": "string"
}
```
<aside class="success">
This operation does not require authentication
</aside>

## getApiV2CustomersCount

> Code samples

```shell
# You can also use wget
curl -X get ://staging.whiplashmerch.com/api/v2/customers/count \
  -H 'Accept: application/json'

```

```http
GET ://staging.whiplashmerch.com/api/v2/customers/count HTTP/1.1
Host: staging.whiplashmerch.com

Accept: application/json

```

```javascript
var headers = {
  'Accept':'application/json'

};

$.ajax({
  url: '://staging.whiplashmerch.com/api/v2/customers/count',
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
  'Accept':'application/json'

};

fetch('://staging.whiplashmerch.com/api/v2/customers/count',
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
  'Accept' => 'application/json'
}

result = RestClient.get '://staging.whiplashmerch.com/api/v2/customers/count', params: {
  }, headers: headers

p JSON.parse(result)
```

```python
import requests
headers = {
  'Accept': 'application/json'
}

r = requests.get('://staging.whiplashmerch.com/api/v2/customers/count', params={

}, headers = headers)

print r.json()
```

```java
URL obj = new URL("://staging.whiplashmerch.com/api/v2/customers/count");
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

`GET /api/v2/customers/count`

*Count of all customers*

Count of all customers

### Parameters

Parameter|In|Type|Required|Description
---|---|---|---|---|
search|query|string|false|JSON search string like {"attribute_eq": "Term"}


### Responses

Status|Meaning|Description
---|---|---|
200|[OK](https://tools.ietf.org/html/rfc7231#section-6.3.1)|Count of all customers
|Unknown|No description

> Example responses

```json
{
  "id": 0,
  "name": "string",
  "created_at": "2017-06-19T15:15:48Z",
  "active": true,
  "auto_merge_gestation": 0,
  "balance": 0,
  "default_warehouse_id": 0,
  "eori_number": "string",
  "estimated_monthly_volume": "string",
  "fedex_account": "string",
  "from_email": "string",
  "instructions": "string",
  "item_scanning_preference": true,
  "label_format": "string",
  "minimum_storage_qty": 0,
  "notes": "string",
  "notify_originator": true,
  "notify_originator_inventory": 0,
  "originator_permissions": true,
  "packing_slip_msg": "string",
  "packingslip_template": "string",
  "partner_id": 0,
  "request_serial_numbers": true,
  "ship_method_preference": 0,
  "shipping_name": "string",
  "ups_account": "string",
  "vat_number": "string",
  "warehouse_fallback": 0,
  "activated_at": "2017-06-19T15:15:48Z",
  "deactivated_at": "2017-06-19T15:15:48Z",
  "authentication_token": "string",
  "auto_merge_skus": true,
  "billing_email": "string",
  "billing_contact_name": "string",
  "billing_company": "string",
  "billing_phone1": "string",
  "billing_phone2": "string",
  "billing_address1": "string",
  "billing_address2": "string",
  "billing_address3": "string",
  "billing_city": "string",
  "billing_state": "string",
  "billing_zip": "string",
  "billing_country": "string",
  "billing_residential": true,
  "items_returnable": true,
  "return_time_limit": 0,
  "return_label_expires_in": 0,
  "return_price_restricted": true,
  "return_sku_match": "string",
  "rma_display_logo": true,
  "rma_footer_content": "string",
  "return_email": "string",
  "return_phone": "string",
  "return_address_1": "string",
  "return_address_2": "string",
  "return_city": "string",
  "return_state": "string",
  "return_zip": "string",
  "return_country": "string",
  "logo_content_type": "string",
  "logo_file_name": "string",
  "logo_file_size": 0,
  "logo_updated_at": "2017-06-19T15:15:48Z",
  "full_logo_url": "string",
  "email_confirmation_from": "string",
  "email_confirmation_name": "string",
  "email_confirmation_msg": "string",
  "email_confirmation_preference": 0,
  "email_confirmation_template": "string"
}
```
```json
{
  "message": "string"
}
```
<aside class="success">
This operation does not require authentication
</aside>

## getApiV2CustomersId

> Code samples

```shell
# You can also use wget
curl -X get ://staging.whiplashmerch.com/api/v2/customers/{id} \
  -H 'Accept: application/json'

```

```http
GET ://staging.whiplashmerch.com/api/v2/customers/{id} HTTP/1.1
Host: staging.whiplashmerch.com

Accept: application/json

```

```javascript
var headers = {
  'Accept':'application/json'

};

$.ajax({
  url: '://staging.whiplashmerch.com/api/v2/customers/{id}',
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
  'Accept':'application/json'

};

fetch('://staging.whiplashmerch.com/api/v2/customers/{id}',
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
  'Accept' => 'application/json'
}

result = RestClient.get '://staging.whiplashmerch.com/api/v2/customers/{id}', params: {
  }, headers: headers

p JSON.parse(result)
```

```python
import requests
headers = {
  'Accept': 'application/json'
}

r = requests.get('://staging.whiplashmerch.com/api/v2/customers/{id}', params={

}, headers = headers)

print r.json()
```

```java
URL obj = new URL("://staging.whiplashmerch.com/api/v2/customers/{id}");
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

`GET /api/v2/customers/{id}`

*Get a customer*

Get a customer

### Parameters

Parameter|In|Type|Required|Description
---|---|---|---|---|
id|path|integer|true|No description


### Responses

Status|Meaning|Description
---|---|---|
200|[OK](https://tools.ietf.org/html/rfc7231#section-6.3.1)|Get a customer
|Unknown|No description

> Example responses

```json
{
  "id": 0,
  "name": "string",
  "created_at": "2017-06-19T15:15:48Z",
  "active": true,
  "auto_merge_gestation": 0,
  "balance": 0,
  "default_warehouse_id": 0,
  "eori_number": "string",
  "estimated_monthly_volume": "string",
  "fedex_account": "string",
  "from_email": "string",
  "instructions": "string",
  "item_scanning_preference": true,
  "label_format": "string",
  "minimum_storage_qty": 0,
  "notes": "string",
  "notify_originator": true,
  "notify_originator_inventory": 0,
  "originator_permissions": true,
  "packing_slip_msg": "string",
  "packingslip_template": "string",
  "partner_id": 0,
  "request_serial_numbers": true,
  "ship_method_preference": 0,
  "shipping_name": "string",
  "ups_account": "string",
  "vat_number": "string",
  "warehouse_fallback": 0,
  "activated_at": "2017-06-19T15:15:48Z",
  "deactivated_at": "2017-06-19T15:15:48Z",
  "authentication_token": "string",
  "auto_merge_skus": true,
  "billing_email": "string",
  "billing_contact_name": "string",
  "billing_company": "string",
  "billing_phone1": "string",
  "billing_phone2": "string",
  "billing_address1": "string",
  "billing_address2": "string",
  "billing_address3": "string",
  "billing_city": "string",
  "billing_state": "string",
  "billing_zip": "string",
  "billing_country": "string",
  "billing_residential": true,
  "items_returnable": true,
  "return_time_limit": 0,
  "return_label_expires_in": 0,
  "return_price_restricted": true,
  "return_sku_match": "string",
  "rma_display_logo": true,
  "rma_footer_content": "string",
  "return_email": "string",
  "return_phone": "string",
  "return_address_1": "string",
  "return_address_2": "string",
  "return_city": "string",
  "return_state": "string",
  "return_zip": "string",
  "return_country": "string",
  "logo_content_type": "string",
  "logo_file_name": "string",
  "logo_file_size": 0,
  "logo_updated_at": "2017-06-19T15:15:48Z",
  "full_logo_url": "string",
  "email_confirmation_from": "string",
  "email_confirmation_name": "string",
  "email_confirmation_msg": "string",
  "email_confirmation_preference": 0,
  "email_confirmation_template": "string"
}
```
```json
{
  "message": "string"
}
```
<aside class="success">
This operation does not require authentication
</aside>

## putApiV2CustomersId

> Code samples

```shell
# You can also use wget
curl -X put ://staging.whiplashmerch.com/api/v2/customers/{id} \
  -H 'Content-Type: application/json' \
  -H 'Accept: application/json'

```

```http
PUT ://staging.whiplashmerch.com/api/v2/customers/{id} HTTP/1.1
Host: staging.whiplashmerch.com
Content-Type: application/json
Accept: application/json

```

```javascript
var headers = {
  'Content-Type':'application/json',
  'Accept':'application/json'

};

$.ajax({
  url: '://staging.whiplashmerch.com/api/v2/customers/{id}',
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
  'Content-Type':'application/json',
  'Accept':'application/json'

};

fetch('://staging.whiplashmerch.com/api/v2/customers/{id}',
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
  'Content-Type' => 'application/json',
  'Accept' => 'application/json'
}

result = RestClient.put '://staging.whiplashmerch.com/api/v2/customers/{id}', params: {
  }, headers: headers

p JSON.parse(result)
```

```python
import requests
headers = {
  'Content-Type': 'application/json',
  'Accept': 'application/json'
}

r = requests.put('://staging.whiplashmerch.com/api/v2/customers/{id}', params={

}, headers = headers)

print r.json()
```

```java
URL obj = new URL("://staging.whiplashmerch.com/api/v2/customers/{id}");
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

`PUT /api/v2/customers/{id}`

*Update a customer*

Update a customer

### Parameters

Parameter|In|Type|Required|Description
---|---|---|---|---|
name|formData|string|false|Customer name.
active|formData|boolean|false|Customer active?
auto_merge_gestation|formData|integer|false|Customer auto merge gestation.
balance|formData|number|false|Customer account balance.
default_warehouse_id|formData|integer|false|Customer default warehouse id.
eori_number|formData|string|false|Customer EORI number.
estimated_monthly_volume|formData|string|false|Customer estimated monthly volume.
fedex_account|formData|string|false|Customer FedEx account.
from_email|formData|string|false|Customer from email.
instructions|formData|string|false|Customer instructions.
item_scanning_preference|formData|boolean|false|Customer has item scanning preference?
label_format|formData|string|false|Customer label format.
minimum_storage_qty|formData|number|false|Customer minimum storage quantity.
notes|formData|string|false|Customer notes.
notify_originator|formData|boolean|false|notify originator?
notify_originator_inventory|formData|integer|false|Customer notify originator inventory.
originator_permissions|formData|boolean|false|originator permissions?
packing_slip_msg|formData|string|false|Customer packing slip message.
packingslip_template|formData|string|false|Customer packing slip template.
partner_id|formData|integer|false|Customer partner id.
request_serial_numbers|formData|boolean|false|request serial numbers?
ship_method_preference|formData|integer|false|Customer shipping method preference.
shipping_name|formData|string|false|Customer shipping name.
ups_account|formData|string|false|Customer UPS account.
vat_number|formData|string|false|Customer VAT number.
warehouse_fallback|formData|integer|false|Customer warehouse fallback.
authentication_token|formData|string|false|No description
auto_merge_skus|formData|boolean|false|auto merge SKUs?
billing_email|formData|string|false|Customer billing email.
billing_contact_name|formData|string|false|Customer billing contact name.
billing_company|formData|string|false|Customer billing company.
billing_phone1|formData|string|false|Customer phone 1.
billing_phone2|formData|string|false|Customer phone 2.
billing_address1|formData|string|false|Customer billing address line 1.
billing_address2|formData|string|false|Customer billing address line 2.
billing_address3|formData|string|false|Customer billing address line 3.
billing_city|formData|string|false|Customer billing city.
billing_state|formData|string|false|Customer billing state.
billing_zip|formData|string|false|Customer billing zip.
billing_country|formData|string|false|Customer billing country.
billing_residential|formData|boolean|false|Customer billing residential?
items_returnable|formData|boolean|false|items returnable by default?
return_time_limit|formData|integer|false|Return time limit.
return_label_expires_in|formData|integer|false|Return label expiration time limit.
return_price_restricted|formData|boolean|false|limit exchange to same value or less?
return_sku_match|formData|string|false|Exchange SKU match policy.
rma_display_logo|formData|boolean|false|display customer logo on returns page?
rma_footer_content|formData|string|false|Return page footer content.
return_email|formData|string|false|Customer return email.
return_phone|formData|string|false|Customer return phone.
return_address_1|formData|string|false|Customer return address line 1.
return_address_2|formData|string|false|Customer return address line 2.
return_city|formData|string|false|Customer return city.
return_state|formData|string|false|Customer return state.
return_zip|formData|string|false|Customer return zip.
return_country|formData|string|false|Customer return country.
logo_content_type|formData|string|false|Customer logo content type.
logo_file_name|formData|string|false|Customer logo file name.
logo_file_size|formData|integer|false|Customer logo file size.
logo_updated_at|formData|string|false|Customer logo updated at.
full_logo_url|formData|string|false|Customer full logo url.
email_confirmation_from|formData|string|false|Customer email confirmation from.
email_confirmation_name|formData|string|false|Customer email confirmation name.
email_confirmation_msg|formData|string|false|Customer email confirmation message.
email_confirmation_preference|formData|integer|false|Customer email confirmation preference.
email_confirmation_template|formData|string|false|Customer email confirmation template.
id|path|integer|true|No description


### Responses

Status|Meaning|Description
---|---|---|
200|[OK](https://tools.ietf.org/html/rfc7231#section-6.3.1)|Update a customer
|Unknown|No description

> Example responses

```json
{
  "id": 0,
  "name": "string",
  "created_at": "2017-06-19T15:15:48Z",
  "active": true,
  "auto_merge_gestation": 0,
  "balance": 0,
  "default_warehouse_id": 0,
  "eori_number": "string",
  "estimated_monthly_volume": "string",
  "fedex_account": "string",
  "from_email": "string",
  "instructions": "string",
  "item_scanning_preference": true,
  "label_format": "string",
  "minimum_storage_qty": 0,
  "notes": "string",
  "notify_originator": true,
  "notify_originator_inventory": 0,
  "originator_permissions": true,
  "packing_slip_msg": "string",
  "packingslip_template": "string",
  "partner_id": 0,
  "request_serial_numbers": true,
  "ship_method_preference": 0,
  "shipping_name": "string",
  "ups_account": "string",
  "vat_number": "string",
  "warehouse_fallback": 0,
  "activated_at": "2017-06-19T15:15:48Z",
  "deactivated_at": "2017-06-19T15:15:48Z",
  "authentication_token": "string",
  "auto_merge_skus": true,
  "billing_email": "string",
  "billing_contact_name": "string",
  "billing_company": "string",
  "billing_phone1": "string",
  "billing_phone2": "string",
  "billing_address1": "string",
  "billing_address2": "string",
  "billing_address3": "string",
  "billing_city": "string",
  "billing_state": "string",
  "billing_zip": "string",
  "billing_country": "string",
  "billing_residential": true,
  "items_returnable": true,
  "return_time_limit": 0,
  "return_label_expires_in": 0,
  "return_price_restricted": true,
  "return_sku_match": "string",
  "rma_display_logo": true,
  "rma_footer_content": "string",
  "return_email": "string",
  "return_phone": "string",
  "return_address_1": "string",
  "return_address_2": "string",
  "return_city": "string",
  "return_state": "string",
  "return_zip": "string",
  "return_country": "string",
  "logo_content_type": "string",
  "logo_file_name": "string",
  "logo_file_size": 0,
  "logo_updated_at": "2017-06-19T15:15:48Z",
  "full_logo_url": "string",
  "email_confirmation_from": "string",
  "email_confirmation_name": "string",
  "email_confirmation_msg": "string",
  "email_confirmation_preference": 0,
  "email_confirmation_template": "string"
}
```
```json
{
  "message": "string"
}
```
<aside class="success">
This operation does not require authentication
</aside>

## putApiV2CustomersIdCallAction

> Code samples

```shell
# You can also use wget
curl -X put ://staging.whiplashmerch.com/api/v2/customers/{id}/call/{action} \
  -H 'Content-Type: application/json' \
  -H 'Accept: application/json'

```

```http
PUT ://staging.whiplashmerch.com/api/v2/customers/{id}/call/{action} HTTP/1.1
Host: staging.whiplashmerch.com
Content-Type: application/json
Accept: application/json

```

```javascript
var headers = {
  'Content-Type':'application/json',
  'Accept':'application/json'

};

$.ajax({
  url: '://staging.whiplashmerch.com/api/v2/customers/{id}/call/{action}',
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
  'Content-Type':'application/json',
  'Accept':'application/json'

};

fetch('://staging.whiplashmerch.com/api/v2/customers/{id}/call/{action}',
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
  'Content-Type' => 'application/json',
  'Accept' => 'application/json'
}

result = RestClient.put '://staging.whiplashmerch.com/api/v2/customers/{id}/call/{action}', params: {
  }, headers: headers

p JSON.parse(result)
```

```python
import requests
headers = {
  'Content-Type': 'application/json',
  'Accept': 'application/json'
}

r = requests.put('://staging.whiplashmerch.com/api/v2/customers/{id}/call/{action}', params={

}, headers = headers)

print r.json()
```

```java
URL obj = new URL("://staging.whiplashmerch.com/api/v2/customers/{id}/call/{action}");
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

`PUT /api/v2/customers/{id}/call/{action}`

*Perform an action on a customer*

Perform an action on a customer

### Parameters

Parameter|In|Type|Required|Description
---|---|---|---|---|
async|formData|boolean|false|Process this action asynchronously
id|path|integer|true|No description
action|path|integer|true|No description


### Responses

Status|Meaning|Description
---|---|---|
200|[OK](https://tools.ietf.org/html/rfc7231#section-6.3.1)|Perform an action on a customer
401|[Unauthorized](https://tools.ietf.org/html/rfc7235#section-3.1)|No description
403|[Forbidden](https://tools.ietf.org/html/rfc7231#section-6.5.3)|No description
405|[Method Not Allowed](https://tools.ietf.org/html/rfc7231#section-6.5.5)|No description
422|[Unprocessable Entity](https://tools.ietf.org/html/rfc2518#section-10.3)|No description

> Example responses

```json
{
  "id": 0,
  "name": "string",
  "created_at": "2017-06-19T15:15:48Z",
  "active": true,
  "auto_merge_gestation": 0,
  "balance": 0,
  "default_warehouse_id": 0,
  "eori_number": "string",
  "estimated_monthly_volume": "string",
  "fedex_account": "string",
  "from_email": "string",
  "instructions": "string",
  "item_scanning_preference": true,
  "label_format": "string",
  "minimum_storage_qty": 0,
  "notes": "string",
  "notify_originator": true,
  "notify_originator_inventory": 0,
  "originator_permissions": true,
  "packing_slip_msg": "string",
  "packingslip_template": "string",
  "partner_id": 0,
  "request_serial_numbers": true,
  "ship_method_preference": 0,
  "shipping_name": "string",
  "ups_account": "string",
  "vat_number": "string",
  "warehouse_fallback": 0,
  "activated_at": "2017-06-19T15:15:48Z",
  "deactivated_at": "2017-06-19T15:15:48Z",
  "authentication_token": "string",
  "auto_merge_skus": true,
  "billing_email": "string",
  "billing_contact_name": "string",
  "billing_company": "string",
  "billing_phone1": "string",
  "billing_phone2": "string",
  "billing_address1": "string",
  "billing_address2": "string",
  "billing_address3": "string",
  "billing_city": "string",
  "billing_state": "string",
  "billing_zip": "string",
  "billing_country": "string",
  "billing_residential": true,
  "items_returnable": true,
  "return_time_limit": 0,
  "return_label_expires_in": 0,
  "return_price_restricted": true,
  "return_sku_match": "string",
  "rma_display_logo": true,
  "rma_footer_content": "string",
  "return_email": "string",
  "return_phone": "string",
  "return_address_1": "string",
  "return_address_2": "string",
  "return_city": "string",
  "return_state": "string",
  "return_zip": "string",
  "return_country": "string",
  "logo_content_type": "string",
  "logo_file_name": "string",
  "logo_file_size": 0,
  "logo_updated_at": "2017-06-19T15:15:48Z",
  "full_logo_url": "string",
  "email_confirmation_from": "string",
  "email_confirmation_name": "string",
  "email_confirmation_msg": "string",
  "email_confirmation_preference": 0,
  "email_confirmation_template": "string"
}
```
```json
{
  "message": "string"
}
```
```json
{
  "message": "string"
}
```
```json
{
  "message": "string"
}
```
```json
{
  "message": "string"
}
```
<aside class="success">
This operation does not require authentication
</aside>

# warehouses

Operations about warehouses

## getApiV2Warehouses

> Code samples

```shell
# You can also use wget
curl -X get ://staging.whiplashmerch.com/api/v2/warehouses \
  -H 'Accept: application/json'

```

```http
GET ://staging.whiplashmerch.com/api/v2/warehouses HTTP/1.1
Host: staging.whiplashmerch.com

Accept: application/json

```

```javascript
var headers = {
  'Accept':'application/json'

};

$.ajax({
  url: '://staging.whiplashmerch.com/api/v2/warehouses',
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
  'Accept':'application/json'

};

fetch('://staging.whiplashmerch.com/api/v2/warehouses',
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
  'Accept' => 'application/json'
}

result = RestClient.get '://staging.whiplashmerch.com/api/v2/warehouses', params: {
  }, headers: headers

p JSON.parse(result)
```

```python
import requests
headers = {
  'Accept': 'application/json'
}

r = requests.get('://staging.whiplashmerch.com/api/v2/warehouses', params={

}, headers = headers)

print r.json()
```

```java
URL obj = new URL("://staging.whiplashmerch.com/api/v2/warehouses");
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

`GET /api/v2/warehouses`

*Get a list of warehouses*

Get a list of warehouses

### Parameters

Parameter|In|Type|Required|Description
---|---|---|---|---|
search|query|string|false|JSON search string like {"attribute_eq": "Term"}
fields|query|string|false|Comma-separated list of fields to include in the response


### Responses

Status|Meaning|Description
---|---|---|
200|[OK](https://tools.ietf.org/html/rfc7231#section-6.3.1)|Get a list of warehouses
401|[Unauthorized](https://tools.ietf.org/html/rfc7235#section-3.1)|No description
403|[Forbidden](https://tools.ietf.org/html/rfc7231#section-6.5.3)|No description

> Example responses

```json
{
  "id": 0,
  "name": "string",
  "shipping_address_1": "string",
  "shipping_address_2": "string",
  "shipping_city": "string",
  "shipping_state": "string",
  "shipping_zip": "string",
  "shipping_country": "string",
  "shipping_country_iso2": "string",
  "active": true,
  "square_footage": 0,
  "created_at": "2017-06-19T15:15:48Z",
  "updated_at": "2017-06-19T15:15:48Z",
  "ups_shipper_number": "string",
  "email": "string",
  "ups_carrier_facility": "string",
  "currency": "string",
  "timezone": "string",
  "vat": 0,
  "latitude": 0,
  "longitude": 0,
  "partner_id": 0,
  "domestic_return_labels": true,
  "international_return_labels": true,
  "eori_number": "string",
  "custom_field1": "string",
  "custom_field1_title": "string",
  "custom_field2": "string",
  "custom_field2_title": "string",
  "custom_field3": "string",
  "custom_field3_title": "string",
  "accepting_new_customers": true,
  "receiving_hours": "string",
  "forklift_available": true,
  "contact_name": "string",
  "delivery_appointment_required": true,
  "label_format": "string",
  "slug": "string"
}
```
```json
{
  "message": "string"
}
```
```json
{
  "message": "string"
}
```
<aside class="success">
This operation does not require authentication
</aside>

## postApiV2Warehouses

> Code samples

```shell
# You can also use wget
curl -X post ://staging.whiplashmerch.com/api/v2/warehouses \
  -H 'Content-Type: application/json' \
  -H 'Accept: application/json'

```

```http
POST ://staging.whiplashmerch.com/api/v2/warehouses HTTP/1.1
Host: staging.whiplashmerch.com
Content-Type: application/json
Accept: application/json

```

```javascript
var headers = {
  'Content-Type':'application/json',
  'Accept':'application/json'

};

$.ajax({
  url: '://staging.whiplashmerch.com/api/v2/warehouses',
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
  'Content-Type':'application/json',
  'Accept':'application/json'

};

fetch('://staging.whiplashmerch.com/api/v2/warehouses',
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
  'Content-Type' => 'application/json',
  'Accept' => 'application/json'
}

result = RestClient.post '://staging.whiplashmerch.com/api/v2/warehouses', params: {
  }, headers: headers

p JSON.parse(result)
```

```python
import requests
headers = {
  'Content-Type': 'application/json',
  'Accept': 'application/json'
}

r = requests.post('://staging.whiplashmerch.com/api/v2/warehouses', params={

}, headers = headers)

print r.json()
```

```java
URL obj = new URL("://staging.whiplashmerch.com/api/v2/warehouses");
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

`POST /api/v2/warehouses`

*Create a warehouse*

Create a warehouse

### Parameters

Parameter|In|Type|Required|Description
---|---|---|---|---|
name|formData|string|false|No description
shipping_country_iso2|formData|string|false|Warehouse country code
email|formData|string|true|Warehouse email.
shipping_address_1|formData|string|false|Warehouse address line 1
shipping_address_2|formData|string|false|Warehouse address line 2
shipping_city|formData|string|false|Warehouse city
shipping_state|formData|string|false| Warehouse state or province
shipping_zip|formData|string|false|Warehouse postal code
shipping_country|formData|string|false|Warehouse country
active|formData|boolean|false|Is the Warehouse active? 
square_footage|formData|integer|false|Warehouse square footage 
ups_shipper_number|formData|string|false|Warehouse UPS shipping number
ups_carrier_facility|formData|string|false|Warehouse carrier facility
currency|formData|string|false|Warehouse currency
timezone|formData|string|false|Warehouse timezone
vat|formData|number|false|Warehouse vat
latitude|formData|number|false|Warehouse latitude
longitude|formData|number|false|Warehouse longitude
partner_id|formData|integer|false|Warehouse partner id 
domestic_return_labels|formData|boolean|false|Warehouse does domestic return labels? 
international_return_labels|formData|boolean|false|Warehouse does intl return labels?
eori_number|formData|string|false|Warehouse EORI number
custom_field1|formData|string|false|Custom field
custom_field1_title|formData|string|false|Custom field title
custom_field2|formData|string|false|Custom field title
custom_field2_title|formData|string|false|Custom field title
custom_field3|formData|string|false|Custom field
custom_field3_title|formData|string|false|Custom field title
accepting_new_customers|formData|boolean|false|Is this Warehouse accepting new customers?
receiving_hours|formData|string|false|Warehouse receiving hours
forklift_available|formData|boolean|false|Does this Warehouse have a forklift available?
contact_name|formData|string|false|Warehouse contact name
delivery_appointment_required|formData|boolean|false|Does this Warehouse have delivery appointment reminders? 
label_format|formData|string|false|Warehouse label format
slug|formData|string|false|Warehouse slug


### Responses

Status|Meaning|Description
---|---|---|
201|[Created](https://tools.ietf.org/html/rfc7231#section-6.3.2)|Create a warehouse
401|[Unauthorized](https://tools.ietf.org/html/rfc7235#section-3.1)|No description
403|[Forbidden](https://tools.ietf.org/html/rfc7231#section-6.5.3)|No description
409|[Conflict](https://tools.ietf.org/html/rfc7231#section-6.5.8)|No description
422|[Unprocessable Entity](https://tools.ietf.org/html/rfc2518#section-10.3)|No description

> Example responses

```json
{
  "id": 0,
  "name": "string",
  "shipping_address_1": "string",
  "shipping_address_2": "string",
  "shipping_city": "string",
  "shipping_state": "string",
  "shipping_zip": "string",
  "shipping_country": "string",
  "shipping_country_iso2": "string",
  "active": true,
  "square_footage": 0,
  "created_at": "2017-06-19T15:15:48Z",
  "updated_at": "2017-06-19T15:15:48Z",
  "ups_shipper_number": "string",
  "email": "string",
  "ups_carrier_facility": "string",
  "currency": "string",
  "timezone": "string",
  "vat": 0,
  "latitude": 0,
  "longitude": 0,
  "partner_id": 0,
  "domestic_return_labels": true,
  "international_return_labels": true,
  "eori_number": "string",
  "custom_field1": "string",
  "custom_field1_title": "string",
  "custom_field2": "string",
  "custom_field2_title": "string",
  "custom_field3": "string",
  "custom_field3_title": "string",
  "accepting_new_customers": true,
  "receiving_hours": "string",
  "forklift_available": true,
  "contact_name": "string",
  "delivery_appointment_required": true,
  "label_format": "string",
  "slug": "string"
}
```
```json
{
  "message": "string"
}
```
```json
{
  "message": "string"
}
```
```json
{
  "message": "string"
}
```
```json
{
  "message": "string"
}
```
<aside class="success">
This operation does not require authentication
</aside>

## getApiV2WarehousesCount

> Code samples

```shell
# You can also use wget
curl -X get ://staging.whiplashmerch.com/api/v2/warehouses/count \
  -H 'Accept: application/json'

```

```http
GET ://staging.whiplashmerch.com/api/v2/warehouses/count HTTP/1.1
Host: staging.whiplashmerch.com

Accept: application/json

```

```javascript
var headers = {
  'Accept':'application/json'

};

$.ajax({
  url: '://staging.whiplashmerch.com/api/v2/warehouses/count',
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
  'Accept':'application/json'

};

fetch('://staging.whiplashmerch.com/api/v2/warehouses/count',
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
  'Accept' => 'application/json'
}

result = RestClient.get '://staging.whiplashmerch.com/api/v2/warehouses/count', params: {
  }, headers: headers

p JSON.parse(result)
```

```python
import requests
headers = {
  'Accept': 'application/json'
}

r = requests.get('://staging.whiplashmerch.com/api/v2/warehouses/count', params={

}, headers = headers)

print r.json()
```

```java
URL obj = new URL("://staging.whiplashmerch.com/api/v2/warehouses/count");
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

`GET /api/v2/warehouses/count`

*Returns count of warehouses*

Returns count of warehouses

### Parameters

Parameter|In|Type|Required|Description
---|---|---|---|---|
search|query|string|false|JSON search string like {"attribute_eq": "Term"}


### Responses

Status|Meaning|Description
---|---|---|
200|[OK](https://tools.ietf.org/html/rfc7231#section-6.3.1)|Returns count of warehouses
401|[Unauthorized](https://tools.ietf.org/html/rfc7235#section-3.1)|No description
403|[Forbidden](https://tools.ietf.org/html/rfc7231#section-6.5.3)|No description

> Example responses

```json
{
  "id": 0,
  "name": "string",
  "shipping_address_1": "string",
  "shipping_address_2": "string",
  "shipping_city": "string",
  "shipping_state": "string",
  "shipping_zip": "string",
  "shipping_country": "string",
  "shipping_country_iso2": "string",
  "active": true,
  "square_footage": 0,
  "created_at": "2017-06-19T15:15:48Z",
  "updated_at": "2017-06-19T15:15:48Z",
  "ups_shipper_number": "string",
  "email": "string",
  "ups_carrier_facility": "string",
  "currency": "string",
  "timezone": "string",
  "vat": 0,
  "latitude": 0,
  "longitude": 0,
  "partner_id": 0,
  "domestic_return_labels": true,
  "international_return_labels": true,
  "eori_number": "string",
  "custom_field1": "string",
  "custom_field1_title": "string",
  "custom_field2": "string",
  "custom_field2_title": "string",
  "custom_field3": "string",
  "custom_field3_title": "string",
  "accepting_new_customers": true,
  "receiving_hours": "string",
  "forklift_available": true,
  "contact_name": "string",
  "delivery_appointment_required": true,
  "label_format": "string",
  "slug": "string"
}
```
```json
{
  "message": "string"
}
```
```json
{
  "message": "string"
}
```
<aside class="success">
This operation does not require authentication
</aside>

## getApiV2WarehousesId

> Code samples

```shell
# You can also use wget
curl -X get ://staging.whiplashmerch.com/api/v2/warehouses/{id} \
  -H 'Accept: application/json'

```

```http
GET ://staging.whiplashmerch.com/api/v2/warehouses/{id} HTTP/1.1
Host: staging.whiplashmerch.com

Accept: application/json

```

```javascript
var headers = {
  'Accept':'application/json'

};

$.ajax({
  url: '://staging.whiplashmerch.com/api/v2/warehouses/{id}',
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
  'Accept':'application/json'

};

fetch('://staging.whiplashmerch.com/api/v2/warehouses/{id}',
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
  'Accept' => 'application/json'
}

result = RestClient.get '://staging.whiplashmerch.com/api/v2/warehouses/{id}', params: {
  }, headers: headers

p JSON.parse(result)
```

```python
import requests
headers = {
  'Accept': 'application/json'
}

r = requests.get('://staging.whiplashmerch.com/api/v2/warehouses/{id}', params={

}, headers = headers)

print r.json()
```

```java
URL obj = new URL("://staging.whiplashmerch.com/api/v2/warehouses/{id}");
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

`GET /api/v2/warehouses/{id}`

*Get a warehouse*

Get a warehouse

### Parameters

Parameter|In|Type|Required|Description
---|---|---|---|---|
id|path|integer|true|No description


### Responses

Status|Meaning|Description
---|---|---|
200|[OK](https://tools.ietf.org/html/rfc7231#section-6.3.1)|Get a warehouse
401|[Unauthorized](https://tools.ietf.org/html/rfc7235#section-3.1)|No description
403|[Forbidden](https://tools.ietf.org/html/rfc7231#section-6.5.3)|No description

> Example responses

```json
{
  "id": 0,
  "name": "string",
  "shipping_address_1": "string",
  "shipping_address_2": "string",
  "shipping_city": "string",
  "shipping_state": "string",
  "shipping_zip": "string",
  "shipping_country": "string",
  "shipping_country_iso2": "string",
  "active": true,
  "square_footage": 0,
  "created_at": "2017-06-19T15:15:48Z",
  "updated_at": "2017-06-19T15:15:48Z",
  "ups_shipper_number": "string",
  "email": "string",
  "ups_carrier_facility": "string",
  "currency": "string",
  "timezone": "string",
  "vat": 0,
  "latitude": 0,
  "longitude": 0,
  "partner_id": 0,
  "domestic_return_labels": true,
  "international_return_labels": true,
  "eori_number": "string",
  "custom_field1": "string",
  "custom_field1_title": "string",
  "custom_field2": "string",
  "custom_field2_title": "string",
  "custom_field3": "string",
  "custom_field3_title": "string",
  "accepting_new_customers": true,
  "receiving_hours": "string",
  "forklift_available": true,
  "contact_name": "string",
  "delivery_appointment_required": true,
  "label_format": "string",
  "slug": "string"
}
```
```json
{
  "message": "string"
}
```
```json
{
  "message": "string"
}
```
<aside class="success">
This operation does not require authentication
</aside>

## putApiV2WarehousesId

> Code samples

```shell
# You can also use wget
curl -X put ://staging.whiplashmerch.com/api/v2/warehouses/{id} \
  -H 'Content-Type: application/json' \
  -H 'Accept: application/json'

```

```http
PUT ://staging.whiplashmerch.com/api/v2/warehouses/{id} HTTP/1.1
Host: staging.whiplashmerch.com
Content-Type: application/json
Accept: application/json

```

```javascript
var headers = {
  'Content-Type':'application/json',
  'Accept':'application/json'

};

$.ajax({
  url: '://staging.whiplashmerch.com/api/v2/warehouses/{id}',
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
  'Content-Type':'application/json',
  'Accept':'application/json'

};

fetch('://staging.whiplashmerch.com/api/v2/warehouses/{id}',
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
  'Content-Type' => 'application/json',
  'Accept' => 'application/json'
}

result = RestClient.put '://staging.whiplashmerch.com/api/v2/warehouses/{id}', params: {
  }, headers: headers

p JSON.parse(result)
```

```python
import requests
headers = {
  'Content-Type': 'application/json',
  'Accept': 'application/json'
}

r = requests.put('://staging.whiplashmerch.com/api/v2/warehouses/{id}', params={

}, headers = headers)

print r.json()
```

```java
URL obj = new URL("://staging.whiplashmerch.com/api/v2/warehouses/{id}");
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

`PUT /api/v2/warehouses/{id}`

*Update a warehouse*

Update a warehouse

### Parameters

Parameter|In|Type|Required|Description
---|---|---|---|---|
name|formData|string|false|No description
shipping_address_1|formData|string|false|Warehouse address line 1
shipping_address_2|formData|string|false|Warehouse address line 2
shipping_city|formData|string|false|Warehouse city
shipping_state|formData|string|false| Warehouse state or province
shipping_zip|formData|string|false|Warehouse postal code
shipping_country|formData|string|false|Warehouse country
shipping_country_iso2|formData|string|false|Warehouse country code
active|formData|boolean|false|Is the Warehouse active? 
square_footage|formData|integer|false|Warehouse square footage 
ups_shipper_number|formData|string|false|Warehouse UPS shipping number
email|formData|string|false|No description
ups_carrier_facility|formData|string|false|Warehouse carrier facility
currency|formData|string|false|Warehouse currency
timezone|formData|string|false|Warehouse timezone
vat|formData|number|false|Warehouse vat
latitude|formData|number|false|Warehouse latitude
longitude|formData|number|false|Warehouse longitude
partner_id|formData|integer|false|Warehouse partner id 
domestic_return_labels|formData|boolean|false|Warehouse does domestic return labels? 
international_return_labels|formData|boolean|false|Warehouse does intl return labels?
eori_number|formData|string|false|Warehouse EORI number
custom_field1|formData|string|false|Custom field
custom_field1_title|formData|string|false|Custom field title
custom_field2|formData|string|false|Custom field title
custom_field2_title|formData|string|false|Custom field title
custom_field3|formData|string|false|Custom field
custom_field3_title|formData|string|false|Custom field title
accepting_new_customers|formData|boolean|false|Is this Warehouse accepting new customers?
receiving_hours|formData|string|false|Warehouse receiving hours
forklift_available|formData|boolean|false|Does this Warehouse have a forklift available?
contact_name|formData|string|false|Warehouse contact name
delivery_appointment_required|formData|boolean|false|Does this Warehouse have delivery appointment reminders? 
label_format|formData|string|false|Warehouse label format
slug|formData|string|false|Warehouse slug
id|path|integer|true|No description


### Responses

Status|Meaning|Description
---|---|---|
200|[OK](https://tools.ietf.org/html/rfc7231#section-6.3.1)|Update a warehouse
401|[Unauthorized](https://tools.ietf.org/html/rfc7235#section-3.1)|No description
403|[Forbidden](https://tools.ietf.org/html/rfc7231#section-6.5.3)|No description
422|[Unprocessable Entity](https://tools.ietf.org/html/rfc2518#section-10.3)|No description

> Example responses

```json
{
  "id": 0,
  "name": "string",
  "shipping_address_1": "string",
  "shipping_address_2": "string",
  "shipping_city": "string",
  "shipping_state": "string",
  "shipping_zip": "string",
  "shipping_country": "string",
  "shipping_country_iso2": "string",
  "active": true,
  "square_footage": 0,
  "created_at": "2017-06-19T15:15:48Z",
  "updated_at": "2017-06-19T15:15:48Z",
  "ups_shipper_number": "string",
  "email": "string",
  "ups_carrier_facility": "string",
  "currency": "string",
  "timezone": "string",
  "vat": 0,
  "latitude": 0,
  "longitude": 0,
  "partner_id": 0,
  "domestic_return_labels": true,
  "international_return_labels": true,
  "eori_number": "string",
  "custom_field1": "string",
  "custom_field1_title": "string",
  "custom_field2": "string",
  "custom_field2_title": "string",
  "custom_field3": "string",
  "custom_field3_title": "string",
  "accepting_new_customers": true,
  "receiving_hours": "string",
  "forklift_available": true,
  "contact_name": "string",
  "delivery_appointment_required": true,
  "label_format": "string",
  "slug": "string"
}
```
```json
{
  "message": "string"
}
```
```json
{
  "message": "string"
}
```
```json
{
  "message": "string"
}
```
<aside class="success">
This operation does not require authentication
</aside>

## deleteApiV2WarehousesId

> Code samples

```shell
# You can also use wget
curl -X delete ://staging.whiplashmerch.com/api/v2/warehouses/{id} \
  -H 'Accept: application/json'

```

```http
DELETE ://staging.whiplashmerch.com/api/v2/warehouses/{id} HTTP/1.1
Host: staging.whiplashmerch.com

Accept: application/json

```

```javascript
var headers = {
  'Accept':'application/json'

};

$.ajax({
  url: '://staging.whiplashmerch.com/api/v2/warehouses/{id}',
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
  'Accept':'application/json'

};

fetch('://staging.whiplashmerch.com/api/v2/warehouses/{id}',
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
  'Accept' => 'application/json'
}

result = RestClient.delete '://staging.whiplashmerch.com/api/v2/warehouses/{id}', params: {
  }, headers: headers

p JSON.parse(result)
```

```python
import requests
headers = {
  'Accept': 'application/json'
}

r = requests.delete('://staging.whiplashmerch.com/api/v2/warehouses/{id}', params={

}, headers = headers)

print r.json()
```

```java
URL obj = new URL("://staging.whiplashmerch.com/api/v2/warehouses/{id}");
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

`DELETE /api/v2/warehouses/{id}`

*Delete a warehouse*

Delete a warehouse

### Parameters

Parameter|In|Type|Required|Description
---|---|---|---|---|
id|path|integer|true|No description


### Responses

Status|Meaning|Description
---|---|---|
200|[OK](https://tools.ietf.org/html/rfc7231#section-6.3.1)|Delete a warehouse
401|[Unauthorized](https://tools.ietf.org/html/rfc7235#section-3.1)|No description
403|[Forbidden](https://tools.ietf.org/html/rfc7231#section-6.5.3)|No description
422|[Unprocessable Entity](https://tools.ietf.org/html/rfc2518#section-10.3)|No description

> Example responses

```json
{
  "id": 0,
  "name": "string",
  "shipping_address_1": "string",
  "shipping_address_2": "string",
  "shipping_city": "string",
  "shipping_state": "string",
  "shipping_zip": "string",
  "shipping_country": "string",
  "shipping_country_iso2": "string",
  "active": true,
  "square_footage": 0,
  "created_at": "2017-06-19T15:15:48Z",
  "updated_at": "2017-06-19T15:15:48Z",
  "ups_shipper_number": "string",
  "email": "string",
  "ups_carrier_facility": "string",
  "currency": "string",
  "timezone": "string",
  "vat": 0,
  "latitude": 0,
  "longitude": 0,
  "partner_id": 0,
  "domestic_return_labels": true,
  "international_return_labels": true,
  "eori_number": "string",
  "custom_field1": "string",
  "custom_field1_title": "string",
  "custom_field2": "string",
  "custom_field2_title": "string",
  "custom_field3": "string",
  "custom_field3_title": "string",
  "accepting_new_customers": true,
  "receiving_hours": "string",
  "forklift_available": true,
  "contact_name": "string",
  "delivery_appointment_required": true,
  "label_format": "string",
  "slug": "string"
}
```
```json
{
  "message": "string"
}
```
```json
{
  "message": "string"
}
```
```json
{
  "message": "string"
}
```
<aside class="success">
This operation does not require authentication
</aside>

# me

Operations about mes

## getApiV2Me

> Code samples

```shell
# You can also use wget
curl -X get ://staging.whiplashmerch.com/api/v2/me \
  -H 'Accept: application/json'

```

```http
GET ://staging.whiplashmerch.com/api/v2/me HTTP/1.1
Host: staging.whiplashmerch.com

Accept: application/json

```

```javascript
var headers = {
  'Accept':'application/json'

};

$.ajax({
  url: '://staging.whiplashmerch.com/api/v2/me',
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
  'Accept':'application/json'

};

fetch('://staging.whiplashmerch.com/api/v2/me',
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
  'Accept' => 'application/json'
}

result = RestClient.get '://staging.whiplashmerch.com/api/v2/me', params: {
  }, headers: headers

p JSON.parse(result)
```

```python
import requests
headers = {
  'Accept': 'application/json'
}

r = requests.get('://staging.whiplashmerch.com/api/v2/me', params={

}, headers = headers)

print r.json()
```

```java
URL obj = new URL("://staging.whiplashmerch.com/api/v2/me");
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

`GET /api/v2/me`

*Gets the current_user*

Gets the current_user

### Responses

Status|Meaning|Description
---|---|---|
200|[OK](https://tools.ietf.org/html/rfc7231#section-6.3.1)|Gets the current_user
401|[Unauthorized](https://tools.ietf.org/html/rfc7235#section-3.1)|No description
403|[Forbidden](https://tools.ietf.org/html/rfc7231#section-6.5.3)|No description

> Example responses

```json
{
  "id": 0,
  "email": "string",
  "sign_in_count": 0,
  "created_at": "2017-06-19T15:15:48Z",
  "first_name": "string",
  "last_name": "string",
  "role": "string",
  "warehouse_id": 0,
  "active": true,
  "customer_ids": 0
}
```
```json
{
  "message": "string"
}
```
```json
{
  "message": "string"
}
```
<aside class="success">
This operation does not require authentication
</aside>

# users

Operations about users

## getApiV2Users

> Code samples

```shell
# You can also use wget
curl -X get ://staging.whiplashmerch.com/api/v2/users \
  -H 'X-Customer-Id: string' \
  -H 'Accept: application/json'

```

```http
GET ://staging.whiplashmerch.com/api/v2/users HTTP/1.1
Host: staging.whiplashmerch.com

Accept: application/json
X-Customer-Id: string

```

```javascript
var headers = {
  'X-Customer-Id':'string',
  'Accept':'application/json'

};

$.ajax({
  url: '://staging.whiplashmerch.com/api/v2/users',
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
  'X-Customer-Id':'string',
  'Accept':'application/json'

};

fetch('://staging.whiplashmerch.com/api/v2/users',
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
  'X-Customer-Id' => 'string',
  'Accept' => 'application/json'
}

result = RestClient.get '://staging.whiplashmerch.com/api/v2/users', params: {
  }, headers: headers

p JSON.parse(result)
```

```python
import requests
headers = {
  'X-Customer-Id': 'string',
  'Accept': 'application/json'
}

r = requests.get('://staging.whiplashmerch.com/api/v2/users', params={

}, headers = headers)

print r.json()
```

```java
URL obj = new URL("://staging.whiplashmerch.com/api/v2/users");
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

`GET /api/v2/users`

*Get all users*

Get all users

### Parameters

Parameter|In|Type|Required|Description
---|---|---|---|---|
X-Customer-Id|header|string|false|The customer associated with this resource.
search|query|string|false|JSON search string like {"attribute_eq": "Term"}
fields|query|string|false|Comma-separated list of fields to include in the response
page|query|integer|false|Page of results to fetch.
per_page|query|integer|false|Number of results to return per page.


### Responses

Status|Meaning|Description
---|---|---|
200|[OK](https://tools.ietf.org/html/rfc7231#section-6.3.1)|Get all users
401|[Unauthorized](https://tools.ietf.org/html/rfc7235#section-3.1)|No description
403|[Forbidden](https://tools.ietf.org/html/rfc7231#section-6.5.3)|No description

> Example responses

```json
{
  "id": 0,
  "email": "string",
  "sign_in_count": 0,
  "created_at": "2017-06-19T15:15:48Z",
  "first_name": "string",
  "last_name": "string",
  "role": "string",
  "warehouse_id": 0,
  "active": true,
  "customer_ids": 0
}
```
```json
{
  "message": "string"
}
```
```json
{
  "message": "string"
}
```
<aside class="success">
This operation does not require authentication
</aside>

## postApiV2Users

> Code samples

```shell
# You can also use wget
curl -X post ://staging.whiplashmerch.com/api/v2/users \
  -H 'X-Customer-Id: string' \
  -H 'Content-Type: application/json' \
  -H 'Accept: application/json'

```

```http
POST ://staging.whiplashmerch.com/api/v2/users HTTP/1.1
Host: staging.whiplashmerch.com
Content-Type: application/json
Accept: application/json
X-Customer-Id: string

```

```javascript
var headers = {
  'X-Customer-Id':'string',
  'Content-Type':'application/json',
  'Accept':'application/json'

};

$.ajax({
  url: '://staging.whiplashmerch.com/api/v2/users',
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
  'X-Customer-Id':'string',
  'Content-Type':'application/json',
  'Accept':'application/json'

};

fetch('://staging.whiplashmerch.com/api/v2/users',
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
  'X-Customer-Id' => 'string',
  'Content-Type' => 'application/json',
  'Accept' => 'application/json'
}

result = RestClient.post '://staging.whiplashmerch.com/api/v2/users', params: {
  }, headers: headers

p JSON.parse(result)
```

```python
import requests
headers = {
  'X-Customer-Id': 'string',
  'Content-Type': 'application/json',
  'Accept': 'application/json'
}

r = requests.post('://staging.whiplashmerch.com/api/v2/users', params={

}, headers = headers)

print r.json()
```

```java
URL obj = new URL("://staging.whiplashmerch.com/api/v2/users");
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

`POST /api/v2/users`

*Create a user*

Create a user

### Parameters

Parameter|In|Type|Required|Description
---|---|---|---|---|
X-Customer-Id|header|string|false|The customer associated with this resource.
email|formData|string|true|Email address
sign_in_count|formData|integer|false|No description
first_name|formData|string|false|first name of the user
last_name|formData|string|false|last name of the user
role|formData|string|false|role of the user
warehouse_id|formData|integer|false|warehouse_id of the user
active|formData|boolean|false|is the user active?
customer_ids|formData|array[integer]|false|is the user active?


### Responses

Status|Meaning|Description
---|---|---|
201|[Created](https://tools.ietf.org/html/rfc7231#section-6.3.2)|Create a user
401|[Unauthorized](https://tools.ietf.org/html/rfc7235#section-3.1)|No description
403|[Forbidden](https://tools.ietf.org/html/rfc7231#section-6.5.3)|No description
409|[Conflict](https://tools.ietf.org/html/rfc7231#section-6.5.8)|No description
422|[Unprocessable Entity](https://tools.ietf.org/html/rfc2518#section-10.3)|No description

> Example responses

```json
{
  "id": 0,
  "email": "string",
  "sign_in_count": 0,
  "created_at": "2017-06-19T15:15:48Z",
  "first_name": "string",
  "last_name": "string",
  "role": "string",
  "warehouse_id": 0,
  "active": true,
  "customer_ids": 0
}
```
```json
{
  "message": "string"
}
```
```json
{
  "message": "string"
}
```
```json
{
  "message": "string"
}
```
```json
{
  "message": "string"
}
```
<aside class="success">
This operation does not require authentication
</aside>

## getApiV2UsersCount

> Code samples

```shell
# You can also use wget
curl -X get ://staging.whiplashmerch.com/api/v2/users/count \
  -H 'X-Customer-Id: string' \
  -H 'Accept: application/json'

```

```http
GET ://staging.whiplashmerch.com/api/v2/users/count HTTP/1.1
Host: staging.whiplashmerch.com

Accept: application/json
X-Customer-Id: string

```

```javascript
var headers = {
  'X-Customer-Id':'string',
  'Accept':'application/json'

};

$.ajax({
  url: '://staging.whiplashmerch.com/api/v2/users/count',
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
  'X-Customer-Id':'string',
  'Accept':'application/json'

};

fetch('://staging.whiplashmerch.com/api/v2/users/count',
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
  'X-Customer-Id' => 'string',
  'Accept' => 'application/json'
}

result = RestClient.get '://staging.whiplashmerch.com/api/v2/users/count', params: {
  }, headers: headers

p JSON.parse(result)
```

```python
import requests
headers = {
  'X-Customer-Id': 'string',
  'Accept': 'application/json'
}

r = requests.get('://staging.whiplashmerch.com/api/v2/users/count', params={

}, headers = headers)

print r.json()
```

```java
URL obj = new URL("://staging.whiplashmerch.com/api/v2/users/count");
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

`GET /api/v2/users/count`

*Returns count of users*

Returns count of users

### Parameters

Parameter|In|Type|Required|Description
---|---|---|---|---|
X-Customer-Id|header|string|false|The customer associated with this resource.
search|query|string|false|JSON search string like {"attribute_eq": "Term"}


### Responses

Status|Meaning|Description
---|---|---|
200|[OK](https://tools.ietf.org/html/rfc7231#section-6.3.1)|Returns count of users
401|[Unauthorized](https://tools.ietf.org/html/rfc7235#section-3.1)|No description
403|[Forbidden](https://tools.ietf.org/html/rfc7231#section-6.5.3)|No description

> Example responses

```json
{
  "id": 0,
  "email": "string",
  "sign_in_count": 0,
  "created_at": "2017-06-19T15:15:48Z",
  "first_name": "string",
  "last_name": "string",
  "role": "string",
  "warehouse_id": 0,
  "active": true,
  "customer_ids": 0
}
```
```json
{
  "message": "string"
}
```
```json
{
  "message": "string"
}
```
<aside class="success">
This operation does not require authentication
</aside>

## getApiV2UsersId

> Code samples

```shell
# You can also use wget
curl -X get ://staging.whiplashmerch.com/api/v2/users/{id} \
  -H 'X-Customer-Id: string' \
  -H 'Accept: application/json'

```

```http
GET ://staging.whiplashmerch.com/api/v2/users/{id} HTTP/1.1
Host: staging.whiplashmerch.com

Accept: application/json
X-Customer-Id: string

```

```javascript
var headers = {
  'X-Customer-Id':'string',
  'Accept':'application/json'

};

$.ajax({
  url: '://staging.whiplashmerch.com/api/v2/users/{id}',
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
  'X-Customer-Id':'string',
  'Accept':'application/json'

};

fetch('://staging.whiplashmerch.com/api/v2/users/{id}',
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
  'X-Customer-Id' => 'string',
  'Accept' => 'application/json'
}

result = RestClient.get '://staging.whiplashmerch.com/api/v2/users/{id}', params: {
  }, headers: headers

p JSON.parse(result)
```

```python
import requests
headers = {
  'X-Customer-Id': 'string',
  'Accept': 'application/json'
}

r = requests.get('://staging.whiplashmerch.com/api/v2/users/{id}', params={

}, headers = headers)

print r.json()
```

```java
URL obj = new URL("://staging.whiplashmerch.com/api/v2/users/{id}");
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

`GET /api/v2/users/{id}`

*Get a user*

Get a user

### Parameters

Parameter|In|Type|Required|Description
---|---|---|---|---|
id|path|integer|true|No description
X-Customer-Id|header|string|false|The customer associated with this resource.


### Responses

Status|Meaning|Description
---|---|---|
200|[OK](https://tools.ietf.org/html/rfc7231#section-6.3.1)|Get a user
401|[Unauthorized](https://tools.ietf.org/html/rfc7235#section-3.1)|No description
403|[Forbidden](https://tools.ietf.org/html/rfc7231#section-6.5.3)|No description

> Example responses

```json
{
  "id": 0,
  "email": "string",
  "sign_in_count": 0,
  "created_at": "2017-06-19T15:15:48Z",
  "first_name": "string",
  "last_name": "string",
  "role": "string",
  "warehouse_id": 0,
  "active": true,
  "customer_ids": 0
}
```
```json
{
  "message": "string"
}
```
```json
{
  "message": "string"
}
```
<aside class="success">
This operation does not require authentication
</aside>

## putApiV2UsersId

> Code samples

```shell
# You can also use wget
curl -X put ://staging.whiplashmerch.com/api/v2/users/{id} \
  -H 'X-Customer-Id: string' \
  -H 'Content-Type: application/json' \
  -H 'Accept: application/json'

```

```http
PUT ://staging.whiplashmerch.com/api/v2/users/{id} HTTP/1.1
Host: staging.whiplashmerch.com
Content-Type: application/json
Accept: application/json
X-Customer-Id: string

```

```javascript
var headers = {
  'X-Customer-Id':'string',
  'Content-Type':'application/json',
  'Accept':'application/json'

};

$.ajax({
  url: '://staging.whiplashmerch.com/api/v2/users/{id}',
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
  'X-Customer-Id':'string',
  'Content-Type':'application/json',
  'Accept':'application/json'

};

fetch('://staging.whiplashmerch.com/api/v2/users/{id}',
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
  'X-Customer-Id' => 'string',
  'Content-Type' => 'application/json',
  'Accept' => 'application/json'
}

result = RestClient.put '://staging.whiplashmerch.com/api/v2/users/{id}', params: {
  }, headers: headers

p JSON.parse(result)
```

```python
import requests
headers = {
  'X-Customer-Id': 'string',
  'Content-Type': 'application/json',
  'Accept': 'application/json'
}

r = requests.put('://staging.whiplashmerch.com/api/v2/users/{id}', params={

}, headers = headers)

print r.json()
```

```java
URL obj = new URL("://staging.whiplashmerch.com/api/v2/users/{id}");
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

`PUT /api/v2/users/{id}`

*Update a user*

Update a user

### Parameters

Parameter|In|Type|Required|Description
---|---|---|---|---|
X-Customer-Id|header|string|false|The customer associated with this resource.
email|formData|string|false|No description
sign_in_count|formData|integer|false|No description
first_name|formData|string|false|first name of the user
last_name|formData|string|false|last name of the user
role|formData|string|false|role of the user
warehouse_id|formData|integer|false|warehouse_id of the user
active|formData|boolean|false|is the user active?
customer_ids|formData|array[integer]|false|is the user active?
id|path|integer|true|No description


### Responses

Status|Meaning|Description
---|---|---|
200|[OK](https://tools.ietf.org/html/rfc7231#section-6.3.1)|Update a user
401|[Unauthorized](https://tools.ietf.org/html/rfc7235#section-3.1)|No description
403|[Forbidden](https://tools.ietf.org/html/rfc7231#section-6.5.3)|No description
422|[Unprocessable Entity](https://tools.ietf.org/html/rfc2518#section-10.3)|No description

> Example responses

```json
{
  "id": 0,
  "email": "string",
  "sign_in_count": 0,
  "created_at": "2017-06-19T15:15:48Z",
  "first_name": "string",
  "last_name": "string",
  "role": "string",
  "warehouse_id": 0,
  "active": true,
  "customer_ids": 0
}
```
```json
{
  "message": "string"
}
```
```json
{
  "message": "string"
}
```
```json
{
  "message": "string"
}
```
<aside class="success">
This operation does not require authentication
</aside>

## deleteApiV2UsersId

> Code samples

```shell
# You can also use wget
curl -X delete ://staging.whiplashmerch.com/api/v2/users/{id} \
  -H 'X-Customer-Id: string' \
  -H 'Accept: application/json'

```

```http
DELETE ://staging.whiplashmerch.com/api/v2/users/{id} HTTP/1.1
Host: staging.whiplashmerch.com

Accept: application/json
X-Customer-Id: string

```

```javascript
var headers = {
  'X-Customer-Id':'string',
  'Accept':'application/json'

};

$.ajax({
  url: '://staging.whiplashmerch.com/api/v2/users/{id}',
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
  'X-Customer-Id':'string',
  'Accept':'application/json'

};

fetch('://staging.whiplashmerch.com/api/v2/users/{id}',
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
  'X-Customer-Id' => 'string',
  'Accept' => 'application/json'
}

result = RestClient.delete '://staging.whiplashmerch.com/api/v2/users/{id}', params: {
  }, headers: headers

p JSON.parse(result)
```

```python
import requests
headers = {
  'X-Customer-Id': 'string',
  'Accept': 'application/json'
}

r = requests.delete('://staging.whiplashmerch.com/api/v2/users/{id}', params={

}, headers = headers)

print r.json()
```

```java
URL obj = new URL("://staging.whiplashmerch.com/api/v2/users/{id}");
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

`DELETE /api/v2/users/{id}`

*Destroy a user*

Destroy a user

### Parameters

Parameter|In|Type|Required|Description
---|---|---|---|---|
id|path|integer|true|No description
X-Customer-Id|header|string|false|The customer associated with this resource.


### Responses

Status|Meaning|Description
---|---|---|
200|[OK](https://tools.ietf.org/html/rfc7231#section-6.3.1)|Destroy a user
401|[Unauthorized](https://tools.ietf.org/html/rfc7235#section-3.1)|No description
403|[Forbidden](https://tools.ietf.org/html/rfc7231#section-6.5.3)|No description
422|[Unprocessable Entity](https://tools.ietf.org/html/rfc2518#section-10.3)|No description

> Example responses

```json
{
  "id": 0,
  "email": "string",
  "sign_in_count": 0,
  "created_at": "2017-06-19T15:15:48Z",
  "first_name": "string",
  "last_name": "string",
  "role": "string",
  "warehouse_id": 0,
  "active": true,
  "customer_ids": 0
}
```
```json
{
  "message": "string"
}
```
```json
{
  "message": "string"
}
```
```json
{
  "message": "string"
}
```
<aside class="success">
This operation does not require authentication
</aside>

## getApiV2UsersIdConfirm

> Code samples

```shell
# You can also use wget
curl -X get ://staging.whiplashmerch.com/api/v2/users/{id}/confirm?confirmation_token=string \
  -H 'X-Customer-Id: string' \
  -H 'Accept: application/json'

```

```http
GET ://staging.whiplashmerch.com/api/v2/users/{id}/confirm?confirmation_token=string HTTP/1.1
Host: staging.whiplashmerch.com

Accept: application/json
X-Customer-Id: string

```

```javascript
var headers = {
  'X-Customer-Id':'string',
  'Accept':'application/json'

};

$.ajax({
  url: '://staging.whiplashmerch.com/api/v2/users/{id}/confirm',
  method: 'get',
  data: '?confirmation_token=string',
  headers: headers,
  success: function(data) {
    console.log(JSON.stringify(data));
  }
})
```

```javascript--nodejs
const request = require('node-fetch');

const headers = {
  'X-Customer-Id':'string',
  'Accept':'application/json'

};

fetch('://staging.whiplashmerch.com/api/v2/users/{id}/confirm?confirmation_token=string',
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
  'X-Customer-Id' => 'string',
  'Accept' => 'application/json'
}

result = RestClient.get '://staging.whiplashmerch.com/api/v2/users/{id}/confirm', params: {
  'confirmation_token' => 'string'
}, headers: headers

p JSON.parse(result)
```

```python
import requests
headers = {
  'X-Customer-Id': 'string',
  'Accept': 'application/json'
}

r = requests.get('://staging.whiplashmerch.com/api/v2/users/{id}/confirm', params={
  'confirmation_token': 'string'
}, headers = headers)

print r.json()
```

```java
URL obj = new URL("://staging.whiplashmerch.com/api/v2/users/{id}/confirm?confirmation_token=string");
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

`GET /api/v2/users/{id}/confirm`

*confirms a user given a User.id and a confirmation token*

confirms a user given a User.id and a confirmation token

### Parameters

Parameter|In|Type|Required|Description
---|---|---|---|---|
X-Customer-Id|header|string|false|The customer associated with this resource.
confirmation_token|query|string|true|Confirmation token of the user
id|path|integer|true|No description


### Responses

Status|Meaning|Description
---|---|---|
200|[OK](https://tools.ietf.org/html/rfc7231#section-6.3.1)|confirms a user given a User.id and a confirmation token
401|[Unauthorized](https://tools.ietf.org/html/rfc7235#section-3.1)|No description
403|[Forbidden](https://tools.ietf.org/html/rfc7231#section-6.5.3)|No description
422|[Unprocessable Entity](https://tools.ietf.org/html/rfc2518#section-10.3)|No description

> Example responses

```json
{
  "id": 0,
  "email": "string",
  "sign_in_count": 0,
  "created_at": "2017-06-19T15:15:48Z",
  "first_name": "string",
  "last_name": "string",
  "role": "string",
  "warehouse_id": 0,
  "active": true,
  "customer_ids": 0
}
```
```json
{
  "message": "string"
}
```
```json
{
  "message": "string"
}
```
```json
{
  "message": "string"
}
```
<aside class="success">
This operation does not require authentication
</aside>

## putApiV2UsersIdCallAction

> Code samples

```shell
# You can also use wget
curl -X put ://staging.whiplashmerch.com/api/v2/users/{id}/call/{action} \
  -H 'Content-Type: application/json' \
  -H 'Accept: application/json'

```

```http
PUT ://staging.whiplashmerch.com/api/v2/users/{id}/call/{action} HTTP/1.1
Host: staging.whiplashmerch.com
Content-Type: application/json
Accept: application/json

```

```javascript
var headers = {
  'Content-Type':'application/json',
  'Accept':'application/json'

};

$.ajax({
  url: '://staging.whiplashmerch.com/api/v2/users/{id}/call/{action}',
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
  'Content-Type':'application/json',
  'Accept':'application/json'

};

fetch('://staging.whiplashmerch.com/api/v2/users/{id}/call/{action}',
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
  'Content-Type' => 'application/json',
  'Accept' => 'application/json'
}

result = RestClient.put '://staging.whiplashmerch.com/api/v2/users/{id}/call/{action}', params: {
  }, headers: headers

p JSON.parse(result)
```

```python
import requests
headers = {
  'Content-Type': 'application/json',
  'Accept': 'application/json'
}

r = requests.put('://staging.whiplashmerch.com/api/v2/users/{id}/call/{action}', params={

}, headers = headers)

print r.json()
```

```java
URL obj = new URL("://staging.whiplashmerch.com/api/v2/users/{id}/call/{action}");
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

`PUT /api/v2/users/{id}/call/{action}`

*Perform an action on a user*

Perform an action on a user

### Parameters

Parameter|In|Type|Required|Description
---|---|---|---|---|
async|formData|boolean|false|Process this action asynchronously
id|path|integer|true|No description
action|path|integer|true|No description


### Responses

Status|Meaning|Description
---|---|---|
200|[OK](https://tools.ietf.org/html/rfc7231#section-6.3.1)|Perform an action on a user
401|[Unauthorized](https://tools.ietf.org/html/rfc7235#section-3.1)|No description
403|[Forbidden](https://tools.ietf.org/html/rfc7231#section-6.5.3)|No description
405|[Method Not Allowed](https://tools.ietf.org/html/rfc7231#section-6.5.5)|No description
422|[Unprocessable Entity](https://tools.ietf.org/html/rfc2518#section-10.3)|No description

> Example responses

```json
{
  "id": 0,
  "email": "string",
  "sign_in_count": 0,
  "created_at": "2017-06-19T15:15:48Z",
  "first_name": "string",
  "last_name": "string",
  "role": "string",
  "warehouse_id": 0,
  "active": true,
  "customer_ids": 0
}
```
```json
{
  "message": "string"
}
```
```json
{
  "message": "string"
}
```
```json
{
  "message": "string"
}
```
```json
{
  "message": "string"
}
```
<aside class="success">
This operation does not require authentication
</aside>

# web_hooks

Operations about web_hooks

## getApiV2WebHooks

> Code samples

```shell
# You can also use wget
curl -X get ://staging.whiplashmerch.com/api/v2/web_hooks \
  -H 'X-Customer-Id: string' \
  -H 'X-Shop-Id: string' \
  -H 'Accept: application/json'

```

```http
GET ://staging.whiplashmerch.com/api/v2/web_hooks HTTP/1.1
Host: staging.whiplashmerch.com

Accept: application/json
X-Customer-Id: string
X-Shop-Id: string

```

```javascript
var headers = {
  'X-Customer-Id':'string',
  'X-Shop-Id':'string',
  'Accept':'application/json'

};

$.ajax({
  url: '://staging.whiplashmerch.com/api/v2/web_hooks',
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
  'X-Customer-Id':'string',
  'X-Shop-Id':'string',
  'Accept':'application/json'

};

fetch('://staging.whiplashmerch.com/api/v2/web_hooks',
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
  'X-Customer-Id' => 'string',
  'X-Shop-Id' => 'string',
  'Accept' => 'application/json'
}

result = RestClient.get '://staging.whiplashmerch.com/api/v2/web_hooks', params: {
  }, headers: headers

p JSON.parse(result)
```

```python
import requests
headers = {
  'X-Customer-Id': 'string',
  'X-Shop-Id': 'string',
  'Accept': 'application/json'
}

r = requests.get('://staging.whiplashmerch.com/api/v2/web_hooks', params={

}, headers = headers)

print r.json()
```

```java
URL obj = new URL("://staging.whiplashmerch.com/api/v2/web_hooks");
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

`GET /api/v2/web_hooks`

*Get a list of web hooks*

Get a list of web hooks

### Parameters

Parameter|In|Type|Required|Description
---|---|---|---|---|
X-Customer-Id|header|string|false|The customer associated with this resource.
X-Shop-Id|header|string|false|The shop associated with this resource.
search|query|string|false|JSON search string like {"attribute_eq": "Term"}
fields|query|string|false|Comma-separated list of fields to include in the response
page|query|integer|false|Page of results to fetch.
per_page|query|integer|false|Number of results to return per page.


### Responses

Status|Meaning|Description
---|---|---|
200|[OK](https://tools.ietf.org/html/rfc7231#section-6.3.1)|Get a list of web hooks
401|[Unauthorized](https://tools.ietf.org/html/rfc7235#section-3.1)|No description
403|[Forbidden](https://tools.ietf.org/html/rfc7231#section-6.5.3)|No description

> Example responses

```json
{
  "id": 0,
  "hookable_id": 0,
  "hookable_type": "string",
  "url": "string",
  "format": "string",
  "created_at": "2017-06-19T15:15:48Z",
  "updated_at": "2017-06-19T15:15:48Z",
  "web_hook_event_id": 0,
  "failed_attempts": 0,
  "active": true
}
```
```json
{
  "message": "string"
}
```
```json
{
  "message": "string"
}
```
<aside class="success">
This operation does not require authentication
</aside>

## postApiV2WebHooks

> Code samples

```shell
# You can also use wget
curl -X post ://staging.whiplashmerch.com/api/v2/web_hooks \
  -H 'X-Customer-Id: string' \
  -H 'X-Shop-Id: string' \
  -H 'Content-Type: application/json' \
  -H 'Accept: application/json'

```

```http
POST ://staging.whiplashmerch.com/api/v2/web_hooks HTTP/1.1
Host: staging.whiplashmerch.com
Content-Type: application/json
Accept: application/json
X-Customer-Id: string
X-Shop-Id: string

```

```javascript
var headers = {
  'X-Customer-Id':'string',
  'X-Shop-Id':'string',
  'Content-Type':'application/json',
  'Accept':'application/json'

};

$.ajax({
  url: '://staging.whiplashmerch.com/api/v2/web_hooks',
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
  'X-Customer-Id':'string',
  'X-Shop-Id':'string',
  'Content-Type':'application/json',
  'Accept':'application/json'

};

fetch('://staging.whiplashmerch.com/api/v2/web_hooks',
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
  'X-Customer-Id' => 'string',
  'X-Shop-Id' => 'string',
  'Content-Type' => 'application/json',
  'Accept' => 'application/json'
}

result = RestClient.post '://staging.whiplashmerch.com/api/v2/web_hooks', params: {
  }, headers: headers

p JSON.parse(result)
```

```python
import requests
headers = {
  'X-Customer-Id': 'string',
  'X-Shop-Id': 'string',
  'Content-Type': 'application/json',
  'Accept': 'application/json'
}

r = requests.post('://staging.whiplashmerch.com/api/v2/web_hooks', params={

}, headers = headers)

print r.json()
```

```java
URL obj = new URL("://staging.whiplashmerch.com/api/v2/web_hooks");
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

`POST /api/v2/web_hooks`

*Create a web hook*

Create a web hook

### Parameters

Parameter|In|Type|Required|Description
---|---|---|---|---|
X-Customer-Id|header|string|false|The customer associated with this resource.
X-Shop-Id|header|string|false|The shop associated with this resource.
url|formData|string|false|No description
hookable_id|formData|integer|false|No description
hookable_type|formData|string|false|No description
format|formData|string|false|No description
web_hook_event_id|formData|integer|false|No description
failed_attempts|formData|integer|false|No description
active|formData|boolean|false|No description
event_name|formData|string|false|No description


### Responses

Status|Meaning|Description
---|---|---|
201|[Created](https://tools.ietf.org/html/rfc7231#section-6.3.2)|Create a web hook
401|[Unauthorized](https://tools.ietf.org/html/rfc7235#section-3.1)|No description
403|[Forbidden](https://tools.ietf.org/html/rfc7231#section-6.5.3)|No description
409|[Conflict](https://tools.ietf.org/html/rfc7231#section-6.5.8)|No description
422|[Unprocessable Entity](https://tools.ietf.org/html/rfc2518#section-10.3)|No description

> Example responses

```json
{
  "id": 0,
  "hookable_id": 0,
  "hookable_type": "string",
  "url": "string",
  "format": "string",
  "created_at": "2017-06-19T15:15:48Z",
  "updated_at": "2017-06-19T15:15:48Z",
  "web_hook_event_id": 0,
  "failed_attempts": 0,
  "active": true
}
```
```json
{
  "message": "string"
}
```
```json
{
  "message": "string"
}
```
```json
{
  "message": "string"
}
```
```json
{
  "message": "string"
}
```
<aside class="success">
This operation does not require authentication
</aside>

## getApiV2WebHooksCount

> Code samples

```shell
# You can also use wget
curl -X get ://staging.whiplashmerch.com/api/v2/web_hooks/count \
  -H 'X-Customer-Id: string' \
  -H 'X-Shop-Id: string' \
  -H 'Accept: application/json'

```

```http
GET ://staging.whiplashmerch.com/api/v2/web_hooks/count HTTP/1.1
Host: staging.whiplashmerch.com

Accept: application/json
X-Customer-Id: string
X-Shop-Id: string

```

```javascript
var headers = {
  'X-Customer-Id':'string',
  'X-Shop-Id':'string',
  'Accept':'application/json'

};

$.ajax({
  url: '://staging.whiplashmerch.com/api/v2/web_hooks/count',
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
  'X-Customer-Id':'string',
  'X-Shop-Id':'string',
  'Accept':'application/json'

};

fetch('://staging.whiplashmerch.com/api/v2/web_hooks/count',
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
  'X-Customer-Id' => 'string',
  'X-Shop-Id' => 'string',
  'Accept' => 'application/json'
}

result = RestClient.get '://staging.whiplashmerch.com/api/v2/web_hooks/count', params: {
  }, headers: headers

p JSON.parse(result)
```

```python
import requests
headers = {
  'X-Customer-Id': 'string',
  'X-Shop-Id': 'string',
  'Accept': 'application/json'
}

r = requests.get('://staging.whiplashmerch.com/api/v2/web_hooks/count', params={

}, headers = headers)

print r.json()
```

```java
URL obj = new URL("://staging.whiplashmerch.com/api/v2/web_hooks/count");
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

`GET /api/v2/web_hooks/count`

*Get a count of web hooks*

Get a count of web hooks

### Parameters

Parameter|In|Type|Required|Description
---|---|---|---|---|
X-Customer-Id|header|string|false|The customer associated with this resource.
X-Shop-Id|header|string|false|The shop associated with this resource.
search|query|string|false|JSON search string like {"attribute_eq": "Term"}


### Responses

Status|Meaning|Description
---|---|---|
200|[OK](https://tools.ietf.org/html/rfc7231#section-6.3.1)|Get a count of web hooks
401|[Unauthorized](https://tools.ietf.org/html/rfc7235#section-3.1)|No description
403|[Forbidden](https://tools.ietf.org/html/rfc7231#section-6.5.3)|No description

> Example responses

```json
{
  "id": 0,
  "hookable_id": 0,
  "hookable_type": "string",
  "url": "string",
  "format": "string",
  "created_at": "2017-06-19T15:15:48Z",
  "updated_at": "2017-06-19T15:15:48Z",
  "web_hook_event_id": 0,
  "failed_attempts": 0,
  "active": true
}
```
```json
{
  "message": "string"
}
```
```json
{
  "message": "string"
}
```
<aside class="success">
This operation does not require authentication
</aside>

## getApiV2WebHooksId

> Code samples

```shell
# You can also use wget
curl -X get ://staging.whiplashmerch.com/api/v2/web_hooks/{id} \
  -H 'X-Customer-Id: string' \
  -H 'X-Shop-Id: string' \
  -H 'Accept: application/json'

```

```http
GET ://staging.whiplashmerch.com/api/v2/web_hooks/{id} HTTP/1.1
Host: staging.whiplashmerch.com

Accept: application/json
X-Customer-Id: string
X-Shop-Id: string

```

```javascript
var headers = {
  'X-Customer-Id':'string',
  'X-Shop-Id':'string',
  'Accept':'application/json'

};

$.ajax({
  url: '://staging.whiplashmerch.com/api/v2/web_hooks/{id}',
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
  'X-Customer-Id':'string',
  'X-Shop-Id':'string',
  'Accept':'application/json'

};

fetch('://staging.whiplashmerch.com/api/v2/web_hooks/{id}',
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
  'X-Customer-Id' => 'string',
  'X-Shop-Id' => 'string',
  'Accept' => 'application/json'
}

result = RestClient.get '://staging.whiplashmerch.com/api/v2/web_hooks/{id}', params: {
  }, headers: headers

p JSON.parse(result)
```

```python
import requests
headers = {
  'X-Customer-Id': 'string',
  'X-Shop-Id': 'string',
  'Accept': 'application/json'
}

r = requests.get('://staging.whiplashmerch.com/api/v2/web_hooks/{id}', params={

}, headers = headers)

print r.json()
```

```java
URL obj = new URL("://staging.whiplashmerch.com/api/v2/web_hooks/{id}");
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

`GET /api/v2/web_hooks/{id}`

*Update a web hook*

Update a web hook

### Parameters

Parameter|In|Type|Required|Description
---|---|---|---|---|
X-Customer-Id|header|string|false|The customer associated with this resource.
X-Shop-Id|header|string|false|The shop associated with this resource.
url|query|string|false|No description
id|path|integer|true|No description


### Responses

Status|Meaning|Description
---|---|---|
200|[OK](https://tools.ietf.org/html/rfc7231#section-6.3.1)|Update a web hook
401|[Unauthorized](https://tools.ietf.org/html/rfc7235#section-3.1)|No description
403|[Forbidden](https://tools.ietf.org/html/rfc7231#section-6.5.3)|No description
422|[Unprocessable Entity](https://tools.ietf.org/html/rfc2518#section-10.3)|No description

> Example responses

```json
{
  "id": 0,
  "hookable_id": 0,
  "hookable_type": "string",
  "url": "string",
  "format": "string",
  "created_at": "2017-06-19T15:15:48Z",
  "updated_at": "2017-06-19T15:15:48Z",
  "web_hook_event_id": 0,
  "failed_attempts": 0,
  "active": true
}
```
```json
{
  "message": "string"
}
```
```json
{
  "message": "string"
}
```
```json
{
  "message": "string"
}
```
<aside class="success">
This operation does not require authentication
</aside>

## deleteApiV2WebHooksId

> Code samples

```shell
# You can also use wget
curl -X delete ://staging.whiplashmerch.com/api/v2/web_hooks/{id} \
  -H 'X-Customer-Id: string' \
  -H 'X-Shop-Id: string' \
  -H 'Accept: application/json'

```

```http
DELETE ://staging.whiplashmerch.com/api/v2/web_hooks/{id} HTTP/1.1
Host: staging.whiplashmerch.com

Accept: application/json
X-Customer-Id: string
X-Shop-Id: string

```

```javascript
var headers = {
  'X-Customer-Id':'string',
  'X-Shop-Id':'string',
  'Accept':'application/json'

};

$.ajax({
  url: '://staging.whiplashmerch.com/api/v2/web_hooks/{id}',
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
  'X-Customer-Id':'string',
  'X-Shop-Id':'string',
  'Accept':'application/json'

};

fetch('://staging.whiplashmerch.com/api/v2/web_hooks/{id}',
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
  'X-Customer-Id' => 'string',
  'X-Shop-Id' => 'string',
  'Accept' => 'application/json'
}

result = RestClient.delete '://staging.whiplashmerch.com/api/v2/web_hooks/{id}', params: {
  }, headers: headers

p JSON.parse(result)
```

```python
import requests
headers = {
  'X-Customer-Id': 'string',
  'X-Shop-Id': 'string',
  'Accept': 'application/json'
}

r = requests.delete('://staging.whiplashmerch.com/api/v2/web_hooks/{id}', params={

}, headers = headers)

print r.json()
```

```java
URL obj = new URL("://staging.whiplashmerch.com/api/v2/web_hooks/{id}");
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

`DELETE /api/v2/web_hooks/{id}`

*Delete a web hook*

Delete a web hook

### Parameters

Parameter|In|Type|Required|Description
---|---|---|---|---|
id|path|integer|true|No description
X-Customer-Id|header|string|false|The customer associated with this resource.
X-Shop-Id|header|string|false|The shop associated with this resource.


### Responses

Status|Meaning|Description
---|---|---|
200|[OK](https://tools.ietf.org/html/rfc7231#section-6.3.1)|Delete a web hook
401|[Unauthorized](https://tools.ietf.org/html/rfc7235#section-3.1)|No description
403|[Forbidden](https://tools.ietf.org/html/rfc7231#section-6.5.3)|No description
422|[Unprocessable Entity](https://tools.ietf.org/html/rfc2518#section-10.3)|No description

> Example responses

```json
{
  "id": 0,
  "hookable_id": 0,
  "hookable_type": "string",
  "url": "string",
  "format": "string",
  "created_at": "2017-06-19T15:15:48Z",
  "updated_at": "2017-06-19T15:15:48Z",
  "web_hook_event_id": 0,
  "failed_attempts": 0,
  "active": true
}
```
```json
{
  "message": "string"
}
```
```json
{
  "message": "string"
}
```
```json
{
  "message": "string"
}
```
<aside class="success">
This operation does not require authentication
</aside>

# filter_sets

Operations about filter_sets

## getApiV2FilterSets

> Code samples

```shell
# You can also use wget
curl -X get ://staging.whiplashmerch.com/api/v2/filter_sets \
  -H 'Accept: application/json'

```

```http
GET ://staging.whiplashmerch.com/api/v2/filter_sets HTTP/1.1
Host: staging.whiplashmerch.com

Accept: application/json

```

```javascript
var headers = {
  'Accept':'application/json'

};

$.ajax({
  url: '://staging.whiplashmerch.com/api/v2/filter_sets',
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
  'Accept':'application/json'

};

fetch('://staging.whiplashmerch.com/api/v2/filter_sets',
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
  'Accept' => 'application/json'
}

result = RestClient.get '://staging.whiplashmerch.com/api/v2/filter_sets', params: {
  }, headers: headers

p JSON.parse(result)
```

```python
import requests
headers = {
  'Accept': 'application/json'
}

r = requests.get('://staging.whiplashmerch.com/api/v2/filter_sets', params={

}, headers = headers)

print r.json()
```

```java
URL obj = new URL("://staging.whiplashmerch.com/api/v2/filter_sets");
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

`GET /api/v2/filter_sets`

*Returns all filter sets*

Returns all filter sets

### Parameters

Parameter|In|Type|Required|Description
---|---|---|---|---|
search|query|string|false|JSON search string like {"attribute_eq": "Term"}
fields|query|string|false|Comma-separated list of fields to include in the response
page|query|integer|false|Page of results to fetch.
per_page|query|integer|false|Number of results to return per page.


### Responses

Status|Meaning|Description
---|---|---|
200|[OK](https://tools.ietf.org/html/rfc7231#section-6.3.1)|Returns all filter sets
|Unknown|No description

> Example responses

```json
{
  "id": 0,
  "name": "string",
  "description": "string",
  "filters": "string",
  "saved_by_id": 0,
  "saved_by_type": "string",
  "access_token": "string",
  "type": "string",
  "visible": true,
  "favorite": true
}
```
```json
{
  "message": "string"
}
```
<aside class="success">
This operation does not require authentication
</aside>

## postApiV2FilterSets

> Code samples

```shell
# You can also use wget
curl -X post ://staging.whiplashmerch.com/api/v2/filter_sets \
  -H 'Content-Type: application/json' \
  -H 'Accept: application/json'

```

```http
POST ://staging.whiplashmerch.com/api/v2/filter_sets HTTP/1.1
Host: staging.whiplashmerch.com
Content-Type: application/json
Accept: application/json

```

```javascript
var headers = {
  'Content-Type':'application/json',
  'Accept':'application/json'

};

$.ajax({
  url: '://staging.whiplashmerch.com/api/v2/filter_sets',
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
  'Content-Type':'application/json',
  'Accept':'application/json'

};

fetch('://staging.whiplashmerch.com/api/v2/filter_sets',
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
  'Content-Type' => 'application/json',
  'Accept' => 'application/json'
}

result = RestClient.post '://staging.whiplashmerch.com/api/v2/filter_sets', params: {
  }, headers: headers

p JSON.parse(result)
```

```python
import requests
headers = {
  'Content-Type': 'application/json',
  'Accept': 'application/json'
}

r = requests.post('://staging.whiplashmerch.com/api/v2/filter_sets', params={

}, headers = headers)

print r.json()
```

```java
URL obj = new URL("://staging.whiplashmerch.com/api/v2/filter_sets");
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

`POST /api/v2/filter_sets`

*Create a filter set*

Create a filter set

### Parameters

Parameter|In|Type|Required|Description
---|---|---|---|---|
name|formData|string|false|filter set name.
description|formData|string|false|filter set description.
filters|formData|string|false|filter set filters.
access_token|formData|string|false|filter set access_token
type|formData|string|false|No description
visible|formData|boolean|false|filter set visible?.
favorite|formData|boolean|false|filter set favorited?.


### Responses

Status|Meaning|Description
---|---|---|
201|[Created](https://tools.ietf.org/html/rfc7231#section-6.3.2)|Create a filter set
|Unknown|No description

> Example responses

```json
{
  "id": 0,
  "name": "string",
  "description": "string",
  "filters": "string",
  "saved_by_id": 0,
  "saved_by_type": "string",
  "access_token": "string",
  "type": "string",
  "visible": true,
  "favorite": true
}
```
```json
{
  "message": "string"
}
```
<aside class="success">
This operation does not require authentication
</aside>

## getApiV2FilterSetsCount

> Code samples

```shell
# You can also use wget
curl -X get ://staging.whiplashmerch.com/api/v2/filter_sets/count \
  -H 'Accept: application/json'

```

```http
GET ://staging.whiplashmerch.com/api/v2/filter_sets/count HTTP/1.1
Host: staging.whiplashmerch.com

Accept: application/json

```

```javascript
var headers = {
  'Accept':'application/json'

};

$.ajax({
  url: '://staging.whiplashmerch.com/api/v2/filter_sets/count',
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
  'Accept':'application/json'

};

fetch('://staging.whiplashmerch.com/api/v2/filter_sets/count',
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
  'Accept' => 'application/json'
}

result = RestClient.get '://staging.whiplashmerch.com/api/v2/filter_sets/count', params: {
  }, headers: headers

p JSON.parse(result)
```

```python
import requests
headers = {
  'Accept': 'application/json'
}

r = requests.get('://staging.whiplashmerch.com/api/v2/filter_sets/count', params={

}, headers = headers)

print r.json()
```

```java
URL obj = new URL("://staging.whiplashmerch.com/api/v2/filter_sets/count");
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

`GET /api/v2/filter_sets/count`

*Returns count of filter sets*

Returns count of filter sets

### Parameters

Parameter|In|Type|Required|Description
---|---|---|---|---|
search|query|string|false|JSON search string like {"attribute_eq": "Term"}


### Responses

Status|Meaning|Description
---|---|---|
200|[OK](https://tools.ietf.org/html/rfc7231#section-6.3.1)|Returns count of filter sets
|Unknown|No description

> Example responses

```json
{
  "id": 0,
  "name": "string",
  "description": "string",
  "filters": "string",
  "saved_by_id": 0,
  "saved_by_type": "string",
  "access_token": "string",
  "type": "string",
  "visible": true,
  "favorite": true
}
```
```json
{
  "message": "string"
}
```
<aside class="success">
This operation does not require authentication
</aside>

## getApiV2FilterSetsOptions

> Code samples

```shell
# You can also use wget
curl -X get ://staging.whiplashmerch.com/api/v2/filter_sets/options \
  -H 'Accept: application/json'

```

```http
GET ://staging.whiplashmerch.com/api/v2/filter_sets/options HTTP/1.1
Host: staging.whiplashmerch.com

Accept: application/json

```

```javascript
var headers = {
  'Accept':'application/json'

};

$.ajax({
  url: '://staging.whiplashmerch.com/api/v2/filter_sets/options',
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
  'Accept':'application/json'

};

fetch('://staging.whiplashmerch.com/api/v2/filter_sets/options',
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
  'Accept' => 'application/json'
}

result = RestClient.get '://staging.whiplashmerch.com/api/v2/filter_sets/options', params: {
  }, headers: headers

p JSON.parse(result)
```

```python
import requests
headers = {
  'Accept': 'application/json'
}

r = requests.get('://staging.whiplashmerch.com/api/v2/filter_sets/options', params={

}, headers = headers)

print r.json()
```

```java
URL obj = new URL("://staging.whiplashmerch.com/api/v2/filter_sets/options");
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

`GET /api/v2/filter_sets/options`

*Returns filter set options*

Returns filter set options

### Responses

Status|Meaning|Description
---|---|---|
200|[OK](https://tools.ietf.org/html/rfc7231#section-6.3.1)|Returns filter set options
|Unknown|No description

> Example responses

```json
{
  "message": "string"
}
```
<aside class="success">
This operation does not require authentication
</aside>

## getApiV2FilterSetsId

> Code samples

```shell
# You can also use wget
curl -X get ://staging.whiplashmerch.com/api/v2/filter_sets/{id} \
  -H 'Accept: application/json'

```

```http
GET ://staging.whiplashmerch.com/api/v2/filter_sets/{id} HTTP/1.1
Host: staging.whiplashmerch.com

Accept: application/json

```

```javascript
var headers = {
  'Accept':'application/json'

};

$.ajax({
  url: '://staging.whiplashmerch.com/api/v2/filter_sets/{id}',
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
  'Accept':'application/json'

};

fetch('://staging.whiplashmerch.com/api/v2/filter_sets/{id}',
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
  'Accept' => 'application/json'
}

result = RestClient.get '://staging.whiplashmerch.com/api/v2/filter_sets/{id}', params: {
  }, headers: headers

p JSON.parse(result)
```

```python
import requests
headers = {
  'Accept': 'application/json'
}

r = requests.get('://staging.whiplashmerch.com/api/v2/filter_sets/{id}', params={

}, headers = headers)

print r.json()
```

```java
URL obj = new URL("://staging.whiplashmerch.com/api/v2/filter_sets/{id}");
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

`GET /api/v2/filter_sets/{id}`

*Returns a filter set*

Returns a filter set

### Parameters

Parameter|In|Type|Required|Description
---|---|---|---|---|
id|path|integer|true|No description


### Responses

Status|Meaning|Description
---|---|---|
200|[OK](https://tools.ietf.org/html/rfc7231#section-6.3.1)|Returns a filter set
|Unknown|No description

> Example responses

```json
{
  "id": 0,
  "name": "string",
  "description": "string",
  "filters": "string",
  "saved_by_id": 0,
  "saved_by_type": "string",
  "access_token": "string",
  "type": "string",
  "visible": true,
  "favorite": true
}
```
```json
{
  "message": "string"
}
```
<aside class="success">
This operation does not require authentication
</aside>

## putApiV2FilterSetsId

> Code samples

```shell
# You can also use wget
curl -X put ://staging.whiplashmerch.com/api/v2/filter_sets/{id} \
  -H 'Content-Type: application/json' \
  -H 'Accept: application/json'

```

```http
PUT ://staging.whiplashmerch.com/api/v2/filter_sets/{id} HTTP/1.1
Host: staging.whiplashmerch.com
Content-Type: application/json
Accept: application/json

```

```javascript
var headers = {
  'Content-Type':'application/json',
  'Accept':'application/json'

};

$.ajax({
  url: '://staging.whiplashmerch.com/api/v2/filter_sets/{id}',
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
  'Content-Type':'application/json',
  'Accept':'application/json'

};

fetch('://staging.whiplashmerch.com/api/v2/filter_sets/{id}',
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
  'Content-Type' => 'application/json',
  'Accept' => 'application/json'
}

result = RestClient.put '://staging.whiplashmerch.com/api/v2/filter_sets/{id}', params: {
  }, headers: headers

p JSON.parse(result)
```

```python
import requests
headers = {
  'Content-Type': 'application/json',
  'Accept': 'application/json'
}

r = requests.put('://staging.whiplashmerch.com/api/v2/filter_sets/{id}', params={

}, headers = headers)

print r.json()
```

```java
URL obj = new URL("://staging.whiplashmerch.com/api/v2/filter_sets/{id}");
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

`PUT /api/v2/filter_sets/{id}`

*Update a filter set*

Update a filter set

### Parameters

Parameter|In|Type|Required|Description
---|---|---|---|---|
name|formData|string|false|filter set name.
description|formData|string|false|filter set description.
filters|formData|string|false|filter set filters.
access_token|formData|string|false|filter set access_token
type|formData|string|false|No description
visible|formData|boolean|false|filter set visible?.
favorite|formData|boolean|false|filter set favorited?.
id|path|integer|true|No description


### Responses

Status|Meaning|Description
---|---|---|
200|[OK](https://tools.ietf.org/html/rfc7231#section-6.3.1)|Update a filter set
|Unknown|No description

> Example responses

```json
{
  "id": 0,
  "name": "string",
  "description": "string",
  "filters": "string",
  "saved_by_id": 0,
  "saved_by_type": "string",
  "access_token": "string",
  "type": "string",
  "visible": true,
  "favorite": true
}
```
```json
{
  "message": "string"
}
```
<aside class="success">
This operation does not require authentication
</aside>

## deleteApiV2FilterSetsId

> Code samples

```shell
# You can also use wget
curl -X delete ://staging.whiplashmerch.com/api/v2/filter_sets/{id} \
  -H 'Accept: application/json'

```

```http
DELETE ://staging.whiplashmerch.com/api/v2/filter_sets/{id} HTTP/1.1
Host: staging.whiplashmerch.com

Accept: application/json

```

```javascript
var headers = {
  'Accept':'application/json'

};

$.ajax({
  url: '://staging.whiplashmerch.com/api/v2/filter_sets/{id}',
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
  'Accept':'application/json'

};

fetch('://staging.whiplashmerch.com/api/v2/filter_sets/{id}',
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
  'Accept' => 'application/json'
}

result = RestClient.delete '://staging.whiplashmerch.com/api/v2/filter_sets/{id}', params: {
  }, headers: headers

p JSON.parse(result)
```

```python
import requests
headers = {
  'Accept': 'application/json'
}

r = requests.delete('://staging.whiplashmerch.com/api/v2/filter_sets/{id}', params={

}, headers = headers)

print r.json()
```

```java
URL obj = new URL("://staging.whiplashmerch.com/api/v2/filter_sets/{id}");
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

`DELETE /api/v2/filter_sets/{id}`

*Destroy a filter set*

Destroy a filter set

### Parameters

Parameter|In|Type|Required|Description
---|---|---|---|---|
id|path|integer|true|No description


### Responses

Status|Meaning|Description
---|---|---|
200|[OK](https://tools.ietf.org/html/rfc7231#section-6.3.1)|Destroy a filter set
|Unknown|No description

> Example responses

```json
{
  "id": 0,
  "name": "string",
  "description": "string",
  "filters": "string",
  "saved_by_id": 0,
  "saved_by_type": "string",
  "access_token": "string",
  "type": "string",
  "visible": true,
  "favorite": true
}
```
```json
{
  "message": "string"
}
```
<aside class="success">
This operation does not require authentication
</aside>

## getApiV2FilterSetsIdResults

> Code samples

```shell
# You can also use wget
curl -X get ://staging.whiplashmerch.com/api/v2/filter_sets/{id}/results \
  -H 'Accept: application/json'

```

```http
GET ://staging.whiplashmerch.com/api/v2/filter_sets/{id}/results HTTP/1.1
Host: staging.whiplashmerch.com

Accept: application/json

```

```javascript
var headers = {
  'Accept':'application/json'

};

$.ajax({
  url: '://staging.whiplashmerch.com/api/v2/filter_sets/{id}/results',
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
  'Accept':'application/json'

};

fetch('://staging.whiplashmerch.com/api/v2/filter_sets/{id}/results',
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
  'Accept' => 'application/json'
}

result = RestClient.get '://staging.whiplashmerch.com/api/v2/filter_sets/{id}/results', params: {
  }, headers: headers

p JSON.parse(result)
```

```python
import requests
headers = {
  'Accept': 'application/json'
}

r = requests.get('://staging.whiplashmerch.com/api/v2/filter_sets/{id}/results', params={

}, headers = headers)

print r.json()
```

```java
URL obj = new URL("://staging.whiplashmerch.com/api/v2/filter_sets/{id}/results");
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

`GET /api/v2/filter_sets/{id}/results`

*Returns the filter set search results*

Returns the filter set search results

### Parameters

Parameter|In|Type|Required|Description
---|---|---|---|---|
search|query|string|false|JSON search string like {"attribute_eq": "Term"}
page|query|integer|false|Page of results to fetch.
per_page|query|integer|false|Number of results to return per page.
id|path|integer|true|No description


### Responses

Status|Meaning|Description
---|---|---|
200|[OK](https://tools.ietf.org/html/rfc7231#section-6.3.1)|Returns the filter set search results
|Unknown|No description

> Example responses

```json
{
  "id": 0,
  "customer_id": 0,
  "first_name": "string",
  "last_name": "string",
  "full_name": "string",
  "billing_company": "string",
  "billing_address_1": "string",
  "billing_address_2": "string",
  "billing_city": "string",
  "billing_state": "string",
  "billing_zip": "string",
  "billing_country": "string",
  "billing_phone": "string",
  "shipping_company": "string",
  "shipping_address_1": "string",
  "shipping_address_2": "string",
  "shipping_city": "string",
  "shipping_state": "string",
  "shipping_zip": "string",
  "shipping_country": "string",
  "shipping_phone": "string",
  "email": "string",
  "ship_actual_cost": 0,
  "shipped_on": "2017-06-19T15:15:48Z",
  "ship_notes": "string",
  "created_at": "2017-06-19T15:15:48Z",
  "updated_at": "2017-06-19T15:15:48Z",
  "shipping_name": "string",
  "shop_shipping_method_price": 0,
  "shipping_confirmation_sent": true,
  "status": 0,
  "previous_status": 0,
  "ship_3rdparty_cost": 0,
  "public_note": "string",
  "gift": true,
  "billed": true,
  "ship_3rdparty_account": "string",
  "ship_3rdparty_zip": "string",
  "ship_3rdparty_country": "string",
  "shop_shipping_method_text": "string",
  "order_batch_id": 0,
  "order_orig": "string",
  "days_in_transit": 0,
  "quote_id": 0,
  "shipping_country_iso2": "string",
  "insure": true,
  "require_signature": true,
  "req_insurance_value": 0,
  "warehouse_id": 0,
  "workable_at": "2017-06-19T15:15:48Z",
  "requested_address": "string",
  "address_verified": true,
  "address_message": "string",
  "return_city": "string",
  "return_state": "string",
  "return_country": "string",
  "return_zip": "string",
  "return_address_1": "string",
  "return_address_2": "string",
  "return_phone": "string",
  "return_email": "string",
  "level1_token": "string",
  "level2_token": "string",
  "return_time_limit": 0,
  "return_address_verified": true,
  "shipping_method_id": 0,
  "skip_street_date": true,
  "shop_warehouse_id": 0,
  "shop_shipping_method_currency": "string",
  "saturday_delivery": true,
  "shop_created_at": "2017-06-19T15:15:48Z",
  "shop_updated_at": "2017-06-19T15:15:48Z",
  "residential": true,
  "skip_address_verification": true,
  "due_at": "2017-06-19T15:15:48Z",
  "do_not_bill": true,
  "return_company": "string",
  "contains_alcohol": true,
  "require_adult_signature": true,
  "order_items": {
    "id": 0,
    "order_id": 0,
    "sku": "string",
    "description": "string",
    "quantity": 0,
    "price": 0,
    "created_at": "2017-06-19T15:15:48Z",
    "updated_at": "2017-06-19T15:15:48Z",
    "unshippable": true,
    "customer_id": 0,
    "item_id": 0,
    "available": true,
    "packed": 0,
    "packaging": true,
    "wholesale_cost": 0,
    "package_id": 0,
    "is_bundle": true,
    "retail_fee": 0,
    "promo": true,
    "quote_item_id": 0,
    "returnable": true,
    "currency": "string",
    "wholesale_fee": 0
  },
  "ship_method": "string",
  "status_name": "string"
}
```
```json
{
  "message": "string"
}
```
<aside class="success">
This operation does not require authentication
</aside>

## getApiV2FilterSetsIdResultsCount

> Code samples

```shell
# You can also use wget
curl -X get ://staging.whiplashmerch.com/api/v2/filter_sets/{id}/results/count \
  -H 'Accept: application/json'

```

```http
GET ://staging.whiplashmerch.com/api/v2/filter_sets/{id}/results/count HTTP/1.1
Host: staging.whiplashmerch.com

Accept: application/json

```

```javascript
var headers = {
  'Accept':'application/json'

};

$.ajax({
  url: '://staging.whiplashmerch.com/api/v2/filter_sets/{id}/results/count',
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
  'Accept':'application/json'

};

fetch('://staging.whiplashmerch.com/api/v2/filter_sets/{id}/results/count',
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
  'Accept' => 'application/json'
}

result = RestClient.get '://staging.whiplashmerch.com/api/v2/filter_sets/{id}/results/count', params: {
  }, headers: headers

p JSON.parse(result)
```

```python
import requests
headers = {
  'Accept': 'application/json'
}

r = requests.get('://staging.whiplashmerch.com/api/v2/filter_sets/{id}/results/count', params={

}, headers = headers)

print r.json()
```

```java
URL obj = new URL("://staging.whiplashmerch.com/api/v2/filter_sets/{id}/results/count");
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

`GET /api/v2/filter_sets/{id}/results/count`

*Returns the filter set search result count*

Returns the filter set search result count

### Parameters

Parameter|In|Type|Required|Description
---|---|---|---|---|
search|query|string|false|JSON search string like {"attribute_eq": "Term"}
id|path|integer|true|No description


### Responses

Status|Meaning|Description
---|---|---|
200|[OK](https://tools.ietf.org/html/rfc7231#section-6.3.1)|Returns the filter set search result count
|Unknown|No description

> Example responses

```json
{
  "id": 0,
  "customer_id": 0,
  "first_name": "string",
  "last_name": "string",
  "full_name": "string",
  "billing_company": "string",
  "billing_address_1": "string",
  "billing_address_2": "string",
  "billing_city": "string",
  "billing_state": "string",
  "billing_zip": "string",
  "billing_country": "string",
  "billing_phone": "string",
  "shipping_company": "string",
  "shipping_address_1": "string",
  "shipping_address_2": "string",
  "shipping_city": "string",
  "shipping_state": "string",
  "shipping_zip": "string",
  "shipping_country": "string",
  "shipping_phone": "string",
  "email": "string",
  "ship_actual_cost": 0,
  "shipped_on": "2017-06-19T15:15:48Z",
  "ship_notes": "string",
  "created_at": "2017-06-19T15:15:48Z",
  "updated_at": "2017-06-19T15:15:48Z",
  "shipping_name": "string",
  "shop_shipping_method_price": 0,
  "shipping_confirmation_sent": true,
  "status": 0,
  "previous_status": 0,
  "ship_3rdparty_cost": 0,
  "public_note": "string",
  "gift": true,
  "billed": true,
  "ship_3rdparty_account": "string",
  "ship_3rdparty_zip": "string",
  "ship_3rdparty_country": "string",
  "shop_shipping_method_text": "string",
  "order_batch_id": 0,
  "order_orig": "string",
  "days_in_transit": 0,
  "quote_id": 0,
  "shipping_country_iso2": "string",
  "insure": true,
  "require_signature": true,
  "req_insurance_value": 0,
  "warehouse_id": 0,
  "workable_at": "2017-06-19T15:15:48Z",
  "requested_address": "string",
  "address_verified": true,
  "address_message": "string",
  "return_city": "string",
  "return_state": "string",
  "return_country": "string",
  "return_zip": "string",
  "return_address_1": "string",
  "return_address_2": "string",
  "return_phone": "string",
  "return_email": "string",
  "level1_token": "string",
  "level2_token": "string",
  "return_time_limit": 0,
  "return_address_verified": true,
  "shipping_method_id": 0,
  "skip_street_date": true,
  "shop_warehouse_id": 0,
  "shop_shipping_method_currency": "string",
  "saturday_delivery": true,
  "shop_created_at": "2017-06-19T15:15:48Z",
  "shop_updated_at": "2017-06-19T15:15:48Z",
  "residential": true,
  "skip_address_verification": true,
  "due_at": "2017-06-19T15:15:48Z",
  "do_not_bill": true,
  "return_company": "string",
  "contains_alcohol": true,
  "require_adult_signature": true,
  "order_items": {
    "id": 0,
    "order_id": 0,
    "sku": "string",
    "description": "string",
    "quantity": 0,
    "price": 0,
    "created_at": "2017-06-19T15:15:48Z",
    "updated_at": "2017-06-19T15:15:48Z",
    "unshippable": true,
    "customer_id": 0,
    "item_id": 0,
    "available": true,
    "packed": 0,
    "packaging": true,
    "wholesale_cost": 0,
    "package_id": 0,
    "is_bundle": true,
    "retail_fee": 0,
    "promo": true,
    "quote_item_id": 0,
    "returnable": true,
    "currency": "string",
    "wholesale_fee": 0
  },
  "ship_method": "string",
  "status_name": "string"
}
```
```json
{
  "message": "string"
}
```
<aside class="success">
This operation does not require authentication
</aside>

# locales

Operations about locales

## getApiV2Locales

> Code samples

```shell
# You can also use wget
curl -X get ://staging.whiplashmerch.com/api/v2/locales \
  -H 'Accept: application/json'

```

```http
GET ://staging.whiplashmerch.com/api/v2/locales HTTP/1.1
Host: staging.whiplashmerch.com

Accept: application/json

```

```javascript
var headers = {
  'Accept':'application/json'

};

$.ajax({
  url: '://staging.whiplashmerch.com/api/v2/locales',
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
  'Accept':'application/json'

};

fetch('://staging.whiplashmerch.com/api/v2/locales',
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
  'Accept' => 'application/json'
}

result = RestClient.get '://staging.whiplashmerch.com/api/v2/locales', params: {
  }, headers: headers

p JSON.parse(result)
```

```python
import requests
headers = {
  'Accept': 'application/json'
}

r = requests.get('://staging.whiplashmerch.com/api/v2/locales', params={

}, headers = headers)

print r.json()
```

```java
URL obj = new URL("://staging.whiplashmerch.com/api/v2/locales");
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

`GET /api/v2/locales`

*Returns locales *

Returns locales 

### Responses

Status|Meaning|Description
---|---|---|
200|[OK](https://tools.ietf.org/html/rfc7231#section-6.3.1)|Returns locales
|Unknown|No description

> Example responses

```json
{
  "message": "string"
}
```
<aside class="success">
This operation does not require authentication
</aside>

# locations

Operations about locations

## getApiV2Locations

> Code samples

```shell
# You can also use wget
curl -X get ://staging.whiplashmerch.com/api/v2/locations \
  -H 'Accept: application/json'

```

```http
GET ://staging.whiplashmerch.com/api/v2/locations HTTP/1.1
Host: staging.whiplashmerch.com

Accept: application/json

```

```javascript
var headers = {
  'Accept':'application/json'

};

$.ajax({
  url: '://staging.whiplashmerch.com/api/v2/locations',
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
  'Accept':'application/json'

};

fetch('://staging.whiplashmerch.com/api/v2/locations',
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
  'Accept' => 'application/json'
}

result = RestClient.get '://staging.whiplashmerch.com/api/v2/locations', params: {
  }, headers: headers

p JSON.parse(result)
```

```python
import requests
headers = {
  'Accept': 'application/json'
}

r = requests.get('://staging.whiplashmerch.com/api/v2/locations', params={

}, headers = headers)

print r.json()
```

```java
URL obj = new URL("://staging.whiplashmerch.com/api/v2/locations");
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

`GET /api/v2/locations`

*Get all locations*

Get all locations

### Parameters

Parameter|In|Type|Required|Description
---|---|---|---|---|
search|query|string|false|JSON search string like {"attribute_eq": "Term"}
fields|query|string|false|Comma-separated list of fields to include in the response
page|query|integer|false|Page of results to fetch.
per_page|query|integer|false|Number of results to return per page.


### Responses

Status|Meaning|Description
---|---|---|
200|[OK](https://tools.ietf.org/html/rfc7231#section-6.3.1)|Get all locations
401|[Unauthorized](https://tools.ietf.org/html/rfc7235#section-3.1)|No description
403|[Forbidden](https://tools.ietf.org/html/rfc7231#section-6.5.3)|No description

> Example responses

```json
{
  "id": 0,
  "name": "string",
  "item_id": 0,
  "quantity": 0,
  "warehouse_id": 0,
  "shipnotice_item_id": 0,
  "active": true,
  "pickable": true
}
```
```json
{
  "message": "string"
}
```
```json
{
  "message": "string"
}
```
<aside class="success">
This operation does not require authentication
</aside>

## postApiV2Locations

> Code samples

```shell
# You can also use wget
curl -X post ://staging.whiplashmerch.com/api/v2/locations \
  -H 'Content-Type: application/json' \
  -H 'Accept: application/json'

```

```http
POST ://staging.whiplashmerch.com/api/v2/locations HTTP/1.1
Host: staging.whiplashmerch.com
Content-Type: application/json
Accept: application/json

```

```javascript
var headers = {
  'Content-Type':'application/json',
  'Accept':'application/json'

};

$.ajax({
  url: '://staging.whiplashmerch.com/api/v2/locations',
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
  'Content-Type':'application/json',
  'Accept':'application/json'

};

fetch('://staging.whiplashmerch.com/api/v2/locations',
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
  'Content-Type' => 'application/json',
  'Accept' => 'application/json'
}

result = RestClient.post '://staging.whiplashmerch.com/api/v2/locations', params: {
  }, headers: headers

p JSON.parse(result)
```

```python
import requests
headers = {
  'Content-Type': 'application/json',
  'Accept': 'application/json'
}

r = requests.post('://staging.whiplashmerch.com/api/v2/locations', params={

}, headers = headers)

print r.json()
```

```java
URL obj = new URL("://staging.whiplashmerch.com/api/v2/locations");
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

`POST /api/v2/locations`

*Create a location*

Create a location

### Parameters

Parameter|In|Type|Required|Description
---|---|---|---|---|
item_id|formData|integer|false|item_id of item in location
name|formData|string|true|location name.
quantity|formData|integer|false|No description
warehouse_id|formData|integer|false|warehouse_id of location
shipnotice_item_id|formData|integer|false|shipnotice_item_id of location
active|formData|boolean|false|is this location active?
pickable|formData|boolean|false|is this location pickable?.


### Responses

Status|Meaning|Description
---|---|---|
201|[Created](https://tools.ietf.org/html/rfc7231#section-6.3.2)|Create a location
401|[Unauthorized](https://tools.ietf.org/html/rfc7235#section-3.1)|No description
403|[Forbidden](https://tools.ietf.org/html/rfc7231#section-6.5.3)|No description
409|[Conflict](https://tools.ietf.org/html/rfc7231#section-6.5.8)|No description
422|[Unprocessable Entity](https://tools.ietf.org/html/rfc2518#section-10.3)|No description

> Example responses

```json
{
  "id": 0,
  "name": "string",
  "item_id": 0,
  "quantity": 0,
  "warehouse_id": 0,
  "shipnotice_item_id": 0,
  "active": true,
  "pickable": true
}
```
```json
{
  "message": "string"
}
```
```json
{
  "message": "string"
}
```
```json
{
  "message": "string"
}
```
```json
{
  "message": "string"
}
```
<aside class="success">
This operation does not require authentication
</aside>

## getApiV2LocationsCount

> Code samples

```shell
# You can also use wget
curl -X get ://staging.whiplashmerch.com/api/v2/locations/count \
  -H 'Accept: application/json'

```

```http
GET ://staging.whiplashmerch.com/api/v2/locations/count HTTP/1.1
Host: staging.whiplashmerch.com

Accept: application/json

```

```javascript
var headers = {
  'Accept':'application/json'

};

$.ajax({
  url: '://staging.whiplashmerch.com/api/v2/locations/count',
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
  'Accept':'application/json'

};

fetch('://staging.whiplashmerch.com/api/v2/locations/count',
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
  'Accept' => 'application/json'
}

result = RestClient.get '://staging.whiplashmerch.com/api/v2/locations/count', params: {
  }, headers: headers

p JSON.parse(result)
```

```python
import requests
headers = {
  'Accept': 'application/json'
}

r = requests.get('://staging.whiplashmerch.com/api/v2/locations/count', params={

}, headers = headers)

print r.json()
```

```java
URL obj = new URL("://staging.whiplashmerch.com/api/v2/locations/count");
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

`GET /api/v2/locations/count`

*Returns count of locations*

Returns count of locations

### Parameters

Parameter|In|Type|Required|Description
---|---|---|---|---|
search|query|string|false|JSON search string like {"attribute_eq": "Term"}


### Responses

Status|Meaning|Description
---|---|---|
200|[OK](https://tools.ietf.org/html/rfc7231#section-6.3.1)|Returns count of locations
401|[Unauthorized](https://tools.ietf.org/html/rfc7235#section-3.1)|No description
403|[Forbidden](https://tools.ietf.org/html/rfc7231#section-6.5.3)|No description

> Example responses

```json
{
  "id": 0,
  "name": "string",
  "item_id": 0,
  "quantity": 0,
  "warehouse_id": 0,
  "shipnotice_item_id": 0,
  "active": true,
  "pickable": true
}
```
```json
{
  "message": "string"
}
```
```json
{
  "message": "string"
}
```
<aside class="success">
This operation does not require authentication
</aside>

## getApiV2LocationsId

> Code samples

```shell
# You can also use wget
curl -X get ://staging.whiplashmerch.com/api/v2/locations/{id} \
  -H 'Accept: application/json'

```

```http
GET ://staging.whiplashmerch.com/api/v2/locations/{id} HTTP/1.1
Host: staging.whiplashmerch.com

Accept: application/json

```

```javascript
var headers = {
  'Accept':'application/json'

};

$.ajax({
  url: '://staging.whiplashmerch.com/api/v2/locations/{id}',
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
  'Accept':'application/json'

};

fetch('://staging.whiplashmerch.com/api/v2/locations/{id}',
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
  'Accept' => 'application/json'
}

result = RestClient.get '://staging.whiplashmerch.com/api/v2/locations/{id}', params: {
  }, headers: headers

p JSON.parse(result)
```

```python
import requests
headers = {
  'Accept': 'application/json'
}

r = requests.get('://staging.whiplashmerch.com/api/v2/locations/{id}', params={

}, headers = headers)

print r.json()
```

```java
URL obj = new URL("://staging.whiplashmerch.com/api/v2/locations/{id}");
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

`GET /api/v2/locations/{id}`

*Get a Location*

Get a Location

### Parameters

Parameter|In|Type|Required|Description
---|---|---|---|---|
id|path|integer|true|No description


### Responses

Status|Meaning|Description
---|---|---|
200|[OK](https://tools.ietf.org/html/rfc7231#section-6.3.1)|Get a Location
401|[Unauthorized](https://tools.ietf.org/html/rfc7235#section-3.1)|No description
403|[Forbidden](https://tools.ietf.org/html/rfc7231#section-6.5.3)|No description

> Example responses

```json
{
  "id": 0,
  "name": "string",
  "item_id": 0,
  "quantity": 0,
  "warehouse_id": 0,
  "shipnotice_item_id": 0,
  "active": true,
  "pickable": true
}
```
```json
{
  "message": "string"
}
```
```json
{
  "message": "string"
}
```
<aside class="success">
This operation does not require authentication
</aside>

## putApiV2LocationsId

> Code samples

```shell
# You can also use wget
curl -X put ://staging.whiplashmerch.com/api/v2/locations/{id} \
  -H 'Content-Type: application/json' \
  -H 'Accept: application/json'

```

```http
PUT ://staging.whiplashmerch.com/api/v2/locations/{id} HTTP/1.1
Host: staging.whiplashmerch.com
Content-Type: application/json
Accept: application/json

```

```javascript
var headers = {
  'Content-Type':'application/json',
  'Accept':'application/json'

};

$.ajax({
  url: '://staging.whiplashmerch.com/api/v2/locations/{id}',
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
  'Content-Type':'application/json',
  'Accept':'application/json'

};

fetch('://staging.whiplashmerch.com/api/v2/locations/{id}',
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
  'Content-Type' => 'application/json',
  'Accept' => 'application/json'
}

result = RestClient.put '://staging.whiplashmerch.com/api/v2/locations/{id}', params: {
  }, headers: headers

p JSON.parse(result)
```

```python
import requests
headers = {
  'Content-Type': 'application/json',
  'Accept': 'application/json'
}

r = requests.put('://staging.whiplashmerch.com/api/v2/locations/{id}', params={

}, headers = headers)

print r.json()
```

```java
URL obj = new URL("://staging.whiplashmerch.com/api/v2/locations/{id}");
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

`PUT /api/v2/locations/{id}`

*Update a location*

Update a location

### Parameters

Parameter|In|Type|Required|Description
---|---|---|---|---|
name|formData|string|false|No description
quantity|formData|integer|false|No description
warehouse_id|formData|integer|false|warehouse_id of location
shipnotice_item_id|formData|integer|false|shipnotice_item_id of location
active|formData|boolean|false|is this location active?
pickable|formData|boolean|false|is this location pickable?.
id|path|integer|true|No description


### Responses

Status|Meaning|Description
---|---|---|
200|[OK](https://tools.ietf.org/html/rfc7231#section-6.3.1)|Update a location
401|[Unauthorized](https://tools.ietf.org/html/rfc7235#section-3.1)|No description
403|[Forbidden](https://tools.ietf.org/html/rfc7231#section-6.5.3)|No description
422|[Unprocessable Entity](https://tools.ietf.org/html/rfc2518#section-10.3)|No description

> Example responses

```json
{
  "id": 0,
  "name": "string",
  "item_id": 0,
  "quantity": 0,
  "warehouse_id": 0,
  "shipnotice_item_id": 0,
  "active": true,
  "pickable": true
}
```
```json
{
  "message": "string"
}
```
```json
{
  "message": "string"
}
```
```json
{
  "message": "string"
}
```
<aside class="success">
This operation does not require authentication
</aside>

## deleteApiV2LocationsId

> Code samples

```shell
# You can also use wget
curl -X delete ://staging.whiplashmerch.com/api/v2/locations/{id} \
  -H 'Accept: application/json'

```

```http
DELETE ://staging.whiplashmerch.com/api/v2/locations/{id} HTTP/1.1
Host: staging.whiplashmerch.com

Accept: application/json

```

```javascript
var headers = {
  'Accept':'application/json'

};

$.ajax({
  url: '://staging.whiplashmerch.com/api/v2/locations/{id}',
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
  'Accept':'application/json'

};

fetch('://staging.whiplashmerch.com/api/v2/locations/{id}',
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
  'Accept' => 'application/json'
}

result = RestClient.delete '://staging.whiplashmerch.com/api/v2/locations/{id}', params: {
  }, headers: headers

p JSON.parse(result)
```

```python
import requests
headers = {
  'Accept': 'application/json'
}

r = requests.delete('://staging.whiplashmerch.com/api/v2/locations/{id}', params={

}, headers = headers)

print r.json()
```

```java
URL obj = new URL("://staging.whiplashmerch.com/api/v2/locations/{id}");
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

`DELETE /api/v2/locations/{id}`

*Destroy a location*

Destroy a location

### Parameters

Parameter|In|Type|Required|Description
---|---|---|---|---|
id|path|integer|true|No description


### Responses

Status|Meaning|Description
---|---|---|
200|[OK](https://tools.ietf.org/html/rfc7231#section-6.3.1)|Destroy a location
401|[Unauthorized](https://tools.ietf.org/html/rfc7235#section-3.1)|No description
403|[Forbidden](https://tools.ietf.org/html/rfc7231#section-6.5.3)|No description
422|[Unprocessable Entity](https://tools.ietf.org/html/rfc2518#section-10.3)|No description

> Example responses

```json
{
  "id": 0,
  "name": "string",
  "item_id": 0,
  "quantity": 0,
  "warehouse_id": 0,
  "shipnotice_item_id": 0,
  "active": true,
  "pickable": true
}
```
```json
{
  "message": "string"
}
```
```json
{
  "message": "string"
}
```
```json
{
  "message": "string"
}
```
<aside class="success">
This operation does not require authentication
</aside>

# shipnotices

Operations about shipnotices

## getApiV2Shipnotices

> Code samples

```shell
# You can also use wget
curl -X get ://staging.whiplashmerch.com/api/v2/shipnotices \
  -H 'X-Customer-Id: string' \
  -H 'Accept: application/json'

```

```http
GET ://staging.whiplashmerch.com/api/v2/shipnotices HTTP/1.1
Host: staging.whiplashmerch.com

Accept: application/json
X-Customer-Id: string

```

```javascript
var headers = {
  'X-Customer-Id':'string',
  'Accept':'application/json'

};

$.ajax({
  url: '://staging.whiplashmerch.com/api/v2/shipnotices',
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
  'X-Customer-Id':'string',
  'Accept':'application/json'

};

fetch('://staging.whiplashmerch.com/api/v2/shipnotices',
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
  'X-Customer-Id' => 'string',
  'Accept' => 'application/json'
}

result = RestClient.get '://staging.whiplashmerch.com/api/v2/shipnotices', params: {
  }, headers: headers

p JSON.parse(result)
```

```python
import requests
headers = {
  'X-Customer-Id': 'string',
  'Accept': 'application/json'
}

r = requests.get('://staging.whiplashmerch.com/api/v2/shipnotices', params={

}, headers = headers)

print r.json()
```

```java
URL obj = new URL("://staging.whiplashmerch.com/api/v2/shipnotices");
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

`GET /api/v2/shipnotices`

*Get all shipnotices*

Get all shipnotices

### Parameters

Parameter|In|Type|Required|Description
---|---|---|---|---|
X-Customer-Id|header|string|false|The customer associated with this resource.
search|query|string|false|JSON search string like {"attribute_eq": "Term"}
fields|query|string|false|Comma-separated list of fields to include in the response
page|query|integer|false|Page of results to fetch.
per_page|query|integer|false|Number of results to return per page.


### Responses

Status|Meaning|Description
---|---|---|
200|[OK](https://tools.ietf.org/html/rfc7231#section-6.3.1)|Get all shipnotices
401|[Unauthorized](https://tools.ietf.org/html/rfc7235#section-3.1)|No description
403|[Forbidden](https://tools.ietf.org/html/rfc7231#section-6.5.3)|No description

> Example responses

```json
{
  "id": 0,
  "customer_id": 0,
  "sender": "string",
  "eta": "2017-06-19T15:15:48Z",
  "status": 0,
  "received_by": "string",
  "notes_by_whiplash": "string",
  "notes_by_customer": "string",
  "total_boxes": 0,
  "created_at": "2017-06-19T15:15:48Z",
  "updated_at": "2017-06-19T15:15:48Z",
  "warehouse_id": 0,
  "arrived_at": "2017-06-19T15:15:48Z",
  "skip_images": true,
  "shipment_id": "string",
  "shipping_label_url": "string",
  "ship_actual_cost": 0,
  "ship_method": "string",
  "tracking": "string",
  "order_id": 0,
  "type": "string",
  "postage_billed": true,
  "handling_billed": true,
  "pick_fee_actual": 0,
  "pack_fee_actual": 0,
  "total_fee_actual": 0,
  "ship_3rdparty_cost": 0,
  "requires_label": true,
  "completed_at": "2017-06-19T15:15:48Z",
  "ship_actual_currency": "string",
  "delivered_at": "2017-06-19T15:15:48Z",
  "due_at": "2017-06-19T15:15:48Z"
}
```
```json
{
  "message": "string"
}
```
```json
{
  "message": "string"
}
```
<aside class="success">
This operation does not require authentication
</aside>

## postApiV2Shipnotices

> Code samples

```shell
# You can also use wget
curl -X post ://staging.whiplashmerch.com/api/v2/shipnotices \
  -H 'X-Customer-Id: string' \
  -H 'Content-Type: application/json' \
  -H 'Accept: application/json'

```

```http
POST ://staging.whiplashmerch.com/api/v2/shipnotices HTTP/1.1
Host: staging.whiplashmerch.com
Content-Type: application/json
Accept: application/json
X-Customer-Id: string

```

```javascript
var headers = {
  'X-Customer-Id':'string',
  'Content-Type':'application/json',
  'Accept':'application/json'

};

$.ajax({
  url: '://staging.whiplashmerch.com/api/v2/shipnotices',
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
  'X-Customer-Id':'string',
  'Content-Type':'application/json',
  'Accept':'application/json'

};

fetch('://staging.whiplashmerch.com/api/v2/shipnotices',
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
  'X-Customer-Id' => 'string',
  'Content-Type' => 'application/json',
  'Accept' => 'application/json'
}

result = RestClient.post '://staging.whiplashmerch.com/api/v2/shipnotices', params: {
  }, headers: headers

p JSON.parse(result)
```

```python
import requests
headers = {
  'X-Customer-Id': 'string',
  'Content-Type': 'application/json',
  'Accept': 'application/json'
}

r = requests.post('://staging.whiplashmerch.com/api/v2/shipnotices', params={

}, headers = headers)

print r.json()
```

```java
URL obj = new URL("://staging.whiplashmerch.com/api/v2/shipnotices");
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

`POST /api/v2/shipnotices`

*Create a shipnotice*

Create a shipnotice

### Parameters

Parameter|In|Type|Required|Description
---|---|---|---|---|
X-Customer-Id|header|string|false|The customer associated with this resource.
id|formData|integer|false|No description
eta|formData|string|false|No description
warehouse_id|formData|integer|false|No description
status|formData|integer|false|status of the shipnotice
received_by|formData|string|false|the name of the person who received the shipnotice
notes_by_whiplash|formData|string|false|notes by whiplash
notes_by_customer|formData|string|false|notes by customer
total_boxes|formData|integer|false|total number of boxes in the shipnotice
arrived_at|formData|string|false|No description
skip_images|formData|boolean|false|allow skipping of images for this shipnotice?
shipment_id|formData|string|false|the ID of the shipment
shipping_label_url|formData|string|false|url of the shipping label
ship_actual_cost|formData|number|false|No description
ship_method|formData|string|false|the method of shipping for the shipnotice
tracking|formData|string|false|the tracking number of the shipnotice
order_id|formData|integer|false|the order_id of the shipnotice
type|formData|string|false|shipnotice type
postage_billed|formData|boolean|false|was postage billed?
handling_billed|formData|boolean|false|was handling billed?
pick_fee_actual|formData|number|false|No description
pack_fee_actual|formData|number|false|No description
total_fee_actual|formData|number|false|No description
ship_3rdparty_cost|formData|number|false|3rd party cost for the shipnotice
requires_label|formData|boolean|false|does this shipnotice require a label?
completed_at|formData|string|false|No description
ship_actual_currency|formData|string|false|currency used for this shipnotice
delivered_at|formData|string|false|date when was the shipnoticed delivered
due_at|formData|string|false|date when the shipnotice is due to be delivered


### Responses

Status|Meaning|Description
---|---|---|
201|[Created](https://tools.ietf.org/html/rfc7231#section-6.3.2)|Create a shipnotice
401|[Unauthorized](https://tools.ietf.org/html/rfc7235#section-3.1)|No description
403|[Forbidden](https://tools.ietf.org/html/rfc7231#section-6.5.3)|No description
409|[Conflict](https://tools.ietf.org/html/rfc7231#section-6.5.8)|No description
422|[Unprocessable Entity](https://tools.ietf.org/html/rfc2518#section-10.3)|No description

> Example responses

```json
{
  "id": 0,
  "customer_id": 0,
  "sender": "string",
  "eta": "2017-06-19T15:15:48Z",
  "status": 0,
  "received_by": "string",
  "notes_by_whiplash": "string",
  "notes_by_customer": "string",
  "total_boxes": 0,
  "created_at": "2017-06-19T15:15:48Z",
  "updated_at": "2017-06-19T15:15:48Z",
  "warehouse_id": 0,
  "arrived_at": "2017-06-19T15:15:48Z",
  "skip_images": true,
  "shipment_id": "string",
  "shipping_label_url": "string",
  "ship_actual_cost": 0,
  "ship_method": "string",
  "tracking": "string",
  "order_id": 0,
  "type": "string",
  "postage_billed": true,
  "handling_billed": true,
  "pick_fee_actual": 0,
  "pack_fee_actual": 0,
  "total_fee_actual": 0,
  "ship_3rdparty_cost": 0,
  "requires_label": true,
  "completed_at": "2017-06-19T15:15:48Z",
  "ship_actual_currency": "string",
  "delivered_at": "2017-06-19T15:15:48Z",
  "due_at": "2017-06-19T15:15:48Z"
}
```
```json
{
  "message": "string"
}
```
```json
{
  "message": "string"
}
```
```json
{
  "message": "string"
}
```
```json
{
  "message": "string"
}
```
<aside class="success">
This operation does not require authentication
</aside>

## getApiV2ShipnoticesCount

> Code samples

```shell
# You can also use wget
curl -X get ://staging.whiplashmerch.com/api/v2/shipnotices/count \
  -H 'X-Customer-Id: string' \
  -H 'Accept: application/json'

```

```http
GET ://staging.whiplashmerch.com/api/v2/shipnotices/count HTTP/1.1
Host: staging.whiplashmerch.com

Accept: application/json
X-Customer-Id: string

```

```javascript
var headers = {
  'X-Customer-Id':'string',
  'Accept':'application/json'

};

$.ajax({
  url: '://staging.whiplashmerch.com/api/v2/shipnotices/count',
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
  'X-Customer-Id':'string',
  'Accept':'application/json'

};

fetch('://staging.whiplashmerch.com/api/v2/shipnotices/count',
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
  'X-Customer-Id' => 'string',
  'Accept' => 'application/json'
}

result = RestClient.get '://staging.whiplashmerch.com/api/v2/shipnotices/count', params: {
  }, headers: headers

p JSON.parse(result)
```

```python
import requests
headers = {
  'X-Customer-Id': 'string',
  'Accept': 'application/json'
}

r = requests.get('://staging.whiplashmerch.com/api/v2/shipnotices/count', params={

}, headers = headers)

print r.json()
```

```java
URL obj = new URL("://staging.whiplashmerch.com/api/v2/shipnotices/count");
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

`GET /api/v2/shipnotices/count`

*Returns count of shipnotices*

Returns count of shipnotices

### Parameters

Parameter|In|Type|Required|Description
---|---|---|---|---|
X-Customer-Id|header|string|false|The customer associated with this resource.
search|query|string|false|JSON search string like {"attribute_eq": "Term"}


### Responses

Status|Meaning|Description
---|---|---|
200|[OK](https://tools.ietf.org/html/rfc7231#section-6.3.1)|Returns count of shipnotices
401|[Unauthorized](https://tools.ietf.org/html/rfc7235#section-3.1)|No description
403|[Forbidden](https://tools.ietf.org/html/rfc7231#section-6.5.3)|No description

> Example responses

```json
{
  "id": 0,
  "customer_id": 0,
  "sender": "string",
  "eta": "2017-06-19T15:15:48Z",
  "status": 0,
  "received_by": "string",
  "notes_by_whiplash": "string",
  "notes_by_customer": "string",
  "total_boxes": 0,
  "created_at": "2017-06-19T15:15:48Z",
  "updated_at": "2017-06-19T15:15:48Z",
  "warehouse_id": 0,
  "arrived_at": "2017-06-19T15:15:48Z",
  "skip_images": true,
  "shipment_id": "string",
  "shipping_label_url": "string",
  "ship_actual_cost": 0,
  "ship_method": "string",
  "tracking": "string",
  "order_id": 0,
  "type": "string",
  "postage_billed": true,
  "handling_billed": true,
  "pick_fee_actual": 0,
  "pack_fee_actual": 0,
  "total_fee_actual": 0,
  "ship_3rdparty_cost": 0,
  "requires_label": true,
  "completed_at": "2017-06-19T15:15:48Z",
  "ship_actual_currency": "string",
  "delivered_at": "2017-06-19T15:15:48Z",
  "due_at": "2017-06-19T15:15:48Z"
}
```
```json
{
  "message": "string"
}
```
```json
{
  "message": "string"
}
```
<aside class="success">
This operation does not require authentication
</aside>

## getApiV2ShipnoticesId

> Code samples

```shell
# You can also use wget
curl -X get ://staging.whiplashmerch.com/api/v2/shipnotices/{id} \
  -H 'X-Customer-Id: string' \
  -H 'Accept: application/json'

```

```http
GET ://staging.whiplashmerch.com/api/v2/shipnotices/{id} HTTP/1.1
Host: staging.whiplashmerch.com

Accept: application/json
X-Customer-Id: string

```

```javascript
var headers = {
  'X-Customer-Id':'string',
  'Accept':'application/json'

};

$.ajax({
  url: '://staging.whiplashmerch.com/api/v2/shipnotices/{id}',
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
  'X-Customer-Id':'string',
  'Accept':'application/json'

};

fetch('://staging.whiplashmerch.com/api/v2/shipnotices/{id}',
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
  'X-Customer-Id' => 'string',
  'Accept' => 'application/json'
}

result = RestClient.get '://staging.whiplashmerch.com/api/v2/shipnotices/{id}', params: {
  }, headers: headers

p JSON.parse(result)
```

```python
import requests
headers = {
  'X-Customer-Id': 'string',
  'Accept': 'application/json'
}

r = requests.get('://staging.whiplashmerch.com/api/v2/shipnotices/{id}', params={

}, headers = headers)

print r.json()
```

```java
URL obj = new URL("://staging.whiplashmerch.com/api/v2/shipnotices/{id}");
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

`GET /api/v2/shipnotices/{id}`

*Get a Shipnotice*

Get a Shipnotice

### Parameters

Parameter|In|Type|Required|Description
---|---|---|---|---|
id|path|integer|true|No description
X-Customer-Id|header|string|false|The customer associated with this resource.


### Responses

Status|Meaning|Description
---|---|---|
200|[OK](https://tools.ietf.org/html/rfc7231#section-6.3.1)|Get a Shipnotice
401|[Unauthorized](https://tools.ietf.org/html/rfc7235#section-3.1)|No description
403|[Forbidden](https://tools.ietf.org/html/rfc7231#section-6.5.3)|No description

> Example responses

```json
{
  "id": 0,
  "customer_id": 0,
  "sender": "string",
  "eta": "2017-06-19T15:15:48Z",
  "status": 0,
  "received_by": "string",
  "notes_by_whiplash": "string",
  "notes_by_customer": "string",
  "total_boxes": 0,
  "created_at": "2017-06-19T15:15:48Z",
  "updated_at": "2017-06-19T15:15:48Z",
  "warehouse_id": 0,
  "arrived_at": "2017-06-19T15:15:48Z",
  "skip_images": true,
  "shipment_id": "string",
  "shipping_label_url": "string",
  "ship_actual_cost": 0,
  "ship_method": "string",
  "tracking": "string",
  "order_id": 0,
  "type": "string",
  "postage_billed": true,
  "handling_billed": true,
  "pick_fee_actual": 0,
  "pack_fee_actual": 0,
  "total_fee_actual": 0,
  "ship_3rdparty_cost": 0,
  "requires_label": true,
  "completed_at": "2017-06-19T15:15:48Z",
  "ship_actual_currency": "string",
  "delivered_at": "2017-06-19T15:15:48Z",
  "due_at": "2017-06-19T15:15:48Z"
}
```
```json
{
  "message": "string"
}
```
```json
{
  "message": "string"
}
```
<aside class="success">
This operation does not require authentication
</aside>

## putApiV2ShipnoticesId

> Code samples

```shell
# You can also use wget
curl -X put ://staging.whiplashmerch.com/api/v2/shipnotices/{id} \
  -H 'X-Customer-Id: string' \
  -H 'Content-Type: application/json' \
  -H 'Accept: application/json'

```

```http
PUT ://staging.whiplashmerch.com/api/v2/shipnotices/{id} HTTP/1.1
Host: staging.whiplashmerch.com
Content-Type: application/json
Accept: application/json
X-Customer-Id: string

```

```javascript
var headers = {
  'X-Customer-Id':'string',
  'Content-Type':'application/json',
  'Accept':'application/json'

};

$.ajax({
  url: '://staging.whiplashmerch.com/api/v2/shipnotices/{id}',
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
  'X-Customer-Id':'string',
  'Content-Type':'application/json',
  'Accept':'application/json'

};

fetch('://staging.whiplashmerch.com/api/v2/shipnotices/{id}',
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
  'X-Customer-Id' => 'string',
  'Content-Type' => 'application/json',
  'Accept' => 'application/json'
}

result = RestClient.put '://staging.whiplashmerch.com/api/v2/shipnotices/{id}', params: {
  }, headers: headers

p JSON.parse(result)
```

```python
import requests
headers = {
  'X-Customer-Id': 'string',
  'Content-Type': 'application/json',
  'Accept': 'application/json'
}

r = requests.put('://staging.whiplashmerch.com/api/v2/shipnotices/{id}', params={

}, headers = headers)

print r.json()
```

```java
URL obj = new URL("://staging.whiplashmerch.com/api/v2/shipnotices/{id}");
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

`PUT /api/v2/shipnotices/{id}`

*Update a shipnotice*

Update a shipnotice

### Parameters

Parameter|In|Type|Required|Description
---|---|---|---|---|
X-Customer-Id|header|string|false|The customer associated with this resource.
customer_id|formData|integer|false|No description
sender|formData|string|false|No description
eta|formData|string|false|No description
status|formData|integer|false|status of the shipnotice
received_by|formData|string|false|the name of the person who received the shipnotice
notes_by_whiplash|formData|string|false|notes by whiplash
notes_by_customer|formData|string|false|notes by customer
total_boxes|formData|integer|false|total number of boxes in the shipnotice
warehouse_id|formData|integer|false|No description
arrived_at|formData|string|false|No description
skip_images|formData|boolean|false|allow skipping of images for this shipnotice?
shipment_id|formData|string|false|the ID of the shipment
shipping_label_url|formData|string|false|url of the shipping label
ship_actual_cost|formData|number|false|No description
ship_method|formData|string|false|the method of shipping for the shipnotice
tracking|formData|string|false|the tracking number of the shipnotice
order_id|formData|integer|false|the order_id of the shipnotice
type|formData|string|false|shipnotice type
postage_billed|formData|boolean|false|was postage billed?
handling_billed|formData|boolean|false|was handling billed?
pick_fee_actual|formData|number|false|No description
pack_fee_actual|formData|number|false|No description
total_fee_actual|formData|number|false|No description
ship_3rdparty_cost|formData|number|false|3rd party cost for the shipnotice
requires_label|formData|boolean|false|does this shipnotice require a label?
completed_at|formData|string|false|No description
ship_actual_currency|formData|string|false|currency used for this shipnotice
delivered_at|formData|string|false|date when was the shipnoticed delivered
due_at|formData|string|false|date when the shipnotice is due to be delivered
id|path|integer|true|No description


### Responses

Status|Meaning|Description
---|---|---|
200|[OK](https://tools.ietf.org/html/rfc7231#section-6.3.1)|Update a shipnotice
401|[Unauthorized](https://tools.ietf.org/html/rfc7235#section-3.1)|No description
403|[Forbidden](https://tools.ietf.org/html/rfc7231#section-6.5.3)|No description
422|[Unprocessable Entity](https://tools.ietf.org/html/rfc2518#section-10.3)|No description

> Example responses

```json
{
  "id": 0,
  "customer_id": 0,
  "sender": "string",
  "eta": "2017-06-19T15:15:48Z",
  "status": 0,
  "received_by": "string",
  "notes_by_whiplash": "string",
  "notes_by_customer": "string",
  "total_boxes": 0,
  "created_at": "2017-06-19T15:15:48Z",
  "updated_at": "2017-06-19T15:15:48Z",
  "warehouse_id": 0,
  "arrived_at": "2017-06-19T15:15:48Z",
  "skip_images": true,
  "shipment_id": "string",
  "shipping_label_url": "string",
  "ship_actual_cost": 0,
  "ship_method": "string",
  "tracking": "string",
  "order_id": 0,
  "type": "string",
  "postage_billed": true,
  "handling_billed": true,
  "pick_fee_actual": 0,
  "pack_fee_actual": 0,
  "total_fee_actual": 0,
  "ship_3rdparty_cost": 0,
  "requires_label": true,
  "completed_at": "2017-06-19T15:15:48Z",
  "ship_actual_currency": "string",
  "delivered_at": "2017-06-19T15:15:48Z",
  "due_at": "2017-06-19T15:15:48Z"
}
```
```json
{
  "message": "string"
}
```
```json
{
  "message": "string"
}
```
```json
{
  "message": "string"
}
```
<aside class="success">
This operation does not require authentication
</aside>

## deleteApiV2ShipnoticesId

> Code samples

```shell
# You can also use wget
curl -X delete ://staging.whiplashmerch.com/api/v2/shipnotices/{id} \
  -H 'X-Customer-Id: string' \
  -H 'Accept: application/json'

```

```http
DELETE ://staging.whiplashmerch.com/api/v2/shipnotices/{id} HTTP/1.1
Host: staging.whiplashmerch.com

Accept: application/json
X-Customer-Id: string

```

```javascript
var headers = {
  'X-Customer-Id':'string',
  'Accept':'application/json'

};

$.ajax({
  url: '://staging.whiplashmerch.com/api/v2/shipnotices/{id}',
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
  'X-Customer-Id':'string',
  'Accept':'application/json'

};

fetch('://staging.whiplashmerch.com/api/v2/shipnotices/{id}',
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
  'X-Customer-Id' => 'string',
  'Accept' => 'application/json'
}

result = RestClient.delete '://staging.whiplashmerch.com/api/v2/shipnotices/{id}', params: {
  }, headers: headers

p JSON.parse(result)
```

```python
import requests
headers = {
  'X-Customer-Id': 'string',
  'Accept': 'application/json'
}

r = requests.delete('://staging.whiplashmerch.com/api/v2/shipnotices/{id}', params={

}, headers = headers)

print r.json()
```

```java
URL obj = new URL("://staging.whiplashmerch.com/api/v2/shipnotices/{id}");
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

`DELETE /api/v2/shipnotices/{id}`

*Destroy a shipnotice*

Destroy a shipnotice

### Parameters

Parameter|In|Type|Required|Description
---|---|---|---|---|
id|path|integer|true|No description
X-Customer-Id|header|string|false|The customer associated with this resource.


### Responses

Status|Meaning|Description
---|---|---|
200|[OK](https://tools.ietf.org/html/rfc7231#section-6.3.1)|Destroy a shipnotice
401|[Unauthorized](https://tools.ietf.org/html/rfc7235#section-3.1)|No description
403|[Forbidden](https://tools.ietf.org/html/rfc7231#section-6.5.3)|No description
422|[Unprocessable Entity](https://tools.ietf.org/html/rfc2518#section-10.3)|No description

> Example responses

```json
{
  "id": 0,
  "customer_id": 0,
  "sender": "string",
  "eta": "2017-06-19T15:15:48Z",
  "status": 0,
  "received_by": "string",
  "notes_by_whiplash": "string",
  "notes_by_customer": "string",
  "total_boxes": 0,
  "created_at": "2017-06-19T15:15:48Z",
  "updated_at": "2017-06-19T15:15:48Z",
  "warehouse_id": 0,
  "arrived_at": "2017-06-19T15:15:48Z",
  "skip_images": true,
  "shipment_id": "string",
  "shipping_label_url": "string",
  "ship_actual_cost": 0,
  "ship_method": "string",
  "tracking": "string",
  "order_id": 0,
  "type": "string",
  "postage_billed": true,
  "handling_billed": true,
  "pick_fee_actual": 0,
  "pack_fee_actual": 0,
  "total_fee_actual": 0,
  "ship_3rdparty_cost": 0,
  "requires_label": true,
  "completed_at": "2017-06-19T15:15:48Z",
  "ship_actual_currency": "string",
  "delivered_at": "2017-06-19T15:15:48Z",
  "due_at": "2017-06-19T15:15:48Z"
}
```
```json
{
  "message": "string"
}
```
```json
{
  "message": "string"
}
```
```json
{
  "message": "string"
}
```
<aside class="success">
This operation does not require authentication
</aside>

## getApiV2ShipnoticesIdShipnoticeItems

> Code samples

```shell
# You can also use wget
curl -X get ://staging.whiplashmerch.com/api/v2/shipnotices/{id}/shipnotice_items \
  -H 'X-Customer-Id: string' \
  -H 'Accept: application/json'

```

```http
GET ://staging.whiplashmerch.com/api/v2/shipnotices/{id}/shipnotice_items HTTP/1.1
Host: staging.whiplashmerch.com

Accept: application/json
X-Customer-Id: string

```

```javascript
var headers = {
  'X-Customer-Id':'string',
  'Accept':'application/json'

};

$.ajax({
  url: '://staging.whiplashmerch.com/api/v2/shipnotices/{id}/shipnotice_items',
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
  'X-Customer-Id':'string',
  'Accept':'application/json'

};

fetch('://staging.whiplashmerch.com/api/v2/shipnotices/{id}/shipnotice_items',
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
  'X-Customer-Id' => 'string',
  'Accept' => 'application/json'
}

result = RestClient.get '://staging.whiplashmerch.com/api/v2/shipnotices/{id}/shipnotice_items', params: {
  }, headers: headers

p JSON.parse(result)
```

```python
import requests
headers = {
  'X-Customer-Id': 'string',
  'Accept': 'application/json'
}

r = requests.get('://staging.whiplashmerch.com/api/v2/shipnotices/{id}/shipnotice_items', params={

}, headers = headers)

print r.json()
```

```java
URL obj = new URL("://staging.whiplashmerch.com/api/v2/shipnotices/{id}/shipnotice_items");
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

`GET /api/v2/shipnotices/{id}/shipnotice_items`

*Get a count of shipnotice items for shipnotice*

Get a count of shipnotice items for shipnotice

### Parameters

Parameter|In|Type|Required|Description
---|---|---|---|---|
X-Customer-Id|header|string|false|The customer associated with this resource.
search|query|string|false|JSON search string like {"attribute_eq": "Term"}
id|path|integer|true|No description


### Responses

Status|Meaning|Description
---|---|---|
200|[OK](https://tools.ietf.org/html/rfc7231#section-6.3.1)|Get a count of shipnotice items for shipnotice
401|[Unauthorized](https://tools.ietf.org/html/rfc7235#section-3.1)|No description
403|[Forbidden](https://tools.ietf.org/html/rfc7231#section-6.5.3)|No description

> Example responses

```json
{
  "id": 0,
  "shipnotice_id": 0,
  "item_id": 0,
  "quantity": 0,
  "quantity_good": 0,
  "quantity_damaged": 0,
  "created_at": "2017-06-19T15:15:48Z",
  "updated_at": "2017-06-19T15:15:48Z",
  "available": true,
  "description": "string",
  "extended_description": "string",
  "include_in_published": true,
  "weight": 0,
  "scancode": "string",
  "length": 0,
  "width": 0,
  "height": 0,
  "media_mail": true,
  "return_action": "string",
  "wholesale_fee": 0,
  "retail_fee": 0
}
```
```json
{
  "message": "string"
}
```
```json
{
  "message": "string"
}
```
<aside class="success">
This operation does not require authentication
</aside>

## postApiV2ShipnoticesIdShipnoticeItems

> Code samples

```shell
# You can also use wget
curl -X post ://staging.whiplashmerch.com/api/v2/shipnotices/{id}/shipnotice_items \
  -H 'X-Customer-Id: string' \
  -H 'Content-Type: application/json' \
  -H 'Accept: application/json'

```

```http
POST ://staging.whiplashmerch.com/api/v2/shipnotices/{id}/shipnotice_items HTTP/1.1
Host: staging.whiplashmerch.com
Content-Type: application/json
Accept: application/json
X-Customer-Id: string

```

```javascript
var headers = {
  'X-Customer-Id':'string',
  'Content-Type':'application/json',
  'Accept':'application/json'

};

$.ajax({
  url: '://staging.whiplashmerch.com/api/v2/shipnotices/{id}/shipnotice_items',
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
  'X-Customer-Id':'string',
  'Content-Type':'application/json',
  'Accept':'application/json'

};

fetch('://staging.whiplashmerch.com/api/v2/shipnotices/{id}/shipnotice_items',
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
  'X-Customer-Id' => 'string',
  'Content-Type' => 'application/json',
  'Accept' => 'application/json'
}

result = RestClient.post '://staging.whiplashmerch.com/api/v2/shipnotices/{id}/shipnotice_items', params: {
  }, headers: headers

p JSON.parse(result)
```

```python
import requests
headers = {
  'X-Customer-Id': 'string',
  'Content-Type': 'application/json',
  'Accept': 'application/json'
}

r = requests.post('://staging.whiplashmerch.com/api/v2/shipnotices/{id}/shipnotice_items', params={

}, headers = headers)

print r.json()
```

```java
URL obj = new URL("://staging.whiplashmerch.com/api/v2/shipnotices/{id}/shipnotice_items");
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

`POST /api/v2/shipnotices/{id}/shipnotice_items`

*create a shipnotice item*

create a shipnotice item

### Parameters

Parameter|In|Type|Required|Description
---|---|---|---|---|
X-Customer-Id|header|string|false|The customer associated with this resource.
quantity|formData|integer|false|No description
item_id|formData|integer|false|No description
description|formData|string|false|description of the item
extended_description|formData|string|false|an extended description of the item
include_in_published|formData|boolean|false|include this item in published amount?
id|path|integer|true|No description


### Responses

Status|Meaning|Description
---|---|---|
201|[Created](https://tools.ietf.org/html/rfc7231#section-6.3.2)|create a shipnotice item
401|[Unauthorized](https://tools.ietf.org/html/rfc7235#section-3.1)|No description
403|[Forbidden](https://tools.ietf.org/html/rfc7231#section-6.5.3)|No description
409|[Conflict](https://tools.ietf.org/html/rfc7231#section-6.5.8)|No description
422|[Unprocessable Entity](https://tools.ietf.org/html/rfc2518#section-10.3)|No description

> Example responses

```json
{
  "id": 0,
  "shipnotice_id": 0,
  "item_id": 0,
  "quantity": 0,
  "quantity_good": 0,
  "quantity_damaged": 0,
  "created_at": "2017-06-19T15:15:48Z",
  "updated_at": "2017-06-19T15:15:48Z",
  "available": true,
  "description": "string",
  "extended_description": "string",
  "include_in_published": true,
  "weight": 0,
  "scancode": "string",
  "length": 0,
  "width": 0,
  "height": 0,
  "media_mail": true,
  "return_action": "string",
  "wholesale_fee": 0,
  "retail_fee": 0
}
```
```json
{
  "message": "string"
}
```
```json
{
  "message": "string"
}
```
```json
{
  "message": "string"
}
```
```json
{
  "message": "string"
}
```
<aside class="success">
This operation does not require authentication
</aside>

## getApiV2ShipnoticesIdMessages

> Code samples

```shell
# You can also use wget
curl -X get ://staging.whiplashmerch.com/api/v2/shipnotices/{id}/messages \
  -H 'Accept: application/json'

```

```http
GET ://staging.whiplashmerch.com/api/v2/shipnotices/{id}/messages HTTP/1.1
Host: staging.whiplashmerch.com

Accept: application/json

```

```javascript
var headers = {
  'Accept':'application/json'

};

$.ajax({
  url: '://staging.whiplashmerch.com/api/v2/shipnotices/{id}/messages',
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
  'Accept':'application/json'

};

fetch('://staging.whiplashmerch.com/api/v2/shipnotices/{id}/messages',
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
  'Accept' => 'application/json'
}

result = RestClient.get '://staging.whiplashmerch.com/api/v2/shipnotices/{id}/messages', params: {
  }, headers: headers

p JSON.parse(result)
```

```python
import requests
headers = {
  'Accept': 'application/json'
}

r = requests.get('://staging.whiplashmerch.com/api/v2/shipnotices/{id}/messages', params={

}, headers = headers)

print r.json()
```

```java
URL obj = new URL("://staging.whiplashmerch.com/api/v2/shipnotices/{id}/messages");
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

`GET /api/v2/shipnotices/{id}/messages`

*Get all messages for a(n) Shipnotice*

Get all messages for a(n) Shipnotice

### Parameters

Parameter|In|Type|Required|Description
---|---|---|---|---|
search|query|string|false|JSON search string like {"attribute_eq": "Term"}
page|query|integer|false|Page of results to fetch.
per_page|query|integer|false|Number of results to return per page.
id|path|integer|true|No description


### Responses

Status|Meaning|Description
---|---|---|
200|[OK](https://tools.ietf.org/html/rfc7231#section-6.3.1)|Get all messages for a(n) Shipnotice
401|[Unauthorized](https://tools.ietf.org/html/rfc7235#section-3.1)|No description
403|[Forbidden](https://tools.ietf.org/html/rfc7231#section-6.5.3)|No description

> Example responses

```json
{
  "id": 0,
  "customer_id": 0,
  "to": "string",
  "from": "string",
  "subject": "string",
  "content": "string",
  "contextuable_id": 0,
  "contextuable_type": "string",
  "created_at": "2017-06-19T15:15:48Z",
  "updated_at": "2017-06-19T15:15:48Z"
}
```
```json
{
  "message": "string"
}
```
```json
{
  "message": "string"
}
```
<aside class="success">
This operation does not require authentication
</aside>

## postApiV2ShipnoticesIdMessages

> Code samples

```shell
# You can also use wget
curl -X post ://staging.whiplashmerch.com/api/v2/shipnotices/{id}/messages \
  -H 'X-Customer-Id: string' \
  -H 'Content-Type: application/json' \
  -H 'Accept: application/json'

```

```http
POST ://staging.whiplashmerch.com/api/v2/shipnotices/{id}/messages HTTP/1.1
Host: staging.whiplashmerch.com
Content-Type: application/json
Accept: application/json
X-Customer-Id: string

```

```javascript
var headers = {
  'X-Customer-Id':'string',
  'Content-Type':'application/json',
  'Accept':'application/json'

};

$.ajax({
  url: '://staging.whiplashmerch.com/api/v2/shipnotices/{id}/messages',
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
  'X-Customer-Id':'string',
  'Content-Type':'application/json',
  'Accept':'application/json'

};

fetch('://staging.whiplashmerch.com/api/v2/shipnotices/{id}/messages',
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
  'X-Customer-Id' => 'string',
  'Content-Type' => 'application/json',
  'Accept' => 'application/json'
}

result = RestClient.post '://staging.whiplashmerch.com/api/v2/shipnotices/{id}/messages', params: {
  }, headers: headers

p JSON.parse(result)
```

```python
import requests
headers = {
  'X-Customer-Id': 'string',
  'Content-Type': 'application/json',
  'Accept': 'application/json'
}

r = requests.post('://staging.whiplashmerch.com/api/v2/shipnotices/{id}/messages', params={

}, headers = headers)

print r.json()
```

```java
URL obj = new URL("://staging.whiplashmerch.com/api/v2/shipnotices/{id}/messages");
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

`POST /api/v2/shipnotices/{id}/messages`

*Create a messages for a(n) Shipnotice*

Create a messages for a(n) Shipnotice

### Parameters

Parameter|In|Type|Required|Description
---|---|---|---|---|
X-Customer-Id|header|string|false|The customer associated with this resource.
to|formData|string|true|No description
from|formData|string|true|No description
subject|formData|string|true|No description
content|formData|string|true|No description
id|path|integer|true|No description


### Responses

Status|Meaning|Description
---|---|---|
201|[Created](https://tools.ietf.org/html/rfc7231#section-6.3.2)|Create a messages for a(n) Shipnotice
401|[Unauthorized](https://tools.ietf.org/html/rfc7235#section-3.1)|No description
403|[Forbidden](https://tools.ietf.org/html/rfc7231#section-6.5.3)|No description
409|[Conflict](https://tools.ietf.org/html/rfc7231#section-6.5.8)|No description
422|[Unprocessable Entity](https://tools.ietf.org/html/rfc2518#section-10.3)|No description

> Example responses

```json
{
  "id": 0,
  "customer_id": 0,
  "to": "string",
  "from": "string",
  "subject": "string",
  "content": "string",
  "contextuable_id": 0,
  "contextuable_type": "string",
  "created_at": "2017-06-19T15:15:48Z",
  "updated_at": "2017-06-19T15:15:48Z"
}
```
```json
{
  "message": "string"
}
```
```json
{
  "message": "string"
}
```
```json
{
  "message": "string"
}
```
```json
{
  "message": "string"
}
```
<aside class="success">
This operation does not require authentication
</aside>

## getApiV2ShipnoticesIdMessagesCount

> Code samples

```shell
# You can also use wget
curl -X get ://staging.whiplashmerch.com/api/v2/shipnotices/{id}/messages/count \
  -H 'Accept: application/json'

```

```http
GET ://staging.whiplashmerch.com/api/v2/shipnotices/{id}/messages/count HTTP/1.1
Host: staging.whiplashmerch.com

Accept: application/json

```

```javascript
var headers = {
  'Accept':'application/json'

};

$.ajax({
  url: '://staging.whiplashmerch.com/api/v2/shipnotices/{id}/messages/count',
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
  'Accept':'application/json'

};

fetch('://staging.whiplashmerch.com/api/v2/shipnotices/{id}/messages/count',
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
  'Accept' => 'application/json'
}

result = RestClient.get '://staging.whiplashmerch.com/api/v2/shipnotices/{id}/messages/count', params: {
  }, headers: headers

p JSON.parse(result)
```

```python
import requests
headers = {
  'Accept': 'application/json'
}

r = requests.get('://staging.whiplashmerch.com/api/v2/shipnotices/{id}/messages/count', params={

}, headers = headers)

print r.json()
```

```java
URL obj = new URL("://staging.whiplashmerch.com/api/v2/shipnotices/{id}/messages/count");
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

`GET /api/v2/shipnotices/{id}/messages/count`

*Returns count of messages for a(n) Shipnotice*

Returns count of messages for a(n) Shipnotice

### Parameters

Parameter|In|Type|Required|Description
---|---|---|---|---|
search|query|string|false|JSON search string like {"attribute_eq": "Term"}
id|path|integer|true|No description


### Responses

Status|Meaning|Description
---|---|---|
200|[OK](https://tools.ietf.org/html/rfc7231#section-6.3.1)|Returns count of messages for a(n) Shipnotice
401|[Unauthorized](https://tools.ietf.org/html/rfc7235#section-3.1)|No description
403|[Forbidden](https://tools.ietf.org/html/rfc7231#section-6.5.3)|No description

> Example responses

```json
{
  "id": 0,
  "customer_id": 0,
  "to": "string",
  "from": "string",
  "subject": "string",
  "content": "string",
  "contextuable_id": 0,
  "contextuable_type": "string",
  "created_at": "2017-06-19T15:15:48Z",
  "updated_at": "2017-06-19T15:15:48Z"
}
```
```json
{
  "message": "string"
}
```
```json
{
  "message": "string"
}
```
<aside class="success">
This operation does not require authentication
</aside>

# shipnotice_items

Operations about shipnotice_items

## getApiV2ShipnoticeItemsId

> Code samples

```shell
# You can also use wget
curl -X get ://staging.whiplashmerch.com/api/v2/shipnotice_items/{id} \
  -H 'Accept: application/json'

```

```http
GET ://staging.whiplashmerch.com/api/v2/shipnotice_items/{id} HTTP/1.1
Host: staging.whiplashmerch.com

Accept: application/json

```

```javascript
var headers = {
  'Accept':'application/json'

};

$.ajax({
  url: '://staging.whiplashmerch.com/api/v2/shipnotice_items/{id}',
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
  'Accept':'application/json'

};

fetch('://staging.whiplashmerch.com/api/v2/shipnotice_items/{id}',
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
  'Accept' => 'application/json'
}

result = RestClient.get '://staging.whiplashmerch.com/api/v2/shipnotice_items/{id}', params: {
  }, headers: headers

p JSON.parse(result)
```

```python
import requests
headers = {
  'Accept': 'application/json'
}

r = requests.get('://staging.whiplashmerch.com/api/v2/shipnotice_items/{id}', params={

}, headers = headers)

print r.json()
```

```java
URL obj = new URL("://staging.whiplashmerch.com/api/v2/shipnotice_items/{id}");
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

`GET /api/v2/shipnotice_items/{id}`

*Get a shipnotice item*

Get a shipnotice item

### Parameters

Parameter|In|Type|Required|Description
---|---|---|---|---|
id|path|integer|true|No description


### Responses

Status|Meaning|Description
---|---|---|
200|[OK](https://tools.ietf.org/html/rfc7231#section-6.3.1)|Get a shipnotice item
401|[Unauthorized](https://tools.ietf.org/html/rfc7235#section-3.1)|No description
403|[Forbidden](https://tools.ietf.org/html/rfc7231#section-6.5.3)|No description

> Example responses

```json
{
  "id": 0,
  "shipnotice_id": 0,
  "item_id": 0,
  "quantity": 0,
  "quantity_good": 0,
  "quantity_damaged": 0,
  "created_at": "2017-06-19T15:15:48Z",
  "updated_at": "2017-06-19T15:15:48Z",
  "available": true,
  "description": "string",
  "extended_description": "string",
  "include_in_published": true,
  "weight": 0,
  "scancode": "string",
  "length": 0,
  "width": 0,
  "height": 0,
  "media_mail": true,
  "return_action": "string",
  "wholesale_fee": 0,
  "retail_fee": 0
}
```
```json
{
  "message": "string"
}
```
```json
{
  "message": "string"
}
```
<aside class="success">
This operation does not require authentication
</aside>

## putApiV2ShipnoticeItemsId

> Code samples

```shell
# You can also use wget
curl -X put ://staging.whiplashmerch.com/api/v2/shipnotice_items/{id} \
  -H 'Content-Type: application/json' \
  -H 'Accept: application/json'

```

```http
PUT ://staging.whiplashmerch.com/api/v2/shipnotice_items/{id} HTTP/1.1
Host: staging.whiplashmerch.com
Content-Type: application/json
Accept: application/json

```

```javascript
var headers = {
  'Content-Type':'application/json',
  'Accept':'application/json'

};

$.ajax({
  url: '://staging.whiplashmerch.com/api/v2/shipnotice_items/{id}',
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
  'Content-Type':'application/json',
  'Accept':'application/json'

};

fetch('://staging.whiplashmerch.com/api/v2/shipnotice_items/{id}',
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
  'Content-Type' => 'application/json',
  'Accept' => 'application/json'
}

result = RestClient.put '://staging.whiplashmerch.com/api/v2/shipnotice_items/{id}', params: {
  }, headers: headers

p JSON.parse(result)
```

```python
import requests
headers = {
  'Content-Type': 'application/json',
  'Accept': 'application/json'
}

r = requests.put('://staging.whiplashmerch.com/api/v2/shipnotice_items/{id}', params={

}, headers = headers)

print r.json()
```

```java
URL obj = new URL("://staging.whiplashmerch.com/api/v2/shipnotice_items/{id}");
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

`PUT /api/v2/shipnotice_items/{id}`

*Update a shipnotice item*

Update a shipnotice item

### Parameters

Parameter|In|Type|Required|Description
---|---|---|---|---|
quantity|formData|integer|false|No description
item_id|formData|integer|false|No description
description|formData|string|false|description of the item
extended_description|formData|string|false|an extended description of the item
include_in_published|formData|boolean|false|include this item in published amount?
id|path|integer|true|No description


### Responses

Status|Meaning|Description
---|---|---|
200|[OK](https://tools.ietf.org/html/rfc7231#section-6.3.1)|Update a shipnotice item
401|[Unauthorized](https://tools.ietf.org/html/rfc7235#section-3.1)|No description
403|[Forbidden](https://tools.ietf.org/html/rfc7231#section-6.5.3)|No description
422|[Unprocessable Entity](https://tools.ietf.org/html/rfc2518#section-10.3)|No description

> Example responses

```json
{
  "id": 0,
  "shipnotice_id": 0,
  "item_id": 0,
  "quantity": 0,
  "quantity_good": 0,
  "quantity_damaged": 0,
  "created_at": "2017-06-19T15:15:48Z",
  "updated_at": "2017-06-19T15:15:48Z",
  "available": true,
  "description": "string",
  "extended_description": "string",
  "include_in_published": true,
  "weight": 0,
  "scancode": "string",
  "length": 0,
  "width": 0,
  "height": 0,
  "media_mail": true,
  "return_action": "string",
  "wholesale_fee": 0,
  "retail_fee": 0
}
```
```json
{
  "message": "string"
}
```
```json
{
  "message": "string"
}
```
```json
{
  "message": "string"
}
```
<aside class="success">
This operation does not require authentication
</aside>

## deleteApiV2ShipnoticeItemsId

> Code samples

```shell
# You can also use wget
curl -X delete ://staging.whiplashmerch.com/api/v2/shipnotice_items/{id} \
  -H 'Accept: application/json'

```

```http
DELETE ://staging.whiplashmerch.com/api/v2/shipnotice_items/{id} HTTP/1.1
Host: staging.whiplashmerch.com

Accept: application/json

```

```javascript
var headers = {
  'Accept':'application/json'

};

$.ajax({
  url: '://staging.whiplashmerch.com/api/v2/shipnotice_items/{id}',
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
  'Accept':'application/json'

};

fetch('://staging.whiplashmerch.com/api/v2/shipnotice_items/{id}',
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
  'Accept' => 'application/json'
}

result = RestClient.delete '://staging.whiplashmerch.com/api/v2/shipnotice_items/{id}', params: {
  }, headers: headers

p JSON.parse(result)
```

```python
import requests
headers = {
  'Accept': 'application/json'
}

r = requests.delete('://staging.whiplashmerch.com/api/v2/shipnotice_items/{id}', params={

}, headers = headers)

print r.json()
```

```java
URL obj = new URL("://staging.whiplashmerch.com/api/v2/shipnotice_items/{id}");
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

`DELETE /api/v2/shipnotice_items/{id}`

*Destroy a shipnotice*

Destroy a shipnotice

### Parameters

Parameter|In|Type|Required|Description
---|---|---|---|---|
id|path|integer|true|No description


### Responses

Status|Meaning|Description
---|---|---|
200|[OK](https://tools.ietf.org/html/rfc7231#section-6.3.1)|Destroy a shipnotice
401|[Unauthorized](https://tools.ietf.org/html/rfc7235#section-3.1)|No description
403|[Forbidden](https://tools.ietf.org/html/rfc7231#section-6.5.3)|No description
422|[Unprocessable Entity](https://tools.ietf.org/html/rfc2518#section-10.3)|No description

> Example responses

```json
{
  "id": 0,
  "shipnotice_id": 0,
  "item_id": 0,
  "quantity": 0,
  "quantity_good": 0,
  "quantity_damaged": 0,
  "created_at": "2017-06-19T15:15:48Z",
  "updated_at": "2017-06-19T15:15:48Z",
  "available": true,
  "description": "string",
  "extended_description": "string",
  "include_in_published": true,
  "weight": 0,
  "scancode": "string",
  "length": 0,
  "width": 0,
  "height": 0,
  "media_mail": true,
  "return_action": "string",
  "wholesale_fee": 0,
  "retail_fee": 0
}
```
```json
{
  "message": "string"
}
```
```json
{
  "message": "string"
}
```
```json
{
  "message": "string"
}
```
<aside class="success">
This operation does not require authentication
</aside>

# accounts

Operations about accounts

## getApiV2Accounts

> Code samples

```shell
# You can also use wget
curl -X get ://staging.whiplashmerch.com/api/v2/accounts \
  -H 'X-Customer-Id: string' \
  -H 'Accept: application/json'

```

```http
GET ://staging.whiplashmerch.com/api/v2/accounts HTTP/1.1
Host: staging.whiplashmerch.com

Accept: application/json
X-Customer-Id: string

```

```javascript
var headers = {
  'X-Customer-Id':'string',
  'Accept':'application/json'

};

$.ajax({
  url: '://staging.whiplashmerch.com/api/v2/accounts',
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
  'X-Customer-Id':'string',
  'Accept':'application/json'

};

fetch('://staging.whiplashmerch.com/api/v2/accounts',
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
  'X-Customer-Id' => 'string',
  'Accept' => 'application/json'
}

result = RestClient.get '://staging.whiplashmerch.com/api/v2/accounts', params: {
  }, headers: headers

p JSON.parse(result)
```

```python
import requests
headers = {
  'X-Customer-Id': 'string',
  'Accept': 'application/json'
}

r = requests.get('://staging.whiplashmerch.com/api/v2/accounts', params={

}, headers = headers)

print r.json()
```

```java
URL obj = new URL("://staging.whiplashmerch.com/api/v2/accounts");
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

`GET /api/v2/accounts`

*Get all accounts*

Get all accounts

### Parameters

Parameter|In|Type|Required|Description
---|---|---|---|---|
X-Customer-Id|header|string|false|The customer associated with this resource.
search|query|string|false|JSON search string like {"attribute_eq": "Term"}
fields|query|string|false|Comma-separated list of fields to include in the response
page|query|integer|false|Page of results to fetch.
per_page|query|integer|false|Number of results to return per page.


### Responses

Status|Meaning|Description
---|---|---|
200|[OK](https://tools.ietf.org/html/rfc7231#section-6.3.1)|Get all accounts
|Unknown|No description

> Example responses

```json
{
  "id": 0,
  "balance": 0,
  "currency": "string",
  "accountable_id": 0,
  "accountable_type": "string",
  "refill_amount": 0,
  "insure_threshold": 0,
  "require_signature_threshold": 0,
  "payment_method_token": "string",
  "created_at": "2017-06-19T15:15:48Z",
  "updated_at": "2017-06-19T15:15:48Z"
}
```
```json
{
  "message": "string"
}
```
<aside class="success">
This operation does not require authentication
</aside>

## postApiV2Accounts

> Code samples

```shell
# You can also use wget
curl -X post ://staging.whiplashmerch.com/api/v2/accounts \
  -H 'X-Customer-Id: string' \
  -H 'Content-Type: application/json' \
  -H 'Accept: application/json'

```

```http
POST ://staging.whiplashmerch.com/api/v2/accounts HTTP/1.1
Host: staging.whiplashmerch.com
Content-Type: application/json
Accept: application/json
X-Customer-Id: string

```

```javascript
var headers = {
  'X-Customer-Id':'string',
  'Content-Type':'application/json',
  'Accept':'application/json'

};

$.ajax({
  url: '://staging.whiplashmerch.com/api/v2/accounts',
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
  'X-Customer-Id':'string',
  'Content-Type':'application/json',
  'Accept':'application/json'

};

fetch('://staging.whiplashmerch.com/api/v2/accounts',
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
  'X-Customer-Id' => 'string',
  'Content-Type' => 'application/json',
  'Accept' => 'application/json'
}

result = RestClient.post '://staging.whiplashmerch.com/api/v2/accounts', params: {
  }, headers: headers

p JSON.parse(result)
```

```python
import requests
headers = {
  'X-Customer-Id': 'string',
  'Content-Type': 'application/json',
  'Accept': 'application/json'
}

r = requests.post('://staging.whiplashmerch.com/api/v2/accounts', params={

}, headers = headers)

print r.json()
```

```java
URL obj = new URL("://staging.whiplashmerch.com/api/v2/accounts");
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

`POST /api/v2/accounts`

*Create an account*

Create an account

### Parameters

Parameter|In|Type|Required|Description
---|---|---|---|---|
X-Customer-Id|header|string|false|The customer associated with this resource.
accountable_id|formData|integer|false|the id of the account parent
accountable_type|formData|string|false|the type of account (Warehouse, Customer, Partner)
currency|formData|string|false|the account currency (USD, GBP, CAD, etc)
balance|formData|number|false|the current account balance
refill_amount|formData|number|false|the account refill amount
insure_threshold|formData|number|false|the account insure threshold
require_signature_threshold|formData|number|false|the account threshold for requiring signature
payment_method_token|formData|string|false|the account payment method token


### Responses

Status|Meaning|Description
---|---|---|
201|[Created](https://tools.ietf.org/html/rfc7231#section-6.3.2)|Create an account
|Unknown|No description

> Example responses

```json
{
  "id": 0,
  "balance": 0,
  "currency": "string",
  "accountable_id": 0,
  "accountable_type": "string",
  "refill_amount": 0,
  "insure_threshold": 0,
  "require_signature_threshold": 0,
  "payment_method_token": "string",
  "created_at": "2017-06-19T15:15:48Z",
  "updated_at": "2017-06-19T15:15:48Z"
}
```
```json
{
  "message": "string"
}
```
<aside class="success">
This operation does not require authentication
</aside>

## getApiV2AccountsId

> Code samples

```shell
# You can also use wget
curl -X get ://staging.whiplashmerch.com/api/v2/accounts/{id} \
  -H 'X-Customer-Id: string' \
  -H 'Accept: application/json'

```

```http
GET ://staging.whiplashmerch.com/api/v2/accounts/{id} HTTP/1.1
Host: staging.whiplashmerch.com

Accept: application/json
X-Customer-Id: string

```

```javascript
var headers = {
  'X-Customer-Id':'string',
  'Accept':'application/json'

};

$.ajax({
  url: '://staging.whiplashmerch.com/api/v2/accounts/{id}',
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
  'X-Customer-Id':'string',
  'Accept':'application/json'

};

fetch('://staging.whiplashmerch.com/api/v2/accounts/{id}',
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
  'X-Customer-Id' => 'string',
  'Accept' => 'application/json'
}

result = RestClient.get '://staging.whiplashmerch.com/api/v2/accounts/{id}', params: {
  }, headers: headers

p JSON.parse(result)
```

```python
import requests
headers = {
  'X-Customer-Id': 'string',
  'Accept': 'application/json'
}

r = requests.get('://staging.whiplashmerch.com/api/v2/accounts/{id}', params={

}, headers = headers)

print r.json()
```

```java
URL obj = new URL("://staging.whiplashmerch.com/api/v2/accounts/{id}");
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

`GET /api/v2/accounts/{id}`

*Get an account*

Get an account

### Parameters

Parameter|In|Type|Required|Description
---|---|---|---|---|
id|path|integer|true|No description
X-Customer-Id|header|string|false|The customer associated with this resource.


### Responses

Status|Meaning|Description
---|---|---|
200|[OK](https://tools.ietf.org/html/rfc7231#section-6.3.1)|Get an account
401|[Unauthorized](https://tools.ietf.org/html/rfc7235#section-3.1)|No description
403|[Forbidden](https://tools.ietf.org/html/rfc7231#section-6.5.3)|No description

> Example responses

```json
{
  "id": 0,
  "balance": 0,
  "currency": "string",
  "accountable_id": 0,
  "accountable_type": "string",
  "refill_amount": 0,
  "insure_threshold": 0,
  "require_signature_threshold": 0,
  "payment_method_token": "string",
  "created_at": "2017-06-19T15:15:48Z",
  "updated_at": "2017-06-19T15:15:48Z"
}
```
```json
{
  "message": "string"
}
```
```json
{
  "message": "string"
}
```
<aside class="success">
This operation does not require authentication
</aside>

## putApiV2AccountsId

> Code samples

```shell
# You can also use wget
curl -X put ://staging.whiplashmerch.com/api/v2/accounts/{id} \
  -H 'X-Customer-Id: string' \
  -H 'Content-Type: application/json' \
  -H 'Accept: application/json'

```

```http
PUT ://staging.whiplashmerch.com/api/v2/accounts/{id} HTTP/1.1
Host: staging.whiplashmerch.com
Content-Type: application/json
Accept: application/json
X-Customer-Id: string

```

```javascript
var headers = {
  'X-Customer-Id':'string',
  'Content-Type':'application/json',
  'Accept':'application/json'

};

$.ajax({
  url: '://staging.whiplashmerch.com/api/v2/accounts/{id}',
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
  'X-Customer-Id':'string',
  'Content-Type':'application/json',
  'Accept':'application/json'

};

fetch('://staging.whiplashmerch.com/api/v2/accounts/{id}',
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
  'X-Customer-Id' => 'string',
  'Content-Type' => 'application/json',
  'Accept' => 'application/json'
}

result = RestClient.put '://staging.whiplashmerch.com/api/v2/accounts/{id}', params: {
  }, headers: headers

p JSON.parse(result)
```

```python
import requests
headers = {
  'X-Customer-Id': 'string',
  'Content-Type': 'application/json',
  'Accept': 'application/json'
}

r = requests.put('://staging.whiplashmerch.com/api/v2/accounts/{id}', params={

}, headers = headers)

print r.json()
```

```java
URL obj = new URL("://staging.whiplashmerch.com/api/v2/accounts/{id}");
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

`PUT /api/v2/accounts/{id}`

*Update an account*

Update an account

### Parameters

Parameter|In|Type|Required|Description
---|---|---|---|---|
X-Customer-Id|header|string|false|The customer associated with this resource.
balance|formData|number|false|the current account balance
currency|formData|string|false|the account currency (USD, GBP, CAD, etc)
accountable_id|formData|integer|false|the id of the account parent
accountable_type|formData|string|false|the type of account (Warehouse, Customer, Partner)
refill_amount|formData|number|false|the account refill amount
insure_threshold|formData|number|false|the account insure threshold
require_signature_threshold|formData|number|false|the account threshold for requiring signature
payment_method_token|formData|string|false|the account payment method token
id|path|integer|true|No description


### Responses

Status|Meaning|Description
---|---|---|
200|[OK](https://tools.ietf.org/html/rfc7231#section-6.3.1)|Update an account
|Unknown|No description

> Example responses

```json
{
  "id": 0,
  "balance": 0,
  "currency": "string",
  "accountable_id": 0,
  "accountable_type": "string",
  "refill_amount": 0,
  "insure_threshold": 0,
  "require_signature_threshold": 0,
  "payment_method_token": "string",
  "created_at": "2017-06-19T15:15:48Z",
  "updated_at": "2017-06-19T15:15:48Z"
}
```
```json
{
  "message": "string"
}
```
<aside class="success">
This operation does not require authentication
</aside>

## deleteApiV2AccountsId

> Code samples

```shell
# You can also use wget
curl -X delete ://staging.whiplashmerch.com/api/v2/accounts/{id} \
  -H 'X-Customer-Id: string' \
  -H 'Accept: application/json'

```

```http
DELETE ://staging.whiplashmerch.com/api/v2/accounts/{id} HTTP/1.1
Host: staging.whiplashmerch.com

Accept: application/json
X-Customer-Id: string

```

```javascript
var headers = {
  'X-Customer-Id':'string',
  'Accept':'application/json'

};

$.ajax({
  url: '://staging.whiplashmerch.com/api/v2/accounts/{id}',
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
  'X-Customer-Id':'string',
  'Accept':'application/json'

};

fetch('://staging.whiplashmerch.com/api/v2/accounts/{id}',
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
  'X-Customer-Id' => 'string',
  'Accept' => 'application/json'
}

result = RestClient.delete '://staging.whiplashmerch.com/api/v2/accounts/{id}', params: {
  }, headers: headers

p JSON.parse(result)
```

```python
import requests
headers = {
  'X-Customer-Id': 'string',
  'Accept': 'application/json'
}

r = requests.delete('://staging.whiplashmerch.com/api/v2/accounts/{id}', params={

}, headers = headers)

print r.json()
```

```java
URL obj = new URL("://staging.whiplashmerch.com/api/v2/accounts/{id}");
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

`DELETE /api/v2/accounts/{id}`

*Destroy an account*

Destroy an account

### Parameters

Parameter|In|Type|Required|Description
---|---|---|---|---|
id|path|integer|true|No description
X-Customer-Id|header|string|false|The customer associated with this resource.


### Responses

Status|Meaning|Description
---|---|---|
200|[OK](https://tools.ietf.org/html/rfc7231#section-6.3.1)|Destroy an account
|Unknown|No description

> Example responses

```json
{
  "id": 0,
  "balance": 0,
  "currency": "string",
  "accountable_id": 0,
  "accountable_type": "string",
  "refill_amount": 0,
  "insure_threshold": 0,
  "require_signature_threshold": 0,
  "payment_method_token": "string",
  "created_at": "2017-06-19T15:15:48Z",
  "updated_at": "2017-06-19T15:15:48Z"
}
```
```json
{
  "message": "string"
}
```
<aside class="success">
This operation does not require authentication
</aside>

## getApiV2AccountsIdAccountTransactions

> Code samples

```shell
# You can also use wget
curl -X get ://staging.whiplashmerch.com/api/v2/accounts/{id}/account_transactions \
  -H 'X-Customer-Id: string' \
  -H 'Accept: application/json'

```

```http
GET ://staging.whiplashmerch.com/api/v2/accounts/{id}/account_transactions HTTP/1.1
Host: staging.whiplashmerch.com

Accept: application/json
X-Customer-Id: string

```

```javascript
var headers = {
  'X-Customer-Id':'string',
  'Accept':'application/json'

};

$.ajax({
  url: '://staging.whiplashmerch.com/api/v2/accounts/{id}/account_transactions',
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
  'X-Customer-Id':'string',
  'Accept':'application/json'

};

fetch('://staging.whiplashmerch.com/api/v2/accounts/{id}/account_transactions',
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
  'X-Customer-Id' => 'string',
  'Accept' => 'application/json'
}

result = RestClient.get '://staging.whiplashmerch.com/api/v2/accounts/{id}/account_transactions', params: {
  }, headers: headers

p JSON.parse(result)
```

```python
import requests
headers = {
  'X-Customer-Id': 'string',
  'Accept': 'application/json'
}

r = requests.get('://staging.whiplashmerch.com/api/v2/accounts/{id}/account_transactions', params={

}, headers = headers)

print r.json()
```

```java
URL obj = new URL("://staging.whiplashmerch.com/api/v2/accounts/{id}/account_transactions");
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

`GET /api/v2/accounts/{id}/account_transactions`

*Get all account transactions for an account*

Get all account transactions for an account

### Parameters

Parameter|In|Type|Required|Description
---|---|---|---|---|
X-Customer-Id|header|string|false|The customer associated with this resource.
search|query|string|false|JSON search string like {"attribute_eq": "Term"}
page|query|integer|false|Page of results to fetch.
per_page|query|integer|false|Number of results to return per page.
id|path|integer|true|No description


### Responses

Status|Meaning|Description
---|---|---|
200|[OK](https://tools.ietf.org/html/rfc7231#section-6.3.1)|Get all account transactions for an account
|Unknown|No description

> Example responses

```json
{
  "id": 0,
  "account_id": 0,
  "description": "string",
  "amount": 0,
  "invoice_id": 0,
  "created_at": "2017-06-19T15:15:48Z",
  "updated_at": "2017-06-19T15:15:48Z",
  "income_account": "string",
  "balance": 0,
  "warehouse_id": 0,
  "currency": "string"
}
```
```json
{
  "message": "string"
}
```
<aside class="success">
This operation does not require authentication
</aside>

# account_transactions

Operations about account_transactions

## getApiV2AccountTransactionsId

> Code samples

```shell
# You can also use wget
curl -X get ://staging.whiplashmerch.com/api/v2/account_transactions/{id} \
  -H 'X-Customer-Id: string' \
  -H 'Accept: application/json'

```

```http
GET ://staging.whiplashmerch.com/api/v2/account_transactions/{id} HTTP/1.1
Host: staging.whiplashmerch.com

Accept: application/json
X-Customer-Id: string

```

```javascript
var headers = {
  'X-Customer-Id':'string',
  'Accept':'application/json'

};

$.ajax({
  url: '://staging.whiplashmerch.com/api/v2/account_transactions/{id}',
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
  'X-Customer-Id':'string',
  'Accept':'application/json'

};

fetch('://staging.whiplashmerch.com/api/v2/account_transactions/{id}',
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
  'X-Customer-Id' => 'string',
  'Accept' => 'application/json'
}

result = RestClient.get '://staging.whiplashmerch.com/api/v2/account_transactions/{id}', params: {
  }, headers: headers

p JSON.parse(result)
```

```python
import requests
headers = {
  'X-Customer-Id': 'string',
  'Accept': 'application/json'
}

r = requests.get('://staging.whiplashmerch.com/api/v2/account_transactions/{id}', params={

}, headers = headers)

print r.json()
```

```java
URL obj = new URL("://staging.whiplashmerch.com/api/v2/account_transactions/{id}");
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

`GET /api/v2/account_transactions/{id}`

*Get an account transaction*

Get an account transaction

### Parameters

Parameter|In|Type|Required|Description
---|---|---|---|---|
id|path|integer|true|No description
X-Customer-Id|header|string|false|The customer associated with this resource.


### Responses

Status|Meaning|Description
---|---|---|
200|[OK](https://tools.ietf.org/html/rfc7231#section-6.3.1)|Get an account transaction
|Unknown|No description

> Example responses

```json
{
  "id": 0,
  "account_id": 0,
  "description": "string",
  "amount": 0,
  "invoice_id": 0,
  "created_at": "2017-06-19T15:15:48Z",
  "updated_at": "2017-06-19T15:15:48Z",
  "income_account": "string",
  "balance": 0,
  "warehouse_id": 0,
  "currency": "string"
}
```
```json
{
  "message": "string"
}
```
<aside class="success">
This operation does not require authentication
</aside>

# shipping_blacklisted_methods

Operations about shipping_blacklisted_methods

## getApiV2ShippingBlacklistedMethods

> Code samples

```shell
# You can also use wget
curl -X get ://staging.whiplashmerch.com/api/v2/shipping_blacklisted_methods \
  -H 'X-Customer-Id: string' \
  -H 'Accept: application/json'

```

```http
GET ://staging.whiplashmerch.com/api/v2/shipping_blacklisted_methods HTTP/1.1
Host: staging.whiplashmerch.com

Accept: application/json
X-Customer-Id: string

```

```javascript
var headers = {
  'X-Customer-Id':'string',
  'Accept':'application/json'

};

$.ajax({
  url: '://staging.whiplashmerch.com/api/v2/shipping_blacklisted_methods',
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
  'X-Customer-Id':'string',
  'Accept':'application/json'

};

fetch('://staging.whiplashmerch.com/api/v2/shipping_blacklisted_methods',
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
  'X-Customer-Id' => 'string',
  'Accept' => 'application/json'
}

result = RestClient.get '://staging.whiplashmerch.com/api/v2/shipping_blacklisted_methods', params: {
  }, headers: headers

p JSON.parse(result)
```

```python
import requests
headers = {
  'X-Customer-Id': 'string',
  'Accept': 'application/json'
}

r = requests.get('://staging.whiplashmerch.com/api/v2/shipping_blacklisted_methods', params={

}, headers = headers)

print r.json()
```

```java
URL obj = new URL("://staging.whiplashmerch.com/api/v2/shipping_blacklisted_methods");
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

`GET /api/v2/shipping_blacklisted_methods`

*Get all shipping_blacklisted_methods*

Get all shipping_blacklisted_methods

### Parameters

Parameter|In|Type|Required|Description
---|---|---|---|---|
X-Customer-Id|header|string|false|The customer associated with this resource.
search|query|string|false|JSON search string like {"attribute_eq": "Term"}
fields|query|string|false|Comma-separated list of fields to include in the response
page|query|integer|false|Page of results to fetch.
per_page|query|integer|false|Number of results to return per page.


### Responses

Status|Meaning|Description
---|---|---|
200|[OK](https://tools.ietf.org/html/rfc7231#section-6.3.1)|Get all shipping_blacklisted_methods
401|[Unauthorized](https://tools.ietf.org/html/rfc7235#section-3.1)|No description
403|[Forbidden](https://tools.ietf.org/html/rfc7231#section-6.5.3)|No description

> Example responses

```json
{
  "id": 0,
  "customer_id": 0,
  "shipping_method_id": 0,
  "origin": "string",
  "destination": "string",
  "created_at": "2017-06-19T15:15:48Z",
  "updated_at": "2017-06-19T15:15:48Z",
  "shipping_method": {
    "id": 0,
    "carrier": "string",
    "service": "string",
    "description": "string",
    "international": true,
    "active": true,
    "flat_rate": true,
    "expedited": true,
    "origins": "string",
    "extended_description": "string",
    "created_at": "2017-06-19T15:15:48Z",
    "updated_at": "2017-06-19T15:15:48Z"
  }
}
```
```json
{
  "message": "string"
}
```
```json
{
  "message": "string"
}
```
<aside class="success">
This operation does not require authentication
</aside>

## postApiV2ShippingBlacklistedMethods

> Code samples

```shell
# You can also use wget
curl -X post ://staging.whiplashmerch.com/api/v2/shipping_blacklisted_methods \
  -H 'X-Customer-Id: string' \
  -H 'Content-Type: application/json' \
  -H 'Accept: application/json'

```

```http
POST ://staging.whiplashmerch.com/api/v2/shipping_blacklisted_methods HTTP/1.1
Host: staging.whiplashmerch.com
Content-Type: application/json
Accept: application/json
X-Customer-Id: string

```

```javascript
var headers = {
  'X-Customer-Id':'string',
  'Content-Type':'application/json',
  'Accept':'application/json'

};

$.ajax({
  url: '://staging.whiplashmerch.com/api/v2/shipping_blacklisted_methods',
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
  'X-Customer-Id':'string',
  'Content-Type':'application/json',
  'Accept':'application/json'

};

fetch('://staging.whiplashmerch.com/api/v2/shipping_blacklisted_methods',
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
  'X-Customer-Id' => 'string',
  'Content-Type' => 'application/json',
  'Accept' => 'application/json'
}

result = RestClient.post '://staging.whiplashmerch.com/api/v2/shipping_blacklisted_methods', params: {
  }, headers: headers

p JSON.parse(result)
```

```python
import requests
headers = {
  'X-Customer-Id': 'string',
  'Content-Type': 'application/json',
  'Accept': 'application/json'
}

r = requests.post('://staging.whiplashmerch.com/api/v2/shipping_blacklisted_methods', params={

}, headers = headers)

print r.json()
```

```java
URL obj = new URL("://staging.whiplashmerch.com/api/v2/shipping_blacklisted_methods");
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

`POST /api/v2/shipping_blacklisted_methods`

*Create a shipping_blacklisted_method*

Create a shipping_blacklisted_method

### Parameters

Parameter|In|Type|Required|Description
---|---|---|---|---|
X-Customer-Id|header|string|false|The customer associated with this resource.
shipping_method_id|formData|integer|false|the blacklisted shipping method shipping method id
destination|formData|string|false|the blacklisted shipping method destination (Worldwide, US, CA, etc)
origin|formData|string|false|the blacklisted shipping method origin country iso2 (US, CA, etc)


### Responses

Status|Meaning|Description
---|---|---|
201|[Created](https://tools.ietf.org/html/rfc7231#section-6.3.2)|Create a shipping_blacklisted_method
401|[Unauthorized](https://tools.ietf.org/html/rfc7235#section-3.1)|No description
403|[Forbidden](https://tools.ietf.org/html/rfc7231#section-6.5.3)|No description
409|[Conflict](https://tools.ietf.org/html/rfc7231#section-6.5.8)|No description
422|[Unprocessable Entity](https://tools.ietf.org/html/rfc2518#section-10.3)|No description

> Example responses

```json
{
  "id": 0,
  "customer_id": 0,
  "shipping_method_id": 0,
  "origin": "string",
  "destination": "string",
  "created_at": "2017-06-19T15:15:48Z",
  "updated_at": "2017-06-19T15:15:48Z",
  "shipping_method": {
    "id": 0,
    "carrier": "string",
    "service": "string",
    "description": "string",
    "international": true,
    "active": true,
    "flat_rate": true,
    "expedited": true,
    "origins": "string",
    "extended_description": "string",
    "created_at": "2017-06-19T15:15:48Z",
    "updated_at": "2017-06-19T15:15:48Z"
  }
}
```
```json
{
  "message": "string"
}
```
```json
{
  "message": "string"
}
```
```json
{
  "message": "string"
}
```
```json
{
  "message": "string"
}
```
<aside class="success">
This operation does not require authentication
</aside>

## getApiV2ShippingBlacklistedMethodsCount

> Code samples

```shell
# You can also use wget
curl -X get ://staging.whiplashmerch.com/api/v2/shipping_blacklisted_methods/count \
  -H 'X-Customer-Id: string' \
  -H 'Accept: application/json'

```

```http
GET ://staging.whiplashmerch.com/api/v2/shipping_blacklisted_methods/count HTTP/1.1
Host: staging.whiplashmerch.com

Accept: application/json
X-Customer-Id: string

```

```javascript
var headers = {
  'X-Customer-Id':'string',
  'Accept':'application/json'

};

$.ajax({
  url: '://staging.whiplashmerch.com/api/v2/shipping_blacklisted_methods/count',
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
  'X-Customer-Id':'string',
  'Accept':'application/json'

};

fetch('://staging.whiplashmerch.com/api/v2/shipping_blacklisted_methods/count',
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
  'X-Customer-Id' => 'string',
  'Accept' => 'application/json'
}

result = RestClient.get '://staging.whiplashmerch.com/api/v2/shipping_blacklisted_methods/count', params: {
  }, headers: headers

p JSON.parse(result)
```

```python
import requests
headers = {
  'X-Customer-Id': 'string',
  'Accept': 'application/json'
}

r = requests.get('://staging.whiplashmerch.com/api/v2/shipping_blacklisted_methods/count', params={

}, headers = headers)

print r.json()
```

```java
URL obj = new URL("://staging.whiplashmerch.com/api/v2/shipping_blacklisted_methods/count");
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

`GET /api/v2/shipping_blacklisted_methods/count`

*Returns count of shipping_blacklisted_methods*

Returns count of shipping_blacklisted_methods

### Parameters

Parameter|In|Type|Required|Description
---|---|---|---|---|
X-Customer-Id|header|string|false|The customer associated with this resource.
search|query|string|false|JSON search string like {"attribute_eq": "Term"}


### Responses

Status|Meaning|Description
---|---|---|
200|[OK](https://tools.ietf.org/html/rfc7231#section-6.3.1)|Returns count of shipping_blacklisted_methods
401|[Unauthorized](https://tools.ietf.org/html/rfc7235#section-3.1)|No description
403|[Forbidden](https://tools.ietf.org/html/rfc7231#section-6.5.3)|No description

> Example responses

```json
{
  "id": 0,
  "customer_id": 0,
  "shipping_method_id": 0,
  "origin": "string",
  "destination": "string",
  "created_at": "2017-06-19T15:15:48Z",
  "updated_at": "2017-06-19T15:15:48Z",
  "shipping_method": {
    "id": 0,
    "carrier": "string",
    "service": "string",
    "description": "string",
    "international": true,
    "active": true,
    "flat_rate": true,
    "expedited": true,
    "origins": "string",
    "extended_description": "string",
    "created_at": "2017-06-19T15:15:48Z",
    "updated_at": "2017-06-19T15:15:48Z"
  }
}
```
```json
{
  "message": "string"
}
```
```json
{
  "message": "string"
}
```
<aside class="success">
This operation does not require authentication
</aside>

## getApiV2ShippingBlacklistedMethodsId

> Code samples

```shell
# You can also use wget
curl -X get ://staging.whiplashmerch.com/api/v2/shipping_blacklisted_methods/{id} \
  -H 'X-Customer-Id: string' \
  -H 'Accept: application/json'

```

```http
GET ://staging.whiplashmerch.com/api/v2/shipping_blacklisted_methods/{id} HTTP/1.1
Host: staging.whiplashmerch.com

Accept: application/json
X-Customer-Id: string

```

```javascript
var headers = {
  'X-Customer-Id':'string',
  'Accept':'application/json'

};

$.ajax({
  url: '://staging.whiplashmerch.com/api/v2/shipping_blacklisted_methods/{id}',
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
  'X-Customer-Id':'string',
  'Accept':'application/json'

};

fetch('://staging.whiplashmerch.com/api/v2/shipping_blacklisted_methods/{id}',
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
  'X-Customer-Id' => 'string',
  'Accept' => 'application/json'
}

result = RestClient.get '://staging.whiplashmerch.com/api/v2/shipping_blacklisted_methods/{id}', params: {
  }, headers: headers

p JSON.parse(result)
```

```python
import requests
headers = {
  'X-Customer-Id': 'string',
  'Accept': 'application/json'
}

r = requests.get('://staging.whiplashmerch.com/api/v2/shipping_blacklisted_methods/{id}', params={

}, headers = headers)

print r.json()
```

```java
URL obj = new URL("://staging.whiplashmerch.com/api/v2/shipping_blacklisted_methods/{id}");
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

`GET /api/v2/shipping_blacklisted_methods/{id}`

*Get a ShippingBlacklistedMethod*

Get a ShippingBlacklistedMethod

### Parameters

Parameter|In|Type|Required|Description
---|---|---|---|---|
id|path|integer|true|No description
X-Customer-Id|header|string|false|The customer associated with this resource.


### Responses

Status|Meaning|Description
---|---|---|
200|[OK](https://tools.ietf.org/html/rfc7231#section-6.3.1)|Get a ShippingBlacklistedMethod
401|[Unauthorized](https://tools.ietf.org/html/rfc7235#section-3.1)|No description
403|[Forbidden](https://tools.ietf.org/html/rfc7231#section-6.5.3)|No description

> Example responses

```json
{
  "id": 0,
  "customer_id": 0,
  "shipping_method_id": 0,
  "origin": "string",
  "destination": "string",
  "created_at": "2017-06-19T15:15:48Z",
  "updated_at": "2017-06-19T15:15:48Z",
  "shipping_method": {
    "id": 0,
    "carrier": "string",
    "service": "string",
    "description": "string",
    "international": true,
    "active": true,
    "flat_rate": true,
    "expedited": true,
    "origins": "string",
    "extended_description": "string",
    "created_at": "2017-06-19T15:15:48Z",
    "updated_at": "2017-06-19T15:15:48Z"
  }
}
```
```json
{
  "message": "string"
}
```
```json
{
  "message": "string"
}
```
<aside class="success">
This operation does not require authentication
</aside>

## putApiV2ShippingBlacklistedMethodsId

> Code samples

```shell
# You can also use wget
curl -X put ://staging.whiplashmerch.com/api/v2/shipping_blacklisted_methods/{id} \
  -H 'X-Customer-Id: string' \
  -H 'Content-Type: application/json' \
  -H 'Accept: application/json'

```

```http
PUT ://staging.whiplashmerch.com/api/v2/shipping_blacklisted_methods/{id} HTTP/1.1
Host: staging.whiplashmerch.com
Content-Type: application/json
Accept: application/json
X-Customer-Id: string

```

```javascript
var headers = {
  'X-Customer-Id':'string',
  'Content-Type':'application/json',
  'Accept':'application/json'

};

$.ajax({
  url: '://staging.whiplashmerch.com/api/v2/shipping_blacklisted_methods/{id}',
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
  'X-Customer-Id':'string',
  'Content-Type':'application/json',
  'Accept':'application/json'

};

fetch('://staging.whiplashmerch.com/api/v2/shipping_blacklisted_methods/{id}',
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
  'X-Customer-Id' => 'string',
  'Content-Type' => 'application/json',
  'Accept' => 'application/json'
}

result = RestClient.put '://staging.whiplashmerch.com/api/v2/shipping_blacklisted_methods/{id}', params: {
  }, headers: headers

p JSON.parse(result)
```

```python
import requests
headers = {
  'X-Customer-Id': 'string',
  'Content-Type': 'application/json',
  'Accept': 'application/json'
}

r = requests.put('://staging.whiplashmerch.com/api/v2/shipping_blacklisted_methods/{id}', params={

}, headers = headers)

print r.json()
```

```java
URL obj = new URL("://staging.whiplashmerch.com/api/v2/shipping_blacklisted_methods/{id}");
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

`PUT /api/v2/shipping_blacklisted_methods/{id}`

*Update a shipping_blacklisted_method*

Update a shipping_blacklisted_method

### Parameters

Parameter|In|Type|Required|Description
---|---|---|---|---|
X-Customer-Id|header|string|false|The customer associated with this resource.
customer_id|formData|integer|false|the blacklisted shipping method customer id
shipping_method_id|formData|integer|false|the blacklisted shipping method shipping method id
origin|formData|string|false|the blacklisted shipping method origin country iso2 (US, CA, etc)
destination|formData|string|false|the blacklisted shipping method destination (Worldwide, US, CA, etc)
id|path|integer|true|No description


### Responses

Status|Meaning|Description
---|---|---|
200|[OK](https://tools.ietf.org/html/rfc7231#section-6.3.1)|Update a shipping_blacklisted_method
401|[Unauthorized](https://tools.ietf.org/html/rfc7235#section-3.1)|No description
403|[Forbidden](https://tools.ietf.org/html/rfc7231#section-6.5.3)|No description
422|[Unprocessable Entity](https://tools.ietf.org/html/rfc2518#section-10.3)|No description

> Example responses

```json
{
  "id": 0,
  "customer_id": 0,
  "shipping_method_id": 0,
  "origin": "string",
  "destination": "string",
  "created_at": "2017-06-19T15:15:48Z",
  "updated_at": "2017-06-19T15:15:48Z",
  "shipping_method": {
    "id": 0,
    "carrier": "string",
    "service": "string",
    "description": "string",
    "international": true,
    "active": true,
    "flat_rate": true,
    "expedited": true,
    "origins": "string",
    "extended_description": "string",
    "created_at": "2017-06-19T15:15:48Z",
    "updated_at": "2017-06-19T15:15:48Z"
  }
}
```
```json
{
  "message": "string"
}
```
```json
{
  "message": "string"
}
```
```json
{
  "message": "string"
}
```
<aside class="success">
This operation does not require authentication
</aside>

## deleteApiV2ShippingBlacklistedMethodsId

> Code samples

```shell
# You can also use wget
curl -X delete ://staging.whiplashmerch.com/api/v2/shipping_blacklisted_methods/{id} \
  -H 'X-Customer-Id: string' \
  -H 'Accept: application/json'

```

```http
DELETE ://staging.whiplashmerch.com/api/v2/shipping_blacklisted_methods/{id} HTTP/1.1
Host: staging.whiplashmerch.com

Accept: application/json
X-Customer-Id: string

```

```javascript
var headers = {
  'X-Customer-Id':'string',
  'Accept':'application/json'

};

$.ajax({
  url: '://staging.whiplashmerch.com/api/v2/shipping_blacklisted_methods/{id}',
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
  'X-Customer-Id':'string',
  'Accept':'application/json'

};

fetch('://staging.whiplashmerch.com/api/v2/shipping_blacklisted_methods/{id}',
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
  'X-Customer-Id' => 'string',
  'Accept' => 'application/json'
}

result = RestClient.delete '://staging.whiplashmerch.com/api/v2/shipping_blacklisted_methods/{id}', params: {
  }, headers: headers

p JSON.parse(result)
```

```python
import requests
headers = {
  'X-Customer-Id': 'string',
  'Accept': 'application/json'
}

r = requests.delete('://staging.whiplashmerch.com/api/v2/shipping_blacklisted_methods/{id}', params={

}, headers = headers)

print r.json()
```

```java
URL obj = new URL("://staging.whiplashmerch.com/api/v2/shipping_blacklisted_methods/{id}");
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

`DELETE /api/v2/shipping_blacklisted_methods/{id}`

*Destroy a shipping_blacklisted_method*

Destroy a shipping_blacklisted_method

### Parameters

Parameter|In|Type|Required|Description
---|---|---|---|---|
id|path|integer|true|No description
X-Customer-Id|header|string|false|The customer associated with this resource.


### Responses

Status|Meaning|Description
---|---|---|
200|[OK](https://tools.ietf.org/html/rfc7231#section-6.3.1)|Destroy a shipping_blacklisted_method
401|[Unauthorized](https://tools.ietf.org/html/rfc7235#section-3.1)|No description
403|[Forbidden](https://tools.ietf.org/html/rfc7231#section-6.5.3)|No description
422|[Unprocessable Entity](https://tools.ietf.org/html/rfc2518#section-10.3)|No description

> Example responses

```json
{
  "id": 0,
  "customer_id": 0,
  "shipping_method_id": 0,
  "origin": "string",
  "destination": "string",
  "created_at": "2017-06-19T15:15:48Z",
  "updated_at": "2017-06-19T15:15:48Z",
  "shipping_method": {
    "id": 0,
    "carrier": "string",
    "service": "string",
    "description": "string",
    "international": true,
    "active": true,
    "flat_rate": true,
    "expedited": true,
    "origins": "string",
    "extended_description": "string",
    "created_at": "2017-06-19T15:15:48Z",
    "updated_at": "2017-06-19T15:15:48Z"
  }
}
```
```json
{
  "message": "string"
}
```
```json
{
  "message": "string"
}
```
```json
{
  "message": "string"
}
```
<aside class="success">
This operation does not require authentication
</aside>

# shipping_aliases

Operations about shipping_aliases

## getApiV2ShippingAliases

> Code samples

```shell
# You can also use wget
curl -X get ://staging.whiplashmerch.com/api/v2/shipping_aliases \
  -H 'X-Customer-Id: string' \
  -H 'Accept: application/json'

```

```http
GET ://staging.whiplashmerch.com/api/v2/shipping_aliases HTTP/1.1
Host: staging.whiplashmerch.com

Accept: application/json
X-Customer-Id: string

```

```javascript
var headers = {
  'X-Customer-Id':'string',
  'Accept':'application/json'

};

$.ajax({
  url: '://staging.whiplashmerch.com/api/v2/shipping_aliases',
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
  'X-Customer-Id':'string',
  'Accept':'application/json'

};

fetch('://staging.whiplashmerch.com/api/v2/shipping_aliases',
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
  'X-Customer-Id' => 'string',
  'Accept' => 'application/json'
}

result = RestClient.get '://staging.whiplashmerch.com/api/v2/shipping_aliases', params: {
  }, headers: headers

p JSON.parse(result)
```

```python
import requests
headers = {
  'X-Customer-Id': 'string',
  'Accept': 'application/json'
}

r = requests.get('://staging.whiplashmerch.com/api/v2/shipping_aliases', params={

}, headers = headers)

print r.json()
```

```java
URL obj = new URL("://staging.whiplashmerch.com/api/v2/shipping_aliases");
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

`GET /api/v2/shipping_aliases`

*Get all shipping_aliases*

Get all shipping_aliases

### Parameters

Parameter|In|Type|Required|Description
---|---|---|---|---|
X-Customer-Id|header|string|false|The customer associated with this resource.
search|query|string|false|JSON search string like {"attribute_eq": "Term"}
fields|query|string|false|Comma-separated list of fields to include in the response
page|query|integer|false|Page of results to fetch.
per_page|query|integer|false|Number of results to return per page.


### Responses

Status|Meaning|Description
---|---|---|
200|[OK](https://tools.ietf.org/html/rfc7231#section-6.3.1)|Get all shipping_aliases
401|[Unauthorized](https://tools.ietf.org/html/rfc7235#section-3.1)|No description
403|[Forbidden](https://tools.ietf.org/html/rfc7231#section-6.5.3)|No description

> Example responses

```json
{
  "id": 0,
  "shipping_method_id": 0,
  "description": "string",
  "destination": "string",
  "customer_id": 0,
  "origin": "string",
  "created_at": "2017-06-19T15:15:48Z",
  "updated_at": "2017-06-19T15:15:48Z",
  "deleted_at": "2017-06-19T15:15:48Z",
  "shipping_method": {
    "id": 0,
    "carrier": "string",
    "service": "string",
    "description": "string",
    "international": true,
    "active": true,
    "flat_rate": true,
    "expedited": true,
    "origins": "string",
    "extended_description": "string",
    "created_at": "2017-06-19T15:15:48Z",
    "updated_at": "2017-06-19T15:15:48Z"
  }
}
```
```json
{
  "message": "string"
}
```
```json
{
  "message": "string"
}
```
<aside class="success">
This operation does not require authentication
</aside>

## postApiV2ShippingAliases

> Code samples

```shell
# You can also use wget
curl -X post ://staging.whiplashmerch.com/api/v2/shipping_aliases \
  -H 'X-Customer-Id: string' \
  -H 'Content-Type: application/json' \
  -H 'Accept: application/json'

```

```http
POST ://staging.whiplashmerch.com/api/v2/shipping_aliases HTTP/1.1
Host: staging.whiplashmerch.com
Content-Type: application/json
Accept: application/json
X-Customer-Id: string

```

```javascript
var headers = {
  'X-Customer-Id':'string',
  'Content-Type':'application/json',
  'Accept':'application/json'

};

$.ajax({
  url: '://staging.whiplashmerch.com/api/v2/shipping_aliases',
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
  'X-Customer-Id':'string',
  'Content-Type':'application/json',
  'Accept':'application/json'

};

fetch('://staging.whiplashmerch.com/api/v2/shipping_aliases',
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
  'X-Customer-Id' => 'string',
  'Content-Type' => 'application/json',
  'Accept' => 'application/json'
}

result = RestClient.post '://staging.whiplashmerch.com/api/v2/shipping_aliases', params: {
  }, headers: headers

p JSON.parse(result)
```

```python
import requests
headers = {
  'X-Customer-Id': 'string',
  'Content-Type': 'application/json',
  'Accept': 'application/json'
}

r = requests.post('://staging.whiplashmerch.com/api/v2/shipping_aliases', params={

}, headers = headers)

print r.json()
```

```java
URL obj = new URL("://staging.whiplashmerch.com/api/v2/shipping_aliases");
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

`POST /api/v2/shipping_aliases`

*Create a shipping_alias*

Create a shipping_alias

### Parameters

Parameter|In|Type|Required|Description
---|---|---|---|---|
X-Customer-Id|header|string|false|The customer associated with this resource.
shipping_method_id|formData|integer|false|the shipping alias shipping method id
description|formData|string|false|the shipping alias description
origin|formData|string|false|the shipping alias origin (US, CA, GB, etc)
destination|formData|string|false|the shipping alias destination (Worldwide, CA, US, etc)
customer_id|formData|integer|false|the shipping alias customer id
deleted_at|formData|string|false|the shipping alias deletion date and time


### Responses

Status|Meaning|Description
---|---|---|
201|[Created](https://tools.ietf.org/html/rfc7231#section-6.3.2)|Create a shipping_alias
401|[Unauthorized](https://tools.ietf.org/html/rfc7235#section-3.1)|No description
403|[Forbidden](https://tools.ietf.org/html/rfc7231#section-6.5.3)|No description
409|[Conflict](https://tools.ietf.org/html/rfc7231#section-6.5.8)|No description
422|[Unprocessable Entity](https://tools.ietf.org/html/rfc2518#section-10.3)|No description

> Example responses

```json
{
  "id": 0,
  "shipping_method_id": 0,
  "description": "string",
  "destination": "string",
  "customer_id": 0,
  "origin": "string",
  "created_at": "2017-06-19T15:15:48Z",
  "updated_at": "2017-06-19T15:15:48Z",
  "deleted_at": "2017-06-19T15:15:48Z",
  "shipping_method": {
    "id": 0,
    "carrier": "string",
    "service": "string",
    "description": "string",
    "international": true,
    "active": true,
    "flat_rate": true,
    "expedited": true,
    "origins": "string",
    "extended_description": "string",
    "created_at": "2017-06-19T15:15:48Z",
    "updated_at": "2017-06-19T15:15:48Z"
  }
}
```
```json
{
  "message": "string"
}
```
```json
{
  "message": "string"
}
```
```json
{
  "message": "string"
}
```
```json
{
  "message": "string"
}
```
<aside class="success">
This operation does not require authentication
</aside>

## getApiV2ShippingAliasesCount

> Code samples

```shell
# You can also use wget
curl -X get ://staging.whiplashmerch.com/api/v2/shipping_aliases/count \
  -H 'X-Customer-Id: string' \
  -H 'Accept: application/json'

```

```http
GET ://staging.whiplashmerch.com/api/v2/shipping_aliases/count HTTP/1.1
Host: staging.whiplashmerch.com

Accept: application/json
X-Customer-Id: string

```

```javascript
var headers = {
  'X-Customer-Id':'string',
  'Accept':'application/json'

};

$.ajax({
  url: '://staging.whiplashmerch.com/api/v2/shipping_aliases/count',
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
  'X-Customer-Id':'string',
  'Accept':'application/json'

};

fetch('://staging.whiplashmerch.com/api/v2/shipping_aliases/count',
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
  'X-Customer-Id' => 'string',
  'Accept' => 'application/json'
}

result = RestClient.get '://staging.whiplashmerch.com/api/v2/shipping_aliases/count', params: {
  }, headers: headers

p JSON.parse(result)
```

```python
import requests
headers = {
  'X-Customer-Id': 'string',
  'Accept': 'application/json'
}

r = requests.get('://staging.whiplashmerch.com/api/v2/shipping_aliases/count', params={

}, headers = headers)

print r.json()
```

```java
URL obj = new URL("://staging.whiplashmerch.com/api/v2/shipping_aliases/count");
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

`GET /api/v2/shipping_aliases/count`

*Returns count of shipping_aliases*

Returns count of shipping_aliases

### Parameters

Parameter|In|Type|Required|Description
---|---|---|---|---|
X-Customer-Id|header|string|false|The customer associated with this resource.
search|query|string|false|JSON search string like {"attribute_eq": "Term"}


### Responses

Status|Meaning|Description
---|---|---|
200|[OK](https://tools.ietf.org/html/rfc7231#section-6.3.1)|Returns count of shipping_aliases
401|[Unauthorized](https://tools.ietf.org/html/rfc7235#section-3.1)|No description
403|[Forbidden](https://tools.ietf.org/html/rfc7231#section-6.5.3)|No description

> Example responses

```json
{
  "id": 0,
  "shipping_method_id": 0,
  "description": "string",
  "destination": "string",
  "customer_id": 0,
  "origin": "string",
  "created_at": "2017-06-19T15:15:48Z",
  "updated_at": "2017-06-19T15:15:48Z",
  "deleted_at": "2017-06-19T15:15:48Z",
  "shipping_method": {
    "id": 0,
    "carrier": "string",
    "service": "string",
    "description": "string",
    "international": true,
    "active": true,
    "flat_rate": true,
    "expedited": true,
    "origins": "string",
    "extended_description": "string",
    "created_at": "2017-06-19T15:15:48Z",
    "updated_at": "2017-06-19T15:15:48Z"
  }
}
```
```json
{
  "message": "string"
}
```
```json
{
  "message": "string"
}
```
<aside class="success">
This operation does not require authentication
</aside>

## getApiV2ShippingAliasesId

> Code samples

```shell
# You can also use wget
curl -X get ://staging.whiplashmerch.com/api/v2/shipping_aliases/{id} \
  -H 'X-Customer-Id: string' \
  -H 'Accept: application/json'

```

```http
GET ://staging.whiplashmerch.com/api/v2/shipping_aliases/{id} HTTP/1.1
Host: staging.whiplashmerch.com

Accept: application/json
X-Customer-Id: string

```

```javascript
var headers = {
  'X-Customer-Id':'string',
  'Accept':'application/json'

};

$.ajax({
  url: '://staging.whiplashmerch.com/api/v2/shipping_aliases/{id}',
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
  'X-Customer-Id':'string',
  'Accept':'application/json'

};

fetch('://staging.whiplashmerch.com/api/v2/shipping_aliases/{id}',
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
  'X-Customer-Id' => 'string',
  'Accept' => 'application/json'
}

result = RestClient.get '://staging.whiplashmerch.com/api/v2/shipping_aliases/{id}', params: {
  }, headers: headers

p JSON.parse(result)
```

```python
import requests
headers = {
  'X-Customer-Id': 'string',
  'Accept': 'application/json'
}

r = requests.get('://staging.whiplashmerch.com/api/v2/shipping_aliases/{id}', params={

}, headers = headers)

print r.json()
```

```java
URL obj = new URL("://staging.whiplashmerch.com/api/v2/shipping_aliases/{id}");
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

`GET /api/v2/shipping_aliases/{id}`

*Get a ShippingAlias*

Get a ShippingAlias

### Parameters

Parameter|In|Type|Required|Description
---|---|---|---|---|
id|path|integer|true|No description
X-Customer-Id|header|string|false|The customer associated with this resource.


### Responses

Status|Meaning|Description
---|---|---|
200|[OK](https://tools.ietf.org/html/rfc7231#section-6.3.1)|Get a ShippingAlias
401|[Unauthorized](https://tools.ietf.org/html/rfc7235#section-3.1)|No description
403|[Forbidden](https://tools.ietf.org/html/rfc7231#section-6.5.3)|No description

> Example responses

```json
{
  "id": 0,
  "shipping_method_id": 0,
  "description": "string",
  "destination": "string",
  "customer_id": 0,
  "origin": "string",
  "created_at": "2017-06-19T15:15:48Z",
  "updated_at": "2017-06-19T15:15:48Z",
  "deleted_at": "2017-06-19T15:15:48Z",
  "shipping_method": {
    "id": 0,
    "carrier": "string",
    "service": "string",
    "description": "string",
    "international": true,
    "active": true,
    "flat_rate": true,
    "expedited": true,
    "origins": "string",
    "extended_description": "string",
    "created_at": "2017-06-19T15:15:48Z",
    "updated_at": "2017-06-19T15:15:48Z"
  }
}
```
```json
{
  "message": "string"
}
```
```json
{
  "message": "string"
}
```
<aside class="success">
This operation does not require authentication
</aside>

## putApiV2ShippingAliasesId

> Code samples

```shell
# You can also use wget
curl -X put ://staging.whiplashmerch.com/api/v2/shipping_aliases/{id} \
  -H 'X-Customer-Id: string' \
  -H 'Content-Type: application/json' \
  -H 'Accept: application/json'

```

```http
PUT ://staging.whiplashmerch.com/api/v2/shipping_aliases/{id} HTTP/1.1
Host: staging.whiplashmerch.com
Content-Type: application/json
Accept: application/json
X-Customer-Id: string

```

```javascript
var headers = {
  'X-Customer-Id':'string',
  'Content-Type':'application/json',
  'Accept':'application/json'

};

$.ajax({
  url: '://staging.whiplashmerch.com/api/v2/shipping_aliases/{id}',
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
  'X-Customer-Id':'string',
  'Content-Type':'application/json',
  'Accept':'application/json'

};

fetch('://staging.whiplashmerch.com/api/v2/shipping_aliases/{id}',
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
  'X-Customer-Id' => 'string',
  'Content-Type' => 'application/json',
  'Accept' => 'application/json'
}

result = RestClient.put '://staging.whiplashmerch.com/api/v2/shipping_aliases/{id}', params: {
  }, headers: headers

p JSON.parse(result)
```

```python
import requests
headers = {
  'X-Customer-Id': 'string',
  'Content-Type': 'application/json',
  'Accept': 'application/json'
}

r = requests.put('://staging.whiplashmerch.com/api/v2/shipping_aliases/{id}', params={

}, headers = headers)

print r.json()
```

```java
URL obj = new URL("://staging.whiplashmerch.com/api/v2/shipping_aliases/{id}");
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

`PUT /api/v2/shipping_aliases/{id}`

*Update a shipping_alias*

Update a shipping_alias

### Parameters

Parameter|In|Type|Required|Description
---|---|---|---|---|
X-Customer-Id|header|string|false|The customer associated with this resource.
shipping_method_id|formData|integer|false|the shipping alias shipping method id
description|formData|string|false|the shipping alias description
destination|formData|string|false|the shipping alias destination (Worldwide, CA, US, etc)
customer_id|formData|integer|false|the shipping alias customer id
origin|formData|string|false|the shipping alias origin (US, CA, GB, etc)
deleted_at|formData|string|false|the shipping alias deletion date and time
id|path|integer|true|No description


### Responses

Status|Meaning|Description
---|---|---|
200|[OK](https://tools.ietf.org/html/rfc7231#section-6.3.1)|Update a shipping_alias
401|[Unauthorized](https://tools.ietf.org/html/rfc7235#section-3.1)|No description
403|[Forbidden](https://tools.ietf.org/html/rfc7231#section-6.5.3)|No description
422|[Unprocessable Entity](https://tools.ietf.org/html/rfc2518#section-10.3)|No description

> Example responses

```json
{
  "id": 0,
  "shipping_method_id": 0,
  "description": "string",
  "destination": "string",
  "customer_id": 0,
  "origin": "string",
  "created_at": "2017-06-19T15:15:48Z",
  "updated_at": "2017-06-19T15:15:48Z",
  "deleted_at": "2017-06-19T15:15:48Z",
  "shipping_method": {
    "id": 0,
    "carrier": "string",
    "service": "string",
    "description": "string",
    "international": true,
    "active": true,
    "flat_rate": true,
    "expedited": true,
    "origins": "string",
    "extended_description": "string",
    "created_at": "2017-06-19T15:15:48Z",
    "updated_at": "2017-06-19T15:15:48Z"
  }
}
```
```json
{
  "message": "string"
}
```
```json
{
  "message": "string"
}
```
```json
{
  "message": "string"
}
```
<aside class="success">
This operation does not require authentication
</aside>

## deleteApiV2ShippingAliasesId

> Code samples

```shell
# You can also use wget
curl -X delete ://staging.whiplashmerch.com/api/v2/shipping_aliases/{id} \
  -H 'X-Customer-Id: string' \
  -H 'Accept: application/json'

```

```http
DELETE ://staging.whiplashmerch.com/api/v2/shipping_aliases/{id} HTTP/1.1
Host: staging.whiplashmerch.com

Accept: application/json
X-Customer-Id: string

```

```javascript
var headers = {
  'X-Customer-Id':'string',
  'Accept':'application/json'

};

$.ajax({
  url: '://staging.whiplashmerch.com/api/v2/shipping_aliases/{id}',
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
  'X-Customer-Id':'string',
  'Accept':'application/json'

};

fetch('://staging.whiplashmerch.com/api/v2/shipping_aliases/{id}',
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
  'X-Customer-Id' => 'string',
  'Accept' => 'application/json'
}

result = RestClient.delete '://staging.whiplashmerch.com/api/v2/shipping_aliases/{id}', params: {
  }, headers: headers

p JSON.parse(result)
```

```python
import requests
headers = {
  'X-Customer-Id': 'string',
  'Accept': 'application/json'
}

r = requests.delete('://staging.whiplashmerch.com/api/v2/shipping_aliases/{id}', params={

}, headers = headers)

print r.json()
```

```java
URL obj = new URL("://staging.whiplashmerch.com/api/v2/shipping_aliases/{id}");
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

`DELETE /api/v2/shipping_aliases/{id}`

*Destroy a shipping_alias*

Destroy a shipping_alias

### Parameters

Parameter|In|Type|Required|Description
---|---|---|---|---|
id|path|integer|true|No description
X-Customer-Id|header|string|false|The customer associated with this resource.


### Responses

Status|Meaning|Description
---|---|---|
200|[OK](https://tools.ietf.org/html/rfc7231#section-6.3.1)|Destroy a shipping_alias
401|[Unauthorized](https://tools.ietf.org/html/rfc7235#section-3.1)|No description
403|[Forbidden](https://tools.ietf.org/html/rfc7231#section-6.5.3)|No description
422|[Unprocessable Entity](https://tools.ietf.org/html/rfc2518#section-10.3)|No description

> Example responses

```json
{
  "id": 0,
  "shipping_method_id": 0,
  "description": "string",
  "destination": "string",
  "customer_id": 0,
  "origin": "string",
  "created_at": "2017-06-19T15:15:48Z",
  "updated_at": "2017-06-19T15:15:48Z",
  "deleted_at": "2017-06-19T15:15:48Z",
  "shipping_method": {
    "id": 0,
    "carrier": "string",
    "service": "string",
    "description": "string",
    "international": true,
    "active": true,
    "flat_rate": true,
    "expedited": true,
    "origins": "string",
    "extended_description": "string",
    "created_at": "2017-06-19T15:15:48Z",
    "updated_at": "2017-06-19T15:15:48Z"
  }
}
```
```json
{
  "message": "string"
}
```
```json
{
  "message": "string"
}
```
```json
{
  "message": "string"
}
```
<aside class="success">
This operation does not require authentication
</aside>

# shipping_methods

Operations about shipping_methods

## getApiV2ShippingMethods

> Code samples

```shell
# You can also use wget
curl -X get ://staging.whiplashmerch.com/api/v2/shipping_methods \
  -H 'Accept: application/json'

```

```http
GET ://staging.whiplashmerch.com/api/v2/shipping_methods HTTP/1.1
Host: staging.whiplashmerch.com

Accept: application/json

```

```javascript
var headers = {
  'Accept':'application/json'

};

$.ajax({
  url: '://staging.whiplashmerch.com/api/v2/shipping_methods',
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
  'Accept':'application/json'

};

fetch('://staging.whiplashmerch.com/api/v2/shipping_methods',
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
  'Accept' => 'application/json'
}

result = RestClient.get '://staging.whiplashmerch.com/api/v2/shipping_methods', params: {
  }, headers: headers

p JSON.parse(result)
```

```python
import requests
headers = {
  'Accept': 'application/json'
}

r = requests.get('://staging.whiplashmerch.com/api/v2/shipping_methods', params={

}, headers = headers)

print r.json()
```

```java
URL obj = new URL("://staging.whiplashmerch.com/api/v2/shipping_methods");
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

`GET /api/v2/shipping_methods`

*Get all shipping_methods*

Get all shipping_methods

### Parameters

Parameter|In|Type|Required|Description
---|---|---|---|---|
search|query|string|false|JSON search string like {"attribute_eq": "Term"}
fields|query|string|false|Comma-separated list of fields to include in the response
page|query|integer|false|Page of results to fetch.
per_page|query|integer|false|Number of results to return per page.


### Responses

Status|Meaning|Description
---|---|---|
200|[OK](https://tools.ietf.org/html/rfc7231#section-6.3.1)|Get all shipping_methods
401|[Unauthorized](https://tools.ietf.org/html/rfc7235#section-3.1)|No description
403|[Forbidden](https://tools.ietf.org/html/rfc7231#section-6.5.3)|No description

> Example responses

```json
{
  "id": 0,
  "carrier": "string",
  "service": "string",
  "description": "string",
  "international": true,
  "active": true,
  "flat_rate": true,
  "expedited": true,
  "origins": "string",
  "extended_description": "string",
  "created_at": "2017-06-19T15:15:48Z",
  "updated_at": "2017-06-19T15:15:48Z"
}
```
```json
{
  "message": "string"
}
```
```json
{
  "message": "string"
}
```
<aside class="success">
This operation does not require authentication
</aside>

## postApiV2ShippingMethods

> Code samples

```shell
# You can also use wget
curl -X post ://staging.whiplashmerch.com/api/v2/shipping_methods \
  -H 'Content-Type: application/json' \
  -H 'Accept: application/json'

```

```http
POST ://staging.whiplashmerch.com/api/v2/shipping_methods HTTP/1.1
Host: staging.whiplashmerch.com
Content-Type: application/json
Accept: application/json

```

```javascript
var headers = {
  'Content-Type':'application/json',
  'Accept':'application/json'

};

$.ajax({
  url: '://staging.whiplashmerch.com/api/v2/shipping_methods',
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
  'Content-Type':'application/json',
  'Accept':'application/json'

};

fetch('://staging.whiplashmerch.com/api/v2/shipping_methods',
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
  'Content-Type' => 'application/json',
  'Accept' => 'application/json'
}

result = RestClient.post '://staging.whiplashmerch.com/api/v2/shipping_methods', params: {
  }, headers: headers

p JSON.parse(result)
```

```python
import requests
headers = {
  'Content-Type': 'application/json',
  'Accept': 'application/json'
}

r = requests.post('://staging.whiplashmerch.com/api/v2/shipping_methods', params={

}, headers = headers)

print r.json()
```

```java
URL obj = new URL("://staging.whiplashmerch.com/api/v2/shipping_methods");
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

`POST /api/v2/shipping_methods`

*Create a shipping_method*

Create a shipping_method

### Parameters

Parameter|In|Type|Required|Description
---|---|---|---|---|
carrier|formData|string|false|the shipping method carrier (FedEx, UPS, etc)
service|formData|string|false|the shipping method service (NextDayAir, Ground, etc)
description|formData|string|false|the shipping method service description (Next Day Air, Ground, etc)
origins|formData|array[string]|false|the shipping method origin countries (["CA", "US", "GB", ...])
international|formData|boolean|false|is the shipping method international?
active|formData|boolean|false|is the shipping method active?
flat_rate|formData|boolean|false|is the shipping method flat rate?
expedited|formData|boolean|false|is the shipping method expedited?
extended_description|formData|string|false|the shipping method extended description


### Responses

Status|Meaning|Description
---|---|---|
201|[Created](https://tools.ietf.org/html/rfc7231#section-6.3.2)|Create a shipping_method
401|[Unauthorized](https://tools.ietf.org/html/rfc7235#section-3.1)|No description
403|[Forbidden](https://tools.ietf.org/html/rfc7231#section-6.5.3)|No description
409|[Conflict](https://tools.ietf.org/html/rfc7231#section-6.5.8)|No description
422|[Unprocessable Entity](https://tools.ietf.org/html/rfc2518#section-10.3)|No description

> Example responses

```json
{
  "id": 0,
  "carrier": "string",
  "service": "string",
  "description": "string",
  "international": true,
  "active": true,
  "flat_rate": true,
  "expedited": true,
  "origins": "string",
  "extended_description": "string",
  "created_at": "2017-06-19T15:15:48Z",
  "updated_at": "2017-06-19T15:15:48Z"
}
```
```json
{
  "message": "string"
}
```
```json
{
  "message": "string"
}
```
```json
{
  "message": "string"
}
```
```json
{
  "message": "string"
}
```
<aside class="success">
This operation does not require authentication
</aside>

## getApiV2ShippingMethodsCount

> Code samples

```shell
# You can also use wget
curl -X get ://staging.whiplashmerch.com/api/v2/shipping_methods/count \
  -H 'Accept: application/json'

```

```http
GET ://staging.whiplashmerch.com/api/v2/shipping_methods/count HTTP/1.1
Host: staging.whiplashmerch.com

Accept: application/json

```

```javascript
var headers = {
  'Accept':'application/json'

};

$.ajax({
  url: '://staging.whiplashmerch.com/api/v2/shipping_methods/count',
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
  'Accept':'application/json'

};

fetch('://staging.whiplashmerch.com/api/v2/shipping_methods/count',
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
  'Accept' => 'application/json'
}

result = RestClient.get '://staging.whiplashmerch.com/api/v2/shipping_methods/count', params: {
  }, headers: headers

p JSON.parse(result)
```

```python
import requests
headers = {
  'Accept': 'application/json'
}

r = requests.get('://staging.whiplashmerch.com/api/v2/shipping_methods/count', params={

}, headers = headers)

print r.json()
```

```java
URL obj = new URL("://staging.whiplashmerch.com/api/v2/shipping_methods/count");
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

`GET /api/v2/shipping_methods/count`

*Returns count of shipping_methods*

Returns count of shipping_methods

### Parameters

Parameter|In|Type|Required|Description
---|---|---|---|---|
search|query|string|false|JSON search string like {"attribute_eq": "Term"}


### Responses

Status|Meaning|Description
---|---|---|
200|[OK](https://tools.ietf.org/html/rfc7231#section-6.3.1)|Returns count of shipping_methods
401|[Unauthorized](https://tools.ietf.org/html/rfc7235#section-3.1)|No description
403|[Forbidden](https://tools.ietf.org/html/rfc7231#section-6.5.3)|No description

> Example responses

```json
{
  "id": 0,
  "carrier": "string",
  "service": "string",
  "description": "string",
  "international": true,
  "active": true,
  "flat_rate": true,
  "expedited": true,
  "origins": "string",
  "extended_description": "string",
  "created_at": "2017-06-19T15:15:48Z",
  "updated_at": "2017-06-19T15:15:48Z"
}
```
```json
{
  "message": "string"
}
```
```json
{
  "message": "string"
}
```
<aside class="success">
This operation does not require authentication
</aside>

## getApiV2ShippingMethodsId

> Code samples

```shell
# You can also use wget
curl -X get ://staging.whiplashmerch.com/api/v2/shipping_methods/{id} \
  -H 'Accept: application/json'

```

```http
GET ://staging.whiplashmerch.com/api/v2/shipping_methods/{id} HTTP/1.1
Host: staging.whiplashmerch.com

Accept: application/json

```

```javascript
var headers = {
  'Accept':'application/json'

};

$.ajax({
  url: '://staging.whiplashmerch.com/api/v2/shipping_methods/{id}',
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
  'Accept':'application/json'

};

fetch('://staging.whiplashmerch.com/api/v2/shipping_methods/{id}',
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
  'Accept' => 'application/json'
}

result = RestClient.get '://staging.whiplashmerch.com/api/v2/shipping_methods/{id}', params: {
  }, headers: headers

p JSON.parse(result)
```

```python
import requests
headers = {
  'Accept': 'application/json'
}

r = requests.get('://staging.whiplashmerch.com/api/v2/shipping_methods/{id}', params={

}, headers = headers)

print r.json()
```

```java
URL obj = new URL("://staging.whiplashmerch.com/api/v2/shipping_methods/{id}");
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

`GET /api/v2/shipping_methods/{id}`

*Get a ShippingMethod*

Get a ShippingMethod

### Parameters

Parameter|In|Type|Required|Description
---|---|---|---|---|
id|path|integer|true|No description


### Responses

Status|Meaning|Description
---|---|---|
200|[OK](https://tools.ietf.org/html/rfc7231#section-6.3.1)|Get a ShippingMethod
401|[Unauthorized](https://tools.ietf.org/html/rfc7235#section-3.1)|No description
403|[Forbidden](https://tools.ietf.org/html/rfc7231#section-6.5.3)|No description

> Example responses

```json
{
  "id": 0,
  "carrier": "string",
  "service": "string",
  "description": "string",
  "international": true,
  "active": true,
  "flat_rate": true,
  "expedited": true,
  "origins": "string",
  "extended_description": "string",
  "created_at": "2017-06-19T15:15:48Z",
  "updated_at": "2017-06-19T15:15:48Z"
}
```
```json
{
  "message": "string"
}
```
```json
{
  "message": "string"
}
```
<aside class="success">
This operation does not require authentication
</aside>

## putApiV2ShippingMethodsId

> Code samples

```shell
# You can also use wget
curl -X put ://staging.whiplashmerch.com/api/v2/shipping_methods/{id} \
  -H 'Content-Type: application/json' \
  -H 'Accept: application/json'

```

```http
PUT ://staging.whiplashmerch.com/api/v2/shipping_methods/{id} HTTP/1.1
Host: staging.whiplashmerch.com
Content-Type: application/json
Accept: application/json

```

```javascript
var headers = {
  'Content-Type':'application/json',
  'Accept':'application/json'

};

$.ajax({
  url: '://staging.whiplashmerch.com/api/v2/shipping_methods/{id}',
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
  'Content-Type':'application/json',
  'Accept':'application/json'

};

fetch('://staging.whiplashmerch.com/api/v2/shipping_methods/{id}',
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
  'Content-Type' => 'application/json',
  'Accept' => 'application/json'
}

result = RestClient.put '://staging.whiplashmerch.com/api/v2/shipping_methods/{id}', params: {
  }, headers: headers

p JSON.parse(result)
```

```python
import requests
headers = {
  'Content-Type': 'application/json',
  'Accept': 'application/json'
}

r = requests.put('://staging.whiplashmerch.com/api/v2/shipping_methods/{id}', params={

}, headers = headers)

print r.json()
```

```java
URL obj = new URL("://staging.whiplashmerch.com/api/v2/shipping_methods/{id}");
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

`PUT /api/v2/shipping_methods/{id}`

*Update a shipping_method*

Update a shipping_method

### Parameters

Parameter|In|Type|Required|Description
---|---|---|---|---|
carrier|formData|string|false|the shipping method carrier (FedEx, UPS, etc)
service|formData|string|false|the shipping method service (NextDayAir, Ground, etc)
description|formData|string|false|the shipping method service description (Next Day Air, Ground, etc)
international|formData|boolean|false|is the shipping method international?
active|formData|boolean|false|is the shipping method active?
flat_rate|formData|boolean|false|is the shipping method flat rate?
expedited|formData|boolean|false|is the shipping method expedited?
origins|formData|array[string]|false|the shipping method origin countries (["CA", "US", "GB", ...])
extended_description|formData|string|false|the shipping method extended description
id|path|integer|true|No description


### Responses

Status|Meaning|Description
---|---|---|
200|[OK](https://tools.ietf.org/html/rfc7231#section-6.3.1)|Update a shipping_method
401|[Unauthorized](https://tools.ietf.org/html/rfc7235#section-3.1)|No description
403|[Forbidden](https://tools.ietf.org/html/rfc7231#section-6.5.3)|No description
422|[Unprocessable Entity](https://tools.ietf.org/html/rfc2518#section-10.3)|No description

> Example responses

```json
{
  "id": 0,
  "carrier": "string",
  "service": "string",
  "description": "string",
  "international": true,
  "active": true,
  "flat_rate": true,
  "expedited": true,
  "origins": "string",
  "extended_description": "string",
  "created_at": "2017-06-19T15:15:48Z",
  "updated_at": "2017-06-19T15:15:48Z"
}
```
```json
{
  "message": "string"
}
```
```json
{
  "message": "string"
}
```
```json
{
  "message": "string"
}
```
<aside class="success">
This operation does not require authentication
</aside>

## deleteApiV2ShippingMethodsId

> Code samples

```shell
# You can also use wget
curl -X delete ://staging.whiplashmerch.com/api/v2/shipping_methods/{id} \
  -H 'Accept: application/json'

```

```http
DELETE ://staging.whiplashmerch.com/api/v2/shipping_methods/{id} HTTP/1.1
Host: staging.whiplashmerch.com

Accept: application/json

```

```javascript
var headers = {
  'Accept':'application/json'

};

$.ajax({
  url: '://staging.whiplashmerch.com/api/v2/shipping_methods/{id}',
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
  'Accept':'application/json'

};

fetch('://staging.whiplashmerch.com/api/v2/shipping_methods/{id}',
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
  'Accept' => 'application/json'
}

result = RestClient.delete '://staging.whiplashmerch.com/api/v2/shipping_methods/{id}', params: {
  }, headers: headers

p JSON.parse(result)
```

```python
import requests
headers = {
  'Accept': 'application/json'
}

r = requests.delete('://staging.whiplashmerch.com/api/v2/shipping_methods/{id}', params={

}, headers = headers)

print r.json()
```

```java
URL obj = new URL("://staging.whiplashmerch.com/api/v2/shipping_methods/{id}");
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

`DELETE /api/v2/shipping_methods/{id}`

*Destroy a shipping_method*

Destroy a shipping_method

### Parameters

Parameter|In|Type|Required|Description
---|---|---|---|---|
id|path|integer|true|No description


### Responses

Status|Meaning|Description
---|---|---|
200|[OK](https://tools.ietf.org/html/rfc7231#section-6.3.1)|Destroy a shipping_method
401|[Unauthorized](https://tools.ietf.org/html/rfc7235#section-3.1)|No description
403|[Forbidden](https://tools.ietf.org/html/rfc7231#section-6.5.3)|No description
422|[Unprocessable Entity](https://tools.ietf.org/html/rfc2518#section-10.3)|No description

> Example responses

```json
{
  "id": 0,
  "carrier": "string",
  "service": "string",
  "description": "string",
  "international": true,
  "active": true,
  "flat_rate": true,
  "expedited": true,
  "origins": "string",
  "extended_description": "string",
  "created_at": "2017-06-19T15:15:48Z",
  "updated_at": "2017-06-19T15:15:48Z"
}
```
```json
{
  "message": "string"
}
```
```json
{
  "message": "string"
}
```
```json
{
  "message": "string"
}
```
<aside class="success">
This operation does not require authentication
</aside>



