# [[Programação/Python/Python|Python]] - Funções
## len():
Retorna a quantidade de elementos de uma string, lista ou outras coleções
```python
	len("hello")
	#return 5
	
	len(['a', 'b', 'c'])
	#return 3
```

[[Programação/Python/Python|Python]] não aceita operações de tipo de dados diferentes, para isso possui funções de conversão de tipo de dados.
```python
	int("5")
	#return 5
	
	str(5)
	#return '5'
	
	str(5) + "2"
	#return '52'
```

Contando o número de digitos em um número:
```python
	len(str(12345))
	#return 5
	
	len(str(2 ** 100))  #quantidade de digitos de 2 elevado a 100
	#return 31
```

### Escrevendo as próprias funções:
```Python
	def square(x):
		return x * x
		
	square(5)
	#return 25
```
**Necessita de indentação**, python usa a indentação para dividir os blocos de código.

Funções podem ser passadas como argumentos.
```Python
	f = square
	f(4)
	#return 16
```

Variáveis globais só podem ser lidas dentro das funções
```Python
	x = 0
	y = 0
	def incr(x):
    	y = x + 1
    	return y
	incr(5)
	print x, y
	#return 0, 0
```
Para altera-las é necessário declarar explicitamente que são globais
```Python
	numcalls = 0
	def square(x):
		global numcalls
		numcalls = numcalls + 1
		return x * x
	#return 
```

### Lambda operator
```Python
	cube = lambda x: x ** 3
	fxy(cube, 2, 3)
	#return 35
	
	fxy(lambda x: x ** 3, 2, 3)
	#return 35
```

Lambda não precisa de um "return", é uma expressão única.
Usado frequentemente quando é necessário funções pequenas a serem passadas como argumentos.