# รายงานผลการทดลอง

<นาย พรหมพัฒน์ ชาญโชคประเสริฐ> <603410052-3>

## Relative Layout

แสดง Control `title` และ `Detail`

<?xml version="1.0" encoding="utf-8"?>

    <androidx.constraintlayout.widget.ConstraintLayout xmlns:android="http://schemas.android.com/apk/res/android"
    xmlns:app="http://schemas.android.com/apk/res-auto"
    xmlns:tools="http://schemas.android.com/tools"
    android:layout_width="match_parent"
    android:layout_height="match_parent"
    tools:context=".RelativeActivity">

        <RelativeLayout
            android:layout_width="match_parent"
            android:layout_height="match_parent"
            android:orientation="horizontal">

            <Button
                android:id="@+id/button4"
                android:layout_width="wrap_content"
                android:layout_height="wrap_content"
                android:text="Button" />

            <EditText
                android:id="@+id/editText6"
                android:layout_width="wrap_content"
                android:layout_height="wrap_content"
                android:ems="10"
                android:inputType="textPersonName"
                android:text="Name" />

            <EditText
                android:id="@+id/editText5"
                android:layout_width="wrap_content"
                android:layout_height="wrap_content"
                android:ems="10"
                android:inputType="textPersonName"
                android:layout_above="@id/editText6"
                android:text="Name" />
        </RelativeLayout>

</androidx.constraintlayout.widget.ConstraintLayout>


แอดทริบิ้วที่แสดงความสัมพันธ์ระหว่าง control ทั้งสอง
android:layout_above="@id/editText6" controlให้อยู่ข้างบน editText6
android:layout_below="@id/editText5" controlให้อยู่ข้างล่าง editText5

## Linear Layout

แสดง Control `to`, `subject`, `tag` และ `message`

<?xml version="1.0" encoding="utf-8"?>
<androidx.constraintlayout.widget.ConstraintLayout xmlns:android="http://schemas.android.com/apk/res/android"
    xmlns:app="http://schemas.android.com/apk/res-auto"
    xmlns:tools="http://schemas.android.com/tools"
    android:layout_width="match_parent"
    android:layout_height="match_parent"
    tools:context=".LinearActivity">
    <LinearLayout
        android:id="@+id/linear"
        android:layout_width="411dp"
        android:layout_height="729dp"
        android:orientation="vertical"
        app:layout_constraintBottom_toBottomOf="parent"
        app:layout_constraintTop_toTopOf="parent"
        tools:layout_editor_absoluteX="0dp">


        <EditText
            android:id="@+id/editText"
            android:layout_width="match_parent"
            android:layout_height="wrap_content"
            android:ems="10"
            android:inputType="textPersonName"
            android:text="Name" />

        <LinearLayout
            android:layout_width="match_parent"
            android:layout_height="match_parent"
            android:layout_weight="1"
            android:orientation="horizontal">

            <EditText
                android:id="@+id/editText2"
                android:layout_width="match_parent"
                android:layout_height="wrap_content"
                android:layout_weight="1"
                android:ems="10"
                android:inputType="textPersonName"
                android:text="Name" />

            <EditText
                android:id="@+id/editText3"
                android:layout_width="match_parent"
                android:layout_height="wrap_content"
                android:layout_weight="1"
                android:ems="10"
                android:inputType="textPersonName"
                android:text="Name" />

        </LinearLayout>

        <EditText
            android:id="@+id/editText4"
            android:layout_width="match_parent"
            android:layout_height="match_parent"
            android:layout_weight="1"
            android:ems="10"
            android:gravity="start|top"
            android:inputType="textMultiLine" />

        <Button
            android:id="@+id/button"
            android:layout_width="match_parent"
            android:layout_height="wrap_content"
            android:text="Button" />

    </LinearLayout>
</androidx.constraintlayout.widget.ConstraintLayout>

อธิบายความแตกต่างระหว่าง vertical และ horizontal orientation

```
vertical orientation คือการจัดเรียงให้อยู่ในแนวตั้ง ส่วน horizontal orientation คือการจัดเรียงให้อยู่ในแนวนอน
```

## Constrant Layout

จงออกแบบและสร้างหน้า Constrant layout สำหรับแสดงข้อมูลนักศึกษา ประกอบไปด้วย รูปโปรไฟล์ รูปพื้นหลัง ชื่อ-นามสกุล รหัสนักศึกษา และเกรดเฉลี่ยรวม

```xml
<?xml version="1.0" encoding="utf-8"?>
<androidx.constraintlayout.widget.ConstraintLayout xmlns:android="http://schemas.android.com/apk/res/android"
    xmlns:app="http://schemas.android.com/apk/res-auto"
    xmlns:tools="http://schemas.android.com/tools"
    android:layout_width="match_parent"
    android:layout_height="match_parent"
    tools:context=".ConstraintActivity">

    <ImageView
        android:id="@+id/imageView2"
        android:layout_width="415dp"
        android:layout_height="615dp"
        android:scaleType="centerCrop"
        app:layout_constraintEnd_toEndOf="parent"
        app:layout_constraintStart_toStartOf="parent"
        app:layout_constraintTop_toTopOf="parent"
        app:srcCompat="@drawable/BG" />

    <TextView
        android:id="@+id/textView"
        android:layout_width="wrap_content"
        android:layout_height="wrap_content"
        android:layout_marginTop="320dp"
        android:text="พรหมพัฒน์ ชาญโชคประเสริฐ"
        android:textSize="20sp"
        app:layout_constraintTop_toTopOf="@+id/imageView2"
        tools:layout_editor_absoluteX="80dp" />

    <Button
        android:id="@+id/button5"
        android:layout_width="142dp"
        android:layout_height="86dp"
        android:text="ย้อนกลับ"
        tools:layout_editor_absoluteX="134dp"
        tools:layout_editor_absoluteY="629dp" />

    <TextView
        android:id="@+id/textView3"
        android:layout_width="wrap_content"
        android:layout_height="wrap_content"
        android:layout_marginStart="80dp"
        android:text="รหัสนักศึกษา 603410052-3"
        android:textSize="20sp"
        app:layout_constraintStart_toStartOf="parent"
        tools:layout_editor_absoluteY="392dp" />

    <ImageView
        android:id="@+id/imageView3"
        android:layout_width="239dp"
        android:layout_height="210dp"
        android:scaleType="centerCrop"
        app:srcCompat="@drawable/me"
        tools:layout_editor_absoluteX="85dp"
        tools:layout_editor_absoluteY="43dp" />

    <TextView
        android:id="@+id/textView2"
        android:layout_width="wrap_content"
        android:layout_height="wrap_content"
        android:text="เกรดเฉลี่ย 3.05"
        android:textSize="20sp"
        tools:layout_editor_absoluteX="140dp"
        tools:layout_editor_absoluteY="467dp" />

</androidx.constraintlayout.widget.ConstraintLayout>
```
