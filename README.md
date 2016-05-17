# Git Utils

## Configurando SSH

### Verificando a existência de uma chave
```
ls -al ~/.ssh
```

### Gerar uma nova chave SSH

```
ssh-keygen -t rsa -b 4096 -C "mauro.filho@gmail.com"
```

### Iniciar ssh-agent

```
eval "$(ssh-agent -s)"
```

### Adicionando a chave ao ssh-agent

```
ssh-add ~/.ssh/id_rsa
```
### Adicionando chave ssh à conta no github

Verificar helper [aqui](https://help.github.com/articles/adding-a-new-ssh-key-to-your-github-account/)

### Testar conexão

```
ssh -T git@github.com
```

## Inicializando um novo repositório

```
echo "# Git Utils"
git init
git add README.md
git commit -m "first commit"
git remote add origin git@github.com:filhodomauro/git_utils.git
git push -u origin master
```

## Clonando o repositório

```
git clone git@github.com:filhodomauro/git_utils.git
```
## Contribuindo com o repositório

### Criando uma branch
```
git checkout -b change_readme
```

### Adicionando arquivos alterados

```
git add --all
```

### Realizando o commit

```
git commit -m "Alterações no README"
```

### Realizando o push para a branch

```
git push origin change_readme
```

### Gerando um pull request

No github, após realizar o push para a branch, uma nova branch será criada no repositório. Com isso, clique em um dos botões para gerar o pull request "New Pull request ou Compare e pull request", em ambos você deverá colocar o comentário referente às alterações realizadas e confirmar a criação do pull request

### Merge do pull request

Ao acessar o repositório no github, haverá um pull request pendente na aba Pull requests,
acesso o registro e realize o merge através do botão "Merge pull request"

### Deletando a branch utilizada para as alterações

```
git checkout master
```

#### Deletando a branch local

```
git branch -d change_readme
```

#### Deletando a branch remota

```
git push origin --delete change_readme
```

## Desfazendo Coisas

### Revertendo add

Ao realizar esses comandos, os arquivos voltam para "untracked files"

```
git reset HEAD <file>
```

ou

```
git reset HEAD
```
