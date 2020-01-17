## Praticidade e Agilidade ao utilizar alis no GIT

Este artigo irá demonstrar como você pode otimizar seus comandos GIT, sem precisar ficar decorando e digitando codigos enormes. Caso você tenha alguma sugestão de algum alias que não esteja neste arquivo, nos envie um PR.

## Instruções para configuração de alis no GIT
Edite seu arquivo .gitconfig que está dentro da pasta do seu usuário, senão tiver crie-o.

**Após adicione os seguintes comandos ao final do arquivo**

    [alias]
      ci = commit -m
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

## Como utilizar

Agora ao invés de utilizar os comandos padrões você utilizará os alias ou seja comandos abreviados, abra seu gitbash ou terminal de sua escolha e use os comandos abaixo:

  

     // commita o arquivo com a mensagem
	 git ci "mensagem"
	 
	 // checkout em um branch
     git co nomebranch
    
     // volta para o branch master (git checkout master)
     git cm
    
    //cria e entra no nome do branch
    git cb nomebranch
    
	//mostra o status dos arquivos da worktree de forma otimizada
    git st
    
	//mostra os arquivos modificados em um commit
    git sf [hashcommit] 
    
	//mostra a arvore de commits de forma otimizada
    git lg
    
	//Retorna todos os commits do remoto que não estão no projeto local
    git incoming 
    
	// Retorna todos os commits locais que não estão dentro do remoto
    git outgoing
    
	//Retira o arquivo do stage do git
    git unstage [arquivo]
    
	// desfaz a ultima alteracao do arquivo
    git undo [arquivo] 
    
	//desfaz o ultimo commit e mantem o arquivo
    git roolback
	

## Créditos
**RocketSeat - Code Drops #07**
https://www.youtube.com/watch?v=VpeU3VpszAc&feature=emb_rel_pause
