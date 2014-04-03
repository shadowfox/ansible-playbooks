An ansible playbook for my personal servers.

## Running the playbook

## Roles

Name          | Description
------------- | -------------
common        | Updates system packages and installs some useful ones. Changes the root password. Sets up a new personal user and locks down SSH, requiring private key authentication by that user.
mail          | Sets up a locally listening [postfix](www.postfix.org) instance which uses a remote mail server for relay.
monitoring    | Provides log analysis via [logwatch](www.logwatch.org), and system/service monitoring via [monit](mmonit.com/monit/). Roles are responsible for providing monit configurations for any services they install.
webserver     | Installs nginx with a decent default configuration
php           | Sets up a PHP5 instance running via FPM. 
database      | Installs postgresql with an optional new user that can be accessed via password authentication. The default postgres user remains accessible via peer authentication.

## Todo
 * Feed reader role
 * Monit configs for nginx/postgres/postfix etc.
 * Role for nginx sites

## Troubleshooting
Todo