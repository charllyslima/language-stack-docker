# Ambiente Docker para Desenvolvimento

![image](https://github.com/charllyslima/language-stack-docker/assets/96506145/e244f60a-4dfb-467f-a793-147a5cefabf7)


Este repositório contém um exemplo de configuração de um ambiente Docker para desenvolvimento que inclui serviços PHP, Python, Node.js, Jupyter Notebook, PHPMyAdmin e MySQL. Você pode usar este ambiente para desenvolver aplicativos web e realizar análises de dados em um ambiente Dockerizado.

## Requisitos

Antes de começar, certifique-se de ter o Docker e o Docker Compose instalados em seu sistema. Você pode encontrar instruções de instalação em [Docker](https://docs.docker.com/get-docker/) e [Docker Compose](https://docs.docker.com/compose/install/).

## Configuração

1. Clone este repositório em seu sistema local:

   ```bash
   git clone https://github.com/charllyslima/language-stack-docker.git
   ```

2. Crie um arquivo `.env` na raiz do projeto para configurar as variáveis de ambiente necessárias. Um exemplo de arquivo `.env` está incluído neste repositório:

   ```plaintext
   # MYSQL
   MYSQL_USER=user
   MYSQL_PASSWORD=12345
   MYSQL_ROOT_PASSWORD=root
   # PHPMYADMIN
   PMA_HOST=mysql
   PMA_USER=user
   PMA_PASSWORD=password
   ```

   Personalize essas variáveis de acordo com suas necessidades.

3. Execute o ambiente Docker com o seguinte comando:

   ```bash
   docker-compose up -d
   ```

   Isso iniciará todos os serviços definidos no arquivo `docker-compose.yml`.

4. Acesse os serviços:

   - PHP: [http://localhost](http://localhost)
   - Python: Acesse o contêiner Python diretamente.
   - Node.js: Acesse o contêiner Node.js diretamente.
   - Jupyter Notebook: [http://localhost:8888](http://localhost:8888)
   - PHPMyAdmin: [http://localhost:8080](http://localhost:8080)
   - MySQL: Você pode se conectar ao MySQL na porta `5959` usando as credenciais definidas no arquivo `.env`.

## Uso

Você pode começar a desenvolver seus aplicativos PHP, Python e Node.js diretamente nos contêineres correspondentes. O Jupyter Notebook está disponível para análises de dados e programação em Python. O PHPMyAdmin permite gerenciar seu banco de dados MySQL.

## Observações

- Mantenha as informações de credenciais definidas no arquivo `.env` em segredo, pois elas contêm informações sensíveis.
- O ambiente Docker foi configurado para fins de desenvolvimento. Certifique-se de ajustar as configurações de segurança e permissões em um ambiente de produção.

## Contribuindo

Se você encontrar problemas ou desejar contribuir para este ambiente Docker, sinta-se à vontade para abrir um problema ou enviar uma solicitação de pull.

## Licença

Este projeto é licenciado sob a Licença MIT. Consulte o arquivo LICENSE para obter detalhes.
