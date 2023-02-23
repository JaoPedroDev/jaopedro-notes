```sql
CREATE TABLE exemplo
(id INTEGER PRIMARY KEY AUTOINCREMENT,
 coluna01 TEXT,
 coluna02 INTEGER);
```

`AUTOINCREMENT` - Utilizado junto com a coluna do primary key para auto incrementar seu valor a cada nova linha na tabela.

Para pular a coluna id em caso de auto incremento precisamos dizer quais colunas iremos inserir na tabela:
```sql
INSERT INTO exemplo(coluna01, coluna02) VALUES ("Valor", 1515);
```

---

Podemos combinar condições que a clausula `WHERE` faz através dos operadores lógicos `AND` e `OR`:
```sql
SELECT * FROM tabela WHERE valor > 5 AND outro_valor < 10;

SELECT * FROM tabela WHERE valor > 5 OR outro_valor < 10;
```

