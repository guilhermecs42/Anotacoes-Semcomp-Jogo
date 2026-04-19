
![[Screenshot from 2026-03-25 19-24-36.png | 300]]

Imagem: à esquerda, uma pincelada (dab). À direita, um traço (stroke), formado por várias pinceladas com um distanciamento. A pincelada é a marca carimbada por um clique, enquanto o traço é a linha formada automaticamente quando arrasta o mouse, carimbando várias pinceladas.

Uma Brush Engine é o software que recebe o input do mouse/caneta e calcula os parâmetros da pincelada para que o Krita saiba exatamente quais pixels colorir e como.

Vamos dissecar esse trecho da Toolbar:

![[brush-toolbar.png]]

O segundo quadradinho tem a miniatura do Brush atual:

![[segundo-quadradinho-brushtoolbar.png| 90]]

![[lista-pinceis.png]]

Clicando nele, temos uma lista (em ordem alfabética) dos pincéis disponíveis. **Rolar** para ver todos. **Botão esquerdo** para selecionar. **Botão direito** para ver o nome, atribuir ou remover tags ao pincel. Onde está escrito "Tudo" é possível filtrar por tag. Em baixo há uma barra de pesquisa.

Após selecionar um pincel (nesse caso, o "Basic mix"), você pode configurá-lo apertando o primeiro quadradinho:

![[primeiro-quadradinho-brushtoolbar.png| 90]] 
![[editor-de-pincel.-ponta.png]]

Vamos ler a imagem de cima para baixo, da esquerda para a direita.

No canto superior esquerdo, temos a miniatura do pincel, a pré-visualização *ao vivo* do traço, e o nome do pincel. À direita do nome do pincel, há um botão com ícone de lápis para mudar o nome. Abaixo do nome do pincel, há o nome da Brush Engine. À direita do nome da Brush Engine, há um botão para resetar a predefinição ao seu estado original (se você não mexeu em nada, esse ícone não aparece). 

No canto superior direito, podemos salvar a predefinição como um novo pincel ou substituir a original com a nova. Ambas os botões abrirão uma janela em que se pode editar a miniatura do pincel.

Abaixo desses botões, há um espaço em branco para rabiscar e testar a predefinição atual. Caso não esteja aparecendo, aperte o botão com a seta para a direita \[ > ] . Você pode ampliar ou diminuir esse espaço arrastando a borda esquerda ou direita. Abaixo desse espaço branco, há 4 botões para enchê-lo com coisas e 1 para limpá-lo (preenchê-lo com cor branca). O zoom desse espaço de rabisco corresponde ao zoom da imagem atual.

Do lado esquerdo temos várias opções, dividas em "Geral", "Cor", e "Textura". A opção selecionada na screenshot acima é a Ponta do Pincel, que é marca carimbada pela pincelada.
## Ponta do pincel

Pode ser de 3 jeitos: automática, predefinida, ou texto. Vamos falar dos parâmetros da Ponta de Pincel automática:

- Diâmetro: tamanho da pincelada. Um tamanho muito grande causa travamentos.
- Fator: estica a pincelada. 
- Desvanecer: o quão abruptas ou suaves são as bordas da pincelada [^1].
- Ângulo: a orientação da pincelada. É mais perceptível se o fator for baixo.
- Pontas: quantas pontas a pincelada tem. É mais perceptível se o fator for baixo.
- Aleatoriedade: afeta a uniformidade da distribuição de tinta na pincelada. Se alta, alguns pixels ficam mais coloridos do que outros.
- Densidade: afeta a quantidade total de tinta na pincelada. Se baixa, menos pixels ficam coloridos.
- Espaço: distância entre pinceladas individuais em um traço.
- Precisão: qualidade do rendering. Quanto maior, mais lento.

[^1]: Não percebi muita diferença entre desvanescer Horizontal e Vertical

Ao mesmo tempo que alteram-se esses parâmetros, a pré-visualização *ao vivo* do traço (canto superior esquerdo) altera-se também. À esquerda desses parâmetros, temos uma pré-visualização da pincelada. Abaixo, podemos selecionar o tipo de máscara, que diz respeito à opacidade da pincelada em função da distância ao centro dela. O tipo "Suave", por exemplo, permite definir uma curva de opacidade qualquer. Abaixo, podemos alternar o formato da máscara entre quadrado e círculo. Na prática, diminuindo o fator e alterando o número de pontas, podemos gerar muito mais formatos do que apenas quadrados e círculos. Exemplo:

![[pincelada-maluca.png]]

Vamos ver outra forma de definir a ponta do pincel, "predefinido".

![[Screenshot from 2026-04-16 18-48-17.png]]

Pode-se escolher uma imagem dentre várias em uma lista (muito parecida com a lista de pincéis) para ser a ponta. Também pode-se pesquisar por nome e filtrar por tag, adicionar e remover tags, etc. Abaixo da lista, há botões para:
 - Importar: inserir um arquivo de imagem como ponta do pincel. Escolha um nome apropriado para o arquivo antes de inserir, pois a lista está em ordem alfabética.
 - Carimbo: inserir a imagem (i.e. pintura) atual como ponta do pincel. 
 - Área de transferência: você pode copiar uma imagem e inseri-la aqui.
 - 🗑 : remover a ponta selecionada. Muito cuidado!
Ao lado da lista de pincéis, há parâmetros iguais aos explicados anteriormente. O modo de pincel é a forma como o Krita irá interpretar a imagem da ponta. Normalmente deve ser "Máscara Alfa". Ele vai interpretar os pixeis mais escuros da imagem da ponta como os pixeis em que a cor deve ser mais opaca na pincelada, e os pixeis mais claros da imagem da ponta como os pixeis mais transparentes da pincelada.

A ponta do pincel também pode ser um texto. A interface é bem explicativa então não abordaremos isso.
## Opções de pincel

Há várias opções que afetam a aparência de um traço. Elas podem variar em tempo real, dependendo de como o artista desenha o traço. Essa relação entre input (sinais do mouse/stylus) e output pode ser configurado da seguinte forma:

Do lado esquerdo temos as diferentes opções que determinam a aparência do traço, e as caixinhas para ativá-las e desativá-las. As únicas opções que estão sempre ativadas são "Opacidade" e "Fluxo" (a diferença será explicada em breve). Clique com o botão direito para bloquear uma opção (ela será aplicada em todos os pincéis).  À direita, temos uma lista de parâmetros que podem afetar a opção selecionada. Esses parâmetros se relacionam à forma como o artista desenha o traço ao vivo. À direita, há um gráfico de como a opção varia de acordo com o parâmetro. Você pode selecionar um gráfico pronto (clicando nos quadradinhos acima) ou clicar no gráfico para adicionar bolinhas e arrastá-las (ou especificar coordenadas nos eixos). Alguns parâmetros como pressão, ângulo, inclinação e rotação só podem ser obtidos com um stylus. Abaixo está um exemplo com vários traços desenhados com velocidades diferentes, afetando a sua opacidade de acordo com a curva estabelecida:

![[opacidade-variando.png]]

Também é possível fazer com que o traço revele uma textura. Você pode escolher uma textura (numa lista, em ordem alfabética, com barra de pesquisa, tag e tudo) ou adicionar/remover uma textura clicando nos botõezinhos em baixo da lista. À direita do botão "Textura", há o botão "Opções" que te permite configurar, entre muitas outras coisas, a escala do padrão (o quão grande são os detalhes).
 
![[padrao.png]]
## Opacidade vs Fluxo

A opacidade é a transparência do traço, enquanto o fluxo é a transparência da pincelada. Uma opacidade baixa significa que o traço todo fica difícil de distinguir. Um fluxo baixo significa que as extremidades do traço ficam suaves (degradê), pois as extremidades de um traço são regiões em que há menos sobreposição de pinceladas. A documentação oficial do Krita tem o seguinte diagrama:
![[opacidade-fluxo.svg | 600]]
