# [[Programação/SQL/SQL|SQL]] - Data Manipulation Language
**Data Manipulation Language**, responsável por realizar inclusões, consultas, alterações e exclusões de dados presentes em registros.

|   Função   | Comando | Descrição                                 | Exemplo                                                                 |
|:----------:|:-------:|:----------------------------------------- | ----------------------------------------------------------------------- |
| Inclusões  | INSERT  | Insere um registro a uma tabela existente | `INSERT INTO Pessoa (id, nome, sexo) VALUE;`                            |
| Alterações | UPDATE  | Alterar valores de linhas já existentes   | `UPDATE Pessoa SET data_nascimento = '11/09/1985' WHERE id_pessoa = 7;` |
| Exclusões  | DELETE  | Remover linhas existentes de tabelas      | `DELETE FROM pessoa WHERE id_pessoa = 7;`                               |
