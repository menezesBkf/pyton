# python
 Crie duas funções para somar dois valores e para subtrair dois valores
 e retorne o resultado para o programa principal.

 exercicio 1

 def soma(n1,n2):
   return n1+n2
 def sub(n1,n2):
   return n1-n2

 n1 = int(input("insira o valor de n1 \n"))
 n2 = int(input("insira o valor de n2 \n"))
 s = soma (n1,n2)
 sb = sub(n1,n2)
 print(f"soma {s}\nsubtração {sb}\n")

 Crie um programa com duas funções, a primeira vai exibir uma mensagem de boas vindas e a segunda vai calcular a idade do usuario no ano atual.
 os resultados são exibidos em cada função

 exercicio 2

 def ola():
  nome=input("insira o nome\n")
   print(f"Olá {nome}, Bem-Vindo ao curso\n")

 def idade():
 ano_atual=int(input("insira o ano atual\n"))
 ano_nasc=int(input("insira seu ano de nascimento\n"))
  idade=ano_atual-ano_nasc
   print(f"idade no ano {ano_atual} é {idade}")

 ola()
 idade()

 def subt(n1,n2):
   return n1-n2
 n1 = float(input("defina o valor de a:"))
 n2 = float(input("defina o valor de b: "))
 sb = subt(n1,n2)
 print(sb)

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




exercicio 4
def val():
    op=int(input("insira a opção: "))
    if (op==1 or op==2 or op==3):
        return op
    else:
        print("opção errada\n")
        return val()
def soma(a,b):
    return a+b

def sub(a,b):
    return a-b

def mult(a,b):
    return a*b

print("menu:\n1-soma\n2-subtração\n3-multiplicação")
escolha = val()
a = int(input("insira o primeiro valor: "))
b = int(input("insira o segundo valor: "))
if escolha == 1:
    s=soma(a,b)
    print(f"soma = {s}")
elif escolha  == 2:
    sb=sub(a,b)
    print(f"subtração {sb}")
else:
    m=mult(a,b)
    print(f"multiplicação {m}")



aula2

import tkinter as tk
root=tk.Tk()
root.title("primeira janela")
root.geometry("400x400")
label1=tk.Label(root,text="Bem-vindo usuário")
label1.pack(padx=20,pady=20)

def ola():
    label2=tk.Label(root,text="botão funcionando")
    label2.pack(padx=25,pady=25)
botao=tk.Button(root,text="ok",command=ola)
botao.pack(padx=30,pady=30)
t=tk.Entry(root)
t.pack(padx=35, pady=35)

def texto():
    valor=t.get()
    label1.config(text="Bem-vindo "+valor)
botao2=tk.Button(root,text="atualizar", command=texto)
botao2.pack(padx=20,pady=20)

def janela():
    frame1=tk.Toplevel(root)
    frame1.title ("Nova janela do usuario")
    frame1.geometry("300 x 300")
    
    label3=tk.Label(frame1,text="Janela do Usuário")
    label3.pack(padx=20,pady=20)

    def sair():
        frame1.destroy()
        frame1.destroy()
        botao3=tk.Button(frame1,text="sair",command=sair)
        botao3.pack(padx=20,pady=20)
    frame1.pack()
botao4=tk.Button(root,text="nova janela",command=janela)
botao4.pack(padx=20,pady=20)
root.mainloop()


aula 3

import tkinter as tk
lista_nomes = []
lista_idades = []
lista_emails = []

def ad():
    valor1=entrada1.get()
    lista_nomes.append(valor1)
    valor2=entrada2.get()
    lista_idades.append(valor2)
    valor3=entrada3.get()
    lista_emails.append(valor3)
    alert=tk.Toplevel(root)
    label9=tk.Label(alert,text="Convidado inserido na lista")
    label9.pack()
    
    def ok():
        alert.destroy()
        b_ok=tk.Button(alert, text="OK", command=ok)
        b_ok.pack()
        entrada1. delete(0,"end")
        entrada2. delete(0,"end")
        entrada3. delete(0,"end")

def exi():
    label5=tk.Label(root,text="Lista de Convidados",font=("Arial",15))
    label5.grid(row=5,column=1)
    for i,item in enumerate(lista_nomes):
        label6=tk.Label(root,text=item,font=("Arial",15))
        label6.grid(row=i+6,column=0)
    for i,item in enumerate(lista_idades):
        label7=tk.Label(root,text=item)
        label7.grid(row=i+6,column=1)
    for i,item in enumerate(lista_emails):
        label8=tk.Label(root,text=item, font=("Arial",15))
        label8.grid(row=i+6,column=2)

root= tk.Tk()
root.title("Convite")
root.geometry("600x350")
label1=tk.Label(root, text="Convidados",font=("arial",15))
label1.grid(row=0,column=0)
label2=tk.Label(root,text="Nome:",font=("arial",15))
label2.grid(row=1,column=0)
entrada1=tk.Entry(root, font=("arial",15))
entrada1.grid(row=1,column=1)
label3=tk.Label(root, text="idade:",font=("arial",15))
label3.grid(row=2,column=0)
entrada2=tk.Entry(root, font=("arial",15))
entrada2.grid(row=2,column=1)
label4=tk.Label(root, text="email",font=("arial",15))
label4.grid(row=3,column=0)
entrada3=tk.Entry(root, font=("arial",15))
entrada3.grid(row=3,column=1)
b_ad=tk.Button(root, text="Adicionar",font=("arial",15),command=ad)
b_ad.grid(row=4,column=0)
b_exibir=tk.Button(root, text="Exibir",font=("Arial",15), command=exi)
b_exibir.grid(row=4, column=1)

root.mainloop()


