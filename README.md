# Trabalho de Estudo Dirigido - Faculdade Única

Nesse trabalho foi solicitado para que fosse desenvolvido um algoritmo em C, que fizesse a leitura do nome e do peso de 5 pessoas, e que após isso retornasse na a tela a média aritmética dos pesos e também retorne quantas pessoas estão com o peso acima do peso médio e seus respectivos nomes.

    ```bash
    #include <stdio.h>

    int main() {
    // Informações do aluno
    /*
    Curso: Tecnólogo de Sistemas de Telecomunicações
    Disciplina: Algorítmos e Programação I
    Tutor: Karina Luiza Silva Teixeira
    Aluno: Jefferson Gomes Garcia
    */

    // Declaração das variáveis
    char nome[5][50];  // Vetor de strings para armazenar os nomes
    float peso[5];      // Vetor para armazenar os pesos
    float soma = 0, media;
    int acimaMedia = 0;

    // Leitura do nome e peso de 5 pessoas
    for (int i = 0; i < 5; i++) {
        printf("Digite o nome da pessoa %d: ", i+1);
        scanf("%s", nome[i]);  // Lê o nome da pessoa
        printf("Digite o peso de %s (em kg): ", nome[i]);
        scanf("%f", &peso[i]); // Lê o peso da pessoa
        soma += peso[i];       // Soma os pesos para cálculo da média
    }

    // Calculando a média dos pesos
    media = soma / 5;

    // Contando quantas pessoas estão acima da média
    printf("\nA média dos pesos é: %.2f\n", media);
    printf("\n");

    // Exibindo quantas pessoas estão acima da média e seus nomes
    for (int i = 0; i < 5; i++) {
        if (peso[i] > media) {
            acimaMedia++;  // Contador de pessoas acima da média
        }
    }

    // Imprime o número de pessoas acima da média
    printf("%d pessoa(s) estão com o peso acima da média.\n", acimaMedia);
    printf("As pessoas que possuem os pesos acima da média são:\n");

    // Exibindo os nomes das pessoas com peso acima da média
    for (int i = 0; i < 5; i++) {
        if (peso[i] > media) {
            printf("%s\n", nome[i]); // Mostra o nome das pessoas acima da média
        }
    }

    return 0;
    }

    ```
