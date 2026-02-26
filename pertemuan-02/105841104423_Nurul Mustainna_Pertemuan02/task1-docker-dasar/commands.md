# 🐳 Docker Commands - Pertemuan 02

## =========================
## TASK 1 - Docker Basic
## =========================

# Pull image nginx
docker pull nginx:alpine

# Menjalankan container
docker run -d --name web-praktikum -p 8080:80 nginx:alpine

# Melihat container yang berjalan
docker ps

# Melihat semua container
docker ps -a

# Melihat logs container
docker logs web-praktikum

# Masuk ke dalam container
docker exec -it web-praktikum sh

# Stop container
docker stop web-praktikum

# Hapus container
docker rm web-praktikum


## =========================
## TASK 2 - Docker Image
## =========================

# Build Docker image
docker build -t praktikum-docker:v1 .

# Melihat daftar image
docker images

# Menjalankan container dari image buatan
docker run -d -p 8080:80 --name praktikum-web praktikum-docker:v1

# Stop container
docker stop praktikum-web

# Hapus container
docker rm praktikum-web


## =========================
## TASK 3 - Docker Compose
## =========================

# Menjalankan semua services
docker compose up -d

# Melihat status services
docker compose ps

# Melihat logs
docker compose logs -f

# Menghentikan semua services
docker compose down

# Menghentikan dan hapus volumes
docker compose down -v