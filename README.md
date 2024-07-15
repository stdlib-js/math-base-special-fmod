<!--

@license Apache-2.0

Copyright (c) 2024 The Stdlib Authors.

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

# Modulus Function

[![NPM version][npm-image]][npm-url] [![Build Status][test-image]][test-url] [![Coverage Status][coverage-image]][coverage-url] <!-- [![dependencies][dependencies-image]][dependencies-url] -->

> [Modulus function][modulus-function].

<section class="intro">

The [modulus function][modulus-function] is defined as

<!-- <equation class="equation" label="eq:modulus_function" align="center" raw="z = x%y" alt="Modulus function"> -->

```math
z = x%y
```

<!-- </equation> -->

where `x` is the **dividend** and `y` is the **divisor**.

</section>

<!-- /.intro -->

<section class="installation">

## Installation

```bash
npm install @stdlib/math-base-special-fmod
```

Alternatively,

-   To load the package in a website via a `script` tag without installation and bundlers, use the [ES Module][es-module] available on the [`esm`][esm-url] branch (see [README][esm-readme]).
-   If you are using Deno, visit the [`deno`][deno-url] branch (see [README][deno-readme] for usage intructions).
-   For use in Observable, or in browser/node environments, use the [Universal Module Definition (UMD)][umd] build available on the [`umd`][umd-url] branch (see [README][umd-readme]).

The [branches.md][branches-url] file summarizes the available branches and displays a diagram illustrating their relationships.

To view installation and usage instructions specific to each branch build, be sure to explicitly navigate to the respective README files on each branch, as linked to above.

</section>

<section class="usage">

## Usage

```javascript
var fmod = require( '@stdlib/math-base-special-fmod' );
```

#### fmod( x, y )

Evaluates the [modulus function][modulus-function].

```javascript
var v = fmod( 8.0, 3.0 );
// returns 2.0

v = fmod( 9.0, 3.0 );
// returns 0.0

v = fmod( 8.9, 3.0 );
// returns 2.9

v = fmod( NaN, 3.0 );
// returns NaN

v = fmod( 5.0, NaN );
// returns NaN

v = fmod( NaN, NaN );
// returns NaN
```

</section>

<!-- /.usage -->

<section class="examples">

## Examples

<!-- eslint no-undef: "error" -->

```javascript
var randu = require( '@stdlib/random-base-randu' );
var round = require( '@stdlib/math-base-special-round' );
var fmod = require( '@stdlib/math-base-special-fmod' );

var x;
var y;
var i;

for ( i = 0; i < 100; i++ ) {
    x = round( randu() * 10.0 );
    y = round( randu() * 10.0 ) - 5.0;
    console.log( '%d^%d = %d', x, y, fmod( x, y ) );
}
```

</section>

<!-- /.examples -->

<!-- C interface documentation. -->

* * *

<section class="c">

## C APIs

<!-- Section to include introductory text. Make sure to keep an empty line after the intro `section` element and another before the `/section` close. -->

<section class="intro">

</section>

<!-- /.intro -->

<!-- C usage documentation. -->

<section class="usage">

### Usage

```c
#include "stdlib/math/base/special/fmod.h"
```

#### stdlib_base_fmod( x, y )

Evaluates the modulus function.

```c
double out = stdlib_base_fmod( 8.9, 3.0 );
// returns 2.9

out = stdlib_base_fmod( 4.0, 2.0 );
// returns 0.0
```

The function accepts the following arguments:

-   **x**: `[in] double` dividend.
-   **y**: `[in] double` divisor.

```c
double stdlib_base_fmod( const double x, const double y );
```

</section>

<!-- /.usage -->

<!-- C API usage notes. Make sure to keep an empty line after the `section` element and another before the `/section` close. -->

<section class="notes">

</section>

<!-- /.notes -->

<!-- C API usage examples. -->

<section class="examples">

### Examples

```c
#include "stdlib/math/base/special/fmod.h"
#include <stdlib.h>
#include <stdio.h>

int main( void ) {
    double out;
    double x;
    double y;
    int i;

    for ( i = 0; i < 100; i++ ) {
        x = ( ( (double)rand() / (double)RAND_MAX ) * 10.0 );
        y = ( ( (double)rand() / (double)RAND_MAX ) * 10.0 ) - 5.0;
        out = stdlib_base_fmod( x, y );
        printf( "fmod(%lf, %lf) = %lf\n", x, y, out );
    }
}
```

</section>

<!-- /.examples -->

</section>

<!-- /.c -->

<!-- Section for related `stdlib` packages. Do not manually edit this section, as it is automatically populated. -->

<section class="related">

</section>

<!-- /.related -->

<!-- Section for all links. Make sure to keep an empty line after the `section` element and another before the `/section` close. -->


<section class="main-repo" >

* * *

## Notice

This package is part of [stdlib][stdlib], a standard library for JavaScript and Node.js, with an emphasis on numerical and scientific computing. The library provides a collection of robust, high performance libraries for mathematics, statistics, streams, utilities, and more.

For more information on the project, filing bug reports and feature requests, and guidance on how to develop [stdlib][stdlib], see the main project [repository][stdlib].

#### Community

[![Chat][chat-image]][chat-url]

---

## Copyright

Copyright &copy; 2016-2024. The Stdlib [Authors][stdlib-authors].

</section>

<!-- /.stdlib -->

<!-- Section for all links. Make sure to keep an empty line after the `section` element and another before the `/section` close. -->

<section class="links">

[npm-image]: http://img.shields.io/npm/v/@stdlib/math-base-special-fmod.svg
[npm-url]: https://npmjs.org/package/@stdlib/math-base-special-fmod

[test-image]: https://github.com/stdlib-js/math-base-special-fmod/actions/workflows/test.yml/badge.svg?branch=main
[test-url]: https://github.com/stdlib-js/math-base-special-fmod/actions/workflows/test.yml?query=branch:main

[coverage-image]: https://img.shields.io/codecov/c/github/stdlib-js/math-base-special-fmod/main.svg
[coverage-url]: https://codecov.io/github/stdlib-js/math-base-special-fmod?branch=main

<!--

[dependencies-image]: https://img.shields.io/david/stdlib-js/math-base-special-fmod.svg
[dependencies-url]: https://david-dm.org/stdlib-js/math-base-special-fmod/main

-->

[chat-image]: https://img.shields.io/gitter/room/stdlib-js/stdlib.svg
[chat-url]: https://app.gitter.im/#/room/#stdlib-js_stdlib:gitter.im

[stdlib]: https://github.com/stdlib-js/stdlib

[stdlib-authors]: https://github.com/stdlib-js/stdlib/graphs/contributors

[umd]: https://github.com/umdjs/umd
[es-module]: https://developer.mozilla.org/en-US/docs/Web/JavaScript/Guide/Modules

[deno-url]: https://github.com/stdlib-js/math-base-special-fmod/tree/deno
[deno-readme]: https://github.com/stdlib-js/math-base-special-fmod/blob/deno/README.md
[umd-url]: https://github.com/stdlib-js/math-base-special-fmod/tree/umd
[umd-readme]: https://github.com/stdlib-js/math-base-special-fmod/blob/umd/README.md
[esm-url]: https://github.com/stdlib-js/math-base-special-fmod/tree/esm
[esm-readme]: https://github.com/stdlib-js/math-base-special-fmod/blob/esm/README.md
[branches-url]: https://github.com/stdlib-js/math-base-special-fmod/blob/main/branches.md

[modulus-function]: https://en.wikipedia.org/wiki/Remainder

<!-- <related-links> -->

<!-- </related-links> -->

</section>

<!-- /.links -->