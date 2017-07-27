# RESPONSI PRAKTIK TCC LANJUT
Implementasi Docker

## Dockerfile
- Membuat image aplikasi dengan Dockerfile
```
FROM httpd:latest
COPY /public-html/ /usr/local/apache2/htdocs/
```
- Mulai membuat image menggunakan perintah `#docker-build -t retccl`
- Menjalankan image docker dengan perintah
`docker run --name some-nginx -d -p 8088:80 some-content-nginx`
- Hasil
<img src="img/1.png">

## Docker Compose
```
restccl:
    build: .
    ports:
        - "8888:80"
    volumes:
        - /var/www/html/

```
- Membangun dengan perintah `#docker-compose build`
- Menjalanankan dengan perintah `#docker-compose up`
- Hasil
<img src="img/2.png">
