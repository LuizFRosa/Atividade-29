# Atividade-29

#include <stdio.h>
#include <stdlib.h>
#include <ctype.h> // Para a função tolower

int main() {
    // Definir uma string para armazenar a entrada do usuário
    char str[100];
    int i, vogais = 0;
    
    // Solicitar ao usuário a entrada da string
    printf("Digite uma string: ");
    fgets(str, sizeof(str), stdin); // fgets é mais seguro do que gets

    // Contar o número de vogais
    for (i = 0; str[i] != '\0'; i++) {
        char ch = tolower(str[i]); // Converte o caractere para minúsculo

        // Verificar se o caractere é uma vogal
        if (ch == 'a' || ch == 'e' || ch == 'i' || ch == 'o' || ch == 'u') {
            vogais++;
        }
    }

    // Exibir o número de vogais
    printf("Número de vogais na string: %d\n", vogais);

    return 0;
}
