# Quando Plugin

The **Quando** Plugin is for [Grav CMS](http://github.com/getgrav/grav).

It exposes business opening hours and other service hours to Grav as a Twig hash. It provides starter templates you might want to copy into your theme, customise, and include.

## Installation

Installing the Quando plugin can be done in one of two ways. The GPM (Grav Package Manager) installation method enables you to quickly and easily install the plugin with a simple terminal command, while the manual method enables you to do so via a zip file.

### GPM Installation (Preferred)

The simplest way to install this plugin is via the [Grav Package Manager (GPM)](http://learn.getgrav.org/advanced/grav-gpm) through your system's terminal (also called the command line).  From the root of your Grav install type:

    bin/gpm install quando

This will install the Quando plugin into your `/user/plugins` directory within Grav. Its files can be found under `/your/site/grav/user/plugins/quando`.

### Manual Installation

To install this plugin, just download the zip version of this repository and unzip it under `/your/site/grav/user/plugins`. Then, rename the folder to `quando`. You can find these files on [GitHub](https://github.com/hughbris/grav-plugin-quando) or via [GetGrav.org](http://getgrav.org/downloads/plugins#extras).

You should now have all the plugin files under

    /your/site/grav/user/plugins/quando

> NOTE: This plugin is a modular component for Grav which requires [Grav](http://github.com/getgrav/grav) and the [Error](https://github.com/getgrav/grav-plugin-error) and [Problems](https://github.com/getgrav/grav-plugin-problems) to operate.

## Configuration

Before configuring this plugin, you should copy the `user/plugins/quando/quando.yaml` to `user/config/plugins/quando.yaml` and only edit that copy.

Here is the default configuration and an explanation of available options:

```yaml
enabled: true
hours: [] # When populated, an indexed array of service hours listings, a complex YAML structure best configured through the Admin dashboard (when the blueprint is done!). One of these listings should be called 'opening' if you want any of the templates to work out of the box.
```

## Usage

It's enabled by default on install but will do nothing unless you use it.

Configure the hours through the Admin plugin is probably simplest. Or copy the [sample YAML](data.sample.yaml) (in fact, you'll have to do that until I add a blueprint for hours).

Copy, customise, and include one of the sample templates, probably start with a simple partial:

* [This week's hours](templates/partials/panel_hours.html.twig) web panel
* [Regular schedule](templates/partials/hours.html.twig)
* [Exceptions list](templates/partials/hours_exceptions.html.twig)

Examples in the wild:

* [QE2 Dental opening hours](https://qe2dental.co.nz/about/opening) page

## Credits

I had this in my original composer.json for some reason: https://github.com/spatie/opening-hours. I'm sorry, I can't remember, but it looks like I have been inspired heavily by this, its API especially.

## To Do

It's all supposed to be in the Issues. (Github make it non-trivial for me to reliably link there in any relative way. I'm sorry for that unfortunate fail. But hey, you can do emojis and fontawesome in markdown - that's important, right?)
