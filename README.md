# Implementing the (new) Facebook pixel in your Shopify theme

This documentation complements the the general guide: "[Setting up Dynamic Product Ads on Facebook (with Shopify)](http://shopify.flexify.net/facebook-dynamic-product-ads-shopify/)". Please make sure to read it before continuing.

## Code bits

Theme name       | Add-To-Cart button selector | Code to extract the variant ID
---------------- | ----------------------------|--------------------------------
Launchpad-Star   | ``$("#AddToCart")``         | ``$( "select#productSelect option:selected").val()``
[Minimal](https://themes.shopify.com/themes/minimal) <br> _* not an ajax shopping cart_  | ``$("#AddToCart")``  |``$( "select#product-select option:selected").val()``
[New Standard](https://themes.shopify.com/themes/new-standard)  <br> _* not an ajax shopping cart_ | ``$("#add")`` | ``$( "select#product-select option:selected").val()``
[Parallax](https://themes.shopify.com/themes/parallax) | ``$(".add_to_cart").first()``| ``$(".product_form option:selected").first().val()``

_*not an ajax shopping cart_

Some themes do not use an ajax shopping cart. In that case a customers gets redirected to the shopping cart immediately  after she clicks the buy button on the product page. This is a common reason for the Facebook pixels to fire inconsistently because the page redirects or reloads before the tracking event reaches Facebook's servers. Make sure your page does not redirect or reload for at least 200ms after the event happens. In some cases a delay of 500ms is necessary.

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
