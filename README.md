# Ex.No:1 To create an Android application for Addition of Two Numbers

## AIM:

To create an Android application for addition of two numbers using Android Studio and display the summation value in the text box.

## EQUIPMENTS REQUIRED:

Latest Version Android Studio

## ALGORITHM:

Step 1: Open Android Studio and click on File -> New -> New Project.

Step 2: Then type the Application name as AdditionApp and click Next.

Step 3: Select the Minimum SDK and click Next.

Step 4: Select Empty Activity and click Next. Finally click Finish.

Step 5: Design the layout in `activity_main.xml`.

Step 6: Create two EditText fields to get two numbers from the user.

Step 7: Create an ADD button to perform the addition operation.

Step 8: Create a TextView to display the summation value.

Step 9: Write the addition logic in the `MainActivity.java` file.

Step 10: Save and run the application.

## PROGRAM:

```text
/*
Program to add two numbers and display the result.
Developed by: NITHILA S
Registration Number: 212224040224
*/
```

## Main Activity.Java
```
package com.example.additionapp;

import android.os.Bundle;
import android.widget.Button;
import android.widget.EditText;
import android.widget.TextView;

import androidx.appcompat.app.AppCompatActivity;

public class MainActivity extends AppCompatActivity {

    EditText num1, num2;
    Button addBtn;
    TextView result;

    @Override
    protected void onCreate(Bundle savedInstanceState) {
        super.onCreate(savedInstanceState);
        setContentView(R.layout.activity_main);

        num1 = findViewById(R.id.num1);
        num2 = findViewById(R.id.num2);
        addBtn = findViewById(R.id.addBtn);
        result = findViewById(R.id.result);

        addBtn.setOnClickListener(v -> {

            double a = Double.parseDouble(
                    num1.getText().toString());

            double b = Double.parseDouble(
                    num2.getText().toString());

            double sum = a + b;

            result.setText("Result = " + sum);
        });
    }
}
```

## activity_main.xml
```
<?xml version="1.0" encoding="utf-8"?>

<LinearLayout
    xmlns:android="http://schemas.android.com/apk/res/android"
    android:layout_width="match_parent"
    android:layout_height="match_parent"
    android:orientation="vertical"
    android:padding="20dp">

    <EditText
        android:id="@+id/num1"
        android:layout_width="match_parent"
        android:layout_height="wrap_content"
        android:hint="Enter first number"
        android:inputType="number" />

    <EditText
        android:id="@+id/num2"
        android:layout_width="match_parent"
        android:layout_height="wrap_content"
        android:hint="Enter second number"
        android:inputType="number" />

    <Button
        android:id="@+id/addBtn"
        android:layout_width="match_parent"
        android:layout_height="wrap_content"
        android:text="ADD" />

    <TextView
        android:id="@+id/result"
        android:layout_width="match_parent"
        android:layout_height="wrap_content"
        android:text="Result"
        android:textSize="20sp" />

</LinearLayout>
```

## OUTPUT:

<img width="1801" height="1198" alt="Screenshot 2026-09-20 194627" src="https://github.com/user-attachments/assets/3bf8517d-e1de-46dc-b459-034fec4d5b51" />

<img width="1917" height="1198" alt="Screenshot 2026-09-20 194702" src="https://github.com/user-attachments/assets/7c37fba4-d1d8-4aad-8798-d27dec899aa9" />

<img width="1917" height="1198" alt="Screenshot 2026-09-20 194740" src="https://github.com/user-attachments/assets/b463c20e-2f5f-4353-bba4-c907ad6f0da2" />


## Result:
Thus, an Android application for Addition of Two Numbers was developed and executed successfully using Android Studio. The two numbers were obtained from the user and their summation value was displayed in the text box.
