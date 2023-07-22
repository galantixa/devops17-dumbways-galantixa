# Terraform
### Install Terraform
- Dalam case ini saya menginstall terraform di ubuntu desktop lokal
- Install GPG keys dan cek key
- ```wget -O- https://apt.releases.hashicorp.com/gpg | gpg --dearmor | sudo tee /usr/share/keyrings/hashicorp-archive-keyring.gpg```
- ```echo "deb [signed-by=/usr/share/keyrings/hashicorp-archive-keyring.gpg] https://apt.releases.hashicorp.com $(lsb_release -cs) main" | sudo tee /etc/apt/sources.list.d/hashicorp.list
- ![Screenshot from 2023-07-19 10-43-54](https://github.com/galantixa/devops17-dumbways-galantixa/assets/92994294/f3929b1e-92bf-4d0e-8aa7-b2af0f21044e)
- ![Screenshot from 2023-07-22 18-33-46](https://github.com/galantixa/devops17-dumbways-galantixa/assets/92994294/ebfe77cc-8575-412a-bfbe-5e1c1d7b738f)
- ```sudo apt update && sudo apt install terraform```
- Periksa apakah sudah terinstall ```terraform --help```
- ![Screenshot from 2023-07-19 10-44-53](https://github.com/galantixa/devops17-dumbways-galantixa/assets/92994294/697673d3-f9a6-4fa6-bb04-248d1e00869c)

### Create VM'S
- Buat folder dan file terpisah untuk script membuat VM 
- Masuk code editor atau bisa juga mengedit file memalui terminal dengan command vi atau nano
- ![Screenshot from 2023-07-19 11-20-58](https://github.com/galantixa/devops17-dumbways-galantixa/assets/92994294/0ab9a3d3-cbf4-40b3-926a-3cdbbbdf4c46)
- Edit dan buat script untuk membuat 3 VM appserver, gatewaym, monitorin
- ![code](https://github.com/galantixa/devops17-dumbways-galantixa/assets/92994294/689d3727-cbc0-4552-a526-9850f913d4f3)
- ![code1](https://github.com/galantixa/devops17-dumbways-galantixa/assets/92994294/c549d935-6ab9-47f5-ba4f-4fdd49c850d7)
- ![3](https://github.com/galantixa/devops17-dumbways-galantixa/assets/92994294/eaab8fff-f22f-45d4-9e6c-6a8eafb0e5ed)
- jalakan pada setiap folder ```terraform init```
- ```terraform plan && terraform apply```
- ![Screenshot from 2023-07-19 11-25-16](https://github.com/galantixa/devops17-dumbways-galantixa/assets/92994294/d8375db2-fb66-4347-92ad-afad29fe5af9)
- ![Screenshot from 2023-07-19 12-21-56](https://github.com/galantixa/devops17-dumbways-galantixa/assets/92994294/3925bab5-3bde-48a5-b0a2-d4f4a6025789)
