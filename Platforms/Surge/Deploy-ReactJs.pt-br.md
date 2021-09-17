#Publicar projeto em ReactJs em surge.sh

*Você precisar ter instalado em sua máquina:*
- Node.Js (Recomendado última versão LTS);
- Cli do próprio surge (Pode ser instalado através do npm)
`npm install --global surge`

####Com os requisitos instalados, você precisa fazer o `build` da sua aplicação, e em seguida o `deploy`.

- Build do projeto:
```
Yarn: yarn build
     Ou
Npm: npm build
```

- Partindo do diretório do build, digite os seguintes comandos:
    - `surge`
    - `{seu_email}`
    - `{sua_senha}` 
	- `{path from project (folder of publish)}`
    - `{seu_dominio (without http/https)}`