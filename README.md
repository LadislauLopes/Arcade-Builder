# Arcade Builder

Ferramentas para planejar a arte de um controle arcade antes de mandar fazer:
um editor que roda no navegador e modelos 3D de oito controles no Blender.

**Abrir o editor:** https://ladislaulopes.github.io/Arcade-Builder/

![Os oito modelos](modelos/todos-os-modelos.jpg)

## Ateliê do Controle (editor)

O editor está em [`index.html`](index.html). É um arquivo só, sem build.

- Escolha o modelo (MINI, BASIC, SLIM, PRO XL e a linha FLAT) e um dos 36 layouts.
- Suba a arte do topo, das pontas e da frente/fundo. Arraste para posicionar, use zoom, gire ou espelhe.
- Se quiser, ponha arte também na base, a placa de baixo. Ela aparece na vista "Baixo" do 3D e só vai para os arquivos quando tem arte. Confirme com a loja se ela imprime a base.
- Ajuste brilho, contraste e saturação de cada arte, ou mostre a imagem inteira com um fundo de cor ou desfocado.
- Escreva um texto (seis fontes, inclusive japonesa) ou ponha um logo por cima da arte e arraste para posicionar.
- Use "Sugerir cores pela arte" para ver as cores Sanwa mais parecidas com a arte e três combinações prontas.
- Veja o resultado em 3D, com os furos dos botões, do stick e dos parafusos no lugar certo.
- Pinte cada botão com as cores Sanwa (ou as capas low-profile da linha FLAT) e escolha a cor do bat-top.
- Baixe os PNGs em 300 DPI prontos para a gráfica, num `.zip` com um `LEIA-ME.txt` que traz as medidas e a lista de botões.
- Baixe um vídeo do controle dando uma volta e terminando parado na vista de cima, para mostrar a ideia para alguém (12 segundos). Se a base tiver arte, o vídeo passa por baixo do controle também (21 segundos). Sai em MP4 no Chrome, no Edge e no Safari, e em WEBM no Firefox.
- Use "Copiar pedido" para levar à loja um texto com o modelo, o layout, a altura da lateral e os botões com as cores.
- Salve o projeto num arquivo `.atelie` (em **Projeto**) e abra em outro computador. Ele leva as artes originais, os ajustes, os textos, os logos e as cores.

### Como usar

Abra o link acima ou o `index.html` direto no navegador. Ele precisa de
internet para carregar o three.js e o JSZip (do cdnjs) e as fontes (do Google
Fonts).

As imagens e os ajustes ficam salvos só no seu navegador (IndexedDB). Nada é
enviado para nenhum servidor. Para levar o trabalho para outro computador ou
guardar uma cópia, salve o projeto em `.atelie`.

O endereço guarda o modelo e o layout escolhidos (por exemplo `#proxl-dual`
ou `#slim-keyboard`), então dá para mandar o link de uma configuração
específica. As artes não vão junto no link.

## Modelos 3D (Blender)

| Pasta | O que tem |
| --- | --- |
| [`modelos/blender/`](modelos/blender/) | Os 8 modelos, um `.blend` cada, mais `todos-os-modelos.blend` com todos lado a lado |
| [`modelos/previas/`](modelos/previas/) | Render de cada modelo |
| [`modelo-novo/final/`](modelo-novo/final/) | PRO XL com layout hitbox, 12 botões de 30 mm, stick bat-top e 6 botões laterais |
| [`modelo-novo/versoes-anteriores/`](modelo-novo/versoes-anteriores/) | Versões anteriores do mesmo controle |

Os arquivos foram salvos no Blender 5.2 e renderizam em Cycles com a câmera
já posicionada. As medidas estão em milímetros. O case tem 50 mm de altura no
total. As paredes têm 40 mm e ficam 6 mm para dentro das placas de acrílico.
Esse recuo é uma estimativa, então confirme com quem vai fabricar antes de
imprimir.

### Colocando a sua arte

Os modelos vêm com uma textura cinza neutra (`sem-arte.png`) no lugar das artes.
Para testar a sua:

1. Abra o `.blend` e vá na aba **Shading**.
2. Selecione o material da superfície:
   - pasta `modelos`: `arte_topo`, `arte_pontas` e `arte_frente_fundo`;
   - pasta `modelo-novo`: `top_art`, `side_art` e `front_art`.
3. No nó **Image Texture**, troque `sem-arte.png` pela sua imagem.

Os PNGs exportados pelo editor já saem no tamanho e na proporção de cada
superfície.

## Aviso

Projeto pessoal. As medidas são aproximadas, então confira tudo com quem vai
fabricar antes de encomendar.
