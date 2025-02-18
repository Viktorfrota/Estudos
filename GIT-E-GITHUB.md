eu criei esse repositório utilizando markdown no [Obsidian](https://obsidian.md/download) para estudo próprio ***(usei IA para ajudar a organizar pois nao domino essa linguagem de marcaçao)*, porem decidi disponibilizar para que seja usado por outros iniciantes, para que nao tenham que ficar horas lendo vários artigos e blogs como eu tive que fazer ,Segue abaixo meu bloco de estudos explicando passo a passo cada comando e conceito para que iniciantes possam estudar e compreender de forma obvia como o Git e o GitHub funcionam

---

# Guia e Revisão Completo de Git e GitHub para Iniciantes

Este guia tem o objetivo de apresentar os conceitos e comandos fundamentais do Git e do GitHub. Você aprenderá desde como iniciar um repositório local até como trabalhar com branches, reverter alterações e sincronizar seu trabalho com repositórios remotos. Sinta-se à vontade para praticar cada comando e consultar a documentação oficial para se aprofundar – e não se esqueça: até os comandos mais avançados podem ter um toque de humor para descontrair!

---

## 1. Introdução ao Git

**Git** é um sistema de controle de versão distribuído que permite gerenciar e acompanhar alterações em arquivos ao longo do tempo. Com ele, é possível trabalhar de forma colaborativa, criar ramificações para novas funcionalidades, reverter alterações e manter um histórico detalhado do projeto.

---

## 2. Repositório Local

Um **repositório local** é uma pasta no seu computador onde o Git guarda todos os arquivos do projeto, o histórico de alterações (commits) e metadados importantes.  
Veja como trabalhar com um repositório local:

### 2.1. Inicializando um Repositório

Para transformar uma pasta em um repositório Git, abra o terminal dentro da pasta e execute:

bash


`git init`

_O que faz:_ Cria um diretório oculto chamado `.git` onde o Git armazenará o histórico e as configurações do projeto.  
_Quando usar:_ Sempre que iniciar um novo projeto ou quando desejar versionar um projeto já existente.

### 2.2. Verificando o Status

Depois de modificar alguns arquivos (ou até se você quiser saber se esqueceu de salvar seu café no lugar certo), verifique o estado atual com:

bash


`git status`

_O que faz:_ Mostra quais arquivos foram modificados, quais estão prontos para serem commitados (staged) e quais ainda não são rastreados (untracked).  
_Importância:_ Ajuda a saber o que precisa ser adicionado ou ajustado antes de criar um commit – é como conferir se você realmente colocou os ingredientes antes de assar o bolo!

### 2.3. Adicionando Arquivos

Para que o Git comece a monitorar seus arquivos, adicione-os à _staging area_:

bash


`git add .`

_O que faz:_ "Prepara" os arquivos para o commit. Pense nisso como arrumar a bagunça antes de tirar uma foto de família.

### 2.4. Realizando um Commit

Crie um snapshot do seu projeto com:

bash


`git commit -m "Descrição clara do que foi alterado"`

_Dica:_ Use mensagens descritivas – se você renomear sua branch de "bugfix" para "solved-when-I-woke-up", seu colega pode rir (ou chorar) e, quem sabe, até resolver o bug junto!

### 2.5. Explorando o Histórico

Visualize o histórico de commits com:

bash


`git log`

_Utilidade:_ Permite rastrear mudanças e entender a evolução do projeto, como se fosse o diário secreto do seu código.

### 2.6. Revertendo Alterações

Caso precise voltar a um estado anterior, use o `git reset` ou explore o `git reflog` para ver todos os movimentos do HEAD.

---

## 3. Repositório Remoto e GitHub

Um **repositório remoto** é um local hospedado (como GitHub, GitLab ou Bitbucket) que permite a colaboração e a sincronização do seu trabalho.

### 3.1. Conectando com um Repositório Remoto

Associe seu repositório local ao remoto:

bash


`git remote add origin https://github.com/usuario/nome-do-repositorio.git`

### 3.2. Sincronizando Alterações

- **Enviar alterações:**
    
    bash
    
    
    `git push -u origin main`
    
- **Atualizar seu repositório local:**
    
    bash
    
    
    `git pull origin main`
    

### 3.3. Clonando um Repositório

Para obter uma cópia local de um repositório remoto:

bash


`git clone https://github.com/usuario/nome-do-repositorio.git`

---

## 4. Branches (Ramificações)

As **branches** permitem que você desenvolva novas funcionalidades sem afetar o código estável.

### 4.1. Criando e Alternando Entre Branches

- **Criar e mudar para uma nova branch:**
    
    bash
    
    `git checkout -b nova-branch`
    

### 4.2. Combinando Branches

Junte suas alterações com:

bash


`git checkout main git merge nova-branch`

Ou, se preferir um histórico mais limpo:

bash


`git checkout nova-branch git rebase main`

---

## 5. Comandos Avançados do Git (para os mais audaciosos!)

Se você já está confortável com o básico e quer dar uma espiadinha nos comandos avançados – sem perder o bom humor – confira essa seleção:

### Gerenciamento de Branches

- **Renomear uma branch:**
    
    bash
    
    `git branch -m antigo novo`
    
    _Exemplo engraçado:_ Se sua branch se chama "fix-bug" e, depois de tanto sofrimento, você resolve o problema, renomeie para "bug-is-gone" e comemore!
    
- **Deletar uma branch local (se ela já foi mesclada):**
    
    bash
    
    `git branch -d nome-da-branch`
    
    _Exemplo:_ Adeus, branch que cumpria seu papel como aquele ex que já não era mais necessário.
    
- **Deletar uma branch local, mesmo sem mesclagem:**
    
    bash
    
    `git branch -D nome-da-branch`
    
    _Nota:_ Use com cuidado – é como dar um "delete" definitivo na sua playlist de músicas ruins!
    
- **Deletar uma branch remota:**
    
    bash
    
    `git push origin --delete nome-da-branch`
    
    _Dica:_ É sempre bom limpar a bagunça do repositório, afinal, branches velhas acumulam poeira como louça na piakkkkkkk
    
- **Criar e mudar para uma nova branch:**
    
    bash
    
    `git checkout -b nova-branch`
    
    _Exemplo:_ É como sair para uma nova aventura: "Nova branch, nova vida!"
    

### Revisão e Alterações

- **Guardar alterações temporariamente:**
    
    bash
    
    `git stash`
    
    _Exemplo:_ Imagine guardar aquele lanche para depois – o stash guarda suas mudanças até você estar pronto para usá-las.
    
- **Recuperar as alterações guardadas:**
    
    bash
    
    `git stash apply`
    
- **Aplicar e remover do stash:**
    
    bash
    
    `git stash pop`
    
- **Listar stashes armazenados:**
    
    bash
    
    `git stash list`
    
- **Remover um stash específico:**
    
    bash
    
    `git stash drop stash@{n}`
    

### Histórico e Revisão de Commits

- **Visualizar o histórico de todas as branches numa linha só:**
    
    bash
    
    `git log --oneline --graph --all`
    
- **Ver as mudanças de cada commit:**
    
    bash
    
    `git log -p`
    
- **Filtrar commits de um autor específico:**
    
    bash
    
    `git log --author="Nome"`
    
- **Ver commits da última semana:**
    
    bash
    
    `git log --since="1 week ago"`
    

### Reescrevendo Histórico

- **Editar a última mensagem de commit:**
    
    bash
    
    `git commit --amend`
    
    _Exemplo engraçado:_ Se você escreveu "fix bugs" e depois percebeu que resolveu mais do que isso, edite para "all bugs ran away"!
    
- **Reescrever os últimos 3 commits interativamente:**
    
    bash
    
    `git rebase -i HEAD~3`
    
- **Desfazer o último commit, mantendo as alterações no stage:**
    
    bash
    
    `git reset --soft HEAD~1`
    
- **Desfazer o último commit, descartando as alterações:**
    
    bash
    
    `git reset --hard HEAD~1`
    

### Sincronização com Repositórios Remotos

- **Buscar alterações e limpar branches remotas deletadas:**
    
    bash
    
    `git fetch --prune`
    
- **Puxar alterações com rebase:**
    
    bash
    
    `git pull --rebase`
    
- **Forçar push com segurança:**
    
    bash
    
    `git push origin nome-da-branch --force-with-lease`
    

### Outros Comandos Úteis

- **Mostrar autores e quantidade de commits:**
    
    bash
    
    `git shortlog -sn`
    
- **Ver quem editou cada linha de um arquivo:**
    
    bash
    
    
    `git blame nome-do-arquivo`
    
- **Iniciar busca binária de bugs:**
    
    bash
    
    
    `git bisect start`
    

---

## 6. Fork: Trabalhando com Projetos de Terceiros

Um **fork** é uma cópia de um repositório de outro usuário. Permite que você faça alterações sem afetar o projeto original.  
_Fluxo básico:_

1. Clique em “Fork” no GitHub.
2. Clone seu fork:
    
    bash
    
    `git clone https://github.com/seu-usuario/nome-do-fork.git`
    
3. Faça suas alterações e envie um Pull Request para o projeto original.

---

## Conclusão

Dominar o Git é como aprender a andar de bicicleta – no começo, pode parecer difícil, mas depois que pega o jeito, você nunca mais esquece (e não vai cair tanto, esperamos)!  
Com esses comandos básicos e avançados, você estará pronto para versionar seu código, colaborar com outros desenvolvedores e manter seu histórico de alterações em dia – sempre com um toque de humor para descontrair a jornada. Bons commits e sucesso na sua aventura com Git e GitHub!





FONTES:

- http://rogerdudler.github.io/git-guide/index.pt_BR.html?authuser=0

- https://git-scm.com/book/pt-br/v1/Primeiros-passos?authuser=0

- https://blog.triadworks.com.br/gerenciando-a-versao-dos-seus-projetos

- https://learngitbranching.js.org/?locale=pt_BR



