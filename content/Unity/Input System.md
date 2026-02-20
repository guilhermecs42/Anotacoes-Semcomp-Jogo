using UnityEngine.InputSystem

Em assets há um arquivo chamado InputSystem_Actions.inputactions. Clique nele para configurar os inputs do jogo.
À esquerda aparecem Action Maps, correspondendo a diferentes elementos do jogo. No meio aparecem Actions, diferentes ações que esse elemento pode tomar. 

Ao criar uma action, no painel da direita você muda o Action Type: button, value, pass-through. Control Type é o que o input vai gerar no Unity.
Em baixo da action, há Bindings para assinalar as teclas. Algumas opções prontas estão disponíveis.

Toda ação tem uma ou mais interações.
# Callbacks

Uma interação passa por 4 fases no decorrer do tempo:

waiting -  a interação está esperando algum input
started - a interação foi iniciada (i.e. algum input foi recebido)
performed - a interação foi concluída
canceled - não há input recebido

Apenas no momento em que a interação passa de um estágio para outro, uma ou mais funções definidas pelo programador podem ser chamadas.

# Prática

Em um script de um GameObject:
	Crie uma função que recebe um argumento InputAction.CallbackContext. Essa é a função que será executada quando a interação acontecer. É desse argumento que se lê o valor do input.
	.
	Para uma Action cujo Action Type é "value":
		obter o valor numérico do input com .ReadValue<ControlType>(). O Control Type é alterado em .inputactions

Adicione Componente PlayerInput ao GameObject: 
	Arrastar o arquivo .inputactions para o campo Actions.
	Selecionar o Default map 
	Behavior: Invoke Unity Events
	Clicar em Events, e então no Action Map que você quer associar ao GameObject. Abrirá a lista das ações.
	Clica no +, arrasta o próprio GameObject em questão. Do lado, selecione o script e a função dentro do script que será chamada quando aquele evento acontecer.
