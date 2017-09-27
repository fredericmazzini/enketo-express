Custom Widgets
================

Since version .... it is possible to add your own widgets to Enketo Express without forking Enketo Express.

### Create your widget in its own repo

See [this guidance] for creating Enketo widgets. The simplest widget has just 1 file, either: a `[NAME}.js` or `[NAME].scss` file. If it has both (a common situation), make sure they have the same file name.

An example of a custom KoBoToolbox widget (for a particular client) is [here]().


### Install your widget

After installing enketo express, install your custom widget manually. A convenient way may be to use npm with a github url, e.g.

```bash
npm install https://github.com/kobotoolbox/image-map-customization-widget.git
```


### Add the widget to the Enketo Express installation

In your config.json `"widgets"` item add your widget using the relative (to the config.json file) URL, e.g.

```json
{
    ...
    "widgets": [......., '../../node_modules/imag-map-customization-widget/image-customization']
    ...
}

Use the filename without extension in the path.
