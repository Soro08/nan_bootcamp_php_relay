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

### Solution

```bash
# 1 si on utilise un email pour la connection

filter_var($email, FILTER_VALIDATE_EMAIL)


# 1 Échappement des caractères spéciaux

<?php

 addslashes($var);
 
?>


```



## La faille XSS

XSS (plus officiellement appelée Cross-Site Scripting) est une faille permettant l'injection de code HTML ou JavaScript dans des variables mal protégées. Il existe en fait deux types de XSS

https://openclassrooms.com/fr/courses/2091901-protegez-vous-efficacement-contre-les-failles-web/2680167-la-faille-xss


## Requête preparé VS query

 Query
```bash

<?php

// On récupère les variables envoyées par le formulaire
$login = $_POST['login'];
$password = $_POST['password'];

// Connexion à la BDD en PDO
try { $bdd = new PDO('mysql:host=localhost;dbname=bdd','root',''); }
catch (Exeption $e) { die('Erreur : ' .$e->getMessage())  or die(print_r($bdd->errorInfo())); }

// Requête SQL
$req = $bdd->query("SELECT * FROM utilisateurs WHERE login='$login' AND password='$password'");

?>

```
Preparé
 
 ```bash
 
 <?php

// On récupère les variables envoyées par le formulaire
$login = $_POST['login'];
$password = $_POST['password'];

// Connexion à la BDD en PDO
try { $bdd = new PDO('mysql:host=localhost;dbname=bdd','root',''); }
catch (Exeption $e) { die('Erreur : ' .$e->getMessage())  or die(print_r($bdd->errorInfo())); }

// Requête SQL sécurisée
$req = $bdd->prepare("SELECT * FROM utilisateurs WHERE login= ? AND password= ?");
$req->execute(array($login, $password));

?>
 
 ```
