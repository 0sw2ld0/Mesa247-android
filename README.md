Reserva
========

Libreria para poder reservar y ver historial de las reservas soportado Mesa247.

Download
--------

Gradle:
```groovy
repositories {
    maven {
        url 'https://dl.bintray.com/oslh/maven'
    }
}
dependencies {
    compile 'com.mesa247.reserva:reserva:1.0.0@aar'
    compile 'com.pnikosis:materialish-progress:1.7'
    compile 'com.jpardogo.materialtabstrip:library:1.1.0'
}
```
Agregar en el AndroidManifest.xml
```groovy
        <activity android:name="com.mesa247.reserva.ui.activity.ReservaActivity"
            android:theme="@style/AppThemeMaterial"
            android:screenOrientation="portrait"/>
        <activity android:name="com.mesa247.reserva.ui.activity.MisReservaActivity"
            android:theme="@style/AppThemeMaterial"
            android:screenOrientation="portrait"/>
```

Para poder utilizar la ventana de reserva utilizar de la siguiente manera:

```groovy
        Intent intent = new Intent(this, ReservaActivity.class);
        intent.putExtra("dni", "46164069");
        intent.putExtra("userName", "Oswaldo Santiago León Huaranga");
        intent.putExtra("production", false);
        startActivity(intent);
```
Para poder utilizar la ventana de mis reservas utilizar de la siguiente manera:

```groovy

        Intent intent = new Intent(this, MisReservaActivity.class);
        intent.putExtra("dni", "46164069");
        intent.putExtra("production", false);
        startActivity(intent);

```

Reserva requires at minimum Java 8 or Android 4.1.



License
=======

    Copyright 2015 Mesa247.

    Licensed under the Apache License, Version 2.0 (the "License");
    you may not use this file except in compliance with the License.
    You may obtain a copy of the License at

       http://www.apache.org/licenses/LICENSE-2.0

    Unless required by applicable law or agreed to in writing, software
    distributed under the License is distributed on an "AS IS" BASIS,
    WITHOUT WARRANTIES OR CONDITIONS OF ANY KIND, either express or implied.
    See the License for the specific language governing permissions and
    limitations under the License.
