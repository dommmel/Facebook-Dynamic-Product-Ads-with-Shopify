# Implementing the (new) Facebook pixel in your Shopify theme

This documentation complements the the general guide: "[Setting up Dynamic Product Ads on Facebook (with Shopify)](http://shopify.flexify.net/facebook-dynamic-product-ads-shopify/)". Please make sure to read it before continuing.


Theme name       | Add-To-Cart button selector | Code to extract the variant ID
---------------- | ----------------------------|--------------------------------
Launchpad-Star   | ``$("#AddToCart")``         | ``$( "select#productSelect option:selected").val()``
[Minimal](https://themes.shopify.com/themes/minimal)   | ``$("#AddToCart")``         | ``$( "select#productSelect option:selected").val()``

## Links
* https://apps.shopify.com/facebook-product-catalog
* https://www.facebook.com/business/help/952192354843755
* http://shopify.flexify.net/facebook-dynamic-product-ads-shopify/
* http://shopify.flexify.net/shopify-facebook-product-feed-app-troubleshooting-faq/

## Can I contribute to this documentation?

Absolutely! We'd love to hear from you if you
* successfulyl implemented the Facebook pixel for a shopify theme that is not listed here
* found an error typo in the existing documentation or
* want to suggest an edit to make things clearer

### How do I contribute?
PLease use [Pull Requests](https://help.github.com/articles/using-pull-requests/) to add your changes and additions to this guide.
