# NY Taxi Fare prediction interface

![](images/snapshot.png)

## Setup

The interface uses 3 APIs:

- The NY Taxi Fare prediction API
- The [MapBox Maps API](https://docs.mapbox.com/mapbox-gl-js/api/) to display a map and address autocomplete
- The [MapBox Directions API](https://docs.mapbox.com/api/navigation/) to display the route on the map

These APIs require credentials and the following steps will guide you to get them and set the interface with.

### NY Taxi Fare prediction API

Update the `script.js` to get prediction from your own API hosted on GCP (make sure to use `https`, not `http`):

```js
// script.js

const taxiFareApiUrl = 'https://YOUR_API_URL/predict';
```


### MapBox Maps and Directions APIs (optional)

- Go to [MapBox](https://www.mapbox.com/) and create an account
- Go to your [Account](https://account.mapbox.com/) and grab your `Access Token` then set it into the `script.js`

```js
//...
mapboxgl.accessToken = 'YOUR_MAPBOX_API_ACCESS_TOKEN';
````

## Local development

To check your setup, run the interface locally with:
```bash
python -m http.server 5001
```

Then go to [http://localhost:5001](http://localhost:5001)

## Deploy on GitHub Pages

Your app is ready to go live!

Create a new branch `gh-pages`:

```bash
git checkout -b gh-pages
```

Deploy your app on GitHub:

```bash
git push origin gh-pages
```

App is visible at `https://multiyumz.github.io/taxi-fare-interface`.
