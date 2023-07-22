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
- Edit dan buat script untuk membuat 3 VM appserver, gateway, monitoring dengan template sebagai berikut!!!
- Bisa diperbanyak sesuai kebutuhan
- ```
  terraform {
    required_providers {
      idcloudhost = {
        source = "bapung/idcloudhost"
        version = "0.1.3"
      }
    }
  }
  
  provider "idcloudhost" {
    auth_token = 
  }
  
  resource "idcloudhost_vm" "fajarapp" {
    name = "fajar-app"
    os_name = "ubuntu"
    os_version = "20.04"
    vcpu = "2"
    memory = "1024"
    disks = "20"
    username = "app"
    initial_password = 
    public_key = 
    billing_account_id = 
  }
  
  resource "idcloudhost_floating_ip" "ip-fajar" {
    name = "appserverIP"
    billing_account_id = "
    assigned_to = idcloudhost_vm.fajarapp.id
  }
  ```
- jalakan pada setiap folder ```terraform init```
- ```terraform plan && terraform apply```
- ![Screenshot from 2023-07-19 11-25-16](https://github.com/galantixa/devops17-dumbways-galantixa/assets/92994294/d8375db2-fb66-4347-92ad-afad29fe5af9)
- ![Screenshot from 2023-07-19 12-21-56](https://github.com/galantixa/devops17-dumbways-galantixa/assets/92994294/3925bab5-3bde-48a5-b0a2-d4f4a6025789)
- Untuk menghapus VM bisa dengen menjalankan ```terraform destroy```
### Untuk installasi yang lebih lengkat bisa di cek di dokumentasi resmi [TERRAFORM](https://developer.hashicorp.com/terraform/tutorials/aws-get-started/install-cli)
