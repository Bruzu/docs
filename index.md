---
title: Simple Image API
layout: default
nav_order: 1 
---

# Simple API
{: .fs-9 }

Bruzu Image API allows you to create dynamic images using nothing more than a URL string. To see it in action, just paste this URL into your browser's address bar:

```
https://img.bruzu.com/?template=9&middle.text=Dynamic%20text
```

Now try changing the text from "Dynamic text" to your name. 

{: .fs-6 .fw-300 }

A very simple yet powerful image generation API. The Bruzu Image API returns an image in response to a URL GET request. 

The API can generate any kind of image, from Social Media or Open Graph to QR codes and Personalized Greetings. 

All the information about the image that you want, such as template, text, color, size and other used images, are part of the URL. 


To make the simplest image possible, all your URL needs to specify is the template id, and properties of elements used in that template. 

You can download the image by opening the URL directly in your browser, or point to it with an <img> tag in your web page. For example, follow this link for a quote image:  

https://img.bruzu.com/?template=7&middle.text=Simple+text+here&bottom.text=footer

All URLs start with https://img.bruzu.com/? followed by the parameters that specify image data and appearance. Parameters are `objectName.propertyName=propertyValue`  pairs, separated by an ampersand character `(&)`, and parameters can be in any order, after the `?`. You can specify as many additional parameters as the template supports.


[Live demo](https://bruzu.com/){: .btn .btn-primary .fs-5 .mb-4 .mb-md-0 .mr-2 }
[Get an API Key](https://bruzu.com){: .btn .fs-5 .mb-4 .mb-md-0 }
<hr>

The API to automatically generate high quality images.

- API that can be used anywhere.
- Very simple to understand.

<hr>

<div class="code-example flex-justify-between" markdown="1">
<img src="https://img.bruzu.com/?template=9&middle.text=So%20simple,%20sounds%20illegal&backgroundImage.src=https://source.unsplash.com/rTZW4f02zY8/500x500"><br />
[Edit it on live demo](https://bruzu.com/?template=9&middle.text=So%20simple,%20sounds%20illegal&backgroundImage.src=https://source.unsplash.com/rTZW4f02zY8/500x500){: .btn }

</div>
```html
<img src="https://img.bruzu.com/?template=9&middle.text=So%20simple,%20sounds%20illegal&backgroundImage.src=https://source.unsplash.com/rTZW4f02zY8/500x500">
```
