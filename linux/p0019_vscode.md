# Instalando o VS Code pelo terminal

Primeiramente é preciso verificar a arquitetura do processador através do comando:

```
$ arch
```

Ou

```
$ uname -m
```

- **$** indica que você deve usar o **usuário comum** para fazer essa operação.

- **uname** serve para mostrar informações do sistema.

- o parâmetro **-m** indica o uname que queremos apenas como retorno a arquitetura da máquina.

No meu caso, é um sistema de 64 bits.

Para baixar o pacote, digite:

```
$ wget "https://go.microsoft.com/fwlink/?LinkID=760868" -O vscode.deb
```

> Para verificar o link da última versão do VS Code, visite a [página oficial](https://code.visualstudio.com/).

- **wget** é um programa para download de arquivos da web; ele suporta HTTP, HTTPS, FTP, entre outros.

- Os argumentos **-O** e **vscode.deb** para renomear o arquivo que está sendo baixado. **-O** O maiúsculo vem de output, seguido do nome do arquivo e sua extensão.

Para instalar o pacote digite no diretório onde o arquivo foi baixado:

```
$ sudo dpkg -i vscode.deb
```

- **sudo** serve para pedir permissões de administrador temporariamente.

- **dpkg** é o gerenciador de pacotes das distribuições baseadas em Debian.

- **-i** é o comando que indica instalação

Caso precise corrigir dependências, digite o comando:

```
$ sudo apt install -f
```

- **apt** do inglês, *Advanced Package Tool*, em português, Ferramenta de Empacotamento Avançada; é a ferramenta que nos ajuda na instalação, atualização e desinstalação de programas, entre outras funções.

- **install** é o comando de instalar, indicando ao apt o que fazer.

- o **-f** é um atalho para o comando **--fix-broken** que tenta fazer as correções de pacotes e dependências.

tags: linux, vscode, dpkg, instalacao
