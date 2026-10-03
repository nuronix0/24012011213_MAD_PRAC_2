# Android Activity Life Cycle & Basic UI Demo

## AIM

Create an Android application to demonstrate:

* Basic Android UI using `TextView`
* Activity Life Cycle methods
* Log messages in Logcat
* Toast messages
* Snackbar messages
* Android built-in color resources
* `ConstraintLayout` properties
* Generating and using a `TextView` ID

## Application Description

This application displays **"Hello World"** in the center of the Activity screen.

The Activity layout has a **yellow background**, and the `TextView` is styled with:

* **Text:** `Hello World`
* **Text Color:** Holo Blue Bright
* **Text Size:** `27sp`
* **Text Style:** Bold and Italic
* **Background:** Yellow
* **Alignment:** Center of the Activity

The application also demonstrates the Android Activity Life Cycle using **Log**, **Toast**, and **Snackbar** messages.

## UI Requirements

The `TextView` should use the following properties:

```xml
android:text="Hello World"
android:textColor="@android:color/holo_blue_bright"
android:textSize="27sp"
android:textStyle="bold|italic"
```

The Activity layout should use:

```xml
android:background="#FFFF00"
```

The `TextView` should have a generated ID so that it can be referenced from the Activity code.

## Activity Life Cycle

The following Activity Life Cycle methods are demonstrated:

1. `onCreate()`
2. `onStart()`
3. `onResume()`
4. `onPause()`
5. `onStop()`
6. `onRestart()`
7. `onDestroy()`

Each method prints a message to **Logcat**.

Example:

```java
Log.d("ActivityLifecycle", "onCreate called");
```

## Messages Demonstrated

### Log Message

Activity Life Cycle methods are printed in Android Studio's **Logcat**.

Example:

```text
onCreate called
onStart called
onResume called
```

### Toast Message

Toast messages are used to display short notifications when Activity Life Cycle methods are executed.

Example:

```java
Toast.makeText(this, "onCreate called", Toast.LENGTH_SHORT).show();
```

### Snackbar Message

A Snackbar is displayed at the bottom of the screen to demonstrate user notifications.

Example:

```java
Snackbar.make(findViewById(R.id.textView),
        "Activity Started",
        Snackbar.LENGTH_SHORT).show();
```

## Expected Output

When the application starts:

* A yellow Activity background is displayed.
* **Hello World** appears in the center.
* The text is blue, bold, italic, and `27sp`.
* Activity Life Cycle messages appear in Logcat.
* Toast and Snackbar notifications are displayed during the appropriate Activity events.

## How to Test the Activity Life Cycle

1. Run the application.
2. Open **Logcat** in Android Studio.
3. Filter the logs using the tag:

```text
ActivityLifecycle
```

4. Observe `onCreate()`, `onStart()`, and `onResume()`.
5. Press the Home button or switch to another application.
6. Observe `onPause()` and `onStop()`.
7. Return to the application.
8. Observe `onRestart()`, `onStart()`, and `onResume()`.
9. Close the Activity/application and observe `onDestroy()` when applicable.

## Technologies Used

* Android Studio
* Java/Kotlin Android Activity
* XML Layout
* `TextView`
* `ConstraintLayout`
* `Logcat`
* `Toast`
* `Snackbar`

## Learning Outcomes

After completing this application, you should understand:

* How to create and configure a `TextView`
* How to set text color, size, and style
* How to use Android built-in resources
* How to generate and reference View IDs
* How `ConstraintLayout` positions UI elements
* How Android Activity Life Cycle methods work
* How to print debugging information using `Log`
* How to display Toast messages
* How to display Snackbar messages

## Conclusion

This project demonstrates the basic Android user interface and the complete Activity Life Cycle. It provides practical experience with `TextView`, XML layout properties, Logcat, Toast, Snackbar, and Activity Life Cycle callbacks.
