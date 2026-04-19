# Interface
## Painéis

São painéis utilitários que podem ser arrastados para qualquer lugar da tela. **> Configurações > Painéis** mostra a lista completa. Os mais importantes são Predefinições de Pincel, Camadas, Opções da ferramenta, Caixa de Ferramentas. É possível arrastar um painel sobre outro e alterná-los pelas pequenas abas que aparecem em cima. Recomendo deixar os painéis "Opções da ferramenta" fixos em algum lugar. As imagens abaixo mostram como você pode arrastar painéis para ficarem livres (paleta na segunda imagem) ou fixos nos cantos (seletor de cores na segunda imagem).

![[Screenshot from 2026-03-20 11-10-21.png | 330]] ![[Screenshot from 2026-03-20 11-10-48.png | 330]]
## Caixa de Ferramentas & Barra de Ferramentas

A Barra de Ferramentas fica em cima da tela, abaixo da Barra de Menu. A Caixa de Ferramentas fica à esquerda, mas como ela é um painel, ela pode ser movida. Para cada uma das ferramentas, a painel Opções da ferramenta te permite configurar da forma como você quiser.
### Desenhar com pincel

Usaremos principalmente a primeira ferramenta, traços livres (atalho: **B**). Não há ferramenta específica de borracha. Aperte **E** para transformar o pincel numa borracha.

![[Screenshot from 2026-03-20 11-25-28.png|100]] ![[Screenshot from 2026-03-20 16-47-10.png|400]]
Mão livre, retângulo, elipse, polígono, polilinha, curva de Bezier (ninguém usa)

Opções da ferramenta: você pode escolher entre três modos de suavizar o traço: básico, pesado e estabilizador. Você também pode ativar "Aderir aos assistentes" para usar em conjunto com a seguinte ferramenta:

![[Assistente 1.png]]

Ela cria uma "trilha" na tela para que o pincel desenhe um traço bem definido. As opções da ferramenta mostram uma grande variedade de desenhos que podem ser facilitados. Primeiro crie o assistente na tela, e então use "Aderir aos assistentes" para traçar por cima. O "Magnetismo" é o quão ajustado o traço fica, e se "Ajustar à linha única" estiver desativado, você pode saltar de assistente em assistente com o pincel, conectando os formatos. Abaixo estão a elipse, perspectiva, elipse em perspectiva, régua e spline. Também há assistentes para perspectiva de 1, 2 e 3 pontos. 

![[Pasted image 20260419175236.png]]

Para remover os assistentes, clique de novo na ferramenta e clique nas latinhas de lixo do lado dos assistentes.
### Selecionar

As mais úteis são à mão livre (**S**) e a de seleção contígua (primeira da terceira linha). Ao selecionar uma área, os pinceles e gradientes serão aplicados apenas a essa área selecionada. **Arraste a borda** para mover a borda sem mover o conteúdo. **Ctrl D** desseleciona. **Ctrl H** esconde a borda da seleção. **Ctrl Shift I** inverte a área selecionada. **Ctrl X + Ctrl V** cria uma nova camada e transporta seleção para ela.

![[selecao.png|117]] ![[Screenshot from 2026-03-20 16-55-31.png | 400]]
Seleção em quadrado, em círculo, polígono livre, mão livre, contígua (cores adjacentes parecidas), por cor (cores parecidas, não necessariamente adjacentes)

Opções da ferramenta: 

![[Pasted image 20260419180641.png]]

Modo e Ação são opções aplicáveis a todas as ferramenta de seleção. O Modo pode ser seleção pixelada ou vetorial (contínua). Como a imagem sempre é pixelada, o modo vetorial tenta extrapolar um pouco as transformação realizadas na área selecionada para suavizar as bordas, dando impressão de curva contínua. A Ação se refere ao que acontece com a seleção quando você tenta selecionar outra área além da atual. Os ícones são autoexplicativos. Existem teclas para escolher a Ação enquanto seleciona:

 - Shift para adicionar
 - Alt para subtrair
 - Ctrl para substituir
 - Shift Alt para intersectar

As seleções em quadrado e círculo tem algumas opções bem simples que afetam o formato da área selecionada. As seleções contíguas e de cores semelhantes tem opções mais complexas que precisam ser explicadas.

![[Pasted image 20260419190218.png|304]]

- Referência: quais camadas o Krita deveria buscar por cores parecidas. A primeira opção seleciona apenas pixels na camada atual. A segunda seleciona todos os pixels de cor parecida em qualquer camada. A terceira filtra as camadas por etiquetas coloridas.
- Limiar: o quão parecida deve ser a cor do pixel (com a cor base que você clicou) para ele ser selecionado. Um limiar baixo seleciona apenas cores idênticas.
- Difusão: é a opacidade da seleção dos pixeis com cores muito diferentes da cor base. Uma baixa difusão faz esses pixeis serem selecionados com um pouco de transparência, de forma que pintar por cima deles não irá sobrescrever totalmente a cor original. Para entender melhor, veja a ferramenta de preenchimento.
- Fechar lacuna: é o comprimento mínimo que uma lacuna deve ter para a seleção poder atravessá-la. Um valor pequeno significa que a seleção se espalha por qualquer lacuna. Um valor alto é mais restritivo.

![[Fechar lacuna 2.png]]
 
 - Crescer: é o quanto a seleção vai ser extrapolada ou contraída. Um valor positivo faz uma "margem de erro", e um valor negativo faz um recuo.
 - Suavização: faz com que os pixeis da borda sejam selecionados de forma mais transparente. Novamente, é uma configuração mais fácil de ver na ferramenta de preenchimento.
### Transformação

Ao fazer uma seleção, você pode arrastar a borda da seleção em relação ao canvas, mas isso não arrasta o conteúdo. Para isso use as seguintes tools:

![[Screenshot from 2026-03-20 11-41-44.png]]

A primeira (**Ctrl T**) permite que você mova, gire, rotacione em 2D (e mude o eixo de rotação), em 3D (segurando Ctrl) e distorça o conteúdo selecionado. Apertar Ctrl T sem ter uma área selecionada faz selecionar toda a parte pintada da camada atual. Aperte Enter para finalizar a edição. A segunda (**T**) serve apenas para mover o conteúdo selecionado.

![[Pasted image 20260320131900.png]] ![[Screenshot from 2026-03-20 13-22-33.png]]
![[Screenshot from 2026-03-20 13-22-56.png]]

Degradê (**G**): você pode customizar as cores na Barra de Ferramentas. É o quarto quadradinho. Para adicionar uma cor customizada, clique em + Add... Nas Opções da ferramenta há degradê circular, espiral, etc. 

![[Screenshot from 2026-03-25 12-21-50.png |200]] ![[Screenshot from 2026-03-25 12-25-11.png | 240]]

Amostragem de cor (**P ou segure Ctrl com pincel**): pega uma cor da tela e aplica ao pincel. O pincel pode ter duas cores, alternadas pela tecla **X**. Essas estão no sexto quadradinho da barra. Clique para escolher manualmente as cores do pincel.

[Preenchimento](https://docs.krita.org/pt_BR/reference_manual/tools/fill.html#fill-tool): é o balde (**F**).