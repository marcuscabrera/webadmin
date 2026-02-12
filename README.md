## SophiMail Dashboard Application

1. Centralized interface for managing distributed Email server engines.
2. Role-based, ideal for VARs, ISPs and IT admins.
3. Integrated in all SophiMail business email installations.
4. Supports all PostfixAdmin installations.
5. Developed on Bootstrap and CakePHP.

## Links

- [Installation instructions](https://github.com/sophimail/webadmin/blob/master/INSTALLATION.md)

## Contributor License Agreement

By committing source code, data or other material to the SophiMail project you are assigning all copyright and/ or similar rights to AVERWAY LTD
in consideration of its agreement to license the source, code, data or other material under GPL v.3.0.

## Screenshots
![Screenshot](https://user-images.githubusercontent.com/28845968/27742554-d34ecb3c-5dc1-11e7-9c3c-5e348ab06256.png)
![Screenshot](https://user-images.githubusercontent.com/28845968/27742582-e50c2086-5dc1-11e7-989b-2f03e5d856e8.png)
![Screenshot](https://user-images.githubusercontent.com/28845968/27742593-eeb5feea-5dc1-11e7-8b20-8fa725f001f5.png)

## Docker Setup

Este projeto pode ser executado facilmente utilizando Docker e Docker Compose.

### Pré-requisitos
- [Docker](https://docs.docker.com/get-docker/)
- [Docker Compose](https://docs.docker.com/compose/install/)

### Como Executar

1. **Construir e Iniciar os Containers:**
   No diretório raiz do projeto, execute:
   ```bash
   docker-compose up -d --build
   ```

2. **Instalar Dependências do PHP (Composer):**
   Após os containers estarem rodando, instale as dependências:
   ```bash
   docker exec -it sophimail_app composer install
   ```

3. **Acessar a Aplicação:**
   Abra o seu navegador e acesse: `http://localhost:8080`

### Serviços Incluídos
- **App:** Servidor Apache com PHP 7.3 configurado para rodar o CakePHP.
- **DB:** Banco de dados MySQL 5.7 (inicializado automaticamente com `SQL/mysql.initial.sql`).
- **Elasticsearch:** Motor de busca (versão 6.8).

### Variáveis de Ambiente
As configurações principais estão definidas no arquivo `docker-compose.yml`. Você pode ajustar:
- `DATABASE_URL`: String de conexão com o banco de dados.
- `DEBUG`: Define se o modo de depuração está ativo.
- `SECURITY_SALT`: Salt de segurança para o CakePHP.

