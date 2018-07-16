# Extra bits for eZ Platform search

[![Build Status](https://img.shields.io/travis/netgen/ezplatform-search-extra.svg?style=flat-square)](https://travis-ci.org/netgen/ezplatform-search-extra)
[![Downloads](https://img.shields.io/packagist/dt/netgen/ezplatform-search-extra.svg?style=flat-square)](https://packagist.org/packages/netgen/ezplatform-search-extra)
[![Latest stable](https://img.shields.io/packagist/v/netgen/ezplatform-search-extra.svg?style=flat-square)](https://packagist.org/packages/netgen/ezplatform-search-extra)
[![License](https://img.shields.io/github/license/netgen/ezplatform-search-extra.svg?style=flat-square)](https://packagist.org/packages/netgen/ezplatform-search-extra)

## Features

Only a short list of features is provided here, see
[documentation](https://netgen-ezplatform-search-extra.readthedocs.io)
for more details.

- [`IsFieldEmpty`](https://github.com/netgen/ezplatform-search-extra/blob/master/lib/API/Values/Content/Query/Criterion/IsFieldEmpty.php) criterion

  This will work only with Solr search engine and it will require initial reindexing after installation.

- [`ObjectStateIdentifier`](https://github.com/netgen/ezplatform-search-extra/blob/master/lib/API/Values/Content/Query/Criterion/ObjectStateIdentifier.php) criterion
- [`SectionIdentifier`](https://github.com/netgen/ezplatform-search-extra/blob/master/lib/API/Values/Content/Query/Criterion/SectionIdentifier.php) criterion
- Support for custom Content subdocuments

  Provides a way to index custom subdocuments to Content document and
  [`SubdocumentQuery`](https://github.com/netgen/ezplatform-search-extra/blob/master/lib/API/Values/Content/Query/Criterion/SubdocumentQuery.php)
  criterion, available in Content search to define grouped conditions for a custom subdocument.

## Installation

To install eZ Platform Search Extra first add it as a dependency to your project:

```sh
composer require netgen/ezplatform-search-extra:^1.0
```

Once the added dependency is installed, activate the bundle in `app/AppKernel.php` file by adding it to the `$bundles` array in `registerBundles()` method, together with other required bundles:

```php
public function registerBundles()
{
    ...

    $bundles[] = new Netgen\Bundle\EzPlatformSearchExtraBundle\NetgenEzPlatformSearchExtraBundle;

    return $bundles;
}
```
