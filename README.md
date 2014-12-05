website-mobile-preview
======================

# Features

* Currently supports iPhone 6.
* 3 different perspectives - front, left, and right facing.
* Choose from the black, white, and gold versions.
* Easy jQuery-like initialization.
* Scrollbars modified for webkit to resemble track and thumb of iPhone 6
* Coded in vanilla Javascript, no library dependencies

# Usage

Place the script and images on your server.

Include the script.

```html
<script type="text/javascript" src="biomp.js"></script>
```

Create a div element, which will contain the preview.

```html
<div id="preview"></div>
```

Initialize a new bioMp object using the div.

*Vanilla JavaScript*

```javascript
bioMp(document.getElementById('preview'));
```

*jQuery*

```javascript
bioMp($('#preview'));
```

You must include options such as an image and viewing perspective for the preview to show correctly.  This is shown in the next section.

# Options

All options must be added to the init function as an object.

Name | Type | Default | Description
-----|------|---------|------------
**url** | string | blank | URL of the web page to preview.
**view** | string | front | The perspective of the phone.  Possible values are **front**, **left**, and **right**.
**image** | string | blank | URL of the image to use for the phone. A total of 9 images are included with this script.
**scale** | float | 1 | Resize the phone preview by a multiplier value. For instance, a value of 1 is full size, while 0.5 would half the size. If this option is set, both width and height options are ignored.
**width** | integer | 428 | The width of the phone in pixels. If this option is set, the height option is automatically set to proportion. If scale is not set, it will be automatically set to proportion as well.
**height** | integer | 889 | The height of the phone in pixels. If this option is set, both the scale and width options are ignored and automatically set to proportion.

For example, to create a left facing preview for http://beeker.io on the gold iPhone, you would initiate the preview div in the usage example with these options.

```javascript
bioMp(document.getElementById('preview'), {
    url: 'http://beeker.io',
    view: 'left',
    image: 'images/iphone6_side_left_gold.png'
});
```

# Credits

Thank you to JustD for the images of the iPhone 6.  You can find his work [here on Behanced](https://www.behance.net/justd).

# License

MIT license, feel free to use however you wish!

Created by [beeker.io](http://beeker.io/display-website-in-iphone-html-css-javascript)