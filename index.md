---
title: Image Generation API
layout: default
nav_order: 1 
---

# Image Generation API
{: .fs-9 }


Bruzu Image Generation API returns an image in response to a Query String.
{: .fs-6 .fw-300 }


To see it in action, just paste this URL into your browser's address bar:

```
https://img.bruzu.com/?a.text=Dynamic
```

Now try changing the text from "Dynamic" to your name or anything. 

The API can generate any kind of image, from Social Media or Open Graph to Personalized Greetings. 

All the information about the image that you want, such as text, color, size and other used images, are part of the URL. 

You can download the image by opening the URL directly in your browser, or point to it with an `img` tag in your web page.


# API URL structure
{: .fs-9 }

All URLs start with `https://img.bruzu.com/?` followed by the parameters that specify image data and appearance. 

Parameters are in `rootPropertyName=propertyValue` and `elementName.propertyName=propertyValue` pairs, separated by an ampersand character `(&)`. Parameters can be in any order. 

Element names can vary form `a` to `z`, You can specify many additional elements with properties.

 For example, there are two text elements ( `a` and `b` ) in this quote image link:  

```
https://img.bruzu.com/
?backgroundImage=https://source.unsplash.com/U-Kty6HxcQc/500x500
&a.text=If you must pivot your company, take both feet off the ground, and jump.
&a.color=white
&a.fontFamily=Poppins
&a.fontWeight=800
&a.width=450
&b.text= @naval
&b.width=450
&b.top=480
&b.originY=bottom
&b.color=white
&b.fontFamily=Playfair Display
&b.fontSize=30
```

<div class="code-example flex-justify-between" markdown="1">
<img src="https://img.bruzu.com/?backgroundImage=https%3A%2F%2Fsource.unsplash.com%2FU-Kty6HxcQc%2F500x500&a.text=If%20you%20must%20pivot%20your%20company%2C%20take%20both%20feet%20off%20the%20ground%2C%20and%20jump.&a.color=white&a.fontFamily=Poppins&a.fontWeight=800&a.width=450&b.text=%40naval&b.width=450&b.top=480&b.originY=bottom&b.color=white&b.fontFamily=Playfair%20Display&b.fontSize=30"><br />
[Edit it on live demo](https://bruzu.com/?backgroundImage=https%3A%2F%2Fsource.unsplash.com%2FU-Kty6HxcQc%2F500x500&a.text=If%20you%20must%20pivot%20your%20company%2C%20take%20both%20feet%20off%20the%20ground%2C%20and%20jump.&a.color=white&a.fontFamily=Poppins&a.fontWeight=800&a.width=450&b.text=%40naval&b.width=450&b.top=480&b.originY=bottom&b.color=white&b.fontFamily=Playfair%20Display&b.fontSize=30){: .btn }

</div>

[Create a new design](https://design.bruzu.com/){: .btn .btn-primary .fs-5 .mb-4 .mb-md-0 .mr-2 }
[Get an API Key](https://bruzu.com){: .btn .fs-5 .mb-4 .mb-md-0 }
<hr>

The API to automatically generate high quality images.

- API that can be used anywhere from webpages to integration into automation tools.
- Very simple to understand and Easy to use.

<hr>
