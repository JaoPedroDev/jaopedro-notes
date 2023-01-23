# [[Python]] - Tipos de Dados
Python suporta todos os tipos de dados básicos, e também possui dados compostos:
## Integers:
```python
	1 + 2
	#return 3
```

## Floating point:
```python
	1.5 + 2.5
	#return 4.0
```

## Strings:
```python
	#duas
	"hello world"
	
	'hello world'
	
	#Strings podem ser multiplicadas
	print("hello" * 5)
	#return hellohellohellohellohello
```

Strings podem ser comparadas
Elas obedecem a ordem alfabética de cada letra.
```python
	"a" < "b"
	#return True
	"b" > "c"
	#return False
```

Strings multilinhas
```python
	""" Essa é uma
	menssagem em
	varias linhas
	"""
```

Escape codes
"\n" indica nova linha
"\t" indica um tab

## [[Python - Listas]]:
```python
	x = ["a", "b", "c"]
	
	x[1]
	#return 'b'
```
Listas podem ser heterogêneas
```python
	x = ["ola", 1, 2, "word", ["another", "list"]]
```

## Tuples:
Usado para armazenar registro de largura fixos. São como listas, mas não podem ser alterados.
```python
	point = (1, 3)
	# or
	point = 1, 3
	point
	#return (1, 3)
	
	#multiplos valores
	yellow = (255, 255, 0)
	r, g, b = yellow
	print(r, g, b)
	#return 255 255 0
```

## Dicionário:
```python
	person = {"name": "Alice", "email": "alice@exemple.com"}
	person['name']
	#return 'Alice'
```

## Set:
Coleção de elementos não ordenados
```python
	x = {1, 2, 3, 2, 1}
	x
	#return x
	{1, 2, 3}
```

## Boolean:
Representa dois valores, Verdadeiro ou Falso

## None:
Presenta "nada" ou vazio
```python
	x = None
	print(x)
	#return None
```