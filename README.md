# Questionario-1
questionario desenvolvido no phyton



def questionario():
    print("Bem-vindo ao questionário")
    print("""
░██████╗░██╗░░░██╗███████╗░██████╗████████╗██╗
██╔═══██╗██║░░░██║██╔════╝██╔════╝╚══██╔══╝██║
██║██╗██║██║░░░██║█████╗░░╚█████╗░░░░██║░░░██║
╚██████╔╝██║░░░██║██╔══╝░░░╚═══██╗░░░██║░░░██║
░╚═██╔═╝░╚██████╔╝███████╗██████╔╝░░░██║░░░██║
░░░╚═╝░░░░╚═════╝░╚══════╝╚═════╝░░░░╚═╝░░░╚═╝
░█████╗░███╗░░██╗░█████╗░██████╗░██╗░█████╗░
██╔══██╗████╗░██║██╔══██╗██╔══██╗██║██╔══██╗
██║░░██║██╔██╗██║███████║██████╔╝██║██║░░██║
██║░░██║██║╚████║██╔══██║██╔══██╗██║██║░░██║
╚█████╔╝██║░╚███║██║░░██║██║░░██║██║╚█████╔╝
░╚════╝░╚═╝░░╚══╝╚═╝░░╚═╝╚═╝░░╚═╝╚═╝░╚════╝░""")
    print("""✍️""")


    nome = input("qual é seu nome?")
    profissao = input("qual a sua profissão?")
    idade = input("qual a sua idade?")
    peso = input("qual seu peso?")
    endereco = input("qual seu endereço?")
    telefone = input("qual o seu endereço?")




    print("/n---Respostas ---")
    print("Nome:", nome)
    print("Profissão:", profissao)
    print("Idade:", idade)
    print("Peso:", peso)
    print("Endereço:", endereço)
    print("Telefone:", telefone)


questionario()
from openpyxl import Workbook


def questionario():


  respostas = []
  for i in range(1,11):
    print(f"Respostas da pessoa {i}:")
    nome = input("qual é seu nome?")
    profissao = input("qual a sua profissao?")
    idade = input("qual a sua idade?")
    peso = input("qual seu peso?")
    altura = input("qual sua altura?")
    cordosolhos = input("qual a cor dos seus olhos?")
    rua = input("qual o nome da sua rua?")
    bairro = input("qual o nome do seu bairro?")
    municipio = input("qual o nome do seu municipio?")


    respostas.append([nome, profissao, idade, peso, altura, cordosolhos, rua, bairro, municipio])


    print()


    return respostas
def criar_planilha(respostas):


    wb = Workbook()
    ws = wb.active
    ws.append(['nome', 'profissao', 'idade', 'peso', 'altura', 'cor dos olhos', 'rua', 'bairro', 'municipio' ])
    for pessoa in respostas:


     ws.append(pessoa)
    wb.save("respostas_questionario_amandaEalice.xlsx")


    print("planilha criada com sucesso.")


respostas = questionario()
