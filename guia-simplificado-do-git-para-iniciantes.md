# Guia simplificado

###1 Configurações iniciais do Git

**Baixando e instalando o Git**
```bash
https://git-scm.com/downloads
```

**Configura nome de usuário**
```bash
git config --global user.name nome-sobrenome
```

**Configura email de usuário**
```bash
git config --global user.email email@email.com.br
```

###2 Inicializando um repositório

**Inicializa o versionamento no respectivo diretório**
```bash
git init
```

###3 Comandos básicos para sobreviver

**Verifica o status do repositório**
```bash
git status
```

**Adiciona o arquivo para ser commitado**
```bash
git add arquivo.extensão
```

**Adiciona todos os arquivos para serem commitados**
```bash
git add .
```

**Commitando arquivos**
```bash
git commit -m "adicionar um comentário significativo"
```

**Editando a mensagem do último commit**
```bash
git commit --amend -m "mensagem do commit"
```

**Excluindo um commit local**
```bash
git reset --hard hash-commit
```
- Para encontrar o hash, você precisa rodar no terminal: `git log`.
- O hash é aquele número que aparece em `comit: xxxxxxx.`

**Visualiza alterações específicas**
```bash
git diff nome-do-arquivo.extensao
```

**Visualizando relatório de commits**
```bash
git log // todos os commits
git log --oneline // exibe log com hash e título do commit
```

**Enviando as modificações para o repositório remoto**
```bash
git push origin <branch>
```

**Puxando alterações do repositório remoto**
```bash
git pull origin <branch>
```

###4 Trabalhando com branchs

**Criando e locomovendo-se para uma nova branch**

```bash
git branch nome-branch

git checkout nome-branch // Acessando a nova branch

git checkout -b nome-branch // Criando e acessando uma nova branch (Prefiro esse)

git checkout --orphan nome-branch // Criando uma nova branch vazia
```
**Renomeando branches**
```bash
git branch -m nome-branch
```
**Deletando uma branch**
```bash
git branch -D nome-branch
```

**Revertendo alterações feitas em arquivos**
```bash
git checkout -- nome-do-arquivo.extensao
```

**Aplicando merge em branchs**
```bash
git merge nome-branch // precisa estar na branch de destino
```

**Visualizando todas as branches existentes no repositório**
```bash
git branch
```

**Deletando uma branch**
```bash
git branch -D nome-branch
```

**Exibir informações sobre o repositório remoto**
```bash
git remote show origin
```

**Enviando as modificações para o GitHub**
```bash
git push origin <branch>
```

## Trabalhando com Git no Servidor

**8.1 Iniciar versionamento no servidor**
```bash
git init --bare
```
**8.2 Clonando repositório do servidor**
```bash
git clone file:////nome-servidor/pasta-desenvolvimento/nome-repositorio
```
**8.3 Consultando nome do remoto (por padrão chama-se origin)**
```bash
git remote
```
**8.4 Enviando arquivos/modificações para o servidor**
```bash
git push origin <branch>
```