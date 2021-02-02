# Heroku

## Comment heberger un projet django sur Heroku?

1 - Creer un compte sur [Heroku](https://www.heroku.com/) 

2 - Creer une application apres s'etre connecter sur son compte Heroku

3 - Telecharger et installer l'application [Heroku CLI](https://devcenter.heroku.com/articles/heroku-cli) pour avoir acces à la commande heroku en ligne de commande

5 -   Créer le fichier Procfile a la racine de votre projet
  
      web: gunicorn nom_projet.wsgi --log-file -
      
6 -   Créer le fichier runtime.txt a la racine de votre projet et ajouter la version de python

      python-3.6.12
      
      
7 - Ajouter requirements.txt contenant les dependances de votre projet

      $ pip freeze > requirements.txt
      
8 - Commandes pour deployer votre projet 

    $ heroku login (for login)
    
    $ cd myapp
    $ git init
    $ git add .
    $ git commit -m "My first commit"
    
    $ git push heroku master
      Initializing repository, done.
       updating 'refs/heads/master'


    


