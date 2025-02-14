# python
# Crie duas funções para somar dois valores e para subtrair dois valores
# e retorne o resultado para o programa principal.

# exercicio 1

# def soma(n1,n2):
#   return n1+n2
# def sub(n1,n2):
#   return n1-n2

# n1 = int(input("insira o valor de n1 \n"))
# n2 = int(input("insira o valor de n2 \n"))
# s = soma (n1,n2)
# sb = sub(n1,n2)
# print(f"soma {s}\nsubtração {sb}\n")

# Crie um programa com duas funções, a primeira vai exibir uma mensagem de boas vindas e a segunda vai calcular a idade do usuario no ano atual.
# os resultados são exibidos em cada função

# exercicio 2

# def ola():
#  nome=input("insira o nome\n")
#   print(f"Olá {nome}, Bem-Vindo ao curso\n")

# def idade():
# ano_atual=int(input("insira o ano atual\n"))
# ano_nasc=int(input("insira seu ano de nascimento\n"))
#  idade=ano_atual-ano_nasc
#   print(f"idade no ano {ano_atual} é {idade}")

# ola()
# idade()

# def subt(n1,n2):
#   return n1-n2
# n1 = float(input("defina o valor de a:"))
# n2 = float(input("defina o valor de b: "))
# sb = subt(n1,n2)
# print(sb)

def potencial(a, b):
    if b == 0:
        return 1;
    else:
        return a * potencial(a, b - 1)


a = int(input("insira a base: "))
b = int(input("insira o expoente: "))
p = potencial(a, b)
print(f"{a} elevado á {b} é: {p}")


ctrl + alt + L = organizar codigos

