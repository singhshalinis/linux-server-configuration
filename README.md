Linux Server Configuration
==================================


What is it? (Functionality)
---------------------------
A baseline ubuntu web server configured to host a sample app. The server is secured from various attack vectors. It uses Google OAuth to login and create items.


Last Update Date
-----------------
Oct, 2018


System Specific Notes (Summary of the software installed)
-----------------------------------------------------------
* Linux Ubuntu 16.04.5 LTS
* Apache2 Web server
* Developed in Python 2.7 using Flask, Jinja, SQLAlchemy, psycopg2, requests etc
* mod-wsgi
* Postgres 9.5
* git


Summary of configurations made
----------------------------------
1. All packages updated and upgraded.
2. Updated firewall and enabled to only allow ports 80, 2200, 123
3. Created user grader, made it a sudoer, generated keys and set login method only using keys.
4. Installed Apache2
5. In PostgresQL, created a database user catalog and created a database catalogdb. Granted all to catalog user.
6. Updated timezone to UTC
7. Cloned git repository from https://github.com/singhshalinis/itemCatalog and made changes to make it work on the server.
8. Added all required applications for the catalog app to run.
9. Created wsgi file to so that the Item Catalog flask app can be served from Apache2.
10. Updated the redirects for Google OAuth.

Testing
----------
* The web app is not tested against all types of security threats.


How to get started
-------------------
To access the app, go to http://ss.yellowmango.co/
To know what all can be done on Item Catalog App, see this readme - https://github.com/singhshalinis/itemCatalog/blob/master/readme.md


References, Credits & Acknowledgements
--------------------------------------
  * Udacity's lectures for basic Linux Server Configuration & Item Catalog.
  * Creating a new user [https://medium.com/coding-blocks/creating-user-database-and-adding-access-on-postgresql-8bfcd2f4a91e]
  * Disable root login [https://www.a2hosting.com/kb/getting-started-guide/accessing-your-account/disabling-ssh-logins-for-root]
  * Postgres: restrict remote login [https://dba.stackexchange.com/questions/156371/for-postgresql-database-restrict-remote-connections-to-password]
  * Install git [https://help.ubuntu.com/lts/serverguide/git.html.en]
  * https://wiki.postgresql.org/wiki/PostgreSQL_For_Development_With_Vagrant
 * https://github.com/jackdb/pg-app-dev-vm/blob/master/Vagrant-setup/bootstrap.sh
 * https://askubuntu.com/questions/256013/apache-error-could-not-reliably-determine-the-servers-fully-qualified-domain-n
 * https://www.vagrantup.com/docs/provisioning/basic_usage.html
 * https://www.topikettunen.com/2018/02/01/h3-linux-palvelimet-ict4tn021-8.html
 * https://askubuntu.com/questions/413585/postgres-password-authentication-fails
 * https://stackoverflow.com/questions/34838443/typeerror-sequence-of-byte-string-values-expected-value-of-type-str-found
 * https://www.compose.com/articles/using-postgresql-through-sqlalchemy/
 * https://docs.sqlalchemy.org/en/latest/orm/tutorial.html#connecting
 * https://blog.theodo.fr/2017/03/developping-a-flask-web-app-with-a-postresql-database-making-all-the-possible-errors/
 * https://github.com/jackdb/pg-app-dev-vm/blob/master/Vagrant-setup/bootstrap.sh
 * https://wiki.postgresql.org/wiki/PostgreSQL_For_Development_With_Vagrant

Contact Information
--------------------
For any comments, queries, issues, and bugs, please contact singhshalinis@gmail.com.
