---
title: Inrō API v0.0.1
language_tabs:
  - ruby: Ruby
  - python: Python
language_clients:
  - ruby: ""
  - python: ""
toc_footers: []
includes: []
search: true
highlight_theme: darkula
headingLevel: 2

---

<!-- Generator: Widdershins v4.0.1 -->

<h1 id="inr-api">Inrō API v0.0.1</h1>

> Scroll down for code samples, example requests and responses. Select a language for code samples from the tabs above or the mobile navigation menu.

Base URLs:

* <a href="//example.org">//example.org</a>

<h1 id="inr-api-me">me</h1>

Operations about mes

## Get information about the current organization

<a id="opIdgetApiV1Me"></a>

> Code samples

```ruby
require 'rest-client'
require 'json'

result = RestClient.get '/example.org/api/v1/me',
  params: {
  }

p JSON.parse(result)

```

```python
import requests

r = requests.get('/example.org/api/v1/me')

print(r.json())

```

`GET /api/v1/me`

Current organization is the owner of the `access_token` you use in the request.

<h3 id="get-information-about-the-current-organization-responses">Responses</h3>

|Status|Meaning|Description|Schema|
|---|---|---|---|
|200|[OK](https://tools.ietf.org/html/rfc7231#section-6.3.1)|Get information about the current organization|None|

<aside class="success">
This operation does not require authentication
</aside>

<h1 id="inr-api-contacts">contacts</h1>

Operations about contacts

## getApiV1Contacts

<a id="opIdgetApiV1Contacts"></a>

> Code samples

```ruby
require 'rest-client'
require 'json'

result = RestClient.get '/example.org/api/v1/contacts',
  params: {
  }

p JSON.parse(result)

```

```python
import requests

r = requests.get('/example.org/api/v1/contacts')

print(r.json())

```

`GET /api/v1/contacts`

List contacts

<h3 id="getapiv1contacts-parameters">Parameters</h3>

|Name|In|Type|Required|Description|
|---|---|---|---|---|
|page|query|integer(int32)|false|Page offset to fetch.|
|per_page|query|integer(int32)|false|Number of results to return per page.|
|offset|query|integer(int32)|false|Pad a number of results.|
|order_direction|query|string|false|Order direction|
|order_column|query|string|false|Order column|

<h3 id="getapiv1contacts-responses">Responses</h3>

|Status|Meaning|Description|Schema|
|---|---|---|---|
|200|[OK](https://tools.ietf.org/html/rfc7231#section-6.3.1)|List contacts|None|

<aside class="success">
This operation does not require authentication
</aside>

## getApiV1ContactsSearch

<a id="opIdgetApiV1ContactsSearch"></a>

> Code samples

```ruby
require 'rest-client'
require 'json'

result = RestClient.get '/example.org/api/v1/contacts/search',
  params: {
  }

p JSON.parse(result)

```

```python
import requests

r = requests.get('/example.org/api/v1/contacts/search')

print(r.json())

```

`GET /api/v1/contacts/search`

Search contacts

<h3 id="getapiv1contactssearch-parameters">Parameters</h3>

|Name|In|Type|Required|Description|
|---|---|---|---|---|
|query|query|string|false|Search query|
|page|query|integer(int32)|false|Page offset to fetch.|
|per_page|query|integer(int32)|false|Number of results to return per page.|
|offset|query|integer(int32)|false|Pad a number of results.|
|order_direction|query|string|false|Order direction|
|order_column|query|string|false|Order column|

<h3 id="getapiv1contactssearch-responses">Responses</h3>

|Status|Meaning|Description|Schema|
|---|---|---|---|
|200|[OK](https://tools.ietf.org/html/rfc7231#section-6.3.1)|Search contacts|None|

<aside class="success">
This operation does not require authentication
</aside>

## putApiV1ContactsId

<a id="opIdputApiV1ContactsId"></a>

> Code samples

```ruby
require 'rest-client'
require 'json'

headers = {
  'Content-Type' => 'application/json'
}

result = RestClient.put '/example.org/api/v1/contacts/{id}',
  params: {
  }, headers: headers

p JSON.parse(result)

```

```python
import requests
headers = {
  'Content-Type': 'application/json'
}

r = requests.put('/example.org/api/v1/contacts/{id}', headers = headers)

print(r.json())

```

`PUT /api/v1/contacts/{id}`

Update a contact (RESTFUL)

> Body parameter

```json
{
  "contact": {
    "email": "string",
    "phone": "string",
    "language": "string"
  }
}
```

<h3 id="putapiv1contactsid-parameters">Parameters</h3>

|Name|In|Type|Required|Description|
|---|---|---|---|---|
|id|path|integer(int32)|true|Contact ID|
|body|body|[putApiV1ContactsId](#schemaputapiv1contactsid)|true|none|

<h3 id="putapiv1contactsid-responses">Responses</h3>

|Status|Meaning|Description|Schema|
|---|---|---|---|
|200|[OK](https://tools.ietf.org/html/rfc7231#section-6.3.1)|Update a contact (RESTFUL)|None|

<aside class="success">
This operation does not require authentication
</aside>

<h1 id="inr-api-contact">contact</h1>

Operations about contacts

## getApiV1Contact

<a id="opIdgetApiV1Contact"></a>

> Code samples

```ruby
require 'rest-client'
require 'json'

result = RestClient.get '/example.org/api/v1/contact',
  params: {
  }

p JSON.parse(result)

```

```python
import requests

r = requests.get('/example.org/api/v1/contact')

print(r.json())

```

`GET /api/v1/contact`

Get a contact

<h3 id="getapiv1contact-parameters">Parameters</h3>

|Name|In|Type|Required|Description|
|---|---|---|---|---|
|id|query|integer(int32)|false|Contact ID|
|username|query|string|false|Contact username|
|email|query|string|false|Contact email|

<h3 id="getapiv1contact-responses">Responses</h3>

|Status|Meaning|Description|Schema|
|---|---|---|---|
|200|[OK](https://tools.ietf.org/html/rfc7231#section-6.3.1)|Get a contact|None|

<aside class="success">
This operation does not require authentication
</aside>

## putApiV1Contact

<a id="opIdputApiV1Contact"></a>

> Code samples

```ruby
require 'rest-client'
require 'json'

headers = {
  'Content-Type' => 'application/json'
}

result = RestClient.put '/example.org/api/v1/contact',
  params: {
  }, headers: headers

p JSON.parse(result)

```

```python
import requests
headers = {
  'Content-Type': 'application/json'
}

r = requests.put('/example.org/api/v1/contact', headers = headers)

print(r.json())

```

`PUT /api/v1/contact`

Update a contact (NON RESTFUL)

> Body parameter

```json
{
  "id": 0,
  "username": "string",
  "email": "string",
  "contact": {
    "email": "string",
    "phone": "string",
    "language": "string"
  }
}
```

<h3 id="putapiv1contact-parameters">Parameters</h3>

|Name|In|Type|Required|Description|
|---|---|---|---|---|
|body|body|[putApiV1Contact](#schemaputapiv1contact)|true|none|

<h3 id="putapiv1contact-responses">Responses</h3>

|Status|Meaning|Description|Schema|
|---|---|---|---|
|200|[OK](https://tools.ietf.org/html/rfc7231#section-6.3.1)|Update a contact (NON RESTFUL)|None|

<aside class="success">
This operation does not require authentication
</aside>

<h1 id="inr-api-folders">folders</h1>

Operations about folders

## getApiV1Folders

<a id="opIdgetApiV1Folders"></a>

> Code samples

```ruby
require 'rest-client'
require 'json'

result = RestClient.get '/example.org/api/v1/folders',
  params: {
  }

p JSON.parse(result)

```

```python
import requests

r = requests.get('/example.org/api/v1/folders')

print(r.json())

```

`GET /api/v1/folders`

List folders

<h3 id="getapiv1folders-parameters">Parameters</h3>

|Name|In|Type|Required|Description|
|---|---|---|---|---|
|page|query|integer(int32)|false|Page offset to fetch.|
|per_page|query|integer(int32)|false|Number of results to return per page.|
|offset|query|integer(int32)|false|Pad a number of results.|

<h3 id="getapiv1folders-responses">Responses</h3>

|Status|Meaning|Description|Schema|
|---|---|---|---|
|200|[OK](https://tools.ietf.org/html/rfc7231#section-6.3.1)|List folders|None|

<aside class="success">
This operation does not require authentication
</aside>

<h1 id="inr-api-contact_properties">contact_properties</h1>

Operations about contact_properties

## getApiV1ContactProperties

<a id="opIdgetApiV1ContactProperties"></a>

> Code samples

```ruby
require 'rest-client'
require 'json'

result = RestClient.get '/example.org/api/v1/contact_properties',
  params: {
  }

p JSON.parse(result)

```

```python
import requests

r = requests.get('/example.org/api/v1/contact_properties')

print(r.json())

```

`GET /api/v1/contact_properties`

List contact properties

<h3 id="getapiv1contactproperties-parameters">Parameters</h3>

|Name|In|Type|Required|Description|
|---|---|---|---|---|
|page|query|integer(int32)|false|Page offset to fetch.|
|per_page|query|integer(int32)|false|Number of results to return per page.|
|offset|query|integer(int32)|false|Pad a number of results.|

<h3 id="getapiv1contactproperties-responses">Responses</h3>

|Status|Meaning|Description|Schema|
|---|---|---|---|
|200|[OK](https://tools.ietf.org/html/rfc7231#section-6.3.1)|List contact properties|None|

<aside class="success">
This operation does not require authentication
</aside>

# Schemas

<h2 id="tocS_PublicApi_Entities_ContactEntity">PublicApi_Entities_ContactEntity</h2>
<!-- backwards compatibility -->
<a id="schemapublicapi_entities_contactentity"></a>
<a id="schema_PublicApi_Entities_ContactEntity"></a>
<a id="tocSpublicapi_entities_contactentity"></a>
<a id="tocspublicapi_entities_contactentity"></a>

```json
{
  "id": "string",
  "name": "string",
  "username": "string",
  "instagram_url": "string",
  "profile_picture": "string",
  "status": "string",
  "notes": "string",
  "is_follower": "string",
  "email": "string",
  "real_name": "string",
  "phone": "string",
  "language": "string",
  "follower_count": "string",
  "follower_growth": "string",
  "bio": "string",
  "website": "string",
  "created_at": "string",
  "updated_at": "string",
  "custom_properties": "string",
  "folders": {
    "id": "string",
    "name": "string"
  },
  "last_messages": {
    "content": "string",
    "received_at": "string",
    "received": "string"
  },
  "last_comments": {
    "text": "string",
    "received_at": "string"
  },
  "last_mentions": {
    "text": "string",
    "received_at": "string"
  }
}

```

### Properties

|Name|Type|Required|Restrictions|Description|
|---|---|---|---|---|
|id|string|false|none|none|
|name|string|false|none|none|
|username|string|false|none|none|
|instagram_url|string|false|none|none|
|profile_picture|string|false|none|none|
|status|string|false|none|none|
|notes|string|false|none|none|
|is_follower|string|false|none|none|
|email|string|false|none|none|
|real_name|string|false|none|none|
|phone|string|false|none|none|
|language|string|false|none|none|
|follower_count|string|false|none|none|
|follower_growth|string|false|none|none|
|bio|string|false|none|none|
|website|string|false|none|none|
|created_at|string|false|none|none|
|updated_at|string|false|none|none|
|custom_properties|string|false|none|none|
|folders|[PublicApi_Entities_FolderEntity](#schemapublicapi_entities_folderentity)|false|none|none|
|last_messages|[PublicApi_Entities_MessageEntity](#schemapublicapi_entities_messageentity)|false|none|none|
|last_comments|[PublicApi_Entities_CommentEntity](#schemapublicapi_entities_commententity)|false|none|none|
|last_mentions|[PublicApi_Entities_MentionEntity](#schemapublicapi_entities_mentionentity)|false|none|none|

<h2 id="tocS_PublicApi_Entities_FolderEntity">PublicApi_Entities_FolderEntity</h2>
<!-- backwards compatibility -->
<a id="schemapublicapi_entities_folderentity"></a>
<a id="schema_PublicApi_Entities_FolderEntity"></a>
<a id="tocSpublicapi_entities_folderentity"></a>
<a id="tocspublicapi_entities_folderentity"></a>

```json
{
  "id": "string",
  "name": "string"
}

```

### Properties

|Name|Type|Required|Restrictions|Description|
|---|---|---|---|---|
|id|string|false|none|none|
|name|string|false|none|none|

<h2 id="tocS_PublicApi_Entities_MessageEntity">PublicApi_Entities_MessageEntity</h2>
<!-- backwards compatibility -->
<a id="schemapublicapi_entities_messageentity"></a>
<a id="schema_PublicApi_Entities_MessageEntity"></a>
<a id="tocSpublicapi_entities_messageentity"></a>
<a id="tocspublicapi_entities_messageentity"></a>

```json
{
  "content": "string",
  "received_at": "string",
  "received": "string"
}

```

### Properties

|Name|Type|Required|Restrictions|Description|
|---|---|---|---|---|
|content|string|false|none|none|
|received_at|string|false|none|none|
|received|string|false|none|none|

<h2 id="tocS_PublicApi_Entities_CommentEntity">PublicApi_Entities_CommentEntity</h2>
<!-- backwards compatibility -->
<a id="schemapublicapi_entities_commententity"></a>
<a id="schema_PublicApi_Entities_CommentEntity"></a>
<a id="tocSpublicapi_entities_commententity"></a>
<a id="tocspublicapi_entities_commententity"></a>

```json
{
  "text": "string",
  "received_at": "string"
}

```

### Properties

|Name|Type|Required|Restrictions|Description|
|---|---|---|---|---|
|text|string|false|none|none|
|received_at|string|false|none|none|

<h2 id="tocS_PublicApi_Entities_MentionEntity">PublicApi_Entities_MentionEntity</h2>
<!-- backwards compatibility -->
<a id="schemapublicapi_entities_mentionentity"></a>
<a id="schema_PublicApi_Entities_MentionEntity"></a>
<a id="tocSpublicapi_entities_mentionentity"></a>
<a id="tocspublicapi_entities_mentionentity"></a>

```json
{
  "text": "string",
  "received_at": "string"
}

```

### Properties

|Name|Type|Required|Restrictions|Description|
|---|---|---|---|---|
|text|string|false|none|none|
|received_at|string|false|none|none|

<h2 id="tocS_PublicApi_Entities_ContactPropertyEntity">PublicApi_Entities_ContactPropertyEntity</h2>
<!-- backwards compatibility -->
<a id="schemapublicapi_entities_contactpropertyentity"></a>
<a id="schema_PublicApi_Entities_ContactPropertyEntity"></a>
<a id="tocSpublicapi_entities_contactpropertyentity"></a>
<a id="tocspublicapi_entities_contactpropertyentity"></a>

```json
{
  "slug": "string",
  "title": "string",
  "property_type": "string"
}

```

### Properties

|Name|Type|Required|Restrictions|Description|
|---|---|---|---|---|
|slug|string|false|none|none|
|title|string|false|none|none|
|property_type|string|false|none|none|

<h2 id="tocS_putApiV1ContactsId">putApiV1ContactsId</h2>
<!-- backwards compatibility -->
<a id="schemaputapiv1contactsid"></a>
<a id="schema_putApiV1ContactsId"></a>
<a id="tocSputapiv1contactsid"></a>
<a id="tocsputapiv1contactsid"></a>

```json
{
  "contact": {
    "email": "string",
    "phone": "string",
    "language": "string"
  }
}

```

Update a contact (RESTFUL)

### Properties

|Name|Type|Required|Restrictions|Description|
|---|---|---|---|---|
|contact|object|true|none|none|
|» email|string|false|none|Contact email|
|» phone|string|false|none|Contact phone|
|» language|string|false|none|Contact language|

<h2 id="tocS_putApiV1Contact">putApiV1Contact</h2>
<!-- backwards compatibility -->
<a id="schemaputapiv1contact"></a>
<a id="schema_putApiV1Contact"></a>
<a id="tocSputapiv1contact"></a>
<a id="tocsputapiv1contact"></a>

```json
{
  "id": 0,
  "username": "string",
  "email": "string",
  "contact": {
    "email": "string",
    "phone": "string",
    "language": "string"
  }
}

```

Update a contact (NON RESTFUL)

### Properties

|Name|Type|Required|Restrictions|Description|
|---|---|---|---|---|
|id|integer(int32)|false|none|Contact ID|
|username|string|false|none|Contact username|
|email|string|false|none|Contact email|
|contact|object|true|none|none|
|» email|string|false|none|Contact email|
|» phone|string|false|none|Contact phone|
|» language|string|false|none|Contact language|
