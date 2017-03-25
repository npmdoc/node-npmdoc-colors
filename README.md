# api documentation for  [colors (v1.1.2)](https://github.com/Marak/colors.js)  [![travis-ci.org build-status](https://api.travis-ci.org/npmdoc/node-npmdoc-colors.svg)](https://travis-ci.org/npmdoc/node-npmdoc-colors)
#### get colors in your node.js console

[![NPM](https://nodei.co/npm/colors.png?downloads=true)](https://www.npmjs.com/package/colors)

[![apidoc](https://npmdoc.github.io/node-npmdoc-colors/build/screen-capture.buildNpmdoc.browser._2Fhome_2Ftravis_2Fbuild_2Fnpmdoc_2Fnode-npmdoc-colors_2Ftmp_2Fbuild_2Fapidoc.html.png)](https://npmdoc.github.io/node-npmdoc-colors/build..beta..travis-ci.org/apidoc.html)

![package-listing](https://npmdoc.github.io/node-npmdoc-colors/build/screen-capture.npmPackageListing.svg)



# package.json

```json

{
    "author": {
        "name": "Marak Squires"
    },
    "bugs": {
        "url": "https://github.com/Marak/colors.js/issues"
    },
    "dependencies": {},
    "description": "get colors in your node.js console",
    "devDependencies": {},
    "directories": {},
    "dist": {
        "shasum": "168a4701756b6a7f51a12ce0c97bfa28c084ed63",
        "tarball": "https://registry.npmjs.org/colors/-/colors-1.1.2.tgz"
    },
    "engines": {
        "node": ">=0.1.90"
    },
    "files": [
        "examples",
        "lib",
        "LICENSE",
        "safe.js",
        "themes"
    ],
    "gitHead": "8bf2ad9fa695dcb30b7e9fd83691b139fd6655c4",
    "homepage": "https://github.com/Marak/colors.js",
    "keywords": [
        "ansi",
        "terminal",
        "colors"
    ],
    "license": "MIT",
    "main": "lib",
    "maintainers": [
        {
            "name": "marak",
            "email": "marak.squires@gmail.com"
        }
    ],
    "name": "colors",
    "optionalDependencies": {},
    "readme": "ERROR: No README data found!",
    "repository": {
        "type": "git",
        "url": "git+ssh://git@github.com/Marak/colors.js.git"
    },
    "scripts": {
        "test": "node tests/basic-test.js && node tests/safe-test.js"
    },
    "version": "1.1.2"
}
```



# <a name="apidoc.tableOfContents"></a>[table of contents](#apidoc.tableOfContents)

#### [module colors](#apidoc.module.colors)
1.  boolean <span class="apidocSignatureSpan">colors.</span>enabled
1.  boolean <span class="apidocSignatureSpan">colors.</span>supportsColor
1.  [function <span class="apidocSignatureSpan">colors.</span>america (str)](#apidoc.element.colors.america)
1.  [function <span class="apidocSignatureSpan">colors.</span>rainbow (str)](#apidoc.element.colors.rainbow)
1.  [function <span class="apidocSignatureSpan">colors.</span>random (str)](#apidoc.element.colors.random)
1.  [function <span class="apidocSignatureSpan">colors.</span>setTheme (theme)](#apidoc.element.colors.setTheme)
1.  [function <span class="apidocSignatureSpan">colors.</span>strip (str)](#apidoc.element.colors.strip)
1.  [function <span class="apidocSignatureSpan">colors.</span>stripColors (str)](#apidoc.element.colors.stripColors)
1.  [function <span class="apidocSignatureSpan">colors.</span>stylize (str, style)](#apidoc.element.colors.stylize)
1.  [function <span class="apidocSignatureSpan">colors.</span>trap (text, options)](#apidoc.element.colors.trap)
1.  [function <span class="apidocSignatureSpan">colors.</span>zalgo (text, options)](#apidoc.element.colors.zalgo)
1.  [function <span class="apidocSignatureSpan">colors.</span>zebra (str)](#apidoc.element.colors.zebra)
1.  object <span class="apidocSignatureSpan">colors.</span>maps
1.  object <span class="apidocSignatureSpan">colors.</span>styles
1.  object <span class="apidocSignatureSpan">colors.</span>themes

#### [module colors.maps](#apidoc.module.colors.maps)
1.  [function <span class="apidocSignatureSpan">colors.maps.</span>america (letter, i, exploded)](#apidoc.element.colors.maps.america)
1.  [function <span class="apidocSignatureSpan">colors.maps.</span>rainbow (letter, i, exploded)](#apidoc.element.colors.maps.rainbow)
1.  [function <span class="apidocSignatureSpan">colors.maps.</span>random (letter, i, exploded)](#apidoc.element.colors.maps.random)
1.  [function <span class="apidocSignatureSpan">colors.maps.</span>zebra (letter, i, exploded)](#apidoc.element.colors.maps.zebra)



# <a name="apidoc.module.colors"></a>[module colors](#apidoc.module.colors)

#### <a name="apidoc.element.colors.america"></a>[function <span class="apidocSignatureSpan">colors.</span>america (str)](#apidoc.element.colors.america)
- description and source-code
```javascript
america = function (str) {
  return sequencer(colors.maps[map], str);
}
```
- example usage
```shell
...
});

addProperty("random", function(){
  return colors.random(this);
});

addProperty("america", function(){
  return colors.america(this);
});

//
// Iterate through all default styles and colors
//
var x = Object.keys(colors.styles);
x.forEach(function (style) {
...
```

#### <a name="apidoc.element.colors.rainbow"></a>[function <span class="apidocSignatureSpan">colors.</span>rainbow (str)](#apidoc.element.colors.rainbow)
- description and source-code
```javascript
rainbow = function (str) {
  return sequencer(colors.maps[map], str);
}
```
- example usage
```shell
...

'''js
var colors = require('colors/safe');

console.log(colors.green('hello')); // outputs green text
console.log(colors.red.underline('i like cake and pies')) // outputs red underlined text
console.log(colors.inverse('inverse the color')); // inverses the color
console.log(colors.rainbow('OMG Rainbows!')); // rainbow
console.log(colors.trap('Run the trap')); // Drops the bass

'''

I prefer the first way. Some people seem to be afraid of extending 'String.prototype' and prefer the second way.

If you are writing good code you will never have an issue with the first approach. If you really don't want to touch 'String.prototype
', the second usage will not touch 'String' native object.
...
```

#### <a name="apidoc.element.colors.random"></a>[function <span class="apidocSignatureSpan">colors.</span>random (str)](#apidoc.element.colors.random)
- description and source-code
```javascript
random = function (str) {
  return sequencer(colors.maps[map], str);
}
```
- example usage
```shell
...
});

addProperty("rainbow", function(){
  return colors.rainbow(this);
});

addProperty("random", function(){
  return colors.random(this);
});

addProperty("america", function(){
  return colors.america(this);
});

//
...
```

#### <a name="apidoc.element.colors.setTheme"></a>[function <span class="apidocSignatureSpan">colors.</span>setTheme (theme)](#apidoc.element.colors.setTheme)
- description and source-code
```javascript
setTheme = function (theme) {
  if (typeof theme === 'string') {
    try {
      colors.themes[theme] = require(theme);
      applyTheme(colors.themes[theme]);
      return colors.themes[theme];
    } catch (err) {
      console.log(err);
      return err;
    }
  } else {
    applyTheme(theme);
  }
}
```
- example usage
```shell
...

### Using standard API

'''js

var colors = require('colors');

colors.setTheme({
silly: 'rainbow',
input: 'grey',
verbose: 'cyan',
prompt: 'grey',
info: 'green',
data: 'grey',
help: 'cyan',
...
```

#### <a name="apidoc.element.colors.strip"></a>[function <span class="apidocSignatureSpan">colors.</span>strip (str)](#apidoc.element.colors.strip)
- description and source-code
```javascript
strip = function (str){
  return ("" + str).replace(/\x1B\[\d+m/g, '');
}
```
- example usage
```shell
...
      var exploded = this.split(""), i = 0;
      exploded = exploded.map(map);
      return exploded.join("");
    }
};

addProperty('strip', function () {
  return colors.strip(this);
});

addProperty('stripColors', function () {
  return colors.strip(this);
});

addProperty("trap", function(){
...
```

#### <a name="apidoc.element.colors.stripColors"></a>[function <span class="apidocSignatureSpan">colors.</span>stripColors (str)](#apidoc.element.colors.stripColors)
- description and source-code
```javascript
stripColors = function (str){
  return ("" + str).replace(/\x1B\[\d+m/g, '');
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.colors.stylize"></a>[function <span class="apidocSignatureSpan">colors.</span>stylize (str, style)](#apidoc.element.colors.stylize)
- description and source-code
```javascript
function stylize(str, style) {
  if (!colors.enabled) {
    return str+'';
  }

  return ansiStyles[style].open + str + ansiStyles[style].close;
}
```
- example usage
```shell
...

//
// Iterate through all default styles and colors
//
var x = Object.keys(colors.styles);
x.forEach(function (style) {
  addProperty(style, function () {
    return colors.stylize(this, style);
  });
});

function applyTheme(theme) {
  //
  // Remark: This is a list of methods that exist
  // on String that you should not overwrite.
...
```

#### <a name="apidoc.element.colors.trap"></a>[function <span class="apidocSignatureSpan">colors.</span>trap (text, options)](#apidoc.element.colors.trap)
- description and source-code
```javascript
function runTheTrap(text, options) {
  var result = "";
  text = text || "Run the trap, drop the bass";
  text = text.split('');
  var trap = {
    a: ["\u0040", "\u0104", "\u023a", "\u0245", "\u0394", "\u039b", "\u0414"],
    b: ["\u00df", "\u0181", "\u0243", "\u026e", "\u03b2", "\u0e3f"],
    c: ["\u00a9", "\u023b", "\u03fe"],
    d: ["\u00d0", "\u018a", "\u0500" , "\u0501" ,"\u0502", "\u0503"],
    e: ["\u00cb", "\u0115", "\u018e", "\u0258", "\u03a3", "\u03be", "\u04bc", "\u0a6c"],
    f: ["\u04fa"],
    g: ["\u0262"],
    h: ["\u0126", "\u0195", "\u04a2", "\u04ba", "\u04c7", "\u050a"],
    i: ["\u0f0f"],
    j: ["\u0134"],
    k: ["\u0138", "\u04a0", "\u04c3", "\u051e"],
    l: ["\u0139"],
    m: ["\u028d", "\u04cd", "\u04ce", "\u0520", "\u0521", "\u0d69"],
    n: ["\u00d1", "\u014b", "\u019d", "\u0376", "\u03a0", "\u048a"],
    o: ["\u00d8", "\u00f5", "\u00f8", "\u01fe", "\u0298", "\u047a", "\u05dd", "\u06dd", "\u0e4f"],
    p: ["\u01f7", "\u048e"],
    q: ["\u09cd"],
    r: ["\u00ae", "\u01a6", "\u0210", "\u024c", "\u0280", "\u042f"],
    s: ["\u00a7", "\u03de", "\u03df", "\u03e8"],
    t: ["\u0141", "\u0166", "\u0373"],
    u: ["\u01b1", "\u054d"],
    v: ["\u05d8"],
    w: ["\u0428", "\u0460", "\u047c", "\u0d70"],
    x: ["\u04b2", "\u04fe", "\u04fc", "\u04fd"],
    y: ["\u00a5", "\u04b0", "\u04cb"],
    z: ["\u01b5", "\u0240"]
  }
  text.forEach(function(c){
    c = c.toLowerCase();
    var chars = trap[c] || [" "];
    var rand = Math.floor(Math.random() * chars.length);
    if (typeof trap[c] !== "undefined") {
      result += trap[c][rand];
    } else {
      result += c;
    }
  });
  return result;

}
```
- example usage
```shell
...
'''js
var colors = require('colors/safe');

console.log(colors.green('hello')); // outputs green text
console.log(colors.red.underline('i like cake and pies')) // outputs red underlined text
console.log(colors.inverse('inverse the color')); // inverses the color
console.log(colors.rainbow('OMG Rainbows!')); // rainbow
console.log(colors.trap('Run the trap')); // Drops the bass

'''

I prefer the first way. Some people seem to be afraid of extending 'String.prototype' and prefer the second way.

If you are writing good code you will never have an issue with the first approach. If you really don't want to touch 'String.prototype
', the second usage will not touch 'String' native object.
...
```

#### <a name="apidoc.element.colors.zalgo"></a>[function <span class="apidocSignatureSpan">colors.</span>zalgo (text, options)](#apidoc.element.colors.zalgo)
- description and source-code
```javascript
function zalgo(text, options) {
  text = text || "   he is here   ";
  var soul = {
    "up" : [
      '̍', '̎', '̄', '̅',
      '̿', '̑', '̆', '̐',
      '͒', '͗', '͑', '̇',
      '̈', '̊', '͂', '̓',
      '̈', '͊', '͋', '͌',
      '̃', '̂', '̌', '͐',
      '̀', '́', '̋', '̏',
      '̒', '̓', '̔', '̽',
      '̉', 'ͣ', 'ͤ', 'ͥ',
      'ͦ', 'ͧ', 'ͨ', 'ͩ',
      'ͪ', 'ͫ', 'ͬ', 'ͭ',
      'ͮ', 'ͯ', '̾', '͛',
      '͆', '̚'
    ],
    "down" : [
      '̖', '̗', '̘', '̙',
      '̜', '̝', '̞', '̟',
      '̠', '̤', '̥', '̦',
      '̩', '̪', '̫', '̬',
      '̭', '̮', '̯', '̰',
      '̱', '̲', '̳', '̹',
      '̺', '̻', '̼', 'ͅ',
      '͇', '͈', '͉', '͍',
      '͎', '͓', '͔', '͕',
      '͖', '͙', '͚', '̣'
    ],
    "mid" : [
      '̕', '̛', '̀', '́',
      '͘', '̡', '̢', '̧',
      '̨', '̴', '̵', '̶',
      '͜', '͝', '͞',
      '͟', '͠', '͢', '̸',
      '̷', '͡', ' ҉'
    ]
  },
  all = [].concat(soul.up, soul.down, soul.mid),
  zalgo = {};

  function randomNumber(range) {
    var r = Math.floor(Math.random() * range);
    return r;
  }

  function is_char(character) {
    var bool = false;
    all.filter(function (i) {
      bool = (i === character);
    });
    return bool;
  }


  function heComes(text, options) {
    var result = '', counts, l;
    options = options || {};
    options["up"] =   typeof options["up"]   !== 'undefined' ? options["up"]   : true;
    options["mid"] =  typeof options["mid"]  !== 'undefined' ? options["mid"]  : true;
    options["down"] = typeof options["down"] !== 'undefined' ? options["down"] : true;
    options["size"] = typeof options["size"] !== 'undefined' ? options["size"] : "maxi";
    text = text.split('');
    for (l in text) {
      if (is_char(l)) {
        continue;
      }
      result = result + text[l];
      counts = {"up" : 0, "down" : 0, "mid" : 0};
      switch (options.size) {
      case 'mini':
        counts.up = randomNumber(8);
        counts.mid = randomNumber(2);
        counts.down = randomNumber(8);
        break;
      case 'maxi':
        counts.up = randomNumber(16) + 3;
        counts.mid = randomNumber(4) + 1;
        counts.down = randomNumber(64) + 3;
        break;
      default:
        counts.up = randomNumber(8) + 1;
        counts.mid = randomNumber(6) / 2;
        counts.down = randomNumber(8) + 1;
        break;
      }

      var arr = ["up", "mid", "down"];
      for (var d in arr) {
        var index = arr[d];
        for (var i = 0 ; i <= counts[index]; i++) {
          if (options[index]) {
            result = result + soul[index][randomNumber(soul[index].length)];
          }
        }
      }
    }
    return result;
  }
  // don't summon him
  return heComes(text, options);
}
```
- example usage
```shell
...
});

addProperty("trap", function(){
  return colors.trap(this);
});

addProperty("zalgo", function(){
  return colors.zalgo(this);
});

addProperty("zebra", function(){
  return colors.zebra(this);
});

addProperty("rainbow", function(){
...
```

#### <a name="apidoc.element.colors.zebra"></a>[function <span class="apidocSignatureSpan">colors.</span>zebra (str)](#apidoc.element.colors.zebra)
- description and source-code
```javascript
zebra = function (str) {
  return sequencer(colors.maps[map], str);
}
```
- example usage
```shell
...
});

addProperty("zalgo", function(){
  return colors.zalgo(this);
});

addProperty("zebra", function(){
  return colors.zebra(this);
});

addProperty("rainbow", function(){
  return colors.rainbow(this);
});

addProperty("random", function(){
...
```



# <a name="apidoc.module.colors.maps"></a>[module colors.maps](#apidoc.module.colors.maps)

#### <a name="apidoc.element.colors.maps.america"></a>[function <span class="apidocSignatureSpan">colors.maps.</span>america (letter, i, exploded)](#apidoc.element.colors.maps.america)
- description and source-code
```javascript
america = function (letter, i, exploded) {
  if(letter === " ") return letter;
  switch(i%3) {
    case 0: return colors.red(letter);
    case 1: return colors.white(letter)
    case 2: return colors.blue(letter)
  }
}
```
- example usage
```shell
...
});

addProperty("random", function(){
  return colors.random(this);
});

addProperty("america", function(){
  return colors.america(this);
});

//
// Iterate through all default styles and colors
//
var x = Object.keys(colors.styles);
x.forEach(function (style) {
...
```

#### <a name="apidoc.element.colors.maps.rainbow"></a>[function <span class="apidocSignatureSpan">colors.maps.</span>rainbow (letter, i, exploded)](#apidoc.element.colors.maps.rainbow)
- description and source-code
```javascript
rainbow = function (letter, i, exploded) {
  if (letter === " ") {
    return letter;
  } else {
    return colors[rainbowColors[i++ % rainbowColors.length]](letter);
  }
}
```
- example usage
```shell
...

'''js
var colors = require('colors/safe');

console.log(colors.green('hello')); // outputs green text
console.log(colors.red.underline('i like cake and pies')) // outputs red underlined text
console.log(colors.inverse('inverse the color')); // inverses the color
console.log(colors.rainbow('OMG Rainbows!')); // rainbow
console.log(colors.trap('Run the trap')); // Drops the bass

'''

I prefer the first way. Some people seem to be afraid of extending 'String.prototype' and prefer the second way.

If you are writing good code you will never have an issue with the first approach. If you really don't want to touch 'String.prototype
', the second usage will not touch 'String' native object.
...
```

#### <a name="apidoc.element.colors.maps.random"></a>[function <span class="apidocSignatureSpan">colors.maps.</span>random (letter, i, exploded)](#apidoc.element.colors.maps.random)
- description and source-code
```javascript
random = function (letter, i, exploded) {
  return letter === " " ? letter : colors[available[Math.round(Math.random() * (available.length - 1))]](letter);
}
```
- example usage
```shell
...
});

addProperty("rainbow", function(){
  return colors.rainbow(this);
});

addProperty("random", function(){
  return colors.random(this);
});

addProperty("america", function(){
  return colors.america(this);
});

//
...
```

#### <a name="apidoc.element.colors.maps.zebra"></a>[function <span class="apidocSignatureSpan">colors.maps.</span>zebra (letter, i, exploded)](#apidoc.element.colors.maps.zebra)
- description and source-code
```javascript
zebra = function (letter, i, exploded) {
  return i % 2 === 0 ? letter : colors.inverse(letter);
}
```
- example usage
```shell
...
});

addProperty("zalgo", function(){
  return colors.zalgo(this);
});

addProperty("zebra", function(){
  return colors.zebra(this);
});

addProperty("rainbow", function(){
  return colors.rainbow(this);
});

addProperty("random", function(){
...
```



# misc
- this document was created with [utility2](https://github.com/kaizhu256/node-utility2)
