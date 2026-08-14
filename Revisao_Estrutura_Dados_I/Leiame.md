# Exercícios em Aula — Linguagem C

Este repositório contém exercícios desenvolvidos durante as aulas de programação em **linguagem C**.

Os exercícios trabalham conceitos básicos de programação, como:

- Declaração de variáveis;
- Tipos de dados `int`, `float` e `char`;
- Entrada de dados com `scanf()`;
- Saída de dados com `printf()`;
- Operadores matemáticos;
- Estruturas condicionais;
- Estrutura `switch`;
- Estrutura de repetição `for`.

---

# Exercício 1 — Cálculo da Média e Situação do Estudante

## Conceitos utilizados

### Tipo de dado

- `float` → utilizado para armazenar as notas, o ponto extra e a média final.

### Estruturas de controle

- `if`
- `else if`
- `else`

### Operadores utilizados

- `+` → soma;
- `/` → divisão;
- `>=` → maior ou igual;
- `<=` → menor ou igual;
- `&&` → operador lógico "E".

## Código

```c
#include <stdio.h>

int main() {

    // Variáveis do tipo float são utilizadas
    // para armazenar valores que podem possuir casas decimais.
    float nota1, nota2, pontoExtra;
    float mediaFinal;

    // Solicita a primeira nota ao usuário
    printf("Digite a primeira nota: ");
    scanf("%f", &nota1);

    // Solicita a segunda nota ao usuário
    printf("Digite a segunda nota: ");
    scanf("%f", &nota2);

    // Solicita o ponto extra
    printf("Digite o ponto extra: ");
    scanf("%f", &pontoExtra);

    // Calcula a média das duas notas
    // e adiciona o ponto extra.
    mediaFinal = ((nota1 + nota2) / 2) + pontoExtra;

    // Exibe a nota final com duas casas decimais
    printf("Nota final: %.2f\n", mediaFinal);

    // Verifica a situação do estudante.
    // Se a média for maior ou igual a 6,
    // o estudante está aprovado.
    if (mediaFinal >= 6.0) {

        printf("Situação: Aprovado\n");

    // Se a média estiver entre 2 e 5.9,
    // o estudante está em recuperação.
    } else if (mediaFinal >= 2.0 && mediaFinal <= 5.9) {

        printf("Situação: Recuperação\n");

    // Caso nenhuma das condições anteriores
    // seja verdadeira, o estudante está reprovado.
    } else {

        printf("Situação: Reprovado\n");
    }

    // Indica que o programa terminou corretamente
    return 0;
}
```

## Resumo

| Item | Utilização |
|---|---|
| Tipo de dado | `float` |
| Estrutura de controle | `if / else if / else` |
| Entrada | `scanf()` |
| Saída | `printf()` |
| Objetivo | Calcular a média e verificar a situação do estudante |

---

# Exercício 2 — Verificação de Vogais

## Conceitos utilizados

### Tipo de dado

- `char` → utilizado para armazenar uma letra.

### Estrutura de controle

- `switch`
- `case`
- `default`

### Comandos utilizados

- `break` → utilizado para encerrar o `case` encontrado.

## Código

```c
#include <stdio.h>

int main() {

    // Variável do tipo char utilizada
    // para armazenar uma letra.
    char letra;

    // Solicita uma letra ao usuário
    printf("Digite uma letra: ");

    // Lê a letra digitada.
    // O espaço antes de %c faz o scanf ignorar
    // espaços e quebras de linha anteriores.
    scanf(" %c", &letra);

    // Verifica o conteúdo da variável "letra"
    // utilizando a estrutura switch.
    switch (letra) {

        // Vogais minúsculas
        case 'a':
        case 'e':
        case 'i':
        case 'o':
        case 'u':

        // Vogais maiúsculas
        case 'A':
        case 'E':
        case 'I':
        case 'O':
        case 'U':

            // Se a letra for uma das opções acima,
            // será considerada uma vogal.
            printf("A letra é uma vogal.\n");

            // Encerra o switch
            break;

        // Caso a letra não corresponda
        // a nenhuma das opções anteriores.
        default:

            printf("A letra é uma consoante.\n");
    }

    // Indica que o programa terminou corretamente
    return 0;
}
```

## Resumo

| Item | Utilização |
|---|---|
| Tipo de dado | `char` |
| Estrutura de controle | `switch` |
| Comandos | `case`, `default`, `break` |
| Entrada | `scanf()` |
| Saída | `printf()` |
| Objetivo | Identificar se a letra é uma vogal |

---

# Exercício 3 — Números Pares de 0 a 100

## Conceitos utilizados

### Tipo de dado

- `int` → utilizado para armazenar números inteiros.

### Estrutura de controle

- `for` → utilizado para realizar a repetição.

## Código

```c
#include <stdio.h>

int main() {

    // Variável do tipo int utilizada
    // como contador do laço.
    int i;

    // O for começa em 0 e continua até 100.
    // A cada repetição, o valor de i aumenta em 2.
    // Dessa forma, apenas números pares são exibidos.
    for (i = 0; i <= 100; i += 2) {

        // Exibe o valor atual de i
        printf("%d\n", i);
    }

    // Indica que o programa terminou corretamente
    return 0;
}
```

## Resumo

| Item | Utilização |
|---|---|
| Tipo de dado | `int` |
| Estrutura de controle | `for` |
| Entrada | Não possui |
| Saída | `printf()` |
| Objetivo | Exibir os números pares de 0 até 100 |

---

# Resumo Geral

| Exercício | Tipo de dado | Estrutura de controle | Objetivo |
|---|---|---|---|
| **1** | `float` | `if / else if / else` | Calcular a média e verificar a situação |
| **2** | `char` | `switch` | Identificar se uma letra é uma vogal |
| **3** | `int` | `for` | Exibir números pares de 0 até 100 |

---

# O que foi praticado

Durante esses exercícios foram praticados os seguintes conceitos da linguagem C:

- **`int`** → números inteiros;
- **`float`** → números com casas decimais;
- **`char`** → caracteres;
- **`printf()`** → exibição de informações;
- **`scanf()`** → entrada de informações;
- **`if / else if / else`** → tomada de decisões;
- **`switch / case / default`** → seleção de opções;
- **`for`** → repetição de comandos;
- **Operadores matemáticos e lógicos**.

> **Observação:** `int`, `float` e `char` são **tipos de dados**. Já `if`, `switch` e `for` são **estruturas de controle de fluxo**. Neste conjunto de exercícios, foram trabalhados os dois conceitos.

---

---

## Autor

Projeto desenvolvido durante as aulas de programação em **linguagem C**.
