print('Seja Bem Vindo a Lanchonete da Tatiane')
print('****************** Cardápio *******************')
 
# tabela de produtos para uma lanchonete
print('| Código |   Descrição           | Valor |')
print('| 100    |   Cachorro Quente     | 9,00  |')
print('| 101    | Cachorro Quente Duplo | 11,00 |')
print('| 102    |      X-Egg            | 12,00 |')
print('| 103    |      X-Salada         | 12,00 |')
print('| 104    |      X-Bacon          | 14,00 |')
print('| 105    |      X-Tudo           | 17,00 |')
print('| 200    |   Refrigerante Lata   | 15,00 |')
print('| 201    |    Chá Gelado         | 4,00  |')
 
produtos = {  # codigo, mais produto, mais valor
    100: ('Cachorro-Quente', 9.00),
    101: ('Cachorro-Quente Duplo', 11.00),
    102: ('X-Egg', 12.00),
    103: ('X-Salada', 13.00),
    104: ('X-Bacon', 14.00),
    105: ('X-Tudo', 17.00),
    200: ('Refrigerante Lata', 5.00),
    201: ('Chá Gelado', 4.00)
}
 
# inicializa a contagem do valor total
total = 0
 
while True:
    codigo = int(input('Entre com o código desejado: '))  # Codigo do prooduto
 
  if codigo in produtos:
        print('Produto selecionado:', produtos[codigo][0])
        total += produtos[codigo][1]  # A soma do pedido, mais se quiser outro pedido
 
  else:
        print('Opção inválida')  # Caso o usuario digito um codigo que não esta na tabela
        continue
 
  opcao = input('Deseja pedir mais alguma coisa? \n' +  # opção de multipla escolha
                  '1 - Sim \n' +
                  '0 - Não\n' +
                  '>> ')
 
  if opcao == '0':
        break
    elif opcao != '1':
        print('+Opção inválida')
        break
 
print(f'Total a pagar: R$%.2f' % total)
