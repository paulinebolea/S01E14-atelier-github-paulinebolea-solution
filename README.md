# S01E14 Atelier Github

Aujourd'hui on va faire un nouvel atelier sur Github, afin de reprendre les notions vues jusqu'ici, mais aussi pour aller un peu plus loin.

:warning: **RAPPEL** : le but des ateliers n'est pas la complétion à 100% ! Allez le plus loin possible par vos propres moyens, mais n'hésitez surtout pas à faire appel à votre formateur ou tuteur si vous êtes bloqués. Si être bloqué dans son coin est toujours une situation peu appréciable, demander de l'aide à ses pairs ou ses seniors au moment opportun est une qualité, voir un prérequis, quand on est dév Junior :wink:

Comme nous l'avons déjà vu rapidement en cours, les informations d'un repo Git sont stockées sur notre machine dans un dossier `.git/` à la racine du dossier du projet.
Lorsque l'on clone un repository existant depuis Github, ce dossier est automatiquement généré.

Mais comment faire si on a un projet existant sur notre machine et qu'on souhaite l'envoyer sur Github ?<br/>
Ou encore, comment s'y prendre si j'ai cloné un repo depuis un Github mais que je souhaite ensuite l'envoyer sur un autre compte ou une autre organisation Github ?

C'est ce que nous allons voir aujourd'hui :smile:

Mais on a également travaillé notre algorithmie ! Ça serait dommage de ne pas mettre tout ça en pratique.

### Objectifs 🏁 : 
* continuer à s'entrainer sur le Terminal, Git, Github et VSCode
* pratiquer la logique algorithmique à travers la rédaction d'une suite d'instructions
* rédiger un fichier clair, lisible, et éventuellement ponctué de commentaires pour le rendre le plus agréable à lire par votre formateur/tuteur
* utiliser la documentation et les ressources à votre disposition pour réaliser les différentes étapes (Kourou pour les fiches récaps)


Aujourd'hui, le fil conducteur de cet atelier sera un fichier Markdown `instructions.md` que vous allez créer, et dans lequel vous allez consigner toutes les étapes et commandes utilisées pour réaliser l'atelier.

En somme, le fichier que vous allez rédiger sera lui-même la solution complète de cet atelier :exploding_head: Plus d'infos dans les étapes suivantes.





## Étape 1 - Créer le repo sur Github, puis le cloner

On commence par cliquer sur le bouton O'Challenge pour générer le repo, mais si vous lisez ceci, c'est que c'est déjà fait.

Une fois le repo généré sur l'orga de la promo, on le clone sur sa machine avec la commande que l'on connait bien :wink:

:warning: __Rappel__ : on essaye de garder ses ateliers et les repos organisés dans sa machine, avec des dossiers pour chaque saison, et éventuellement pour chaque épisode.




## Étape 2 - Supprimer le dossier `.git/`

Une fois le projet cloné sur votre machine, on se rend dans le dossier (avec le Terminal Git Bash de préférence).
Dans le dossier du projet on va complètement supprimer (toujours avec le terminal) le dossier `.git/`.

Désormais le dossier de notre projet est complètement détaché de Github.
On va pouvoir le lier à un nouveau repo, que ce soit sur un autre compte ou une autre organisation.




## Étape 3 - Créer le second repo

On commence par se rendre sur la page des repositories de l'orga puis vous allez créer un nouveau repo que vous allez nommer `S01E14-atelier-github-votrepseudo-solution`.

:warning: _Cette fois-ci on ne coche pas la case `Add a README file` puisque le fichier existe déjà dans le dossier du projet.

Vous devriez arriver sur une page qui ressemble à ceci:
![New Repo](https://cdn.discordapp.com/attachments/1208043598558400520/1217374888566980698/image.png?ex=6603cbb7&is=65f156b7&hm=ee44c28f21304a90fb0ad56ba9eb8eb7a5767d295328b821ea6f5ac8fc2fe9f4&)

Notez que l'on ne clone pas ce repo 😉




 ## Étape 4 - Relier le nouveau repo Github au projet local

On retourne donc sur son terminal, en faisant évidemment attention de bien se placer dans le dossier de notre projet.

Puis on effectue les commandes indiquées (comme ci-dessous), en remplaçant bien sûr le lien SSH par celui de votre propre repo.

Une fois dans le dossier du projet :
```bash
git init
git add README.md
git commit -m "first commit"
git remote add origin git@github.com:O-clock-DWA-Session1/test-charly.git (à remplacer par votre lien SSH)
git push -u origin master
```

Et voilà, le dossier du projet devrait être bien relié à votre nouveau repo sur Github.




## Étape 5 - Rédiger le fichier Markdown

Maintenant que notre dossier de projet est prêt, on va pouvoir passer à la rédaction de notre fichier `instructions.md` en y consignant **dans l'ordre** toutes les étapes et commandes que l'on a effectué jusque là.

Il sera fortement apprecié de voir chacune des étapes accompagnée d'un petit commentaire pour indiquer quelle action on est en train d'effectuer, ainsi bien sûr que de la commande Terminal associée.

> _Exemple_
> 2. Je clone le repo avec la commande `$ git clone git@github.com:O-clock-DWA-Session1/test-charly.git`

On y rajoutera évidemment à la fin, les 3 étapes qui permettent de sauvegarder et d'envoyer son travail sur Github.

:warning: __Rappel__ : on essaye d'appliquer la logique algorithmique vues ces derniers jours. On rédige une série d'instructions avec un début et une fin, et sans ambigüité qui pourra être réalisée par n'importe qui (un collègue, une machine, etc...)




## Étape 6 - On envoie sur Github

On envoie son travail finalisé sur Github avec les 3 commandes que l'on connaît bien, en ayant bien ajouté ces étapes dans le fichier `instructions.md` en amont.





## Bonus 1 - Supprimer le repo généré par O'Challenge

Cette étape est **complètement optionnelle** !

Retournez sur le repo initial généré par le bouton O'Challenge, puis allez dans l'onglet " :gear:	Settings" du repo.

De là, on descend tout en bas de la page des paramètres, et vous verrez l'option "Delete repository".





## Bonus 2 - Le fichier .gitignore

Cette étape est **complètement optionnelle** !

Vous vous en souvenez peut-être que l'on a rapidement parlé de ce fichier et de son utilité.

En effet, dans un projet, il y a parfois certains fichiers ou dossiers que l'on ne souhaite pas envoyer sur Github.

> Pourquoi ?

Tout simplement parce que certains dossiers sont trop lourds et peuvent réinstallés autrement (on reparlera de dépendances plus tard dans votre formation).<br/>
Ou alors parce que certains fichiers contiennent des informations sensibles nécessaires au travail du développeur, comme des identifiants ou des mots de passe de connexion.

Et c'est ce que vous allez tester vous-même avec ce premier bonus.

Vous allez créer un nouveau fichier dans votre dossier de projet que vous allez nommer `identifiants.txt`

Dans ce fichier, vous allez y indiquer un email et un mot de passe factices. :warning: _ATTENTION_ : ne mettez pas de vraies informations dans ce fichier, ça serait dommage si ça se retrouvait en ligne :wink:

> _Exemple_
> email : charly@mail.fr
> password : azerty

Ensuite, on crée un fichier `.gitignore`, toujours à la racine du dossier du projet.
Dans ce fichier, on indique le nom du fichier sensible `identifiants.txt`

Maintenant, vous pouvez envoyer votre travail une nouvelle fois sur Github. Sur votre repo, vous devriez voir le fichier `.gitignore` dans lequel est indiqué le fichier `identifiants.txt`




## Bonus de La Muerte

Cette étape est **complètement optionnelle** !

_Bonus à réaliser pour les personnes très à l'aise avec toutes les notions précédemment vues pendant cette saison._

On crée un fichier HTML dans lequel on reprend les mêmes informations que notre fichier Markdown.

Vous avez compris, l'étape suivant le Markdown, c'est le HTML.

Vous serez donc autonomes quant à vos recherches sur les différentes balises à utiliser, leur sémantique, la structure de votre fichier, etc...

Bien entendu, on reste à votre disposition si vous avez des questions, des incompréhensions concernant cette étape bonus :wink:


