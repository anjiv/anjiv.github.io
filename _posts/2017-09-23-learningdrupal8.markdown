---
layout: post
title:  "Learning Drupal 8 theming"
date:   2017-09-23
categories: anjali update
---

Drupal site can be themed by a single individual or according to one's requirement. Theming is done to make the site more appealing and attractive.

Drupal consist of few core themes that can be used and changed according to the one's requirement or one can also creates it's own custom theme making any of the core themes as base theme.

#### Few core themes available are:
1. Bartik (Default theme)
2. Classy
3. Seven (Default admin theme)
4. Stark
5. Stable

So, one can use these themes as their default theme for building Drupal site.

Now, if someone wants to create it's own custom theme then it is also possible with Drupal.

Steps to create a custom theme :
1. Create a customtheme folder(theme name can be according to one's choice) in the project themes folder.
2. Create a customtheme.info.yml in customtheme folder.
    (This file contains all the information about the theme we have created including it's name, type, base theme that it is using, description about the custom theme, libraries for css and js, and the regions that are created for the pages like header, content, sidebar, footer, etc.)

    ` customtheme.info.yml `
    ``` yml
    name: Customtheme
    type: theme
    base theme: classy
    description: 'A flexible, recolorable theme with many regions and a responsive, mobile-first layout.'

    regions:
      header: Header
      menu: Menu
      page_top: 'Page top'
      page_bottom: 'Page bottom'
      sidebar: Sidebar
      content: Content
      footer: 'Footer'

    libraries:
      - bills/global-styling

    core: '8.x'
    project: 'drupal'
    datestamp: 1493834648
    ```

3. Create a customtheme.libraries.yml in customtheme folder.
    (This file contains all the css and js libraries.)

    ` customtheme.libraries.yml `
    ``` yml
    global-styling:
      version: VERSION
      css:
        style:
          css/styles.css: {}

      js:
        js/script.js: {}

      dependencies:
        - core/jquery
        - core/jquery.ui.dialog

    ```
4. Setup the task runners like Gulp or Grunt and define their task in the respective files.
5. Create different folders for Images, js, css, sass, templates(contains twig templates).
