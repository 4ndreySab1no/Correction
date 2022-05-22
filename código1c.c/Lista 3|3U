#include <stdio.h>
#include <stdlib.h>

void intercalacao(int ESQUERDA, int DIREITA, int MEIO, int Vetor[]){
    int vetorA = (MEIO - ESQUERDA) + 1;
    int vetorB = (DIREITA - MEIO);
    int K = ESQUERDA;
    int A[vetorA];
    int B[vetorB];
    int i, j;//contadores auxiliares.

        for (i = 0; i < vetorA; i++){
             A[i] = Vetor[ESQUERDA + 1];
            }
                for (j = 0; j < vetorB; j++){
                    B[j] = Vetor[MEIO + 1 + j];
                }
            i = 0;
            j = 0;
            //os contadores foram zerados, para evitar erros!
                while (i < vetorA && j < vetorB){
                        if (A[i] < B[j]){
                            Vetor[K] = A[i];
                            i++;
                            }
                             else{
                                Vetor[K] = B[j];
                                j++;
                             }

                         K++;                 
                }
                //verifica se o primeiro vetor não chegou até o final!
                while (i < vetorA){
                    Vetor[K] = A[i];
                    i++;
                    K++;
                }
                //Verifica se o Segundo vetor não chegou até o final!
                while (j < vetorB){
                    Vetor[K] = B[j];
                    j++;
                    K++;
                }            
}

void MERGESORT(int INICIO, int FINAL, int VETOR[]){
    //Agora se inicia a "magica" real do MS, que divide o problema em 2, e verifica os elementos apartir do seu meio!
    if (INICIO < FINAL){
        int MEIO = (INICIO + FINAL)/2;
        MERGESORT(INICIO, MEIO, VETOR);
        MERGESORT(MEIO + 1, FINAL, VETOR);
        intercalacao(INICIO, MEIO, FINAL, VETOR);
    }
    
}

int main() {
  int V[10] = {33, 71, 75, 10, 29, 55, 74, 73, 65, 19};
  int i;
  printf("números a serem ordenados:\n");
//exibindo números do vetor
    for ( i = 0; i < 10; i++){
        printf("%4d", V[i]);
    }

    //exibe valores ordenados
    printf("\nnúmeros ordenados:\n");

    MERGESORT(0, 10 - 1, V);

        for (i = 0; i < 10; i++){
            printf("%4d", V[i]);
        }

  system ("pause");
  return 0;
}
