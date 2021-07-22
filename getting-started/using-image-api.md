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

If you want to remove the watermark from your images, you can get an API key by clicking *Login with Twitter* link on home page. 

- You need to pass the API key same as other parameters. (`apiKey`)
- Keep you API Key secure. If exposed, it could be used to call API using your account.


## Creating an image

To generate an image, make an HTTP request to the API.

<pre class="http-method fs-4">
  <span>GET</span> https://img.bruzu.com<b>/?...</b>
</pre>

### Parameters

The create image endpoint accepts the following parameters.

| Name        | Type          | Description |
|:-------------|:------------------|:------|
| **apiKey**           | `String`  | API key of your account |
| **height** | `Integer` | The height of the image. Maximum `2000`. Default value is `500` |
| **width**  | `Integer`  | The width of the image. Maximum `2000`. Default value is `500` |
| **backgroundColor**  | `String`  |  Background Color of the Image. Default is `none` ( transparent ) |
| **backgroundImage**  | `String`  | Background Image url. |
| **backgroundImage.opacity**  | `Float`  | Opacity or the background image, between 0 and 1. Default value is 1|
| **scale**   | `Integer` | Set the scale of output image.  |
| **download**     | `Integer` | Set `download=1` and the image will be served as a downloadable attachment. |


### Aditional Parameters

Element names can vary form `a` to `z`, You can specify many elements with properties like `a.text` or `b.src` etc.

## Every Type of Element have these properties

| Name        | Type          | Description | Default value |
|:-------------|:------------------|:------|:--------|
| `[a-z]`.**type**           | `String`  | Type of element ( `textbox`, `image`, `rect`, `circle`, `line`, `tringle`) | `textbox`( if `.text` exists ), `image`( if `.src` exists ) |
| `[a-z]`.**angle**           | `Number`  | Angle of rotation of an element (in degrees) | `0`|
| `[a-z]`.**color**           | `String`  | Color of an element. takes css colors, (hax, rgb, rgba or name or color) | `black`|
| `[a-z]`.**backgroundColor**  | `String`  | Background color of an element. takes css colors, (hax, rgb, rgba or name or color) | `transparent`|
| `[a-z]`.**height**           | `Number`  |   Element height   | `(root image height)/2`|
| `[a-z]`.**width**           | `Number`  |   Element width   | `(root image width)/2`|
| `[a-z]`.**originX**           | `String`  |   Horizontal origin of transformation of an element (one of "left", "right", "center")    | `center`|
| `[a-z]`.**originY**           | `String`  |   Vertical origin of transformation of an object (one of "top", "bottom", "center")    | `center`|
| `[a-z]`.**left**           | `Number`  |    Left position of an element. Note that by default it's relative to element center ( This can be changed by changing originX of the element).| `(root image width)/2`|
| `[a-z]`.**top**           | `Number`  |    Top position of an element. Note that by default it's relative to element center. ( This can be changed by changing originY of the element) | `(root image width)/2`|
| `[a-z]`.**opacity**           | `Number`  |    Opacity of an element   | `1`|
| `[a-z]`.**scaleX**           | `Number`  |     Element scale factor (horizontal)    | `1`|
| `[a-z]`.**scaleY**           | `Number`  |     Element scale factor (vertical)   | `1`|
| `[a-z]`.**shadow**           | `String`  |     Shadow color   | `transparent`|
| `[a-z]`.**skewX**           | `Number`  |     Angle of skew on x axes of an element  (in degrees).   | `0`|
| `[a-z]`.**skewY**           | `Number`  |     Angle of skew on y axes of an element (in degrees).   | `0`|
| `[a-z]`.**stroke**           | `String`  |     Element border color   | `transparent`|
| `[a-z]`.**strokeWidth**           | `Number`  |     Width of border.    | `0`|
| `[a-z]`.**flipX**           | `Boolean`  |  When true, an object is rendered as flipped horizontally.  | `false`|
| `[a-z]`.**flipY**           | `Boolean`  |   When true, an object is rendered as flipped vertically.  | `false`|


### Example
This image was generated with a template.

```javascript
https://img.bruzu.com/
?backgroundImage=https://source.unsplash.com/500x500/?gradient
&a.type=rect
&a.originX=left
&a.originY=top
&a.left=73
&a.top=224
&a.width=354
&a.height=51
&a.fill=white
&a.rx=5
&a.ry=5
&b.originX=left
&b.originY=top
&b.left=385.98
&b.top=238.66
&b.width=100
&b.height=100
&b.fill=rgb(0,0,0)
&b.scaleX=0.23
&b.scaleY=0.23
&b.src=https://i.imgur.com/8tNQSOl.png
&c.text=Think! Why?
&c.originX=left
&c.originY=center
&c.left=89.67
&c.top=249.96
&c.width=280
&c.height=22.6
&c.maxHeight=30
&c.fontSize=20
&c.fontWeight=400
&c.fontFamily=Roboto
&c.fontStyle=normal
&c.lineHeight=1.16
```
<img src="https://img.bruzu.com/?backgroundImage=https://source.unsplash.com/500x500/?gradient&a.type=rect&a.originX=left&a.originY=top&a.left=73&a.top=224&a.width=354&a.height=51&a.fill=white&a.rx=5&a.ry=5&b.originX=left&b.originY=top&b.left=385.98&b.top=238.66&b.width=100&b.height=100&b.fill=rgb(0,0,0)&b.scaleX=0.23&b.scaleY=0.23&b.src=https://i.imgur.com/8tNQSOl.png&c.text=Think! Why?&c.originX=left&c.originY=center&c.left=89.67&c.top=249.96&c.width=280&c.height=22.6&c.maxHeight=30&c.fontSize=20&c.fontWeight=400&c.fontFamily=Roboto&c.fontStyle=normal&c.lineHeight=1.16">

<hr>

### Example responses
```
HTTP/1.1 200 OK
Content-Type: image/png

...png document bytes

```

```
STATUS: 400 BAD REQUEST
```

```javascript
{
    "error": "Something is missing"
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



<hr>
