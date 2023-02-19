# SQL
**Structured Query Language**, é a linguagem padrão para manipulação de dados de banco de dados relacional.

Ela possui subconjuntos, cada um contendo comandos usados para fazer uma determinada categoria de ações:

- [[Programação/SQL/SQL - Data Manipulation Language|SQL - Data Manipulation Language]]: Responsável por realizar inclusões, consultas, alterações e exclusões de dados presentes em registros;
- [[Programação/SQL/SQL - Data Definition Language|SQL - Data Definition Language]]: Permite definir novas tabelas e elementos associados.
- [[Programação/SQL/SQL - Data Control Language|SQL - Data Control Language]]: Permite controlar as autorizações de modificação dos dados do banco de dados.
- [[Programação/SQL/SQL - Data Transaction Language|SQL - Data Transaction Language]]: Controla as transações, permitindo desfazer comandos executados.
- [[Programação/SQL/SQL - Data Query Language|SQL - Data Query Language]]: Utilizado para filtrar dados.

## Exemplo prático
Criando uma tabela chamada "**compras**" com as colunas id, nome, quantity e corredor:
```sql
CREATE TABLE compras (id INTEGER PRIMARY KEY, nome TEXT, quantidade INTEGER, corredor INTEGER);
```

- `PRIMARY KEY` - Utilizamos para definir a coluna que será usada como o identificador único para cada item da tabela.
- `TEXT` - Define que a coluna irá armazenar valores do tipo texto.
- `INTEGER` - Define que a coluna irá armazenar valores numéricos.

Podemos agora adicionar itens (linhas) a tabela:
```sql
INSERT INTO compras VALUES (1, "Banana", 20, 7);
INSERT INTO compras VALUES (2, "Requeijão", 1, 2);
INSERT INTO compras VALUES (3, "Margarina", 1, 2);
INSERT INTO compras VALUES (4, "Sorvete", 2, 12);
INSERT INTO compras VALUES (5, "Pão Francês", 2, 4);
```

Os valores de cada linha são adicionados separados por virgula, na mesma ordem em que as coluna foram criadas pelo `CREATE TABLE`.

Agora podemos visualizar a tabela, selecionando todas as colunas da tabela compras:
```sql
SELECT * FROM compras;
```

`SELECT` - Seleciona as tabelas indicadas, usando o **\*** selecionamos todas as colunas da tabela.

Renderização da tabela após o comando:

| id  | nome        | quantidade | corredor |
| --- | ----------- | ---------- | -------- |
| 1   | Banana      | 20         | 7        |
| 2   | Requeijão   | 5          | 2        |
| 3   | Margarina   | 1          | 2        |
| 4   | Sorvete     | 2          | 12       |
| 5   | Pão Francês | 6          | 4        |

---

Agora que temos nossa tabela, podemos realizar buscas personalizadas.

Se caso quisermos ordenar os items seguindo alguma coluna, podemos usar o seguinte comando:
```sql
SELECT nome, quantidade FROM compras ORDER BY quantidade;
```

`ORDER BY` - Ordena a tabela de forma crescente de acordo com a coluna indicada.

Renderização:

| nome        | quantidade |
| ----------- | ---------- |
| Banana      | 20         |
| Pão Francês | 6          |
| Requeijão   | 5          |
| Sorvete     | 2          |
| Margarina   | 1          |

Observe que não selecionamos todas as colunas, apenas as colunas nome e quantidade, que são as que nos interessa nesse caso.

---

Em tabelas muito grandes é conveniente limitar os resultados obtidos:
```sql
SELECT nome, quantidade FROM compras WHERE quantidade >= 5 ORDER BY quantidade;
```

`WHERE` - Filtra os dados de acordo com uma condição.

Renderização:

| nome        | quantidade |
| ----------- | ---------- |
| Banana      | 20         |
| Pão Francês | 6          |
| Requeijão   | 5          |

---

SQL possui funções internas que facilitam alguns trabalhos:
```sql
SELECT SUM(quantidade) FROM compras;
```

`SUM` - Retorna a soma de todos os itens da coluna;

Renderização:

| SUM(quantidade) |
| --------------- |
| 34              |

---

Podemos agrupar os resultados de uma busca de acordo com uma coluna:
```sql
SELECT corredor, SUM(quantidade) FROM compras GROUP BY corredor;
/*selecionamos a coluna corredor para melhor visualização*/
```

`GROUP BY` - Realiza a busca efetuada para cada valor **diferente** da coluna especificada.

Renderização:

| corredor | SUM(quantidade) |
| -------- | --------------- |
| 7        | 20              |
| 2        | 6               |
| 12       | 2               |
| 4        | 6               |

Nesse exemplo vemos que cada linha diz a quantidade de itens que cada corredor possui.

## Relacionado
- [[TODO/Banco de Dados| Banco de Dados]]