# Notas e dicas dos cursos de git da DIO

## Configuração Inicial
```bash
# Connfiguração de nome de usuário
git config user.name # exibe o usuário configurado
git config user.name "seu nome" # altera o usuário

# Escopo da configuração (--local, --global, --system), se não informado, é considerado local
git config --local user.name # apenas o repositório atual
git config --global user.name # todos os repositórios do usuario logado
git config --system user.name # todos os repositórios do sistema independente de usuário
git config --show-origin user.name # exibe o caminho do arquivo de onde a configuração (neste caso nome do usuário) esta sendo usada

# Configurar e-mail
git config --global user.email "seu@email.com"

# Configurar a branch padrão
git config --init.defaultBranch main

# Configurar cache de autenticação
git config credential.helper store # armazenamento permanente
git config credential.helper cache # armazenamento temporário

# Exibir as todas as configurações
git config --list

# Para visualizar o conteudo do arquivo de configurações do git
cat .git/config
```

## Inicialização e clone
```bash
# Iniciar um repositório Git em um diretório existente
git init

# Clonar um repositório existente
git clone <url_do_repositorio>

# Clonar um repositório existente em uma pasta com nome diferente
git clone <url_do_repositorio> "nome da pasta"
```
## Operações básicas
```bash
# Adicionar todas as mudanças para o próximo commit
git add .

# Adicionar um arquivo específico para o próximo commit
git add nome_do_arquivo

# Confirmar as mudanças com uma mensagem de commit
git commit -m "Sua mensagem de commit"

# Adicionar as alterações ao stage e fazer commit
git commit -am "Sua mensagem de commit"
```

# Ramificação e merge
```bash
# Criar uma nova branch
git branch nome_da_branch

# Trocar para uma branch existente
git checkout nome_da_branch

# Criar e trocar para uma nova branch
git checkout -b nome_da_branch

# Mesclar alterações de uma branch para outra
git merge nome_da_branch

# Altera o nome do branch atual
git branch -M main

```

# Atualizações remotas
```bash
# Adicionar um repositório remoto
git remote add nome_remoto url_do_repositorio

# Listar repositórios remotos
git remote -v

# Obter alterações do repositório remoto
git pull nome_remoto nome_da_branch

# Enviar alterações para o repositório remoto
git push nome_remoto nome_da_branch

# Enviar alterações para o repositório remote salvando o repositório remoto, 
# das proximas vezes somente git push será necessário
git push -u nome_remote nome_da_branch
```

# Status e Histórico
```bash
# Verificar o status do repositório
git status

# Verificar histórico de commits
git log

# Visualizar mudanças feitas em arquivos
git diff
```

# Desfazer Alterações
```bash
# Desfazer o último commit mantendo alterações do commit em stage
git reset --soft HEAD~1

# Desfazer o último commit mantendo alterações locais
git reset HEAD~1

# Desfazer o último commit com alterações locais
git reset --hard HEAD~1

# Desfazer a alteração do arquivo restaurando como no último commit
git restore [nome-do-arquivo]
```

# Outros comandos úteis
```bash
# Criar um arquivo .gitignore para listar arquivos a serem ignorados
echo "nome_do_arquivo" > .gitignore
npx gitignore [nome-da-linguagem] # criar o gitignore para uma linguagem a partir da biblioteca gitignore
npx gitignore node # cria gitignore para node
npx gitignore types # para visualizar os templates de gitignore

# Visualizar branches locais e remotas
git branch -a

# Criar e aplicar um patch
git diff > nome_do_patch
git apply < nome_do_patch
```
