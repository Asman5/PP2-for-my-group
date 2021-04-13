import pygame
import random

pygame.init()

sprites = pygame.image.load("lion.bmp")

screen = pygame.display.set_mode((800, 600))

background = pygame.Surface(screen.get_size())

background.fill((255, 255, 255))

screen.blit(background, (0, 0))


lions = []

size = 128

w, h = 128, 64

for i in range(4):
    lions.append(sprites.subsurface( (size * i, 64, w, h) ) )

for i in range(2):
    lions.append(sprites.subsurface( (size * i, 198, w, h) ) )
    
for i in range(len(lions)):
    lions[i].set_colorkey( (0, 0, 0) )

FPS = 30
interval = 0.1
cycletime = 0
number = 0
clock = pygame.time.Clock()

x = 200
y = 300
# секунды больше милисекунд
# часы больше минут
# 600 минут
# часов = 600 минут / 60
# 600 миллисекунд
# секунды = 600 / 1000

run = True
while run:
    milliseconds = clock.tick(FPS)
    seconds = milliseconds / 1000
    cycletime += seconds
    if cycletime > interval:
        number += 1
        if number > 5:
            number = 0
            cycletime = 0
    for event in pygame.event.get():
        if event.type == pygame.QUIT:
            run = False
        if event.type == pygame.KEYDOWN:
            if event.key == pygame.K_ESCAPE:
                run = False

    screen.fill( (28, 34, 175) )
    picture = lions[number]
    screen.blit(picture, (x, y))
    x += 20
    if x > screen.get_size()[0]:
        x = 0
    pygame.display.flip()
#Познавший человочество умом не обделен
#Познавший сам себя - умней вдвойне
#Кто победил другого, тот силен
#Кто победил себя - стократ сильней
#Одаривает жизнь смирившихся с судьбой
#Удача ждетуверенных в себе
#Чтоб долго жить, живи в ладу с собой
#Чтоб вечно жить, войди в сердца людей
