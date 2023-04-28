## Buatlah BASH Script untuk Instalasi Docker 
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

