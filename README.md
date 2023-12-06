# Resumo do curso de Git

Markdown com resumo do curso de Git e GitHub da DIO.

## 🔧 Configurações iniciais
```
git config --global user.name "Nome"
git config --global user.email "email@exemplo.com"
git config --global init.defaultBranch main
```

## 👨‍💻 Comandos

## init
```
git init (comando para inicializar/ criar um repositorio Git)
```

## clone
```
git clone <URL> (clonar um repositório direto do GitHub)
git clone <URL> --branch <branch> --single-branch (clonar uma branch para o repositorio local)
```

## status
```
git status (checar o status do Git)
```

## add
```
git add (adiciona arquivos e prepara para o commit)
```

## commit
```
git commit -m "msg" (criar um commit com uma mensagem)
git commit --amend -m "msg" (renomeia o commit)
```

## restore
```
git restore <file> (restaura as mudanças de um arquivo)
```

## log
```
git log (mostra o log do commit)
```

## reset
```
git reset --op <hash> (desfaz um commit)

op pode ser: 
soft: 
mixed:
hard: Retorna os arquivos até aquele commit selecionado
```

## remote add
```
git remote add origin <URL> (conecta com o repositorio remoto)
```

## push
```
git push -u origin main (envia o commit para o repositorio remoto)
```

## pull
```
git pull (puxa as alterações do repositorio remoto para o local)
```

## checkout
```
git checkout -b <branch> (cria um branch)
git checkout <branch> (muda para a branch desejada)
```

## merge
```
git merge <branch> (mescla a branch selecionada para a main)
git merge origin/main (mescla o repositorio remoto com o local)
```

## branch
```
git branch (vê as branch existentes)
git branch -v (vê o último commit de cada branch)
git branch -d <branch> (deleta a branch selecionada)
```

## fetch
```
git fetch origin main (baixa repositorio remoto sem mesclar com o local)
```

## 📗 Convenção de Commits

| Tipo de Commit | Descrição                                                                                                 |
| -------------- | --------------------------------------------------------------------------------------------------------- |
| `feat`         | Adiciona uma nova funcionalidade ao projeto.                                                              |
| `fix`          | Corrige um bug ou problema no projeto.                                                                    |
| `docs`         | Altera a documentação do projeto. Ex.: README, comentários no código.                                     |
| `style`        | Realiza mudanças na aparência, sem alterar a funcionalidade.                                              |
| `refactor`     | Realiza mudanças no código que não alteram a funcionalidade.                                              |
| `test`         | Adiciona ou modifica testes no projeto.                                                                   |

##### Exemplo commit

`feat: adicionado novo arquivo`
