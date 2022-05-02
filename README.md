# Slim + ReactJS Demo Auction

## Installation to dev
- run command `make init`
- see working elements:
  - Frontend http://localhost:8080/
  - API http://localhost:8081/
  - MailHog http://localhost:8082/
- also, there are **Jenkins** (from another project) - http://localhost:8000/
- also, there are **Docker Registry** (from another project) - http://localhost:5000/v2/

## Installation to production
- install the Jenkins to production, for more info go to demo-auction-jenkins project.
- install the Docker Registry to production, for more info go to demo-auction-registry project.
- go to provision directory and prepare target servers
  - cd pro*
  - make site
  - make authorize
  - make generate-deploy-key
  - make authorize-deploy
  - docker-login
- return to main directory and deploy project to target servers by example command:  
  - `make deploy`


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
