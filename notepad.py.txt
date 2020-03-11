import re

busca = (']0100')

count = 0

with open('arquivo_de_busca.txt', 'r', encoding="utf-8") as arquivo:
    for linha in arquivo:# assume que cada linha do arquivo é uma frase

        if busca in linha: # se a palavra está na linha, imprime a linha ("frase") inteira
            count = count + 1
            print('{}. {}'.format(count, linha))


            arquivo = open('arquivo_de_saida.txt', 'r')  # Abra o arquivo (leitura), criar um arquivo com este nome
            conteudo = arquivo.readlines()
            conteudo.append('{}. {}'.format(count, linha))  # insira seu conteúdo

            arquivo = open('arquivo_de_saida.txt', 'w')  # Abre novamente o arquivo (escrita)
            arquivo.writelines(conteudo)  # escreva o conteúdo criado anteriormente nele.
            arquivo.close()

# gravar frase em arquivo de texto
# 00610042.97
