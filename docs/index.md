# API CEP

## Visao geral

API em FastAPI para consultar CEP usando o servico ViaCEP.

## Como executar

- Swagger UI: http://localhost:8000/docs
- OpenAPI JSON: http://localhost:8000/openapi.json

## Endpoint

`GET /cep/{cep}`

Retorna informacoes do CEP informado no caminho. Use 8 digitos, sem hifen.

### Exemplo de requisicao

```bash
curl http://localhost:8000/cep/01310100
```

### Exemplo de resposta

```json
{
	"cep": "01310-100",
	"logradouro": "Avenida Paulista",
	"complemento": "de 1499 a 3047 - lado impar",
	"bairro": "Bela Vista",
	"localidade": "Sao Paulo",
	"uf": "SP",
	"ibge": "3550308",
	"gia": "1004",
	"ddd": "11",
	"siafi": "7107"
}
```

## Erros comuns

- 404: CEP nao encontrado no ViaCEP.
- 422: CEP invalido (formato incorreto).

## Observacoes

- A disponibilidade e os dados dependem do servico ViaCEP.