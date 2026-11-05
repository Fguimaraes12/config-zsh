# config-zsh

Backup/exportação das suas configurações do Zsh + Oh My Zsh + Powerlevel10k.

## Conteúdo

- `.zshrc` — configuração principal do Zsh/Oh My Zsh: PATH, tema, plugins, aliases e `source` do Powerlevel10k.
- `.p10k.zsh` — configuração visual do Powerlevel10k: segmentos, cores, separadores, degradês, ícone do Debian, diretório, horário, etc.
- `.fzf.zsh` — integração do fzf usada pelo `.zshrc`.
- `oh-my-zsh-custom/` — sua pasta `~/.oh-my-zsh/custom`: temas e plugins customizados, incluindo o Powerlevel10k.

## Como restaurar em outra máquina/usuário

1. Instale dependências:

   ```zsh
   sudo apt update
   sudo apt install zsh git curl fzf
   ```

2. Instale o Oh My Zsh:

   ```zsh
   sh -c "$(curl -fsSL https://raw.githubusercontent.com/ohmyzsh/ohmyzsh/master/tools/install.sh)"
   ```

3. Copie os arquivos de volta:

   ```zsh
   cp .zshrc ~/.zshrc
   cp .p10k.zsh ~/.p10k.zsh
   cp .fzf.zsh ~/.fzf.zsh
   mkdir -p ~/.oh-my-zsh
   cp -a oh-my-zsh-custom ~/.oh-my-zsh/custom
   ```

4. Recarregue:

   ```zsh
   exec zsh
   ```

## Observações

- A pasta `~/.oh-my-zsh/custom` contém temas/plugins instalados manualmente, como o Powerlevel10k.
- O Oh My Zsh oficial em `~/.oh-my-zsh/plugins` e `~/.oh-my-zsh/themes` não foi copiado porque é reinstalado pelo instalador oficial.
- `.zsh_history` e `.cache/` não foram copiados de propósito.
- Se o ícone do Debian não aparecer corretamente, instale uma Nerd Font, por exemplo MesloLGS NF: <https://github.com/romkatv/powerlevel10k#meslo-nerd-font-patched-for-powerlevel10k>
