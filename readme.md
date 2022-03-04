# Anotações
## Git

Adiciona ao repositório local a referencia do repositório remoto
git remote add origin [endereço]
Exemplo: git push --set-upstream [repositório remoto] master

Vincula um branch ao repositório remoto. Assim não precisa especificar ao usar pull, push e etc.
git push --set-upstream [repositório remoto/branch remoto] [branch local]
Exemplo: git push --set-upstream origin/master master