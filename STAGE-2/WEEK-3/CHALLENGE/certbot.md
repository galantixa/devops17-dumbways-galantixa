# CERTBOT

### Install Snap & Certbot
#### Apa itu snap? snap adalah package manager untuk penginstalan sofware atau service pada linux sama seperti apt, bedanya apt merupakan package manager bawaan dari debian base salah satunya adalah ubuntu
-  ```sudo apt update && sudo apt install snap```
-  ![WaysHub - Google Chrome 08_07_2023 16_50_29](https://github.com/galantixa/devops17-dumbways-galantixa/assets/92994294/345585ec-3c32-473b-890d-f43553c1ee58)
-  ```sudo snap install core; sudo snap refresh core``` untuk mengupdate snap
-  ![Terminal 08_07_2023 16_53_14](https://github.com/galantixa/devops17-dumbways-galantixa/assets/92994294/5ca341c8-0d54-4697-9489-51fd61956fde)
-  ***NOTE!*** Jika sebelumnya sudah menginstall certbot dengan package manager apt! alangkah baiknya hapus dulu ```sudo apt remove certbot```
-  ![Certbot Instructions _ Certbot - Google Chrome 08_07_2023 16_54_00](https://github.com/galantixa/devops17-dumbways-galantixa/assets/92994294/b8a9f781-7ac6-4532-bf9a-8a827e695f0e)
-  Kemudian install certbot melalui snap ``` sudo snap install --classic certbot```
-  ![Certbot Instructions _ Certbot - Google Chrome 08_07_2023 16_55_14](https://github.com/galantixa/devops17-dumbways-galantixa/assets/92994294/60cc296a-905d-435b-a494-854688d3cf32)
-  Jalankan perintah ```sudo ln -s /snap/bin/certbot /usr/bin/certbot``` ***NOTE*** Digunakan untuk memastikan comand ```certbot``` dapat dieksekusi dan dijalankan pada terminal
-  ![Certbot Instructions _ Certbot - Google Chrome 08_07_2023 16_55_46](https://github.com/galantixa/devops17-dumbways-galantixa/assets/92994294/f521bef1-69dc-4cb4-a8a8-31d85fc66e1e)
-  ***SPECIAL CASE!!!*** Untuk mendapatkan sertifikasi ```https://``` pada reverse-proxy nginx aplikasi wayshub
-  ```sudo certbot --nginx``` konfirmasi email dan domain mana yang akan kita dapatkan sertifikasi https nya
-  Lakukan hal yang sama pada domain backend
-  ![Terminal 08_07_2023 16_57_19](https://github.com/galantixa/devops17-dumbways-galantixa/assets/92994294/f515bc11-99b5-4667-9354-677740dbf5b2)
-  ![Terminal 08_07_2023 16_57_33](https://github.com/galantixa/devops17-dumbways-galantixa/assets/92994294/e8b0edd4-619a-4b47-a118-241382bfe1ac)
-  ![Certbot Instructions _ Certbot - Google Chrome 08_07_2023 17_19_47](https://github.com/galantixa/devops17-dumbways-galantixa/assets/92994294/729c3301-d975-4bc4-a383-2e0c7015d200)
-  ```https://fajar.studentdumbways.my.id``` ```https://api.fajar.studentdumbways.my.id```
-  ![WaysHub - Google Chrome 08_07_2023 17_23_33](https://github.com/galantixa/devops17-dumbways-galantixa/assets/92994294/92653001-7174-4f50-b7e8-50621598fc62)
-  ![WaysHub - Google Chrome 08_07_2023 17_23_53](https://github.com/galantixa/devops17-dumbways-galantixa/assets/92994294/d2442298-85ac-48dc-ac76-f37b548fbd33)

### YAUDAH!
