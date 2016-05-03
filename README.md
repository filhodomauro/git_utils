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
