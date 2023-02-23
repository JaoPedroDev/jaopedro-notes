# HTTP

Hypertext Transfer Protocol(HTTP) é a base da World Wide Web, e é usado para carregar paginas da [[Internet/Internet|Internet]] usando hypertext links. O fluxo de HTTP começa com o computador de alguém que acessa uma página na web mandando um *request* para o servidor, que então manda uma mensagem de resposta.

## HTTP request
Um HTTP request é a maneira que plataformas de comunicação da internet, como navegadores, solicitam as informações aos servidores para carregar as paginas.

Um HTTP requeste geralmente possui:
- Versão do tipo de HTTP
- Uma URL
- Um método HTTP
- HTTP request headers
- HTTP body opcional

## Método HTTP
Indica a ação que o HTTP request espera do servidor. Dois dos métodos mais comuns são "GET" e "POST". "GET" espera informação em retorno(geralmente no formato de um site), enquanto o "POST" significa que o usuário esta enviando informações para o servidor, usuário e senha por exemplo.

## HTTP request headers
Contem informações armazenadas em um formato de key-value, e são incluídos em todos os HTTP request. Informações essas que são de grande importância, como qual o navegador usado pelo cliente e qual informação está sendo solicitada.

![](https://i.imgur.com/iJC28bx.png)

## HTTP response
É oque web clients recebem de um servidor como resposta a um HTTP request.

Um HTTP response geralmente possui:
- Um código de status HTTP
- HTTP response headers
- HTTP body opcional

## HTTP status code
São código de 3 dígitos, geralmente usados para indicar se um HTTP request foi completado ou não. Status codes são quebrados em 5 blocos:
- 1xx Informacional
- 2xx Sucesso
- 3xx Redirecionar
- 4xx Erro do cliente
- 5xx Erro do servidor

Os xx referem diferentes números entre 00 e 99.

## HTTP response headers
Possui informações importantes como o idioma e o formato de data sendo enviado no body.

![](https://i.imgur.com/pFVsmDE.png)

## HTTP response body

"GET" HTTP responses geralmente possuem um body que contem as informações solicitadas. Na maioria das vezes, essas informações são dados HTML que o navegador utiliza para construir o site.

# Relacionado
- [[Internet/Internet]]