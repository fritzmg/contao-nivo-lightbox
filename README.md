Contao Nivo Lightbox
=====================

Contao extension to integrate the [Nivo Lightbox](http://docs.dev7studios.com/jquery-plugins/nivo-lightbox) overlay.

## Usage

Simply activate the `j_nivo_lightbox` template in your page layout under _jQuery_. Do _not_ activate `j_colorbox` or `moo_mediabox` as well! The overlay will work with all links that use the `data-lightbox="..."` parameter.

## Customizing

If you want to use your own custom parameters, simply create your own `j_nivo_lightbox` template and insert your custom options at this line:
```php
// init nivo lightbox
$links.nivoLightbox();
```
Refer to the [Nivo Lightbox documentation](http://docs.dev7studios.com/jquery-plugins/nivo-lightbox) for all available parameters.

## Types

By default, Nivo Lightbox acts as an image overlay. Nivo Lightbox also lets you open an URL via AJAX or iframe. Or you can display existing HTML in the overlay by referencing the id of the HTML element. This extension provides an initiation mechanic, so that most use cases can still be controlled via the `data-lightbox` parameter, as it is common in Contao. 

Show a page via iframe:
```html
<a href="page.html" data-lightbox="iframe">...</a>
```

Load a page via AJAX:
```html
<a href="page.html" data-lightbox="ajax">...</a>
```

Display some HTML element in the overlay:
```html
<a href="#some-element" data-lightbox="inline">...</a>
```

All regular parameters mentioned in the [Nivo Lightbox documentation](http://docs.dev7studios.com/jquery-plugins/nivo-lightbox) should still work as well. If you do not provide any of this in your HTML source, the extension will open any non-image URLs in an iframe by default.
