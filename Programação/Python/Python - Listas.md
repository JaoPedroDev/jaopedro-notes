# [[Python]] - Listas
São conjuntos de elementos de vários tipos de dados.
```python
	x = ["a", "b", "c"] 	# declara uma lista
	
	x[1]	# acessa um elemento da lista
	#return 'b'
	
	x[-1]	# numeros negativos acessam da direita pra esquerda
	#return 'c'
```

Listas podem ser heterogeneas, contendo mais de um unico tipo de dado
```python
	x = ["ola", 1, 2, "word", ["another", "list"]]
```

A função "range()" cria uma lista contendo todos os numeros entre dois numeros.
```python
	x = range(1, 4)
	print(x[-1], x[0])
	#return 3, 1
```

Listas podem ser somadas e multiplicadas usando "+" e "\*".
```python
	a = [1, 2, 3]
	b = [4, 5]
	
	a + b
	#return [1, 2, 3, 4, 5]
	
	b * 3
	#return [4, 5, 4, 5, 4, 5]
```

Podemos acessar mais de um elemento de uma lista de uma vez, criando um sublista através do "slicing"
```python
	a = [1, 2, 3, 4, 5]
	
	a[0:2] 
	#return [1, 2]
	
	a[1:4]
	#return [2, 3, 4]
	
	a[0:-1] 
	#return [1, 2, 3]
```
A lista retornada é composta dos elementos entre os endereços especificados, **incluindo o primeiro endereço, mas excluindo o segundo.**

Podemos adicionar um terceiro numero para especificar o incremento entre cada valor da nova lista
```python
	a = [1, 2, 3, 4, 5]
	
	a[0:6:2]
	#return [1, 3, 5]

	a[::-1] #retorna a lista invertida
	#return [5, 4, 3, 2, 1]
```

Verificar se uma lista possui determinado elemento usando o operardor **in**
```python
	a = [1, 2, 3, 4, 5]

	2 in a
	#return True

	10 in a
	#return False
```

Podemos adicionar elementos em uma lista existente atrvés do método **append()**
```python
	a = [1, 2, 3]

	a.append(4)

	a
	#return [1, 2, 3, 4]
```

O statement **for** é usado para iterar uma lista. Ele executa um bloco de código especificado para cada elemento da lista.
```python
	for x in [1, 2, 3, 4]:
		print(x)
	#return: 
	#1
	#2
	#3	
	#4

	for i in range(10):
		print(i, i*i, i*i*i)
	#return: 
	#0 0 0
	#1 1 1
	#2 4 8
	#3 9 27
	#4 16 64
	#5 25 125
	#6 36 216
	#7 49 343
	#8 64 512
	#9 81 729
```

A função **zip()** transforma duas lista em uma lista de pares. É util quando é preciso iterar duas listas juntas.
```python
	zip(["a", "b", "c"], [1, 2, 3])
	#return [('a', 1), ('b', 2), ('c', 3)]

	names = ["a", "b", "c"]
	values = [1, 2, 3]
	for name, value in zip(names, values):
		print(name, value)
	#return:
	#a 1
	#b 2
	#c 3
```

O método **sort** ordena uma lista. Funciona até mesmo com listas com multiplos tipos de objetos
```python
	a = [2, 10, 4, 3, 7]
	a.sort()
	a
	#return [2, 3, 4, 7, 10]

	x = ["hello", 1, "world", 45, 2]
	x.sort()
	x
	#return [1, 2, 45, 'hello', 'world']

	y = [[2, 3], [1, 6]]
	y.sort()
	y
	#return [[1, 6], [2, 3]]
```
Podemos opcionalmente especificar uma função como uma chave
```python
	a = [[1, 3], [4, 6], [6, 1]]
	
	#ordena a lista de acordo com o segundo elemento de cada entrada
	a.sort(key=lambda x: x[1]) 
	
	a
	#return [[6, 1], [2, 3], [4, 6]]
```

A função **sorted** retorna uma nova lista ordenada, sem modificar a lista original
```python
	a = [2, 10, 4, 3, 7]
	sorted(a)
	#return [2, 3, 4, 7, 10]
```

# Relacionado
- [[Python]]