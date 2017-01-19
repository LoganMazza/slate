---
title: EchidnAPI

language_tabs:
  - shell
  - ruby
  - python
  - javascript

toc_footers:
  - <a href='https://github.com/LoganMazza'>Modified by Logan Mazza</a>
  - <a href='https://github.com/tripit/slate'>Documentation Powered by Slate</a>
  - <a href='#'>Sign Up for a Developer Key</a>

includes:
  - errors

search: true
---

# Introduction

Welcome to EchidnAPI! You can use my API to access EchidnAPI endpoints, which can get information on various echidnas.

Echidnas are monotremes, which make them, along with fellow monotremes the platypus, unique among other mammals in the world in that they lay eggs and lack many of the traditional "mammal" characteristics. 

There are language bindings in JS, Shell, Ruby, and Python! You can view code examples in the dark area to the right, and you can switch the programming language of the examples with the tabs at the top right.

# Authentication

> To authorize, use this code:

```ruby
require 'echid'

api = EchidnAPI::APIClient.authorize!('grrgrr')
```

```python
import echid

api = echid.authorize('grrgrr')
```

```shell
# With shell, you can just pass the correct header with each request
curl "api_endpoint_here"
  -H "Authorization: grrgrr"
```

```javascript
const echid = require('echid');

let api = echid.authorize('grrgrr');
```

> Make sure to replace `grrgrr` with your API key.

EchidnAPI uses API keys to allow access to the API. You can register a new EchidnAPI key at our [developer portal](http://example.com/developers).

EchidnAPI expects for the API key to be included in all API requests to the server in a header that looks like the following:

`Authorization: grrgrr`

<aside class="notice">
You must replace <code>grrgrr</code> with your personal API key.
</aside>

# Echidnas

## Get All Echidnas

```ruby
require 'echid'

api = EchidnAPI::APIClient.authorize!('grrgrr')
api.echidnas.get
```

```python
import echid

api = echid.authorize('grrgrr')
api.echidnas.get()
```

```shell
curl "http://example.com/api/echidnas"
  -H "Authorization: grrgrr"
```

```javascript
const echid = require('echid');

let api = echid.authorize('grrgrr');
let echidnas = api.echidnas.get();
```

> The above command returns JSON structured like this:

```json
[
  {
    "id": 1,
    "name": "Knuckles",
    "breed": "unknown",
    "weirdness": 8,
    "has_knuckles": 1
  },
  {
    "id": 2,
    "name": "Pokey",
    "breed": "short-beaked",
    "weirdness": 10,
    "has_knuckles": 0
  }
]
```

This endpoint retrieves all echidnas currently in the database.

### HTTP Request

`GET http://example.com/api/echidnas`

### Query Parameters

Parameter | Default | Description
--------- | ------- | -----------
include_monotremes | false | If set to true, the result will also include platypi.
captive | true | If set to false, the result will include echidnas and/or platypi that have already been released.

<aside class="success">
Remember — echidnas will burrow when threatened, so make sure you authenticate correctly!
</aside>

## Get a Specific Echidna

```ruby
require 'echid'

api = EchidnAPI::APIClient.authorize!('grrgrr')
api.echidnas.get(2)
```

```python
import echid

api = echid.authorize('grrgrr')
api.echidnas.get(2)
```

```shell
curl "http://example.com/api/echidnas/2"
  -H "Authorization: grrgrr"
```

```javascript
const echid = require('echid');

let api = echid.authorize('grrgrr');
let pokey = api.echidnas.get();
```

> The above command returns JSON structured like this:

```json
{
  "id": 2,
  "name": "Pokey",
  "breed": "short-beaked",
  "weirdness": 10,
  "has_knuckles": 0
}
```

This endpoint retrieves a specific echidna from the database.

### HTTP Request

`GET http://example.com/echidnas/<ID>`

### URL Parameters

Parameter | Description
--------- | -----------
ID | The ID of the echidna to retrieve

