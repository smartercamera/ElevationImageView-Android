[![Android Arsenal]( https://img.shields.io/badge/Android%20Arsenal-ElevationImageView-green.svg?style=flat )]( https://android-arsenal.com/details/1/6843 )

# ElevationImageView
Imageview with elevation shadow

![alt text](https://raw.githubusercontent.com/qhutch/ElevationImageView/master/sample_gif.gif)


## How to use ?


### Install
Add this to your app build.gradle
```
dependencies {
    ...
    implementation 'com.qhutch.elevationimageview:elevationimageview:2.4'
}
```
You will also need support renderscript, also in your build.gradle :
```
android {
    ...
    defaultConfig {
        ...

        renderscriptTargetApi 18
        renderscriptSupportModeEnabled true
    }
}
```



### Usage

Use as any ImageView, set your image and add elevation (either with elevation attribute, or compatEvelation if your minSdk is below 21)

The clipShadow attribute is set to false by default, if true, it will clip the shadow to the View boundaries.

To set the elevation programmatically, you can use setElevation() and pass a value in pixels or setElevationDp() and pass a value in dp.

Use translucent attribute or setTranslucent() method to make the shadow keep the color of the image

## Changelog

- **V2.4** : fixed clipped shadows and migrate to androidX

- **V2.3** : fixed npe when drawable was null

- **V2.1** : support for android P (thanks to @jlurena)

- **V2.0** : Boolean attribute 'forceClip' to use another clipping method if set as true

- **V1.7** : Fixed NPE when no drawable was set

- **V1.6** : Use color matrix instead of custom script

- **V1.5** : Added translucent attribute

- **V1.4** : Opened ElevationImageView class

- **V1.3** : Fixed crash in edit mode by disabling renderscript

- **V1.2** : Extend AppCompatImageView to allow usage of `app:srcCompat` attribute

- **V1.1** : Fixed NPE when view was detached from window and the reattached


## Contact

Pull requests are more than welcome.

- **Email**: quentin.menini.us@gmail.com
- **Medium**: https://medium.com/@qhutch


# License
```
Licensed under the Apache License, Version 2.0 (the "License");
you may not use this file except in compliance with the License.
You may obtain a copy of the License at

   http://www.apache.org/licenses/LICENSE-2.0

Unless required by applicable law or agreed to in writing, software
distributed under the License is distributed on an "AS IS" BASIS,
WITHOUT WARRANTIES OR CONDITIONS OF ANY KIND, either express or implied.
See the License for the specific language governing permissions and
limitations under the License.
```
