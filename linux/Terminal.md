# Introdução

Um profissional da computação precisa saber interagir com o sistema operacional por meio de um terminal e muitas são as razões para isso:

- nem sempre um sistema de janelas estará disponível com formulários e assistentes de configuração;

- acessos remotos para administração de servidores ocorre normalmente via terminal;

- possibilita a criação de scripts para automação de tarefas, conhecer  os comandos é essencial.

O terminal básico fornecido pelo sistema operacional pode não parecer produtivo, mas isso não quer dizer que não podemos configurá-lo para melhorar a produtividade.

Recomendo pesquisar sobre:

[Tilix](https://gnunn1.github.io/tilix-web/): terminal com recursos avançados;

[Zsh](https://zsh.sourceforge.io/): interpretador de comando para shell;

[Oh My Zsh](https://ohmyz.sh/): framework para gerenciar as configurações do shel Zsh, com diversos plugins e temas.



# Instalando o Zsh

Para instalar o Zsh:

```bash
sudo apt install zsh
```

Para torná-lo o shell padrão sempre que o terminal for aberto:

```bash
chsh -s $(which zsh)
```

# Instalando o Oh My Zsh

```bash
sh -c "$(curl -fsSL https://raw.githubusercontent.com/ohmyzsh/ohmyzsh/master/tools/install.sh)"
```

ou

```bash
sh -c "$(wget https://raw.github.com/ohmyzsh/ohmyzsh/master/tools/install.sh -O -)"
```

O arquivo **~/.zshrc** passa a ser o arquivo de configuração do shell e não mais o **~/.bash_profile** ou derivados.

Encerre o terminal e abra-o novamente para visualizar a aplicação das novas alterações.

## Instalando Plugins

São muitos os plugins disponíveis para instalação. Veja a lista em [Oh My Zsh Plugins](https://github.com/ohmyzsh/ohmyzsh/wiki/Plugins).

Vamos abordar alguns plugins famosos.

### zsh-syntax-highlighting

Plugin que destaca em cores se o comando digitado está correto ou incorreto. Para instalar:

```bash
git clone https://github.com/zsh-users/zsh-autosuggestions \$ZSH_CUSTOM/plugins/zsh-autosuggestions
```

### zsh-autosuggestions

Sugere comandos baseado no histórico de comandos já executados. Para instalar:

```bash
git clone https://github.com/zsh-users/zsh-autosuggestions ${ZSH_CUSTOM:-~/.oh-my-zsh/custom}/plugins/zsh-autosuggestions
```

### fzf

Buscador de arquivos interativo. Para instalar:

```bash
git clone --depth 1 https://github.com/junegunn/fzf.git ~/.fzf && ~/.fzf/install
```

Responda sim para todas as perguntas.

Para pesquisar arquivos e pastas, pressione as teclas **CTRL + T + nome do arquivo** e, para pesquisar por comandos, digite **CTRL + R + comando desejado**.

Digite `**` e pressione **TAB** duas vezes para listar todos os arquuivos e filtrar.

## Ativando os plugins

Para ativar os plugins instalados faz-se necessário editar o arquivo **~/.zshrc** e editar a linha sobre plugins com a lista de plugins desejados:

```vim
plugins=(git zsh-syntax-highlighting zsh-autosuggestions fzf)
```

Após salvar o arquivo basta encerrar o terminal e abrir novamente para ver aplicadas as novas configurações.

