# Instruções para Configurar o Projeto Docker

Siga os passos abaixo para clonar o repositório, entrar no diretório e iniciar o Docker:

### 1. **Clonar o Repositório:**
Abra o terminal e execute o seguinte comando para clonar o repositório:
```bash
git clone https://github.com/jessicaosilva/dockerPS.git
```

### 2. **Entrar no Repositório:**
No terminal, execute o seguinte comando para mudar de pasta e entrar no projeto clonado:
```bash
cd dockerPS
```

### 3. **Build:**
Execute o seguinte comando para construir os serviços especificados no arquivo `docker-compose.yml`:
```bash
docker-compose build
```

### 4. **Iniciar o Docker Compose:**
Execute o seguinte comando para iniciar o Docker Compose e levantar os serviços em segundo plano:
```bash
docker-compose up -d
```

### 5. **Avançar uma Pasta:**
Execute o seguinte comando para entrar na pasta front:
```bash
cd front
```

### 6. **Clonar Projeto Laravel:**
Execute o seguinte comando para clonar o repositório:
```bash
git clone https://github.com/jessicaosilva/ps piloto
```

### 7. **Abrir a Pasta Piloto:**
Abra a pasta piloto no seu editor de texto favorito.

### 8. **Configuração do .env:**
Crie um arquivo `.env` na raiz do projeto e adicione as seguintes variáveis de ambiente para configurar a conexão com o banco de dados:
```plaintext
DB_CONNECTION=mysql
DB_HOST=mysql
DB_PORT=3306
DB_DATABASE=app
DB_USERNAME=user
DB_PASSWORD=password
```

### 9. **Instalação de Dependências:**
Dentro do container, execute o Composer para instalar as dependências do projeto:
```bash
docker-compose exec dockerps-php-1 composer install
```

### 10. **Gerar Key:**
Gere a chave da aplicação executando:
```bash
docker-compose exec dockerps-php-1 php artisan key:generate
```

### 11. **Executar Migrations:**
Para criar as tabelas no banco de dados, execute:
```bash
docker-compose exec dockerps-php-1 php artisan migrate
```

## Pronto!

Seu projeto Docker está configurado e pronto para ser utilizado no seu localhost, na porta 80 (padrão).