---
layout: page
title: Using the API
permalink: /getting-started/using-the-api/
parent: Getting started
nav_order: 1
---
# Using the Bruzu Image API
{: .no_toc }
{: .fs-9 }

Generate images Using simple but powerfull API.
{: .fs-6 .fw-300 }

[Live demo](https://bruzu.com/){: .btn .btn-primary .fs-5 .mb-4 .mb-md-0 .mr-2 }
[Get an API Key](https://bruzu.com){: .btn .fs-5 .mb-4 .mb-md-0 }

<hr>

Table of contents
{: .text-delta }
- TOC
{:toc}

<hr>

## Authentication
(Coming soon)

- API Key.

## Creating an image

To generate an image, make an HTTP request to the API.

<pre class="http-method fs-4">
  <span>get</span> https://img.bruzu.com<b>/?template=...</b>
</pre>

### Parameters

The create image endpoint accepts the following parameters.

| Name        | Type          | Description |
|:-------------|:------------------|:------|
| **template**<span class="text-red-200">*</span>           | `String`  | This is the unique template id |


### objectName.propertyName=propertyValue

API support variables in form of {% raw %} objectName.propertyName=Value {% endraw %}.

The object (element) value gets replaced with the passed value like while creating your image.

### Example
This image was generated with a template.

```javascript
https://img.bruzu.com/?template=15&top.text=Reminder&middle.text=This%2520too%2520shall%2520pass&bottom.text=OK
```
<img src="https://img.bruzu.com/?template=15&top.text=Reminder&middle.text=This%2520too%2520shall%2520pass&bottom.text=OK">

<hr>

### Example responses
```
STATUS: 201 CREATED
```

```javascript
BINARY IMAGE DATA
```

```
STATUS: 400 BAD REQUEST
```

```javascript
{
    "error": "Param template is missing"
}
```

```
STATUS: 429 TOO MANY REQUESTS
```

```javascript
{
    "error": "Plan limit exceeded",
    "statusCode": 429,
    "message": "You've used X of your N request quota. Upgrade via the Dashboard: https://bruzu.com"
}
```

<hr>

### File formats

The API supports `png` for now. you'll get back a png by default.


### Query parameters

Query parameters can be added to the URL to adjust your image.

| Name        | Type          | Description |
|:-------------|:------------------|:------|
| **height** | `Integer` | The height of the image. Maximum `2000`. |
| **width**  | `Integer`  | The width of the image. Maximum `2000`. |
| **zoom**   | `Integer` | Set the zoom/scale of output image.  |
| **download**     | `Integer` | Set `download=1` and the image will be served as a downloadable attachment. |

<hr>
