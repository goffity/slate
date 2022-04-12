---
title: xopay-line v1.0.0
language_tabs:
  - shell: Shell
  - go: Go
  - java: Java
  - javascript: JavaScript
  - javascript--node: Node.JS
language_clients:
  - javascript: axios
  - java: okhttp
toc_footers: []
includes: []
search: true
highlight_theme: darkula
headingLevel: 2

---

<!-- Generator: Widdershins v4.0.1 -->

<h1 id="xopay-line">xopay-line v1.0.0</h1>

> Scroll down for code samples, example requests and responses. Select a language for code samples from the tabs above or the mobile navigation menu.

Base URLs:

* <a href="http://localhost:3000">http://localhost:3000</a>

# Authentication

* API Key (API-KEY)
    - Parameter Name: **api-key**, in: header. 

<h1 id="xopay-line-players">players</h1>

## post-players

<a id="opIdpost-players"></a>

> Code samples

```shell
curl --request POST \
  --url http://localhost:3000/players \
  --header 'Accept: application/json' \
  --header 'Content-Type: application/json' \
  --header 'api-key: abcd' \
  --data '{"nameTH":"string","nameEN":"string","phone":"string","bankAccName":"string","bankAccNo":"string","bankName":"string","lineUserId":"string","isBonus":true,"agentID":"string","username":"string"}'
```

```go
package main

import (
	"fmt"
	"strings"
	"net/http"
	"io/ioutil"
)

func main() {

	url := "http://localhost:3000/players"

	payload := strings.NewReader("{\"nameTH\":\"string\",\"nameEN\":\"string\",\"phone\":\"string\",\"bankAccName\":\"string\",\"bankAccNo\":\"string\",\"bankName\":\"string\",\"lineUserId\":\"string\",\"isBonus\":true,\"agentID\":\"string\",\"username\":\"string\"}")

	req, _ := http.NewRequest("POST", url, payload)

	req.Header.Add("Content-Type", "application/json")
	req.Header.Add("Accept", "application/json")
	req.Header.Add("api-key", "abcd")

	res, _ := http.DefaultClient.Do(req)

	defer res.Body.Close()
	body, _ := ioutil.ReadAll(res.Body)

	fmt.Println(res)
	fmt.Println(string(body))

}
```

```java
OkHttpClient client = new OkHttpClient();

MediaType mediaType = MediaType.parse("application/json");
RequestBody body = RequestBody.create(mediaType, "{\"nameTH\":\"string\",\"nameEN\":\"string\",\"phone\":\"string\",\"bankAccName\":\"string\",\"bankAccNo\":\"string\",\"bankName\":\"string\",\"lineUserId\":\"string\",\"isBonus\":true,\"agentID\":\"string\",\"username\":\"string\"}");
Request request = new Request.Builder()
  .url("http://localhost:3000/players")
  .post(body)
  .addHeader("Content-Type", "application/json")
  .addHeader("Accept", "application/json")
  .addHeader("api-key", "abcd")
  .build();

Response response = client.newCall(request).execute();
```

```javascript
import axios from "axios";

const options = {
  method: 'POST',
  url: 'http://localhost:3000/players',
  headers: {
    'Content-Type': 'application/json',
    Accept: 'application/json',
    'api-key': 'abcd'
  },
  data: {
    nameTH: 'string',
    nameEN: 'string',
    phone: 'string',
    bankAccName: 'string',
    bankAccNo: 'string',
    bankName: 'string',
    lineUserId: 'string',
    isBonus: true,
    agentID: 'string',
    username: 'string'
  }
};

axios.request(options).then(function (response) {
  console.log(response.data);
}).catch(function (error) {
  console.error(error);
});
```

```javascript--node
const http = require("http");

const options = {
  "method": "POST",
  "hostname": "localhost",
  "port": "3000",
  "path": "/players",
  "headers": {
    "Content-Type": "application/json",
    "Accept": "application/json",
    "api-key": "abcd"
  }
};

const req = http.request(options, function (res) {
  const chunks = [];

  res.on("data", function (chunk) {
    chunks.push(chunk);
  });

  res.on("end", function () {
    const body = Buffer.concat(chunks);
    console.log(body.toString());
  });
});

req.write(JSON.stringify({
  nameTH: 'string',
  nameEN: 'string',
  phone: 'string',
  bankAccName: 'string',
  bankAccNo: 'string',
  bankName: 'string',
  lineUserId: 'string',
  isBonus: true,
  agentID: 'string',
  username: 'string'
}));
req.end();
```

`POST /players`

*Register player*

Register player.

> Body parameter

```json
{
  "nameTH": "string",
  "nameEN": "string",
  "phone": "string",
  "bankAccName": "string",
  "bankAccNo": "string",
  "bankName": "string",
  "lineUserId": "string",
  "isBonus": true,
  "agentID": "string",
  "username": "string"
}
```

<h3 id="post-players-parameters">Parameters</h3>

|Name|In|Type|Required|Description|
|---|---|---|---|---|
|body|body|object|false|none|
|» nameTH|body|string|true|none|
|» nameEN|body|string|true|none|
|» phone|body|string|true|none|
|» bankAccName|body|string|true|none|
|» bankAccNo|body|string|true|none|
|» bankName|body|string|true|none|
|» lineUserId|body|string|true|none|
|» isBonus|body|boolean|true|none|
|» agentID|body|string|true|none|
|» username|body|string|true|none|

> Example responses

> Example response

```json
{
  "code": 200,
  "status": "SUCCESS",
  "message": "OK",
  "display_message": "OK"
}
```

```json
{
  "code": 200,
  "status": "SUCCESS",
  "message": "OK",
  "display_message": "OK"
}
```

```json
{
  "code": 200,
  "status": "SUCCESS",
  "message": "OK",
  "display_message": "OK"
}
```

```json
{
  "code": 200,
  "status": "SUCCESS",
  "message": "OK",
  "display_message": "OK"
}
```

```json
{
  "code": 200,
  "status": "SUCCESS",
  "message": "OK",
  "display_message": "OK"
}
```

<h3 id="post-players-responses">Responses</h3>

|Status|Meaning|Description|Schema|
|---|---|---|---|
|201|[Created](https://tools.ietf.org/html/rfc7231#section-6.3.2)|Example response|Inline|
|400|[Bad Request](https://tools.ietf.org/html/rfc7231#section-6.5.1)|Example response|Inline|
|401|[Unauthorized](https://tools.ietf.org/html/rfc7235#section-3.1)|Example response|Inline|
|403|[Forbidden](https://tools.ietf.org/html/rfc7231#section-6.5.3)|Example response|Inline|
|404|[Not Found](https://tools.ietf.org/html/rfc7231#section-6.5.4)|Example response|Inline|

<h3 id="post-players-responseschema">Response Schema</h3>

Status Code **201**

|Name|Type|Required|Restrictions|Description|
|---|---|---|---|---|
|» code|integer|false|none|none|
|» status|string|false|none|none|
|» message|string|false|none|none|
|» display_message|string|false|none|none|

Status Code **400**

|Name|Type|Required|Restrictions|Description|
|---|---|---|---|---|
|» code|integer|false|none|none|
|» status|string|false|none|none|
|» message|string|false|none|none|
|» display_message|string|false|none|none|

Status Code **401**

|Name|Type|Required|Restrictions|Description|
|---|---|---|---|---|
|» code|integer|false|none|none|
|» status|string|false|none|none|
|» message|string|false|none|none|
|» display_message|string|false|none|none|

Status Code **403**

|Name|Type|Required|Restrictions|Description|
|---|---|---|---|---|
|» code|integer|false|none|none|
|» status|string|false|none|none|
|» message|string|false|none|none|
|» display_message|string|false|none|none|

Status Code **404**

|Name|Type|Required|Restrictions|Description|
|---|---|---|---|---|
|» code|integer|false|none|none|
|» status|string|false|none|none|
|» message|string|false|none|none|
|» display_message|string|false|none|none|

<aside class="warning">
To perform this operation, you must be authenticated by means of one of the following methods:
API-KEY
</aside>

<h1 id="xopay-line-transactions">transactions</h1>

## post-transactions

<a id="opIdpost-transactions"></a>

> Code samples

```shell
curl --request POST \
  --url http://localhost:3000/transactions \
  --header 'api-key: abcd'
```

```go
package main

import (
	"fmt"
	"net/http"
	"io/ioutil"
)

func main() {

	url := "http://localhost:3000/transactions"

	req, _ := http.NewRequest("POST", url, nil)

	req.Header.Add("api-key", "abcd")

	res, _ := http.DefaultClient.Do(req)

	defer res.Body.Close()
	body, _ := ioutil.ReadAll(res.Body)

	fmt.Println(res)
	fmt.Println(string(body))

}
```

```java
OkHttpClient client = new OkHttpClient();

Request request = new Request.Builder()
  .url("http://localhost:3000/transactions")
  .post(null)
  .addHeader("api-key", "abcd")
  .build();

Response response = client.newCall(request).execute();
```

```javascript
import axios from "axios";

const options = {
  method: 'POST',
  url: 'http://localhost:3000/transactions',
  headers: {'api-key': 'abcd'}
};

axios.request(options).then(function (response) {
  console.log(response.data);
}).catch(function (error) {
  console.error(error);
});
```

```javascript--node
const http = require("http");

const options = {
  "method": "POST",
  "hostname": "localhost",
  "port": "3000",
  "path": "/transactions",
  "headers": {
    "api-key": "abcd"
  }
};

const req = http.request(options, function (res) {
  const chunks = [];

  res.on("data", function (chunk) {
    chunks.push(chunk);
  });

  res.on("end", function () {
    const body = Buffer.concat(chunks);
    console.log(body.toString());
  });
});

req.end();
```

`POST /transactions`

*Create transactions*

<h3 id="post-transactions-responses">Responses</h3>

|Status|Meaning|Description|Schema|
|---|---|---|---|
|200|[OK](https://tools.ietf.org/html/rfc7231#section-6.3.1)|OK|None|

<aside class="warning">
To perform this operation, you must be authenticated by means of one of the following methods:
API-KEY
</aside>

<h1 id="xopay-line-issues">issues</h1>

## post-issues

<a id="opIdpost-issues"></a>

> Code samples

```shell
curl --request POST \
  --url http://localhost:3000/issues \
  --header 'api-key: abcd'
```

```go
package main

import (
	"fmt"
	"net/http"
	"io/ioutil"
)

func main() {

	url := "http://localhost:3000/issues"

	req, _ := http.NewRequest("POST", url, nil)

	req.Header.Add("api-key", "abcd")

	res, _ := http.DefaultClient.Do(req)

	defer res.Body.Close()
	body, _ := ioutil.ReadAll(res.Body)

	fmt.Println(res)
	fmt.Println(string(body))

}
```

```java
OkHttpClient client = new OkHttpClient();

Request request = new Request.Builder()
  .url("http://localhost:3000/issues")
  .post(null)
  .addHeader("api-key", "abcd")
  .build();

Response response = client.newCall(request).execute();
```

```javascript
import axios from "axios";

const options = {
  method: 'POST',
  url: 'http://localhost:3000/issues',
  headers: {'api-key': 'abcd'}
};

axios.request(options).then(function (response) {
  console.log(response.data);
}).catch(function (error) {
  console.error(error);
});
```

```javascript--node
const http = require("http");

const options = {
  "method": "POST",
  "hostname": "localhost",
  "port": "3000",
  "path": "/issues",
  "headers": {
    "api-key": "abcd"
  }
};

const req = http.request(options, function (res) {
  const chunks = [];

  res.on("data", function (chunk) {
    chunks.push(chunk);
  });

  res.on("end", function () {
    const body = Buffer.concat(chunks);
    console.log(body.toString());
  });
});

req.end();
```

`POST /issues`

*Create issues*

<h3 id="post-issues-responses">Responses</h3>

|Status|Meaning|Description|Schema|
|---|---|---|---|
|200|[OK](https://tools.ietf.org/html/rfc7231#section-6.3.1)|OK|None|

<aside class="warning">
To perform this operation, you must be authenticated by means of one of the following methods:
API-KEY
</aside>

# Schemas

