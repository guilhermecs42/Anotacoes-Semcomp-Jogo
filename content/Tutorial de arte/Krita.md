# Instalação

O [site oficial](https://krita.org/pt-br/download/) deve redirecionar você a instalar para o seu sistema operacional em uso.

No caso do Windows, você baixará um instalador, executá-lo, prosseguir algumas vezes, aceitar os termos de uso, escolher uma pasta para instalação, prosseguir mais vezes e após a instalação terminar aparecerá um atalho na sua Área de Trabalho. Caso não haja atalho, você pode apertar a tecla Windows e pesquisar "Krita" e criar o atalho e abrir o programa.

No caso do Linux, você baixará uma AppImage. Coloque ela no diretório que você quiser. Precisa dar permissão de execução ao arquivo. Você pode fazer isso pelo gerenciador de arquivos ou pelo terminal. 
- **Gerenciador:** clique com botão direto no arquivo e clique em "Propriedades". Vá para a aba "Permissões" e aperte na caixinha "Permitir executar arquivo como programa".
- **Terminal:** abra o terminal nesse diretório e digite o seguinte comando para dar permissão de execução ao arquivo (trocando o nome do arquivo pelo nome que estiver no seu computador):
```
chmod a+x krita-5.2.16-x86_64.appimage
```

Por fim, abra o Krita digitando `./krita-5.2.16-x86_64.appimage` (aperte Tab para autocompletar o nome) ou clicando no arquivo em um gerenciador de arquivos.

Para esse tutorial, me referirei ao Krita em inglês americano. A linguagem pode ser trocada na barra de menu, em **> Settings/Configurações > Switch Application Language/Mudar o idioma do aplicativo**

# Projetos

### Criar um projeto: 

**> New Image**. Defina um tamanho (altura/largura) para a imagem ou escolha uma opção pré-definida. A resolution (relação entre pixels na tela e centímetros no mundo real) não importa, pois não vamos imprimir nada. Escolha Color Model **RGB/Alpha**, Depth de **8-bit**, Profile **sRGB-elle-V2-srgbtrc.icc (Default)**.  **> Create**.

O Color Model é a representação matemática de cada cor. Escolher RGB/Alpha com depth de 8 bits significa que cada cor será salva como uma lista de 4 números variando de 0 a 255. Os três primeiros são a quantidade vermelho, verde e azul na cor, e o Alpha é a transparência da cor. Esse modelo é comumente representado em hexadecimal, começando por #.
Exemplos: 
 ![[Screenshot from 2026-03-19 21-58-43.png]] ![[Screenshot from 2026-03-19 21-59-26.png]]
![[Screenshot from 2026-03-19 22-01-41.png]] ![[Screenshot from 2026-03-19 22-01-18.png]]
Essa representação é preferida por computadores pois cada pixel na tela é composto por supixels vermelho, verde e azul. Então dizer o quanto cada supixel deve brilhar para representar uma cor é a forma natural de se comunicar com a tela.

O Color Profile relaciona cada lista de 4 números com uma cor real. Dependendo do Color Profile, um mesmo conjunto de 4 números pode representar cores um pouco diferentes, e algumas cores podem ser impossíveis de serem representadas. Para (tentar) colaborarmos efetivamente, precisamos usar as mesmas configurações. **> Settings > Color Management > Display** e **desative Use system monitor profile**.
### Salvar um projeto:

Um projeto pode ser salvo como projeto .kra para ser retomado posteriormente, ou exportado


# Interface




![[monitor550exportar550.png]]

![[monitor550exportarSRGB.png]]