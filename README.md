# Código em Python - Estudo
# Estudando If, Elif e Else (Estrutura de repetição).

DESAFIO 036: Escreva um programa para aprovar o empréstimo bancário para a compra de uma casa.
O programa vai perguntar o valor da casa, o salário do comprador e em quantos anos ele vai pagar.
Calcule o valor da prestação mensal, sabendo que ele não pode exceder 30%
do salário ou então o empréstimo será negado.

import time

print('\n\t\t\t\033[1;30;41mVAMOS CALCULAR UM EMPRÉSTIMO?\033[m\n\033[1;30;41m------------------------------------------------------\033[m\n')

valorCasa = float(input('Qual o valor da casa que deseja financiar?\033[0;32m R$ \033[m'))
salario = float(input('Qual é o seu salário?\033[0;32m R$ \033[m'))
anosParcela = int(input('Em quantos anos pretende pagar? '))

print('\n\033[1;30;41mAguarde um momento até finalizarmos sua solicitação.\033[m')
time.sleep(10)   # Para fazer o usuário esperar como se estivesse em uma agência bancária.

anosPagar = anosParcela * 12   # Pega a quantidade de anos que o usuário deseja financiar a casa e multiplica por 12 meses de cada ano. Então tenho quantos meses ele irá pagar.
prestasaoMensal = valorCasa / anosPagar   # Pega o valor da casa e divide pela quantidade de meses que o usuário vai pagar.
porcentagemSalario = salario / 100 * 30   # Calculando quanto é 30% do salário.

if prestasaoMensal <= porcentagemSalario:   # Se o valor das prestações for abaixo de 30% do valor do salário, então imprima na tela.
    print('\nDesculpe pela demora.')
    print('\033[0;32mO seu empréstimo foi aprovado!')
    print('Você irá financiar esta casa durante \033[1m{} meses.\033[m'.format(anosPagar))
    print('\033[0;32mE o valor das parcelar serão de \033[1mR$ {:.2f} reais\033[m\033[0;32m por mês.\033[m'.format(prestasaoMensal))

    print('\n\033[4;33mCARREGANDO... ESPERE UM MOMENTO...\033[m')
    time.sleep(10)   # Para esperar alguns segundos.

    escolha = int(input('\n\033[1;34m---> \033[mSe está de acordo digite 1.'
                        '\n\033[1;34m---> \033[mSe deseja outra solicitação digite 2.'
                        '\n\033[1;34m---> \033[mse deseja cancelar digite 3.'
                        '\n\nO que o Senhor deseja fazer? '))
    if escolha == 1:
        print('\n\033[1;30;41mObrigado! Bom fazer negócio com você!\033[m')

    elif escolha ==2:
        print('\n\033[1;30;43m##### NOVA SOLICITAÇÃO #####\033[m')

        print('\n\t\t\t\033[1;30;41mVAMOS CALCULAR UM EMPRÉSTIMO?\033[m\n\033[1;30;41m------------------------------------------------------\033[m\n')

        # Valores que o usuário terá que colocar como entrada.
        valorCasa = float(input('Qual o valor da casa que deseja financiar?\033[0;32m R$ \033[m'))
        salario = float(input('Qual é o seu salário?\033[0;32m R$ \033[m'))
        anosParcela = int(input('Em quantos anos pretende pagar? '))

        print('\n\033[1;30;41mAguarde um momento até finalizarmos sua solicitação.\033[m')
        time.sleep(10)  # Para fazer o usuário esperar como se estivesse em uma agência bancária.

        anosPagar = anosParcela * 12  # Pega a quantidade de anos que o usuário deseja financiar a casa e multiplica por 12 meses de cada ano. Então tenho quantos meses ele irá pagar.
        prestasaoMensal = valorCasa / anosPagar  # Pega o valor da casa e divide pela quantidade de meses que o usuário vai pagar.
        porcentagemSalario = salario / 100 * 30  # Calculando quanto é 30% do salário.

        if prestasaoMensal <= porcentagemSalario:  # Se o valor das prestações for abaixo de 30% do valor do salário, então imprima na tela.
            print('\nDesculpe pela demora.')
            print('\033[0;32mO seu empréstimo foi aprovado!')
            print('Você irá financiar esta casa durante \033[1m{} meses.\033[m'.format(anosPagar))
            print('\033[0;32mE o valor das parcelar serão de \033[1mR$ {:.2f} reais\033[m\033[0;32m por mês.\033[m'.format(prestasaoMensal))

            print('\n\033[4;33mCARREGANDO... ESPERE UM MOMENTO...\033[m')
            time.sleep(10)  # Para esperar alguns segundos.

            novaEscolha = str(input('\n\033[1;34m--->\033[m Se esta de acordo digite S, ou quer cancelar digite N: ')).upper()

            if novaEscolha == 'S':
                print('\n\033[1;30;41mObrigado! Bom fazer negócio com você!\033[m')

            else:
                print('\n\033[1;31mA solicitação foi cancelada!\033[m')

        else:
            print('\n\033[1;31mO seu empréstimo não foi aprovado!')
            print('Excedeu 30% do valor do seu salário.\033[m')

    else:
        print('\n\033[1;31mA solicitação foi cancelada!\033[m')

else:
    print('\n\033[1;31mO seu empréstimo não foi aprovado!')
    print('Excedeu 30% do valor do seu salário.\033[m')
