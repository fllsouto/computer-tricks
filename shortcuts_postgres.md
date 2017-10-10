# Postgres Shortcuts

## Conectar ao banco de dados

```
# Troca para o usuario root
sudo su

# Troca para o usuario postgres
su - postres

# Loga no banco de dados com o usuário <usuario>
psql -U <usuario>

# Loga no banco de dados com o usuário <usuario> no banco <db>
psql -U <usuario> -d <db>

# Login por extenso
psql --username=postgres --dbname=dbname
```

## Comandos uteis para o Postgres

```
# Mostra os usuários
\dg

# Conecta a um db específico
\c <db>

# Lista todas os bancos
\l

# Lista todas as colunas de um db
\dt

# Mostra ajuda
\?
```


## Restaurar DB

```
# Mover o dump para a pasta \var\lib\pgsql ou logar com o usuário e rodar pwd e ver qual a pasta
psql --username=postgres
CREATE DATABSE db_name
\q
psql --username=postgres --set ON_ERROR_STOP=on db_name < db_name_dump_999999

```
