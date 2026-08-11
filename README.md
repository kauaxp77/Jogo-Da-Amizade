# Jogo da Amizade 🐻🐰

Um divertido e criativo minigame desenvolvido inteiramente com **HTML5, Vanilla CSS e Vanilla JavaScript**, sem o uso de engine ou a tag `<canvas>`. O objetivo do jogo é controlar um simpático urso, usar o radar para encontrar coelhinhos tristes espalhados pelo mapa e dar um belo abraço neles para espalhar a felicidade!

## 🎮 Como Jogar

1. **Objetivo:** Encontrar e abraçar todos os coelhinhos tristes.
2. **Movimentação:** Basta **clicar (no computador)** ou **tocar na tela (em dispositivos móveis)** em direção de onde você quer que o urso vá.
3. **Radar:** Observe a bússola/radar no centro-inferior ou lateral da tela (dependendo do seu dispositivo). Ele vai indicar a **direção e a distância** dos coelhos mais próximos.

## 🛠 Técnicas e Tecnologias Diferenciadas Neste Projeto

Este projeto parece simples, mas envolve uma série de conhecimentos sólidos de programação front-end raiz:

* **Engine em DOM (Document Object Model):** Ao invés do tradicional `<canvas>`, os elementos do jogo foram construídos usando divs HTML sobrepostas e o estado do jogo e a engine calculam posições diretamente no CSS (`left`, `top`, `z-index`).
* **Sistema de Animação com CSS Sprites:** A animação dos personagens andando e trocando de direção foi feita combinando propriedades de `background-position` a um arquivo de imagem condensado (Sprite), gerenciado via JavaScript e CSS Variables.
* **Sistema de Radar (Física e Matemática):**
  * Uso de trigonometria com a função `Math.atan2(y, x)` para calcular o arco e o ângulo entre o urso e os coelhos a fim de rodar a seta do radar na direção correta.
  * Uso do **Teorema de Pitágoras** (fórmula da distância euclidiana via `Math.sqrt(Math.pow(delta X) + Math.pow(delta Y))`) para calcular quais coelhos estão mais perto (ordenando os mais próximos) e a proximidade do urso em relação aos obstáculos.
* **Sistema de Colisões (Bounding Box Circular/Ponto):** Lógica inteligente que varre as "árvores", os limites do mapa e outros "atores" no ambiente, impedindo o jogador e os coelhinhos de ultrapassar as bordas e objetos, validando os passos antes da UI ser renderizada.
* **Padrões Parecidos com POO no Modelo de Agentes:** Separação das responsabilidades do `player` e criação instanciada e procedural de dezenas de `trees` e `bunnies` através de Arrays, gerando um mapa com posições randômicas a cada jogatina utilizando Vanilla JS.

## 💻 Como Rodar Localmente

Por usar Vanilla JS sem frameworks de build ou bundlers nativos:

1. Clone o repositório:
```bash
git clone https://github.com/kauaxp77/Jogo-Da-Amizade.git
```
2. Abra o arquivo `index.html` em qualquer navegador.
3. Jogue!

## 🎨 Autor(es)
Desenvolvido como projeto de estudo de Design Web e Lógica de Programação.
* _Kaua_ (GitHub: [@kauaxp77](https://github.com/kauaxp77))
