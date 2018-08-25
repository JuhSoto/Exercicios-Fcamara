# Exercicios-Fcamara

#include<stdio.h>
#include<stdlib.h>
#define ex05
/*1) Um funcionário de uma empresa recebe, anualmente, aumento salarial.
Sabe-se que:
Esse funcionário foi contratado em 2005 com salário inicial de R$ 1.000,00;
Em 2006 ele recebeu aumento de 1,5% sobre seu salário inicial; e
A partir de 2007, os aumentos salariais sempre corresponderam ao dobro
do percentual do ano anterior.
Faça um algoritmo que determine o salário atual deste funcionário.*/
#ifdef ex01


main()
{
    int anoatual;
    float i,salario,aumento,novosalario,porcSala;
    printf("Digite o ano");
    scanf("%d",&anoatual);
    salario =1000;
    aumento = 1.5;
    porcSala=1000/aumento;
    novosalario = salario;

    for(i=2006; i<=anoatual; i++)
    {

        porcSala = (novosalario+aumento)*2;
        novosalario = novosalario+porcSala;
    }
    printf("O salario atual eh:%f",novosalario);

}
#endif // ex01


#ifdef ex02

/*Elabore um algoritmo para mostrar os números primos existentes em um
intervalo.
O usuário deverá fornecer os valores inicial (inicial > 0) e final (inicial <
final) e os números primos existentes no intervalo ([inicial, final]) devem
ser separados por um espaço em branco

Exemplo:
Entrada: 2 13
Saída: 2 3 5 7 11 13*/

main()
{

    int n1,n2,p,div,i,x,j;
    do
    {
        printf("Entre com o primeiro numero primo da sequencia");
        scanf("%d",&n1);
    }
    while(n1<0);
    do
    {
        printf("Entre com o ultimo numero primo da sequencia");
        scanf("%d",&n2);
    }
    while(n2<0);

    for (i = n1; i <= n2; i++)
    {
        if(i==0 || i==1)
        {
            p=0;
        }
        else
        {
            p=1;
            for(j = 2; j < i; j++)
            {
                if (i % j == 0)
                {
                    p = 0;
                }
            }
        }
        if (p == 1)
        {
            printf("%i ", i);
        }
    }
}

#endif // ex02
/*Receba o número de horas trabalhadas por uma pessoa e o valor do
salário mínimo e mostre o salário a receber baseado nas seguintes regras:
A hora trabalhada equivale a 10% do salário mínimo informado;
O salário bruto é dado pelo número de horas trabalhadas multiplicado pelo
valor de cada hora;
O imposto pago é de 3%.
O salário a receber é equivalente ao salário bruto subtraído do imposto.*/
#ifdef ex03

main()
{
    float salario,horas,imposto,porcento;

    printf("Insira o valor do salario minimo\n");
    scanf("%f",&salario);
    printf("Insira quantidade de horas trabalhadas\n");
    scanf("%f",&horas);

    salario=salario*0.10;
    imposto = salario*0.03;
    salario=(horas*salario)-imposto;
    printf("O salario a receber eh: %f\n",salario);

}

#endif // ex03
/*Faça um programa para uma loja de tintas. O programa deverá pedir o
tamanho em metros quadrados da área a ser pintada. Considere que a
cobertura da tinta é de 1 litro para cada 3 metros quadrados e que a tinta é
vendida em latas de 18 litros, que custam R$ 80,00. Informe ao usuário a
quantidades de latas de tinta a serem compradas e o preço total.*/
#ifdef ex04

main()
{

    int tam,litro,latas,capacidade,preco;
    printf("Digite o tamanho em metros da area");
    scanf("%d",&tam);

    litro = tam/3;
    capacidade=18;
    preco = 80.00;

    latas = litro/capacidade;
    preco = latas*preco;
    if (tam < 54)
    {
        latas = 1;
        preco = 80.00;
    }
    printf("Numero de latas necessarias:%d \n Preco:%d",latas,preco);


}
#endif // ex04
Crie uma classe para implementar uma conta corrente. A classe deve
possuir os seguintes atributos:
número da conta, nome do correntista e
saldo. Os métodos são os seguintes:
alterarNome, depósito e saque;
No construtor, saldo é opcional, com valor default zero e os demais atributos
    são obrigatórios.
#ifdef ex05
    main()
{
    public class conta corrente
    {
        private int conta;
        private string nome;
        private float saldo;
    }
}
#endif // ex05
