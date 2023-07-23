# Create user and login with ssh
### Create hosts inventory
  - Dalam folder ansible buat file dengan nama```inventory/hosts```
  - 
  - Isi file dengan daftar hosts dan variable ansible_user diisi dengan username vm kita yang dibuat pada terraform
  - Cek koneksi dengan jalankan ```ansible all -m ping``` pastikan tidak ada error
  - Buat script file untuk create user untuk login vm
  - ```
    ---
    - name: Create new user
      hosts: # hosts
      become: # grant superuser acces
    
      # Memasukkan variabel untuk username dan password
      # Syntax name harus diawali - ( - name: )
      vars:
        new_username: 
        new_user_password: 
    
      # Tugas yang akan dijalankan oleh playbook Ansible
      tasks:
        - name: Create new user
          user:
            name: "{{ new_username }}"
            password: "{{ new_user_password | password_hash('sha512') }}"
            shell: /bin/bash # jenis shell yang akan digunakan
            createhome: yes # buat home dir
            state: present # memastikan akan membuat user baru jika belum ada
            groups: sudo 
    
        - name: Copy ssh public
          authorized_key: # module untuk menambahkan kunci publik
            user: "{{ new_username }}" # nama user yang akandi daftarkan
            state: present 
            key: "{{ lookup('file', '~/.ssh/id_rsa.pub') }}" # mengkopi file dari vm lokal
    
        - name: Grant privilages
          copy: # dalam stage ini digunakan untuk membuat file dan mendapatkan perijinan user
            content: "{{ new_username }} ALL=(ALL) ALL"
            dest: /etc/sudoers.d/{{ new_username }}
            mode: 0440 # izin untuk membaca (user, group dan 0 untuk tidak ada izin apapun pada pengguna lain)
            validate: /usr/sbin/visudo -cf %s # untuk memastikan data sesuai
    
        - name: Login into VM
          become: yes
          user: 
            name: "{{ new_username }}"
            groups: sudo
            append: yes
      ```
    - Untuk menjalankan scrip bisa dengan menjalanklan ```ansible-playbook nama-file.yml``` jika berada didalam folder ```ansible-playbook folder/nama-file.yml -i inventory-hosts```
    - Tes login vm dengan user yang baru kita buat
