# Useful Bash Aliases
Some useful bash aliases ( personal use )

### Common Bash Commands

```bash
alias cls='clear'
alias flush='source ~/.bashrc'
alias snano='sudo nano'
# for debian based system
alias update='sudo apt-get update'
alias upgrade='sudo apt-get upgrade'
alias install='sudo apt-get install'
alias u-install='apt-get install'
```

### For Apache2
```bash
alias a2sites='cd /etc/apache2/sites-available'
alias a2sites-en='cd /etc/apache2/sites-enabled'
alias a2restart='sudo systemctl restart apache2' # add apache2.service instead of apache2 if it's not working
alias a2stop='sudo systemctl stop apache2'
alias a2start='sudo systemctl start apache2'
alias a2sites-edit='sudo "$1" /etc/apache2/sites-available/"$2"' # use 'set filename' first if it doesn't work directly
# use it like - 'a2sites-edit nano( or vim) default.conf(.conf file)
```

### For Web Directory
```bash
alias cdm='cd /var/www/html'
alias cdmp='cd /var/www/html/"$1"' # project dir name
```

### For Laravel
```bash
alias create-laravel='sudo composer create-project laravel/laravel'
alias create-laravel-dist='sudo composer create-project laravel/laravel --prefer-dist'

# for artisan commands
alias 'phart'='sudo php artisan'
alias 'pharts'='sudo php artisan serve'
alias 'phartsp'='sudo php artisan serve --port "$1"'
alias 'phtinker'='sudo php artisan tinker' # for using tinker

# migrations
alias phartm='sudo php artisan migrate'
alias phartmf='sudo php artisan migrate:fresh'
alias phartmr='sudo php artisan migrate:rollback'
alias phartmrs='sudo php artisan migrate:rollback --step="$1"' # rollback step
alias 'artmmi'='sudo php artisan make:migration'
alias 'artmmi-create'='sudo php artisan make:migration --create="$"'
alias 'artmmi-table'='sudo php artisan make:migration --create="$"'

# models
alias artmmo='sudo php artisan make:model'
alias artmmo-mi='sudo php artisan make:model "$1" -m'

# controllers
alias artmco='sudo php artisan make:controller'
alias artmco-r='sudo php artisan make:controller "$1" -r'
```