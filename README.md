# Vamos lá explicar essa receita!
## Vamos usar uma imagem oficial do WordPress.
A imagem que vamos usar é a versão mais recente, neste caso a 6. Coloquei tags do PHP-FPM porque estou mais familiarizado em usar o Nginx.

## Docker-Compose
Nossa arquivo especifica a rede que deverá ser criada, os volumes que serão usados.
Vou usar a porta 92 para acessar o Nginx. Como o WordPress está funcionando com o PHP-FPM, a porta deste é 9000.
Você pode observar que além do Nginx estão listado o Redis e o MariaDB.
Vou explicar melhor cada item.

### Nginx
O Nginx irá funcionar como servidor http. 
Nesta configuração a porta que ele irá usar é a 92.
Os arquivos de configuração estão na pasta nginx. Você pode alterá-la conforme achar necessário para o seu projeto.

### MariaDB
O MariaDB é o banco de dados que o WordPress precisa acessar. As configurações do MariaDB está no arquivo wordpress_db.env. Lembre-se de alterar as senha lá.
Banco de dados é onde são armazenados os dados do seu site. Sem um banco de dados não tem como fazer o WordPress funcionar.

### Redis
O Redis será usado como cache. O cache é uma forma de otimizar seu site.
Funciona mais ou menos assim: Quando alguém acessa seu site, o que a pessoa verá é um cache do site, uma fotografia do site. Assim, você tornam tudo mais rápido, seguro e funcional.

em construção...
