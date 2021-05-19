# Heroku

## Comment heberger un projet django sur Heroku?

1 - Creer un compte sur [Heroku](https://www.heroku.com/) 

2 - Creer une application apres s'etre connecter sur son compte Heroku

3 - Telecharger et installer l'application [Heroku CLI](https://devcenter.heroku.com/articles/heroku-cli) pour avoir acces à la commande heroku en ligne de commande

5 -   Créer le fichier Procfile a la racine de votre projet
  
      web: gunicorn nom_projet.wsgi --log-file -
      
 6 - install Gunicorn
  
      $ pip install gunicorn
      
7 -   Créer le fichier runtime.txt a la racine de votre projet et ajouter la version de python

      python-3.6.12
      
      
8 - Ajouter requirements.txt contenant les dependances de votre projet

      $ pip freeze > requirements.txt
      
9 - Commandes pour deployer votre projet 

    $ heroku login (for login)
    
    $ cd myapp
    $ git init
    $ git add .
    $ git commit -m "My first commit"
    
    $ git push heroku master
      Initializing repository, done.
       updating 'refs/heads/master'

 10 - Configure Postgres on your project
 
   a- Install Dj database
   
       $ pip install dj-database-url
       
   b- Install Psycopg2
  
    $ pip install psycopg2
  
  c- Configurate our url
  
    postgres://My_USER:My_PASSWORD@My_HOST:PORT/bd_NAME
    
   d- Settings.py [Detail](https://pypi.org/project/dj-database-url/)
   
    import dj_database_url
    DATABASES['default'] = dj_database_url.config()
              
      
          
    


