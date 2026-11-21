
#include <stdio.h>

int menuPagamento() {
    int opcao;
    printf("\nOpcoes de pagamento:\n");
    printf("1 - A vista com 10%% de desconto\n");
    printf("2 - Em duas vezes (preco da etiqueta)\n");
    printf("3 - De 3 ate 10 vezes com 3%% de juros ao mes (somente acima de R$ 100,00)\n");
    printf("Escolha a opcao: ");
    scanf("%d", &opcao);
    return opcao;
}

void aVista(float total) {
    float valor = total - (total * 0.10);
    printf("Valor a vista com desconto: R$ %.2f\n", valor);
}

void emDuasVezes(float total) {
    float parcela = total / 2;
    printf("2 parcelas de R$ %.2f\n", parcela);
    printf("Total: R$ %.2f\n", total);
}

void parcelado(float total) {
    int parcelas, i;
    float valorTotal, parcela;

    if (total <= 100) {
        printf("Essa opcao so vale para compras acima de R$ 100,00\n");
    } else {
        printf("Digite o numero de parcelas (3 a 10): ");
        scanf("%d", &parcelas);

        if (parcelas >= 3 && parcelas <= 10) {
            valorTotal = total;

            for (i = 0; i < parcelas; i++) {
                valorTotal = valorTotal * 1.03;
            }

            parcela = valorTotal / parcelas;

            printf("%d parcelas de R$ %.2f\n", parcelas, parcela);
            printf("Total: R$ %.2f\n", valorTotal);
        } else {
            printf("Numero de parcelas invalido\n");
        }
    }
}

int main() {
    float total;
    int opcao;

    printf("Digite o total gasto pelo cliente: ");
    scanf("%f", &total);

    opcao = menuPagamento();

    if (opcao == 1) {
        aVista(total);
    } else if (opcao == 2) {
        emDuasVezes(total);
    } else if (opcao == 3) {
        parcelado(total);
    } else {
        printf("Opcao invalida\n");
    }

    return 0;
}
