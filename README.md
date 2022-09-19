# Practical_4
Aim: What is Intent? Write down types of Intent and types of Intent Action. Create an application which demonstrates implicit Intent for following features and also create different activities and demonstrate explicit Intent. Use parent theme Theme.Material3.Dark.NoActionBar for Dark theme and Theme.Material3.Light.NoActionBar for Light Theme
*CODE*:
Activity_main.xml File:

<?xml version="1.0" encoding="utf-8"?>
<androidx.constraintlayout.widget.ConstraintLayout xmlns:android="http://schemas.android.com/apk/res/android"
    xmlns:app="http://schemas.android.com/apk/res-auto"
    xmlns:tools="http://schemas.android.com/tools"
    android:layout_width="match_parent"
    android:layout_height="match_parent"
    tools:context=".MainActivity">


    <com.google.android.material.textfield.TextInputLayout
        android:id="@+id/text_browse"
        android:layout_width="230sp"
        android:layout_height="wrap_content"
        style="@style/Widget.MaterialComponents.TextInputLayout.OutlinedBox"
        app:boxStrokeColor="@color/black"
        android:layout_marginTop="50sp"
        app:layout_constraintEnd_toStartOf="@+id/button_browse"
        app:layout_constraintStart_toEndOf="@id/button_browse"
        app:layout_constraintStart_toStartOf="parent"
        app:layout_constraintTop_toTopOf="parent">
        <com.google.android.material.textfield.TextInputEditText
            android:id="@+id/input_browse"
            android:layout_width="match_parent"
            android:layout_height="wrap_content"
            android:inputType="textUri"
            android:drawableStart="@drawable/ic_baseline_web_24"
            android:hint="   Web URL"
            >
        </com.google.android.material.textfield.TextInputEditText>
    </com.google.android.material.textfield.TextInputLayout>

    <com.google.android.material.textfield.TextInputLayout
        android:id="@+id/text_call"
        android:layout_width="230sp"
        android:layout_height="wrap_content"
        android:layout_marginTop="10sp"
        style="@style/Widget.MaterialComponents.TextInputLayout.OutlinedBox"
        app:boxStrokeColor="@color/black"
        app:layout_constraintEnd_toStartOf="@+id/button_call"
        app:layout_constraintStart_toEndOf="@+id/button_call"
        app:layout_constraintStart_toStartOf="parent"
        app:layout_constraintTop_toBottomOf="@+id/text_browse">

        <com.google.android.material.textfield.TextInputEditText
            android:id="@+id/input_call"
            android:layout_width="match_parent"
            android:layout_height="wrap_content"
            android:drawableStart="@drawable/ic_baseline_call_24"
            android:hint="   Call Number"
            android:inputType="number"
            >
        </com.google.android.material.textfield.TextInputEditText>
    </com.google.android.material.textfield.TextInputLayout>

    <com.google.android.material.textfield.TextInputLayout
        android:id="@+id/text_contact"
        android:layout_width="230sp"
        android:layout_height="wrap_content"
        android:layout_marginTop="10sp"
        style="@style/Widget.MaterialComponents.TextInputLayout.OutlinedBox"
        app:boxStrokeColor="@color/black"
        app:layout_constraintEnd_toStartOf="@+id/button_contact"
        app:layout_constraintStart_toEndOf="@id/button_contact"
        app:layout_constraintStart_toStartOf="parent"
        app:layout_constraintTop_toBottomOf="@+id/text_call">
        <com.google.android.material.textfield.TextInputEditText
            android:layout_width="match_parent"
            android:layout_height="wrap_content"
            android:drawableStart="@drawable/ic_baseline_contact_phone_24"
            android:hint="   Contact List"
            >
        </com.google.android.material.textfield.TextInputEditText>
    </com.google.android.material.textfield.TextInputLayout>

    <com.google.android.material.textfield.TextInputLayout
        android:id="@+id/text_calllog"
        android:layout_width="230sp"
        android:layout_height="wrap_content"
        android:layout_marginTop="10sp"
        style="@style/Widget.MaterialComponents.TextInputLayout.OutlinedBox"
        app:boxStrokeColor="@color/black"
        app:layout_constraintEnd_toStartOf="@+id/button_calllog"
        app:layout_constraintStart_toEndOf="@id/button_calllog"
        app:layout_constraintStart_toStartOf="parent"
        app:layout_constraintTop_toBottomOf="@+id/text_contact">
        <com.google.android.material.textfield.TextInputEditText
            android:layout_width="match_parent"
            android:layout_height="wrap_content"
            android:drawableStart="@drawable/ic_baseline_web_24"
            android:hint="   Call Log"
            >
        </com.google.android.material.textfield.TextInputEditText>
    </com.google.android.material.textfield.TextInputLayout>

    <com.google.android.material.textfield.TextInputLayout
        android:id="@+id/text_gallery"
        android:layout_width="230sp"
        android:layout_height="wrap_content"
        android:layout_marginTop="10sp"
        style="@style/Widget.MaterialComponents.TextInputLayout.OutlinedBox"
        app:boxStrokeColor="@color/black"
        app:layout_constraintEnd_toStartOf="@+id/button_gallery"
        app:layout_constraintStart_toEndOf="@id/button_gallery"
        app:layout_constraintStart_toStartOf="parent"
        app:layout_constraintTop_toBottomOf="@+id/text_calllog">
        <com.google.android.material.textfield.TextInputEditText
            android:layout_width="match_parent"
            android:layout_height="wrap_content"
            android:drawableStart="@drawable/ic_baseline_image_24"
            android:hint="   Gallery"
            >
        </com.google.android.material.textfield.TextInputEditText>
    </com.google.android.material.textfield.TextInputLayout>

    <com.google.android.material.textfield.TextInputLayout
        android:id="@+id/text_camera"
        android:layout_width="230sp"
        android:layout_height="wrap_content"
        android:layout_marginTop="10sp"
        style="@style/Widget.MaterialComponents.TextInputLayout.OutlinedBox"
        app:boxStrokeColor="@color/black"
        app:layout_constraintEnd_toStartOf="@+id/button_camera"
        app:layout_constraintStart_toEndOf="@id/button_camera"
        app:layout_constraintStart_toStartOf="parent"
        app:layout_constraintTop_toBottomOf="@+id/text_gallery">
        <com.google.android.material.textfield.TextInputEditText
            android:layout_width="match_parent"
            android:layout_height="wrap_content"
            android:drawableStart="@drawable/ic_baseline_camera_alt_24"
            android:hint="   Camera"
            >
        </com.google.android.material.textfield.TextInputEditText>
    </com.google.android.material.textfield.TextInputLayout>

    <com.google.android.material.textfield.TextInputLayout
        android:id="@+id/text_alarm"
        android:layout_width="230sp"
        android:layout_height="wrap_content"
        android:layout_marginTop="10sp"
        style="@style/Widget.MaterialComponents.TextInputLayout.OutlinedBox"
        app:boxStrokeColor="@color/black"
        app:layout_constraintEnd_toStartOf="@+id/button_alarm"
        app:layout_constraintStart_toEndOf="@id/button_alarm"
        app:layout_constraintStart_toStartOf="parent"
        app:layout_constraintTop_toBottomOf="@+id/text_camera">
        <com.google.android.material.textfield.TextInputEditText
            android:layout_width="match_parent"
            android:layout_height="wrap_content"
            android:drawableStart="@drawable/ic_baseline_alarm_24"
            android:hint="   Alarm"
            >
        </com.google.android.material.textfield.TextInputEditText>
    </com.google.android.material.textfield.TextInputLayout>

    <Button
        android:id="@+id/button_browse"
        android:layout_width="wrap_content"
        android:layout_height="55sp"
        android:layout_marginTop="56dp"
        android:layout_marginEnd="10dp"
        android:width="110sp"
        android:text="Browse"
        app:cornerRadius="20sp"
        app:layout_constraintEnd_toEndOf="parent"
        app:layout_constraintTop_toTopOf="parent" />

    <Button
        android:id="@+id/button_call"
        android:layout_width="wrap_content"
        android:layout_height="55sp"
        android:layout_marginTop="20dp"
        android:layout_marginEnd="10dp"
        android:width="110sp"
        android:text="Call"
        app:cornerRadius="20sp"
        app:layout_constraintEnd_toEndOf="parent"
        app:layout_constraintTop_toBottomOf="@id/button_browse" />

    <Button
        android:id="@+id/button_contact"
        android:layout_width="wrap_content"
        android:layout_height="55sp"
        android:layout_marginTop="20dp"
        android:layout_marginEnd="10dp"
        android:width="110sp"
        android:text="Contact"
        app:cornerRadius="20sp"
        app:layout_constraintEnd_toEndOf="parent"
        app:layout_constraintTop_toBottomOf="@id/button_call" />

    <Button
        android:id="@+id/button_calllog"
        android:layout_width="wrap_content"
        android:layout_height="55sp"
        android:layout_marginTop="16dp"
        android:layout_marginEnd="10dp"
        android:width="110sp"
        android:text="Call log"
        app:cornerRadius="20sp"
        app:layout_constraintEnd_toEndOf="parent"
        app:layout_constraintTop_toBottomOf="@id/button_contact" />

    <Button
        android:id="@+id/button_gallery"
        android:layout_width="wrap_content"
        android:layout_height="55sp"
        android:layout_marginTop="20dp"
        android:layout_marginEnd="10dp"
        android:width="110sp"
        android:text="Gallery"
        app:cornerRadius="20sp"
        app:layout_constraintEnd_toEndOf="parent"
        app:layout_constraintTop_toBottomOf="@id/button_calllog" />

    <Button
        android:id="@+id/button_camera"
        android:layout_width="wrap_content"
        android:layout_height="55sp"
        android:layout_marginTop="20dp"
        android:layout_marginEnd="10dp"
        android:width="110sp"
        android:text="Camera"
        app:cornerRadius="20sp"
        app:layout_constraintEnd_toEndOf="parent"
        app:layout_constraintTop_toBottomOf="@id/button_gallery" />

    <Button
        android:id="@+id/button_alarm"
        android:layout_width="wrap_content"
        android:layout_height="55sp"
        android:layout_marginTop="16dp"
        android:layout_marginEnd="10dp"
        android:width="110sp"
        android:text="Alarm"
        app:cornerRadius="20sp"
        app:layout_constraintEnd_toEndOf="parent"
        app:layout_constraintTop_toBottomOf="@id/button_camera" />

</androidx.constraintlayout.widget.ConstraintLayout>

MainActivity.kt File:

package ru.kotlin.a20012011183_yatharthpatel_practical_4

import android.content.Intent
import android.net.Uri
import androidx.appcompat.app.AppCompatActivity
import android.os.Bundle
import android.provider.AlarmClock
import android.provider.CallLog
import android.provider.ContactsContract
import android.provider.MediaStore
import android.text.BoringLayout.make
import android.widget.Button
import android.widget.EditText
import android.widget.Toast
import ru.kotlin.a20012011183_yatharthpatel_practical_4.R
import com.google.android.material.textfield.TextInputEditText
import org.w3c.dom.Text


class MainActivity : AppCompatActivity() {
    override fun onCreate(savedInstanceState: Bundle?) {
        super.onCreate(savedInstanceState)
        setContentView(R.layout.activity_main)

        var buttonBrowse=findViewById<Button>(R.id.button_browse)
        buttonBrowse.setOnClickListener{
            val url = findViewById<TextInputEditText>(R.id.input_browse).text
            var url_text = url.toString()
            Intent(Intent.ACTION_VIEW).setData(Uri.parse(url_text)).apply { startActivity(this) }
        }

        var buttonCall = findViewById<Button>(R.id.button_call)
        buttonCall.setOnClickListener{
            var number = findViewById<TextInputEditText>(R.id.input_call).text
            var number_text = "tel: $number"
            Intent(Intent.ACTION_DIAL).setData(Uri.parse(number_text)).apply { startActivity(this) }
        }

        var buttonContact = findViewById<Button>(R.id.button_contact)
        buttonContact.setOnClickListener{
            Intent(Intent.ACTION_VIEW).setType(ContactsContract.Contacts.CONTENT_TYPE).apply { startActivity(this) }
        }

        var buttonCallLog = findViewById<Button>(R.id.button_calllog)
        buttonCallLog.setOnClickListener{
            Intent(Intent.ACTION_VIEW).setType(CallLog.Calls.CONTENT_TYPE).apply { startActivity(this) }
        }

        var buttonGallery = findViewById<Button>(R.id.button_gallery)
        buttonGallery.setOnClickListener{
            Intent(Intent.ACTION_VIEW).setType("image/*").apply { startActivity(this) }
        }
        var buttonCamera = findViewById<Button>(R.id.button_camera)
        buttonCamera.setOnClickListener{
            Intent(MediaStore.ACTION_IMAGE_CAPTURE).apply { startActivity(this) }
        }
        var buttonAlarm = findViewById<Button>(R.id.button_alarm)
        buttonAlarm.setOnClickListener{
            Intent(AlarmClock.ACTION_SHOW_ALARMS).apply { startActivity(this) }}}}
Output:
![image](https://user-images.githubusercontent.com/93566991/190939958-6ffc4f75-83f2-480d-b2fe-4e352acf1c3a.png)
![image](https://user-images.githubusercontent.com/93566991/190939974-680dba4c-3861-4050-9b57-1365a2e3b2c0.png)
![image](https://user-images.githubusercontent.com/93566991/190939984-d935dc20-2bde-4425-ba35-f9cb75461b8d.png)
![image](https://user-images.githubusercontent.com/93566991/190939994-9dbf6886-75f4-4705-89d1-53e3ec5c094f.png)
