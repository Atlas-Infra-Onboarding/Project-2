# Project-2

Hello World em NGINX

Para esse projeto espera-se que o candidato seja capaz de realizar a instalação do servidor web NGINX em uma máquina de sua escolha.
Essa máquina deve obrigatoriamente responder às seguintes requisições:
```
Rota: http://project-2.com/
Tipo: GET
Resposta: "Hello World!"
Comando: curl -w "%{http_code}" -s -X GET 'http://project-2.com/'
```

```
Rota: http://project-2.com/Hello
Tipo: GET
Resposta: "World!"
Comando: curl -w "%{http_code}" -s -X GET 'http://project-2.com/Hello'
```

É avaliado nesse projeto:
- Limpeza e organização do arquivo de configuração
- Adesão aos padrões de configuração da ferramenta
- Funcionalidade

Como pontos bônus temos:

Responder as rotas:

```
Rota: http://project-2.com/
Tipo: HEAD
Resposta: Header 'Access-Control-Allow-Origin' presente e com valor '\*'
Comando: curl -I 'http://project-2.com/'
```

```
Rota: http://project-2.com/static-files
Tipo: HEAD
Resposta: Header 'Access-Control-Allow-Origin' presente e com valor 'http://project-2.com'
Comando: curl -I 'http://project-2.com/static-files'
```

```
Rota: http://project-2.com/whoami
Tipo: HEAD
Resposta: Header 'Project-Name' presente e com valor 'project-2'
Comando: curl -I 'http://project-2.com/whoami'
```

```
Rota: http://project-2.com/admin
Tipo: GET
Resposta: Status Code 401 pedindo autenticação básica
Comando: curl -w "%{http_code}" -s -X GET 'http://project-2.com/admin'
```
