# QRCode.js
QRCode.js is javascript library for making QRCode. QRCode.js supports Cross-browser with HTML5 Canvas and table tag in DOM.
QRCode.js has no dependencies.

## Why this fork?
This fork merges in some fixes. This is mostly created to be used in my project [Chhoto URL](https://github.com/SinTan1729/chhoto-url).
1. Proper Unicode support by @19z.
1. Updated the minified file to fix an issue with string lengths stemming from the minification process.

## Basic Usages
You can load it from a CDN.
```html
<script
src="https://cdn.jsdelivr.net/gh/sintan1729/qrcodejs@0.1.0/qrcode.min.js"
async
></script>
```
Then use it to generate QR codes.
```html
<div id="qrcode"></div>
<script type="text/javascript">
new QRCode(document.getElementById("qrcode"), "http://jindo.dev.naver.com/collie");
</script>
```

or with some options

```html
<div id="qrcode"></div>
<script type="text/javascript">
var qrcode = new QRCode(document.getElementById("qrcode"), {
	text: "http://jindo.dev.naver.com/collie",
	width: 128,
	height: 128,
	colorDark : "#000000",
	colorLight : "#ffffff",
	correctLevel : QRCode.CorrectLevel.H
});
</script>
```

and you can use some methods

```html
qrcode.clear(); // clear the code.
qrcode.makeCode("http://naver.com"); // make another code.
```

## Full UTF-8 encoding support

```html
qrcode.clear(); // clear the code.
qrcode.makeCode("你好 こんにちは 여보세요"); // make another code.
```

## Browser Compatibility
IE6~10, Chrome, Firefox, Safari, Opera, Mobile Safari, Android, Windows Mobile, ETC.

## License
MIT License

## Contact
twitter @davidshimjs

[![Bitdeli Badge](https://d2weczhvl823v0.cloudfront.net/davidshimjs/qrcodejs/trend.png)](https://bitdeli.com/free "Bitdeli Badge")

