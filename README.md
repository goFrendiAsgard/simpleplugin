# Chimera CMS simple plugin

This is a plugin example for `Chimera CMS`. You can use it as boiler-plate of any other plugin for Chimera CMS.

# How to

## Packing (without publishing)

Packing make your plugin installable by using `npm`. However, the packed package will not be published in `npmjs.com`. This is useful if you want to create private plugin

Here are the steps required to pack a package:

* Make sure you are in this package directory.
* Invoke

  ```bash
  npm pack
  ```
* A new `<your-plugin-name>.tgz` file will be created.

## Publishing

Similar to packing, publishing will also make your plugin installable by using npm. Plus, it will be published in npmjs.com. So, as long as you are connected to the internet, you will be able to install plugin anywhere.

Here are the steps required to pack a package:

* Make sure you have set your npm credentials.
* Make sure you are in this package directory.
* Invoke

  ```bash
  npm publish
  ```
* Your plugin will be published.

## Installing

To install your plugin, please make sure you are already in `Chimera CMS` directory

### Installing a packed plugin

You can install a packed plugin by invoking:

```bash
npm install <path-to-your-plugin>.tgz
```

### Installing a published plugin

You can install a published plugin by invoking:

```bash
npm install <plugin-name>
```

## Uninstalling

To uninstall your plugin, please make sure you are already in `Chimera CMS` directory.

Then, you can invoke the following command:

```bash
npm uninstall <plugin-name>
```

# What's included on Simple Plugin

* A static page
  - `migrations/simpleplugin-0.001-static-page.chiml`: Migration file to create a route to the static file 
  - `views/example.js`: static page's view
* CCK entities
  - `migrations/simpleplugin-0.002-cck.chiml`: Migration file to create two CCK structures, `hogu` and `servants`
  - `migrations/simpleplugin-0.004-noble-phantasm.chiml`: Migration file to fill the `hogu` CCK Entity with several data
  - `migrations/simpleplugin-0.005-servant.chiml`: Migration file to fill the `servants` CCK Entity with several data
* Navigation link
  - `migrations/simpleplugin-0.003-navigation.chiml`: Migration file to modify navigation configuration, so that the static page and the CCK entities will be accessible from the top/left navigation bar.