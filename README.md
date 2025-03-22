# Fake Shop

Fake Shop se trata de um e-commercio. Esta aplicação foi feita estruturada de tal forma que facilite o processo de manutenção e entrega, para tanto foi automatizado diversos processos.

Dentre eles possui automação para rodar a aplicação em container, rodar com containers de forma orquestrada com kubernetes, e um pipeline ci/cd pelo github actions.

Para rodar o container, executar os comandos:
1. docker build -t fake-shop .\src\
2. docker run fake-shop

Para rodar os containers de forma orquestrada, executar os comandos:
* Fazer push da imagem no repositório docker hub
1. kubectl apply -f .\k8s\deployment.yaml

Para rodar o pipeline ci/cd:
1. Fazer push no repositório, o pipeline ci/cd será chamado automaticamente
2. Rodar o workflow pelo próprio portal github actions

## Variável de Ambiente
DB_HOST	=> Host do banco de dados PostgreSQL.

DB_USER => Nome do usuário do banco de dados PostgreSQL.

DB_PASSWORD	=> Senha do usuário do banco de dados PostgreSQL.

DB_NAME	=>	Nome do banco de dados PostgreSQL.

DB_PORT	=>	Porta de conexão com o banco de dados PostgreSQL.
