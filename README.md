# ===== Inicialização =====
# ----- Importa e inicia pacotes
import pygame

pygame.init()

# ----- Gera tela principal
WIDTH = 800
HEIGHT = 500
window = pygame.display.set_mode((WIDTH, HEIGHT))
pygame.display.set_caption('Flappy Bird')

# ----- Inicia estruturas de dados
game = True

# ----- Inicia assets
image = pygame.image.load('downloads/referencia/assets/img/paisagem.png').convert()
unicornio = pygame.image.load('downloads/referencia/assets/img/198 flying right clone clone.gif').convert()
# ===== Loop principal =====
while game:
    # ----- Trata eventos
    for event in pygame.event.get():
        # ----- Verifica consequências
        if event.type == pygame.QUIT:
            game = False

    # ----- Gera saídas
    window.fill((0, 0, 0))  # Preenche com a cor branca
    window.blit(image, [0, 0])
    window.blit(unicornio, [10, HEIGHT/2])

    # ----- Atualiza estado do jogo
    pygame.display.update()  # Mostra o novo frame para o jogador

# ===== Finalização =====
pygame.quit() 
