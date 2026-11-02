# 📒 Mon carnet de bord

**Nom : PAPALIA 

**Prénom : GUILLAUME

**Adresse de mon site :** https://guillaume971.pythonanywhere.com

> Modifiez ce fichier directement sur GitHub (icône crayon ✏️) pour répondre aux questions de chaque exercice.
> Écrivez avec vos propres mots : une réponse courte et juste vaut mieux qu'un long copier-coller ! 🙂

---

## 🟢 Exercice 1 — Mon premier déploiement

1. Où se trouve physiquement le code qui fabrique votre page : sur votre ordinateur, sur GitHub ou sur PythonAnywhere ?

   > _Ma réponse : Sur PythonAnywhere, c'est le serveur qui exécute le code et qui fabrique la page. GitHub garde seulement une copie du code avec l'historique.

2. Pourquoi votre voisin(e) peut-il voir votre site, alors que vous n'avez rien installé sur son ordinateur ?

   > _Ma réponse : Parce que le site tourne sur le serveur PythonAnywhere qui est connecté à Internet tout le temps.

---

## 🟢 Exercice 2 — Les URL et les routes

1. Dans l'URL `https://www.google.com/maps`, quel est le nom de domaine ? Quel est le chemin ?

   > _Ma réponse : Le nom de domaine c'est "www.google.com" Et le chemin c'est "/maps" 

2. Que veut dire le message *Not Found* ? Qui l'a envoyé : votre navigateur ou le serveur ?

   > _Ma réponse : Ça veut dire que la page demandée n'existe pas(erreur 404), C'est le serveur qui l'envoie parce qu'il n'a pas de route pour cette adresse.

3. Que se passe-t-il si deux fonctions portent le même nom dans `flask_app.py` ? (Indice : essayez, puis lisez l'Error log.)

   > _Ma réponse : Le site plante et affiche une page d'erreur. Dans l'Error log il y a 'AssertionError'

---

## 🔵 Exercice 3 — Le langage HTML

1. Quelle est la différence entre ce que le serveur **envoie** et ce que le navigateur **affiche** ?

   > _Ma réponse : La différence ce sont les balises HTML, C'est elle qui indique comment interpréter Le texte pour savoir Comment elles doivent s'afficher

2. À quoi servent les balises `<h1>`, `<p>`, `<ul>` et `<li>` ?

   > _Ma réponse : "<h1>" c'est pour le titre, '<p>' pour un paragraphe, '<ul>' pour une liste à puces et '<li>' pour chaque élément de la liste.


3. Pourquoi l'image s'affiche-t-elle alors qu'elle n'est pas sur votre serveur ?

   > _Ma réponse : Parce que le HTML donne l'adresse de l'image. Le navigateur suit cette adresse et va chercher l'image directement sur l'autre serveur.

---

## 🔵 Exercice 4 — Les templates

1. Pourquoi est-ce une bonne idée de séparer le code Python et le HTML ? (Pensez à une équipe avec un développeur et un graphiste.)

   > _Ma réponse :_ Le code est mieux rangé et plus lisible, on sait où est chaque chose. par exemple dans une équipe, le graphiste peut modifier le HTML et le développeur le Python


2. Les `{{ prenom }}` sont-ils remplacés par le serveur ou par le navigateur ? Comment l'avez-vous vérifié ?

   > _Ma réponse :_ Par le serveur. J'ai fait Ctrl + U : dans le code source, il y a « Léa Martin » et plus les `{{ prenom }}`. Le serveur les a remplacés avant d'envoyer la page.

---

## 🔵 Exercice 5 — Le CSS et les liens

1. Quelle est la différence de rôle entre le HTML et le CSS ?

   > _Ma réponse : Le HTML donne la structure de la page (titre, paragraphe, liste…). Le CSS s'occupe de l'apparence (couleurs, police, marges…).


2. Pour afficher votre page `/presentation`, combien de fichiers le navigateur doit-il télécharger ? (Vous pourrez le vérifier à l'exercice suivant !)

   > _Ma réponse : 2 fichiers : la page HTML, puis le fichier `style.css`. Le navigateur voit la balise `<link>` dans le HTML et va chercher le CSS en plus.

3. Pourquoi faut-il parfois faire **Ctrl + F5** pour voir les changements de CSS ?

   > _Ma réponse : Parce que le navigateur garde une copie du CSS en mémoire (le cache) pour aller plus vite. Il ne le retélécharge pas, donc il affiche l'ancien. Ctrl + F5 l'oblige à tout retélécharger.

---

## 🟣 Exercice 6 — Espionner le navigateur

1. Que signifie HTTP ? Qui envoie la **requête** et qui envoie la **réponse** ?

   > _Ma réponse :_ HTTP veut dire HyperText Transfer Protocol. C'est la façon dont le navigateur et le serveur se parlent. Le navigateur envoie la requête et le serveur envoie la réponse.

2. Combien de requêtes votre page `/presentation` a-t-elle déclenchées ? Lesquelles ?

   > _Ma réponse :_ 'presentation' (la page HTML), 'style.css' (le style) et 'favicon.ico' (l'icône de l'onglet).


3. Que signifie le code `200` ? Et le code `404` de la favicon ?

   > _Ma réponse :_ 200 veut dire que tout s'est bien passé et que le serveur a envoyé le fichier. 404 veut dire que le fichier n'existe pas : mon site n'a pas d'icône.

4. Pourquoi les modifications faites dans l'onglet Éléments ne sont-elles pas visibles par les autres visiteurs ?

   > _Ma réponse :_ Parce que je modifie seulement la copie de la page dans mon navigateur. Le code sur le serveur ne change pas, donc les autres reçoivent toujours la page normale.

---

## 🟣 Exercice 7 — Envoyer des informations dans l'URL

1. Dans l'URL `https://www.youtube.com/results?search_query=chat`, quel est le nom du paramètre ? Quelle est sa valeur ?

   > _Ma réponse :_ Le paramètre c'est `search_query` et sa valeur c'est `chat`.


2. Pourquoi le serveur plante-t-il avec `a=bonjour` ? Que faudrait-il faire pour l'éviter ?

   > _Ma réponse :_ Parce que `int()` ne peut pas transformer « bonjour » en nombre, donc Python fait une erreur (ValueError). Il faudrait vérifier que la valeur est bien un nombre avant de la convertir, et sinon afficher un message d'erreur.


3. Pourquoi est-il dangereux d'afficher **tel quel** ce que l'utilisateur envoie ?

   > _Ma réponse :_ Parce que l'utilisateur peut mettre du HTML ou un script dans l'URL, et il s'exécute dans la page. Un pirate pourrait envoyer ce lien à quelqu'un et lancer un script malveillant chez lui, par exemple pour voler ses infos. C'est une faille XSS.

---

## 🟣 Exercice 8 — Les formulaires

1. Quelle est la différence visible entre GET et POST ?

   > _Ma réponse :_ Avec GET les données sont dans l'URL (`/salut?prenom=Guillaume&ville=Noisiel`) et avec POST, l'URL reste juste `/salut` : les données sont envoyées dans le corps de la requête, on ne les voit pas dans la barre d'adresse.


2. Pour un formulaire de **recherche**, quelle méthode choisiriez-vous ? Et pour un formulaire de **connexion avec mot de passe** ? Pourquoi ?

   > _Ma réponse :_ Pour une recherche GET on peut copier le lien, le partager ou le mettre en favori. Pour une connexion POST : le mot de passe n'apparaît pas dans l'URL, ni dans l'historique du navigateur.

3. Les données envoyées en POST sont-elles vraiment « secrètes » ? (Pensez à ce que vous avez vu dans l'onglet Réseau.)

   > _Ma réponse :_ Non On les voit dans l'onglet Réseau (Charge utile). POST les cache juste de l'URL. Ce qui protège vraiment les données pendant le trajet, c'est le HTTPS.

---

## 🔴 Exercice 9 — Les codes de statut

1. Quelle est la différence entre une erreur `4xx` et une erreur `5xx` ? Qui est « fautif » dans chaque cas ?

   > _Ma réponse :_ Les erreurs 4xx c'est quand le problème vient du visiteur, par exemple il demande une page qui n'existe pas (404) ou il n'a pas le droit d'y accéder (403). Les erreurs 5xx c'est quand le problème vient du serveur, par exemple un bug dans le code Python (500). Donc pour 4xx c'est le visiteur qui est fautif et pour 5xx c'est le serveur.

2. Comment fonctionne une redirection ? Qui fait la deuxième requête : le serveur ou le navigateur ?

   > _Ma réponse :_ Le serveur répond avec un code 302 et il donne la nouvelle adresse. Ensuite c'est le navigateur qui fait tout seul une deuxième requête vers cette adresse.

3. Donnez un exemple de situation où un vrai site utilise une redirection.

   > _Ma réponse :_ Quand on se connecte sur un site, après avoir mis son mot de passe on est renvoyé vers la page d'accueil ou vers son compte. Ou quand on tape une adresse en http le site nous renvoie direct vers la version en https.

---

## 🔴 Exercice 10 — Ce que le serveur sait de vous

1. Citez trois informations que le serveur connaît sur vous, sans que vous ayez rien rempli.

   > _Ma réponse :_ 

2. À quoi peut servir l'en-tête `Accept-Language` pour un site comme Wikipédia ?

   > _Ma réponse :_ 

3. Dans l'Access log, retrouvez une requête qui a reçu un code `404`. Quelle page était demandée ?

   > _Ma réponse :_ 

4. Après cet exercice, que pensez-vous de la notion de « navigation anonyme » ?

   > _Ma réponse :_ 

---

## 🔴 Exercice 11 — Le Web des machines : API et JSON

1. Quelle est la différence entre une page HTML et une réponse JSON ? À qui chacune est-elle destinée ?

   > _Ma réponse :_ 

2. Dans la page `/horloge`, quel code s'exécute sur le **serveur** et quel code s'exécute dans le **navigateur** ?

   > _Ma réponse :_ 

3. Citez une application de votre téléphone qui, selon vous, utilise une API. Quelles données échange-t-elle ?

   > _Ma réponse :_ 

---

## 🏁 Pour conclure

En quelques phrases, expliquez à un ami ce qui se passe entre le moment où il tape une adresse dans son navigateur et celui où la page s'affiche :

> _Ma réponse :_ 
