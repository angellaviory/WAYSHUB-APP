# CI/CD: Jenkins
## 1. Jalankan Jenkins On-Top Docker
- Install docker terlebih dahulu
<img width="928" alt="Screenshot 2023-04-28 at 23 18 39" src="https://user-images.githubusercontent.com/102456153/235202394-fd9ae812-cdb3-45ff-a85e-d402ca90bf49.png">

- Kemudian build jenkins dengan docker compose
<img width="634" alt="Screenshot 2023-04-28 at 23 19 11" src="https://user-images.githubusercontent.com/102456153/235202405-6e44697a-0d55-4afe-bcb7-07798240e787.png">
<img width="633" alt="Screenshot 2023-04-28 at 23 24 52" src="https://user-images.githubusercontent.com/102456153/235202633-cfd18de5-493e-493b-a901-40fda857c619.png">

- Pastikan docker jenkins telah running
<img width="1481" alt="Screenshot 2023-04-28 at 23 25 33" src="https://user-images.githubusercontent.com/102456153/235202644-77498819-2de5-4d6f-900e-27dd4bfb45fd.png">

- Jenkins telah berhasil dijalankan di browser
<img width="1317" alt="Screenshot 2023-04-28 at 22 55 47" src="https://user-images.githubusercontent.com/102456153/235200074-c021d62c-a93c-426b-b984-b4ae58f16aaf.png">

## 2. Membuat Pipeline Jenkins untuk Aplikasi Wayshub-frontend dan Wayshub-backend
- Lakukan registry jenkins dan login ke akun jenkins
<img width="1317" alt="Screenshot 2023-04-28 at 22 55 47" src="https://user-images.githubusercontent.com/102456153/235200074-c021d62c-a93c-426b-b984-b4ae58f16aaf.png">

- Kemudian masukkan private key pada configure manage credentials 
<img width="1320" alt="Screenshot 2023-04-28 at 22 56 41" src="https://user-images.githubusercontent.com/102456153/235200123-ea6b108e-c4d4-4aaa-a670-46b8452316f3.png">

- Mulai membuat pipeline untuk aplikasi wayshub-frontend dan wayshub-backend
<img width="1319" alt="Screenshot 2023-04-28 at 22 57 15" src="https://user-images.githubusercontent.com/102456153/235200208-5104b515-2767-49ec-bc41-d0fec35d47db.png">
<img width="1315" alt="Screenshot 2023-04-28 at 22 57 26" src="https://user-images.githubusercontent.com/102456153/235200221-c494865b-c6cd-4d0b-83f3-01d9a8d6130d.png">

- Masukkan ssh url github, branch dan dll. Hal ini dikarenakan setiap mengalami perubahan, penambahan pada Jenkinsfile harus di *add*, *commit* dan *push* ke akun github yang sudah di setting di server.
<img width="1320" alt="Screenshot 2023-04-28 at 22 58 08" src="https://user-images.githubusercontent.com/102456153/235200267-36a399db-76a0-47f4-9ca6-62e8d3d62a9c.png">
<img width="1317" alt="Screenshot 2023-04-28 at 22 58 14" src="https://user-images.githubusercontent.com/102456153/235200272-e239fa40-b7de-441c-832d-34add095f1d5.png">
<img width="1512" alt="Screenshot 2023-04-28 at 22 58 19" src="https://user-images.githubusercontent.com/102456153/235200278-6411f097-73e7-4954-aeb8-fb0430839647.png">

- Aplikasi wayshub-frontend dan wayshub-backend sudah berhasil di pull, build, run dan push ke docker hub.
<img width="1508" alt="Screenshot 2023-04-28 at 22 53 26" src="https://user-images.githubusercontent.com/102456153/235195567-3ffdc4ea-7e67-4313-9405-3ade6c8675ec.png">
<img width="1512" alt="Screenshot 2023-04-28 at 22 46 06" src="https://user-images.githubusercontent.com/102456153/235195576-e8631805-b921-4a56-9c3f-d9e2ed6cf954.png">

- Berikut aplikasi wayshub-frontend dan wayshub-backend telah berhasil di push ke docker hub.
<img width="1347" alt="Screenshot 2023-04-28 at 22 47 01" src="https://user-images.githubusercontent.com/102456153/235195582-f6d6c04c-5734-4a94-9b7b-a67744d27ab9.png">

## 3. Reverse Proxy dan SSL Certificate
- Berikut reverse proxy dan certbot sertifikasi yang ada di server **GATEWAY**
<img width="571" alt="Screenshot 2023-04-28 at 22 30 31" src="https://user-images.githubusercontent.com/102456153/235193107-0c2b3958-ace4-468b-b2dc-825d008b75e1.png">
