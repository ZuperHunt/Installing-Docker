Penulis: [Nur Muhammad Luthfi](https://x.com/luthfi0x)

# Tutorial Install Docker
Bab ini berisi tutorial cara menginstall Docker di VPS dengan Operating Sistem Ubuntu

## Requirement
Syarat menjalankan XXX
- Spek Komputer
  
| Name | Minimum |
| ------------- | ------------- |
| Operating System  | Ubuntu LTS versi terbaru  |
| CPU  | 1 Cores  |
| RAM  | 512 MB  |
| SSD  | 10 GB  |
  
## Dependencies

### Update Package List 
```
sudo apt update
```

### Install Dependencies
```
sudo apt install apt-transport-https ca-certificates curl software-properties-common
```

### Menambahkan Official GPG Key Docker
```
curl -fsSL https://download.docker.com/linux/ubuntu/gpg | sudo gpg --dearmor -o /usr/share/keyrings/docker-archive-keyring.gpg
```

### Menambahkan Repository Docker
```
echo "deb [arch=amd64 signed-by=/usr/share/keyrings/docker-archive-keyring.gpg] https://download.docker.com/linux/ubuntu $(lsb_release -cs) stable" | sudo tee /etc/apt/sources.list.d/docker.list > /dev/null
```

### Update Package List (Again lol)
```
sudo apt update
```

### Install Docker
```
sudo apt install docker-ce docker-ce-cli containerd.io
```

## Menjalankan Docker

### Enable Docker
```
sudo systemctl start docker
sudo systemctl enable docker
```

### Cek Versi Docker
```
sudo docker --version
```

Jika semua berjalan dengan benar, maka akan muncul versi Docker yang sudah kamu install.

## Help
Join komunitas [Discord ZuperHunt](https://t.co/n7TeWVlA48) jika kamu ada pertanyaan.

## Change Logs
* 0.0.1
    * Initial Release
