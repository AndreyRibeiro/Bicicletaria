listaPecas = []
def cadastrarPeca(peca):
    print("Você selecionou a opção de cadastrar peças")
    print("O código da peça a ser cadastrada é: {}" .format(peca))
    nome = input("Por favor, entre com o NOME da peça: ")
    fabricante = input("Por favor, entre com o FABRICANTE da peça: ")
    valor = int(input("Por favor, entre com o VALOR(R$) da peça: "))
    dicionarioPeca = {'Código' : peca, 'Nome' : nome, 'Fabricante' : fabricante, 'Valor' : valor}
    listaPecas.append(dicionarioPeca.copy())

def consultarPeca():
    while True:
        try:
            print("Você selecionou a opção de consultar peças")
            opConsultar = int(input("Entre com a opção desejada:\n 1 - Consultar todas as peças \n 2 - Consultar peças por código \n 3 - Consultar peças por fabricante \n 4 - Retornar \n"))
            if opConsultar == 1:
                print("-" * 15)
                for pecas in listaPecas:
                    for key, value in pecas.items():
                        print("{} : {}" .format(key,value))
            if opConsultar == 2:
                print("-" * 15)
                codigo = int (input("Digite o código desejado: "))
                for pecas in listaPecas:
                    if(pecas['Código'] == codigo):
                       for key, value in pecas.items():
                         print("{} : {}" .format(key,value))   
            if opConsultar == 3:
                print("-" * 15)
                fabricante = input("Digite o fabricante desejado: ")
                for pecas in listaPecas:
                    if(pecas['Fabricante'] == fabricante):
                       for key, value in pecas.items():
                         print("{} : {}" .format(key,value))   
            if opConsultar == 4:
                print("-" * 15)
                break
        except ValueError:
            print("Digite uma opção válida")

def removerPeca():
    print("Você selecionou a opção de remover peças")
    codigo = int(input("Digite o código desejado: "))
    for pecas in listaPecas:
        if(pecas['Código'] == codigo):
            listaPecas.remove(pecas)

print("Bem Vindo ao Controle de Estoque da Bicicletaria do Andrey Grigoletto")
registroPeca = 0
while True:
    try:
        opcao = int (input("Escolha a opção desejada: \n 1-Cadastrar peças \n 2-Consultar peças \n 3-Remover peças \n 4-Sair \n"))
        if opcao == 1:
            registroPeca = registroPeca + 1
            cadastrarPeca(registroPeca)
        elif opcao == 2:
            consultarPeca()
        elif opcao == 3:
            removerPeca()
        elif opcao == 4:
            print("Programa finalizado")
            break
        else:
            print("Digite uma opção válida")
    except:
        print("Selecione uma opção válida")
