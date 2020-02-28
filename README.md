# go-docker

# Остановить все Docker контейнеры.
    docker stop $(docker ps -a -q)
# Удалить все Docker контейнеры
    docker rm $(docker ps -a -q)
# Удалить все Docker images
    docker rmi $(docker images -q)
    
# 1. Развертывание nginx-прокси с Let's Encrypt
    docker-compose -f nginx-proxy-compose.yaml up -d

# 2. Создание и запуск файла Docker Compose
    docker-compose -f go-app-compose.yaml up -d
# 3. Перезапуск контейнера go-app
    docker-compose -f go-app-compose.yaml up -d --no-deps --build

# Источник
https://quasar.site/tutorials/173/kak-razvernut-veb-prilozhenie-go-s-pomoshchyu-docker-i-nginx-v-ubuntu-1804
