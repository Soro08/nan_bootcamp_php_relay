
# ![logo NaN](http://nan.ci/static/images/favicons.ico/apple-icon-57x57.png) Projet NaN Blog



  Pour plus de visibilité sur google, NaN décide de mettre en place un blog qui traite des sujets d'ordre informatique.


  un utilisateur recherchant une aide sur google peut être redirigé sur notre blog.


## comment le blog fonctionne

3 - type de compte

  - Compte **admin** ( NaN )

  - Compte **Membre** 
  
    ( ce dernier s'inscrit en tant que membre et l'admin valide sa demande d'hadesion )
    
    un compte user peut écrire un article. Seul l'admin peut autoriser la publication ( visibilité sur le site )
  
    l'user a une partie admin pour lui où il peut voir la liste de ces posts, nombre de vue par post, nombre de like, nombre de dislike  (graphique d'illustration).


  - Compte **Visiteur**
    ( il peut seulement commenter, liker, partager, lire les posts.) ce dernier peut faire une demande d'adhésion afin d'être     reconu comme **membre**


## Template

https://colorlib.com/wp/template/ruft/


## Réalisation

![vue js django graphql](https://miro.medium.com/max/1200/1*KDLOb-elHdFuUMUrvU7kOw.png)



Pour la réalisation vous allez utiliser: Vue js, Django et graphQl



## Fonctionnalité

  - **Inscription**
    Lors de l'inscription l'utilisateur a le choix:
      - Membre
      - Visiteur
      
      Possibilité de s'inscrit via **gmail**, **facebook**, **github**
      
      Un **mail** où Un **SMS** de confirmation est envoyé.

      **SMS** le message contient un code que l'utilisateur doit entrer pour valider l'inscription
      
      **MAIL** Un message suivit d'un lien cripté sur lequel l'utilisateur doit cliquer pour valider son inscription

  - **Panneau d'administration:**
    - Admin Django (reservé à l'admin principale )
    - Créer une partie admin pour les membres (https://colorlib.com/wp/free-admin-templates/) vous pouvez choisir parmis les template du site colorlib
    - Une partie admin pour les visiteurs inscrits ( ajouter un bouton les incite à devenir membre)

  - **Notification**

    - Un mail ou un SMS est envoyé à tous les utilisateurs lors de l'activation d'un nouveau post.
    - Un mail est envoyé à l'admin lors de l'ajout d'un nouveau post par un membre.
    - Un mail est envoyé à l'admin lors d'une demande d'adhésion



