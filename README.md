# Jarkom-Modul-2-B06-2022

### Kelompok 10 Kelas B

| **No** | **NRP** | **Nama** | 
| ------------- | ------------- | --------- |
| 1 | 5025201100 | Hansen Idden | 
| 2 | 5025201109 | Mohammad Firman Fardiansyah |
| 3 | 5025201167 | William Zefanya Maranatha |


## Soal 1
### WISE akan dijadikan sebagai DNS Master, Berlint akan dijadikan DNS Slave, dan Eden akan digunakan sebagai Web Server. Terdapat 2 Client yaitu SSS, dan Garden. Semua node terhubung pada router Ostania, sehingga dapat mengakses internet
Ostania untuk node dapat terhubung

<img width="1028" alt="image" src="https://user-images.githubusercontent.com/83849481/198837055-744b26e0-ba2a-4913-ac40-b1efa7be6da1.png">

Untuk node lainnya
`Echo “nameserver 192.168.122.1” > /etc/resolv.conf`

<img width="1026" alt="image" src="https://user-images.githubusercontent.com/83849481/198837109-1dac88e7-d710-4bc0-b946-42c1c20cf76c.png">

## Soal 2
### Untuk mempermudah mendapatkan informasi mengenai misi dari Handler, bantulah Loid membuat website utama dengan akses wise.yyy.com dengan alias www.wise.yyy.com pada folder wise
WISE

etc/bind/named.conf.local
<img width="790" alt="image" src="https://user-images.githubusercontent.com/83849481/198837166-4703f05d-df91-4b7e-a94f-e7b94cbb31ac.png">

etc/bind/wise/wise.b06.com
<img width="976" alt="image" src="https://user-images.githubusercontent.com/83849481/198837190-a521972b-5d42-4a77-aa36-01f83e11005e.png">

Ping wise.b06.com sudah berhasil
<img width="1011" alt="image" src="https://user-images.githubusercontent.com/83849481/198837209-ea876ced-6055-4198-9ba5-72a252c9597f.png">

## Soal 3
### Setelah itu ia juga ingin membuat subdomain eden.wise.yyy.com dengan alias www.eden.wise.yyy.com yang diatur DNS-nya di WISE dan mengarah ke Eden.
WISE

Cukup menambahkan eden pada wise.b06.com
<img width="995" alt="image" src="https://user-images.githubusercontent.com/83849481/198837262-fffb0bae-64f0-4104-9f96-cfdddc0af887.png">

Ping eden.wise.b06.com sudah berhasil
<img width="862" alt="image" src="https://user-images.githubusercontent.com/83849481/198837283-9bd1d1b4-8071-44b3-bfb8-4cecf0808527.png">

## Soal 4
### Buat juga reverse domain untuk domain utama
WISE

tambahkan ini ke /etc/bind/named.conf.local
<img width="895" alt="image" src="https://user-images.githubusercontent.com/83849481/198837358-d0c4abf2-800e-4aba-92d2-aaae0e97e13c.png">

/etc/bind/wise/3.6.10.in-addr.arpa
<img width="985" alt="image" src="https://user-images.githubusercontent.com/83849481/198837368-4d79ddd4-cbb0-463f-b3cb-760e65ae21eb.png">

Reverse sudah berhasil
<img width="697" alt="image" src="https://user-images.githubusercontent.com/83849481/198837391-237710d9-c76a-4394-adf1-1d8ee2f16066.png">

## Soal 5
### Agar dapat tetap dihubungi jika server WISE bermasalah, buatlah juga Berlint sebagai DNS Slave untuk domain utama
WISE

<img width="774" alt="image" src="https://user-images.githubusercontent.com/83849481/198837436-d5675e50-c388-43e4-b238-b8853696dd07.png">

Berlint

<img width="624" alt="image" src="https://user-images.githubusercontent.com/83849481/198837452-6e19d5ba-7611-4f0d-98ba-987d295b4cc1.png">

Test
Sudah berhasil
<img width="554" alt="image" src="https://user-images.githubusercontent.com/83849481/198837461-cb26455c-bd8f-4b88-a61d-320460a6be93.png">
<img width="820" alt="image" src="https://user-images.githubusercontent.com/83849481/198837470-3a32b146-5312-454b-99f8-71b26c554098.png">

## Soal 6
### Karena banyak informasi dari Handler, buatlah subdomain yang khusus untuk operation yaitu operation.wise.yyy.com dengan alias www.operation.wise.yyy.com yang didelegasikan dari WISE ke Berlint dengan IP menuju ke Eden dalam folder operation
WISE

<img width="994" alt="image" src="https://user-images.githubusercontent.com/83849481/198837504-ef3d3fbd-211b-4411-8362-a2c7d97996a1.png">
Berlint

<img width="871" alt="image" src="https://user-images.githubusercontent.com/83849481/198837539-ce2c5d8c-697c-4318-aef5-fffc5704ea85.png">
<img width="1021" alt="image" src="https://user-images.githubusercontent.com/83849481/198837555-2cb254de-ff5e-4edb-9334-c381c5429f74.png">

Ping operation.wise.b06.com sudah berhasil
<img width="887" alt="image" src="https://user-images.githubusercontent.com/83849481/198837573-08c8062f-4e78-4b98-ad53-490d0f72d6ab.png">

## Soal 7
### Untuk informasi yang lebih spesifik mengenai Operation Strix, buatlah subdomain melalui Berlint dengan akses strix.operation.wise.yyy.com dengan alias www.strix.operation.wise.yyy.com yang mengarah ke Eden
<img width="459" alt="image" src="https://user-images.githubusercontent.com/83849481/198837758-e18b066c-00fc-4bff-ba2a-d7da1993d669.png">

## Soal 8
### Setelah melakukan konfigurasi server, maka dilakukan konfigurasi Webserver. Pertama dengan webserver www.wise.yyy.com. Pertama, Loid membutuhkan webserver dengan DocumentRoot pada /var/www/wise.yyy.com
<img width="459" alt="image" src="https://user-images.githubusercontent.com/83849481/198837806-c757bde0-0244-48e1-9517-6789645a6fb2.png">

## Soal 9
### Setelah itu, Loid juga membutuhkan agar url www.wise.yyy.com/index.php/home dapat menjadi menjadi www.wise.yyy.com/home
<img width="331" alt="image" src="https://user-images.githubusercontent.com/83849481/198837834-968ce462-1ed8-4810-b190-4bf298fb517f.png">

## Soal 10 
### Setelah itu, pada subdomain www.eden.wise.yyy.com, Loid membutuhkan penyimpanan aset yang memiliki DocumentRoot pada /var/www/eden.wise.yyy.com
<img width="439" alt="image" src="https://user-images.githubusercontent.com/83849481/198837867-cd833852-4c04-40f9-befc-4a1d2caa13da.png">

## Soal 11 
### Akan tetapi, pada folder /public, Loid ingin hanya dapat melakukan directory listing saja
<img width="329" alt="image" src="https://user-images.githubusercontent.com/83849481/198837888-f7876f75-4d91-4177-9a81-ea2f9476cfa9.png">

## Soal 12 
### Tidak hanya itu, Loid juga ingin menyiapkan error file 404.html pada folder /error untuk mengganti error kode pada apache
<img width="325" alt="image" src="https://user-images.githubusercontent.com/83849481/198838067-a0d49fdc-8715-4a36-83ab-2818f545a6eb.png">

## Soal 13 
### Loid juga meminta Franky untuk dibuatkan konfigurasi virtual host. Virtual host ini bertujuan untuk dapat mengakses file asset www.eden.wise.yyy.com/public/js menjadi www.eden.wise.yyy.com/js
<img width="364" alt="image" src="https://user-images.githubusercontent.com/83849481/198838092-884dfb9a-d1c7-422c-aae3-5ae41b2b48d2.png">

## Soal 14
### Loid meminta agar www.strix.operation.wise.yyy.com hanya bisa diakses dengan port 15000 dan port 15500
<img width="575" alt="image" src="https://user-images.githubusercontent.com/83849481/198838134-4c8255c1-005b-4777-be35-c944ff824e27.png">
<img width="308" alt="image" src="https://user-images.githubusercontent.com/83849481/198838146-e9acdc0d-7649-4756-902d-938f2df37fbb.png">
<img width="437" alt="image" src="https://user-images.githubusercontent.com/83849481/198838156-7ff8a20a-c066-48cd-b54b-1ceef3641cbd.png">

## Soal 15
### Dengan autentikasi username Twilight dan password opStrix dan file di /var/www/strix.operation.wise.yyy
<img width="406" alt="image" src="https://user-images.githubusercontent.com/83849481/198838171-275b2e9e-0b60-4ed5-bb39-de08a3165811.png">

## Soal 16
### Dan setiap kali mengakses IP Eden akan dialihkan secara otomatis ke www.wise.yyy.com
<img width="338" alt="image" src="https://user-images.githubusercontent.com/83849481/198838198-ca881e93-b328-4ad2-bcc8-0398a5ac6308.png">

## Soal 17
### Karena website www.eden.wise.yyy.com semakin banyak pengunjung dan banyak modifikasi sehingga banyak gambar-gambar yang random, maka Loid ingin mengubah request gambar yang memiliki substring “eden” akan diarahkan menuju eden.png. Bantulah Agent Twilight dan Organisasi WISE menjaga perdamaian!
<img width="393" alt="image" src="https://user-images.githubusercontent.com/83849481/198838246-de446fa1-ae0b-4373-aab4-43d23862ebee.png">
<img width="368" alt="image" src="https://user-images.githubusercontent.com/83849481/198838255-f065f50b-bb44-4801-9cd2-b9b6ff32533e.png">


### Kendala
Masih perlu latihan lagi agar dapat menyelesaikan semua soal lebih cepat







