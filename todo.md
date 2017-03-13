# TODO

## Miscellaneous

*   Tip: Apart Profiel / gebruiker in Chrome zonder plugins
*   Display skeleton screens instead of loading indicators
*   [Use gzip compression on assets](http://softstribe.com/wordpress/enable-gzip-compression-in-wordpress/)
*   Use a CDN (for example [MaxCDN](https://www.maxcdn.com/)) for faster content delivery
*   [Text in Image :frowning:](http://ux.stackexchange.com/questions/41593/is-the-usage-of-text-embedded-in-an-image-a-bad-practice-for-very-controlled-us)
*   Use HTTPS to serve images (console gives 'insecure content' warning)
*   Store PDF files on https://aws.amazon.com/s3/
*   [Reduce the number of plugins you use on your site] (https://hostingfacts.com/how-to-speed-up-your-website/#1) 
*   Fallbacks for HTML, CSS and JavaScript
*   Reduce inline javascript
*   Eliminate render-blocking JavaScript and CSS in above-the-fold content
*   Minimize cookie size
*   Reduce Latency with a Content Delivery Network (CDN)

## HTTP optimisation

### HTTP/1

*   Concatenate
*   Icon fonts
*   Domain Sharding
*   Reduce external HTTP requests

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
*   Compress images with [TinyPNG](https://tinypng.com/) or [TinyJPG](https://tinyjpg.com/) to reduce filesizes before upload
    * TinyPNG also have a WordPress plugin that works with the API of TinyPNG, so when you upload a image in WordPress it will also automatically compressed for every image size WordPress generates.
*   [Lazyload images](http://verlok.github.io/lazyload/)
*   Manually compress images with https://compressor.io
*   Use sprites (Les requests) for small images

## JavaScript performance

*   Prevent multiple versions and requests for jQuery. The page itself requests jQuery, but the plugins also include different versions.
*   Get rid of js files that aren't used. JS takes up ~50% of the requests and bytes

## Caching

*   [gulp-rev](https://github.com/sindresorhus/gulp-rev)
    — Static asset revisioning by appending content hash to filenames
*   Caching plugin for Wordpress https://www.w3-edge.com/products/w3-total-cache
*   Use [Varnish Caching](http://varnishspeedtest.nl/?url=https%3A%2F%2Fwww.cmd-amsterdam.nl%2Fcmd%2F) for up to 300% speed increase
*   [WP Rocket](https://wp-rocket.me/) - Most advanced caching plugin for WordPress.

## Minify

*   Minify plugin for WordPress [Autoptimize](https://wordpress.org/plugins/autoptimize/): HTML, CSS and JS. Also have option for above the fold and critical CSS.

### CSS

*   [clean-css](https://github.com/jakubpawlowicz/clean-css)
    — Fast and efficient CSS optimizer for node.js and the Web
*   Remove unused css files / use cascading
*   Don't use unnecessary classes
*   Remove inline css and add it in a seperate file
*   Critical CSS
*   Combine external CSS files. Merge them into as few files as possible
*   Remove unused CSS rules. A lot of rules aren't used is the CSS files.
*   [Prioritize above-the-fold content](https://developers.google.com/speed/docs/insights/PrioritizeVisibleContent) — Show the content that is first visible first
*   Remove the woocommerence css stylesheets

### HTML

*   [html-minifier](https://github.com/kangax/html-minifier)
    — Javascript-based HTML compressor/minifier
*   Remove unused js files

### JavaScript

*   [Uglify](https://github.com/mishoo/UglifyJS2)
    — JavaScript parser / mangler / compressor / beautifier toolkit
*   Optimise script loading (defer attribute in script src) [source](https://www.w3schools.com/tags/att_script_defer.asp)
*   What if no javascript is loaded? (fallback for menu? maybe?)
*   Use attribute 'defer' if you want to place scripts in the head
*   Avoid blocking scripts, so use defer/async or put your code at the bottom 

### Fonts

*   Subset fonts using fontsquirrel
*   load fallback font before custom font show content faster
    https://github.com/bramstein/fontfaceobserver
*   Enhance font after async loading to prevent FOIT
*   Replace font-awesome with SVG-icons

### Images

*   Downsize images with Adobe PhotoShop, by saving for web
*   [Combine Your Background Images into Image Sprites] (https://hostingfacts.com/how-to-speed-up-your-website/#14) — reducing requests
*   Save images as WEBP https://developers.google.com/speed/webp/gallery1
*   Loading the logo's inline
*   Use SVG for images, although Wordpress doesn't support this due to [security isues](https://www.bjornjohansen.no/svg-in-wordpress)
*   Use Kraken.io (https://kraken.io/) to compress images
*   Serve Scaled Images

### Perceived Performance

*   [Facebook content placeholder](http://cloudcannon.com/deconstructions/2014/11/15/facebook-content-placeholder-deconstruction.html)
*   Add animations to improve the perceived performance. Let the user know it's loading. (http://tobiasahlin.com/spinkit/)

## Server-side optimisation

*   Upgrade PHP to version 7. [It's much faster.](http://blog.wpoven.com/2016/03/31/php-5-6-vs-php-7-wordpress-sites-nginx/)
*   Enable the nginx content cache. [Documentation](https://www.nginx.com/resources/admin-guide/content-caching/)

### Void Space

*   Set min-height for <div class="container-wrap"/> in order to stop the footer from beingat the top of the page onload.

### WordPress
*   Build custom theme
*   Reserve space for the full size image on the home page. When the page is loaded, the content won't jump around
