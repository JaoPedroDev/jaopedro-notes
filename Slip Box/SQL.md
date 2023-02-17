# SQL
Criar uma tabela:
```sql
CREATE TABLE nome_da_tabela (coluna01 TIPODEDADO, coluna02 TIPODEDADO...);
```

`PRIMARY KEY` - Usado para definir aquela coluna como identificador único para a tabela
Exemplo:
```sql
CREATE TABLE compras (id INTEGER PRIMARY KEY, nome TEXT, quantidade INTEGER);
```

Adicionando dados na tabela criada
```sql
					 /*ID, Item, Quantidade*/
INSERT INTO compras VALUES (1, "Bananas", 4);
INSERT INTO compras VALUES (2, "Macarrão", 1);
INSERT INTO compras VALUES (3, "Mingual", 2);
```

Selecionando uma tabela(Também mostra a tabela):
```sql
SELECT * FROM compras;
/*Seleciona tudo da tabela*/
```

Renderização da tabela compras:

| id  | nome     | quantidade |
| --- | -------- | ---------- |
| 1   | Bananas  | 4          |
| 2   | Macarrão | 1          |
| 3   | Mingau   | 2          |


`ORDER BY` - Ordena a tabela de forma crescente de acordo com a coluna indicada:
```sql
SELECT * FROM compras ORDER BY quantidade;
```

Render:

| id | nome     | quantidade |
| --- | -------- | ---------- |
| 2   | Macarrão | 1          |
| 3   | Mingau   | 2          |
| 1   | Bananas  | 4          |

---

`WHERE` - Filtra os dados de acordo com uma condição:
```sql
SELECT * FROM compras WHERE quantidade < 3 ORDER BY quantidade;
```

Render:

| id  | nome     | quantidade | 
| --- | -------- | ---------- |
| 2   | Macarrão | 1          |
| 3   | Mingau   | 2          |

---

Considere a seguinte tabela chamada **groceries**:

| id  | name                | quantity | aisle |
| --- | ------------------- | -------- | ----- |
| 1   | Bananas             | 56       | 7     |
| 2   | Peanut Butter       | 1        | 2     |
| 3   | Dark Chocolate Bars | 2        | 2     |
| 4   | Ice cream           | 1        | 12    |
| 5   | Cherries            | 6        | 2     |
| 6   | Chocolate syrup     | 1        | 4     |

`SUM(coluna)` - Podemos usar a função SUM para somar todos os valores de uma coluna:
```sql
SELECT SUM(quantity) FROM groceries;
```

Render:

| SUM (quantity) |
|:-------------- |
| 67             |

`GROUP BY` - Agrupa as linhas que possuem os mesmos valores em linhas únicas, geralmente usado com funções:
```sql
SELECT aisle, SUM(quantity) FROM groceries GROUP BY aisle;
/*selecionamos a coluna aisle para melhor visualização*/
```

Com isso podemos ver a quantidade de itens de cada aisle. Render:

| aisle | SUM(quantity) |
| ----- | ------------- |
| 2     | 9             |
| 4     | 1             |
| 7     | 56            |
| 12    | 1             |

