# Projeto-de-adivinha-o.PYTHON
# Projeto abaixo (CRISTIANO RONALDO)

import time

def jogar_adivinhacao():
    print("Ok, vamos jogar!")
    time.sleep(1)

    dicas = [
        "Dica 1: Ele nasceu em Portugal",
        "Dica 2: Ele já jogou pelo Sporting de Portugal",
        "Dica 3: Ele é o jogador em atividade com mais gols na carreira.",
        "Dica 4: Ele já ganhou 5 Bolas de ouro.",
        "Dica 5: Ele é conhecido pelo apelido: Senhor Champions."
    ]
    jogador_secreto = "cristiano ronaldo"
    tentativas = 5

    for i in range(tentativas):
        print(dicas[i])
        time.sleep(3)
        palpite = input(f"Qual é o seu palpite? (Tentativa {i + 1}/{tentativas}) ")
        if palpite.casefold() == jogador_secreto:
            print("Muito bem, você acertou!")
            print("Obrigado por jogar!!!")
            print("Curiosidade: Apesar de ser conhecido pela educação na vida real, o astro já teve os seus momentos de rebeldia na infância. Cristiano Ronaldo simplesmente já foi expulso de uma escola que estudava por arremessar uma cadeira na professora. E qual foi a justificativa que deu à coordenação? Segundo ele, sofreu zoações por conta do seu sotaque.")
            return
        else:
            print("Você errou, tente novamente.")
            time.sleep(1)
    print(f"Você esgotou suas tentativas. O jogador era o {jogador_secreto.title()}.")
    print("Obrigado por jogar!!!")



pergunta = input(str("Olá, gostaria de jogar o que é o que é ?. Adivinhe o jogador que pensei, você tem 5 chances. "))

if pergunta.casefold() == "sim":
    jogar_adivinhacao()
elif pergunta.casefold() == "não":
    print("Obrigado pela atenção!")
else:
    print("Por favor, digite sim ou não.")
