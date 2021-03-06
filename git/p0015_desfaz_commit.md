# git checkout: Desfazendo commits

Uma forma de desfazer **commits** é usando o **checkout**.

Para voltar ao **commit** anterior, digite:

```
$ git checkout HEAD~1
```

- o símbolo **$** indica que você deve usar o **usuário comum** para fazer essa operação.

Aqui é importante notar que será criado um **branch temporário**.

![fluxo do git com o ramo temporário](img/p0015-0.png)

Você pode confirmar isso através do comando

```
$ git branch
```

O retorno será algo semelhante a:

![branch temporária](img/p0015-1.png)

Nesse ponto, você estará visualizando as alterações que foram feitas até esse **commit**.

Após fazer os testes e/ou alterações, basta fazer o commit. Aqui será apresentado uma chave ao lado do commit. Exemplo:

![chave do commit](img/p0015-2.png)

Para não perder as informações é necessário criar um novo **branch**, desse jeito:

```
$ git branch nome_do_novo_ramo chave_do_útimo_commit
```

Em seguida basta ir até o novo **branch** criado com o comando

```
$ git checkout nome_do_novo_ramo
```

tags: checkout, git, commit, head
