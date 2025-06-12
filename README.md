# 💥 Jogo de Objetos Móveis com Reações Polimórficas (SFML + C++)

Este projeto foi desenvolvido como parte de um trabalho prático para testar e demonstrar **técnicas de polimorfismo** em C++ utilizando a biblioteca gráfica **SFML**. O programa simula múltiplos objetos animados colidindo com as paredes da janela, cada um com comportamentos distintos ao bater nas bordas.

## 🎯 Objetivo

O foco principal é aplicar **conceitos de orientação a objetos** e **polimorfismo dinâmico**, implementando uma hierarquia de classes com um comportamento comum (`Movel`) e múltiplas especializações (`Bola`, `Barra`, `Mageste`, `Heart`), cada uma com sua própria lógica de movimento e resposta a colisões.

## 📦 Estrutura de Classes

### 🧱 Classe Base: `Movel`

Define a interface comum para todos os objetos móveis:
- Armazena posição, velocidade e textura.
- Implementa lógica padrão de colisão com as bordas da janela.
- Métodos virtuais para `move()` e `mostra()` permitem sobrescrita.

### 🔁 Classes Derivadas:

- **`Bola`**: se move apenas no eixo Y e desenha um círculo colorido dinâmico ao redor do sprite.
- **`Barra`**: movimenta-se horizontalmente.
- **`Mageste`**: rotaciona o sprite em colisões e se move em ambas direções.
- **`Heart`**: movimento alternado por ciclos com padrões diferentes a cada fase.

Cada classe redefine métodos como `move()` e `testaColisaoComParede()` com comportamento próprio, ilustrando claramente o uso de polimorfismo.

## 🧠 Conceitos de Programação Utilizados

- ✅ **Herança e classes virtuais**
- ✅ **Polimorfismo dinâmico com sobrescrita de métodos**
- ✅ **Uso de ponteiros para a classe base (`Movel*`)**
- ✅ **Composição com SFML: `sf::Sprite`, `sf::Texture`, `sf::RenderWindow`**
- ✅ **Enumeração para tipos de objetos (`enum OBJETO`)**
- ✅ **Criação de objetos aleatórios com comportamento individual**

## 🖼️ Demonstração Visual

*(Insira aqui screenshots ou GIFs, se disponível)*

## 🛠️ Como Compilar e Executar

### Pré-requisitos

- SFML 2.5+ instalada ([tutorial oficial](https://www.sfml-dev.org/tutorials/2.5/start-linux.php))
- Compilador C++ compatível com C++11 ou superior

### Compilação

```bash
g++ main.cpp -o objetos -lsfml-graphics -lsfml-window -lsfml-system
