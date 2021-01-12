---
layout: page
title: Curl
parent: Example code
permalink: /example-code/curl/
description: >-
  Convert URL string to an image with Curl + the Bruzu Image
  API.
---
# Curl
{: .no_toc }
{: .fs-9 }

Generate images from your terminal with cURL.
{: .fs-4 .fw-300 }

[Live demo](https://bruzu.com/){: .btn .btn-primary .fs-5 .mb-4 .mb-md-0 .mr-2 }
[Get an API Key](https://bruzu.com/){: .btn .fs-5 .mb-4 .mb-md-0 }
<hr>

Table of contents
{: .text-delta }
- TOC
{:toc}

## Generate an image with cURL

Run this command in your terminal to generate an image using the API.

For more details on how this works, see [Creating an image](/getting-started/using-the-api#creating-an-image).

```ruby
# Replace UserID and APIKey with your credentials from the dashboard https://htmlcsstoimage.com/dashboard
curl -X GET https://img.bruzu.com \
     -d apiKey=YOUR_API_KEY \
     -d template=TEMPLATE_ID \
     .....OTHER_PARAMETERS.... \ 
     -o "output.png"
```

## Response

The API will return an image. Open the "output.png" to check results.

{% include code_footer.md version=3 %}
