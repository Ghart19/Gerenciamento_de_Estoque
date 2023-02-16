import random
import string

# Dados do usuário
nome_de_usuario = 'admin'
senha = 'admin'

# Dicionário para armazenar as referências dos produtos
referencias_de_produtos = {}

# Dicionário para armazenar os itens em estoque
estoque = {}

# Função para realizar login
def login():
    while True:
        try:
            input_usuario = input('Digite o usuário: ')
            input_senha = input('Digite a senha: ')

            if input_usuario == nome_de_usuario and input_senha == senha:
                print('-' * 20)
                print('Acesso liberado')
                print('-' * 20)
                break
            else:
                raise ValueError('Usuário ou senha incorretos.')
        except ValueError as e:
            print(f'Erro: {e}')
            print('-' * 20)

# Função para adicionar item ao estoque
def adicionar_item_ao_estoque(item, quantidade):
    if item in referencias_de_produtos:
        referencia = referencias_de_produtos[item]
    else:
        referencia = ''.join(random.choice(string.ascii_uppercase + string.digits) for _ in range(6))
        referencias_de_produtos[item] = referencia

    if item in estoque:
        estoque[item] += quantidade
    else:
        estoque[item] = quantidade

    item_formatado = f'Produto: {item}; Referência: {referencia}; Quantidade: {quantidade}'
    print(f'Adicionado ao estoque:\n{item_formatado}\n')
    print('-' * 20)

# Função para remover item do estoque
def remover_item_do_estoque(item, quantidade):
    if item in estoque:
        if quantidade <= estoque[item]:
            estoque[item] -= quantidade
            print(f'Removido do estoque:\nProduto: {item}; Quantidade: {quantidade}\n')
        else:
            print(f'Não é possível remover mais do que a quantidade em estoque ({estoque[item]} unidades)')
    else:
        print(f'{item} não está no estoque.')
    print('-' * 20)

# Função para contar itens no estoque
def contar_itens_no_estoque():
    print('Itens em estoque:')
    for item, quantidade in estoque.items():
        print(f'{item}: {quantidade}')
    print('-' * 20)

# Função para gerar relatório de vendas
def gerar_relatorio_de_vendas():
    print('Relatório de vendas:')
    total_vendido = 0
    for item, quantidade in estoque.items():
        vendas = random.randint(0, quantidade)
        total_vendido += vendas
        print(f'{item}: {vendas} vendido(s)')
    print(f'Total vendido: {total_vendido}')
    print('-' * 20)

# Função para o loop principal do programa
def loop_principal():
    # Loop principal do programa
    while True:
        # Opções de ação
        print("""[1] - Adicionar item ao estoque
[2] - Remover item do estoque
[3] - Contar itens no estoque
[4] - Gerar relatório de vendas
""")
        try:
            acao = int(input('O que deseja fazer?: '))
            print('-' * 20)

            # Adicionar itens ao estoque
            if acao == 1:
                item = input('Digite o nome do produto: ')
                quantidade = int(input('Digite a quantidade a ser adicionada: '))
                adicionar_item_ao_estoque(item, quantidade)
            # Remover
            elif acao == 2:
                item = input('Digite o nome do produto: ')
                quantidade = int(input('Digite a quantidade a ser removida: '))
                remover_item_do_estoque(item, quantidade)

            # Contar itens
            elif acao == 3:
               contar_itens_no_estoque()

            # Gerar relatório de vendas
            elif acao == 4:
                gerar_relatorio_de_vendas()

            # Sair
            elif acao == 0:
                 print('Saindo do programa...')
                 break

        # Opção inválida
            else:
                print('Opção inválida. Tente novamente.')
                print('-' * 20)
        except ValueError:
            print('Opção inválida. Tente novamente.')
            print('-' * 20)

# Chamada das funções
login()
loop_principal()
