# Git tutorial

[Download git:]
(https://git-scm.com/download)

Configurações de nome e email:
```
git config --global user.name "Seu nome"
git config --global user.email "Seu email"
```

Verificar itens acima:
```
git config --list
```

No menu iniciar achar Opções do explorador de arquivos e fazer as seguintes mudanças:
- Desmarcar "Ocultar as extensões dos tipos de arquivos conhecidos".
- Marcar "Mostrar arquivos, pastas e unidades ocultas".


Configurar chave SSH para o Github, novo sistema de segurança sem utilização de senha.

Cadastrar previamente quais computadores podem acessar seu Git.

Para isso vamos:
- Gerar uma chave SSH no nosso computador:
  - Abra o Git Bash.
  - ssh-keygen -t ed25519 -C "Seu email", ou ssh-keygen -t rsa -b 4096 -C "Seu email"
  
 Ele vai perguntar se quero senha a minha escolha e sugerir local onde a chave vai ficar.
    Meu local foi Usuario/MeuUsuario/.ssh
  
 - Cadastrar essa chave no nosso Git:
    No meu git acessar Settings/SSH and GPG keys/New SSH key
    
Salvar primeira versão de um projeto:
Como exemplo posso deixar arquivos salvos em determinada pasta e dai começar:
```
1. git init 
2. git add .
3. git status 
4. git commit -m "Mensagem explicativa sobre" 
5. git branch -M main 
6. git remote add origin git@github.com:"meuUsuario"/"meuRepositorio".git 
7. git push -u origin main
```

Referente aos comandos acima:

Após comando acima já vai ser criada uma pasta .git   

Vai mandar todos os arquivos para uma área chamada Stage

(Opcional) Mostra as modificações a serem salvas

Vai salvar a versão efetivamente

Por padrão agora o git salva como main, antigamente era Master. Esse comando garante caso tenha uma versão salva no computador como Master.

Deixo salvo um repositório lá no git já, tem que ter o mesmo nome do repo as pastas do nosso projeto.
