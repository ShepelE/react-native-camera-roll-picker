
[![version](https://img.shields.io/npm/v/react-native-camera-roll-picker.svg)](https://www.npmjs.org/package/react-native-camera-roll-picker) [![npm](https://img.shields.io/npm/dt/react-native-camera-roll-picker.svg)](https://www.npmjs.org/package/react-native-camera-roll-picker)

# react-native-camera-roll-picker
CameraRoll Picker component for React native

<a href="https://raw.githubusercontent.com/jeanpan/react-native-camera-roll-picker/master/demo/demo.gif"><img src="https://raw.githubusercontent.com/jeanpan/react-native-camera-roll-picker/master/demo/demo.gif" width="350"></a>

Requires `react-native >=0.60.0`

the single reason to make this fork was not to repeat photos in the list when groupTypes={'All'}

## Add to Project
* Make sure node_modules/react-native/Libraries/CameraRoll/RCTCameraRoll.xcodeproj has been imported to project libraries by following the [libraries linking instructions](https://facebook.github.io/react-native/docs/linking-libraries-ios.html). Don't forget to link the `libRCTCamera.a` into `Link Binary with Binaries` on your target's Build Phases.
* Install component through npm
```
$ npm install react-native-cameraroll --save
$ npm install react-native-camera-roll-picker --save
```

* Require component
```
import CameraRollPicker from 'react-native-camera-roll-picker';
```

## Basic Usage
```js
<CameraRollPicker
  callback={this.getSelectedImages} />
```

## Props
- `callback` : Callback function when images was selected. (is required!). Return a selected image array and current selected image.
- `initialNumToRender` : Specifies how many rows we want to render on our first render pass. (Default: 5)
- `groupTypes` : The group where the photos will be fetched, one of 'Album', 'All', 'Event', 'Faces', 'Library', 'PhotoStream' and 'SavedPhotos'. (Default: SavedPhotos)
- `assetType` : The asset type, one of 'Photos', 'Videos' or 'All'. (Default: Photos)
- `selected` : Already be selected images array. (Default: [])
- `selectSingleItem` : Boolean to select only one single image at time. (Default: `false`)
- `maximum` : Maximum number of selected images. (Default: 15)
- `imagesPerRow` : Number of images per row. (Default: 3)
- `imageMargin` : Margin size of one image. (Default: 5)
- `containerWidth` : Width of camer roll picker container. (Default: device width)
- `selectedMarker` : Custom selected image marker component. (Default: checkmark).
- `backgroundColor` : Set background color. (Default: white).
- `emptyText`: Text to display instead of a list when there are no photos found. (Default: 'No photos.')
- `emptyTextStyle`: Styles to apply to the `emptyText`. (Default: `textAlign: 'center'`)
- `loader`: Loader component node. (Default: `<ActivityIndicator />`)

## Run Example
```
$ git clone https://github.com/jeanpan/react-native-camera-roll-picker.git
$ cd react-native-camera-roll-picker
$ cd Example
$ npm install
$ react-native run-ios
```
