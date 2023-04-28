# DOCKER
## Server
### Appserver
<img width="928" alt="Screenshot 2023-04-19 at 11 42 57" src="https://user-images.githubusercontent.com/102456153/232969015-842bafb1-3e12-4ed2-9edb-7d8e634cddfb.png">

### Gateway
<img width="929" alt="Screenshot 2023-04-19 at 11 43 01" src="https://user-images.githubusercontent.com/102456153/232969010-fb6b0d60-4973-4f39-8789-be5880c02f68.png">

## 1. Instalasi Docker
1. Pertama lakukan update pada appserver. Kemudian lakukan instalasi **ca-certificate**, **curl**, dan **gpug**.
<img width="574" alt="Screenshot 2023-04-17 at 19 08 07" src="https://user-images.githubusercontent.com/102456153/232969217-5c44753e-3174-41df-94c9-e38b8abf6e58.png">
<img width="972" alt="Screenshot 2023-04-17 at 19 15 58" src="https://user-images.githubusercontent.com/102456153/232969235-254551df-646d-4499-8190-91dda8a33ed8.png">


2. Membuat directory baru untuk GPG key, yang kemudian di download kunci GPG tersebut di Docker dan disimpan di directory. 
<img width="914" alt="Screenshot 2023-04-17 at 19 17 06" src="https://user-images.githubusercontent.com/102456153/232969227-9c40665e-b16f-4b6b-ac45-f158beced6cb.png">


3. Selanjutnya melakukan set up repository.
<img width="977" alt="Screenshot 2023-04-17 at 19 19 02" src="https://user-images.githubusercontent.com/102456153/232969255-266581f6-cc6b-45ca-90d7-0bfb7c91ae56.png">


4. Setelah semua telah dilakukan, update appserver untuk memperbaharui apa yang telah di install dan juga memastikan sudah di instalasi.
<img width="986" alt="Screenshot 2023-04-17 at 19 19 24" src="https://user-images.githubusercontent.com/102456153/232969276-922fcc0f-a25a-43fd-ad6d-4eab9291717d.png">



5. Sekarang adalah langkah dimana menginstalasi docker engine, docker container dan plugin untuk docker build & docker compose.
<img width="983" alt="Screenshot 2023-04-17 at 19 19 31" src="https://user-images.githubusercontent.com/102456153/232968362-ecb65157-a2f1-472a-9c74-69a0d8ae521e.png">


6. Untuk memastikan docker telah berhasil di install, lakukan docker version. Dapat di lihat bahwa ada tulisan permission denied untuk user anba. Hal yang harus dilakukan adalah memberikan permission pada user anba.
<img width="906" alt="Screenshot 2023-04-17 at 19 21 49" src="https://user-images.githubusercontent.com/102456153/232969287-0c4355da-e9af-4fd9-a52c-0e746507dd52.png">


7. Dapat di lihat, setelah memberikan permission, user anba dapat mengakses dan berikut isi dari docker version.
<img width="775" alt="Screenshot 2023-04-17 at 19 22 24" src="https://user-images.githubusercontent.com/102456153/232969299-bc992f86-e0a8-4d7f-991f-e6818f6c9a4d.png">


## 2. Deploy Aplikasi Wayshub
1. Pertama lakukan clone aplikasi wayshub frontend dan wayshub backend dari github.
<img width="776" alt="Screenshot 2023-04-17 at 19 23 12" src="https://user-images.githubusercontent.com/102456153/232968414-d1420594-68f9-41be-9522-09f83e9d5e82.png">


2. Masuk ke dalam directory wayshub-frontend, dan ubah configurasi di config.js.
<img width="777" alt="Screenshot 2023-04-17 at 19 24 32" src="https://user-images.githubusercontent.com/102456153/232968437-57182622-0240-4e54-8a30-c319b31b8fc4.png">


3. Lakukan hal sama pada configurasi pada wayshub-backend di config.json.
<img width="774" alt="Screenshot 2023-04-17 at 19 26 10" src="https://user-images.githubusercontent.com/102456153/232968441-6c86ac87-27ff-420c-a4f1-dff64c98cb50.png">


4. Buat **Dockerfile** pada directory wayshub-frontend dan wayshub-backend.
<img width="774" alt="Screenshot 2023-04-17 at 19 27 21" src="https://user-images.githubusercontent.com/102456153/232968305-f5e84ae9-b8c5-4cfe-98f7-7892a653dc85.png">
<img width="774" alt="Screenshot 2023-04-17 at 19 25 10" src="https://user-images.githubusercontent.com/102456153/232968313-76e3ce26-3527-4ea7-90b2-5cfcae0c7df0.png">

5. Selanjutnya membuat docker compose menggunakan yaml file.
<img width="573" alt="Screenshot 2023-04-28 at 20 34 55" src="https://user-images.githubusercontent.com/102456153/235189475-4f14e9eb-5069-482a-a297-2a844312fb96.png">
<img width="574" alt="Screenshot 2023-04-28 at 20 35 04" src="https://user-images.githubusercontent.com/102456153/235189836-087c4901-9f73-419e-b1e9-583365a386d6.png">


6. Buat juga docker compose untuk database mysql.
<img width="573" alt="Screenshot 2023-04-28 at 20 35 22" src="https://user-images.githubusercontent.com/102456153/235189487-38728fd4-a1bf-47a2-84f9-6415662a34bc.png">


7. Kemudian build docker compose dan database compose.
<img width="731" alt="Screenshot 2023-04-28 at 20 55 23" src="https://user-images.githubusercontent.com/102456153/235189562-09b7c2fe-85f0-4eac-8868-1ce7f1392230.png">
<img width="571" alt="Screenshot 2023-04-28 at 22 20 55" src="https://user-images.githubusercontent.com/102456153/235189567-40adcaa4-545f-4301-b5e7-73260da35d85.png">

8. Pastikan jika aplikasi wayshub telah berhasil di build dan sudah running.
<img width="1276" alt="Screenshot 2023-04-28 at 22 21 34" src="https://user-images.githubusercontent.com/102456153/235189587-bef6b3cf-6717-47ff-92b5-24cfdd75ab9e.png">


9. Aplikasi telah berhasil berjalan di browser.
<img width="1348" alt="Screenshot 2023-04-28 at 22 23 17" src="https://user-images.githubusercontent.com/102456153/235189604-fb3812e8-4fbe-48b9-b0a0-450725760d8c.png">
<img width="1349" alt="Screenshot 2023-04-28 at 22 23 09" src="https://user-images.githubusercontent.com/102456153/235189612-a5e9bcf9-28bc-40e1-a99c-c84a54a77025.png">

## 3. Reverse Proxy dan SSL Certificate
- Berikut reverse proxy dan serta certbot sertifikasi pada aplikasi wayshub-frontend dan wayshub-backend di server **GATEWAY** 
<img width="571" alt="Screenshot 2023-04-28 at 22 30 38" src="https://user-images.githubusercontent.com/102456153/235191029-5070ba3b-7945-4542-b3d0-fee56fc88a6d.png">
<img width="571" alt="Screenshot 2023-04-28 at 22 30 44" src="https://user-images.githubusercontent.com/102456153/235191037-8632d78a-fe71-4c54-82e9-8d2267600c05.png">

