# O comando cat

O comando **cat** é usado para unir, criar e exibir arquivos. O nome remete a "concatenate" ("concatenar" em inglês).

![code cat](./img/cat.jpg)

### Criando um novo arquivo com o cat

O comando cat permite a criação de novos arquivos de texto. Para isso utilize o operador de redirecionamento > para redirecionar o texto no arquivo. Exemplo:
```
$ cat > arquivo
[logo abaixo você poderá inserir seu texto. Pressione enter para quebra de linha ou para finalizar o documento e use control+C para sair]
```

### Visualizando o conteúdo de um arquivo

Esse comando lerá o conteúdo do arquivo e exibi-lo-á no terminal. Exemplo:
```
$ cat arquivo.txt
```
Muito útil para a leitura de logs e outros arquivos do sistema.

Adicionando o argumento **| more** o resultado mostrará as opções _“mostrar mais”_ ou _“mostrar menos”_. Exemplo:
```
$ cat arquivo.txt | more
[para mostrar a continuação do texto a cada enter]
```
```
$ cat arquivo.txt | less
[para mostrar o texto com uma barra de rolagem que pode ser controlada pelas setas do teclado. Para sair basta pressionar a tecla q.]
```

### Redirecionar Conteúdo

Ao invés de exibir os conteúdos no terminal, você pode redirecionar o resultado para outro arquivo com a opção >. O comando fica assim:
```
$ cat fonte.txt > destino.txt
```
Se o arquivo de destino não existir, o comando irá criá-lo ou sobrescrever o arquivo já existente com o mesmo nome.

Se você não deseja que o arquivo seja substituído, mas incrementado ao final, basta usar o comando **>>**. Exemplo:
```
$ cat fonte.txt >> destino.txt
```
Desse modo o arquivo fonte será anexado ao final do arquivo destino.

Para incrementar no modo de edição:
```
$ cat >> arquivo
```

### Concatenanado Arquivos

Para a concatenação de diversos arquivos em apenas um, siga o exemplo:
```
$ cat fonte1.txt fonte2.txt > destino.txt
```

### Exibindo o número de linhas

Para visualizar o conteúdo de um arquivo com o número das linhas, adicione **-n** como parâmetro. Exemplo:
```
$ cat -n arquivo
```

tags: linux, cat, concatenar, comando