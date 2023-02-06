# jogo-numero-secreto-em-C-com-for


#include <stdio.h>
#include <stdlib.h>
#define NUMERO_DE_TENTATIVAS 3
int main()
{

    int NumeroSecreto = 42;

    int Chute;

    printf("-------------------------------------------\n");
    printf("bem vindo ao jogo adivinhe o numero secreto\n");
     printf("-------------------------------------------\n");
     printf("digite um numero que voce acha que eh o numero secreto. voce tem 3 tentativas. boa sorte!\n\n");
    //for(declara quanto vale o valor inicial; condiciona até onde esse valor vai; executa o codigo )
    for(int i = 1; i <= NUMERO_DE_TENTATIVAS; i++)
    {
        printf("tentativa %d de %d\n", i, NUMERO_DE_TENTATIVAS);
        printf("qual seu chute?\n");
        scanf("%d", &Chute);
        printf("seu chute foi %d\n\n", Chute);

        if(Chute < 0)
        {
            printf("voce nao pode chutar números negativos\n\n");
            i--; //não vai contar como tentativa
            continue; //faz o for continuar.
        }


        else if(Chute == 42)
        {

            printf("parabens, voce acertou o numero secreto\n\n");
            //break serve para parar o codigo. ex: se eu acertar o codigo de primeira, o jogo termina.
            break;
        }



        else
        {

            if(Chute > NumeroSecreto)
            {
                printf("o numero escolhido foi mais alto, tente um menor.\n\n");
            }
            else
            {
                printf("o numero escolhido foi menor, tente um  maior.\n\n");
            }

        }
    }
    printf("fim de jogo.");
}

