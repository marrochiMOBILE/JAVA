# parseInt 1

Metode ini digunakan untuk mendapatkan tipe data primitif dari String tertentu. parseInt () adalah metode statis dan dapat memiliki satu atau dua argumen. yg pada intinya merubah string menjadi nilai integer

### syntax
```java
 int nama = parseInt(String s)
 int nama2 = parseInt(String s, int radix)
```
### Parameters

1. s - Ini adalah representasi string desimal.
1. radix - Ini akan digunakan untuk mengubah String menjadi integer.

### Return Value
1. parseInt (String s) - Ini mengembalikan integer (hanya desimal).
1. parseInt (int i) - Ini mengembalikan bilangan bulat, diberi representasi string desimal, biner, oktal, atau heksadesimal (radix masing-masing 10, 2, 8, atau 16) angka sebagai input.


contoh program dibawah ini :
```java
      int x =Integer.parseInt("9");
      double c = Double.parseDouble("5");
      int b = Integer.parseInt("444",16);

      System.out.println(x);
      System.out.println(c);
      System.out.println(b);
```

contoh dialam android :
```java
// disimpan dalam varibel nilai dari form yg di input untuk jenis text field
                String inputnama = String.valueOf(enama.getText().toString());
                String inputtempatlahir = String.valueOf(etempatlahir.getText().toString());
                String inputtanggallahir = String.valueOf(etanggallahir.getText().toString());
                String inputTugas = String.valueOf(etTugas.getText().toString());
                String inputUTS = String.valueOf(etUTS.getText().toString());
                String inputUAS = String.valueOf(etUAS.getText().toString());

                // disimpan dalam varibel nilai dari form yg di input untuk jenis radio button
                int gender = rgjk.getCheckedRadioButtonId(); // disini data akan ditangkap nilai integer contoh 1,2,...

                // iniliasisasi untuk radio button group yg dipilih
                RadioButton jk = (RadioButton) findViewById(gender);

                // disimpan kedalam variabel
                String inputjk = String.valueOf(jk.getText().toString());

                //perhitungan total nilai, rata-rata,  grade
                int totalNilai = Integer.parseInt(inputTugas) + Integer.parseInt(inputUTS) + Integer.parseInt(inputUAS) ;
                int NilairataRata = (Integer.parseInt(inputTugas) + Integer.parseInt(inputUTS) + Integer.parseInt(inputUAS))/3 ;
```
