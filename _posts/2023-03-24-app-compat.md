---
title: "AppCompat"
header:
  teaser: "assets/images/aludmila-gdev/agdev-appcompat.png"
categories:
- Android
tags:
  - mobile development
  - android
  - kotlin
  - Android from A to Z
toc: true
---
## What is AppCompat?

[Appcompat](https://developer.android.com/jetpack/androidx/releases/appcompat) is a support library for Android application developers that allows applications to run on different versions of the Android operating system with a consistent look and feel. This library provides features that allow developers to build apps that are backwards compatible with previous versions of Android, including actions such as changing the appearance of buttons, the toolbar, and other parts of the user interface.

The AppCompat library also provides support for more advanced features like theme compatibility, support for floating menus, the night mode feature, and much more. In summary, AppCompat is an essential tool for Android application developers as it helps ensure that their applications have a consistent look and feel across different versions of the Android operating system.
___

## Key facts about AppCompat

### Developed by the Google team
AppCompat is an official Google support library for Android app developers. This means that it is developed and maintained by the Google team, which ensures that developers have access to a high-quality and reliable tool.

### Retroactive feature support
One of the main features of AppCompat is its backward feature support. This means that developers can use the latest Android features on devices running older versions of the operating system.

### Theme Compatibility
AppCompat supports custom themes, allowing developers to customize the appearance of their apps. This is particularly useful for apps that need to fit a brand's visual identity.

### Night Mode Feature
AppCompat supports Night Mode feature which allows users to change the app appearance to a dark theme. This can help improve app readability in low-light environments.

### Floating menu support
AppCompat also supports floating menus, which are a convenient way to display menu options in mobile apps. This can help improve the user experience by making it easier for users to find and navigate the app's options.

### Widely Used
AppCompat is widely used by Android app developers all over the world. This means that there is a large community of developers who can provide support and resources for other developers who are using the library.

___
## Example

Suppose you want to add a custom toolbar to your Android app:

First, you need to add the AppCompat library to your project's dependencies in the app module's build.gradle file:

```groovy
dependencies {
    implementation 'com.android.support:appcompat-v7:28.0.0'
}
```
Next, create a Kotlin activity that uses the AppCompat library:

```kotlin
import android.os.Bundle
import androidx.appcompat.app.AppCompatActivity
import androidx.appcompat.widget.Toolbar

class MainActivity : AppCompatActivity() {

    override fun onCreate(savedInstanceState: Bundle?) {
        super.onCreate(savedInstanceState)
        setContentView(R.layout.activity_main)

        val myToolbar = findViewById<Toolbar>(R.id.my_toolbar)
        setSupportActionBar(myToolbar)
        supportActionBar?.setDisplayHomeAsUpEnabled(true)
    }
}
```
In this example, we are configuring the custom toolbar in the activity's `onCreate` method. First, we're getting the custom toolbar via the `findViewById` method, which returns an instance of `Toolbar`. 
Next, we're setting it up as the application's toolbar using the `setSupportActionBar` method. Finally, we are enabling the "Back" navigation button using the safe call operator (`?.`) and the `setDisplayHomeAsUpEnabled` method.
___
## Useful links

- [Official Android documentation on the AppCompat support library](https://developer.android.com/topic/libraries/support-library/packages#v7-appcompat)
- [AppCompat toolbar code example in Kotlin](https://developer.android.com/training/appbar/setting-up)
- [Sample code on how to use AppCompat with a RecyclerView in Kotlin](https://www.raywenderlich.com/1560485-android-recyclerview-tutorial-with-kotlin)
- [AppCompat library migration guide for AndroidX (the new Android support library)](https://developer.android.com/jetpack/androidx/migrate/artifact-mappings)