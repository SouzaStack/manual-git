# Manual Prático de Git e Github

Este repositório contém um guia prático baseado no tutorial "[Como usar Git e GitHub na prática](https://www.youtube.com/watch?v=UBAX-13g8OM&list=PLhkO7OMKgT_rqwGYldqcFxyN4yjFgmDh8)" do canal [Rafaella Ballerini](https://www.youtube.com/@rafaellaballerini). Aqui, você encontrará um passo a passo detalhado dos conceitos e comandos abordados no vídeo,  além de anotações pessoais que ajudam a reforçar e revisar o aprendizado sobre `Git` e `GitHub`.

## Criando um novo projeto
1. Crie uma pasta com o nome do projeto ex: "**manual-git**"
2. Abra o Visual Code nessa pasta
3. estreie o projeto inicial e salve-o

Agora é hora de usarmos o **Git**

4. Utilize o terminal **Git** de sua escolha
5. inicialize o repositório `git init`

Na pasta do seu projeto **manual-git** sera criado uma pasta chamada `.git` e é ali que contem toda a funcionabilidade **Git**, então não apague.

6. `git add <arquivo>` O comando `git add` prepara as alterações de um arquivo, movendo-as para a área de **staging**, onde ficam prontas para o _commit_. Ele é essencial para indicar ao **Git** quais alterações devem ser incluídas no próximo _commit_.

`git add README.md` Isso adiciona o arquivo `README.md` à área de staging.  
`git add .` Adicionar todos os arquivos modificados.    

- `git branch -M "main"` Este comando renomeia a branch principal do repositório de `master` para `main`. Essa **mudança** é **recomendada** para promover uma nomenclatura mais inclusiva e alinhada às práticas modernas adotadas por plataformas como o **GitHub**.
8. `git commit -m "minha descrição"` Utilizando este comando, você registra as alterações realizadas no repositório, associando uma mensagem que descreve claramente as modificações efetuadas. Mensagens de _commit_ bem elaboradas são essenciais para manter um histórico de alterações organizado e compreensível. 

## Interfaces Gráficas do Git

​Após realizar um _commit_, é comum querer visualizar de forma mais intuitiva o estado atual do projeto e as alterações implementadas. Embora o **Git** seja amplamente utilizado via linha de comando, diversas interfaces gráficas estão disponíveis para facilitar essa visualização. Essas ferramentas permitem examinar o histórico de _commits_, comparar versões e identificar alterações específicas. Para uma visão abrangente dos tipos de [interfaces gráficas disponíveis](https://git-scm.com/downloads/guis).

# Enviando seu repositório local para o GitHub

1. Crie um novo repositório no **GitHub**.
2. No campo "**Repository name**", digite o nome do seu repositório local.
3. Não marque a opção "**README.md**" se você já tiver criado um arquivo com o mesmo nome localmente.
4. Clique em "**Create repository**".

## Alterando arquivo local ao repositório remoto no GitHub

Após criar o repositório no **GitHub**, você verá uma **URL** de acesso remoto do repositório. Ela será algo como `https://github.com/SeuUsuario/manual-git.git`. Agora, você precisa associar o repositório local ao repositório remoto.

1. `git remote add origin <link do repositório>` Isso adiciona o repositório do **GitHub** como um repositório remoto para o seu repositório local. O nome `origin` é o nome padrão usado para o repositório remoto principal.

Agora já temos o nosso repositório local conectado com o respositório do **Github**, porém o _commit_ que damos na máquina não sobe automaticamente para a plataforma para isso precisaremos fazer o primeiro **_push_** para o **GitHub**.

2. `git push -u origin main` Esse comando faz o **_push_** da sua branch `main` para o repositório remoto no **GitHub**. O `-u` configura o repositório remoto como o destino padrão para a sua branch main.

Após o **_push_** ser concluído, vá até o **GitHub** e recarregue a página do repositório. Você verá todos os seus arquivos, que você adicionou anteriormente.