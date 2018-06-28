# fastgif

```js
import {Decoder} from './node_modules/fastgif/fastgif.js';

const decoder = new Decoder();

window.fetch('path/to/gif.js')
    .then((response) => response.arrayBuffer())
    .then((buffer) => decoder.decode(buf))
    .then((out) => {
      // out is an array of {imageData: ImageData, delay: number}
    });
```

Requires WebAssembly support, aka modern Edge, Chrome, Safari or Firefox.
Check first by looking for `window.WebAssembly`.

Based on [Wuffs](https://github.com/google/wuffs).

For a demo and speed comparison, [check here](https://samthor.github.io/fastgif/fastgif.html).
For a writeup of how this works, see [Fast GIF parsing on the web with WASM + Wuffs](https://dev.to/samthor/fast-gif-parsing-on-the-web-with-wasm--wuffs-48l4)!
