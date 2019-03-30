## INSTALL DOCKER

### Install docker dari ubuntu repository

```
$ sudo apt install docker.io
```

Perintah linux berikut ini akan memulai Docker dan memastikan bahwa dimulai setelah reboot:

```
$ sudo systemctl start docker
$ sudo systemctl mengaktifkan buruh pelabuhan
```

Selesai instalasi cek docker dengan mengetik :

```
$ docker --version
```

### Install docker dari Official Docker Repository

Install the Dependencies

```
$ sudo apt update
$ sudo apt install apt-transport-https ca-certificates curl software-properties-common
```

Tambah Docker Repository

```
$ curl -fsSL https://download.docker.com/linux/ubuntu/gpg | sudo apt-key add -
$ sudo apt update
```

Install Docker CE

```
$ sudo apt install docker-ce
```

Selesai instalasi cek docker dengan mengetik :

```
$ docker --version
```


