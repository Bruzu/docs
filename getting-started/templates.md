---
layout: page
title: Image Templates
permalink: /getting-started/templates/
description: >-
  Create re-usable templates using a simple designer.
parent: Getting started
nav_order: 2
---
# Image Templates
{: .no_toc }
{: .fs-9 }

Create re-usable templates to make image generation easy.
{: .fs-6 .fw-300 }

[Get an API Key](https://bruzu.com){: .btn .btn-blue .fs-5 .mb-4 .mb-md-0 }

<hr>

Table of contents
{: .text-delta }
- TOC
{:toc}

<hr>

## What are Templates?

A template can be designed to includes **variables** in API call to
image creation.

### Variables
API support variables in form of {% raw %}
`objectName.propertyName=Value` {% endraw %}.

The object (element) value gets replaced with the passed value like
while creating your image.

### Common usecases
- Create a reusable template, then pass variables to it to generate
unique images.
- Create images using a `GET` request.
- Useful for social sharing images.

### Example
This image was generated with a template.

```javascript
https://img.bruzu.com/?template=15&top.text=Reminder&middle.text=This%2520too%2520shall%2520pass&bottom.text=OK
```
<img src="https://img.bruzu.com/?template=15&top.text=Reminder&middle.text=This%2520too%2520shall%2520pass&bottom.text=OK">
