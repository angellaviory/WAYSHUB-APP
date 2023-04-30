## 1. Buatlah BASH Script untuk Instalasi Docker 
1. Buat file nano docker.sh
<img width="811" alt="Screenshot 2023-04-19 at 17 32 39" src="https://user-images.githubusercontent.com/102456153/233049025-9c7e4cc2-3047-42ab-8488-23b7ee9e4e35.png">

2. Didalam file tersebut, tulis command untuk menginstall docker seperti dibawah ini.
```
#!/usr/bin/env bash

sudo apt-get update

sudo apt-get install
ca-certificates
curl
gnupg

sudo install -m 0755 -d/etc/apt/keyrings

curl -fsSL https://download.docker.com/linux/ubuntu/gpg sudo gpg --dearmor -o /etc/apt/keyrings/docker.gpg

sudo chmod a+r /etc/apt/keyrings/docker.gpg

sudo aot-get undate

sudo apt-get install docker-ce docker-ce-cl1 contalnerd.10 docker-bulldx-plugin docker-compose-plugin
```

3. Kemudian jalankan perintah ``bash docker.sh`` dan docker pun akan terinstall
<img width="807" alt="Screenshot 2023-04-19 at 17 33 31" src="https://user-images.githubusercontent.com/102456153/233049063-000cdef8-cf36-4084-81ed-b1f0d2f8f86a.png">


## 2. Dockerized Image Aplikasi wayshub-frontend Sekecil Mungkin


## 3. Jalankan NGINX On Top Docker
- Pertama membuat file docker compose nginx
<img width="574" alt="Screenshot 2023-04-30 at 22 25 50" src="https://user-images.githubusercontent.com/102456153/235362406-695ca796-e5fc-454b-9090-e03ca5280d19.png">

- Build file docker nginx
<img width="571" alt="Screenshot 2023-04-30 at 22 26 23" src="https://user-images.githubusercontent.com/102456153/235362409-03567d18-e50e-40b7-a9ee-2163023b9501.png">

- Pastikan nginx sudah running
<img width="1219" alt="Screenshot 2023-04-30 at 22 26 42" src="https://user-images.githubusercontent.com/102456153/235362411-5585bebe-8e50-4827-a228-cff9913dcc0c.png">

- Coba akses di browser. Nginx telah berhasil running menggunakan docker
<img width="1321" alt="Screenshot 2023-04-30 at 22 27 32" src="https://user-images.githubusercontent.com/102456153/235362416-bbe1a264-6358-42ca-9d2a-2fbb0cdc7962.png">
