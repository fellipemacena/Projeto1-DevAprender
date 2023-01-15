# Projeto1-DevAprender
Tutorial versionamento Git/GitHub - Dev Aprender
https://www.youtube.com/watch?v=kB5e-gTAl_s

Passo a Passo Git / GitHub:

- Na pasta do projeto -> botão direito mouse -> Git Bash Here
- comando: git init
- criar o arquivo com linha de texto dentro
- para verificar o status do repositório
- comando: git status
- caso haja "No commits uet", significa que não há versões do código. Commits significa versões.
- Caso haja "Untracked files:"  ele irá indicar quais arquivos não estão no controle de versão
- Para adicionar ao controle de versão basta digitar
- comando:  git add "nome do arquivo" (incluindo sua extensão - conforme o Untracked files)
- Para adicionar mais de um arquivo deve digitar
- comando: git add .

Github é a núvem de versionamento de arquivos

Criando versões do código:
-comando git commit -m "commit inicial"
O m significa mensagem e é um registro do motivo da nova versão do documento. (Boa prática)
após o código precisa aparecer uma mensagem semelhante a essa:

[master (root-commit) 8174c8f] commit inicial
 1 file changed, 1 insertion(+)
 create mode 100644 meu codigo.txt

- Indicando a mensagem escrita, em qual commit está, quantos arquivos e o nome dos arquivos
- Caso não seja executado provavelmente irá pedir para digitar os seguintes comando:
config --global user.email  "e-mail"
 config --global user.name "Your Name"

Para enviar pro GitHub:
- Criar conta no GitHub
- Criar um novo repositório 
- Copiar a URL da página da raíz do repositório criado
- Ir para o GitBash e digitar 
- comando: git remote add origin (defigit nição para onde o código será enviado)
- depois digitar
- comando: git push --set-upstream origin master 

Para atualizações futuras:
-comando: git status
-comando: git add .
-comando: git push

Para verificar histórico de atualizações:
-comando: git reflog

Para voltar a versão anterior:
-Após digitar reflog, o git gerá uma histórico de versão, sendo a versão do topo a mais atual, com isso, a ordem fica do mais atual para o mais antigo (cima para baixo).
- Em seguida, para acessar uma versão anterior que queira trabalhar digitar
- comando: git reset --hard "código do início da linha da versão no reflog que queira acessar"
-Após esse comando poderá acessar o arquivo com a versão em questão.
- O mesmo funciona para voltar para a função mais atual.
- "Consultar a equipe e chefe para verificar o procedimento que a equipe segue  de verificar o acesso a versões anteriores"

Criação de outras Branchs
-comando: git branch (para identificar quantas e quais branchs tem no repositório)
-comando: git branch "um nome pra nova branch" (cria uma nova branch)
-comando: git cheackout "um nome pra nova branch" (pula para a nova branch)

Obs: Após realizar a criação da nova branch e realizar a revisão do arquivo, onde o mesmo agora estará atrelado a nova branch. Ao realizar o git push, provavelmente irá aparecer um comando que o git irá pedir. Faça.
-comando:  git push --set-upstream origin staging

Merge:
-comando: git checkout master (ir para a branch principal ou para a branch que deseja levar o código concluído/finalizado)
-comando: git merge "branch de execução e validação" (nesse passo a passo foi usada a branch staging)

Obs: Para verificar que está efetuando o merge nas versões mais atuais dos arquivos na branch principal, digitar
- git pull da branch principal (baixar arquivos GitHub)
- Gerar uma nova branch a partir da branch principal
- Efetuar as modificações e finalizar o trabalho na branch temporária
- Git checkout na branch principal
- Git Pull
- Mergear (unir) o código da branch temporária com a branch principal
- Git push da branch principal

Git ignore:
- comando: touch .gitignore
- Criado o arquivo txt e dentro dele poderão ser incluídos os arquivos que você deseja que não entrem no versionamento. 
