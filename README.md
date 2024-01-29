# calculadora
#include <stdio.h>

int main() {
    char operador;
    double num1, num2, resultado;
    // Solicitar operação ao usuário
    printf("Digite a operacao (+, -, *, /): ");
    scanf("%c", &operador);
    // Solicitar dois números ao usuário
    printf("Digite o primeiro numero: ");
    scanf("%lf", &num1);

   printf("Digite o segundo numero: ");
    scanf("%lf", &num2);
    // Realizar a operação escolhida
    switch (operador) {
        case '+':
            resultado = num1 + num2;
            break;
        case '-':
            resultado = num1 - num2;
            break;
        case '*':
            resultado = num1 * num2;
            break;
        case '/':
            // Verificar se o divisor não é zero
            if (num2 != 0) {
                resultado = num1 / num2;
            } else {
                printf("Erro: Divisao por zero!\n");
                return 1;  // Encerrar o programa com código de erro
            }
            break;
        default:
            printf("Erro: Operacao invalida!\n");
            return 1;  // Encerrar o programa com código de erro
    }

  // Exibir o resultado
    printf("Resultado: %.2lf\n", resultado);

   return 0;
}

