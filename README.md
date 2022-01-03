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
