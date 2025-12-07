# Exercícios 

1. Escreva um código onde o usuário entra com um número e seja gerada a tabuada de 1 até 10 desse número;

2. Escreva um código onde o usuário entra com sua altura e peso, seja feito o calculo do seu IMC(IMC = peso/(altura * altura)) e seja exibida a mensagem de acordo com o resultado:
   - Se for menor ou igual a 18,5 "Abaixo do peso";
   - se for entre 18,6 e 24,9 "Peso ideal";
   - Se for entre 25,0 e 29,9 "Levemente acima do peso";
   - Se for entre 30,0 e 34,9 "Obesidade Grau I";
   - Se for entre 35,0 e 39,9 "Obesidade Grau II (Severa)";
   - Se for maior ou igual a 40,0 "Obesidade III (Mórbida)";

3. Escreva um código que o usuário entre com um primeiro número, um segundo número maior que o primeiro e escolhe entre a opção par e impar, com isso o código deve informar todos os números pares ou ímpares (de acordo com a seleção inicial) no intervalo de números informados, incluindo os números informados e em ordem decrescente;

```
import java.util.Scanner;

   public class Main{

       public static void main(String[] args) {
           Scanner sc = new Scanner(System.in);

              System.out.print("Digite o primeiro número: ");
              int number1 = sc.nextInt();
      
              int number2;
              do{
                  System.out.print("Digite o segundo número (maior que o primeiro número): ");
                  number2 = sc.nextInt();
      
                  if(number2 <= number1){
                      System.out.println("O segundo número deve ser MAIOR que o primeiro.");
                  }
              }while (number2 <= number1);
      
              int op;
              do{
                  System.out.println("\nEscolha qual opção de número:\n1 - Par\n2 - Ímpar\nOpção:");
                  op = sc.nextInt();
                  if(op != 1 && op != 2){
                      System.out.println("Opção inválida. Escolha 1 ou 2.");
                  }
              }while (op != 1 && op != 2);
              
              switch(op){
                  case 1 -> System.out.println("\nVocê escolheu os números pares");
                  case 2 -> System.out.println("\nVocê escolheu os números ímpares");
              }
      
              if(op == 1){
                  if (number2 % 2 == 0){
                      for (int i = number2; i >= number1; i -= 2){
                          System.out.println(i);
                      }
                  } else {
                      for (int i = number2 - 1; i >= number1; i -= 2){
                          System.out.println(i);
                      }
                  }
              } else {
                  if (number2 % 2 == 0){
                      for (int i = number2 - 1 ; i >= number1; i -= 2){
                          System.out.println(i);
                      }
                  } else {
                      for (int i = number2; i >= number1; i -= 2){
                          System.out.println(i);
                      }
                  }
              }
              sc.close();
          }
      }

4. Escreva um código onde o usuário informa um número inicial, posteriormente irá informar outros N números, a execução do código irá continuar até que o número informado dividido pelo primeiro número tenha resto diferente de  0 na divisão, números menores que o primeiro número devem ser ignorados
