# Guia Completo - Git & GitHub para Iniciantes

## 1️⃣ Instalação do Git

Para utilizar o Git no seu computador, você precisa instalá-lo.

[🔗 Guia de instalação do Git](https://emalherbi.github.io/aulas/programacao-web/aula-7-git/#/)

Após instalar, verifique a versão do Git com:
```
git --version
```

## 2️⃣ Configuração Inicial

Após instalar, é necessário configurar o Git com seu nome e e-mail, que serão usados nos commits.

### Definir usuário e e-mail
```
git config --global user.name "Seu Nome"
git config --global user.email "seu@email.com"
```

### Verificar configurações atuais
```
git config --list
```
Essas configurações ficam armazenadas no arquivo **.gitconfig**, localizado no diretório do usuário:

📌 **Windows**: C:\Users\SEU_NOME\.gitconfig    
📌 **Linux/Mac**: ~/.gitconfig

## 3️⃣ Criando ou Clonando um Repositório

### Criar um novo repositório Git

Isso cria um novo repositório Git na pasta atual:
```
git init
```

Após esse comando, o Git passa a monitorar as alterações feitas nos arquivos da pasta.

#### Dica: Para iniciar um repositório já configurado para `main`, use:
```
git init -b main
```

### Clonar um repositório existente
Se o repositório já existe no GitHub, você pode baixá-lo no seu computador:
```
git clone link_do_repositorio
```

## 4️⃣ Controle de Arquivos

### Verificar o estado dos arquivos
```
git status
```

Esse comando mostra quais arquivos foram modificados e precisam ser adicionados ao Git.

### Adicionar arquivos ao staged

###### Adicionar todos os arquivos modificados
```
git add .
```

###### Adicionar um arquivo específico
```
git add meu_arquivo.txt
```

###### Adicionar um diretório específico
```
git add meu_diretorio/
```

### Fazer commit das alterações
```
git commit -m "Descrição da alteração"
```

## 5️⃣ Trabalhando com Branches

### Criar e mudar para um novo branch
```
git checkout -b nome_do_branch
```

### Trocar para um branch existente
```
git checkout nome_do_branch
```

### Enviar um branch para o repositório remoto
```
git push -u origin nome_do_branch
```

### Listar branches locais
```
git branch
```

### Renomear a branch principal para main
Este comando renomeia a branch principal do repositório de `master` para `main`. Essa **mudança** é **recomendada** para promover uma nomenclatura mais inclusiva e alinhada às práticas modernas adotadas por plataformas como o **GitHub**.
```
git branch -M main
```

### Excluir um branch local
```
git branch -D nome_do_branch
```

### Excluir um branch remoto
```
git push origin --delete nome_do_branch
```

## 6️⃣ Merge - Unir uma Branch à Principal (`main`)

### Passo 1: Trocar para a branch main
Antes de mesclar, sempre atualize a branch principal para evitar conflitos:
```
git checkout main
git pull origin main
```

### Passo 2: Fazer o merge do branch desejado
```
git merge nome_do_branch
```

### Passo 3: Resolver conflitos (se houver)
Se o Git detectar conflitos, edite os arquivos indicados e depois:
```
git add .
git commit -m "Resolvendo conflitos do merge"
git push origin main
```

### Passo 4 (Opcional): Excluir o branch que foi mesclado
```
git branch -D nome_do_branch
git push origin --delete nome_do_branch
```

## 7️⃣ Enviar e Atualizar o Repositório

### Enviar commits para o repositório remoto
```
git push
```

### Atualizar repositório local com mudanças do remoto
```
git pull
```

### Buscar alterações sem aplicá-las imediatamente
```
git fetch -p
```

## 8️⃣ Histórico e Logs
### Exibir histórico de commits
```
git log
```

### Exibir histórico resumido
```
git log --oneline --graph --all
```

### Exibir alterações recentes
```
git log -p -2
```

## 9️⃣ Stash - Guardar Alterações Temporariamente
Se precisar mudar de branch sem perder suas mudanças, use stash:

### Criar um stash
```
git stash
```

### Listar stashes salvos
```
git stash list
```

### Aplicar o último stash salvo
```
git stash apply
```

## 🔟 Comandos Rápidos
### Criar um branch e enviá-lo para o repositório
```
git checkout -b novo_branch
git add .
git commit -m "Alterações feitas"
git push -u origin novo_branch
```

### Voltar para a branch `main` e atualizar o repositório local
```
git checkout main
git pull
```

## 🔹 Git Alias (Atalhos de Comandos)
Você pode criar atalhos para comandos do Git, facilitando o uso no dia a dia.

### Editar o arquivo .gitconfig e adicionar:
```
[user]
  email = seu@email.com
  name = Seu Nome
[alias]
  ad = add .
  br = branch
  ch = checkout
  co = commit -m
  pl = pull
  ps = push
  rb = rebase origin/main
  st = status -sb
  up = pull
```

### Listar configurações do Git
```
git config --list
```

## 🎯 Contribuições
Esse guia é para iniciantes que estão aprendendo **Git** e **GitHub**. Se tiver dúvidas ou sugestões, sinta-se à vontade para contribuir! **Fork me**! 🚀

### Referências

- [Git Guides](https://github.com/git-guides/git-commit)

- [Git Book](https://git-scm.com/book/pt-br/v2/Fundamentos-de-Git-Obtendo-um-Reposit%C3%B3rio-Git)

- [Git Guia Prático](http://rogerdudler.github.io/git-guide/index.pt_BR.html)