Curso de Java: Do Básico ao Polimorfismo

Fase 1: Fundamentos Básicos de Java

1.1 Introdução ao Java e Ambiente de Desenvolvimento

Java é uma linguagem de programação orientada a objetos, de alto nível, desenvolvida pela Sun Microsystems (agora Oracle). É conhecida por sua portabilidade (Write Once, Run Anywhere - WORA), segurança e robustez. É amplamente utilizada para desenvolvimento de aplicações corporativas, mobile (Android), web, sistemas embarcados e muito mais.

1.1.1 O que é Java?

Java é uma plataforma de desenvolvimento que inclui uma linguagem de programação, uma máquina virtual (JVM - Java Virtual Machine) e um conjunto de bibliotecas (APIs). A JVM é o que permite a portabilidade do código Java, pois ela interpreta o bytecode Java (código compilado) para o sistema operacional específico.

1.1.2 Vantagens do Java

•
Portabilidade: O código compilado (bytecode) pode ser executado em qualquer plataforma que possua uma JVM.

•
Orientação a Objetos: Facilita a organização e manutenção do código, promovendo a reutilização.

•
Segurança: Possui um modelo de segurança robusto, ideal para aplicações em rede.

•
Robustez: Gerenciamento automático de memória (Garbage Collector) e tratamento de exceções.

•
Multithreading: Suporte nativo para programação concorrente.

•
Comunidade: Grande comunidade de desenvolvedores e vasta quantidade de recursos e bibliotecas.

1.1.3 Ambiente de Desenvolvimento Java (JDK, JRE, JVM)

Para desenvolver e executar aplicações Java, você precisará dos seguintes componentes:

•
JDK (Java Development Kit): É um kit completo para desenvolvimento em Java. Inclui o JRE, o compilador Java (javac), o depurador (jdb) e outras ferramentas.

•
JRE (Java Runtime Environment): É o ambiente de execução Java. Contém a JVM e as bibliotecas necessárias para executar aplicações Java. Se você só precisa executar programas Java, o JRE é suficiente.

•
JVM (Java Virtual Machine): É a máquina virtual que executa o bytecode Java. Ela é responsável por traduzir o bytecode para o código nativo do sistema operacional.

1.1.4 Configurando o Ambiente de Desenvolvimento

1.
Download e Instalação do JDK: Baixe a versão mais recente do JDK no site oficial da Oracle ou utilize uma distribuição OpenJDK (como o Adoptium).

2.
Configuração da Variável de Ambiente JAVA_HOME: Defina a variável de ambiente JAVA_HOME para o diretório de instalação do JDK.

3.
Adicionar o JDK ao PATH: Adicione o diretório bin do JDK à variável de ambiente PATH do seu sistema operacional.

Exemplo de configuração (Linux/macOS):

Bash


export JAVA_HOME=/path/to/your/jdk
export PATH=$PATH:$JAVA_HOME/bin


Verificando a instalação:

Abra um terminal e digite:

Bash


java -version
javac -version


Se a instalação estiver correta, você verá as versões do Java e do compilador.

1.1.5 IDEs (Integrated Development Environments)

IDEs são ferramentas que facilitam o desenvolvimento, oferecendo recursos como edição de código, depuração, compilação e gerenciamento de projetos. As mais populares para Java são:

•
IntelliJ IDEA: Altamente produtivo e com muitos recursos.

•
Eclipse: Gratuito, de código aberto e muito utilizado.

•
VS Code: Leve e extensível, com bom suporte a Java através de plugins.

Recomenda-se instalar uma IDE para uma melhor experiência de desenvolvimento.




1.2 Sintaxe Básica, Tipos de Dados, Variáveis e Operadores

1.2.1 Estrutura Básica de um Programa Java

Todo programa Java começa com uma classe. O método main é o ponto de entrada da aplicação.

Java


public class MeuPrimeiroPrograma {
    public static void main(String[] args) {
        // Seu código vai aqui
        System.out.println("Olá, Mundo!");
    }
}


•
public class MeuPrimeiroPrograma: Declara uma classe pública chamada MeuPrimeiroPrograma. O nome do arquivo Java deve ser o mesmo nome da classe pública (ex: MeuPrimeiroPrograma.java).

•
public static void main(String[] args): É o método principal onde a execução do programa começa.

•
public: O método é acessível de qualquer lugar.

•
static: O método pertence à classe, não a uma instância específica do objeto.

•
void: O método não retorna nenhum valor.

•
main: É o nome padrão do método de entrada.

•
(String[] args): Parâmetros de linha de comando que podem ser passados para o programa.



•
System.out.println("Olá, Mundo!");: Imprime a string "Olá, Mundo!" no console e adiciona uma nova linha.

1.2.2 Comentários

Comentários são usados para explicar o código e são ignorados pelo compilador.

Java


// Este é um comentário de linha única

/*
 * Este é um comentário de múltiplas linhas.
 * Ele pode abranger várias linhas.
 */

/**
 * Este é um comentário de documentação (Javadoc).
 * Usado para gerar documentação automática.
 */


1.2.3 Tipos de Dados

Java possui dois tipos de dados: primitivos e de referência.

Tipos Primitivos: Armazenam valores simples diretamente.

TipoTamanho (bits)Faixa de Valoresbyte8-128 a 127short16-32.768 a 32.767int32-2.147.483.648 a 2.147.483.647long64-9.223.372.036.854.775.808 a 9.223.372.036.854.775.807float32Ponto flutuante de precisão simplesdouble64Ponto flutuante de precisão duplaboolean1true ou falsechar16Caractere Unicode (0 a 65.535)

Tipos de Referência: Armazenam referências (endereços de memória) para objetos. Exemplos incluem String, Array e todas as classes que você cria.

1.2.4 Variáveis

Variáveis são "contêineres" para armazenar dados. Antes de usar uma variável, ela deve ser declarada e, opcionalmente, inicializada.

Declaração: tipo nomeDaVariavel;
Inicialização: nomeDaVariavel = valor;
Declaração e Inicialização: tipo nomeDaVariavel = valor;

Java


public class Variaveis {
    public static void main(String[] args) {
        // Declaração e inicialização de variáveis primitivas
        int idade = 30;
        double altura = 1.75;
        boolean estaAtivo = true;
        char inicial = 'J';

        // Variável de referência (String é uma classe em Java)
        String nome = "João";

        System.out.println("Nome: " + nome);
        System.out.println("Idade: " + idade);
        System.out.println("Altura: " + altura);
        System.out.println("Ativo: " + estaAtivo);
        System.out.println("Inicial: " + inicial);
    }
}


1.2.5 Operadores

Operadores são símbolos que realizam operações em variáveis e valores.

Operadores Aritméticos: +, -, *, /, % (módulo)

Java


int a = 10;
int b = 3;
System.out.println(a + b); // 13
System.out.println(a - b); // 7
System.out.println(a * b); // 30
System.out.println(a / b); // 3 (divisão inteira)
System.out.println(a % b); // 1 (resto da divisão)


Operadores de Atribuição: =, +=, -=, *=, /=, %=

Java


int x = 5;
x += 3; // Equivalente a x = x + 3; (x agora é 8)


Operadores de Comparação (Relacionais): == (igual a), != (diferente de), > (maior que), < (menor que), >= (maior ou igual a), <= (menor ou igual a)

Java


int num1 = 10;
int num2 = 20;
System.out.println(num1 == num2); // false
System.out.println(num1 < num2);  // true


Operadores Lógicos: && (AND lógico), || (OR lógico), ! (NOT lógico)

Java


boolean condicao1 = true;
boolean condicao2 = false;
System.out.println(condicao1 && condicao2); // false
System.out.println(condicao1 || condicao2); // true
System.out.println(!condicao1);             // false


Operadores de Incremento/Decremento: ++ (incremento), -- (decremento)

Java


int contador = 0;
contador++; // contador agora é 1
contador--; // contador agora é 0

// Pré-incremento/decremento vs Pós-incremento/decremento
int i = 5;
int j = ++i; // j é 6, i é 6 (incrementa antes de atribuir)
int k = i++; // k é 6, i é 7 (atribui antes de incrementar)





1.3 Estruturas de Controle de Fluxo

As estruturas de controle de fluxo permitem que você execute blocos de código condicionalmente ou repita a execução de blocos de código.

1.3.1 Estruturas Condicionais (if, else if, else, switch)

if-else: Executa um bloco de código se uma condição for verdadeira, e outro bloco se for falsa.

Java


public class Condicionais {
    public static void main(String[] args) {
        int idade = 18;

        if (idade >= 18) {
            System.out.println("Você é maior de idade.");
        } else {
            System.out.println("Você é menor de idade.");
        }

        int nota = 75;
        if (nota >= 90) {
            System.out.println("Conceito A");
        } else if (nota >= 80) {
            System.out.println("Conceito B");
        } else if (nota >= 70) {
            System.out.println("Conceito C");
        } else {
            System.out.println("Conceito D");
        }
    }
}


switch: Permite selecionar um entre muitos blocos de código a serem executados.

Java


public class SwitchCase {
    public static void main(String[] args) {
        int diaDaSemana = 3; // 1 = Domingo, 2 = Segunda, etc.
        String nomeDoDia;

        switch (diaDaSemana) {
            case 1:
                nomeDoDia = "Domingo";
                break;
            case 2:
                nomeDoDia = "Segunda-feira";
                break;
            case 3:
                nomeDoDia = "Terça-feira";
                break;
            case 4:
                nomeDoDia = "Quarta-feira";
                break;
            case 5:
                nomeDoDia = "Quinta-feira";
                break;
            case 6:
                nomeDoDia = "Sexta-feira";
                break;
            case 7:
                nomeDoDia = "Sábado";
                break;
            default:
                nomeDoDia = "Dia inválido";
                break;
        }
        System.out.println("Hoje é " + nomeDoDia);
    }
}


1.3.2 Estruturas de Repetição (Loops: for, while, do-while, for-each)

for: Repete um bloco de código um número fixo de vezes.

Java


public class LoopFor {
    public static void main(String[] args) {
        for (int i = 0; i < 5; i++) {
            System.out.println("Contagem: " + i);
        }

        // Loop for para iterar sobre um array
        String[] frutas = {"Maçã", "Banana", "Laranja"};
        for (int i = 0; i < frutas.length; i++) {
            System.out.println(frutas[i]);
        }
    }
}


while: Repete um bloco de código enquanto uma condição for verdadeira.

Java


public class LoopWhile {
    public static void main(String[] args) {
        int contador = 0;
        while (contador < 3) {
            System.out.println("Contador: " + contador);
            contador++;
        }
    }
}


do-while: Similar ao while, mas garante que o bloco de código seja executado pelo menos uma vez.

Java


public class LoopDoWhile {
    public static void main(String[] args) {
        int i = 0;
        do {
            System.out.println("Valor de i: " + i);
            i++;
        } while (i < 3);
    }
}


for-each (Enhanced for loop): Usado para iterar sobre arrays e coleções.

Java


public class LoopForEach {
    public static void main(String[] args) {
        int[] numeros = {1, 2, 3, 4, 5};
        for (int numero : numeros) {
            System.out.println("Número: " + numero);
        }
    }
}


1.3.3 break e continue

•
break: Sai imediatamente do loop ou da estrutura switch.

•
continue: Pula a iteração atual do loop e vai para a próxima.

Java


public class BreakContinue {
    public static void main(String[] args) {
        for (int i = 0; i < 10; i++) {
            if (i == 5) {
                break; // Sai do loop quando i for 5
            }
            if (i % 2 != 0) {
                continue; // Pula números ímpares
            }
            System.out.println(i);
        }
    }
}
// Saída esperada: 0, 2, 4





1.4 Métodos

Métodos são blocos de código que realizam uma tarefa específica. Eles ajudam a organizar o código, torná-lo reutilizável e mais legível.

1.4.1 Declaração de Métodos

Um método é declarado com um modificador de acesso, um tipo de retorno, um nome, e uma lista de parâmetros (opcional).

Java


modificadorDeAcesso tipoDeRetorno nomeDoMetodo(tipoParametro1 nomeParametro1, tipoParametro2 nomeParametro2, ...) {
    // Corpo do método
    // ...
    return valorDeRetorno; // Se o tipoDeRetorno não for 'void'
}


•
modificadorDeAcesso: Define onde o método pode ser acessado (public, private, protected, ou padrão/package-private).

•
tipoDeRetorno: O tipo de dado que o método retorna. Se o método não retorna nada, use void.

•
nomeDoMetodo: Um identificador para o método. Deve seguir as convenções de nomenclatura Java (camelCase).

•
listaDeParametros: Uma lista de variáveis que o método aceita como entrada, separadas por vírgulas. Cada parâmetro tem um tipo e um nome.

1.4.2 Exemplos de Métodos

Java


public class ExemploMetodos {

    // Método que não retorna valor (void) e não recebe parâmetros
    public static void saudacao() {
        System.out.println("Olá! Bem-vindo ao curso de Java.");
    }

    // Método que retorna um valor (int) e recebe dois parâmetros (int)
    public static int somar(int a, int b) {
        int resultado = a + b;
        return resultado;
    }

    // Método que retorna um valor (String) e recebe um parâmetro (String)
    public static String formatarNome(String nome, String sobrenome) {
        return sobrenome.toUpperCase() + ", " + nome;
    }

    // Método que calcula a média de três números (double)
    public static double calcularMedia(double n1, double n2, double n3) {
        return (n1 + n2 + n3) / 3;
    }

    public static void main(String[] args) {
        // Chamando o método saudacao
        saudacao(); // Saída: Olá! Bem-vindo ao curso de Java.

        // Chamando o método somar e armazenando o resultado
        int soma = somar(5, 3);
        System.out.println("A soma é: " + soma); // Saída: A soma é: 8

        // Chamando o método formatarNome
        String nomeCompleto = formatarNome("Maria", "Silva");
        System.out.println("Nome formatado: " + nomeCompleto); // Saída: SILVA, Maria

        // Chamando o método calcularMedia
        double media = calcularMedia(7.5, 8.0, 6.5);
        System.out.println("A média é: " + media); // Saída: A média é: 7.333...
    }
}


1.4.3 Sobrecarga de Métodos (Method Overloading)

Java permite que uma classe tenha múltiplos métodos com o mesmo nome, desde que eles tenham listas de parâmetros diferentes (número de parâmetros, tipo de parâmetros ou ordem dos parâmetros). Isso é chamado de sobrecarga de métodos.

Java


public class SobrecargaMetodos {

    // Método para somar dois inteiros
    public static int somar(int a, int b) {
        return a + b;
    }

    // Método sobrecarregado para somar três inteiros
    public static int somar(int a, int b, int c) {
        return a + b + c;
    }

    // Método sobrecarregado para somar dois doubles
    public static double somar(double a, double b) {
        return a + b;
    }

    public static void main(String[] args) {
        System.out.println("Soma de 2 inteiros: " + somar(10, 20)); // Saída: 30
        System.out.println("Soma de 3 inteiros: " + somar(10, 20, 30)); // Saída: 60
        System.out.println("Soma de 2 doubles: " + somar(10.5, 20.3)); // Saída: 30.8
    }
}





1.5 Exemplos Práticos da Fase 1

Exemplo 1: Calculadora Simples

Este programa demonstra o uso de variáveis, operadores aritméticos, entrada de dados (usando Scanner) e estruturas condicionais.

Java


import java.util.Scanner;

public class CalculadoraSimples {
    public static void main(String[] args) {
        Scanner scanner = new Scanner(System.in);

        System.out.println("--- Calculadora Simples ---");
        System.out.print("Digite o primeiro número: ");
        double num1 = scanner.nextDouble();

        System.out.print("Digite o segundo número: ");
        double num2 = scanner.nextDouble();

        System.out.print("Escolha a operação (+, -, *, /): ");
        char operacao = scanner.next().charAt(0);

        double resultado;

        switch (operacao) {
            case '+':
                resultado = num1 + num2;
                System.out.println("Resultado: " + resultado);
                break;
            case '-':
                resultado = num1 - num2;
                System.out.println("Resultado: " + resultado);
                break;
            case '*':
                resultado = num1 * num2;
                System.out.println("Resultado: " + resultado);
                break;
            case '/':
                if (num2 != 0) {
                    resultado = num1 / num2;
                    System.out.println("Resultado: " + resultado);
                } else {
                    System.out.println("Erro: Divisão por zero não é permitida.");
                }
                break;
            default:
                System.out.println("Operação inválida.");
        }

        scanner.close();
    }
}


Exemplo 2: Verificador de Número Primo

Este programa utiliza loops e condicionais para verificar se um número é primo.

Java


import java.util.Scanner;

public class VerificadorPrimo {
    public static void main(String[] args) {
        Scanner scanner = new Scanner(System.in);

        System.out.print("Digite um número inteiro positivo: ");
        int numero = scanner.nextInt();

        if (numero <= 1) {
            System.out.println(numero + " não é um número primo.");
        } else {
            boolean ehPrimo = true;
            for (int i = 2; i <= Math.sqrt(numero); i++) {
                if (numero % i == 0) {
                    ehPrimo = false;
                    break;
                }
            }

            if (ehPrimo) {
                System.out.println(numero + " é um número primo.");
            } else {
                System.out.println(numero + " não é um número primo.");
            }
        }
        scanner.close();
    }
}


Exemplo 3: Tabuada com Método

Este exemplo demonstra a criação e uso de um método para gerar a tabuada de um número.

Java


import java.util.Scanner;

public class TabuadaComMetodo {

    public static void gerarTabuada(int numero) {
        System.out.println("Tabuada do " + numero + ":");
        for (int i = 1; i <= 10; i++) {
            System.out.println(numero + " x " + i + " = " + (numero * i));
        }
    }

    public static void main(String[] args) {
        Scanner scanner = new Scanner(System.in);

        System.out.print("Digite um número para ver a tabuada: ");
        int num = scanner.nextInt();

        gerarTabuada(num);

        scanner.close();
    }
}





1.6 Exercícios da Fase 1

1.
Cálculo de Média: Crie um programa que solicite ao usuário três notas, calcule a média e informe se o aluno foi aprovado (média >= 7) ou reprovado.

2.
Conversor de Temperatura: Desenvolva um programa que converta uma temperatura de Celsius para Fahrenheit. A fórmula é F = C * 1.8 + 32. Peça ao usuário para inserir a temperatura em Celsius.

3.
Contagem Regressiva: Escreva um programa que faça uma contagem regressiva de 10 até 0, imprimindo cada número e, ao final, a mensagem "FIM!".

4.
Verificador de Par ou Ímpar: Crie um método que receba um número inteiro como parâmetro e retorne true se o número for par e false se for ímpar. No método main, chame este método e imprima o resultado.

5.
Maior de Três Números: Implemente um método que receba três números inteiros e retorne o maior entre eles. Utilize este método no main para testar com diferentes valores.




Fase 2: Programação Orientada a Objetos - Classes e Objetos

2.1 Classes e Objetos

Java é uma linguagem orientada a objetos (POO). A Programação Orientada a Objetos é um paradigma de programação que organiza o software em torno de objetos, em vez de ações e lógica. Um objeto é uma instância de uma classe, e uma classe é um modelo ou "planta" para criar objetos.

2.1.1 O que é uma Classe?

Uma classe é um modelo, um protótipo ou uma "planta" a partir da qual os objetos são criados. Ela define as características (atributos) e os comportamentos (métodos) que os objetos desse tipo terão. Pense em uma classe como a planta de uma casa: ela descreve como a casa será construída, mas não é a casa em si.

Sintaxe de uma Classe:

Java


public class NomeDaClasse {
    // Atributos (variáveis de instância)
    tipoAtributo1 nomeAtributo1;
    tipoAtributo2 nomeAtributo2;

    // Construtores
    // ...

    // Métodos (comportamentos)
    modificadorDeAcesso tipoDeRetorno nomeDoMetodo(parametros) {
        // Corpo do método
    }
}


Exemplo de Classe Carro:

Java


public class Carro {
    // Atributos
    String marca;
    String modelo;
    int ano;
    String cor;

    // Métodos
    public void ligar() {
        System.out.println("O carro " + modelo + " está ligado.");
    }

    public void acelerar() {
        System.out.println("O carro " + modelo + " está acelerando.");
    }

    public void frear() {
        System.out.println("O carro " + modelo + " está freando.");
    }
}


2.1.2 O que é um Objeto?

Um objeto é uma instância concreta de uma classe. É a "casa" construída a partir da "planta". Cada objeto tem seu próprio conjunto de valores para os atributos definidos na classe e pode executar os métodos definidos por ela.

Criando Objetos (Instanciação):

Para criar um objeto, usamos a palavra-chave new seguida do nome da classe e parênteses (que chamam o construtor).

Java


public class ExemploObjeto {
    public static void main(String[] args) {
        // Criando um objeto da classe Carro
        Carro meuCarro = new Carro();

        // Acessando e modificando atributos do objeto
        meuCarro.marca = "Toyota";
        meuCarro.modelo = "Corolla";
        meuCarro.ano = 2022;
        meuCarro.cor = "Prata";

        System.out.println("Marca: " + meuCarro.marca);
        System.out.println("Modelo: " + meuCarro.modelo);
        System.out.println("Ano: " + meuCarro.ano);
        System.out.println("Cor: " + meuCarro.cor);

        // Chamando métodos do objeto
        meuCarro.ligar();
        meuCarro.acelerar();
        meuCarro.frear();

        // Criando outro objeto da classe Carro
        Carro seuCarro = new Carro();
        seuCarro.marca = "Honda";
        seuCarro.modelo = "Civic";
        seuCarro.ano = 2023;
        seuCarro.cor = "Preto";

        System.out.println("\nMarca: " + seuCarro.marca);
        System.out.println("Modelo: " + seuCarro.modelo);
        seuCarro.ligar();
    }
}


Neste exemplo, meuCarro e seuCarro são dois objetos distintos da classe Carro. Cada um tem seus próprios valores para marca, modelo, ano e cor.




2.2 Construtores

Um construtor é um método especial usado para inicializar objetos. Ele é chamado automaticamente quando um objeto de uma classe é criado usando a palavra-chave new. O nome do construtor deve ser exatamente o mesmo nome da classe e ele não possui tipo de retorno (nem mesmo void).

2.2.1 Construtor Padrão (Default Constructor)

Se você não definir nenhum construtor em sua classe, o Java fornecerá um construtor padrão (sem argumentos) implicitamente. Este construtor inicializa os atributos com seus valores padrão (0 para numéricos, false para booleanos, null para referências).

2.2.2 Construtor Sem Argumentos

Você pode definir seu próprio construtor sem argumentos, que pode conter lógica de inicialização específica.

Java


public class Pessoa {
    String nome;
    int idade;

    // Construtor sem argumentos
    public Pessoa() {
        this.nome = "Desconhecido";
        this.idade = 0;
        System.out.println("Objeto Pessoa criado com construtor padrão.");
    }

    public void apresentar() {
        System.out.println("Olá, meu nome é " + nome + " e tenho " + idade + " anos.");
    }
}


2.2.3 Construtor Com Argumentos

É comum usar construtores para inicializar os atributos de um objeto com valores fornecidos no momento da criação. Isso garante que o objeto seja criado em um estado válido.

Java


public class Produto {
    String nome;
    double preco;
    int quantidade;

    // Construtor com argumentos
    public Produto(String nome, double preco, int quantidade) {
        this.nome = nome; // 'this' refere-se à instância atual do objeto
        this.preco = preco;
        this.quantidade = quantidade;
        System.out.println("Produto " + nome + " criado.");
    }

    public void exibirDetalhes() {
        System.out.println("Nome: " + nome + ", Preço: " + preco + ", Quantidade: " + quantidade);
    }
}


2.2.4 Sobrecarga de Construtores

Assim como métodos, construtores também podem ser sobrecarregados. Isso significa que uma classe pode ter múltiplos construtores, desde que cada um tenha uma lista de parâmetros diferente.

Java


public class Livro {
    String titulo;
    String autor;
    int anoPublicacao;

    // Construtor 1: Apenas título e autor
    public Livro(String titulo, String autor) {
        this.titulo = titulo;
        this.autor = autor;
        this.anoPublicacao = 0; // Valor padrão
    }

    // Construtor 2: Título, autor e ano de publicação
    public Livro(String titulo, String autor, int anoPublicacao) {
        // Reutilizando o construtor 1 usando 'this()'
        this(titulo, autor);
        this.anoPublicacao = anoPublicacao;
    }

    public void exibirInfo() {
        System.out.println("Título: " + titulo + ", Autor: " + autor + ", Ano: " + (anoPublicacao == 0 ? "Não informado" : anoPublicacao));
    }

    public static void main(String[] args) {
        Livro livro1 = new Livro("O Senhor dos Anéis", "J.R.R. Tolkien");
        livro1.exibirInfo();

        Livro livro2 = new Livro("1984", "George Orwell", 1949);
        livro2.exibirInfo();
    }
}


O uso de this() dentro de um construtor permite chamar outro construtor da mesma classe, evitando duplicação de código.




2.3 Atributos e Métodos

Atributos e métodos são os pilares de uma classe, definindo o que um objeto "é" (seus dados) e o que ele "faz" (seu comportamento).

2.3.1 Atributos (Variáveis de Instância)

Atributos são variáveis que pertencem a uma classe e definem as características ou o estado de um objeto. Cada objeto criado a partir da classe terá sua própria cópia desses atributos, com seus próprios valores.

Java


public class ContaBancaria {
    // Atributos
    String numeroConta;
    String titular;
    double saldo; // Saldo inicial da conta
    boolean ativa; // Indica se a conta está ativa

    // ... construtores e métodos
}


•
numeroConta, titular, saldo, ativa são atributos da classe ContaBancaria.

•
Eles são chamados de variáveis de instância porque seus valores são específicos para cada instância (objeto) da classe.

2.3.2 Métodos (Comportamentos)

Métodos são blocos de código que definem o comportamento de um objeto. Eles realizam ações, manipulam os atributos do objeto ou interagem com outros objetos. Métodos são a forma como os objetos se comunicam e executam tarefas.

Java


public class ContaBancaria {
    String numeroConta;
    String titular;
    double saldo;
    boolean ativa;

    public ContaBancaria(String numeroConta, String titular, double saldoInicial) {
        this.numeroConta = numeroConta;
        this.titular = titular;
        this.saldo = saldoInicial;
        this.ativa = true;
    }

    // Método para depositar dinheiro
    public void depositar(double valor) {
        if (valor > 0) {
            saldo += valor;
            System.out.println("Depósito de R$" + valor + " realizado. Novo saldo: R$" + saldo);
        } else {
            System.out.println("Valor de depósito inválido.");
        }
    }

    // Método para sacar dinheiro
    public boolean sacar(double valor) {
        if (valor > 0 && saldo >= valor) {
            saldo -= valor;
            System.out.println("Saque de R$" + valor + " realizado. Novo saldo: R$" + saldo);
            return true;
        } else if (valor <= 0) {
            System.out.println("Valor de saque inválido.");
            return false;
        } else {
            System.out.println("Saldo insuficiente para saque de R$" + valor + ". Saldo atual: R$" + saldo);
            return false;
        }
    }

    // Método para exibir o saldo
    public double getSaldo() {
        return saldo;
    }

    // Método para verificar se a conta está ativa
    public boolean isAtiva() {
        return ativa;
    }

    // Método para desativar a conta
    public void desativarConta() {
        this.ativa = false;
        System.out.println("Conta " + numeroConta + " desativada.");
    }

    public static void main(String[] args) {
        ContaBancaria minhaConta = new ContaBancaria("12345-6", "Alice Silva", 1000.0);
        System.out.println("Saldo inicial: R$" + minhaConta.getSaldo());

        minhaConta.depositar(500.0);
        minhaConta.sacar(200.0);
        minhaConta.sacar(1500.0); // Tentativa de saque com saldo insuficiente

        System.out.println("Saldo final: R$" + minhaConta.getSaldo());
        System.out.println("Conta ativa? " + minhaConta.isAtiva());

        minhaConta.desativarConta();
        System.out.println("Conta ativa? " + minhaConta.isAtiva());
    }
}


Neste exemplo, depositar, sacar, getSaldo, isAtiva e desativarConta são métodos que definem o comportamento de um objeto ContaBancaria. Eles operam sobre os atributos (saldo, ativa) da própria instância do objeto.

