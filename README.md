# Configuração

Criação de um projeto empty: npm init -y
Criar pasta src/index.ts e inserir no package.json o script de start e build
Configurar tsconfig em e selecionar a versão do seu nodejs: https://github.com/tsconfig/bases/tree/main/bases

Instalação de dependências:
1 - drizzle-orm
2 - express
3 - pg (postgres)
4 - npm install --save rimraf (inserir no script de buil para remover a pasta dist antes de buildar)
5 - npm install --save-dev pino pino-http (biblioteca de logger)

Dependências para desenvolvimento:
 - [npm install --save-dev typescript @types/express @types/node @types/pg drizzle-kit tsup tsx @faker-js/faker]
 - tsup o node não reconhece typescript, por isso o tsup serve para converter typescript em javascript.
 - faker-js biblioteca de mock de api
 - npm install --save body-parser compression cors helmet essas bibliotecas é necessário para o express conseguir ler o body das request quando são enviados através do arquivo api.http
 - instalando seus types no modo dev: npm install --save @types/body-parser @types/compression @types/cors @types/helmet

1. [Descrição](#descrição)

### Descrição

Aplicação Node.js utilizando uma biblioteca mock chamada faker-js.
A aplicação utiliza typescript, express, postgres, logger, errorHandler e Grafana k6.

O arquivo api.http contém as requisições do sistema para teste

Utilizamos o docker-compose.yml para criar o banco postgres e outras configurações.

Ao criar uma tabela ou inserir nova coluna :
1 - npm run db:generate
2 - npm run db:migrate
3 - npm run db:studio (para abrir a interface do drizzle e acessar as tabelas)
4 - npm run db:seed inserir dados nas tabelas


