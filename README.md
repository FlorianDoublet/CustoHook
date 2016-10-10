# RefactoringClientServerGit
Outils de refactoring client/serveur sous Git automatisé, dans le cadre du premier projet d'OPL.

  L’implémentation est presque entièrement automatique, mais requiert cependant quelques interactions de la part de l’utilisateur. L'ensemble a été conçu de sorte à ce que l’installation soit la plus simple possible avant de pouvoir utiliser notre application.

  Tout d’abord, l'ensemble de l’application qui se greffe au projet se trouve dans un dossier “hooks” qui devras être placé à la racine de projet Git par le propriétaire du projet.

  Ensuite, le contributeur, qui aura donc cloné le projet et aura optionnellement fournit son propre fichier de configuration pour le refactoring (sinon celui par defaut est pris en compte), devras lancer un script intitulé “setup_hooks.py” en Python3. Celui-ci s’occupera de rajouter la fonction qui override Git dans son bashrc, si elle n’est pas déjà présente. Le cas échéant, il se contentera d'ajouter le chemin du projet dans celle-ci afin de détecter le projet Git comme étant géré par notre application.

  La partie refactoring, qui fait également partie de notre projet, à été géré sur ce répository : https://github.com/MickaelAlvarez/CodeStyleFormatter
