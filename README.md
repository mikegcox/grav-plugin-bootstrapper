# Grav Bootstrapper Plugin


`bootstrapper` is a [Grav](http://github.com/getgrav/grav) plugin that can be used as a dependency for other themes and plugins to load [Bootstrap Framework assets](http://getbootstrap.com/).  The main purpose of this plugins is to allow the Boostrap theme to depend on the bootstrap CSS/JS and allow the plugin to be updated independently of the theme itself.

# Installation

## GPM Installation (Preferred)

The simplest way to install this plugin is via the [Grav Package Manager (GPM)](http://learn.getgrav.org/advanced/grav-gpm).  From the root of your Grav install type:

    bin/gpm install bootstrapper

## Manual Installation 

If for some reason you can't use GPM you can manually install this plugin. Download the zip version of this repository and unzip it under `/your/site/grav/user/plugins`. Then, rename the folder to `bootstrapper`.

You should now have all the plugin files under

	/your/site/grav/user/plugins/bootstrapper

# Usage

To best understand what Bootstrapper plugin provides, you should read through the original [Bootstrap project documentation](http://getbootstrap.com/).

## Configuration

Featherlight is **enabled** but **not active** by default.  You can change this behavior by setting `active: true` in the plugin's configuration.  Simply copy the `user/plugins/bootstrapper/bootstrapper.yaml` into `user/config/plugins/bootstrapper.yaml` and make your modifications.

```
enabled: true                   # Enable / Disable this plugin
always_load: false              # If set to `false` the Theme must have `public $load_bootstrapper_plugin = true;` to add the CSS/JS
mode: production                # Production mode will use the `.min` compressed CSS and JS files
load_core_css: true             # Load the core `bootstrap.css` CSS file
load_theme_css: true            # Load the theme `bootstrap-theme.css` CSS file
load_core_js: true              # Load the core `bootstrap.js` JS file
```
