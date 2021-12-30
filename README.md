# PhxAuth

ayex@HP:~/projects$ mix phx.new phx_auth

$ mix deps.get
$ mix deps.compile

context: Accounts
schema : User
Table  : users 

$ mix phx.gen.auth Accounts User users
$ mix deps.get

