This plugin is not maintaned for a long time. If you still see it usefull and have any fixes, feel free to submit a pull request!

# Blog plugin for [pimcore](http://www.pimcore.org/) #

## Features ##

*   Entries and categories build on pimcore [data objects](http://www.pimcore.org/wiki/display/PIMCORE/Data+Objects)
*   RSS feed
*   Snippets with categories / calendar / feed links / latest entries
*   Comments provided by [Commenting](https://github.com/rafalgalka/pimcore-plugin-commenting) plugin integration
*   Tags provided by [Tags Field V2](http://www.pimcore.org/resources/extensions/detail/Tagfield) plugin integration

## Setup ##

Just like other Pimcore plugins:

  * [download plugin by composer](https://www.pimcore.org/wiki/display/PIMCORE3/Extension+management+using+Composer)
    or use [Extension Manager](https://github.com/pimcore-extensions/manager)
  * navigate to `Extras -> Extensions` in admin panel
  * enable & install plugin
  * reload admin interface

If everything went smoothly you will find `Blog` custom view just below `Objects` in right panel.
Now you can add some entries/categories.

Create document named eg. `Blog` using defined document type:

![Blog document type](https://raw.github.com/pimcore-extensions/blog/master/docs/screenshots/document_type.png)

**NOTE: If you need Tag Field plugin integration install it first.
Otherwise installer will skip tag field in blog entry class definition.
Of course you can add tag field manualy later.**

### Snippets ###

Plugin provides some snippets that you can place anywhere on your site (eg. sidebar, mainpage):
*   latest entries (Blog/snippet/latest)
*   categories list (Blog/snippet/categories)
*   calendar (Blog/snippet/calendar)
*   links to rss/atom feed (Blog/snippet/feed)

![Blog snippet types](https://raw.github.com/pimcore-extensions/blog/master/docs/screenshots/snippet_types.png)

## Customization ##

You can add/modify/remove entry/category data fields using default pimcore Object Classes interface.

You can overwrite any of default view scripts by copying `Blog/views/scripts/:controller/:action.php`
into `website/views/scripts/blog/:controller/:action.php`.
Your custom view script will be used automatically instead of default one.
This will allow you to update plugin without loosing your project markup.

## Changelog ##
 * 2015-02-21   1.0.5   composer.json - published on [Packagist](https://packagist.org/packages/pimcore-extensions/blog)
 * 2013-06-05   1.0.4   Added predefined document types.
 * 2013-04-14   1.0.3   Fixed installation after changes in pimcore.
 * 2012-12-07   1.0.2   Removed empty js/css paths from plugin.xml
 * 2012-11-26   1.0.1   Added example blog layout. Fixed template overwriting.

## Todo ##
*   Settings management
*   Tag cloud snippet
