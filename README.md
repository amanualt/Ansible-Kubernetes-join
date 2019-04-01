# Install otomastis dan join di master sama worker.
- copy file `~/.ssh/id_rsa.pub` local(leptop/server) yang akan kita gunakan ke dalam `~/.ssh/authorized_keys ` yang ada di master dan worker.
- ganti `ip_address_master` yang ada di file `hosts` sesuai dengan ip public master dan worker.
- sesuaikan nama user `ansible_user=ubuntu` dengan user yang ada di master atau worker pada file `hosts`.

### Cara menjalankan
- test terlebih dahulu dengan menggunakan perintah
```
ansible all -m ping
```
jika hasilnya `pong` maka berhasil
- jalankan perintah berikut unt7uk menjalankan ansible
```
ansible-playbook -s master.yml  
```
