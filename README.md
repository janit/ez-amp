# eZ AMP Bundle
This is an extension to the eZ Platform CMS that provides Accelerated Mobile Pages (AMP) Support.

Accelerated Mobile Pages is an initiative from Google to speed up mobile browsing. AMP is an open standard based on HTML. It enforces performance by limiting functionality and includes remote caching from Google to allow quick embedded views to search results.

Given Google's continuing dominance search both publishers and CMS vendors need to take AMP into account. This bundle enables <a href="http://ezplatform.com">eZ Platform</a> installations to have quick access to an AMP formatted version of content objects.

## Installation

Installation is similar to most Symfony Bundles:

1. Require using composer
2. Update AppKernel
3. Add header link to content (to make AMP pages discoverable)

After this your content pages' head section should contain a reference to the AMP version:

```
<link rel="amphtml" href="http://example/amp/1" />
```

The AMP version should also contain a canonical link back to the main version of the site:

```
<link rel="canonical" href="http://symfony-cms.net/bolt-cms" />
```

Next if you have not yet done so, verify your site on <a href="https://www.google.com/webmasters/">Google Webmaster tools</a> and follow the state of the AMP validation

## Overriding with bundle inheritance

While this bundle aims to provide valid AMP output by default, it is very crude as it is. If you wish to use this version, you can use <a href="http://symfony.com/doc/current/bundles/inheritance.html">Symfony Bundle Inheritance</a> to override the templates to have a more pleasing outlook.

## Missing features

There are quite a few more things that should be added to the bundle, both on eZ Platform and AMP side, some of which are:

- Configuration of templates
- Configuration of content types to be served as AMP
- Support for JSON-LD metadata
- Support for analytics
- Support for ads
