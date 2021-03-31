# MULTIPLE YAML UNTUK TESTING KAFKA

Ada beberapa yaml yang bisa digunakan untuk melakukan testing kafka, untuk contoh zookeeper
dan kafka-rest dalam repo ini hanya menggunakan 1 buah saja. Silahkan di edit jika ingin
menggunakan lebih dari satu zookeeper dan kafka-rest

Untuk dapat menggunakan docker-compose yaml ini kita harus tahu terlebih dahulu IP private di pc/notebook/vm. IP ini akan digunakan untuk mengakses zookeeper/kafka.

Jika sudah tahu ipnya, masukan ke dalam file yaml yang ingin digunakan.

Cara menggunakan docker-compose :

## 1. Single Kafka

### Menjalankan pertama kali atau ada update pada isi file docker-compose

```
docker-compose -f 01-single-zoo-kafka-rest.yaml up -d
```

### Menghentikan docker-compose

```
docker-compose -f 01-single-zoo-kafka-rest.yaml stop
```

### Menjalankan kembali docker-compose yang sudah dihentikan

```
docker-compose -f 01-single-zoo-kafka-rest.yaml start
```

### Menghapus docker-compose
```
docker-compose -f 01-single-zoo-kafka-rest.yaml down
docker volume prune
```

Docker volume prune merupakan perintah untuk menghapus volume yang sudah tidak digunakan.

## 2. Multiple Kafka

### Menjalankan pertama kali atau ada update pada isi file docker-compose

```
docker-compose -f 02-single-zoo-rest-multiple-kafka.yaml up -d
```

### Menghentikan docker-compose

```
docker-compose -f 02-single-zoo-rest-multiple-kafka.yaml stop
```

### Menjalankan kembali docker-compose yang sudah dihentikan

```
docker-compose -f 02-single-zoo-rest-multiple-kafka.yaml start 
```

### Menghapus docker-compose
```
docker-compose -f 02-single-zoo-rest-multiple-kafka.yaml down
docker volume prune
```

Docker volume prune merupakan perintah untuk menghapus volume yang sudah tidak digunakan.
