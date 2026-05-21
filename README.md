# ansible-network
ansible-network-core/
│
├── inventory/
│   ├── hosts.yaml         <-- Daftar IP perangkat dan grupnya
│   └── group_vars/
│       └── all.yaml       <-- Variabel global (Username, Password, Secret)
│
├── playbooks/
│   ├── run_command.yaml   <-- Kode untuk menjalankan perintah 'show'
│   └── backup_config.yaml <-- Kode untuk mengambil & backup konfigurasi
│
└── ansible.cfg            <-- File konfigurasi utama Ansible

# Cara Menjalankan Ansible Ini:
- Pastikan Anda sudah menginstal Ansible di komputer/server Anda (Ansible paling optimal berjalan di Linux/macOS/WSL Windows):
```
    pip install ansible
```
- Pastikan Anda berada di dalam folder utama (ansible-network/).
- Jalankan perintah berikut untuk mengeksekusi Playbook:
```
    **Untuk menjalankan perintah show interface:**
     ansible-playbook playbooks/run_command.yaml
     **Untuk melakukan backup konfigurasi:**
     ansible-playbook playbooks/backup_config.yaml
```
