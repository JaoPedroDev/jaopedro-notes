# Java - Packages Imports
## Packages
Java Packages são usados para agrupar um conjunto de [[Computação/Programação/Java/Java - Classes e Objetos|Classes]] e interfaces. 

Damos um nome ao Package colocando a primeira linha de todos os arquivos com o key word `package` seguido do nome do pacote:
```java
package NomeDoPacote

public class App{
	public static void main(String[] args){
		// Code here
	}
}
```

## Imports
Através dos Packages podemos facilmente importar um conjunto de classes e interfaces em outro pacote, assim tendo acesso a todo um novo conjunto de métodos e funções presentes no pacote importado.

O java possui pacotes pré disponíveis para uso, basta importa-los paro o pacote atual e usar suas funções:
```java
package NomeDoPacote

// Pacote com metodos para opracoes matematicas
import java.lang.Math; 

public class App{
	public static void main(String[] args){
		// retorna o resultado de 2 elevado a 3
		Math.pow(2, 3); 
	}
}
```

