# **[VectorDrawables](https://developer.android.com/guide/topics/graphics/vector-drawable-resources#vector-drawable-class)** 
A VectorDrawable is a vector graphic defined in an XML file as a set of points, lines, and curves along with its associated color information.  
The major advantage of using a vector drawable is image scalability.  
It can be scaled without loss of display quality, which means the same file is resized for different screen densities without loss of image quality.  
This results in smaller APK files and less developer maintenance.  
You can also use vector images for animation by using multiple XML files instead of multiple images for each display resolution.

## 1. Enable Support
You need to opt in to AndroidX vector support in your app’s build.gradle:
```gradle 
android {
    defaultConfig {
        vectorDrawables.useSupportLibrary = true
    }
}
```
This flag prevents the Android Gradle Plugin from generating PNG versions of your vector assets if your minSdkVersion is < 21—we don’t need this as we’ll use the AndroidX library instead.

## ImageView, ImageButton:
* Don’t: android:src
* Do: app:srcCompat

## CheckBox, RadioButton:
* Don’t: android:button
* Do: app:buttonCompat

## How to set VectorDrawables
<img width="657" alt="Dice_Roller_–_activity_main_xml__Dice_Roller_app_" src="https://user-images.githubusercontent.com/47273077/147915080-a0ded3a8-ac62-449e-b921-2c8aa2512a6e.png">

```xml
xmlns:app="http://schemas.android.com/apk/res-auto"
```
