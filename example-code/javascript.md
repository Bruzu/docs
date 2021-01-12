---
layout: default
title: JavaScript
parent: Example code
permalink: /example-code/javascript/
description: >-
  Generate an image with Bruzu Image API.
---

## JavaScript example - async/await

If your code supports async/await, we recommend using the axios package.

This example uses the [axios package](https://www.npmjs.com/package/axios). Install with `npm install axios`.

```javascript
const axios = require('axios'); 
const fs = require('fs')

// Replace YOUR_API_KEY and TEMPLATE_ID with proper values

axios.get('https://img.bruzu.com/?template=TEMPLATE_ID&apiKey=YOUR_API_KEY&otherParameters', {responseType: "stream"} )  
.then(response => {  
    // Saving file to working directory  
    response.data.pipe(fs.createWriteStream("output.png"));  
})  
    .catch(error => {  
    console.log(error);  
}); 
```

<hr>

## Plain JavaScript \(Node.js\) example

If you prefer not to install an HTTP library for making the request. This example shows you how to use the API without any dependencies.

```javascript
const http = require('https');
const fs = require('fs');

// Replace YOUR_API_KEY and TEMPLATE_ID with proper values

const file = fs.createWriteStream("output.png");
const request = http.get("https://img.bruzu.com/?template=TEMPLATE_ID&apiKey=YOUR_API_KEY&otherParameters",
    function(response) {
        response.pipe(file);
    })
```

{% include code_footer.md version=1 %}
