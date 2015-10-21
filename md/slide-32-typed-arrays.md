##Typed Arrays

<div class="code-extra es6">
```js
var buf = new ArrayBuffer( 32 );
buf.byteLength; // 32
// buf is now a binary buffer that is 32 bytes long, pre-initialised to 0s

// 16 bit unsigned integers
var arr = new Uint16Array( buf );
arr.length; // 16
```
</div>
<div class="code-extra es6">
```js
// single buffer multiple views
var buf = new ArrayBuffer( 2 );

var view8 = new Uint8Array( buf );
var view16 = new Uint16Array( buf );

view16[0] = 3085;
view8[0]; // 13
view8[1]; // 12

view8[0].toString( 16 ); // "d"
view8[1].toString( 16 ); // "c"

// swap endian
var tmp = view8[0];
view8[0] = view8[1];
view8[1] = tmp;

view16[0]; // 3340
```

Note:
- providing structured access to binary data using array-like semantics

- Type in the name refers to the 'view'

- create a bucket of bits (buffer), then view it using a typed array

- Implement:
  - network protocols
  - cryptography algorithms
  - file format manipulations
  - Audio processing

- Endianness
  - mapped to platform JS is running on
  - can be different between platforms (beware)

- multiple views on same buffer
