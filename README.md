# Gerenciamento_de_Estoque
Este é um programa simples de gerenciamento de estoque que permite ao usuário adicionar e remover itens do estoque, contar os itens no estoque e gerar um relatório de vendas.

O programa começa solicitando que o usuário digite um nome de usuário e senha para login. Depois que o usuário é autenticado, o loop principal do programa é iniciado. O usuário pode escolher entre quatro ações - adicionar itens ao estoque, remover itens do estoque, contar os itens do estoque e gerar um relatório de vendas.

O programa utiliza dois dicionários para armazenar dados - um para armazenar as referências dos produtos e outro para armazenar os itens em estoque. O programa gera um código de referência aleatório para um produto se ainda não existir no dicionário de referência.

A função adicionar_item_ao_estoque usa um nome de item e uma quantidade como entrada e adiciona o item ao estoque. Ele primeiro verifica se o item já existe no dicionário de referência. Em caso afirmativo, ele obtém o código de referência do item. Caso contrário, ele gera um código de referência aleatório e o adiciona ao dicionário de referência. A função então verifica se o item já existe no dicionário de inventário. Em caso afirmativo, adiciona a quantidade à quantidade existente. Caso contrário, adiciona o item ao dicionário de estoque com a quantidade fornecida.

A função remover_item_do_estoque usa um nome de item e uma quantidade como entrada e remove o item do estoque. Ele primeiro verifica se o item existe no dicionário de inventário. Em caso afirmativo, verifica se a quantidade solicitada é menor ou igual à quantidade do estoque. Se for, remove a quantidade solicitada do estoque. Se não estiver, imprime uma mensagem de erro. Caso o item não exista no estoque, imprime uma mensagem de erro.

A função contar_itens_no_estoque simplesmente percorre o dicionário de inventário e imprime os nomes e as quantidades dos itens.

A função gerar_relatorio_de_vendas gera um valor de vendas aleatório para cada item no estoque, soma os valores de vendas e imprime o valor total de vendas.

O loop principal do programa solicita que o usuário escolha uma ação e, em seguida, chama a função correspondente. Se o usuário escolher uma ação inválida, o programa imprimirá uma mensagem de erro. Se o usuário optar por sair, o programa sai do loop e termina.
