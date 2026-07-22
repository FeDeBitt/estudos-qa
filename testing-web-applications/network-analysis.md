# Análise de Requisições de Rede (Network Requests)

Este documento demonstra a análise e o monitoramento de requisições HTTP utilizando as ferramentas de desenvolvedor do navegador (DevTools - Network Tab). O foco é identificar os diferentes comportamentos da aplicação com base nos códigos de status (Status Codes).

## Tabela de Requisições Analisadas

| Request Name | Method | Request URL | Status Code | Categoria |
| :--- | :---: | :--- | :--- | :--- |
| `index.json` | GET | `https://conduit.mate.academy/_next/data/.../index.json` | **200 OK** | Sucesso |
| `admin.json` | GET | `https://conduit.mate.academy/_next/data/.../admin.json` | **304 Not Modified** | Sucesso (Cache) |
| `500` | GET | `https://mock.httpstatus.io/500` | **500 Internal Server Error** | Erro de Servidor (Back-end) |
| `dummy` | GET | `https://example.com/dummy?data=someData` | **404 Not Found** | Erro de Cliente (Front-end) |

## Análise Prática

*   **200 OK:** A comunicação com o servidor ocorreu sem problemas e os dados foram retornados como esperado.
*   **304 Not Modified:** O recurso solicitado não sofreu alterações desde o último acesso, instruindo o navegador a utilizar a versão em cache (otimização de performance).
*   **404 Not Found:** O cliente tentou acessar uma rota ou arquivo inexistente no servidor.
*   **500 Internal Server Error:** O servidor falhou ao processar a requisição, indicando um "crash" no back-end que exige investigação nos logs da aplicação.