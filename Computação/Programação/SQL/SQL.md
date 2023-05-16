# SQL
**Structured Query Language**, é a linguagem padrão para manipulação de dados de banco de dados relacional.

Ela possui subconjuntos, cada um contendo comandos usados para fazer uma determinada categoria de ações:

- [[Computação/Programação/SQL/SQL - Data Manipulation Language|SQL - Data Manipulation Language]]: Responsável por realizar inclusões, consultas, alterações e exclusões de dados presentes em registros;
- [[Computação/Programação/SQL/SQL - Data Definition Language|SQL - Data Definition Language]]: Permite definir novas tabelas e elementos associados.
- [[Computação/Programação/SQL/SQL - Data Control Language|SQL - Data Control Language]]: Permite controlar as autorizações de modificação dos dados do banco de dados.
- [[Computação/Programação/SQL/SQL - Data Transaction Language|SQL - Data Transaction Language]]: Controla as transações, permitindo desfazer comandos executados.
- [[Computação/Programação/SQL/SQL - Data Query Language|SQL - Data Query Language]]: Utilizado para filtrar dados.

## Criação
Criando uma tabela chamada "**compras**" com as colunas id, nome, quantity e corredor:
```sql
CREATE TABLE compras (id INTEGER PRIMARY KEY AUTOINCREMENT, nome TEXT, quantidade INTEGER, corredor INTEGER);
```

- `PRIMARY KEY` - Utilizamos para definir a coluna que será usada como o identificador único para cada item da tabela.
- `TEXT` - Define que a coluna irá armazenar valores do tipo texto.
- `INTEGER` - Define que a coluna irá armazenar valores numéricos.
- `AUTOINCREMENT` - Utilizado junto com a coluna do primary key para auto incrementar seu valor a cada nova linha criada na tabela.

Podemos agora adicionar itens (linhas) a tabela:
```sql
INSERT INTO compras VALUES (1, "Banana", 20, 7);
```

Os valores de cada linha são adicionados separados por virgula, na mesma ordem em que as coluna foram criadas pelo `CREATE TABLE`.

Para pular a coluna id em caso de auto incremento precisamos dizer quais colunas iremos inserir na tabela:
```sql
INSERT INTO compras(nome, quantidade, corredor) VALUES ("Requeijão", 1, 2);
INSERT INTO compras(nome, quantidade, corredor) VALUES ("Margarina", 1, 2);
INSERT INTO compras(nome, quantidade, corredor) VALUES ("Sorvete", 2, 12);
INSERT INTO compras(nome, quantidade, corredor) VALUES ("Pão Francês", 2, 4);
```

## Seleção
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

## Ordenação
Se caso quisermos ordenar os items com base em alguma coluna, podemos usar o seguinte comando:
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

Observe que **não selecionamos** todas as colunas, apenas as colunas nome e quantidade, que são as que nos interessa nesse caso.

## Filtragem

### Where
Utilizado para filtrar os dados de acordo com uma condição.
```sql
SELECT nome, quantidade FROM compras WHERE quantidade >= 5 ORDER BY quantidade;
```
Renderização:

| nome        | quantidade |
| ----------- | ---------- |
| Banana      | 20         |
| Pão Francês | 6          |
| Requeijão   | 5          |

### IN
`IN` - Utilizado para procurar linhas que possuem qualquer um dos valores da lista de valores na coluna especificada:
```sql
SELECT id, nome FROM compras WHERE nome IN ("Banana", "Sorvete", "Manga");
```
Renderização:

| id  | nome    |
| --- | ------- |
| 1   | Banana  |
| 4   | Sorvete |

## LIKE
É utilizado para fazer busca de valores contidos em outros valores, não necessitando ser valores iguais:
```sql
SELECT nome,quantidde FROM compras WHERE nome LIKE "%a";
```

O caractere de porcentagem é utilizado como "*coringa*", ou seja, ele será igual a qualquer caractere que for comparado, assim a expressão "*%a*" retorna todos os valores que terminam com "a".

Renderização:

| nome      | quantidade |
| --------- | ---------- |
| Banana    | 20         |
| Margarina | 1          | 

### AND e OR
Utilizados para filtrar items em mais de uma condição:
```sql
SELECT nome, quantidade FROM compras WHERE quantidade > 2 AND quantidade < 10;

SELECT nome, quantidade FROM compras WHERE nome = "Margarina" OR quantidade > 1;
```

## Sub-consultas

Podemos fazer **sub-consultas** dentro de outras consultas:
```sql
SELECT * FROM compras WHERE nome IN (
	SELECT nome FROM compras WHERE nome <> "Banana"
);
```

É comumente utilizado com buscas em outras tabelas.

## Funções Agregadas

SQL possui funções internas que facilitam alguns trabalhos:
```sql
SELECT SUM(quantidade) FROM compras;
```

`SUM` - Retorna a soma de todos os itens da coluna;

Renderização:

| SUM(quantidade) |
| --------------- |
| 34              |

Outras funções:
- `AVG` - Média
- `COUNT` - Conta a quantidade de linhas
- `MAX` - Maior número
- `MIN` - Menor número

## Renomear - AS
Utilizado para renomear o nome das colunas, oque facilita a interação com tabelas criadas por funções agregadas:
```sql
SELECT SUM(quantidade) AS Soma;
```

Renderização:

| Soma         |
| --------------- |
| 34               |

## Agrupar

### GROUP BY
Realiza a busca efetuada para cada valor **diferente** da coluna especificada:
```sql
SELECT corredor, SUM(quantidade) AS Soma FROM compras GROUP BY corredor;
/*selecionamos a coluna corredor para melhor visualização*/
```

Renderização:

| corredor | Soma |
| -------- | ---- |
| 7        | 20   |
| 2        | 6    |
| 12       | 2    |
| 4        | 6    |

Nesse exemplo vemos que cada linha diz a quantidade de itens que cada corredor possui.

### HAVING
Utilizado para filtrar os resultados de um `GROUP BY`:
```sql
SELECT corredor, SUM(quantidade) AS Soma FROM compras GROUP BY corredor HAVING Soma > 5;
```

Renderização:

| corredor | Soma |
| -------- | ---- |
| 7        | 20   |
| 2        | 6    |
| 4        | 6    |

Utilizamos o nome que damos para o resultado da soma para fazer a condição.
## Relacionado
- [[TODO/Banco de Dados| Banco de Dados]]