---
layout: docs
title: Customization options
group: getting-started
---

Material Design for Bootstrap 4 is designed to be customized via Sass variables. You may customize any Bootstrap or MDB variable. 

{% callout info %}
The following assumes you have [setup your Build tools](../build-tools)
{% endcallout %}

{% callout warning %}
If overriding a variable via Sass, ensure that your are `@import`ing the _underscored_ file `_core.scss` **not** the main file used for distributions.  For more information see this [StackOverflow post](http://stackoverflow.com/a/25191403/2363935). 
{% endcallout %}

Here are some ways to customize:

## 1. (Recommended) Include the source in your application

Installing via Bower, customizing MDB is a breeze.  
 
1. Add `bootstrap-material-design` as a dependeny to your `bower.json`
1. `bower install`
1. In your application's Sass, redefine any customized variable _before_ `@import`ing bootstrap material design from your bower dependency directory.  For example:

~~~~~~~~
$brand-primary: #3f51b5;         // bootstrap variable
$mdb-label-color-focus: #303f9f; // mdb variable

@import "../bower_components/bootstrap-material-design/scss/core"; // make sure to use _core.scss!
~~~~~~~~


## 2. Download the source and change/compile

{% callout warning %}
This method is not recommended because it may be difficult to use source control **and** keep up to date with new releases.  Please consider the recommended method above. 
{% endcallout %}

1. Download the source via bower or otherwise
2. Change any of the variables
3. Run `grunt dist`
