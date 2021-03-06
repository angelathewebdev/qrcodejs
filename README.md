# QRCode.js
QRCode.js is javascript library for making QRCode.

QRCode.js supports Cross-browser with HTML5 Canvas and table tag in DOM. QRCode.js has no dependencies.

This is a fork of https://github.com/davidshimjs/qrcodejs

In this version, I have added the following features:

- `blockRatio` to change the size of the block. It takes a value between 0 and 1. It's probably not a good idea to use a value smaller than 0.3.
- `cover` is a URL pointing to an image. This image should be the same size as the QR code.
- `overlayOptions` contain the same thing as other options. Because a second layer is drawn on top of the cover image, you can configure additional options here.

## Basic Usages
```
<div id="qrcode"></div>
<script type="text/javascript">
new QRCode(document.getElementById("qrcode"), "http://jindo.dev.naver.com/collie");
</script>
```

or with some options

```
<div id="qrcode"></div>
<script type="text/javascript">
var qrcode = new QRCode(document.getElementById("qrcode"), {
	text: "http://raventech.com/",
	cover: "http://raventech.com/public/images/flow_logo.1b0d6d39.png"
	width: 280,
	height: 280,
	colorDark : "#000000",
	colorLight : "#ffffff",
	correctLevel : QRCode.CorrectLevel.H,
	overlayOptions: {
		blockRatio: 0.4,
	}
});
</script>
```

and you can use some methods

```
qrcode.clear(); // clear the code.
qrcode.makeCode("http://naver.com"); // make another code.
```

## Browser Compatibility
IE6~10, Chrome, Firefox, Safari, Opera, Mobile Safari, Android, Windows Mobile, ETC.

## License
MIT License
