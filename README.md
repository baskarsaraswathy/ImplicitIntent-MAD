# Ex.No:2a Develop program to create a text field and a button “Navigate”. When you enter “www.gmail.com” and press navigate button it should open google page using Implicit Intents.


## AIM:

To create a navigate button using Implicit Intent to display the gmail page using Android Studio.

## EQUIPMENTS REQUIRED:

Latest Version Android Studio

## ALGORITHM:



## PROGRAM:

```
Program to print the text “Implicitintent”.
Developed by: BASKAR J
Registeration Number : 212223040025
MainActivity.java
```
```
package com.example.implicitintent;

import android.content.Intent;
import android.net.Uri;
import android.os.Bundle;
import android.view.View;
import android.widget.Button;
import android.widget.EditText;

import androidx.activity.EdgeToEdge;
import androidx.appcompat.app.AppCompatActivity;
import androidx.core.graphics.Insets;
import androidx.core.view.ViewCompat;
import androidx.core.view.WindowInsetsCompat;

public class MainActivity extends AppCompatActivity {

    @Override
    protected void onCreate(Bundle savedInstanceState) {
        super.onCreate(savedInstanceState);
        setContentView(R.layout.activity_main);
        EditText editText;
        Button button;

        setContentView(R.layout.activity_main);

        button = findViewById(R.id.button);
        editText = (EditText) findViewById(R.id.editTextText);

        button.setOnClickListener(new View.OnClickListener() {
            @Override
            public void onClick(View view) {
                String url=editText.getText().toString();
                Intent intent = new Intent(Intent.ACTION_VIEW, Uri.parse(url));
                startActivity(intent);
            }
        });
    }
}
```
### activity_main.xml
```
<?xml version="1.0" encoding="utf-8"?>
<androidx.constraintlayout.widget.ConstraintLayout xmlns:android="http://schemas.android.com/apk/res/android"
    xmlns:app="http://schemas.android.com/apk/res-auto"
    xmlns:tools="http://schemas.android.com/tools"
    android:id="@+id/main"
    android:layout_width="match_parent"
    android:layout_height="match_parent"
    android:background="@drawable/img"
    android:backgroundTintMode="add"
    tools:context=".MainActivity">

    <Button
        android:id="@+id/button"
        android:layout_width="154dp"
        android:layout_height="65dp"
        android:text="Navigate"
        android:textColorLink="#FFFFFF"
        app:layout_constraintBottom_toBottomOf="parent"
        app:layout_constraintEnd_toEndOf="parent"
        app:layout_constraintHorizontal_bias="0.552"
        app:layout_constraintStart_toStartOf="parent"
        app:layout_constraintTop_toTopOf="parent"
        app:layout_constraintVertical_bias="0.857" />

    <EditText
        android:id="@+id/editTextText"
        android:layout_width="318dp"
        android:layout_height="58dp"
        android:layout_marginBottom="81dp"
        android:ems="10"
        android:hint="Enter the URL!"
        android:inputType="text"
        app:layout_constraintBottom_toTopOf="@+id/button"
        app:layout_constraintEnd_toEndOf="parent"
        app:layout_constraintHorizontal_bias="0.494"
        app:layout_constraintStart_toStartOf="parent"
        app:layout_constraintTop_toTopOf="parent"
        app:layout_constraintVertical_bias="1.0" />

    <TextView
        android:id="@+id/textView"
        android:layout_width="275dp"
        android:layout_height="174dp"
        android:text="Implicit Intent Using implicit Intent, components can’t be specified. An action to be performed is declared by implicit intent. Then android operating system will filter out components that will respond to the action"
        android:textAlignment="center"
        android:textColor="#000000"
        android:textStyle="bold"
        app:layout_constraintBottom_toTopOf="@+id/editTextText"
        app:layout_constraintEnd_toEndOf="parent"
        app:layout_constraintHorizontal_bias="0.397"
        app:layout_constraintStart_toStartOf="parent"
        app:layout_constraintTop_toTopOf="parent"
        app:layout_constraintVertical_bias="0.957" />

    <ImageView
        android:id="@+id/imageView2"
        android:layout_width="391dp"
        android:layout_height="74dp"
        android:layout_marginBottom="107dp"
        app:layout_constraintBottom_toTopOf="@+id/textView"
        app:layout_constraintEnd_toEndOf="parent"
        app:layout_constraintHorizontal_bias="0.2"
        app:layout_constraintStart_toStartOf="parent"
        app:layout_constraintTop_toTopOf="parent"
        app:layout_constraintVertical_bias="1.0"
        app:srcCompat="@drawable/img_1" />

</androidx.constraintlayout.widget.ConstraintLayout>
```

## OUTPUT

### activity_main.xml
<img width="1920" height="1020" alt="image" src="https://github.com/user-attachments/assets/ee5fbbf1-6b0a-491c-8325-1a86d3b45c3a" />

### MainActivity.java
<img width="1920" height="1020" alt="image" src="https://github.com/user-attachments/assets/bd2139bf-b3c4-4bc3-b040-5e7d36f87f6c" />

### Implicit Intent
<img width="470" height="836" alt="Screenshot 2025-09-10 094824" src="https://github.com/user-attachments/assets/c75c2154-e51c-4c47-a619-4f6f77fcdad7" />

### Navigated to URL
<img width="465" height="842" alt="Screenshot 2025-09-10 094847" src="https://github.com/user-attachments/assets/d3c177aa-4692-4e37-9afd-06f7333bb58b" />






## RESULT
Thus a Simple Android Application create a navigate button using Implicit Intent to display the gmail page using Android Studio is developed and executed successfully.


