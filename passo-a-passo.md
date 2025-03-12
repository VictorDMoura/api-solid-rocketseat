Como iniciar um projeto node para fastify

npm init -y
npm i typescript @types/node tsx tsup -D
npm i fastify
Então criar uma pasta src, com app e server.
Adiciona os scripts:

    "start:dev": "tsx src/server.ts",
    "start": "node build/server.js",
    "build": "tsup src --out-dir build"

Roda o npx tsc --init para gerar o tsconfig.json
e muda "target": "es2020"

Logo depois configura variáveis de ambiente:
instala o zod npm i zod e o dotenv
Cria uma pasta chama env e o arquivo .env
Faz a validação nessa pasta
e importa no server.ts

## Configuração do EsLint

npm i eslint @rocketseat/eslint-config -D

Caso não queira usar npm eslint
npx eslint --init

cria o arquivo .eslintrc.json
e configura o tipo de formatação

## Alias de import

vai em tsconfig.json
vamos no baseUrl
E depois usar o paths com @/_: ./src/_

## Fundamentos do PrismaORM

Podemos usar o drive nativo ou usar um ORM
Prisma, TypeORM, Sequelize

https://efficient-sloth-d85.notion.site/Prisma-Configurando-extens-o-no-VSCode-256d8348033b4957955e0598eedd01eb

npm i prisma -D

npx prisma init

modifica e cria modelo no arquivo schema.prisma, criando model que seriam as tabelas

executa npx prisma generate

Agora para começar a trabalhar precisa instalar o @prisma/client

## Fundamentos do docker

## PostgreSQL com Docker

Diego usa a bitname/postgresql
Comando docker

docker run --name api-solid-pg -e POSTGRESQL_USERNAME=docker -e POSTGRESQL_PASSWORD=docker -e POSTGRESQL_DATABASE=apisolid -p 5432:5432 bitnami/postgresql

docker ps - retonna todos os container rodando
docker ps -a - retornar todo os criados

docker start <passando o id ou o nome do container>

docker stop para o container

Posso usar no env, posso usar o DATABSE_URL
Vou executar o npx prisma migrate dev
npx prisma studio - para abrir o studio

## Utilizando o Docker compose

docker down -> deleta todos os container e remove
docker prune também, mas é uma limpeza geral

## Criando Schema do Prisma

OBS para deploy usar npx prims migrate deploy
