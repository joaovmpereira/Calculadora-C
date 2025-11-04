#include <stdio.h>

// Funções para cada operação
float soma(float a, float b) {
    return a + b;
}

float subtracao(float a, float b) {
    return a - b;
}

float multiplicacao(float a, float b) {
    return a * b;
}

float divisao(float a, float b) {
    if (b != 0) {
        return a / b;
    } else {
        printf("Erro! Divisao por zero.\n");
        return 0;
    }
}

int main() {
    float num1, num2;
    int operacao;

    // Exibe as opções de operação
    printf("Selecione a operacao:\n");
    printf("1. Soma\n");
    printf("2. Subtracao\n");
    printf("3. Multiplicacao\n");
    printf("4. Divisao\n");
    printf("Escolha a operacao (1/2/3/4): ");
    scanf("%d", &operacao);

    // Solicita os números ao usuário
    printf("Digite o primeiro numero: ");
    scanf("%f", &num1);
    printf("Digite o segundo numero: ");
    scanf("%f", &num2);

    // Realiza a operação selecionada
    switch(operacao) {
        case 1:
            printf("%.2f + %.2f = %.2f\n", num1, num2, soma(num1, num2));
            break;
        case 2:
            printf("%.2f - %.2f = %.2f\n", num1, num2, subtracao(num1, num2));
            break;
        case 3:
            printf("%.2f * %.2f = %.2f\n", num1, num2, multiplicacao(num1, num2));
            break;
        case 4:
            printf("%.2f / %.2f = %.2f\n", num1, num2, divisao(num1, num2));
            break;
        default:
            printf("Operacao invalida!\n");
    }

    return 0;
}
