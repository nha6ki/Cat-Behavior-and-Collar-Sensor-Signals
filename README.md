# Cat Behavior & Collar Sensor Signals

This bilingual browser demo replays annotated cat behavior alongside movement signals from collar accelerometers. It includes 11,578 one-second observations from 12 cats.

## Run locally

Open `docs/index.html` in a browser, or run the following from the repository root and visit <http://localhost:8000>.

```sh
python3 -m http.server 8000 --directory docs
```

Each cat loops through its own recording segment. The 15-second traces use the same logarithmic vertical scale. Select a cat to inspect the original sensor values, UTC time and behavior annotation. The animations illustrate observed behaviors; on-screen paths and coat colors are illustrative.

## Data and attribution

Michelle Smit (2023), [R dataframes of annotated behaviour data and accelerometer data, version 2](https://doi.org/10.6084/m9.figshare.23605842.v2), distributed under [CC BY 4.0](https://creativecommons.org/licenses/by/4.0/).

The embedded subset in `docs/records.js` matches collar measurements to annotations by cat and timestamp. It includes one continuous segment per cat, with the original behavior label and the VM_Mean and ODBA15_Mean values. The display transform is applied only when drawing ODBA15_Mean.

## GitHub Pages

The demo is a static site. To publish it from this repository, select **Settings → Pages → Deploy from a branch**, then select **main** and **/docs**.
