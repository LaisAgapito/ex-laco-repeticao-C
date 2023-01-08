# ex-laco-repeticao-C
// Exercício de laços de repetição / Programa para calculo de notas/média de alunos 

#include <stdio.h>

int main()
{
    float trabalho1; 
    float trabalho2; 
    float prova;
    int qtdAluno;
    int aluno;
    float mediaAluno; 
    float mediaTurma;
    float acumuloNotas = 0;
    
    printf("Digite a quantidade de alunos:_ ");
    scanf ("%d", &qtdAluno);
    
    for (aluno = 1; aluno <= qtdAluno; aluno++) {
        do {
            printf("\n Digite a nota do primeiro trabalho:_");
            scanf ("%f", &trabalho1);
        }while (trabalho1 < 0 || trabalho1 > 1.0);
        
        do {
             printf("\n Digite a nota do segundo trabalho:_");
            scanf ("%f", &trabalho2);
        }while (trabalho2 < 0 || trabalho2 > 1.0);
        
        do {
             printf("\n Digite a nota da prova:_");
            scanf ("%f", &prova);
        }while (prova < 0 || prova > 3.0);
        
        mediaAluno = trabalho1 + trabalho2 + prova;
        printf("\n A média desse aluno é de %2.f \n", mediaAluno);
        
        mediaTurma = mediaTurma + mediaAluno;
    }
    
    mediaTurma = mediaTurma / qtdAluno;
    printf("\n A média da turma é de %2.f", mediaTurma);
    
    if (mediaTurma >= 3.0) {
        printf("\n A turma foi bem!");
    } else {
        printf("\n A turma não foi muito bem.");
    }
    
    

    return 0;
}


