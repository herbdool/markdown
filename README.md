Markdown filter
========

This is a simple filter module. It handles Markdown, which is a "markup" that is also meant to be as human-readable as possible when left as "source".

INSTALLATION
------------

- Install this module using the official Backdrop CMS instructions at
  https://backdropcms.org/guide/modules

- Go to Configuration > Content authoring > Text formats
  (admin/config/content/formats). For each format on which you wish to add Markdown
  Filter:

  1. Click the "Configure" link.

  2. Under "Enabled filters", check the markdown filter checkbox.

  3. Under "Filter processing order", rearrange the filtering chain to resolve any conflicts. Filters that should be run before Markdown filter includes:
    * Code Filter
    * GeSHI filter for code syntax highlighting
    Filters that should be run after Markdown filter includes:
    * Typogrify
    The "Limit allowed HTML tags" filter is a special case:

    For best security, ensure that it is run after the Markdown filter and that only markup you would like to allow via HTML and/or Markdown is configured to be allowed.

    If you on the other hand want to make sure that all converted Markdown text is perserved, run it before the Markdown filter. Note that blockquoting with Markdown doesn't work in this case since "Limit allowed HTML tags" filter converts the ">" in to ">".

  4. Click the "Save configuration" button.

License
-------

This project is GPL v2 software. See the LICENSE.txt file in this directory for
complete text.

Current Maintainers
-------------------

This module is currently seeking maintainers.

Credits
-------

Ported to Backdrop by Herb van den Dool (https://github.com/herbdool/)

This module was originally written for Drupal (https://drupal.org/project/markdown), based on the Markdown Extras PHP filter by Michel Fortin (http://michelf.ca/projects/php-markdown/extra).
