Iris Setosa Petal
===
[![NPM version][npm-image]][npm-url] [![Build Status][travis-image]][travis-url] [![Coverage Status][codecov-image]][codecov-url] [![Dependencies][dependencies-image]][dependencies-url]

> Edgar Anderson's [data](https://en.wikipedia.org/wiki/Iris_flower_data_set) for *Iris setosa* petal length and width.


## Installation

``` bash
$ npm install datasets-iris-setosa-petal
```

For use in the browser, use [browserify](https://github.com/substack/node-browserify).


## Usage

``` javascript
var data = require( 'datasets-iris-setosa-petal' );
```

#### data.len

Edgar Anderson's [data](https://en.wikipedia.org/wiki/Iris_flower_data_set) for *Iris setosa* [petal length](https://github.com/datasets-io/iris-setosa-petal-length).

``` javascript
console.log( data.len );
// returns [ 1.4, 1.4, 1.3, ... ]
```

#### data.width

Edgar Anderson's [data](https://en.wikipedia.org/wiki/Iris_flower_data_set) for *Iris setosa* [petal width](https://github.com/datasets-io/iris-setosa-petal-width).

``` javascript
console.log( data.width );
// returns [ 0.2, 0.2, 0.2, ... ]
```


## Examples

``` javascript
var toMatrix = require( 'compute-to-matrix' ),
	mean = require( 'compute-mean' ),
	variance = require( 'compute-variance' ),
	data = require( 'datasets-iris-setosa-petal' );

// Convert the data arrays to a matrix:
var mat = toMatrix( [ data.len, data.width ] );

// Calculate the sample mean along the rows:
console.log( mean( mat ).toString() );

// Calculate the sample variance along the rows:
console.log( variance( mat ).toString() );
```

To run the example code from the top-level application directory,

``` bash
$ node ./examples/index.js
```


## References

*	Anderson, Edgar (1935). "The irises of the Gaspe Peninsula," *Bulletin of the American Iris Society*, __59__, 2–5.
*	Fisher, Ronald A. (1936). "The use of multiple measurements in taxonomic problems." *Annals of Eugenics*, __7__, Part II, 179–188.


## See Also

*	[iris](https://github.com/datasets-io/iris)
*	[iris-setosa](https://github.com/datasets-io/iris-setosa)
*	[iris-setosa-petal-length](https://github.com/datasets-io/iris-setosa-petal-length)
*	[iris-setosa-petal-width](https://github.com/datasets-io/iris-setosa-petal-width)


## Tests

### Unit

Unit tests use the [Mocha](http://mochajs.org/) test framework with [Chai](http://chaijs.com) assertions. To run the tests, execute the following command in the top-level application directory:

``` bash
$ make test
```

All new feature development should have corresponding unit tests to validate correct functionality.


### Test Coverage

This repository uses [Istanbul](https://github.com/gotwarlost/istanbul) as its code coverage tool. To generate a test coverage report, execute the following command in the top-level application directory:

``` bash
$ make test-cov
```

Istanbul creates a `./reports/coverage` directory. To access an HTML version of the report,

``` bash
$ make view-cov
```


---
## License

[MIT license](http://opensource.org/licenses/MIT).


## Copyright

Copyright &copy; 2015. The [Compute.io](https://github.com/compute-io) Authors.


[npm-image]: http://img.shields.io/npm/v/datasets-iris-setosa-petal.svg
[npm-url]: https://npmjs.org/package/datasets-iris-setosa-petal

[travis-image]: http://img.shields.io/travis/datasets-io/iris-setosa-petal/master.svg
[travis-url]: https://travis-ci.org/datasets-io/iris-setosa-petal

[codecov-image]: https://img.shields.io/codecov/c/github/datasets-io/iris-setosa-petal/master.svg
[codecov-url]: https://codecov.io/github/datasets-io/iris-setosa-petal?branch=master

[dependencies-image]: http://img.shields.io/david/datasets-io/iris-setosa-petal.svg
[dependencies-url]: https://david-dm.org/datasets-io/iris-setosa-petal

[dev-dependencies-image]: http://img.shields.io/david/dev/datasets-io/iris-setosa-petal.svg
[dev-dependencies-url]: https://david-dm.org/dev/datasets-io/iris-setosa-petal

[github-issues-image]: http://img.shields.io/github/issues/datasets-io/iris-setosa-petal.svg
[github-issues-url]: https://github.com/datasets-io/iris-setosa-petal/issues
