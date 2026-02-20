# Compilação

Todos os scripts são compilados juntos. Por isso, para que a alteração em um script se manifeste, é importante que nenhum outro script tenha um erro de compilação.
# Relação com Inspector

Escreva `[SerializeField]` antes de uma variável para torná-la visível e alterável pelo Inspector.
Escreva `[HideFromInspector]` antes de uma variável para torná-la invisível ao Inspector.

Variáveis `public` por padrão são visíveis e alteráveis pelo Inspector, exceto se forem declaradas com `[SerializeField]`.
Variáveis `private` não são visíveis a partir do Inspector, exceto se forem declaradas com `[HideFromInspector]`.
# Usando variáveis e funções de outro script

Para que variáveis e funções de um script possam ser usadas em outro script, elas precisam ser `public`.

Dentro de um script, para fazer referência a outro script e usar uma variável dele, crie uma variável pública cuja classe é igual à classe do script que você quer usar. Para atribuir o outro script a essa variável, há duas soluções: 
- arraste o Component ou GameObject do outro script para esse campo no Inspector.
- use o método .GetComponent\<ClasseScript\>() a partir de uma variável GameObject que contenha GameObject que executa o outro script.

Então use as coisas do outro script escrevendo essa variável, ponto, e o nome da variável/função.

Exemplo:

**Script 1:**
```C#
public class ScriptComVarEFunc : MonoBehaviour
{
	public int var = 3;

	public func(){
	
	}
}
```

**Script 2:**
```C#
public class ScriptQueUsa : MonoBehaviour
{
	public ScriptComVarEFunc outroscript;
	
	// Compile e arraste o Component ou GameObject do outro script para o campo
	// pertencente a variável acima no Inspector 
	
	outroscript.var = 4;
	outroscript.func();
}
```



Para usar uma variável pública de outro script, faça:
```C#
// Script 1

private NomeDoOutroScript script;
script.variavel;
```

Outra forma de fazer isso é:
```C#
public 
```

# Acessando um GameObject

Para acessar um determinado GameObject, um script deve estar na Hierarchy, isto é, também pertencer a outro GameObject. Não é possível acessar um GameObject específico em uma Scene a partir de um script que está apenas na pasta do projeto. Ele deve estar na Hierarchy também.