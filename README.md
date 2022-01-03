# **[VectorDrawables](https://medium.com/androiddevelopers/using-vector-assets-in-android-apps-4318fd662eb9)** 

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
