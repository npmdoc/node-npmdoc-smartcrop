# api documentation for  [smartcrop (v1.1.1)](https://github.com/jwagner/smartcrop.js)  [![npm package](https://img.shields.io/npm/v/npmdoc-smartcrop.svg?style=flat-square)](https://www.npmjs.org/package/npmdoc-smartcrop) [![travis-ci.org build-status](https://api.travis-ci.org/npmdoc/node-npmdoc-smartcrop.svg)](https://travis-ci.org/npmdoc/node-npmdoc-smartcrop)
#### Content aware image cropping.

[![NPM](https://nodei.co/npm/smartcrop.png?downloads=true)](https://www.npmjs.com/package/smartcrop)

[![apidoc](https://npmdoc.github.io/node-npmdoc-smartcrop/build/screenCapture.buildNpmdoc.browser._2Fhome_2Ftravis_2Fbuild_2Fnpmdoc_2Fnode-npmdoc-smartcrop_2Ftmp_2Fbuild_2Fapidoc.html.png)](https://npmdoc.github.io/node-npmdoc-smartcrop/build/apidoc.html)

![npmPackageListing](https://npmdoc.github.io/node-npmdoc-smartcrop/build/screenCapture.npmPackageListing.svg)

![npmPackageDependencyTree](https://npmdoc.github.io/node-npmdoc-smartcrop/build/screenCapture.npmPackageDependencyTree.svg)



# package.json

```json

{
    "author": {
        "name": "Jonas Wagner",
        "email": "jonas@29a.ch",
        "url": "http://29a.ch/"
    },
    "bugs": {
        "url": "https://github.com/jwagner/smartcrop.js/issues"
    },
    "dependencies": {},
    "description": "Content aware image cropping.",
    "devDependencies": {
        "500px": "~0.3.2",
        "benchmark": "~1.0.0",
        "chai": "^1.9.1",
        "grunt": "^0.4.4",
        "grunt-contrib-connect": "~0.7.1",
        "grunt-contrib-watch": "~0.6.1",
        "grunt-rsync": "~0.5.0",
        "karma": "^1.1.0",
        "karma-chrome-launcher": "^1.0.1",
        "karma-mocha": "^1.1.1",
        "karma-sauce-launcher": "^1.0.0",
        "microtime": "^2.0.0",
        "mocha": "^1.18.2",
        "promise-polyfill": "^5.2.1"
    },
    "directories": {},
    "dist": {
        "shasum": "d8a16262f43c418fffa7b9f12a3e03d65d5d19f8",
        "tarball": "https://registry.npmjs.org/smartcrop/-/smartcrop-1.1.1.tgz"
    },
    "gitHead": "0c631a57f2544305da49b32d4142ca1130cba13a",
    "homepage": "https://github.com/jwagner/smartcrop.js",
    "license": "MIT",
    "main": "./smartcrop",
    "maintainers": [
        {
            "name": "jonas",
            "email": "jonas@29a.ch"
        }
    ],
    "name": "smartcrop",
    "optionalDependencies": {},
    "readme": "ERROR: No README data found!",
    "repository": {
        "type": "git",
        "url": "git+https://github.com/jwagner/smartcrop.js.git"
    },
    "scripts": {
        "test": "karma start karma.conf.js"
    },
    "version": "1.1.1"
}
```



# <a name="apidoc.tableOfContents"></a>[table of contents](#apidoc.tableOfContents)

#### [module smartcrop](#apidoc.module.smartcrop)
1.  [function <span class="apidocSignatureSpan">smartcrop.</span>ImgData (width, height, data)](#apidoc.element.smartcrop.ImgData)
1.  [function <span class="apidocSignatureSpan">smartcrop.</span>Promise ()](#apidoc.element.smartcrop.Promise)
1.  [function <span class="apidocSignatureSpan">smartcrop.</span>_canvasImageOperations (canvasFactory)](#apidoc.element.smartcrop._canvasImageOperations)
1.  [function <span class="apidocSignatureSpan">smartcrop.</span>_downSample (input, factor)](#apidoc.element.smartcrop._downSample)
1.  [function <span class="apidocSignatureSpan">smartcrop.</span>crop (inputImage, options_, callback)](#apidoc.element.smartcrop.crop)
1.  [function <span class="apidocSignatureSpan">smartcrop.</span>importance (options, crop, x, y)](#apidoc.element.smartcrop.importance)
1.  [function <span class="apidocSignatureSpan">smartcrop.</span>isAvailable (options)](#apidoc.element.smartcrop.isAvailable)
1.  object <span class="apidocSignatureSpan">smartcrop.</span>DEFAULTS

#### [module smartcrop.DEFAULTS](#apidoc.module.smartcrop.DEFAULTS)
1.  boolean <span class="apidocSignatureSpan">smartcrop.DEFAULTS.</span>debug
1.  boolean <span class="apidocSignatureSpan">smartcrop.DEFAULTS.</span>prescale
1.  boolean <span class="apidocSignatureSpan">smartcrop.DEFAULTS.</span>ruleOfThirds
1.  [function <span class="apidocSignatureSpan">smartcrop.DEFAULTS.</span>canvasFactory (w, h)](#apidoc.element.smartcrop.DEFAULTS.canvasFactory)
1.  number <span class="apidocSignatureSpan">smartcrop.DEFAULTS.</span>aspect
1.  number <span class="apidocSignatureSpan">smartcrop.DEFAULTS.</span>boostWeight
1.  number <span class="apidocSignatureSpan">smartcrop.DEFAULTS.</span>cropHeight
1.  number <span class="apidocSignatureSpan">smartcrop.DEFAULTS.</span>cropWidth
1.  number <span class="apidocSignatureSpan">smartcrop.DEFAULTS.</span>detailWeight
1.  number <span class="apidocSignatureSpan">smartcrop.DEFAULTS.</span>edgeRadius
1.  number <span class="apidocSignatureSpan">smartcrop.DEFAULTS.</span>edgeWeight
1.  number <span class="apidocSignatureSpan">smartcrop.DEFAULTS.</span>height
1.  number <span class="apidocSignatureSpan">smartcrop.DEFAULTS.</span>maxScale
1.  number <span class="apidocSignatureSpan">smartcrop.DEFAULTS.</span>minScale
1.  number <span class="apidocSignatureSpan">smartcrop.DEFAULTS.</span>outsideImportance
1.  number <span class="apidocSignatureSpan">smartcrop.DEFAULTS.</span>saturationBias
1.  number <span class="apidocSignatureSpan">smartcrop.DEFAULTS.</span>saturationBrightnessMax
1.  number <span class="apidocSignatureSpan">smartcrop.DEFAULTS.</span>saturationBrightnessMin
1.  number <span class="apidocSignatureSpan">smartcrop.DEFAULTS.</span>saturationThreshold
1.  number <span class="apidocSignatureSpan">smartcrop.DEFAULTS.</span>saturationWeight
1.  number <span class="apidocSignatureSpan">smartcrop.DEFAULTS.</span>scaleStep
1.  number <span class="apidocSignatureSpan">smartcrop.DEFAULTS.</span>scoreDownSample
1.  number <span class="apidocSignatureSpan">smartcrop.DEFAULTS.</span>skinBias
1.  number <span class="apidocSignatureSpan">smartcrop.DEFAULTS.</span>skinBrightnessMax
1.  number <span class="apidocSignatureSpan">smartcrop.DEFAULTS.</span>skinBrightnessMin
1.  number <span class="apidocSignatureSpan">smartcrop.DEFAULTS.</span>skinThreshold
1.  number <span class="apidocSignatureSpan">smartcrop.DEFAULTS.</span>skinWeight
1.  number <span class="apidocSignatureSpan">smartcrop.DEFAULTS.</span>step
1.  number <span class="apidocSignatureSpan">smartcrop.DEFAULTS.</span>width
1.  object <span class="apidocSignatureSpan">smartcrop.DEFAULTS.</span>imageOperations
1.  object <span class="apidocSignatureSpan">smartcrop.DEFAULTS.</span>skinColor



# <a name="apidoc.module.smartcrop"></a>[module smartcrop](#apidoc.module.smartcrop)

#### <a name="apidoc.element.smartcrop.ImgData"></a>[function <span class="apidocSignatureSpan">smartcrop.</span>ImgData (width, height, data)](#apidoc.element.smartcrop.ImgData)
- description and source-code
```javascript
function ImgData(width, height, data) {
  this.width = width;
  this.height = height;
  if (data) {
    this.data = new Uint8ClampedArray(data);
  }
  else {
    this.data = new Uint8ClampedArray(width * height * 4);
  }
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.smartcrop.Promise"></a>[function <span class="apidocSignatureSpan">smartcrop.</span>Promise ()](#apidoc.element.smartcrop.Promise)
- description and source-code
```javascript
function Promise() { [native code] }
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.smartcrop._canvasImageOperations"></a>[function <span class="apidocSignatureSpan">smartcrop.</span>_canvasImageOperations (canvasFactory)](#apidoc.element.smartcrop._canvasImageOperations)
- description and source-code
```javascript
function canvasImageOperations(canvasFactory) {
  return {
    // Takes imageInput as argument
    // returns an object which has at least
    // {width: n, height: n}
    open: function(image) {
      // Work around images scaled in css by drawing them onto a canvas
      var w = image.naturalWidth || image.width;
      var h = image.naturalHeight || image.height;
      var c = canvasFactory(w, h);
      var ctx = c.getContext('2d');
      if (image.naturalWidth && (image.naturalWidth != image.width || image.naturalHeight != image.height)) {
        c.width = image.naturalWidth;
        c.height = image.naturalHeight;
      }
      else {
        c.width = image.width;
        c.height = image.height;
      }
      ctx.drawImage(image, 0, 0);
      return smartcrop.Promise.resolve(c);
    },
    // Takes an image (as returned by open), and changes it's size by resampling
    resample: function(image, width, height) {
      return Promise.resolve(image).then(function(image) {
        var c = canvasFactory(~~width, ~~height);
        var ctx = c.getContext('2d');

        ctx.drawImage(image, 0, 0, image.width, image.height, 0, 0, c.width, c.height);
        return smartcrop.Promise.resolve(c);
      });
    },
    getData: function(image) {
      return Promise.resolve(image).then(function(c) {
        var ctx = c.getContext('2d');
        var id = ctx.getImageData(0, 0, c.width, c.height);
        return new ImgData(c.width, c.height, id.data);
      });
    },
  };
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.smartcrop._downSample"></a>[function <span class="apidocSignatureSpan">smartcrop.</span>_downSample (input, factor)](#apidoc.element.smartcrop._downSample)
- description and source-code
```javascript
function downSample(input, factor) {
  var idata = input.data;
  var iwidth = input.width;
  var width = Math.floor(input.width / factor);
  var height = Math.floor(input.height / factor);
  var output = new ImgData(width, height);
  var data = output.data;
  var ifactor2 = 1 / (factor * factor);
  for (var y = 0; y < height; y++) {
    for (var x = 0; x < width; x++) {
      var i = (y * width + x) * 4;

      var r = 0;
      var g = 0;
      var b = 0;
      var a = 0;

      var mr = 0;
      var mg = 0;
      var mb = 0;

      for (var v = 0; v < factor; v++) {
        for (var u = 0; u < factor; u++) {
          var j = ((y * factor + v) * iwidth + (x * factor + u)) * 4;
          r += idata[j];
          g += idata[j + 1];
          b += idata[j + 2];
          a += idata[j + 3];
          mr = Math.max(mr, idata[j]);
          mg = Math.max(mg, idata[j + 1]);
          mb = Math.max(mb, idata[j + 2]);
        }
      }
      // this is some funky magic to preserve detail a bit more for
      // skin (r) and detail (g). Saturation (b) does not get this boost.
      data[i] = r * ifactor2 * 0.5 + mr * 0.5;
      data[i + 1] = g * ifactor2 * 0.7 + mg * 0.3;
      data[i + 2] = b * ifactor2;
      data[i + 3] = a * ifactor2;
    }
  }
  return output;
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.smartcrop.crop"></a>[function <span class="apidocSignatureSpan">smartcrop.</span>crop (inputImage, options_, callback)](#apidoc.element.smartcrop.crop)
- description and source-code
```javascript
crop = function (inputImage, options_, callback) {
  var options = extend({}, smartcrop.DEFAULTS, options_);

  if (options.aspect) {
    options.width = options.aspect;
    options.height = 1;
  }

  if (options.imageOperations === null) {
    options.imageOperations = canvasImageOperations(options.canvasFactory);
  }

  var iop = options.imageOperations;

  var scale = 1;
  var prescale = 1;

  return iop.open(inputImage, options.input).then(function(image) {

    if (options.width && options.height) {
      scale = min(image.width / options.width, image.height / options.height);
      options.cropWidth = ~~(options.width * scale);
      options.cropHeight = ~~(options.height * scale);
      // Img = 100x100, width = 95x95, scale = 100/95, 1/scale > min
      // don't set minscale smaller than 1/scale
      // -> don't pick crops that need upscaling
      options.minScale = min(options.maxScale, max(1 / scale, options.minScale));

      if (options.prescale !== false) {
        prescale = 1 / scale / options.minScale;
        if (prescale < 1) {
          image = iop.resample(image, image.width * prescale, image.height * prescale);
          options.cropWidth = ~~(options.cropWidth * prescale);
          options.cropHeight = ~~(options.cropHeight * prescale);
          if (options.boost) {
            options.boost = options.boost.map(function(boost) {
              return {
                x: ~~(boost.x * prescale),
                y: ~~(boost.y * prescale),
                width: ~~(boost.width * prescale),
                height: ~~(boost.height * prescale),
                weight: boost.weight
              };
            });
          }
        }
        else {
          prescale = 1;
        }
      }
    }
    return image;
  })
  .then(function(image) {
    return iop.getData(image).then(function(data) {
      var result = analyse(options, data);

      var crops = result.crops || [result.topCrop];
      for (var i = 0, iLen = crops.length; i < iLen; i++) {
        var crop = crops[i];
        crop.x = ~~(crop.x / prescale);
        crop.y = ~~(crop.y / prescale);
        crop.width = ~~(crop.width / prescale);
        crop.height = ~~(crop.height / prescale);
      }
      if (callback) callback(result);
      return result;
    });
  });
}
```
- example usage
```shell
...
1. Rank them using an importance function to focus the detail in the center
  and avoid it in the edges.
1. Output the candidate crop with the highest rank


## Simple Example
'''javascript
smartcrop.crop(image, {width: 100, height: 100}).then(function(result){
  console.log(result);
});
'''
Output:
'''javascript
{topCrop: {x: 300, y: 200, height: 200, width: 200}}
'''
...
```

#### <a name="apidoc.element.smartcrop.importance"></a>[function <span class="apidocSignatureSpan">smartcrop.</span>importance (options, crop, x, y)](#apidoc.element.smartcrop.importance)
- description and source-code
```javascript
function importance(options, crop, x, y) {
  if (crop.x > x || x >= crop.x + crop.width || crop.y > y || y >= crop.y + crop.height) {
    return options.outsideImportance;
  }
  x = (x - crop.x) / crop.width;
  y = (y - crop.y) / crop.height;
  var px = abs(0.5 - x) * 2;
  var py = abs(0.5 - y) * 2;
  // Distance from edge
  var dx = Math.max(px - 1.0 + options.edgeRadius, 0);
  var dy = Math.max(py - 1.0 + options.edgeRadius, 0);
  var d = (dx * dx + dy * dy) * options.edgeWeight;
  var s = 1.41 - sqrt(px * px + py * py);
  if (options.ruleOfThirds) {
    s += (Math.max(0, s + d + 0.5) * 1.2) * (thirds(px) + thirds(py));
  }
  return s + d;
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.smartcrop.isAvailable"></a>[function <span class="apidocSignatureSpan">smartcrop.</span>isAvailable (options)](#apidoc.element.smartcrop.isAvailable)
- description and source-code
```javascript
isAvailable = function (options) {
  if (!smartcrop.Promise) return false;

  var canvasFactory = options ? options.canvasFactory : defaultCanvasFactory;

  if (canvasFactory === defaultCanvasFactory) {
    var c = document.createElement('canvas');
    if (!c.getContext('2d')) {
      return false;
    }
  }

  return true;
}
```
- example usage
```shell
n/a
```



# <a name="apidoc.module.smartcrop.DEFAULTS"></a>[module smartcrop.DEFAULTS](#apidoc.module.smartcrop.DEFAULTS)

#### <a name="apidoc.element.smartcrop.DEFAULTS.canvasFactory"></a>[function <span class="apidocSignatureSpan">smartcrop.DEFAULTS.</span>canvasFactory (w, h)](#apidoc.element.smartcrop.DEFAULTS.canvasFactory)
- description and source-code
```javascript
function defaultCanvasFactory(w, h) {
  var c = document.createElement('canvas');
  c.width = w;
  c.height = h;
  return c;
}
```
- example usage
```shell
n/a
```



# misc
- this document was created with [utility2](https://github.com/kaizhu256/node-utility2)
