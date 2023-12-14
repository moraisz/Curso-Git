# Comandos do Git

Markdown com resumo do curso de Git e GitHub da DIO junto com conhecimento que coletei com estudos e pesquisas por fora, será usado o terminal para executar os comandos.

## 🔧 Configurações iniciais
```
git config --global user.name "Nome"
git config --global user.email "email@exemplo.com"
git config --global init.defaultBranch main
```

## 👨‍💻 Comandos essenciais

Para iniciar um repositório local, deve ser usado o comando `git init`:
```
git init
```

Após ser criado o repositório local, deve fazer a conexão com o remoto, usando o comando `git remote add`:
```
git remote add origin <URL>
```

Aconselho acompanhar o processo constantemente ao decorrer do processo, pra isso use o comando `git status`:
```
git status
```

para adicionar os arquivos e preparar o commit deve ser usando o comando `git add` e após, fazer o commit com `git commit`. Recomendo fazer o commit de grupos de arquivos separados, para fazer uma mensagem individual.
```
git add <arquivo>
git commit -m "mensagem"
```

Após esse processo, só falta fazer o push para o repositório remoto, para isso use o comando `git push`, como mostrado abaixo:
```
git push -u origin main
```

## 🧾 Comandos extras

### git commit --amend
```
git commit --amend -m "msg" (renomeia o commit)
```

### git clone
```
git clone <URL> (clonar um repositório direto do GitHub)
git clone <URL> --branch <branch> --single-branch (clonar uma branch para o repositorio local)
```

### git restore
```
git restore <file> (restaura as mudanças de um arquivo)
```

### git log
```
git log (mostra o log do commit)
```

### git reset
```
git reset --<op> <hash> (desfaz um commit)
```

op pode ser: 
* soft:  Move o branch atual para um commit específico, mas mantém as alterações do commit no índice 

* mixed (opção padrão se nenhuma opção for fornecida): Move o branch atual para um commit específico e remove as alterações desses commits do índice (staging area), mas mantém as alterações nos arquivos de trabalho.

* hard: Move o branch atual para um commit específico, descartando completamente todas as alterações posteriores desse commit.


### git pull
```
git pull (puxa as alterações do repositorio remoto para o local)
```

### git checkout
```
git checkout -b <branch> (cria um branch)
git checkout <branch> (muda para a branch desejada)
```

### git merge
```
git merge <branch> (mescla a branch selecionada para a main)
git merge origin/main (mescla o repositorio remoto com o local)
```

### git branch
```
git branch (vê as branch existentes)
git branch -v (vê o último commit de cada branch)
git branch -d <branch> (deleta a branch selecionada)
```

### git fetch
```
git fetch origin main (baixa repositorio remoto sem mesclar com o local)
```

## 📗 Convenção de Commits
Aqui está algumas boas práticas de commits:


| Tipo de Commit | Descrição                                                                                                 |
| -------------- | --------------------------------------------------------------------------------------------------------- |
| `feat`         | Adiciona uma nova funcionalidade ao projeto.                                                              |
| `fix`          | Corrige um bug ou problema no projeto.                                                                    |
| `docs`         | Altera a documentação do projeto. Ex.: README, comentários no código.                                     |
| `style`        | Realiza mudanças na aparência, sem alterar a funcionalidade.                                              |
| `refactor`     | Realiza mudanças no código que não alteram a funcionalidade.                                              |
| `test`         | Adiciona ou modifica testes no projeto.                                                                   |

Aqui está um exemplo de commit com boas práticas, recomenda-se fazer o comentário em inglês.
```
docs: Update README.md
```

