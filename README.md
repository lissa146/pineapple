# pineapple
import pygame
pygame.init

screen = pygame.display.set_mode((800,800))
pygame.display.set_caption("pineapple")
mousePos = (400,400)

while True:
    event = pygame.event.wait()
    if event.type == pygame.MOUSEMOTION:
        mousePos = event.pos
    print(mousePos)
    
#FRUIT BODY
    pygame.draw.ellipse(screen, (255, 255, 51), (200,180, 400,500))

#CRISSCROSS
    for i in range(0, 800,30):
        pygame.draw.line(screen, (0, 0, 0), (i,0), (i+200, 800), 2)
    
    for i in range(0, 800,30):
        pygame.draw.line(screen, (0, 0, 0), (i,0), (i-300, 800), 2)

#top of the leaf
    pygame.draw.polygon(screen, (76, 153, 0), ((340,200), (250,50), (460,200)))
    pygame.draw.polygon(screen, (76, 153, 0), ((340,200), (320,50), (460,200)))
    pygame.draw.polygon(screen, (76, 153, 0), ((340,200), (390,50), (460,200)))
    pygame.draw.polygon(screen, (76, 153, 0), ((340,200), (450,50), (460,200)))
    pygame.draw.polygon(screen, (76, 153, 0), ((340,200), (520,50), (460,200)))
    
    
    pygame.display.flip()
