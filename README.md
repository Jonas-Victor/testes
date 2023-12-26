# Nunes Sportes - Configuração do Banco de Dados CRUD

Este é um guia passo a passo para configurar o banco de dados MySQL usando o MySQL Workbench 8.0 para o projeto Nunes Sportes.

## Pré-requisitos

- MySQL Workbench 8.0 instalado.
- Conhecimento básico sobre SQL.

## Passos

### 1. Abra o MySQL Workbench

Inicie o MySQL Workbench no seu computador.

### 2. Conexão ao Servidor

- Crie uma nova conexão ao seu servidor MySQL.
- Insira as credenciais necessárias (usuário, senha e host) para se conectar.

### 3. Criando o Banco de Dados

Abra uma nova janela de consulta SQL e execute o seguinte comando para criar o banco de dados:

```sql
CREATE DATABASE IF NOT EXISTS crud;

```
### 4. Selecionando o Banco de Dados

Após criar o banco de dados, selecione-o para realizar operações nele:

```sql
USE crud;
```

```sql
```

### 5. Criando a Tabela 'produtos'
Agora, vamos criar a tabela 'produtos' com os campos especificados:
```sql
CREATE TABLE IF NOT EXISTS produtos (
    id INT AUTO_INCREMENT PRIMARY KEY,
    nome VARCHAR(100),
    productDescription VARCHAR(100),
    productCode VARCHAR(10),
    priceProduct VARCHAR(100)
);
```

### 6. Verificando a Criação da Tabela
Você pode verificar se a tabela foi criada com sucesso usando:

```sql
DESCRIBE produtos;
```
### 7. Inserindo Dados na Tabela (Opcional)
Se desejar, insira alguns dados de exemplo na tabela:

```sql
INSERT INTO produtos (nome, productDescription, productCode, priceProduct)
VALUES
    ('Nome do Produto 1', 'Descrição do Produto 1', 'CODE001', 19.99),
    ('Nome do Produto 2', 'Descrição do Produto 2', 'CODE002', 29.99);
```
## 8. Configurando a Autenticação para o MySQL Workbench (Opcional)

Se você estiver enfrentando problemas de autenticação ao conectar-se ao MySQL Workbench, especialmente após atualizações ou em cenários específicos, pode ser necessário ajustar as configurações de autenticação do usuário 'root'.

### Passos:

1. **Abra o MySQL Workbench**

Inicie o MySQL Workbench no seu computador.

2. **Conexão ao Servidor**

- Conecte-se ao servidor MySQL usando o MySQL Workbench.
- Caso ocorram erros de autenticação ou falhas ao utilizar a senha para o usuário 'root', talvez seja necessário configurar a autenticação para esse usuário.

3. **Abrindo uma Janela de Consulta SQL**

Crie uma nova consulta SQL na interface do MySQL Workbench.

4. **Alterando a Autenticação do Usuário 'root'**

Cole e execute o seguinte comando SQL na consulta:

   ```sql
   ALTER USER 'root'@'localhost' IDENTIFIED WITH mysql_native_password BY 'nunes123';
   ```
Substitua 'nunes123' pela nova senha desejada para o usuário 'root'.

### 9. Finalizando
Você configurou o banco de dados CRUD com a tabela 'produtos'.


