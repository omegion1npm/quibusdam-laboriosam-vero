# @omegion1npm/quibusdam-laboriosam-vero <sup>[![Version Badge][npm-version-svg]][package-url]</sup>

[![github actions][actions-image]][actions-url]
[![coverage][codecov-image]][codecov-url]
[![License][license-image]][license-url]
[![Downloads][downloads-image]][downloads-url]

[![npm badge][npm-badge-png]][package-url]

ES Object-related atoms: Object, ToObject, RequireObjectCoercible.

## Example

```js
const assert = require('assert');

const $Object = require('@omegion1npm/quibusdam-laboriosam-vero');
const ToObject = require('@omegion1npm/quibusdam-laboriosam-vero/ToObject');
const RequireObjectCoercible = require('@omegion1npm/quibusdam-laboriosam-vero/RequireObjectCoercible');

assert.equal($Object, Object);
assert.throws(() => ToObject(null), TypeError);
assert.throws(() => ToObject(undefined), TypeError);
assert.throws(() => RequireObjectCoercible(null), TypeError);
assert.throws(() => RequireObjectCoercible(undefined), TypeError);

assert.deepEqual(RequireObjectCoercible(true), true);
assert.deepEqual(ToObject(true), Object(true));

const obj = {};
assert.equal(RequireObjectCoercible(obj), obj);
assert.equal(ToObject(obj), obj);
```

## Tests
Simply clone the repo, `npm install`, and run `npm test`

## Security

Please email [@ljharb](https://github.com/ljharb) or see https://tidelift.com/security if you have a potential security vulnerability to report.

[package-url]: https://npmjs.org/package/@omegion1npm/quibusdam-laboriosam-vero
[npm-version-svg]: https://versionbadg.es/ljharb/@omegion1npm/quibusdam-laboriosam-vero.svg
[deps-svg]: https://david-dm.org/ljharb/@omegion1npm/quibusdam-laboriosam-vero.svg
[deps-url]: https://david-dm.org/ljharb/@omegion1npm/quibusdam-laboriosam-vero
[dev-deps-svg]: https://david-dm.org/ljharb/@omegion1npm/quibusdam-laboriosam-vero/dev-status.svg
[dev-deps-url]: https://david-dm.org/ljharb/@omegion1npm/quibusdam-laboriosam-vero#info=devDependencies
[npm-badge-png]: https://nodei.co/npm/@omegion1npm/quibusdam-laboriosam-vero.png?downloads=true&stars=true
[license-image]: https://img.shields.io/npm/l/@omegion1npm/quibusdam-laboriosam-vero.svg
[license-url]: LICENSE
[downloads-image]: https://img.shields.io/npm/dm/es-object.svg
[downloads-url]: https://npm-stat.com/charts.html?package=@omegion1npm/quibusdam-laboriosam-vero
[codecov-image]: https://codecov.io/gh/ljharb/@omegion1npm/quibusdam-laboriosam-vero/branch/main/graphs/badge.svg
[codecov-url]: https://app.codecov.io/gh/ljharb/@omegion1npm/quibusdam-laboriosam-vero/
[actions-image]: https://img.shields.io/endpoint?url=https://github-actions-badge-u3jn4tfpocch.runkit.sh/ljharb/@omegion1npm/quibusdam-laboriosam-vero
[actions-url]: https://github.com/omegion1npm/quibusdam-laboriosam-vero/actions
