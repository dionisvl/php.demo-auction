# Cucumber
Фреймворк для сквозного (E2E) BDD тестирования

# Puppeteer 
https://pptr.dev/
либа для работы с API браузера напрямую

## Внятное объяснение разных типов тестирования
- https://www.atlassian.com/continuous-delivery/software-testing/types-of-software-testing
- тоже, только на русском: https://www.atlassian.com/ru/continuous-delivery/software-testing/types-of-software-testing


## Запуск e2e тестов
**Смоук**:  
- `make test-smoke`
- or `docker-compose run --rm cucumber-node-cli yarn smoke`
- or внутри кукумбер контейнера: `cucumber-js --tags @smoke --fail-fast --parallel 2`

**Основные**:
- `make cucumber-e2e`
- or `docker-compose run --rm cucumber-node-cli yarn e2e`
- or внутри кукумбер контейнера: `cucumber-js --parallel 4`