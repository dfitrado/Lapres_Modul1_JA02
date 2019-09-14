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
##### Screenshot:

### NO2
Filter sehingga wireshark hanya mengambil paket yang berasal dari port 80 (ajk.if.its.ac.id)
#### Jawab:
```
src port 80 && host ajk.if.its.ac.id
```
##### Screenshot:

### NO3
Filter sehingga wireshark hanya menampilkan paket yang menuju port 443 (google.com)
#### Jawab:
````
dst port 443 && host google.com
````
##### Screenshot:

### NO4
Filter sehingga wireshark hanya mengambil paket yang berasal dari ip kalian
#### Jawab:
```
src ip <ip kalian>
```
##### Screenshot:

### NO5
Filter sehingga wireshark hanya mengambil paket yang tujuannya ke monta.if.its.ac.id
#### Jawab:
````
dst host monta.if.its.ac.id
````
##### Screenshot:

<br />

## Display Filter
### NO1
Tampilkan semua paket yang hostnya mengandung www.ne.its.ac.id
#### Jawab:
```
http.host == ne.its.ac.id
```
#### Screenshot:


### NO2
Tampilkan paket yang hanya berasal dari IP 10.151.36 81 dan menuju web "mb.its.ac.id"
#### Jawab:
```
ip.src == 10.151.36.81 && http.host == "mb.its.ac.id"
```
#### Screenshot:


### NO3
Simpan gambar ckedokteran.png
#### Jawab:

#### Screenshot:

### NO4
Cari charset dari halaman "ajk.if.its.ac.id"
#### Jawab:

#### Screenshot:

### NO5
Cari username dan password ketika login di "freeshare.lp.if.its ac.id"
#### Jawab:

#### Screenshot:

### NO6
Sebutkan web server yang digunakan pada "www.ne.its.ac.id"
#### Jawab:

#### Screenshot:

### NO7
Sebutkan versi PHP dan yang digunakan pada "riset.ajk.if.its.ac.id"
#### Jawab:

#### Screenshot:

### NO8
Filter pada wireshark kalian sehingga menampilkan hasil ping
#### Jawab:

#### Screenshot:

### NO9
Dapatkan semua metode GET yang mengakses "monta.if.its.ac.id"
#### Jawab:

#### Screenshot:

### NO10
Tunjukkan username dan password yang dimasukkan ketika login FTP
#### Jawab:

#### Screenshot:

### NO11
Tunjukkan di wireshark, paket mana yang dikirimkan FTP client ketika upload file 
#### Jawab:

#### Screenshot:

### NO12
Tunjukkan di wireshark, paket mana yang dikirimkan FTP client ketika menghapus file 
#### Jawab:

#### Screenshot:

### NO13
Tunjukkan di wireshark, paket mana yang dikirimkan FTP client ketika mengganti nama file "sutlin.png"
#### Jawab:

#### Screenshot:

### NO14
Tunjukkan di wireshark, paket mana yang dikirimkan FTP client ketika download file "sutlun.png"
#### Jawab:

#### Screenshot:

### NO15
Cari file .zip di wireshark lalu download dan extract file tersebut <br />
clue: "50 4B 03 04"
#### Jawab:

#### Screenshot:



