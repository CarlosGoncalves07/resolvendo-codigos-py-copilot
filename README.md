# Resolvendo Códigos em Python com o Github Copilot e ChatGPT

Olá!! Fiz alguns projeto em Python com base nos desafios propostos, espero que goste!

## 1 - Concatenando Dados 🐾

# Programa simples de concatenação de strings

nome = input("Digite seu nome: ")
cidade = input("Digite a sua cidade: ")

# Concatena as duas strings em uma frase
mensagem = "Olá, " + nome + "! Você é de " + cidade + "."
print(mensagem)

O que aprendemos?

* Manipulação de Strings (string)
* Concatenação
* Entrada de dados
* Utilização eficiente do Github Copilot

<br>

------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------
## 2 - Repetindo Textos ✏️

# Gerador de Slogans Personalizados

## Criando um programa em Python que peça ao usuário uma frase e quantas vezes repetir, e gere um slogan impactante com essa repetição, com opções de “estilo” de slogan.
Digite seu slogan: Vamos Ganhar!
Digite quantas vezes repetir: 4
Escolha um estilo:
1) Linha única
2) Com separador “–”
3) Em colunas (cada repetição em nova linha)
Resultado (se escolher 2):

Vamos Ganhar! – Vamos Ganhar! – Vamos Ganhar! – Vamos Ganhar!
def gerar_slogan(frase, repeticoes, estilo):
    # Função que monta o slogan conforme o estilo escolhido
    if estilo == 1:
        # Linha única simples
        return " ".join([frase for _ in range(repeticoes)])
    elif estilo == 2:
        # Linha única com separador “ – ”
        return " – ".join([frase for _ in range(repeticoes)])
    elif estilo == 3:
        # Cada repetição em uma nova linha
        return "\n".join([frase for _ in range(repeticoes)])
    else:
        return "Estilo inválido! Por favor escolha 1, 2 ou 3."

# Entrada de dados do usuário
slogan = input("Digite seu slogan: ")
qtd = int(input("Digite quantas vezes repetir: "))

# Mostrar opções de estilo com os textos conforme seu exemplo
print("\nEscolha um estilo:")
print("1) Linha única")
print("2) Com separador “–”")
print("3) Em colunas (cada repetição em nova linha)")

estilo_escolhido = int(input("Escolha uma opção (1, 2 ou 3): "))

# Gera e mostra o resultado
resultado = gerar_slogan(slogan, qtd, estilo_escolhido)

print("\nResultado (se escolher {}):\n".format(estilo_escolhido))
print(resultado)

O que aprendemos?

* Manipulação de Strings (string)
* Números Inteiros (int)
* Múltiplas repetições
* Entrada de dados
* Aproveitar as sugestões do Github Copilot

<br>

------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------
## 3 - Operações Matemáticas Simples 📐

## Calculadora simples!

# Programa para ler dois números e realizar uma operação entre eles

# Solicita os números ao usuário
num1 = float(input("Digite o primeiro número: "))
num2 = float(input("Digite o segundo número: "))

# Pergunta qual operação deseja realizar
operacao = input("Digite a operação (+, -, * ou /): ")

# Realiza a operação escolhida e exibe o resultado
if operacao == "+":
    resultado = num1 + num2
    print("Soma: " + str(resultado))
elif operacao == "-":
    resultado = num1 - num2
    print("Subtração: " + str(resultado))
elif operacao == "*":
    resultado = num1 * num2
    print("Multiplicação: " + str(resultado))
elif operacao == "/":
    # Verifica divisão por zero
    if num2 != 0:
        resultado = num1 / num2
        print("Divisão: " + str(resultado))
    else:
        print("Erro: divisão por zero!")
else:
    print("Operação inválida!")


O que aprendemos?

* Operações Matemáticas Básicas
* Entrada de dados
* Utilização eficiente do Github Copilot

<br>

------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------
## 4 - Verificando Números Pares e Ímpares 🧮

# Programa para verificar se o número é par ou ímpar

numero = int(input("Digite um número inteiro: "))

if numero % 2 == 0:
    print(str(numero) + " é um número PAR.")
else:
    print(str(numero) + " é um número ÍMPAR.")


O que aprendemos?
* Utilização de condicionais em Python (if, else) para realizar verificações.
* Introdução ao conceito de operador de módulo (%) para verificar se um número é par ou ímpar.
* Exploração do uso de uma ferramenta de IA, como o Github Copilot, para otimizar a estrutura do código.


<br>

------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------
## 5 - Calculando Média de Notas 📚

## Criando um programa para calcular a media de um aluno!

print("== Cálculo da Média do Aluno ==")

# Entradas de notas
nota1 = float(input("Digite a primeira nota: "))
nota2 = float(input("Digite a segunda nota: "))
nota3 = float(input("Digite a terceira nota: "))

# Cálculo da média
media = (nota1 + nota2 + nota3) / 3

# Exibindo resultado
print("\n=== Resultado ===")
print(f"Notas: {nota1}, {nota2}, {nota3}")
print(f"Média do aluno: {media:.2f}")

# Verificando situação do aluno
if media >= 7:
    print("Situação: Aprovado 🎉")
elif media >= 5:
    print("Situação: Recuperação ⚠️")
else:
    print("Situação: Reprovado 😢")


O que aprendemos?
* Uso de variáveis para armazenar dados fornecidos pelo usuário.
* Aplicação de operadores aritméticos (+, /) para calcular a média de um conjunto de valores.
* Prática na solicitação e manipulação de entrada do usuário.

<br>

------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------
## 6 - Verificando Palíndromos 🔄

## 🎮 Projeto de jogo educativo: “Caça‑Palíndromos”

import random

# Lista de exemplos de palavras
palavras = ["arara", "python", "radar", "casa", "ovo", "amora", "level", "bola", "kayak", "moto"]

# Função para verificar palíndromo
def eh_palindromo(p):
    p = p.lower()  # Ignora maiúsculas/minúsculas
    return p == p[::-1]  # Compara com a versão invertida

print("=== Jogo: Caça‑Palíndromos ===")
print("Responda 'sim' se a palavra for palíndromo ou 'nao' se não for.")

pontos = 0

# Loop por 5 rodadas (você pode mudar)
for i in range(5):
    palavra_atual = random.choice(palavras)
    print(f"\nPalavra {i+1}: {palavra_atual}")
    resposta = input("É palíndromo? (sim/nao): ").strip().lower()

    # Verifica se a palavra é palíndromo
    correto = eh_palindromo(palavra_atual)

    if (resposta == "sim" and correto) or (resposta == "nao" and not correto):
        print("✔️ Certo!")
        pontos += 1
    else:
        print("❌ Errado!")

print("\n=== Resultado Final ===")
print("Você acertou", pontos, "de 5!")


O que aprendemos?
* Manipulação de strings em Python, especialmente invertendo uma string.
* Compreensão de como comparar a string original com sua versão invertida para determinar se é um palíndromo.
* Introdução ao conceito de palíndromos e sua aplicação em problemas de programação.
