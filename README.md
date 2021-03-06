<div style="text-align:center">
<a href="http://timber.github.io/timber"><img src="http://i.imgur.com/PbEwvZ9.png" style="display:block; margin:auto; width:100%; max-width:100%"/></a>
</div>

By [Jared Novack](https://github.com/jarednova) ([@jarednova](https://twitter.com/jarednova)), [Lukas Gächter](https://github.com/gchtr) ([@lgaechter](https://twitter.com/lgaechter)), [Linda Gorman](https://github.com/lggorman) ([@lggorman](https://twitter.com/lggorman)) and [Upstatement](https://twitter.com/upstatement)


[![Build Status](https://img.shields.io/travis/timber/timber/master.svg?style=flat-square)](https://travis-ci.org/timber/timber)
[![Coverage Status](https://img.shields.io/coveralls/timber/timber.svg?style=flat-square)](https://codecov.io/gh/timber/timber)
[![Dependency Status](https://www.versioneye.com/user/projects/574e40e6e298f30048059b9f/badge.svg?style=flat-square)](https://www.versioneye.com/user/projects/574e40e6e298f30048059b9f)
[![Scrutinizer Code Quality](https://img.shields.io/scrutinizer/g/timber/timber.svg?style=flat-square)](https://scrutinizer-ci.com/g/timber/timber/?branch=master)
[![Latest Stable Version](https://img.shields.io/packagist/v/timber/timber.svg?style=flat-square)](https://packagist.org/packages/timber/timber)
[![WordPress Download Count](https://img.shields.io/wordpress/plugin/dt/timber-library.svg?style=flat-square)](https://wordpress.org/plugins/timber-library/)
[![Join the chat at https://gitter.im/timber/timber](https://img.shields.io/gitter/room/timber/timber.svg?style=flat-square)](https://gitter.im/timber/timber?utm_source=badge&utm_medium=badge&utm_campaign=pr-badge&utm_content=badge)
[![WordPress Rating](https://img.shields.io/wordpress/plugin/r/timber-library.svg?style=flat-square)](https://wordpress.org/support/plugin/timber-library/reviews/)


### Because WordPress is awesome, but the_loop isn't
Timber helps you create fully-customized WordPress themes faster with more sustainable code. With Timber, you write your HTML using the [Twig Template Engine](http://twig.sensiolabs.org/) separate from your PHP files.

This cleans-up your theme code so, for example, your php file can focus on being the data/logic, while your twig file can focus 100% on the HTML and display.

This is what Timber's `.twig` files look like:

```twig
{% extends "base.twig" %}
{% block content %}
  <h1 class="big-title">{{ foo }}</h1>
  <h2 class="post-title">{{ post.title }}</h2>
  <img src="{{ post.thumbnail.src }}" />
  <div class="body">
	{{ post.content }}
  </div>
{% endblock %}
```
Once Timber is installed and activated in your plugin directory, it gives any WordPress theme the ability to take advantage of the power of Twig and other Timber features.

### Looking for docs?
* [Timber Documentation](https://github.com/timber/timber/wiki)
* [Twig Reference](http://twig.sensiolabs.org/doc/templates.html)
* [Video Tutorials](https://github.com/timber/timber/wiki/Video-Tutorials)
* [Overview / Getting Started Guide](https://github.com/timber/timber/wiki/getting-started)

* * *

### Installation

The GitHub version of Timber requires [Composer](https://getcomposer.org/download/). If you'd prefer one-click installation, you should use the [WordPress.org](https://wordpress.org/plugins/timber-library/) version.

```shell
composer require timber/timber
```

If your theme is not setup to pull in Composer's autoload file, you will need to

```php
require_once(__DIR__ . '/vendor/autoload.php');
```

at the top of your `functions.php` file.

Initialize Timber with
```php
$timber = new \Timber\Timber();
```
* * *

### Mission Statement
Timber is a tool for developers who want to translate their HTML into high-quality WordPress themes through an intuitive, consistent and fully-accessible interface.
* **Intuitive**: The API is written to be user-centric around a programmer's expectations.
* **Consistent**: All WordPress objects can be accessed through polymorphic properties like slug, ID and name.
* **Accessible**: No black boxes. Every effort is made so the developer has access to 100% of their HTML.

#### What does it look like?
Nothing. Timber is meant for you to build a theme on. Like the [Starkers](https://github.com/viewportindustries/starkers) or [Boilerplate theme](https://github.com/zencoder/html5-boilerplate-for-wordpress) it comes style-free, because you're the style expert. Instead, Timber handles the logic you need to make a kick-ass looking site.

#### Who is it good for?
Timber is great for any WordPress developer who cares about writing good, maintainable code. It helps teams of designers and developers working together. At [Upstatement](http://upstatement.com) we made Timber because while our entire team needs to participate in building WordPress sites, not everyone knows the ins-and-outs of the_loop(),  codex and PHP (nor should they). With Timber your best WordPress dev can focus on building the .php files with requests from WordPress and pass the data into .twig files. Once there, designers can easily mark-up data and build out a site's look-and-feel.

#### Related Projects
* [**Timber Starter Theme**](https://github.com/timber/starter-theme) The "_s" of Timber to give you an easy start to the most basic theme you can build upon and customize.
* [**Timber Debug Bar**](https://github.com/timber/debug-bar-timber) Adds a debug bar panel that will show you which template is in-use and the data sent to your twig file.
* [**TimberPhoton**](https://github.com/slimndap/TimberPhoton) Plug-in to use JetPack's free Photon image manipulation and CDN with Timber.
* [**Timber CLI**](https://github.com/nclud/wp-timber-cli) A CLI for Timber.
* [**Timber Sugar**](https://github.com/timber/sugar) A catch-all for goodies to use w Timber.
* [**Timmy**](https://github.com/MINDKomm/Timmy) Advanced image manipulation for Timber.
* [**Twig**](https://github.com/fabpot/Twig) The template language used by Timber.
* [**Pine**](https://github.com/azeemhassni/pine) A CLI installer for timber

#### Projects that use Timber
* [**Gantry5**](https://wordpress.org/plugins/gantry5/) a framework for theme development
* [**Branch**](https://github.com/JeyKeu/branch/) Bootstrap + Timber = Branch starter theme!

#### Helpful Links
* [**CSS Tricks**](https://css-tricks.com/timber-and-twig-reignited-my-love-for-wordpress/) introduction to Timber by [@tjFogarty](https://github.com/tjFogarty)
* [**Twig for Timber Cheatsheet**](http://notlaura.com/the-twig-for-timber-cheatsheet/) by [@laras126](https://github.com/laras126)
* [**TutsPlus**](http://code.tutsplus.com/articles/kick-start-wordpress-development-with-twig-introduction--cms-24781) A guide to getting started by [@ahmadawais](https://github.com/ahmadawais)

#### Support
Please post on [StackOverflow under the "Timber" tag](http://stackoverflow.com/questions/tagged/timber). Please use GitHub issues only for specific bugs, feature requests and other types of issues.

#### Should I use it?
It's MIT-licensed, so please use in personal or commercial work. Just don't re-sell it. Timber is used on [hundreds of sites](http://timber.github.io/timber/#showcase) (and tons more we don't know about)

#### Contributing
Read the [contributor guidelines](https://github.com/timber/timber/wiki#contributing) in the wiki.


## [Documentation](http://timber.github.io/timber/)

Documentation for Timber classes and functions is [auto generated](https://github.com/jarednova/PHP-Markdown-Documentation-Generator), so any changes to the object reference docs should be made by editing the function's DocBlock.  To make a change to one of the guides, edit the relevant file in the `docs` directory.

#### To publish docs:

1. `composer install` if not already run
2. Clone the [timber/slate](https://github.com/timber/slate) repo at the same directory level as Timber
3. From the root of the slate directory, run these commands:
```bash
sh publish-docs.sh
```



