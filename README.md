#desenvolvendo um aplicativo de vendas em atacado que aplique descontos, de acordo com o valor gasto da compra

produto = float(input('Bem-vindo a Loja da Juliana Fernandes\n \nEntre com o valor do produto: R$ ')) #recebe o valor do produto "float" indica pode ser valor flutuante decimal

quantidade  = int(input('\nQual a quantidade do produto adquirido :')) # a quantidade "int" para que receba um valor inteiro

valor_total = produto * quantidade

if valor_total < 2500: # if significa que "se" caso o "valor total" gasto pelo cliente "for menor que R$2.500", ele não ganhará "desconto nenhum"
    desconto = 0
elif valor_total >= 2500 and valor_total < 6000: # aqui "senão" (referindo-se a condição if anterior) se gastar entre R$2.500 até R$6.000 pila, o cliente vai ter um desconto de 0.04, que é igual a 4%
    desconto = valor_total * 0.04
elif valor_total >= 6000 and valor_total <10000: # se caso o cliente gastar de R$6.000 pila pra mais e o valor total for menor que R$10.000 reais, terá um desconto de 0.07 que é igual a 7% de desconto no valor da compra
    desconto = valor_total * 0.07
else:
    desconto = valor_total * 0.11 # agora se o cliente acabar estourando a boca do balão e quase comprando de R$10.000 para mais, ganhará um desconto de 0.11 que é 11% de deconto de acordo com o valor gasto

resultado = produto * quantidade #multiplicando o resultado para saber o valor do produto vezes a quantidade do produto, para descobrir o valor total gasto
valor_desconto = resultado - desconto #descobrindo qual será o exato valor do desconto

print('\nO valor SEM o desconto é de: R$ {:.2f}'.format (resultado)) #calculando o valor sem o desconto aplicado
print('\nO valor COM o desconto é de: R$ {:.2f}'.format (valor_desconto)) # calculando o valor já com o desconto aplicado


#obs:  o prof disse que os comentários deveriam ser bem explicadinhos como se qualquer pessoa que batesse o olho no codigo, conseguisse entender com as explicações. Se fiz errado nesses comentários, por favor fessor me perdoe, e que o Guido van Rossum te abençoe viu, amém ♡
