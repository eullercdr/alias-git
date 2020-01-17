Edite seu arquivo .gitconfig que está dentro da pasta do seu usuário, senão tiver
crie-o =P

Após adicione os seguintes comandos:

[alias]
  ci = commit
  co = checkout
  cm = checkout master
  cb = checkout -b
  st = status -sb
  sf = show --name-only
  lg = log --pretty=format:'%Cred%h%Creset %C(bold)%cr%Creset %Cgreen<%an>%Creset %s' --max-count=30
  incoming = !(git fetch --quiet && git log --pretty=format:'%C(yellow)%h %C(white)- %C(red)%an %C(white)- %C(cyan)%d%Creset %s %C(white)- %ar%Creset' ..@{u})
  outgoing = !(git fetch --quiet && git log --pretty=format:'%C(yellow)%h %C(white)- %C(red)%an %C(white)- %C(cyan)%d%Creset %s %C(white)- %ar%Creset' @{u}..)
  unstage = reset HEAD --
  undo = checkout --
  rollback = reset --soft HEAD~1

  #Explicação

  git ci "Mensagem de Commit"
   
  git co nomebranch = git checkout branch

  git cm volta para o branch master

  git cb nomebrance - cria e entra no nome do branch

  git st = mostra o status dos arquivos da worktree de forma otimizada

  git sf [hashcommit] = mostra os arquivos modificados em um commit

  git lg = mostra a arvore de commits de forma otimizada

  git incoming = Retorna todos os commits do remoto que não estão no projeto local

  git outgoing = Retorna todos os commits locais que não estão dentro do remoto

  git unstage [arquivo]= Retira o arquivo do stage do git 

  git undo [arquivo] = desfaz a ultima alteracao do arquivo

  git roolback = desfaz o ultimo commit e mantem o arquivo

  