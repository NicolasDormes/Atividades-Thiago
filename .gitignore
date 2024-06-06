#include <stdio.h>
#include <string.h>

#define MAX_ITEMS 100
#define MAX_NAME_LENGTH 50

typedef struct {
int id;
char nome[MAX_NAME_LENGTH];
float unitario;
int qtde;
float total_item;
} Item;

int main() {
Item items[MAX_ITEMS];
int num_items;
int i, j;
int id;
float total_final = 0.0;

// Solicitar ao usuário o número de itens que ele deseja inserir
printf("Quantos itens deseja inserir? ");
scanf("%d", &num_items);

for (i = 0; i < num_items; i++) {
// Solicitar e armazenar os campos necessários
printf("Insira o codigo do item %d: ", i + 1);
scanf("%d", &id);

// Verificar se o código já foi inserido
for (j = 0; j < i; j++) {
if (items[j].id == id) {
printf("Codigo ja inserido. Insira um codigo diferente.\n");
i--; // Decrementar o contador para repetir a iteração
continue;
}
}
items[i].id = id;

printf("Insira o nome do item %d: ", i + 1);
scanf(" %[^\n]", items[i].nome);

printf("Insira o valor unitario do item %d: ", i + 1);
scanf("%f", &items[i].unitario);

printf("Insira a quantidade do item %d: ", i + 1);
scanf("%d", &items[i].qtde);

items[i].total_item = items[i].unitario * items[i].qtde;
total_final += items[i].total_item;
}

// Imprimir a lista dos itens com seus respectivos preços
printf("\nCODIGO\t\tNOME\t\t\tQTDE\tUNIT\tTOTAL\n");
for (i = 0; i < num_items; i++) {
printf("%05d\t\t%-20s\t%d\t%.2f\t%.2f\n", items[i].id, items[i].nome, items[i].qtde, items[i].unitario, items[i].total_item);
}

// Calcular e imprimir o total dos preços de todos os itens
printf("\nTOTAL FINAL\t%.2f\n", total_final);

return 0;
}
