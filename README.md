# projeto3PAYGAME


“PySnake” geralmente é um projeto do famoso jogo da cobrinha feito em Python usando a biblioteca Pygame. A ideia é aprender programação criando um jogo simples. ([Pygame][1])

## Como funciona o PySnake

No jogo:

* A cobra se move pela tela
* Ela come frutas/comida
* Cada fruta faz a cobra crescer
* O jogador perde se bater na parede ou no próprio corpo

## O que normalmente existe no código

### 1. Criar a janela do jogo

O Python abre uma janela usando a biblioteca `pygame`.

Exemplo:

```python
pygame.display.set_mode((600, 400))
```

Isso cria uma tela de 600x400 pixels.

---

### 2. Movimento da cobra

A cobra tem coordenadas `x` e `y`.

Quando você aperta as setas:

* esquerda → x diminui
* direita → x aumenta
* cima → y diminui
* baixo → y aumenta

---

### 3. Corpo da cobra

O corpo geralmente é guardado em uma lista.

Exemplo:

```python
snake = [[100, 50], [90, 50], [80, 50]]
```

Cada item representa uma parte da cobra.

---

### 4. Comida/fruta

O jogo cria comida em posições aleatórias.

Exemplo:

```python
food_x = random.randrange(1, 50) * 10
```

---

### 5. Colisão

O programa verifica:

* se a cobra bateu na parede
* se bateu nela mesma

Se acontecer:

```python
game_over()
```

---

## Biblioteca usada

A maioria dos projetos PySnake usa o Pygame, que serve para criar jogos em Python. ([Python Programming][2])

## Exemplo bem simples

```python
import pygame

pygame.init()

tela = pygame.display.set_mode((400, 300))

rodando = True

while rodando:
    for evento in pygame.event.get():
        if evento.type == pygame.QUIT:
            rodando = False
```

Esse código:

* inicia o pygame
* cria uma janela
* mantém ela aberta

---

## O que você aprende fazendo PySnake

Criar um jogo da cobrinha ajuda a aprender:

* lógica de programação
* listas
* funções
* loops (`while`)
* condições (`if`)
* colisões
* movimentação
* eventos do teclado


