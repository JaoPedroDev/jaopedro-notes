# Java - Classes e Objetos

- Classes: É um template para um objeto, que possui seus possíveis atributos e métodos.
- Objeto: É a instancia de uma classe, com seus atributos individuais definidos.

Digamos que queremos representar um humano, então criamos a classe Humano, todo o humano possui os atributos: nome, idade e altura, e todo humano possui os métodos: correr e pular. A classe Humano representa apenas oque é um humano, não algum humano em especifico.
Já o Objeto é uma instancia de uma classe, nesse caso podemos criar o Objeto do tipo Humano com os atributos: 
nome = "Jorge"
idade = 34
Outro Objeto do tipo Humano com os atributos:
nome = "Ana"
idade = 20
Ambas as instancias podem executar os métodos correr e pular, mesmo possuindo atributos diferentes.

## Declarando Classe e Objeto
Em java podemos declarar uma classe da seguinte maneira:
```java
public class Humano {
	String nome;
	int idade;
	
	// Constructor, usado na instanciacao
	// de um novo objeto
	public Humano(String nome, int idade){
		this.nome = nome;
		this.idade = idade;
	}
	
	public void correr() {
		System.out.println("Correndo");
	}
	
	public void pular() {
		System.out.println("Correndo");
	}
}
```

Podemos então declarar um Objeto a partir dessa classe:
```java
public class App {
   public static void main(String []args) {
		// Novo objeto da classe humano
		// Nome = Jorge
		// Idade = 34
		Humano jorge = new Humano("Jorge", 34);
		
		// Chamando os metodos
		jorge.correr();
		jorge.pular();
   }
}
```