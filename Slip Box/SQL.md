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

---

`IN` - Utilizado para procurar linhas que possuem qualquer um dos valores da lista de valores na coluna especificada:
```sql
SELECT * FROM tabela WHERE coluna IN ("Valor1", "Valor2", "Valor3");
```

---

Podemos fazer **sub-consultas** dentro de outras consultas:
```sql
SELECT * FROM tabela WHERE coluna IN (
	SELECT coluna FROM outra_tabela WHERE coluna = 5
);
```

Assim o primeiro SELECT utiliza o resultado do segundo SELECT como lista de procura do IN.

---

`LIKE` - É utilizado para fazer busca de valores contidos em outros valores, não necessitando ser valores iguais:
```sql
SELECT * FROM tabela WHERE coluna LIKE "%string%";
```

O caractere de porcentagem é utilizado como "*coringa*", ou seja, ele será igual a qualquer caractere que for comparado, assim a expressão "*%string%*" retorna todos os valores que contém a palavra "string".