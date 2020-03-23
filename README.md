# Cours-git

Cours git signes et formations

!!! Pro tip: Git, c'est sombre et mystique au début, c'est pourquoi il est fortement recommandé de vous en servir pour TOUS vos prochains projets, surtout ceux qui se réalisent en équipe, afin que git devienne naturel chez vous. Par exemple, je m'en sers moi-même pour noter, ranger, classer tous les cours/conférences que je suis ammené à suivre pendant mes formations. POURQUOI s'embêter avec ca? Car avec de la pratique, utiliser cet outil sera comme respirer pour vous, et un pro git est très souvent apprécié en entreprise (vu que ca parraît sombre, mystérieux et magique pour ceux qui ne savent pas l'utiliser). !!!

## GIT ? C'est quoi ?

Créé par l'éminent Linus Torvalds, git est un gestionnaire de version, c'est à dire qu'il permet entre autres de gérer l'ajout de nouvelles features sur un projet sans qu'il n'y ait de conflit entre les différentes versions.

En effet, imaginez-vous en train de travailler sur un projet en même temps que toute une équipe;
Si des modifications sont faites par plusieurs personnes sur le même fichier, sans git, il faudrait passer un temps fou pour toutes les fusionner, et en cas de bug ce serait l'enfer pour revenir a une version stable.

De plus, git est la base du logiciel libre: le logiciel libre est le partage de codes sources sur des plateformes git telles que github, gitlab ou bitbucket, permettant a tout le monde de pouvoir collaborer librement à un projet même sans en connaître les auteurs). C'est un réel réseau social des dévelopeurs.

Pour un développeur débutant cherchant un travail, il peut aussi être intéressant d'avoir un github recensant les projets qu'il a réalisé, comme un portfolio de ses compétences.

Enfin, les gestionnaires de package tels que npm, brew, etc... fonctionnent avec git.

Bref, pour résumer, imaginez un bouton "sauvegarde" avant un boss de jeu vidéo, et imaginez que vous avez un nombre infini de slots de sauvegarde. Git, c'est ça.

## Sommaire

Nous utiliserons un mix entre la méthodologie 42 et un cours "normal"; vous devrez réaliser une série d'exercices dont les connaissances vous auront été expliquées brièvement à l'oral. Pour chaque exercice vous aurez aussi une base de connaissances dans ce fichier. Ainsi, vous pourrez garder ce cours et vous en servir comme une CheatSheet, et/ou refaire les exercices chez vous.

Ce cours sera décomposé en 4 grandes parties:

* partie1 **Add, Commit, Push**: Ici vous créerez votre premier repository et aprendrez a vous en servir de manière basique, en sauvegardant votre travail de manière régulière.

* partie2 **Le versionning**: Dans cette partie, vous apprendrez à naviguer entre les différentes versions de votre code.

* partie3 **Les branches**: Une nouvelle feature dans votre code? Ne cassez pas ce qui fonctionne déjà et développez votre feature en toute sécurité.

* partie4 **Les merge**: Fuuuuu-sion! Découvrez comment fusionner vos branches entre elles une fois que tout fonctionne.

Et enfin une **cheatsheet** dans laquelle vous irez piocher vos commandes pour les exercices.

## Partie1: Add, Commit, Push

Bravo! Tu viens de changer de branche. Tu pourras répéter l'opération pour aller sur les parties suivantes une fois celle-la terminée. Si tu souhaites retourner voir la branche principale, elle s'appelle master donc... `git checkout master`. Ici, tu vois donc que ce fichier n'a plus du tout la même tête, et tu pourras aussi voir que de nouveaux fichiers sont apparus.

### Exercice 0: Un nouveau repo, si c'est pas beau!

Tu arrives juste en stage et ton nouveau patron te demande de créer un nouveau projet qui va servir a dire bonjour aux personnes qui entrent dans le batîment.
Direction github! va sur ton compte et crée-toi un nouveau repository, puis clone-le sur ta machine. Les prérequis pour créer ton repo sont en photo dans les images.

### Exercice 1: hello world

Code un hello world (programme qui une fois lancé affiche "hello world", au caractère près) dans le language de ton choix, add les fichiers, commit avec le bon message (voir la partie norme des commits après le lexique), puis push le tout. Montre-moi ton github une fois que c'est fait.

### Exercice 2: Hello World!

Ton patron vient de te passer un savon parceque tu as oublié les majuscules et le point d'exclamation. Ton programme doit maintenant sortir un "Hello World!". Modifie-le, add les modifications, commit, puis push le tout et appelle-moi.

### Exercice 3: Readme? c'est quoi ce fichier?

Ton patron revient te voir, te félicite pour ta nouvelle orthographe, mais exige que tu supprimes ton Readme parceque "de toute manière il est vide". Bla, bla, bla et appelle-moi, tu connais la musique maintenant.

### Exercice 4: Changement de machine

En rentrant chez toi tu t'est rendu compte que tu avais échangé ton ordi avec celui de ton collègue, et ton patron t'appelle pour te dire qu'il veut que tu remettes un README.md avec indiqué dedans le nom du projet, et comment l'installer/le lancer. Exemple: <https://github.com/jojomon42153/LIBFT>
Tu prends donc l'ordi de ton binôme (lui prendra le tien), tu clones ton projet, tu ajoutes un README.md convenable et tu push
("Mais il sert a rien cet exo" => sisi, tkt, regarde l'exo suivant).

### Exercice 5: Retour au travail

Le lendemain matin, tu récupères donc ton ordi auprès de ton collègue. Il te faut maintenant récupérer sur ta machine les modifications que tu as push la veille, sans faire de "git clone".

## Lexique des commandes

### La base

* `git clone https://github.com/mon_pseudo_github/ZeBestRepoEver.git`: ~télécharge~ clone le repository git de l'adresse pasée en paramètre.
* `git status`: affiche où l'on en est dans les commits (fichiers modifiés, supprimés, ajoutés, ou tout simplement si on a des commits a push)
* `git add fichier`: ajoute un nouveau fichier ou un fichier modifié au prochain commit
* `git rm fichier_que_je_veux_supprimer`: supprime un fichier du repo au prochain commit
* `git commit -m "mon message de commit"`: commit(sauvegarde) les modifications faites et ayant été ajoutées au commit via `git add` ou `git rm`
* `git push`: envoie tous les commits sur le repertoire distant
* `git pull`: "Récupère les derniers commits sur le repo distant qui ne sont pas présent en local. Assurez-vous de ne pas avoir fait de modifications en local avant, sous peine de vous exposer, en cas de modification du meme fichier, aux "merge conflicts" => partie 4 et si ca t'arrive maintenant, appelle-moi.

### Les branches

* `git checkout nom_de_ma_branche`: change de branche pour aller sur "nom_de_ma_branche"

## Norme des commits

Et oui, puisqu'on parle d'entreprise, on parle aussi de norme ou de conventions! Ici, on va apprendre a bien nommer ses commits puisqu'ils font office de description des modifications.
Imaginez-vous chercher un commit en particulier, et trouver des messages du type "LOL" ou "ya plein de trucs" ou "push" ou quoi que ce soit d'autre qui n'explique en rien ce qui a été fait! (exemple en image)
En soi, il peut y avoir une norme propre à l'entreprise dans laquelle vous travaillez ou pas du tout de norme.
Je vous en propose 2 ici, la mienne (quand c'est un petit projet) + celle d'angular (quand le projet est beaucoup plus volumineux):

### La mienne

``` jojoCode

    [mon_nom]
    -fichier_en_question1 => nature_de_la_modification: description
    -fichier_en_question2 => natu...

    // ou si plusieurs fichiers sont affectés par une meme modification

    [mon_nom]
    -nature_de_la_modification <fichiers> => description

```

Nature de la modification:

* fix = réparation d'un bug
* add = ajout d'un truc (add feat, add file, add tout court, on s'en fout tant que ça parle)
* del/rm = suppression d'un truc
* refactor = change la tete du code sans changer le fonctionnement
* comment = ajoute des commentaires
* perf = améliore les perf
* ... regarde la norme angular plus bas il y a plein de bonnes idées (dans ta tete aussi il y en a peut-être)
  
Exemple: fais un `git log` dans ton terminal et tu verras mes commits sur cette branche. Appuye sur les flèches pour te déplacer dedans, et sur Q pour quitter le log.

### Angular

[Ce site](https://buzut.net/git-bien-nommer-ses-commits/) l'expliquera mieux que moi:
