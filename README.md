# MediaType
![Packagist Version](https://img.shields.io/packagist/v/neoncitylights/media-type)
![GitHub](https://img.shields.io/github/license/neoncitylights/php-media-type)
[![Build Status](https://github.com/neoncitylights/php-media-type/actions/workflows/php.yml/badge.svg?branch=main)](https://github.com/neoncitylights/php-media-type/actions/workflows/php.yml)

**MediaType** is a PHP library for dealing with IANA media types as entities.

## Install
```bash
composer require neoncitylights/media-type
```

## Usage
```php
<?php

use Neoncitylights\MediaType\MediaType;

$mediaType = MediaType::newFromString( 'text/plain;charset=UTF-8' );

print( $mediaType->getType() );
// 'text'

print( $mediaType->getSubType() );
// 'plain'

print( $mediaType->getEssence() );
// 'text/plain'

print( $mediaType->getParameterValue( 'charset' ) );
// 'UTF-8'
```

## License
MediaType is licensed under the [MIT license](/LICENSE).

## References
* Freed, N., I., &amp; Borenstein, N. (2016, November). Multipurpose Internet Mail Extensions (MIME) Part Two: Media Types. Retrieved October 29, 2020, from https://tools.ietf.org/html/rfc2046
* Freed, N., Innosoft, &amp; Borenstein, N. (1996, November). Multipurpose Internet Mail Extensions (MIME) Part One: Format of Internet Message Bodies. Retrieved October 29, 2020, from https://tools.ietf.org/html/rfc2045
* Freed, N., O., Klensin, J., Hansen, T., &amp; A. (2013, January). Media Type Specifications and Registration Procedures. Retrieved October 29, 2020, from https://tools.ietf.org/html/rfc6838
* Hemsley, G. P., Barth, A., &amp; Hickson, I. (2020, September 30). MIME Sniffing Standard. Retrieved October 29, 2020, from https://mimesniff.spec.whatwg.org/
