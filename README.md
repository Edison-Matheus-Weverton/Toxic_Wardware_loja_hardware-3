# Toxic_Wardware_loja_hardware-3
#include <stdio.h>
#include <stdlib.h>
#include <string.h>
#include <windows.h>
#include <locale.h>
#define estcoo 523
#define estcpu 811
#define estmram 675
#define estpdv 731
#define estpm 800

typedef struct{
    float cep;
    float casa;
    char rua[100];
    char bairro[100];
    char cidade[100];
    char estado[100];
    float regiao;
}endereco;
void compra(float preco,int un,float carteira) //função para realizar a compra dos produtos
{   float ttl=0,precoUN;
    precoUN=preco*un;
    if(precoUN>carteira){printf(" DINHEIRO INSUFICIENTE!!!");}
    else printf(" COMPRA REALIZADA COM SUCESSO!!!\n\n");
    ttl=ttl+precoUN;
}
float taxa(float valorr,int forma){
    float result;
    if(forma == 1){
        result = (valorr/100)*15;
    }
    else if(forma == 2){
        result = (valorr/100)*10;
    }
    return (result);
}

int main()
{

    setlocale(LC_ALL,"");
    int resp,resp2,cad=0,u;
    float cart=0,pr=0;
    char nome[100],sn;
    endereco endereco;

    printf("\n\n================================================================================\n\n");
    printf("\t\t\t\tToxic Hardwares\n\n");
    printf("\n================================================================================\n\n");

    printf(" Toxic hardwares é uma loja voltada para a venda de peças de informática que atende a qualquer pessoa do país virtualmente, o frete varia de acordo com sua região e os produtos são sempre bem embalados visando a segurança do produto.\n");
    Sleep(2000);
    printf("\n Seja bem vindo!\n\n");
    system("pause");
    system("cls");

    do{printf("\n\n================================================================================\n\n");
    printf("\t\t\t\tToxic Hardwares\n\n");
    printf("\n================================================================================\n\n");
    printf("\n Selecione o que deseja ver agora\n\n 1= Cadastro\n 2= Produtos\n 3= Salário dos funcionários\n 4= Estoque\n 5= Fornecedores\n 6 = Despesas\n 7 = Vendas\n 8 = Marcas\n 9= Tamanho\n 10= Consultar Valor dos Fretes\n 11 = Formas de pagamento e Taxas de pagamento\n 12 = Sair");
    printf("\n\n Digite o número: ");
    scanf("%d",&resp);

    switch (resp)
    {case 1:  system("cls");

        if(cad==0){
         printf(" Insira seu nome: ");
         fflush(stdin);
         gets (nome);
         fflush(stdin);
         printf("\n Insira o saldo em seu cartão: R$ ");
         scanf("%f",&cart);
         system("cls");
         printf(" OK, usuário cadastrado com sucesso\n\n\n");

         cad=1;
         }
         else {
            printf(" Ops, você já está cadastrado!\n\n\n");
         }
        system("pause");
        system("cls");
    break;

    case 2: do {
        system("cls");
        printf("\n O dinheiro atual na sua carteira é de R$%.2f\n\n",cart);
        printf(" 1-> Cooler\n\n");
        printf(" 2-> CPU\n\n");
        printf(" 3-> Memória RAM\n\n");
        printf(" 4-> Placa de vídeo\n\n");
        printf(" 5-> Placa-mãe\n\n");
        printf(" 6-> Voltar\n\n");
        printf("\n\n Digite o número: ");
        scanf("%d",&resp2);

        switch (resp2){
        case 1: system("cls");
            printf(" O preço do Cooler é R$31.43\n Deseja comprar (s/n)? ");
            fflush(stdin);
            scanf("%c",&sn);
            fflush(stdin);
            if(sn=='s')
            {printf("\n\n Quantas unidades? ");
            scanf("%d",&u);
            pr=pr+31.43;
            compra(pr,u,cart);
            pr=0;}
            if((sn!='s')&&(sn!='n')){printf("\n\n\n VALOR INVÁLIDO!!!\n\n");}
            system("pause");
            system("cls");
        break;

        case 2: system("cls");
            printf(" O preço do CPU é R$941.06\n Deseja comprar (s/n)? ");
            fflush(stdin);
            scanf("%c",&sn);
            fflush(stdin);
            if(sn=='s')
            {printf("\n\n Quantas unidades? ");
            scanf("%d",&u);
            pr=pr+941.06;
            compra(pr,u,cart);
            pr=0;}
            if((sn!='s')&&(sn!='n')){printf("\n\n VALOR INVÁLIDO!!!\n\n");}
            system("pause");
            system("cls");
        break;

        case 3: system("cls");
            printf(" O preço do Memória RAM é R$435.18\n Deseja comprar (s/n)? ");
            fflush(stdin);
            scanf("%c",&sn);
            fflush(stdin);
            if(sn=='s')
            {printf("\n\n Quantas unidades? ");
            scanf("%d",&u);
            pr=pr+435.18;
            compra(pr,u,cart);
            pr=0;}
            if((sn!='s')&&(sn!='n')){printf("\n\n VALOR INVÁLIDO!!!\n\n");}
            system("pause");
            system("cls");
            break;

        case 4: system("cls");
            printf(" O preço do Placa de vídeo é R$10588.12\n Deseja comprar (s/n)? ");
            fflush(stdin);
            scanf("%c",&sn);
            fflush(stdin);
            if(sn=='s')
            {printf("\n\n Quantas unidades? ");
            scanf("%d",&u);
            pr=pr+10588.12;
            compra(pr,u,cart);
            pr=0;}
            if((sn!='s')&&(sn!='n')){printf("\n\n VALOR INVÁLIDO!!!\n\n");}
            system("pause");
            system("cls");
        break;

        case 5: system("cls");
            printf(" O preço do Placa-mãe é R$682.24\n Deseja comprar (s/n)? ");
            fflush(stdin);
            scanf("%c",&sn);
            fflush(stdin);
            if(sn=='s')
            {printf("\n\n Quantas unidades? ");
            scanf("%d",&u);
            pr=pr+682.24;
            compra(pr,u,cart);
            pr=0;}
            if((sn!='s')&&(sn!='n')){printf("\n\n VALOR INVÁLIDO!!!\n\n");}
            system("pause");
            system("cls");
        break;

        case 6:system("cls");
        break;
        default: system("cls");
        printf(" Por favor, insira um número válido!\n\n\n");
        system("pause");
        system("cls");
        break;
        }
    }while(resp2!=6);
    break;

    case 3: system("cls");
    printf("\n O salário do Cleyton da Silva é R$1.045,00\n O salário da Roberta Fonseca é R$1.045,00\n O salário do Felipe Dias Lima é R$1.045,00\n O salário do Freddie Aragão Lanna é R$2.435,00\n O salário da Carmen é R$3.431,00\n O salário do Bartolomeu Marazzo Frota é R$4.567,00\n\n");
    system("pause");
    system("cls");
    break;

    case 4: system("cls");
    printf(" Temos em estoque:\n %d Coolers\n %d CPUs\n %d Memórias RAM\n %d Placas de vídeo\n %d Placas-mãe\n\n",estcoo, estcpu,estmram,estpdv,estpm);
    system("pause");
    system("cls");
    break;

    case 5: system("cls");
    printf("\n Kabum - https://m.kabum.com.br/\n");
    printf("\n Terabyteshop - https://www.terabyteshop.com.br/\n");
    printf("\n Ednaldo Pereira tel: (11)99935-2764\n");
    system("pause");
    system("cls");
    break;

    case 6: system("cls");
    printf("\nEnergia para manter o sistema ativo = R$1.000 -- 3.000");
    printf("\nGasto com funcionarios = R$13.568,00");
    printf("\nGasto com produtos = R$0 -- R$15.000");
    printf("\nMaquinário e serviços = R$12.500,00");
    printf("\nCustos Gerais = R$20.000 -- R$100.000\n\n");
    system("pause");
    system("cls");
    break;


    case 7: system("cls");
    printf("\nAtualmente nossa empresa não possui o número exato de vendas, mas acreditamos que seja por volta de 36,858 mil produtos\n\n");
    system("pause");
    system("cls");
    break;


    case 8: system("cls");
    printf("\nMarcas dos Coolers = GAMEMAX e EVGA");
    printf("\nMarca das Memorias Ram = CORSAIR, PCCOOLER e TRIDENTZ");
    printf("\nMarcas das Placas de Vídeo = EVGA, GIGABYTE, PNY e ASUS");
    printf("\nMarcas das Placas-Mãe = ASROCK, GIGABYTE e ASUS\n\n");
    system("pause");
    system("cls");
    break;


    case 9: system("cls");
    printf("\nTamanho dos Coolers = 135 x 80 x 154.5mm");
    printf("\nTamanho das Memorias Ram = 5cm x 0.5cm");
    printf("\nTamanho das Placas de Vídeo = - Altura: 111.15 mm Comprimento: 285.37 mm Largura: 2.2 slots");
    printf("\nTamanho das Placas-Mãe = Modelo mATX 24.4 cm por 24 cm (9.6 polegadas por 9.5 polegadas)\n\n");
    system("pause");
    system("cls");
    break;

    case 10: system("cls");
    printf("\nINFORME SEUS DADOS PARA QUE POSSAMOS CALCULAR SEU FRETE:");
    printf("\n");
    gets(endereco.cidade);
    printf("CIDADE: ");
    gets(endereco.cidade);
    printf("BAIRRO: ");
    gets(endereco.bairro);
    printf("Numero da casa: ");
    scanf("%f", &endereco.casa);
    printf("CEP: ");
    scanf("%f", &endereco.cep);
    printf("");
    gets(endereco.estado);
    printf("Estado: ");
    gets(endereco.estado);
    printf("REGIAO(1- NORTE, 2- SUL, 3- NORDESTE, 4- SUDESTE, 5- CENTRO OESTE: ");
    scanf("%f", &endereco.regiao);
    if(endereco.regiao == 1){
        printf("\n\nO VALOR DO FRETE EH: 67,89 VIA SEDEX\n\n");
    }
    else if(endereco.regiao == 2){
        printf("\n\nO VALOR DO FRETE EH: 56,99 VIA SEDEX\n\n");
    }
    else if(endereco.regiao == 3){
        printf("\n\nO VALOR DO FRETE EH: 98,90 VIA SEDEX\n\n");
    }
    else if(endereco.regiao == 4){
        printf("\n\nO VALOR DO FRETE EH: 54,40 VIA SEDEX\n\n");
    }
    else if(endereco.regiao == 5){
        printf("\n\nO VALOR DO FRETE EH: 127,54 VIA SEDEX\n\n");
    }
    else{
        printf("\n\nRegiao invalida, digite um valor valido\n\n");
    }
    system("pause");
    system("cls");
    break;

    case 11: system("cls");
    char u;
    int f;
    float v, td;
    printf("\nCartão de Credito = 15 por cento de taxa em até 12x");
    printf("\nBoleto Bancario = 10 por cento de Desconto");
    printf("\n\nCalcular alguma taxa e ou desconto? s/n: ");
    scanf("%s", &u);
    if(u=='s'){
        printf("\nSELECIONE A FORMA DE PAGAMENTO:\n");
        printf("1- cartao\n2-Boleto\n\n");
        scanf("%d", &f);
        printf("Digite o valor a ser pago: ");
        scanf("%f", &v);
        if(f==1){
            td = taxa(v, f);
            printf("Voce ira pagar de taxa %.2f, sendo assim o valor total a ser pago eh: %.2f\n\n", td, td+v);
        }
        else if(f==2){
            td = taxa(v, f);
            printf("Voce ira receber de desconto %.2f sendo assim o valor total a ser pago eh: %.2f \n\n", td, v-td);
        }
        else{
            printf("VALOR INVALIDO");
        }


    }
    else {
        printf("OK!");
    }
    system("pause");
    system("cls");
    break;


    case 12: system("cls");
    break;

    default: system("cls");
    printf(" Por favor, insira um número válido!\n\n\n");
    system("pause");
    system("cls");
    break;}} while (resp!=12);

    printf(" Obrigado pela escolha!\n\n Volte sempre!\n");
    return 0;
}
