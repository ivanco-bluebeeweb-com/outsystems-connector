# OutSystems Connector — Discovery & Vendor API Specification

**Официальный сайт:** https://www.outsystems.com  
**Базовый эндпоинт API:** `https://<outsystems-env>/LifeTimeSDK/rest/v2`  
**Схема авторизации:** LifeTime API Token (Authorization: Bearer <token>)

## Поддерживаемые сущности API
- приложения applications (/applications)
- окружения environments (/environments)
- деплойменты deployments
- модули

## Архитектурные требования
- Использование безопасного клиента с контролем таймаутов, повторных попыток (backoff) и обработкой rate limit.
- Валидация входных данных через Pydantic-схемы без утечки чувствительных полей в логи.
- Тестовая точка проверки подключения: `GET /LifeTimeSDK/rest/v2/environments`.
