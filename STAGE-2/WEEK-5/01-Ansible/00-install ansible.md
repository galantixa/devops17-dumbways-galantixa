## Install ansible local machine
-  Install ansible dengan apt module
-  masukan repository ppa ansible
-  ![Screenshot from 2023-07-19 20-53-58](https://github.com/galantixa/devops17-dumbways-galantixa/assets/92994294/833f6779-e4ba-4c56-a524-8af14777785b)
-  ```sudo apt install ansible -y```
-  Cek versi ansible
-  ![Screenshot from 2023-07-19 20-54-13](https://github.com/galantixa/devops17-dumbways-galantixa/assets/92994294/fbba487b-0746-4ecf-af9a-c908a4a8986c)
-  ![Screenshot from 2023-07-19 13-24-53](https://github.com/galantixa/devops17-dumbways-galantixa/assets/92994294/8dcc46ed-eaa7-40c0-a30c-d4cd6a5b20d0)
- Buat config file ```ansible.cfg``` dan ```Inventory``` hosts untuk remote akses
- ![code17](https://github.com/galantixa/devops17-dumbways-galantixa/assets/92994294/e715621c-39e5-4089-8882-23705b5e99ef)
- ![code18](https://github.com/galantixa/devops17-dumbways-galantixa/assets/92994294/f788696f-f734-48d4-9436-2d6000ec1756)
- cek koneksi remote ```ansible all -m ping``` pastikan semua hosts terindikasi hijau