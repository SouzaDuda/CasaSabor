# 🥘 CasaSabor

Repositório dedicado para a atividade de ESC II na FECAP, de versionamento de Git e Github.

## 👩‍💻 Integrantes do projeto

- [Andre Seiji Shiroma](https://github.com/Andreseij15) - 2ADS
- [Débora Mayumi ](https://github.com/DMayumi) - 2ADS
- [Felipe Rodrigues dos Santos Farias](https://github.com/felipenono) - 2ADS
- [Guilherme Ryuki Kawahira](https://github.com/GuiRyuki) - 2ADS
- [Lucas Kazuo](https://github.com/LucasKazuo-lol) - 2ADS
- [Maria Eduarda da Silva Souza](https://github.com/SouzaDuda) - 2MACCOMP

## 🧑‍🏫 Professor Orientador:

- Robson de Oliveira Cardoso

## 🔀 Versionamento

O projeto usa **Git** (versionamento local) e **GitHub** (repositório remoto), seguindo um fluxo com branches por funcionalidade. Todos os comandos abaixo são executados no **Git Bash**, dentro da pasta do projeto.

### 🌿 Estrutura de branches

| Branch | Função |
| --- | --- |
| `main` | Versão estável do projeto. Não se trabalha direto nela. |
| `b-<nome-da-tarefa>` | Branch de trabalho de cada integrante (ex.: `b-cafedamanha`). |

Fluxo geral: `main` → cria branch → alterações + commits → `push` → Pull Request → revisão → merge na `main`.

### 🚀 Primeiros passos (uma única vez)

```bash
# Clonar o repositório
git clone https://github.com/SouzaDuda/CasaSabor.git

# Entrar na pasta do projeto
cd CasaSabor

# Configurar nome e e-mail (mesmos do GitHub)
git config --global user.name "Seu Nome"
git config --global user.email "seu-email@exemplo.com"
```

### 🔁 Fluxo de trabalho do dia a dia

**1. Atualizar a `main` antes de começar**
```bash
git checkout main
git pull origin main
```

**2. Criar a sua branch e entrar nela**
```bash
git checkout -b b-nome-da-tarefa
```

**3. Fazer as alterações e conferir o que mudou**
```bash
git status        # arquivos alterados
git diff          # linhas alteradas
```

**4. Adicionar e commitar**
```bash
git add .                                   # adiciona tudo
git add brunch.html img/                    # ou só arquivos específicos
git commit -m "Adiciona página Brunch"
```

**5. Enviar a branch para o GitHub**
```bash
git push -u origin b-nome-da-tarefa         # primeiro push da branch
git push                                    # pushes seguintes
```

**6. Abrir o Pull Request no GitHub**

No repositório, clique em **Compare & pull request**, descreva o que foi feito, peça revisão de um colega e faça o **Merge** na `main`.

**7. Voltar para a `main` e atualizar**
```bash
git checkout main
git pull origin main
git branch -d b-nome-da-tarefa              # apaga a branch local já mesclada
```

### 🧰 Comandos úteis

| Comando | O que faz |
| --- | --- |
| `git status` | Mostra o estado dos arquivos |
| `git log --oneline` | Lista o histórico de commits resumido |
| `git branch` | Lista as branches locais (a atual tem `*`) |
| `git branch -a` | Lista também as branches remotas |
| `git checkout nome-da-branch` | Troca de branch |
| `git fetch` | Baixa novidades do GitHub sem mesclar |
| `git pull` | Baixa e mescla as novidades da branch atual |
| `git merge nome-da-branch` | Mescla outra branch na branch atual |
| `git restore arquivo` | Descarta alterações não commitadas de um arquivo |
| `git remote -v` | Mostra o endereço do repositório remoto |

### ⚠️ Resolvendo conflitos de merge

Se o Git avisar `CONFLICT`, abra o arquivo indicado, procure as marcações `<<<<<<<`, `=======` e `>>>>>>>`, escolha o conteúdo correto e remova as marcações. Depois:

```bash
git add arquivo-corrigido.html
git commit -m "Resolve conflito em arquivo-corrigido.html"
```

### ✍️ Padrão de mensagens de commit

Mensagens curtas, no presente e começando com um verbo de ação:

- `Adiciona página Jantar`
- `Corrige layout da página Almoço conforme o Figma`
- `Atualiza imagens do Café da Manhã`
- `Atualiza README com fluxo de versionamento`

### ✅ Boas práticas do time

- Nunca fazer commit direto na `main`.
- Uma branch para cada tarefa ou página.
- Dar `git pull` antes de começar a trabalhar.
- Commits pequenos e com mensagem clara.
- Conferir o `git status` antes de cada commit.

## 🛠 Estrutura de pastas

```
📁 CasaSabor (Pasta Raiz do Projeto)
│
├── 📄 index.html              (Página Home)
├── 📄 cafe-da-manha.html      (Página Café da Manhã)
├── 📄 brunch.html             (Página Brunch)
├── 📄 almoco.html             (Página Almoço)
├── 📄 jantar.html             (Página Jantar)
├── 📄 sobremesa.html          (Página Sobremesa)
├── 📄 README.md               (Documentação do projeto)
│
├── 📁 css
│   └── 📄 style.css           (O arquivo único de estilos)
│
└── 📁 img                     (Imagens das páginas e favicon)
```

## ▶️ Como executar

Não é necessário instalar nada. Basta abrir o arquivo `index.html` no navegador (ou usar a extensão **Live Server** no VS Code) e navegar pelo menu.
