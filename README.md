# Laporan Praktikum Modul 1 Jarkom 2019

### Oleh:
- Donny Fitrado (05111740000171)
- Faqih Fathan Irfani (05111740000175)

## Capture Filter
### NO1
Filter sehingga wireshark hanya mengambil paket yang mengandung port 21
#### Jawab:
```
port 21
```

### NO2
Filter sehingga wireshark hanya mengambil paket yang berasal dari port 80 (ajk.if.its.ac.id)
#### Jawab:
```
src port 80 && host ajk.if.its.ac.id
```

### NO3
Filter sehingga wireshark hanya menampilkan paket yang menuju port 443 (google.com)
#### Jawab:
````
dst port 443 && host google.com
````

### NO4
Filter sehingga wireshark hanya mengambil paket yang berasal dari ip kalian
#### Jawab:
```
src ip <ip kalian>
```

### NO5
Filter sehingga wireshark hanya mengambil paket yang tujuannya ke monta.if.its.ac.id
#### Jawab:
````
dst host monta.if.its.ac.id
````

<br />

## Display Filter
### NO1
Tampilkan semua paket yang hostnya mengandung www.ne.its.ac.id

### NO2
Tampilkan paket yang hanya berasal dari IP 10.151.36 81 dan menuju web "mb.its.ac.id"

### NO3
Simpan gambar ckedokteran.png

### NO4
Cari charset dari halaman "ajk.if.its.ac.id"

### NO5
Cari username dan password ketika login di "freeshare.lp.if.its ac.id"

### NO6
Sebutkan web server yang digunakan pada "www.ne.its.ac.id"

### NO7
Sebutkan versi PHP dan yang digunakan pada "riset.ajk.if.its.ac.id"

### NO8
Filter pada wireshark kalian sehingga menampilkan hasil ping

### NO9
Dapatkan semua metode GET yang mengakses "monta.if.its.ac.id"

### NO10
Tunjukkan username dan password yang dimasukkan ketika login FTP

### NO11
Tunjukkan di wireshark, paket mana yang dikirimkan FTP client ketika upload file 

### NO12
Tunjukkan di wireshark, paket mana yang dikirimkan FTP client ketika menghapus file 

### NO13
Tunjukkan di wireshark, paket mana yang dikirimkan FTP client ketika mengganti nama file "sutlin.png"

### NO14
Tunjukkan di wireshark, paket mana yang dikirimkan FTP client ketika download file "sutlun.png"

### NO15
Cari file .zip di wireshark lalu download dan extract file tersebut 
                                clue: "50 4B 03 04"




