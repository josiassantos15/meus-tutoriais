# Configurar repositório remoto

## Passo 1: Preparar o projeto no VS Code
Crie uma pasta local

```bash
mkdir meus-tutoriais
cd meus-tutoriais
code .  # Abre o VS Code na pasta
```

Estrutura de pastas sugerida (no Explorer do VS Code):

```text
📁 meus-tutoriais/
├── 📁 pdfs/
├── 📁 imagens/
├── 📁 notas/
│    └── 📄 index.md  # Arquivo principal de links
└── 📄 README.md      # Descrição do repositório
```

Inicialize o Git (Terminal do VS Code: <kbd>Ctrl</kbd> + <kbd>`</kbd>):

```bash
git init
```

## Passo 2: Configurar os repositórios remotos
1. Crie um repositório no GitHub:

- Acesse github.com/new
- Nome: meus-tutoriais
- Não marque "Initialize with README"

2. Crie um repositório no GitLab:

- Acesse gitlab.com/projects/new
- Nome: meus-tutoriais
- Não marque "Initialize repository with a README"

## Passo 3: Vincular ao VS Code
No terminal do VS Code:

```bash
# Adicione GitHub como remote
git remote add github https://github.com/SEU_USUARIO/meus-tutoriais.git

# Adicione GitLab como remote
git remote add gitlab https://gitlab.com/SEU_USUARIO/meus-tutoriais.git

# Verifique os remotes
git remote -v
```

### Passo 4: Primeiro commit e push
1. Adicione os arquivos (PDFs, imagens, .md):

```bash
git add .  # Adiciona tudo
### OU para adicionar pastas específicas:
git add pdfs/ imagens/ notas/ README.md
```
2. Faça o commit:

```bash
git commit -m "Adiciona primeiros tutoriais e estrutura de pastas"
```
3. Envie para ambos os repositórios:

```bash
## Para GitHub
git push -u github main

## Para GitLab
git push -u gitlab main
```
Passo 5: Atualizações futuras
Sempre que adicionar novos arquivos:

```bash
git add .
git commit -m "Adiciona novos tutoriais de Angular"
git push github main
git push gitlab main
```