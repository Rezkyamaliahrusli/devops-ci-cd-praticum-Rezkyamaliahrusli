# 1. Pull image nginx
docker pull nginx:alpine

# 2. Jalankan container dengan nama
docker run -d --name web-praktikum -p 8080:80 nginx:alpine

# 3. Akses di browser: http://localhost:8080

# 4. Lihat logs container
docker logs web-praktikum

# 5. Masuk ke dalam container
docker exec -it web-praktikum sh

# Di dalam container, coba:
ls -la /usr/share/nginx/html
cat /etc/nginx/nginx.conf
exit

# 6. Stop dan hapus container
docker stop web-praktikum
docker rm web-praktikum