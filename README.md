# go-docker

# 1. Развертывание nginx-прокси с Let's Encrypt
    docker-compose -f nginx-proxy-compose.yaml up -d

# 2. Создание и запуск файла Docker Compose
    docker-compose -f go-app-compose.yaml up -d