## EX:NO:05:Develop a program to create a simple calculator using android studio.

## Aim:
To create and design an android application for a simple calculator using android studio.

## EQUIPMENTS REQUIRED:
Android Studio(Latest Version)

## ALGORITHM:
Step 1: Open Android Stdio and then click on File -> New -> New project.

Step 2: Then type the Application name as smsintent and click Next.

Step 3: Then select the Minimum SDK as shown below and click Next.

Step 4: Then select the Empty Activity and click Next. Finally click Finish.

Step 5: Design layout in activity_main.xml.

Step 6:Display details give in MainActivity file.

Step 7: Save and run the application.
## PROGRAM:
```
/*
Program to create and design an android application simple calculator using Intent.
Developed by:Nalini P
Registeration Number :212223220063
*/
```
## MainActivity.java:
```
package com.example.muiex054;

import android.os.Bundle;
import android.widget.Button;
import android.widget.EditText;
import android.widget.TextView;

import androidx.appcompat.app.AppCompatActivity;

public class MainActivity extends AppCompatActivity {

    EditText num1, num2;
    Button add, sub, mul, div;
    TextView result;

    @Override
    protected void onCreate(Bundle savedInstanceState) {
        super.onCreate(savedInstanceState);
        setContentView(R.layout.activity_main);

        num1 = findViewById(R.id.num1);
        num2 = findViewById(R.id.num2);

        add = findViewById(R.id.add);
        sub = findViewById(R.id.sub);
        mul = findViewById(R.id.mul);
        div = findViewById(R.id.div);

        result = findViewById(R.id.result);

        add.setOnClickListener(v -> {

            double a = Double.parseDouble(
                    num1.getText().toString());

            double b = Double.parseDouble(
                    num2.getText().toString());

            result.setText("Result : " + (a + b));
        });

        sub.setOnClickListener(v -> {

            double a = Double.parseDouble(
                    num1.getText().toString());

            double b = Double.parseDouble(
                    num2.getText().toString());

            result.setText("Result : " + (a - b));
        });

        mul.setOnClickListener(v -> {

            double a = Double.parseDouble(
                    num1.getText().toString());

            double b = Double.parseDouble(
                    num2.getText().toString());

            result.setText("Result : " + (a * b));
        });

        div.setOnClickListener(v -> {

            double a = Double.parseDouble(
                    num1.getText().toString());

            double b = Double.parseDouble(
                    num2.getText().toString());

            result.setText("Result : " + (a / b));
        });
    }
}


```
## activity_main.xml:
```
<?xml version="1.0" encoding="utf-8"?>

<LinearLayout xmlns:android="http://schemas.android.com/apk/res/android"
    android:layout_width="match_parent"
    android:layout_height="match_parent"
    android:orientation="vertical"
    android:padding="20dp"
    android:gravity="center">

    <EditText
        android:id="@+id/num1"
        android:layout_width="match_parent"
        android:layout_height="wrap_content"
        android:hint="Enter First Number"
        android:inputType="numberDecimal"/>

    <EditText
        android:id="@+id/num2"
        android:layout_width="match_parent"
        android:layout_height="wrap_content"
        android:hint="Enter Second Number"
        android:inputType="numberDecimal"
        android:layout_marginTop="10dp"/>

    <TextView
        android:id="@+id/result"
        android:layout_width="wrap_content"
        android:layout_height="wrap_content"
        android:text="Result"
        android:textSize="22sp"
        android:textStyle="bold"
        android:layout_marginTop="20dp"/>

    <LinearLayout
        android:layout_width="wrap_content"
        android:layout_height="wrap_content"
        android:orientation="horizontal"
        android:layout_marginTop="20dp">

        <Button
            android:id="@+id/add"
            android:layout_width="wrap_content"
            android:layout_height="wrap_content"
            android:text="+"/>

        <Button
            android:id="@+id/sub"
            android:layout_width="wrap_content"
            android:layout_height="wrap_content"
            android:text="-"
            android:layout_marginLeft="10dp"/>

        <Button
            android:id="@+id/mul"
            android:layout_width="wrap_content"
            android:layout_height="wrap_content"
            android:text="*"
            android:layout_marginLeft="10dp"/>

        <Button
            android:id="@+id/div"
            android:layout_width="wrap_content"
            android:layout_height="wrap_content"
            android:text="/"
            android:layout_marginLeft="10dp"/>

    </LinearLayout>

</LinearLayout>
```

## Manifext.xml

```
<?xml version="1.0" encoding="utf-8"?>

<manifest xmlns:android="http://schemas.android.com/apk/res/android"
    package="com.example.muiex054">

    <application
        android:allowBackup="true"
        android:label="MUIEX054"
        android:supportsRtl="true"
        android:theme="@style/Theme.AppCompat.Light.DarkActionBar">

        <activity
            android:name=".MainActivity"
            android:exported="true">

            <intent-filter>

                <action android:name=
                    "android.intent.action.MAIN"/>

                <category android:name=
                    "android.intent.category.LAUNCHER"/>

            </intent-filter>

        </activity>

    </application>

</manifest>

```
## OUTPUT

<img width="1920" height="1200" alt="Screenshot (111)" src="https://github.com/user-attachments/assets/9aff91a6-0254-461e-93fa-54b0d3a7ff8a" />
<img width="1920" height="1200" alt="Screenshot (112)" src="https://github.com/user-attachments/assets/80c4f4d6-7b54-465f-b24f-808c672a90ac" />
<img width="1920" height="1200" alt="Screenshot (113)" src="https://github.com/user-attachments/assets/bd7570c8-45bf-44ef-ae7c-467ddb7673c6" />
<img width="1920" height="1200" alt="Screenshot (114)" src="https://github.com/user-attachments/assets/a59ed983-3d01-4ee6-a1e0-0639d57b326d" />



## RESULT
Thus a Simple Android Application create a simple calculator using Android Studio is developed and executed successfully.
