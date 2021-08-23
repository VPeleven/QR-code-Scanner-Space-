# QR CODE Scanner Demo

[Demo Version](https://vpeleven.github.io/QR-code-Scanner-Space-/)

JsQR is designed to be a completely standalone library for scanning QR codes. By design it does not include any platform specific code. This allows it to just as easily scan a frontend webcam stream, a user uploaded image, or be used as part of a backend Node.js process.

## Getting Started


### Installing

* Available on npm. Can be used in a Node.js program or with a module bundler such as Webpack or Browserify.




```
npm install jsqr --save
```
```
// ES6 import
import jsQR from "jsqr";

// CommonJS require
const jsQR = require("jsqr");

jsQR(...);
```

## Browser

Alternatively for frontend use jsQR.js can be included with a script tag
```
<script src="jsQR.js"></script>
<script>
  jsQR(...);
</script>
```

## Return value
* binaryData - Uint8ClampedArray - The raw bytes of the QR code.
* data - The string version of the QR code data.
* chunks - The QR chunks.
* version - The QR version.
* location - An object with keys describing key points of the QR code. Each key is a point of the form {x: number, y: number}. Has points for the following locations.
Corners - topRightCorner/topLeftCorner/bottomRightCorner/bottomLeftCorner;
Finder patterns - topRightFinderPattern/topLeftFinderPattern/bottomLeftFinderPattern
May also have a point for the bottomRightAlignmentPattern assuming one exists and can be located.
