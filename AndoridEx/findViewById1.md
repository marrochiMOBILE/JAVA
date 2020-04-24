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

