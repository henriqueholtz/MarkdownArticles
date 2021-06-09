**Olá** dev, tudo bem? :smiley: 

Hoje explicarei de forma simples e direta os conceitos de uma ***API REST*** e como ela pode ser denominada como uma ***API RESTFUL***. 

Representational State Transfer (REST)
Uma API pode ser denominada como RESTFUL quando cumpre todo o conjunto de 05 princípios de arquitetura :

***Stateless (Sem estado):*** Esse princípio diz que cada requisição feita a API deve ser independente, ou seja, ter todos os dados necessários para autenticação e autorização, por exemplo, quando aplicável.

***Client-Server (Separação de Cliente-Servidor):*** Esse princípio diz que devemos separar a interface do usuário (normalmente gráfica) do armazenamento de dados.

***Layered System (Camadas de sistema):*** A indicação é de que a arquitetura da API seja construída com camadas independentes, de forma que cada camada não pode ver além da camada adjacente, bem como as mudanças de uma camada não afetem as demais. É recomentado que entre o cliente-servidor tenha-se uma balanceador de carga (Load Balancer). Uma das vantagens de ter uma API dividida em camadas é que a arquitetura se torna menos completa e fica mais propensa a modificações.

***Cache (Armazenamento em cache):*** O cache é um armazenamento em memória do lado do servidor que ajuda muito quando o assunto é performance e eficiência, visto que uma informação "cacheada" é retornada de forma muito mais rápida. A indicação é que seja possível fazer uma consulta sem cache a qualquer momento através de um recurso chamado HTTP Header.

***Uniform Interface (Interface Uniforme):*** Resume-se em componentes uniformes entre cliente-servidor. Subdividida em 4 partes:
```
* Identificação dos Recursos;
* Representação dos recursos;
* Mensagens auto descritivas;
* Hypermedia (HATEOAS);
```
&nbsp; 
&nbsp;
##Algumas boas práticas são:
- Criar rotas no plural, por exemplo:
`https://meusite.com.br/produtos` 
&nbsp;

- Utilizar letras minúsculas;
- Manter coerência nos métodos HTTP, exemplos mais comuns:

| Método | Descrição |
| ------ | ------ |
|`GET`    | Consultas em geral|
|`POST`   | Normalmente utilizado para inserção de registros|
|`PUT`    | Edição de registros|
|`DELETE` | Deletar registros|
&nbsp;
- Manter coerência com os códigos de retorno das chamadas (StatusCode), alguns exemplos:

| Código                    | Descrição                  |
| ------                    | ------                     |
| :white_check_mark: 200    | Ok                         |
| :white_check_mark: 201    | Criado                     |
| :warning: 401             | Não Autorizado             |
| :warning: 403             | Acesso Proibido            |
| :x: 500                   | Erro interno do Servidor   |

&nbsp;
Henrique Holtz, desenvolvedor de software. :v:

- [Meu Github](https://github.com/henriqueholtz)
- [Meu LinkedIn](https://www.linkedin.com/in/henrique-holtz/)
- [Markdown do Artigo](https://github.com/henriqueholtz/MarkdownArticles)