# POO
Glossário POO
# Glossário POO
Índice
========

   * [Construtor](#constructor)
   * [Instanciação](#instanciação)
   * [Getters/Setters](#getters-e-setters)
   * [Assinatura de método](#assinatura-de-metodo)
   * [Sobrecarga de método](#sobrecarga-de-metodo)
   * [Escopo de classe](#escopo-de-classe)
   * [Escopo de objeto](#escopo-de-objeto)
   * [Palavra reservada new](#palavra-reservada-new)
   * [Palavra reservada instanciof](#palavra-reservada-instanciof)
   * [Palavra reservada this](#palavra-reservada-instanciof)
   * [Palavra reservada public/private](#palavra-reservada-public-e-private)
   * [Palavra reservada final](#palavra-reservada-final)
   * [Relacionamento de dependência](#relacionamento-de-dependencia)
   * [Relacinamento de Agregação](#relacionamento-de-agregação)
   * [Relacionamento de Composição](#relacionamento-de-composção)
   

Constructor
========
Os construtores são os responsáveis por criar o objeto em memória, ou seja, instanciar a classe que foi definida.
**Exemplo:**
```java
public class Carro{

private String cor;
private double preco;
private String modelo;

/* CONSTRUTOR PADRÃO */

public Carro(){

}

/* CONSTRUTOR COM 2 PARÂMETROS */

public Carro(String modelo, double preco){

	//Se for escolhido o construtor sem a COR do veículo
	//definimos a cor padrão como sendo PRETA`

	this.cor = “PRETA”;
	this.modelo = modelo;
	this.preco = preco;

}

/* CONSTRUTOR COM 3 PARÂMETROS */

public Carro(String cor, String modelo, double preco){

	this.cor = cor;
	this.modelo = modelo;
	this.preco = preco;

}

}

```

Instanciação
========
Instanciar uma classe significa criar um objeto daquela classe, ou seja: objeto é o conjunto de atributos e métodos da classe. Métodos são 'Funções' que alteram o comportamento dos objetos.
**Exemplo:**
```java
public class Livro{  
	long preco;  
	int quantidade;  
	char tipo;  
}
```
Encapsulamento
========
- Encapsulamento é a restrição de determinados dados de uma classe,tornando assim, disponiveis apenas por meio de métodos.  
Ocultamento é uma parte do encapsulamento.  
São usadas as seguintes palavras para determinar o encapsulamento:  
  
* +Public: Pode ser acessado fora da classe.
* #Protected: Apenas a classe e suas heranças tem acesso.
* -Private: Apenas a própria classe pode acessar.

Getters e Setters
========
O método Getter é utilizado para recuperar alguma informação, geralmente utilizado para trazer informação de algum atributo, sem ter que utilizar o atributo explicitamente. Então chamamos atraves de métodos
Método setter é utilizado para setar um valor dentro de um objeto, de uma variável.
**Exemplo:**
```java
public  class MoradorBean{
	private String nomeMorador;
	private  int apto;
	//método Set
	public void setNomeMorador(String nomeMorador) { 
		this.nomeMorador = nomeMorador;
	} 
	//método get
	public String getNomeMorador() { 
		return nomeMorador;
	}
	//método Set
	public void setApto(int apto) {
		this.apto = apto;
	}
	//método get  
	public int getApto() { 
		return apto; 
	}
	
```


Assinatura de metodo
========
A assinatura é o jeito de identificar um método de forma única. Em linguagens onde vários métodos podem ter o mesmo nome, você precisa ter uma outra forma de evitar a ambiguidade. O compilador precisa saber qual dos métodos com mesmo nome você está chamando. Então você precisa se valer de informações extras disponíveis no método para tomar uma decisão.
**Exemplo:**
```java
int FazAlgumaCoisa() { // faz alguma coisa aqui }

int FazAlgumacoisa(int valor) { // faz alguma coisa aqui }

```

Sobrecarga de metodo
========
**Sobrecarga de método** permite a existência de vários métodos de mesmo nome, porém com assinaturas levemente diferentes ou seja variando no número , tipo de argumentos , no valor de retorno e até variáveis diferentes. Ficará a cargo do compilador escolher de acordo com as listas de argumentos os procedimentos ou métodos a serem executados.
```java
public class Soma {

  public int soma(int x, int y) {
    return x+y;
  } 
  
  public String soma(String x, String y) {
    return x+y;
  } 
  
  public double soma(double x, double y) {
    return x+y;
  } 

}
```
Escopo de classe
========
Escopo refere-se à vida e acessibilidade de uma variável. Quão grande é o alcance depende de onde uma variável é declarada. Por exemplo, se uma variável é declarada na parte superior de uma classe, ela será acessível a todos os métodos de classe. Se for declarada num método, em seguida, só pode ser utilizada em tal método.
**Exemplo:**
```java
public class Main {

    // variavel de classe
    public static int score = 5;
    
    // metodo de classe
    public static void score() {
    }
}
```

Escopo de objeto
========
No escopo de objeto, um atributo ou método existe para o sistema como um todo. Por exemplo, uma variável definida fora do escopo da classe, pode ser acessada por todas as classes.
Caso não seja utilizada a palavra *static*, se define como Escopo de objeto qualquer atributo ou método criado.


Palavra reservada new
========
O operador **new** tem o propósito de criar um novo objeto, o new faz:

1.  instancia a classe através da atribuição de memória para um novo objeto;
    
2.  retorna uma referência à memória alocada;
    
3.  chama o construtor do objeto.
```java
public class TV {
	int tamanho;
	int canal;
	boolean ligada;

	TV() {
		tamanho = 21;
		canal = 0
		ligada = false;
	}
	
	public static void main (String[] args) {

		TV objeto1 = new TV();
		TV objeto2;
		objeto2 = new TV();
	}
}
```

Palavra reservada instanciof
========
*instanceof* compara se um objeto pertence ao mesmo tipo de determinada classe especificada. retorna-se um valor booleano na comparação.
**Exemplo:**
```java
public class cao {
    cao doberman = new cao();
    //Boolean
    boolean resultado;
    resultado = (doberman instanceof cao);
    }
```

Palavra reservada this
========
*This* é utilizado por um objeto para se referenciar a ele mesmo. Utilizado dentro de métodos para fazer referência a atributos do próprio objeto.

**Exemplo:**
```java
public String getModel() {
		return this.model;
	}
```

Palavra reservada public/private
========
Palavras usadas para se definir a visibilidade de um atríbuto ou método ou classe.
*Public* usado para definir que um atríbuto ou método ou classe é visivel para o sístema todo e para qualquer classe do sistema.
*Private* é usado para se definir que um atríbuto ou método é vísivel apenas na própria classe, assim bloquando a alteração de dados ou comportamentos por outras classes.
**Exemplo Public:**
```java
public class Account{
    //Exemplo de váriaveis publicas, acessiveis e modificaveis por diversas classes.
    public double accBalance;
    public String name;
}
```
**Exemplo Private:**
```java
public class Account {
    //Exemplos de váriaveis privadas que podem ser modificadas apenas pela classe Account.
	private double accBalance;
	private String name;
}
```


Palavra reservada final
========
*Final*, utilizada em valores constantes, ou seja, que são imutaveis, somente leitura.
Pode ser usado por uma classe que não poderá ser sobescrita ou uma váriavel que não será mudada durante o processo.

```java
//Classe final
final class Final{
    //Variavel final
    final int HorasdoDia = 24;
}

```

Relacionamento de Dependencia
========
Quando uma classe depende da instancia de outra classe para funcionar, é chamado de relacionamento de dependência. Sendo o objeto recebido como argumento pela classe, para funcionar.
```java
public class DVD-PLAYER
{
//Sendo DVD-MIDIA, outra classe.
 public play(DVD-MIDIA filme){
 }
}
```
Relacinamento de Agregação
========
Uma classe composta por outra classe é um relacionamento de agregação, porém na agregação, um objeto que compõe a classe pode ser utilizado por outras instancias, na agregação, com uma associação parte-todo, mesmo sem o todo, a parte pode continuar a existir.
Na agregação, outras classes podem obter a referência dos objetos que compõem a classe, usando geralmente os métodos getters.  

**Exemplo agregação:**  
![Alt text](https://i.imgur.com/GkJTUr0.gif "Exemplo agregação")

Relacionamento de Composição
========
Composição é um tipo de associação mais forte que a agregação, pois a composição é um relacionamento caracterizado como parte-todo, mas em caso de composição o todo, ele é responsável pelo ciclo de vida da parte, sendo assim a composição é aplicada quando a parte não faz sentido existir sem o todo e quando o objeto que representa o todo for destruido a parte também deverá ser destruída.   
**Exemplo Composição:**  
![Alt text](https://i.imgur.com/ABAYOZf.gif "Exemplo agregação")
