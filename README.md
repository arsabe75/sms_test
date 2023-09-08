# sms_test

A new Flutter project.

## Getting Started

Funciona con telephony 0.2.0

Hay que agregar lo siguiente a AndroidManifest.xml (SEND_SMS & READ_SMS)

<manifest xmlns:android="http://schemas.android.com/apk/res/android">

    <uses-permission android:name="android.permission.SEND_SMS"/>
    <uses-permission android:name="android.permission.READ_SMS"/>

    <application
        android:label="sms_test"
...

Hay que poner el mínimo SDK a 23 (minSdkVersion 23) en build.gradle

defaultConfig {
        // TODO: Specify your own unique Application ID (https://developer.android.com/studio/build/application-id.html).
        applicationId "com.example.sms_test"
        // You can update the following values to match your application needs.
        // For more information, see: https://docs.flutter.dev/deployment/android#reviewing-the-gradle-build-configuration.
        //minSdkVersion flutter.minSdkVersion
        minSdkVersion 23
        targetSdkVersion flutter.targetSdkVersion
        versionCode flutterVersionCode.toInteger()
        versionName flutterVersionName
    }

Sólo me funcionó en android 12, tengo otro teléfono con android 6, que es el que uso
para pruebas y ahí no funcionó. Así que debería funcionar en las últimas versiones de android.