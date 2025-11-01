# Validador de CPF - Azure Function

Azure Function desenvolvida em .NET 8 para validação de CPF.

## Funcionalidades

- Validação de CPF via HTTP POST
- Verifica dígitos verificadores
- Remove caracteres especiais automaticamente
- Retorna mensagem amigável

## Como usar

### Requisição

```http
POST /api/fnvalidacpf
Content-Type: application/json

{
    "cpf": "123.456.789-09"
}
```

### Respostas

Sucesso:
```json
{
    "message": "CPF 12345678909 é válido."
}
```

CPF Inválido:
```json
{
    "message": "CPF inválido."
}
```

## Desenvolvimento Local

1. Pré-requisitos:
   - .NET 8 SDK
   - Azure Functions Core Tools
   - Visual Studio Code ou Visual Studio 2022

2. Clone o repositório:
   ```bash
   git clone https://github.com/celiovetrano/validador-cpf-azure-function.git
   cd validador-cpf-azure-function
   ```

3. Execute localmente:
   ```bash
   func start
   ```

## Deploy no Azure

1. Publicar usando Azure Functions Core Tools:
   ```bash
   func azure functionapp publish cvetranofunctionapp
   ```

2. Ou pelo Visual Studio:
   - Clique direito no projeto
   - Selecione "Publish..."
   - Escolha "Azure Function App"
   - Selecione sua subscription e Function App

## Tecnologias

- .NET 8
- Azure Functions
- C#