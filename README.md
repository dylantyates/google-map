google-map
==========

This fork is using [v2.0.3](https://github.com/GoogleWebComponents/google-map/tree/v2.0.3) with the fix for [#407](https://github.com/GoogleWebComponents/google-map/issues/407).

```js
    _clearListener: function(name) {
      // Fixes TypeError: Cannot read property of undefined
      if (this._listeners && this._listeners[name]) {
             google.maps.event.removeListener(this._listeners[name]);
             this._listeners[name] = null;
           }
    }
```


[![Published on webcomponents.org](https://img.shields.io/badge/webcomponents.org-published-blue.svg)](https://beta.webcomponents.org/element/GoogleWebComponents/google-map)

<!---
```
<custom-element-demo>
  <template>
    <script src="../webcomponentsjs/webcomponents-lite.min.js"></script>
    <link rel="import" href="google-map.html">
    <style>
      google-map {
        height: 300px;
      }
    </style>
    <next-code-block></next-code-block>
  </template>
</custom-element-demo>
```
-->
```html
<google-map fit-to-markers api-key="AIzaSyD3E1D9b-Z7ekrT3tbhl_dy8DCXuIuDDRc">
  <google-map-marker latitude="37.78" longitude="-122.4" draggable="true"></google-map-marker>
</google-map>
```

Breaking changes:
 * Markers added to `<google-map>` must now specify `slot="markers"` to be added correctly.
