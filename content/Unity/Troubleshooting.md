**GameObject não aparece:** o Z dele é menor que o Z da câmera, tem um objeto entre ele e a câmera, ele está dentro de outro objeto (lembra que todos eles tem espessura) ou o objeto não tem sprite

**Variável pública ou com \[SerializeField] não aparece no Inspector:** o script não está compilando. Pode ser que algum outro script tenha um erro de compilação que está impedindo a compilação dos demais. 

**Áudio não está em loop**: o método AudioSource.playOneShot() não aceita vai repetir o áudio mesmo se AudioSource.clip é true. Use AudioSource.Play()