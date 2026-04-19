Operações sobre as camadas ou sobre a imagem (tela) toda podem demorar bastante para serem processadas. Não saia fazendo muitas de uma vez!

Área acoplável de camadas:

![[camadas-docker.png]]

Clique com o **botão esquerdo** no nome de uma camada para ==editá-la== (a camada atual fica com o nome em negrito). **Ctrl Clique** para ==selecionar mais camadas uma por uma== e **Shift Clique** para ==selecionar todas as camadas== num intervalo. Na barra em baixo da área acoplável, da esquerda para a direita, temos os seguintes comandos:

 - Adicionar nova camada acima da atual
 - Duplicar camada, criando uma cópia acima da atual
 - Mover camada atual para baixo
 - Mover camada atual para cima
 - Ver ou modificar propriedades da camada
 - Excluir camada

Para ==renomear a camada==, clique duas vezes ou aperte **F2**. À esquerda do nome de uma camada, há uma miniatura do conteúdo da camada. **Ctrl Clique** na miniatura para ==selecionar todo o conteúdo da camada==. À esquerda disso, há uma caixinha para ==(des)selecionar a camada==, sendo que no mínimo uma camada deve estar selecionada. À esquerda disso, há um ícone de olho que ==ativa e desativa a visibilidade== da camada. À direita do nome da camada, há três ícones: um cadeado, que ==bloqueia a camada== para não ser mais alterada; uma letra alfa, que faz a camada ==herdar o alfa das camadas abaixo== no mesmo grupo; e um quadriculado, que faz novos traços na camada ==herdarem o alfa da própria camada.== 

Ao selecionar múltiplas camadas, você pode ==agrupá-las== com **Ctrl G** e ==desagrupá-las com **Alt Ctrl G**==. À esquerda do nome do grupo há uma setinha para baixo que ==mostra e esconde as camadas== do grupo. É possível criar subgrupos dentro de grupos. Acima dos nomes das camadas, há um ==controle da Opacidade== da camada/grupo atual. A opacidade do grupo é multiplicada às opacidades de cada camada/subgrupo dentro do grupo. A opacidade de uma camada afeta a camada imediatamente acima no grupo se esta de cima tiver o "Herdar alfa" ativado. **Ctrl E** para ==mesclar as camadas== selecionadas em uma só. Operações com agrupamento e ordem de camadas pode ser feita simplesmente arrastando elas pelo painel.

Para entender o funcionamento do alfa entre as camadas, observe a imagem a seguir. Todas as opacidades são de 100%. A camada mais de baixo tem o desenho do número 1 vermelho. A camada acima tem um 2 verde. A camada acima tem um 3 azul. Então foi ativado o ícone de quadriculado na camada 3 e feito um traço amarelo. O "Herdar alfa" da camada 2 está ativado. Perceba que o verde da camada 2 está visível apenas no formato do número 1 desenhado na camada de baixo, e que o traço amarelo afetou apenas a região ocupada pelo número 3. Se a camada "Background" estivesse no mesmo grupo, então o "Herdar alfa" da camada 2 não faria diferença, pois a camada "Background" é toda branca com alfa = 100%.

![[exemplo-camadas.png]]

**Ctrl T** para selecionar e mover todo o conteúdo (não transparente) da camada.
Selecione uma área de uma camada e aperte **Ctrl X Ctrl V** para transferir para uma camada acima.
**Delete** para apagar os conteúdos das camadas selecionadas.
**Botão direito > Estilo da Camada** para adicionar sombras, brilhos, relevo, contorno, etc. Não vou explicar essas configurações pois são muitas e pouco úteis (suponho). Abaixo de Estilo da Camada, há quadradinhos coloridos para atribuir uma *etiqueta colorida* à camada. Algumas ferramentas podem filtrar as camadas por etiqueta.
# Modos de mistura

Obs: os efeitos de cada um são bem difíceis de entender e explicar. As explicações podem estar confusas ou até erradas. O melhor vídeo sobre esse tópico que eu encontrei é esse [aqui](https://youtu.be/orhiTEHBEs0?si=ZV_gzj8JZziRsf0q).

Se refere ao que acontece quando uma cor semitransparente é sobreposta sobre outra (ou a mesma) cor. Há duas formas de uma cor sobrepor a outra: ou dois traços na mesma layer se intersectam, dois traços em layers diferentes se intersectam. No primeiro caso, o blending mode é editado na barra de ferramentas, ou no Editor de Pincel. No segundo caso, o modo de mistura é editado na área acoplável de Camadas.

![[modos-de-mistura.png]]

As cores internamente são representadas por uma tripla de números entre 0 e 1, seguindo a ordem RGB (Vermelho, Verde, Azul). Cores cujos valores são 0 ou 1 são chamadas de puras. As cores puras podem ser primárias (vermelho, verde, azul), secundárias (amarelo, magenta, ciano) ou acromáticas (branco, preto).

Quando duas cores se sobrepõem, o Krita calcula a cor resultante a partir de fórmulas matemáticas, que são os modos de mistura, separados em alguns grupos.
### Mistura

- Normal: a cor de cima substitui a de baixo.
- Apagar: funciona como uma borracha, ele apaga as cores abaixo e deixa a região transparente.
- Sobrepor: faz com que o traço de cima seja distinguível da cor de baixo, mas não muito diferente. Se a cor de baixo for escura, a cor resultante tende a ser mais clara, e vice-versa. Isso é útil para desenhar detalhes e inscrições em objetos já iluminados e/ou coloridos, pois não é necessário ajustar a cor do pincel toda hora para que o detalhe desenhado não seja invisível ou exagerado.
### Escurecer

- Multiplicar: a cor resultante sempre é mais escura, mesmo se a cor escrita por cima for mais clara do que a de baixo. Cores em baixo são mais afetadas se forem claras do que escuras. Usado para adicionar sombras em objetos coloridos (basta usar a mesma cor por cima) e colorir uma imagem em escala de cinza ou lineart em preto e branco (nesse caso, a escala de cinza/lineart deve ficar em cima e a cor em baixo).
- Escurecer: a cor resultante é formada pela escolha dos menores valores RGB entre as duas cores. A cor de cima é plenamente visível onde a cor de baixo for clara, e invisível onde a cor de baixo for escura. Se ambas as cores forem escuras, o resultado é uma versão mais enegrecida da cor de baixo.
- Gravar: é como o multiplicar, mas a cor resultante é mais intensa. 
### Clarear

- Clarear: a cor resultante é formada pela escolha dos maiores valores RGB entre as duas cores. A cor de cima é plenamente visível onde a cor de baixo for escura, e invisível onde a cor de baixo for clara. Se ambas as cores forem claras, o resultado é uma versão mais branqueada da cor de baixo.
- Tela: É o contrário do multiplicar. A cor resultante é sempre mais clara. Cores em baixo são mais afetadas se forem escuras do que claras. Usado para adicionar brilho em objetos coloridos.
- Subexposição de cores: é como o clarear, mas a cor resultante é mais intensa.
### HSV
- Cor: A matiz da cor de baixo é sobrescrita pela cor de cima, mas os valores são preservados. Usado para colorir imagens em escala de cinza. Nesse caso, a imagem fica em baixo.
# Filtros

Na barra de menu, há um menu **"Filtrar"**. Os filtros são aplicados à camada atual. Em **"Ajustar"**, há vários filtros configuráveis para alterar a exposição (como o "Desviar"), saturação e cores ("Ajuste do HSV"). Há alguns filtros não configuráveis, que basta clicar para aplicar, como "Contraste Automático" e "Inverter".

Filtros das opções **"Ajustar"**, **"Artístico"** e **"Borrar"** parecem ser os mais úteis.