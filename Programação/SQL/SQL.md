# SQL
**Structured Query Language**, é a linguagem padrão para manipulação de dados de banco de dados relacional.

Ela possui subconjuntos, cada um contendo comandos usados para fazer uma determinada categoria de ações:

## DML
**Data Manipulation Language**, responsável por realizar inclusões, consultas, alterações e exclusões de dados presentes em registros.

|   Função   | Comando | Descrição                                 | Exemplo                                                               |
|:----------:|:-------:|:----------------------------------------- | --------------------------------------------------------------------- |
| Inclusões  | INSERT  | Insere um registro a uma tabela existente | `INSERT INTO Pessoa (id, nome, sexo) VALUE;`                          |
| Alterações | UPDATE  | Alterar valores de linhas já existentes   | `UPDATE Pessoa SET data_nascimento = '11/09/1985' WHERE id_pessoa = 7;` |
| Exclusões  | DELETE  | Remover linhas existentes de tabelas      | `DELETE FROM pessoa WHERE id_pessoa = 7;`                               |

## DDL
**Data Definition Language**, permite definir novas tabelas e elementos associados.

| Função   | Comando | Descrição                                 | Exemplo                                      |
| -------- | ------- | ----------------------------------------- | -------------------------------------------- |
| Criações | CREATE  | Cria um objeto dentro da base de dados    | `CREATE TABLE Clientes`                      |
| Apagar   | DROP    | Apaga um objeto de um banco de dados      | `DROP TABLE Clients`                         |
| Alterar  | ALTER   | Adicionar elementos a um objeto existente | `ALTER TABLE Clients ADD Telefone CHAR (9);` |         |         |                                           |                                              |

## DCL
**Data Control Language**, permite controlar as autorizações de modificação dos dados do banco de dados.

| Função    | Comando | Descrição           | Exemplo                                 |
| --------- | ------- | ------------------- | --------------------------------------- |
| Autorizar | GRANT   | Autoriza usuário    | `GRANT SELECT ON Clients TO usuario01;` |
| Revogar   | REVOKE  | Desautoriza usuário | `REVOKE SELECT ON Clients TO usuario01;`                                        |

## DTL
**Data Transaction Language**, controla as transações, permitindo oficializar(COMMIT) ou desfazer(ROLLBACK) as transações realizadas de pois de iniciar uma transação(BEGIN WORK).

| Função      | Comando    | Descrição                                           |
| ----------- | ---------- | --------------------------------------------------- |
| Iniciar     | BEGIN WORK | Inicia uma transação que pode ser completada ou não |
| Oficializar | COMMIT     | Torna as transações oficiais                        |
| Desfazer    | ROLLBACK   | Desfaz as transações feitas                         |

## DQL
**Data Query Language**, utilizada para filtrar dados especifico do banco de dados.

| Função    | Comando | Descrição                                  | Exemplo |
| --------- | ------- | ------------------------------------------ | ------- |
| Consultar | SELECT  | Realizar consultar aos dados de uma tabela | `SELECT * FROM Clients;`        |

## Relacionado
- [[TODO/Banco de Dados| Banco de Dados]]