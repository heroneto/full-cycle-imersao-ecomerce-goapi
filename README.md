# API Ecommerce

Este projeto é uma API desenvolvida na semana Imersão 17 da escola Full Cycle.


## Tecnologias

A API foi desenvolvida em Go, e durante a aula foi criado um CRUD e integrado com banco de dados Mysql.

O banco de dados foi criado com docker-compose


## Funcionalidades

- [x] Listar categorias
- [x] Criar categoria
- [x] Ler categoria
- [x] Criar Produto
- [x] Listar produtos
- [x] Listar produtos de uma categoria
- [x] Listar produto pelo ID


## Como executar o projeto

Para executar é necessário ter o docker instalado na sua máquina, para instalar acesse o site Docker e baixe o instalador para o seu SO
[Site Docker](https://www.docker.com)

Com o docker instalado, suba o container mysql executando o comando abaixo na raiz do projeto.

```bash
docker-compose up -d 
```

Caso ocorra algum erro verifique os Logs

```bash
docker-compose logs mysql
```

Entre no container e crie as tabelas

```bash
docker-compose exec mysql bash
mysql -u root -p imersao17
```

Caso peça senha insira a senha `root`

Copie oi conteúdo do arquivo `db.sql` na raiz deste projeto e cole no terminal do mysql que foi aberto.

Deve retornar uma mensagem como essa `Query OK, 0 rows affected (0.04 sec)`

Feche o terminal do mysql e execute a aplicação em go.

```bash
go run cmd/catalog/main.go
```

## Como testar via http.test

Para testar usamos o plugin `Rest Client` no VSCODE [Link](humao.rest-client) 

Após instalar abra o arquivo `http.test` e com a aplicação em execução envie as requests.

## Link

[Link para imersão 17 Full Cycle](https://imersao.fullcycle.com.br/evento/)