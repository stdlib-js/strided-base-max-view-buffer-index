<!--

@license Apache-2.0

Copyright (c) 2021 The Stdlib Authors.

Licensed under the Apache License, Version 2.0 (the "License");
you may not use this file except in compliance with the License.
You may obtain a copy of the License at

   http://www.apache.org/licenses/LICENSE-2.0

Unless required by applicable law or agreed to in writing, software
distributed under the License is distributed on an "AS IS" BASIS,
WITHOUT WARRANTIES OR CONDITIONS OF ANY KIND, either express or implied.
See the License for the specific language governing permissions and
limitations under the License.

-->


<details>
  <summary>
    About stdlib...
  </summary>
  <p>We believe in a future in which the web is a preferred environment for numerical computation. To help realize this future, we've built stdlib. stdlib is a standard library, with an emphasis on numerical and scientific computation, written in JavaScript (and C) for execution in browsers and in Node.js.</p>
  <p>The library is fully decomposable, being architected in such a way that you can swap out and mix and match APIs and functionality to cater to your exact preferences and use cases.</p>
  <p>When you use stdlib, you can be absolutely certain that you are using the most thorough, rigorous, well-written, studied, documented, tested, measured, and high-quality code out there.</p>
  <p>To join us in bringing numerical computing to the web, get started by checking us out on <a href="https://github.com/stdlib-js/stdlib">GitHub</a>, and please consider <a href="https://opencollective.com/stdlib">financially supporting stdlib</a>. We greatly appreciate your continued support!</p>
</details>

# maxViewBufferIndex

[![NPM version][npm-image]][npm-url] [![Build Status][test-image]][test-url] [![Coverage Status][coverage-image]][coverage-url] <!-- [![dependencies][dependencies-image]][dependencies-url] -->

> Return the maximum accessible index based on a set of provided strided array parameters.

<!-- Section to include introductory text. Make sure to keep an empty line after the intro `section` element and another before the `/section` close. -->

<section class="intro">

</section>

<!-- /.intro -->

<!-- Package usage documentation. -->



<section class="usage">

## Usage

```javascript
import maxViewBufferIndex from 'https://cdn.jsdelivr.net/gh/stdlib-js/strided-base-max-view-buffer-index@v0.3.1-deno/mod.js';
```

#### maxViewBufferIndex( N, stride, offset )

Returns the maximum accessible index based on a set of provided strided array parameters.

```javascript
var idx = maxViewBufferIndex( 3, 2, 10 );
// returns 14
```

</section>

<!-- /.usage -->

<!-- Package usage notes. Make sure to keep an empty line after the `section` element and another before the `/section` close. -->

<section class="notes">

## Notes

-   If `N <= 0`, the function returns the specified `offset`; however, do note that, when `N` equals zero, no strided array elements should be accessed.

</section>

<!-- /.notes -->

<!-- Package usage examples. -->

<section class="examples">

## Examples

<!-- eslint no-undef: "error" -->

```javascript
import discreteUniform from 'https://cdn.jsdelivr.net/gh/stdlib-js/random-base-discrete-uniform@deno/mod.js';
import maxViewBufferIndex from 'https://cdn.jsdelivr.net/gh/stdlib-js/strided-base-max-view-buffer-index@v0.3.1-deno/mod.js';

// Generate a random number of indexed elements:
var N = discreteUniform( 10, 20 );

// Generate a random stride length:
var stride = discreteUniform( -10, 10 );

// Generate a random offset:
var offset = discreteUniform( 0, 100 ) + ( ( stride < 0 ) ? (1-N)*stride : 0 );

// Compute the maximum accessible index:
var idx = maxViewBufferIndex( N, stride, offset );

console.log( 'N: %d, stride: %d, offset: %d => %d', N, stride, offset, idx );
```

</section>

<!-- /.examples -->



<!-- Section to include cited references. If references are included, add a horizontal rule *before* the section. Make sure to keep an empty line after the `section` element and another before the `/section` close. -->

<section class="references">

</section>

<!-- /.references -->

<!-- Section for related `stdlib` packages. Do not manually edit this section, as it is automatically populated. -->

<section class="related">

</section>

<!-- /.related -->

<!-- Section for all links. Make sure to keep an empty line after the `section` element and another before the `/section` close. -->


<section class="main-repo" >

* * *

## Notice

This package is part of [stdlib][stdlib], a standard library with an emphasis on numerical and scientific computing. The library provides a collection of robust, high performance libraries for mathematics, statistics, streams, utilities, and more.

For more information on the project, filing bug reports and feature requests, and guidance on how to develop [stdlib][stdlib], see the main project [repository][stdlib].

#### Community

[![Chat][chat-image]][chat-url]

---

## License

See [LICENSE][stdlib-license].


## Copyright

Copyright &copy; 2016-2026. The Stdlib [Authors][stdlib-authors].

</section>

<!-- /.stdlib -->

<!-- Section for all links. Make sure to keep an empty line after the `section` element and another before the `/section` close. -->

<section class="links">

[npm-image]: http://img.shields.io/npm/v/@stdlib/strided-base-max-view-buffer-index.svg
[npm-url]: https://npmjs.org/package/@stdlib/strided-base-max-view-buffer-index

[test-image]: https://github.com/stdlib-js/strided-base-max-view-buffer-index/actions/workflows/test.yml/badge.svg?branch=v0.3.1
[test-url]: https://github.com/stdlib-js/strided-base-max-view-buffer-index/actions/workflows/test.yml?query=branch:v0.3.1

[coverage-image]: https://img.shields.io/codecov/c/github/stdlib-js/strided-base-max-view-buffer-index/main.svg
[coverage-url]: https://codecov.io/github/stdlib-js/strided-base-max-view-buffer-index?branch=main

<!--

[dependencies-image]: https://img.shields.io/david/stdlib-js/strided-base-max-view-buffer-index.svg
[dependencies-url]: https://david-dm.org/stdlib-js/strided-base-max-view-buffer-index/main

-->

[chat-image]: https://img.shields.io/badge/zulip-join_chat-brightgreen.svg
[chat-url]: https://stdlib.zulipchat.com

[stdlib]: https://github.com/stdlib-js/stdlib

[stdlib-authors]: https://github.com/stdlib-js/stdlib/graphs/contributors

[umd]: https://github.com/umdjs/umd
[es-module]: https://developer.mozilla.org/en-US/docs/Web/JavaScript/Guide/Modules

[deno-url]: https://github.com/stdlib-js/strided-base-max-view-buffer-index/tree/deno
[deno-readme]: https://github.com/stdlib-js/strided-base-max-view-buffer-index/blob/deno/README.md
[umd-url]: https://github.com/stdlib-js/strided-base-max-view-buffer-index/tree/umd
[umd-readme]: https://github.com/stdlib-js/strided-base-max-view-buffer-index/blob/umd/README.md
[esm-url]: https://github.com/stdlib-js/strided-base-max-view-buffer-index/tree/esm
[esm-readme]: https://github.com/stdlib-js/strided-base-max-view-buffer-index/blob/esm/README.md
[branches-url]: https://github.com/stdlib-js/strided-base-max-view-buffer-index/blob/main/branches.md

[stdlib-license]: https://raw.githubusercontent.com/stdlib-js/strided-base-max-view-buffer-index/main/LICENSE

</section>

<!-- /.links -->
