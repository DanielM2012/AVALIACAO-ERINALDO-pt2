1- Escreva um programa em C que solicite ao usuário o valor inicial de um
investimento, a taxa de juros anual (em porcentagem) e o número de anos que o
dinheiro será investido. O programa deve calcular o valor final do investimento ao
final de cada ano, aplicando os juros compostos, e mostrar uma tabela com o valor
acumulado ano a ano.

#include <stdio.h>
#include <math.h>

int main() {
double valor_inicial, taxa_juros, valor_final;
int anos;

printf("Digite o valor inicial do investimento: ");
scanf("%lf", &valor_inicial);

printf("Digite a taxa de juros anual: ");
scanf("%lf", &taxa_juros);

printf("Digite o número de anos: ");
scanf("%d", &anos);

printf("\nAno\tValor Acumulado\n");
printf("-----------------------\n");
for (int i = 1; i <= anos; i++) {

    valor_final = valor_inicial * pow((1 + taxa_juros / 100), i);


    printf("%d\t%.2f\n", i, valor_final);
}

return 0;
}
