# VisibleRangePlugin

<md-button class="md-raised md-primary" href="https://photo-sphere-viewer.js.org/api/PSV.plugins.VisibleRangePlugin.html">API Documentation</md-button>

> Locks visible longitude and/or latitude.

This plugin is available in the core `photo-sphere-viewer` package in `dist/plugins/visible-range.js`.

[[toc]]


## Usage

The plugins allow to define `latitudeRange` and `longitudeRange` to lock to viewable zone. It affects manual moves and automatic rotation.

```js
const viewer = new PhotoSphereViewer.Viewer({
  plugins: [
    [PhotoSphereViewer.VisibleRangePlugin, {
      longitudeRange: [-Math.PI / 2, Math.PI / 2],
      latitudeRange : [-Math.PI / 3, Math.PI / 3],
    }],
  ],
});

const visibleRangePlugin = viewer.getPlugin(PhotoSphereViewer.VisibleRangePlugin);

visibleRangePlugin.setLongitudeRange(['0deg', '180deg']);
visibleRangePlugin.setLatitudeRange(null);
```


## Example

TODO


## Configuration

#### `longitudeRange`
- type: `double[]|string[]`
- default: `null`

Visible longitude as two angles.

#### `latitudeRange`
- type: `double[]|string[]`
- default: `null`

Visible latitude as two angles.
