Exp.No : 04 
&emsp;
&emsp;
&emsp;
&emsp;
&emsp;
&emsp;
&emsp;
&emsp;
&emsp;
&emsp;
&emsp;
&emsp;
&emsp;
&emsp;
&emsp;
&emsp;
&emsp;
&emsp;
&emsp;
&emsp;
&emsp;
&emsp;
Date : 02.05.2023 
<br>
# Sensor 
## AIM:
To develop a sensor application to use the sensor manager class to identify and get the list of available sensors on a device. in Android Studio.
## EQUIPMENTS REQUIRED:
Android Studio(Min.required Artic Fox)
## ALGORITHM:
- **Step 1:** Open Android Stdio and then click on File -> New -> New project.
- **Step 2:** Then type the Application name as Sensor and click Next. 
- **Step 3:** Then select the Minimum SDK as shown below and click Next.
- **Step 4:** Then select the Empty Activity and click Next. Finally click Finish.
- **Step 5:** Design layout in activity_main.xml.
- **Step 6:** Display avaliable sensor in android mobile devices.
- **Step 7:** Save and run the application.

## PROGRAM:
> Program to print the avaliable sensor in android mobile devices<br> Developed by: Kaushika A<br>Registeration Number : 212221230048

### activity_mail.xml
```xml
<?xml version="1.0" encoding="utf-8"?>
<LinearLayout xmlns:android="http://schemas.android.com/apk/res/android"
    xmlns:app="http://schemas.android.com/apk/res-auto"
    xmlns:tools="http://schemas.android.com/tools"
    android:layout_width="match_parent"
    android:layout_height="match_parent"
    tools:context=".MainActivity">

    <TextView
        android:id="@+id/textView"
        android:layout_width="wrap_content"
        android:layout_height="wrap_content"
        android:layout_gravity="center"
        android:gravity="center"
        android:text="Sensors"
        android:textSize="20dp"
        android:textStyle="bold" />
</LinearLayout>
```
### MainActivity.java
```java
package com.kass.sensors;

import androidx.appcompat.app.AppCompatActivity;

import android.content.Context;
import android.hardware.Sensor;
import android.hardware.SensorManager;
import android.os.Bundle;
import android.view.View;
import android.widget.TextView;

import java.util.List;

public class MainActivity extends AppCompatActivity {
    private SensorManager sm;
    private TextView text;
    @Override
    protected void onCreate(Bundle savedInstanceState) {
        super.onCreate(savedInstanceState);
        setContentView(R.layout.activity_main);

        text=(TextView) findViewById(R.id.textView);
        sm = (SensorManager)getSystemService(Context.SENSOR_SERVICE);
        List<Sensor> sensorlist = sm.getSensorList(Sensor.TYPE_ALL);
        StringBuilder sb = new StringBuilder();
        for(Sensor s:sensorlist)
        {
            sb.append(s.getName()+"\n");
        }
        text.setVisibility(View.VISIBLE);
        text.setText(sb);
    }
}
```
## OUTPUT
<img src="https://github.com/Kaushika-Anandh/Advance-Android-Odd-/blob/main/Sensor/1.PNG" width="600" height="290">

## RESULT
Thus a Simple Android Application to display the avaliable sensor in android mobile devices using Sensor Manager in Android Studio is developed and executed successfully.
