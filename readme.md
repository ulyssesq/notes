# Anotações
## Git

**git remote add origin [endereço]**
Adiciona ao repositório local a referencia do repositório remoto.
Exemplo: *git push --set-upstream [repositório remoto] master*

**git push --set-upstream [repositório remoto/branch remoto] [branch local]**
Vincula um branch ao repositório remoto. Assim não precisa especificar ao usar pull, push e etc.
Exemplo: *git push --set-upstream origin/master master*

**git restore**
Desfaz as alterações no arquivo que ainda não foi adicionado
Exemplo: *git restore .*

**git reset --soft**
Desfaz o git add. (Retira do stage)
Exemplo: *git reset --soft*

**git reset --hard**
Desfaz commit
Exemplo: *git reset --hard*



## ElasticSearch

**POST indice/_doc/id**
Adiciona documento com id especifico, se o índice não existir já cria dinamicamente incluindo o mapping.
Exemplo: 

POST person/_doc/1234
{
	"name": "Ulysses",
	"interests": {"nodejs", "react", "git"}
}

**GET indice/_mapping**
Busca informações do mapping
Exemplo: 
GET person/_mapping





