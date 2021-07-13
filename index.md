---
title: Simple Image API
layout: default
nav_order: 1 
---

# Simple Image API
{: .fs-9 }


A very simple yet powerful image generation API. The Bruzu Image API returns an image in response to a URL GET request.
{: .fs-6 .fw-300 }


Bruzu Image API allows you to create dynamic images using nothing more than a URL string. To see it in action, just paste this URL into your browser's address bar:

```
https://img.bruzu.com/ewogICJvYmplY3RzIjogWwoJCXsKCQkJIm5hbWUiOiAibWlkZGxlIiwKCQkJInR5cGUiOiAiVGV4dGJveCIsCgkJCSJ0ZXh0IjogIklmIHlvdSBjYW4gdGhpbmssIHNwZWFrLCBhbmQgd3JpdGUgY29kZSwgeW91IGFyZSBhYnNvbHV0ZWx5IGRlYWRseS4iCgkJfQoJXQp9/?middle.text=Dynamic%20text
```

Now try changing the text from "Dynamic text" to your name. 


The API can generate any kind of image, from Social Media or Open Graph to QR codes and Personalized Greetings. 

All the information about the image that you want, such as template, text, color, size and other used images, are part of the URL. 


To make the simplest image possible, all your URL needs to specify is the template JSON ( base64 encoded ) , and properties of elements used in that template. 

You can download the image by opening the URL directly in your browser, or point to it with an `img` tag in your web page. For example, follow this link for a quote image:  

```
https://img.bruzu.com/ewogICJvYmplY3RzIjogWwoJCXsKCQkJIm5hbWUiOiAibWlkZGxlIiwKCQkJInR5cGUiOiAiVGV4dGJveCIsCgkJCSJ0ZXh0IjogIklmIHlvdSBjYW4gdGhpbmssIHNwZWFrLCBhbmQgd3JpdGUgY29kZSwgeW91IGFyZSBhYnNvbHV0ZWx5IGRlYWRseS4iCgkJfQoJXQp9/?middle.text=Dynamic%20text
```

All URLs start with `https://img.bruzu.com/?` followed by the parameters that specify image data and appearance. Parameters are `objectName.propertyName=propertyValue`  pairs, separated by an ampersand character `(&)`, and parameters can be in any order, after the `?`. You can specify as many additional parameters as the template supports.


[Live demo](https://bruzu.com/){: .btn .btn-primary .fs-5 .mb-4 .mb-md-0 .mr-2 }
[Get an API Key](https://bruzu.com){: .btn .fs-5 .mb-4 .mb-md-0 }
<hr>

The API to automatically generate high quality images.

- API that can be used anywhere.
- Very simple to understand.

<hr>

<div class="code-example flex-justify-between" markdown="1">
<img src="https://img.bruzu.com/ewoJImhlaWdodCI6IDUwMCwKCSJ3aWR0aCI6IDUwMCwKCSJiYWNrZ3JvdW5kSW1hZ2UiOiB7CgkJInR5cGUiOiAiSW1hZ2UiLAoJCSJzcmMiOiAiaHR0cHM6Ly9zb3VyY2UudW5zcGxhc2guY29tL1dXZXNtSEVnWERzLzUwMHg1MDAiCgl9LAoJIm9iamVjdHMiOiBbCgkJewoJCQkibmFtZSI6ICJtaWRkbGUiLAoJCQkidHlwZSI6ICJUZXh0Ym94IiwKCQkJInRleHQiOiAiWW91ck5hbWUiLAoJCQkib3JpZ2luWCI6ICJjZW50ZXIiLAoJCQkib3JpZ2luWSI6ICJjZW50ZXIiLAoJCQkidGV4dEFsaWduIjogImNlbnRlciIsCgkJCSJiYWNrZ3JvdW5kQ29sb3IiOiAicmVkIiwKCQkJImxlZnQiOiAyNDUsCgkJCSJ0b3AiOiAyMDAsCgkJCSJ3aWR0aCI6IDE1MCwKCQkJImhlaWdodCI6IDQ1MCwKCQkJImZpbGwiOiAid2hpdGUiLAoJCQkiZm9udFNpemUiOiAzNSwKCQkJImZvbnRXZWlnaHQiOiAiNDAwIiwKCQkJImZvbnRGYW1pbHkiOiAiRGlkYWN0IEdvdGhpYyIsCgkJCSJmb250U3R5bGUiOiAibm9ybWFsIiwKCQkJImxpbmVIZWlnaHQiOiAwLjkKCQl9CgldCn0=/?middle.text=YourName"><br />
[Edit it on live demo](https://bruzu.com/?json=ewoJImhlaWdodCI6IDUwMCwKCSJ3aWR0aCI6IDUwMCwKCSJiYWNrZ3JvdW5kSW1hZ2UiOiB7CgkJInR5cGUiOiAiSW1hZ2UiLAoJCSJzcmMiOiAiaHR0cHM6Ly9zb3VyY2UudW5zcGxhc2guY29tL1dXZXNtSEVnWERzLzUwMHg1MDAiCgl9LAoJIm9iamVjdHMiOiBbCgkJewoJCQkibmFtZSI6ICJtaWRkbGUiLAoJCQkidHlwZSI6ICJUZXh0Ym94IiwKCQkJInRleHQiOiAiWW91ck5hbWUiLAoJCQkib3JpZ2luWCI6ICJjZW50ZXIiLAoJCQkib3JpZ2luWSI6ICJjZW50ZXIiLAoJCQkidGV4dEFsaWduIjogImNlbnRlciIsCgkJCSJiYWNrZ3JvdW5kQ29sb3IiOiAicmVkIiwKCQkJImxlZnQiOiAyNDUsCgkJCSJ0b3AiOiAyMDAsCgkJCSJ3aWR0aCI6IDE1MCwKCQkJImhlaWdodCI6IDQ1MCwKCQkJImZpbGwiOiAid2hpdGUiLAoJCQkiZm9udFNpemUiOiAzNSwKCQkJImZvbnRXZWlnaHQiOiAiNDAwIiwKCQkJImZvbnRGYW1pbHkiOiAiRGlkYWN0IEdvdGhpYyIsCgkJCSJmb250U3R5bGUiOiAibm9ybWFsIiwKCQkJImxpbmVIZWlnaHQiOiAwLjkKCQl9CgldCn0=&&middle.text=YourName){: .btn }

</div>
```html
<img src="https://img.bruzu.com/?template=9&middle.text=So%20simple,%20sounds%20illegal&backgroundImage.src=https://source.unsplash.com/rTZW4f02zY8/500x500">
```
