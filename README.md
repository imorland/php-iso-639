# PHP ISO-639
![Tests](https://github.com/imorland/php-iso-639/workflows/tests/badge.svg)
![Coverage](https://img.shields.io/codecov/c/github/imorland/php-iso-639?logo=codecov)
[![Total Download](https://img.shields.io/packagist/dt/ianm/iso-639.svg)](https://packagist.org/packages/ianm/iso-639)
[![Latest Stable Version](https://img.shields.io/packagist/v/ianm/iso-639.svg)](https://packagist.org/packages/ianm/iso-639)

PHP library to convert ISO-639-1 code to language name, based on Wikipedia's [List of ISO 639-1 codes](https://en.wikipedia.org/wiki/List_of_ISO_639-1_codes).

Forked to modify the response for French native to simply 'Français', rather than 'Français, langue française'.

## Installation

Using composer: `composer require ianm/iso-639`

## Usage Example

```php
<?php

required 'src/ISO639.php';
//required 'vendor/autoload.php'; // If using composer

$iso = new IanM\ISO639\ISO639;

// Get language name from ISO-639-1 code
echo $iso->languageByCode1('en'); // English
echo $iso->languageByCode1('id'); // Indonesian
echo $iso->languageByCode1('jv'); // Javanese

// Get native language name from ISO-639-1 code
echo $iso->nativeByCode1('en'); // English
echo $iso->nativeByCode1('id'); // Bahasa Indonesia
echo $iso->nativeByCode1('jv'); // basa Jawa

// Get language name from ISO-639-2t code
echo $iso->languageByCode2t('eng'); // English
echo $iso->languageByCode2t('ind'); // Indonesian
echo $iso->languageByCode2t('jav'); // Javanese

// Get native language name from ISO-639-2t code
echo $iso->nativeByCode2t('eng'); // English
echo $iso->nativeByCode2t('ind'); // Bahasa Indonesia
echo $iso->nativeByCode2t('jav'); // basa Jawa

// Get language name from ISO-639-2b code
echo $iso->languageByCode2b('eng'); // English
echo $iso->languageByCode2b('ind'); // Indonesian
echo $iso->languageByCode2b('jav'); // Javanese

// Get native language name from ISO-639-2b code
echo $iso->nativeByCode2b('eng'); // English
echo $iso->nativeByCode2b('ind'); // Bahasa Indonesia
echo $iso->nativeByCode2b('jav'); // basa Jawa

// Get language name from ISO-639-3 code
echo $iso->languageByCode3('eng'); // English
echo $iso->languageByCode3('ind'); // Indonesian
echo $iso->languageByCode3('jav'); // Javanese

// Get native language name from ISO-639-3 code
echo $iso->nativeByCode3('eng'); // English
echo $iso->nativeByCode3('ind'); // Bahasa Indonesia
echo $iso->nativeByCode3('jav'); // basa Jawa

// Get language array from ISO-639-2b code
echo $iso->getLanguageByIsoCode2b('eng'); // ['en', 'eng', 'eng', 'eng', 'English', 'English']
echo $iso->getLanguageByIsoCode2b('ind'); // ['id', 'ind', 'ind', 'ind', 'Indonesian', 'Bahasa Indonesia']
echo $iso->getLanguageByIsoCode2b('jav'); // ['jv', 'jav', 'jav', 'jav', 'Javanese', 'basa Jawa']
```

## To Do

* Convert language name to ISO-639 code
