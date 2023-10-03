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

1. Após comando acima já vai ser criada uma pasta .git   
2. Vai mandar todos os arquivos para uma área chamada Stage
3.(Opcional) Mostra as modificações a serem salvas
4. Vai salvar a versão efetivamente
5. Por padrão agora o git salva como main, antigamente era Master. Esse comando garante caso tenha uma versão salva no computador como Master.
6. Deixo salvo um repositório lá no git já, tem que ter o mesmo nome do repo as pastas do nosso projeto.
  - Preciso criar OBRIGATORIAMENTE o repositório lá no git que eu pego direto lá o item 6 acima. E também deixar algum arquivo dentro senão fica dando erro.
7. Sobe no git.

```
Depois de criado para subir qualquer versão nova uso os seguintes comandos:
1. git add .
2. git commit -m "Mensagem explicativa sobre" 
3. git branch -M main 
4. git push -u origin main
```
Caso eu tenha um repositório existente uso os comandos

```
git remoto adicionar origem git@github.com:AguinaldoGabrielJr/docker.git
git branch -M main 
git push -u origin main
```
