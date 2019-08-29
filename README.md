# Welcome to Project Atlas

This is a starting point for a front-end web application with an interactive map.
Based on: https://leafletjs.com/examples/quick-start/

### In a folder called `atlas`,

#### save this as `index.html`:

```html
<html>
  <head>
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <link rel="stylesheet" type="text/css" href="style.css">
    <link rel="stylesheet" href="https://unpkg.com/leaflet@1.5.1/dist/leaflet.css">
  </head>
  <body>
    <div id="app">
      <div id="navigation-panel">
        <div class="card">
          <p class="name">Culture</p>
          <p class="neighborhood">Park Slope</p>
        </div>
      </div>
      <div id="map"></div>
    </div>
    <script src="https://unpkg.com/leaflet@1.5.1/dist/leaflet.js"></script>
    <script src="index.js"></script>
  </body>
</html>
```

#### save this as `index.js`:
```js
// Initialize a map:

var myMap = L.map('map').setView([40.713681, -73.993257], 12);

L.tileLayer('http://{s}.basemaps.cartocdn.com/light_all/{z}/{x}/{y}.png', {
  attribution: '&copy; <a href="http://www.openstreetmap.org/copyright">OpenStreetMap</a> contributors',
  maxZoom: 18,
}).addTo(myMap);


// Add markers and popups to the map:

// Marker for culture
var culture = L.marker([40.672557, -73.983408]).addTo(myMap);
culture.bindPopup(
  `
  <h1>Culture</h1>
  <h3>331 5th Ave, Brooklyn, NY 11215</h3>
  `
);

// Marker for ...
```

#### save this as `style.css`:
```css
body {
  margin: 0px;
}

#app {
  display: flex;
  height: 100vh;
}

#map {
  flex: 2;
}

#navigation-panel {
  flex: 1;
/*  width: 300px;*/
}
```

## A quick intro

### Useful features of text editors
- quick access to many open files
- language specific text highlighting
- comment code with `cmd + /`
- duplicate selections with `cmd + D`

### Languages browsers speak
- **`html`**: The content of the page
- **`css`**: The style of the page
- **`js`**: (javascript) For interactivity

### Chrome Developer Tools (**`View -> Developer`**)
- shows errors
- view and edit css styles

### Resources
- W3 Schools
- Stackoverflow


## CSS selectors

**a `#` selects by ID**
```css
#map {
  flex: 2;
}
```

**a `.` selects by class**
```css
.card {
  border: 1px solid #bfbfbf;
}
```

**use just the name to select html tags (`body`, `div`, `p`, etc)**
```css
body {
  margin: 0px;
}
```
