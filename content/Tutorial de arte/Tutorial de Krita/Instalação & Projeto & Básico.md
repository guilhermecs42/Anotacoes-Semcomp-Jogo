# Instalação

[Esse link](https://krita.org/pt-br/download/) deve redirecionar você ao botão de download para o seu sistema operacional.

No caso do Windows, você baixará um instalador, executá-lo, prosseguir algumas vezes, aceitar os termos de uso, escolher uma pasta para instalação, prosseguir mais vezes e após a instalação terminar aparecerá um atalho na sua Área de Trabalho. Caso não haja atalho, você pode apertar a tecla Windows e pesquisar "Krita" e criar o atalho e abrir o programa.

No caso do Linux, você baixará uma AppImage. Coloque ela no diretório que você quiser. Precisa dar permissão de execução ao arquivo. Você pode fazer isso pelo gerenciador de arquivos ou pelo terminal. 
- **Gerenciador:** clique com botão direto no arquivo e clique em "Propriedades". Vá para a aba "Permissões" e aperte na caixinha "Permitir executar arquivo como programa".
- **Terminal:** abra o terminal nesse diretório e digite o seguinte comando para dar permissão de execução ao arquivo (trocando o nome do arquivo pelo nome que estiver no seu computador):
```
chmod a+x krita-5.2.16-x86_64.appimage
```

Por fim, abra o Krita digitando `./krita-5.2.16-x86_64.appimage` (aperte Tab para autocompletar o nome) ou clicando no arquivo em um gerenciador de arquivos.

# Projetos

### Criar um projeto: 

**> New Image**. Defina um tamanho (altura/largura) para a imagem ou escolha uma opção pré-definida. A resolution (relação entre pixels na tela e centímetros no mundo real) não importa, pois não vamos imprimir nada. Escolha Modelo **RGB/Alfa**, Profundidade de **8-bits**, Perfil **sRGB-elle-V2-srgbtrc.icc (Padrão)**.  **> Criar**.

As cores internamente são representadas por uma tripla de números entre 0 e 1. O que cada número significa depende do *modelo de cor*. No modelo RGB, o primeiro número é a quantidade de vermelho, o segundo é a quantidade de verde, e então azul. Exemplos: 
- (0, 0, 0) preto 
- (1, 1, 1) branco
- (1, 1, 0) amarelo
- (1, 0, 1) magenta
- (0, 1, 1) ciano
- (1, 0.5, 0) laranja
- (0.5, 0, 1) púrpura

No modelo RGB/Alfa ou RGBA, há um quarto valor para indicar a transparência da cor. Esse quarto valor é controlado pela *opacidade* do pincel, indo de 0% a 100%. A quantidade de valores possíveis para cada número na tripla/quadra RGB é determinada pela *profundidade*, que é o número de bits usado para representar cada número. Quando são 8 bits, há 256 valores possíveis. Esse formato é tão comum que muitas vezes dentro e fora do Krita, as cores são representadas por uma tripla de números de 0 a 255 que pode ser representada em hexadecimal (precedida de um #):

Exemplos: 
 ![[Screenshot from 2026-03-19 21-58-43.png]] ![[Screenshot from 2026-03-19 21-59-26.png]]
![[Screenshot from 2026-03-19 22-01-41.png]] ![[Screenshot from 2026-03-19 22-01-18.png]]

No Krita, a transparência ou opacidade de uma cor determina como ela fica mais forte quando passamos o brush de novo. Também determina o quanto as layers (camadas) abaixo ficarão visíveis. Exemplo de como a opacidade afeta a "força" da cor:

![[Screenshot from 2026-03-20 15-31-45.png || 200]]

Essa representação é preferida por computadores pois cada pixel na tela é composto por subpixels vermelho, verde e azul. Então dizer o quanto cada subpixel deve brilhar para representar uma cor é a forma natural de se comunicar com a tela.

Em fórmulas matemáticas, considera-se que os valores vão de 0 a 1 em vez de 0 a 255.

O Color Profile relaciona cada lista de 4 números com uma cor real, e tenta fazer a mesma cor ser exibida em diferentes monitores. Para (tentar) colaborarmos efetivamente, precisamos usar as mesmas configurações. **> Settings > Configure Krita > Color Management > Display** e **desative Use system monitor profile**. Além disso, verifique se o Color Profile no seu sistema operacional também é sRGB (não importa qual versão).
### Salvar um projeto:

Um projeto pode ser salvo em formato .kra para ser retomado posteriormente, ou exportado em diversos formatos de imagem. Tudo isso está na barra de menu **File**, que exibe os respectivos [[#Atalhos|atalhos]]. Usaremos .png, que aceita pixeis transparentes. Quando exportar, marque as caixas: 
![[Screenshot from 2026-03-20 01-14-22.png]]

# Básico

Imagem é como é chamado a tela em que se desenha. A imagem atual é o estado atual da pintura.

**Segure espaço e arraste** com o mouse para mover.
**Scroll** do mouse para dar zoom.
**M** inverte a visualização (útil para achar erros no desenho).
Use uma tool de desenho (B) e aperte o **botão esquerdo** para escolher o brush e mudar a cor.
**Shift + Espaço + arrastar**: rotaciona o canvas. Aperte **5** para restaurar o ângulo original.
**Tab** para ver apenas o canvas.
**Delete**: apaga os conteúdos da layer atual.
**> Image > Resize canvas**: aumenta ou diminui o espaço para desenhar
**> Image > Scale Image to New Size**: aumenta ou diminui o tamanho do pixel. 

**Shift e arrasta** para mudar o tamanho do brush.
**Ctrl** para pegar uma cor da tela.
**E** para transformar o brush numa borracha.