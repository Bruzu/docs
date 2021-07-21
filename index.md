---
title: Image Generation API
layout: default
nav_order: 1 
---

# Image Generation API
{: .fs-9 }


A very simple yet powerful image generation API. The Bruzu Image API returns an image in response to a URL GET request.
{: .fs-6 .fw-300 }


Bruzu Image API allows you to create dynamic images using nothing more than a URL string. To see it in action, just paste this URL into your browser's address bar:

```
https://img.bruzu.com/?a.text=Dynamic
```

Now try changing the text from "Dynamic" to your name or anything. 

The API can generate any kind of image, from Social Media or Open Graph to QR codes and Personalized Greetings. 

All the information about the image that you want, such as text, color, size and other used images, are part of the URL. 

You can download the image by opening the URL directly in your browser, or point to it with an `img` tag in your web page. For example, follow this link for a quote image:  

```
https://img.bruzu.com/?backgroundColor=white&a.text=Bruzu&a.textAlign=center&a.fontFamily=Rubik&a.fontSize=120&a.fontWeight=900&a.color=%23D1F93E
```

All URLs start with `https://img.bruzu.com/?` followed by the parameters that specify image data and appearance. Parameters are `objectName.propertyName=propertyValue`  pairs, separated by an ampersand character `(&)`, and parameters can be in any order, after the `?`. You can specify as many additional elements with properties.


[Live demo](https://bruzu.com/){: .btn .btn-primary .fs-5 .mb-4 .mb-md-0 .mr-2 }
[Get an API Key](https://bruzu.com){: .btn .fs-5 .mb-4 .mb-md-0 }
<hr>

The API to automatically generate high quality images.

- API that can be used anywhere.
- Very simple to understand.

<hr>

<div class="code-example flex-justify-between" markdown="1">
<img src="https://img.bruzu.com/?backgroundImage=https%3A%2F%2Fsource.unsplash.com%2FU-Kty6HxcQc%2F500x500&a.text=If%20you%20must%20pivot%20your%20company%2C%20take%20both%20feet%20off%20the%20ground%2C%20and%20jump.&a.color=white&a.fontFamily=Poppins&a.fontWeight=800&a.width=450&b.text=%40naval&b.width=100&b.height=33&b.top=450&b.color=white&b.fontFamily=Playfair%20Display&b.fontSize=30"><br />
[Edit it on live demo](https://bruzu.com/?backgroundImage=https%3A%2F%2Fsource.unsplash.com%2FU-Kty6HxcQc%2F500x500&a.text=If%20you%20must%20pivot%20your%20company%2C%20take%20both%20feet%20off%20the%20ground%2C%20and%20jump.&a.color=white&a.fontFamily=Poppins&a.fontWeight=800&a.width=450&b.text=%40naval&b.width=100&b.height=33&b.top=450&b.color=white&b.fontFamily=Playfair%20Display&b.fontSize=30e){: .btn }

</div>
```html
<img src=" https://img.bruzu.com/?backgroundImage=https://source.unsplash.com/U-Kty6HxcQc/500x500&a.text=If you must pivot your company, take both feet off the ground, and jump.&a.color=white&a.fontFamily=Poppins&a.fontWeight=800&a.width=450&b.text=@naval&b.width=100&b.height=33&b.top=450&b.color=white&b.fontFamily=Playfair Display&b.fontSize=30">
```
