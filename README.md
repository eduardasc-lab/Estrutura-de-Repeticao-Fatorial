# Estrutura-de-Repeticao-Fatorial
##CÓDIGO

#include <stdio.h>

//Atividade de fatorial\
int main(){\
  int f; //fatorial que eu quero\
  long long fatorial = 1; //serve para números inteiros com grande capacidade como 20!\
  printf("Você deseja saber o fatorial de qual número? ");\
  scanf("%u", &f); //%u serve para responder apenas à números positivos\
  //condição if para cravar uma regra dos fatoriais\
  if(f==0){\
      fatorial=1;\
  //se não, executa o comportamento típico dos fatoriais\
  }else{\
  //a contagem do multiplicador começa por 1, e continua até que o mesmo seja igual ao fatorial solicitado\
      for(int i=1; i<=f; i++){\
           fatorial *=i; // multiplica sucessivamente a cada execução de if else até que a condição seja atendida\
      }\
  }\
  printf("%u! = %llu\n", f, fatorial); //%ll formata long long\
  //condição para dar erro ao solicitar número negativo\
  if(f<0){\
      return 1;\
  }\
  //só aceito até 20!, acima disso é erro\
  if(f>20){\
       return 1;\
  }\
   return 0;\
}
