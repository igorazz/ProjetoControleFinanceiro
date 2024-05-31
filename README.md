# ProjetoControleFinanceiro

Este repositório/Exercício feito em contém um programa em C para controle de receitas e despesas de uma empresa comercial com 10 projetos. O programa permite a entrada e saída de recursos financeiros para cada projeto, classificando-os como receitas ou despesas. As receitas são somadas ao saldo do projeto e as despesas são subtraídas. O programa finaliza quando o usuário insere o código do projeto igual a -1 e, ao final, exibe o saldo final de cada projeto.

//*Uma empresa comercial possui um programa para controle das receitas e despesas em seus 10 projetos. Os projetos são numerados de 0 até 9. Faça um programa C que controle a entrada e saída de recursos dos projetos. O programa deverá ler um conjunto de informações contendo: Número do projeto, valor, tipo despesa ("R" - Receita e "D" - Despesa). O programa termina quando o valor do código do projeto for igual a -1. Sabe-se que Receita deve ser somada ao saldo do projeto e despesa subtraída do saldo do projeto. Ao final do programa, imprirmir o saldo final de cada projeto.*//

/**Dica usar uma estrutura do tipo vetor para controlar os saldos dos projetos. Usar o conceito de struct para agrupar as informações lidas.*/



#include <stdio.h>
#include <stdlib.h>

int main () {
    float projetos [10];
    int i;
    struct 
    {
      int numero;
      float valor;
      char tipo;
    } boleto;

    for (i=0; i < 10; i++){
    projetos[i] = 0.0;
  }
    
printf("\n\n Digite o codigo do projeto: ");
  scanf("%d", &boleto.numero);
  while (boleto.numero != -1) {
   printf("\n\n Digite o Valor : ");
   scanf("%f", &boleto.valor);
   printf("\n\n Digite o tipo de transacao (R ou D): ");
   getchar();//limpar o teclado do Enter anterior
   scanf("%c", &boleto.tipo);

    if (boleto.tipo == 'R' || boleto.tipo == 'r') {
      projetos[boleto.numero] = projetos[boleto.numero] + boleto.valor;
   }
   else {
    if (boleto.tipo == 'D' || boleto.tipo == 'd') {
      projetos[boleto.numero] = projetos[boleto.numero] - boleto.valor;
    }
    else {
      printf("Tipo Invalido !!");
    }
   }
   printf("\n\n Digite o codigo do projeto: ");
   scanf("%d", &boleto.numero);
  }
  for (i=0; i < 10; i++){
    printf("\n Saldo do projeto %d = %f",i, projetos[i]);
  }
}
