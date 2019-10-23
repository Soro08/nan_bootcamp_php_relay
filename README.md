# nan_bootcamp_php_relay
Bootcamp NaN 2019

Hello dans ce tutorial je vais vous montrer quelque notion php

## Injection SQL

La faille SQLi, abréviation de SQL Injection, soit injection SQL en français, est un groupe de méthodes d'exploitation de faille de sécurité d'une application interagissant avec une base de données. Elle permet d'injecter dans la requête SQL en cours un morceau de requête non prévu par le système et pouvant en compromettre la sécurité.

### Exemple 
```bash
# Requête SQL pour verifier si un utilisateur est connecté

SELECT uid FROM Users WHERE name = '(nom)' AND password = '(mot de passe hashé)';

# injection SQL

SELECT uid FROM Users WHERE name = 'Dupont' AND password = '' or 1 --';


# bah je comprend rien

Oui bro

le mot de pass a été remplacé par " '' or 1 --' " ce qui autorise l'utilisateur à ce connecter coute que coute.

Vous aurez plus de détail dans la pratique

```

### 



## Faill relation au requete
## Requête preparé VS query
## filtrer les variables
