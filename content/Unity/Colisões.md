Nem toda colisão interrompe o movimento, você pode apenas detectar a sobreposição entre dois objetos para realizar uma ação
# Parents & Childs

Child World Position = Parent World Position + Child Local Offset

Quando o parent se move, a child é teleportada para ele, de acordo com o offset. Isso significa que Colliders e RigidBody PARA COLISÃO NÃO DEVEM FICAR NA CHILD, pois o sinal para parar o movimento será ignorado.
# Colliders & RigidBody

Um componente Collider é uma hitbox, detecta quando outro Collider encosta nele.
A caixinha "Is Trigger" desativa a interrupção do movimento.
Numa colisão que muda o movimento, o objeto afetado deve ter um componente RigidBody
Um objeto estacionário (como uma parede) precisa apenas do Collider.
Um RigidBody pode ser de três tipos:
- Static: não sofre forças físicas, o que inclui gravidade e colisões, e não pode ser movido por script. Objetos sem RigidBody mas com Collider também são "Static" (de alguma forma). Tecnicamente, um script pode mudar a sua posição diretamente, mas isso é ineficiente.
- Kinematic: não sofre forças físicas, assim como o static, mas pode ser movido por script diretamente. Como tem massa infinita, empurra todos os Dynamic Objects pelo caminho.
- Dynamic: sofre forças físicas, gravidade e colisões. Possui massa limitada. Pode ser movido por script diretamente e indiretamente (a partir de forças físicas).
# Como mover objetos

- Static: não devem ser movidos, mas é possível com transform.position = <vetor 3D>. Colisões no meio do caminho não são detectadas.
- Kinematic: RigidBody.MovePosition(<vetor 3D>). Um componente RigidBody é necessário para que a Unity possa analisar a trajetória entre a posição antiga e a posição nova para detectar colisões.
- Dynamic: .linearVelocity = <vetor 2D>, .AddForce(<vetor 2D>)



Use a função void FixedUpdate() para rodar o código a intervalos regulares independente do FPS.



Você pode alterar os pontos que formam o EdgeCollider2D em Points. O formato dos pontos sofre com a position, rotation e scaling.
É bom que objeto com que o player colide tenha uma tag para o script da colisão no player possa identificar com que colidiu.

Exemplo (a função específica pode mudar):
```C#
private void OnTriggerEnter2D(Collider2D collision){
	if(collision.tag == "Parede"){
		// player para
	}
}
```
Essa função funciona para qualquer componente Collider, desde que seja 2D.


Edit > Project Settings > Physics2D > Layer Collision Matrix
Lá você pode desativar colisões entre objetos que pertençam a layers diferentes