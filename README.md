# 🧮 Calculadora em Java

Uma calculadora simples executada via console (terminal) desenvolvida em Java. O programa recebe dois números e permite ao usuário escolher entre as quatro operações matemáticas básicas.

## 🚀 Funcionalidades

* **Soma (+)**
* **Subtração (-)**
* **Multiplicação (*)**
* **Divisão (/)**

## 💻 Código Fonte Atualizado

O código abaixo já conta com melhorias para aceitar números decimais (`sc.nextDouble()`) e evitar que o programa feche com erros caso o usuário digite um ponto flutuante:

```java
import java.util.Scanner;

public class Calculadora {
    public static void main(String[] args) {
        Scanner sc = new Scanner(System.in);
        double V1, V2, resultado;
        int operacao;

        System.out.println("***CALCULADORA***\n");

        System.out.print("Digite o primeiro valor: ");
        V1 = sc.nextDouble();

        System.out.print("Digite o segundo valor: ");
        V2 = sc.nextDouble();

        System.out.println("\n===Digite o Operador===\n");
        System.out.println("Digite 1 para Soma");
        System.out.println("Digite 2 para Subtração:");
        System.out.println("Digite 3 para Multiplicação:");
        System.out.println("Digite 4 para Dividir:");
        operacao = sc.nextInt();

        switch (operacao) {
            case 1:
                resultado = V1 + V2;
                System.out.println("Resultado: " + resultado);
                break;
            case 2:
                resultado = V1 - V2;
                System.out.println("Resultado: " + resultado);
                break;
            case 3:
                resultado = V1 * V2;
                System.out.println("Resultado: " + resultado);
                break;
            case 4:
                if (V2 != 0) {
                    resultado = V1 / V2;
                    System.out.println("Resultado: " + resultado);
                } else {
                    System.out.println("Erro: Não é possível dividir por zero!");
                }
                break;
            default:
                System.out.println("Valor Inválido");
        }

        System.out.println("\nFIM DO PROGRAMA OBRIGADO!!!");
        sc.close();
    }
}
```

## 🛠️ Como Executar o Projeto

### Pré-requisitos
Você vai precisar do [JDK (Java Development Kit)](https://oracle.com) instalado na sua máquina (versão 8 ou superior).

### Passo a Passo

1. **Clone o repositório ou baixe o arquivo:**
   ```bash
   git clone https://github.com
   ```

2. **Abra o terminal/prompt de comando** na pasta onde o arquivo `Calculadora.java` está salvo.

3. **Compile o código:**
   ```bash
   javac Calculadora.java
   ```

4. **Execute o programa:**
   ```bash
   java Calculadora
   ```

## 📝 Aprendizados e Conceitos Praticados

* Estrutura condicional de escolha (`switch-case`).
* Entrada de dados com a classe `Scanner`.
* Manipulação de variáveis do tipo primitivo (`int` e `double`).
