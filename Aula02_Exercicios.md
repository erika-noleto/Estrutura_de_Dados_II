# Exercício 1 
```python
numeros = []

for i in range(10):
    numeros.append(int(input("Digite um número: ")))

soma = sum(numeros)
media = soma / 10

print("Números:", numeros)
print("Soma:", soma)
print("Média:", media)
```

# Exercício 2 

```python
numeros = []

for i in range(10):
    numeros.append(int(input("Digite um número: ")))

maior = max(numeros)
menor = min(numeros)

print("Maior:", maior)
print("Menor:", menor)

print("Posições do maior:")
for i in range(10):
    if numeros[i] == maior:
        print(i)

print("Posições do menor:")
for i in range(10):
    if numeros[i] == menor:
        print(i)
```

# Exercício 3 
```python
numeros = []

for i in range(20):
    numeros.append(int(input("Digite um número: ")))

quantidade = 0
soma = 0

print("Números pares:")

for numero in numeros:
    if numero % 2 == 0:
        print(numero)
        quantidade += 1
        soma += numero

print("Quantidade:", quantidade)
print("Soma:", soma)
```

# Exercício 4 
```python
numeros = []

for i in range(10):
    numeros.append(int(input("Digite um número: ")))

print("Vetor original:", numeros)

inicio = 0
fim = 9

while inicio < fim:
    numeros[inicio], numeros[fim] = numeros[fim], numeros[inicio]
    inicio += 1
    fim -= 1

print("Vetor invertido:", numeros)
```

# Exercício 5 
```python
matriz = []

for i in range(3):
    linha = []

    for j in range(3):
        linha.append(int(input("Digite um número: ")))

    matriz.append(linha)

soma = 0
maior = matriz[0][0]

print("Matriz:")

for i in range(3):
    print(matriz[i])

    for j in range(3):
        soma += matriz[i][j]

        if matriz[i][j] > maior:
            maior = matriz[i][j]

print("Soma:", soma)
print("Maior:", maior)
```

# Exercício 6 

```python
matriz = []

for i in range(4):
    linha = []

    for j in range(4):
        linha.append(int(input("Digite um número: ")))

    matriz.append(linha)

soma = 0

print("Diagonal principal:")

for i in range(4):
    print(matriz[i][i])
    soma += matriz[i][i]

print("Soma:", soma)
```

# Exercício 7 
```python
notas = []

for i in range(4):
    aluno = []

    for j in range(3):
        aluno.append(float(input("Digite a nota: ")))

    notas.append(aluno)

for i in range(4):
    media = sum(notas[i]) / 3
    print("Aluno", i + 1, "média:", media)
```

# Exercício 8 

```python
class Produto:
    def __init__(self, nome, codigo, preco, quantidade):
        self.nome = nome
        self.codigo = codigo
        self.preco = preco
        self.quantidade = quantidade


produtos = []

for i in range(5):
    nome = input("Nome: ")
    codigo = int(input("Código: "))
    preco = float(input("Preço: "))
    quantidade = int(input("Quantidade: "))

    produtos.append(Produto(nome, codigo, preco, quantidade))

maior = produtos[0]

for produto in produtos:
    valor = produto.preco * produto.quantidade

    print(produto.nome, "- Valor em estoque:", valor)

    if valor > maior.preco * maior.quantidade:
        maior = produto

print("Maior valor em estoque:", maior.nome)
```

# Exercício 9 

```python
class Aluno:
    def __init__(self, nome, idade, nota1, nota2, nota3):
        self.nome = nome
        self.idade = idade
        self.nota1 = nota1
        self.nota2 = nota2
        self.nota3 = nota3


alunos = []

for i in range(5):
    nome = input("Nome: ")
    idade = int(input("Idade: "))
    nota1 = float(input("Nota 1: "))
    nota2 = float(input("Nota 2: "))
    nota3 = float(input("Nota 3: "))

    alunos.append(Aluno(nome, idade, nota1, nota2, nota3))

aprovados = 0
reprovados = 0
maior_media = 0
melhor = ""

for aluno in alunos:
    media = (aluno.nota1 + aluno.nota2 + aluno.nota3) / 3

    print(aluno.nome, "- Média:", media)

    if media >= 7:
        print("Aprovado")
        aprovados += 1
    else:
        print("Reprovado")
        reprovados += 1

    if media > maior_media:
        maior_media = media
        melhor = aluno.nome

print("Aprovados:", aprovados)
print("Reprovados:", reprovados)
print("Maior média:", melhor)
```

# Exercício 10 

```python
class Funcionario:
    def __init__(self, nome, idade, cargo, salario):
        self.nome = nome
        self.idade = idade
        self.cargo = cargo
        self.salario = salario


funcionarios = []

while True:
    print("\n1 - Cadastrar funcionários")
    print("2 - Listar funcionários")
    print("3 - Maior salário")
    print("4 - Média salarial")
    print("5 - Salários acima da média")
    print("0 - Sair")

    opcao = input("Escolha uma opção: ")

    if opcao == "1":
        funcionarios = []

        for i in range(10):
            nome = input("Nome: ")
            idade = int(input("Idade: "))
            cargo = input("Cargo: ")
            salario = float(input("Salário: "))

            funcionarios.append(
                Funcionario(nome, idade, cargo, salario)
            )

    elif opcao == "2":
        for funcionario in funcionarios:
            print(
                funcionario.nome,
                funcionario.idade,
                funcionario.cargo,
                funcionario.salario
            )

    elif opcao == "3":
        maior = funcionarios[0]

        for funcionario in funcionarios:
            if funcionario.salario > maior.salario:
                maior = funcionario

        print("Maior salário:", maior.nome, maior.salario)

    elif opcao == "4":
        soma = 0

        for funcionario in funcionarios:
            soma += funcionario.salario

        media = soma / len(funcionarios)
        print("Média salarial:", media)

    elif opcao == "5":
        soma = 0

        for funcionario in funcionarios:
            soma += funcionario.salario

        media = soma / len(funcionarios)

        for funcionario in funcionarios:
            if funcionario.salario > media:
                print(funcionario.nome, funcionario.salario)

    elif opcao == "0":
        break
```

