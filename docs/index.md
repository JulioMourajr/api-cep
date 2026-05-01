# API CEP

## Visão geral

API simples em FastAPI para consultar CEP usando o serviço ViaCEP.

## Como executar

- Swagger UI: http://localhost:8000/docs
- OpenAPI JSON: http://localhost:8000/openapi.json

## Endpoint principal

`GET /cep/{cep}`

Exemplo:

```bash
curl http://localhost:8000/cep/01310100
```