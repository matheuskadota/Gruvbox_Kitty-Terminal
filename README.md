# 🖥️ Gruvbox Kitty-Terminal

> Setup completo do terminal **Kitty** com tema **Gruvbox** no **Fedora Linux (Laptop)**.

![Preview do Terminal](IMG/preview.png)

---

## 📦 Stack

| Ferramenta | Função |
|---|---|
| [Kitty](https://sw.kovidgoyal.net/kitty/) | Emulador de terminal (GPU-accelerated) |
| [Zsh](https://www.zsh.org/) | Shell interativo |
| [Starship](https://starship.rs/) | Prompt customizável (Powerline pills) |
| [Fastfetch](https://github.com/fastfetch-cli/fastfetch) | System info na abertura do terminal |
| [Nerd Fonts](https://www.nerdfonts.com/) | Ícones e glifos no prompt |

---

## 📂 Estrutura

```
.
├── kitty/
│   └── kitty-fedora.conf      # Paleta de cores Gruvbox para o Kitty
├── zsh/
│   └── zshrc-fedora            # Configuração do Zsh (aliases, histórico, starship init)
├── starship/
│   └── starship-fedora.toml   # Prompt Starship estilo Gruvbox Rainbow
├── fastfetch/
│   └── fastfetch-fedora.jsonc # Configuração do Fastfetch
└── IMG/
    └── preview.png             # Screenshot do terminal (em breve)
```

---

## 🚀 Restauração Rápida

### Pré-requisitos

```bash
# Instalar dependências no Fedora
sudo dnf install kitty zsh fastfetch util-linux-user

# Instalar Starship
curl -sS https://starship.rs/install.sh | sh

# Instalar uma Nerd Font (ex: JetBrainsMono)
# Baixe de https://www.nerdfonts.com/font-downloads
# Extraia os .ttf em ~/.local/share/fonts/ e execute:
fc-cache -fv

# Definir Zsh como shell padrão
chsh -s $(which zsh)
```

### Aplicar as configurações

```bash
# Clonar o repositório
git clone https://github.com/matheuskadota/Gruvbox_Kitty-Terminal.git
cd Gruvbox_Kitty-Terminal

# Kitty — cores Gruvbox
mkdir -p ~/.config/kitty
cp kitty/kitty-fedora.conf ~/.config/kitty/kitty.conf

# Zsh — configuração do shell
cp zsh/zshrc-fedora ~/.zshrc

# Starship — prompt customizado
mkdir -p ~/.config
cp starship/starship-fedora.toml ~/.config/starship.toml

# Fastfetch — system info
mkdir -p ~/.config/fastfetch
cp fastfetch/fastfetch-fedora.jsonc ~/.config/fastfetch/config.jsonc
```

### Reiniciar o Kitty

```bash
# Feche e reabra o Kitty para ver tudo funcionando ✨
```

---

## 🎨 Paleta Gruvbox (Dark)

| Cor | Hex |
|---|---|
| Background | `#32302f` |
| Foreground | `#ebdbb2` |
| Red | `#fb4934` |
| Green | `#b8bb26` |
| Yellow | `#fabd2f` |
| Blue | `#83a598` |
| Purple | `#d3869b` |
| Aqua | `#8ec07c` |

---

## 📝 Notas

- A fonte configurada deve ser uma **Nerd Font** para os ícones do Starship renderizarem corretamente.
- O `fastfetch` roda automaticamente ao abrir um novo terminal (configurado no `.zshrc`).
- O prompt Starship usa estilo **Powerline (pills)** com as cores Gruvbox.

---

<p align="center">
  Feito com ☕ por <a href="https://github.com/matheuskadota">@matheuskadota</a>
</p>
