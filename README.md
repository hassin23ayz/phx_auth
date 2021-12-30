# PhxAuth

ayex@HP:~/projects$ mix phx.new phx_auth

$ mix deps.get
$ mix deps.compile

context: Accounts
schema : User
Table  : users 

$ mix phx.gen.auth Accounts User users
$ mix deps.get

$ sudo -u postgres psql
postgres=# create user phx_auth with encrypted password 'auth_phx';
postgres=# ALTER ROLE phx_auth CREATEDB;
postgres=# ALTER ROLE phx_auth LOGIN;
postgres=# ALTER ROLE phx_auth SUPERUSER;

> config/dev.exs            : change password of DB

$ mix ecto.create
$ mix ecto.migrate

$ iex -S mix phx.server 

> register an user 

after login -> One browser = One user : 2 users cannot be present in the same browser 

the password inputted by user is not persisted in DB. The Hash(by-bycrypt) of the password gets persisted 



