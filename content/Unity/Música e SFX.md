Componentes AudioSource são como canais. Cada uma pode tocar um áudio por vez;
A classe AudioClip armazena arquivos de áudio, que podem facilmente ser atribuídos pelo Inspector.

AudioSource.PlayClipAtPoint(AudioClip, Vector3, float) : cria um GameObject temporário com AudioSource para tocar o áudio definido
AudioSource.PlayOneShot(AudioClip) : usa a AudioSource para tocar o áudio definido somente uma vez, sem poder parar ou loopar.
AudioSource.clip : é o AudioClip que será reproduzido pela AudioSource
AudioSource.Play() : usa a AudioSource para tocar o AudioClip que ela contém
AudioSource.Stop() : para o áudio reproduzido pela AudioSource

Crie um Empty Object para gerenciar o áudio. Crie um script nele.
Crie duas variáveis privadas do tipo AudioSource, uma para a música e outra para o SFX.
Crie múltiplas variáveis públicas do tipo AudioClip, uma para cada SFX do jogo.
Deixe todas essas variáveis visíveis ao Inspector.

Adicione dois filhos ao objeto, e adicione um componente AudioSource em cada um, um para a música e outro para o SFX. Os componentes poderiam ser adicionados ao pai, mas distribui-los para os filhos evita confundi-los no futuro.

Arraste os objetos para o Inspector no script do pai, nos campos referentes aos AudioSource.
Arraste os arquivos de áudio para os campos referentes aos AudioClip.

No script do pai:
```C#
varaudiosource.clip = varaudioclip; // atribui um som a um audiosource
varaudiosource.Play(); // toca a audiosource
```

Para SFX:

```C#
public void PlaySFX(AudioClip clip){
	varaudiosource.PlayOneShot(clip); // quando a função é chamada, toca o SFX
}
```

Essa função é pública para ser chamada em qualquer script.

https://youtu.be/DU7cgVsU2rM?si=lnOa7KtlHM9BzAnk

