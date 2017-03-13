# TODO

## Miscellaneous

*   Tip: Apart Profiel / gebruiker in Chrome zonder plugins
*   Display skeleton screens instead of loading indicators
*   [Use gzip compression on assets](http://softstribe.com/wordpress/enable-gzip-compression-in-wordpress/)

## HTTP optimisation

### HTTP/1

*   Concatenate
*   Icon fonts
*   Domain Sharding

### HTTP/2

*   Don’t concatenate
*   No icon fonts
*   No Domain Sharding

## Audits

*   [PageSpeed](https://developers.google.com/speed/pagespeed/insights/)
*   [WebPageTest](https://www.webpagetest.org)
*   [Chrome Dev Tools](https://developer.chrome.com/devtools)
*   [Chrome Audits](https://developer.chrome.com/extensions/experimental_devtools_audits)

## Image performance

*   [client hints](http://httpwg.org/http-extensions/client-hints.html)
*   [`srcset`](https://css-tricks.com/responsive-images-youre-just-changing-resolutions-use-srcset/) and [`sizes`](https://developer.mozilla.org/en-US/docs/Web/HTML/Element/img#Example_4_Using_the_srcset_and_sizes_attributes)
*   [`<picture>` element](https://developer.mozilla.org/en-US/docs/Web/HTML/Element/picture)

## Caching

*   [gulp-rev](https://github.com/sindresorhus/gulp-rev)
    — Static asset revisioning by appending content hash to filenames

## Minify

### CSS

*   [clean-css](https://github.com/jakubpawlowicz/clean-css)
    — Fast and efficient CSS optimizer for node.js and the Web
    — Remove unused css files / use cascading

### HTML

*   [html-minifier](https://github.com/kangax/html-minifier)
    — Javascript-based HTML compressor/minifier
    — Remove unused js files

### JavaScript

*   [Uglify](https://github.com/mishoo/UglifyJS2)
    — JavaScript parser / mangler / compressor / beautifier toolkit
    

### Fonts

### Images

*   Downsize images with Adobe PhotoShop, by saving for web

### Perceived Performance

*   [Facebook content placeholder](http://cloudcannon.com/deconstructions/2014/11/15/facebook-content-placeholder-deconstruction.html)

## Server-side optimisation
 
*  Upgrade PHP to version 7. [It's much faster.](http://blog.wpoven.com/2016/03/31/php-5-6-vs-php-7-wordpress-sites-nginx/)

### Void Space

*   Set min-height for <div class="container-wrap"/> in order to stop the footer from beingat the top of the page onload.
