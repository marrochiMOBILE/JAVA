# findViewById 1

Digunakan untuk mencari id dari widget/view/elemen dari layar.

#### syntax
```
findViewById(R.id.nama_view)
```
#### Keterangan:
```
R.id.nama_view ini adalah view/widget yang mempunyai id=”@+id/nama_view“.
```

potongan didalam sebuah file xml anda akan menemukan id=@+id/...

```xml
<Button

android:text=”Tekan”
android:id=”@+id/tombol”
android:layout_width=”wrap_content”
android:layout_height=”wrap_content”

/>
```

cara menangkapnya

```
findViewById(R.id.tombol)
```
anda jugha bisa menggunakan cara seperti ini dengan attribut
```java
// atribut
Button btnOK;

// inialisasi
btnOK = (Button) findViewById(R.id.tomboln);

```


## getText
getText() adalah fungsi yang ada pada Java untuk mengambil teks yang diinput pada form

```java
// atribut
EditText InputNim;

// inialisasi
InputNim = (EditText) findViewById(R.id.tomboln);

InputNim.getText().toString();
```

## setText()
untuk memunculkan sebuah teks pada text area atau text field dapat menggunakan fungsi setText().

```java
// atribut
EditText InputNim;
TextView Hasil;

// inialisasi
InputNim = (EditText) findViewById(R.id.tomboln);
Hasil.setText("\n" + "hasil input: "+ InputNim.getText().toString() +
"\n");
```
## getCheckedRadioButtonId
 adalah fungsi yang ada pada Java untuk mengambil teks yang diinput pada form radio button
 ```java
 // attribut
 RadioGroup rgjk;
 
 // inialisasi
 rgjk = (RadioGroup) findViewById(R.id.jk);
 
 // menaruh nilai ke variable 
 int gender = rgjk.getCheckedRadioButtonId();
 
 // inialisasi lagi
 RadioButton jk = (RadioButton) findViewById(gender);
 
// disimpan kedalam variable tapi bukan lagi radio button tapi text
String inputjk = String.valueOf(jk.getText().toString());
 ```
 
## perhatikan 1

#### activity_main.xml
```xml
<?xml version="1.0" encoding="utf-8"?>
<LinearLayout xmlns:android="http://schemas.android.com/apk/res/android"
xmlns:app="http://schemas.android.com/apk/res-auto"
xmlns:tools="http://schemas.android.com/tools"
tools:context=".MainActivity"
android:orientation="vertical"
android:layout_width="match_parent"
android:layout_height="match_parent">

<LinearLayout
    android:layout_width="match_parent"
    android:layout_height="match_parent"
    android:orientation="vertical">

    <LinearLayout
        android:layout_width="match_parent"
        android:layout_height="wrap_content"
        android:background="#e7e">

        <TextView
            android:layout_width="match_parent"
            android:layout_height="wrap_content"
            android:layout_marginBottom="10dp"
            android:layout_marginTop="10dp"
            android:text="BAGIAN HEADER"
            android:textAlignment="center"
            android:textColor="#fff"
            android:textStyle="bold" />
    </LinearLayout>

    <ScrollView
        android:layout_width="match_parent"
        android:layout_height="match_parent">
        <LinearLayout
            android:layout_width="match_parent"
            android:layout_height="wrap_content"
            android:layout_marginLeft="5dp"
            android:layout_marginRight="5dp"
            android:orientation="vertical">

            <TextView
                android:layout_width="match_parent"
                android:layout_height="wrap_content"
                android:text="NPM\t\t:" />

            <EditText
                android:id="@+id/isinpm"
                android:inputType="number"
                android:layout_width="match_parent"
                android:layout_height="wrap_content"
                android:hint="Masukan NPM" />

            <TextView
                android:layout_width="match_parent"
                android:layout_height="wrap_content"
                android:text="Nama\t\t:" />

            <EditText
                android:id="@+id/isinama"
                android:layout_width="match_parent"
                android:layout_height="wrap_content"
                android:hint="Masukan Nama" />

            <TextView
                android:layout_width="match_parent"
                android:layout_height="wrap_content"
                android:text="Jenis Kelamin\t:" />
            <RadioGroup
                android:layout_width="match_parent"
                android:id="@+id/jk"
                android:layout_height="wrap_content">
                <RadioButton
                    android:layout_width="wrap_content"
                    android:layout_height="wrap_content"
                    android:text="Laki - laki" />

                <RadioButton
                    android:layout_width="wrap_content"
                    android:layout_height="wrap_content"
                    android:text="Perempuan" />
            </RadioGroup>

            <TextView
                android:layout_width="match_parent"
                android:layout_height="wrap_content"
                android:text="Kelas\t\t\t\t\t\t:" />

            <Spinner
                android:id="@+id/kelas"
                android:entries="@array/pilihkelas"
                android:layout_width="match_parent"
                android:layout_height="wrap_content"></Spinner>

            <TextView
                android:layout_width="match_parent"
                android:layout_height="wrap_content"
                android:text="Agama\t\t\t\t\t:" />

            <Spinner
                android:id="@+id/agama"
                android:entries="@array/pilihagama"
                android:layout_width="match_parent"
                android:layout_height="wrap_content"></Spinner>

            <TextView
                android:layout_width="match_parent"
                android:layout_height="wrap_content"
                android:text="Tempat Lahir\t:" />

            <EditText
                android:id="@+id/tempatlahir"
                android:layout_width="wrap_content"
                android:layout_height="wrap_content"
                android:text=""
                android:hint="Masukan Tempat Lahir" />

            <TextView
                android:layout_width="match_parent"
                android:layout_height="wrap_content"
                android:text="Tanggal Lahir\t:" />

            <EditText
                android:id="@+id/tanggallahir"
                android:layout_width="wrap_content"
                android:text=""
                android:inputType="date"
                android:layout_height="wrap_content"
                android:hint="dd/MM/yyyy" />

            <TextView
                android:layout_width="match_parent"
                android:layout_height="wrap_content"
                android:text="Masukan Nilai Tugas\t:" />

            <EditText
                android:id="@+id/NilaiTugas"
                android:layout_width="wrap_content"
                android:text=""
                android:layout_height="wrap_content"
                android:hint="....................."
                android:inputType="number"/>

            <TextView
                android:layout_width="match_parent"
                android:layout_height="wrap_content"
                android:text="Masukan Nilai UTS\t:" />

            <EditText
                android:id="@+id/NilaiUTS"
                android:layout_width="wrap_content"
                android:text=""
                android:layout_height="wrap_content"
                android:hint="....................."
                android:inputType="number"/>
            <TextView
                android:layout_width="match_parent"
                android:layout_height="wrap_content"
                android:text="Masukan Nilai UAS\t:" />

            <EditText
                android:id="@+id/NilaiUAS"
                android:layout_width="wrap_content"
                android:text=""
                android:layout_height="wrap_content"
                android:hint="....................."
                android:inputType="number"/>

            <Button
                android:id="@+id/simpan"
                android:layout_width="match_parent"
                android:layout_height="wrap_content"
                android:text="SIMPAN" />

            <TextView
                android:layout_width="match_parent"
                android:layout_height="wrap_content"
                android:text="===== HASIL INPUT ====="
                android:textAlignment="center" />
            <TextView
                android:id="@+id/hasil"
                android:layout_width="match_parent"
                android:layout_height="wrap_content"
                android:text=""
               />

            <TextView
                android:layout_width="match_parent"
                android:layout_height="wrap_content"
                android:text="======================="
                android:textAlignment="center" />
        </LinearLayout>

    </ScrollView>
</LinearLayout>
</LinearLayout>
```
kemudian tambahkan ke strings.xml dibawah ini
```xml
 <string-array name="pilihkelas">
        <item >--Pilih--</item>
        <item   >A</item>
        <item   >B</item>
        <item   >D</item>
        <item   >E</item>
        <item   >F</item>
        <item   >G</item>
        <item   >H</item>
        <item   >I</item>
        <item   >J</item>
        <item   >K</item>
        <item   >L</item>
        <item   >M</item>
        <item   >N</item>
    </string-array>

    <string-array name="pilihagama">
        <item >--Pilih--</item>
        <item   >Islam</item>
        <item   >Katolik</item>
        <item   >Protestan</item>
        <item   >Budha</item>
        <item   >Hindu</item>
        <item   >Konghucu</item>
    </string-array>
```

#### utsmarrochi171011400286.java
```java
package com.example.utsmarrochi171011400286;

import androidx.appcompat.app.AppCompatActivity;
import android.os.Bundle;
import android.view.View;
import android.widget.Button;
import android.widget.EditText;
import android.widget.RadioButton;
import android.widget.RadioGroup;
import android.widget.Spinner;
import android.widget.TextView;

public class MainActivity extends AppCompatActivity {
    // attribute
    Button bsimpan;
    EditText enpm, enama, etempatlahir, etanggallahir, etTugas, etUTS, etUAS;
    TextView thasil;
    RadioGroup rgjk;
    Spinner skelas, sagama;

    @Override
    protected void onCreate(Bundle savedInstanceState) {
        super.onCreate(savedInstanceState);
        setContentView(R.layout.activity_main);

        // inisialisasi
        bsimpan = (Button) findViewById(R.id.simpan);
        enpm = (EditText) findViewById(R.id.isinpm);
        enama = (EditText) findViewById(R.id.isinama);
        thasil = (TextView) findViewById(R.id.hasil);
        rgjk = (RadioGroup) findViewById(R.id.jk);
        skelas = (Spinner) findViewById(R.id.kelas);
        sagama  = (Spinner) findViewById(R.id.agama);
        etempatlahir = (EditText) findViewById(R.id.tempatlahir);
        etanggallahir = (EditText) findViewById(R.id.tanggallahir);
        etTugas = (EditText) findViewById(R.id.NilaiTugas);
        etUTS = (EditText) findViewById(R.id.NilaiUTS);
        etUAS = (EditText) findViewById(R.id.NilaiUAS);

        bsimpan.setOnClickListener(new View.OnClickListener() {
            @Override
            public void onClick(View v) {
                // String inputnpm = String.valueOf(enpm.getText().toString());

                // disimpan dalam varibel nilai dari form yg di input untuk jenis text field
                String inputnama = String.valueOf(enama.getText().toString());
                String inputtempatlahir = String.valueOf(etempatlahir.getText().toString());
                String inputtanggallahir = String.valueOf(etanggallahir.getText().toString());
                String inputTugas = String.valueOf(etTugas.getText().toString());
                String inputUTS = String.valueOf(etUTS.getText().toString());
                String inputUAS = String.valueOf(etUAS.getText().toString());

                // disimpan dalam varibel nilai dari form yg di input untuk jenis radio button
                int gender = rgjk.getCheckedRadioButtonId();

                // iniliasisasi untuk radio button group yg dipilih
                RadioButton jk = (RadioButton) findViewById(gender);

                // disimpan kedalam variabel
                String inputjk = String.valueOf(jk.getText().toString());

                //perhitungan total nilai, rata-rata,  grade
                int totalNilai = Integer.parseInt(inputTugas) + Integer.parseInt(inputUTS) + Integer.parseInt(inputUAS) ;
                int NilairataRata = (Integer.parseInt(inputTugas) + Integer.parseInt(inputUTS) + Integer.parseInt(inputUAS))/3 ;

                // sengaja diisi null atau '' biar tidak error
                String gradeNilai = null;

                // validation jika
                if(NilairataRata >= 80 && NilairataRata <= 100){
                    gradeNilai = "A";
                }else if(NilairataRata >= 70 && NilairataRata <= 79){
                    gradeNilai = "B";
                }else if(NilairataRata >= 60 && NilairataRata <= 69){
                    gradeNilai = "C";
                }else if(NilairataRata >= 50 && NilairataRata <= 59){
                    gradeNilai = "D";
                }else if(NilairataRata >= 0 && NilairataRata <= 49){
                    gradeNilai = "E";
                }

                // tampilkan dengan setText ke id thasil
                thasil.setText("\n" + "NPM\t\t\t\t\t\t\t\t\t\t: " + enpm.getText().toString() + "\n" +
                        "Nama\t\t\t\t\t\t\t\t\t\t: " + inputnama + "\n" +
                        "Jenis Kelamin\t\t\t\t\t: " + inputjk +"(  " + gender +"    )"+ "\n" +
                        "Kelas\t\t\t\t\t\t\t\t\t\t: " + skelas.getSelectedItem().toString() + "\n" +
                        "Agama\t\t\t\t\t\t\t\t\t: " + sagama.getSelectedItem().toString() + "\n" +
                        "Jenis Kelamin\t\t\t\t\t: " + inputtempatlahir + "\n" +
                        "Tanggal Lahir\t\t\t\t\t: " + inputtanggallahir + "\n" +
                        "Nilai Tugas \t\t\t\t\t\t: " + inputTugas + "\n" +
                        "Nilai UTS \t\t\t\t\t\t\t: " + inputUTS + "\n" +
                        "Nilai UAS \t\t\t\t\t\t\t: " + inputUAS + "\n" +
                        "Total Nilai \t\t\t\t\t\t\t: " + totalNilai + "\n" +
                        "Nilai Rata Rata \t\t\t\t: " + NilairataRata + "\n" +
                        "Grade \t\t\t\t\t\t\t\t\t: " + gradeNilai + "\n"

                );
            }
        });

    }
}

```
