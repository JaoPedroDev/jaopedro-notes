# [[Computação/Programação/SQL/SQL|SQL]] - Data Control Language
**Data Control Language**, permite controlar as autorizações de modificação dos dados do banco de dados.

| Função    | Comando | Descrição           | Exemplo                                 |
| --------- | ------- | ------------------- | --------------------------------------- |
| Autorizar | GRANT   | Autoriza usuário    | `GRANT SELECT ON Clients TO usuario01;` |
| Revogar   | REVOKE  | Desautoriza usuário | `REVOKE SELECT ON Clients TO usuario01;`                                        |