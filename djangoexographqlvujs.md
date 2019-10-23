# Projet NaN Blog



  Pour plus de visibilité sur google, NaN décide de mettre en place un blog qui traitre des sujet d'odre informatique.


  un utilisateur récherchant une aide sur google peut être redirigé sur notre blog.


## comment le blog fonctionne

3 - type de compte

  - Compte **admin** ( NaN )

  - Compte **Membre** 
  
    ( ce dernier s'inscrit en tant que membre et l'admin valide sa demande d'hadesion )
    
    un compt user peut écrit un article. Seul l'admin peut autoriser la publication ( visibilité sur le site )
  
    l'user a une partie admin pour lui où il peut voir la liste de ces posts, nombre de vue par post, nombre de like, nombre de dislike  (graphique d'illustration).


  - Compte **Visiteur**
    ( il peut seulement commenter, liker, partager, lire les posts.) ce dernier peut faire une demande d'hadesion afin d'être     reconus comme **membre**


## Template

https://colorlib.com/wp/template/ruft/


## Réalisation

![vue js django graphql](https://miro.medium.com/max/1200/1*KDLOb-elHdFuUMUrvU7kOw.png)



Pour la réalisation vous allez utiliser: Vue js, Django et graphQl



## Fonctionnalité

  - **Inscription**
    Lors de l'inscription j'ai le choix:
      - Membre
      - Visiteur
      
      Un **mail** où Un **SMS** de confirmation est envoyer.

      **SMS** le message contient un code que l'utilisateur doit entrer pour valider l'inscription
      
      **MAIL** Un message suivit d'un lien cripté que sur laquel l'utilisateur doit cliquer pour valider sont inscription

  - **Panneau d'administration:**
    - Admin Django (reservé à l'admin principale )
    - Créer une partie admin pour les membres (https://colorlib.com/wp/free-admin-templates/) vous pouvez choisir parmin les template du site colorlib
    - Une partie admin pour les visiteur inscrit ( ajouter un boutton les incitent à dévenir membre)

  - **Notification**

    - Un mail ou un SMS est envoyé à tous les utilisateurs lors de l'activation d'un nouveau post.
    - Un mail est envoyé à l'admin lors de l'ajout d'un nouveau post par un membre.
    - Un mail à l'admin lors d'une demande d'adhesion


