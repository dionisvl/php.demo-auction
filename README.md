# Slim + ReactJS Demo Auction

## Installation to dev
- run command `make init`
- see working elements:
  - Frontend: http://localhost/
  - API: http://api.localhost/
  - MailHog: http://mailer.localhost/
  - S3 MINIO: http://backup-storage.localhost/
- also, there are **Jenkins** (from another project) - http://localhost:8000/
- also, there are **Docker Registry** (from another project) - http://localhost:5000/v2/

## Installation to production
### See actual instruction in "Cluster" project.
### See next sites:
- http://api.demo-auction.phpqa.ru/
- http://demo-auction.phpqa.ru/
- http://registry.demo-auction.phpqa.ru/
- http://cache-registry.demo-auction.phpqa.ru/
- http://jenkins.demo-auction.phpqa.ru/


## Another remarks
#### Enter directly in root user in docker container
`docker exec -itu 0 container_id bash`

### Docker Swarm
- Добавление ноды менеджера или воркера:
  - `docker swarm join-token`
  - полученную команду с токеном надо выполнить на той машине которую подключаем.
- Версии Docker Engine должны совпадать на всех системах
- Проверить что все ок:
  - `ssh deploy@130.255.170.54 -p 222`
  - `docker node ls`

- Проверить что деплой Docker Swarm прошел успешно:
  - `docker service ls`
  - `docker service ps auction_gateway`
