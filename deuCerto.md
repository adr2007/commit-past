```
$ git checkout --orphan NEWBRANCH
$ git rm -rf .
```

`--orphan` cria um novo branch, mas ele inicia sem qualquer commit. Depois de executar o comando acima, você estará em um novo branch "NEWBRANCH", e o primeiro commit criado a partir deste estado iniciará um novo histórico sem qualquer ancestralidade.

Você pode então começar a adicionar arquivos e enviá-los e eles ficarão em seu próprio branch. Se você der uma olhada no log, verá que ele está isolado do log original.

`git rm -rf .` é importante para que ao executar o comando `git status` não exista histórico que os arquivos da branch foram apagados e assim a nova branch apenas irá registrar o novo conteúdo do commit.