# Projet de TD - Jeu de Memory en JavaScript

[Lien direct vers le jeu jouable en ligne](https://ElyasAhm4di.github.io/js-memory-game/)

## Le projet en quelques mots
Ce dépôt contient mon rendu pour le TD de BUT Informatique 2A. Il s'agit d'un jeu de Memory classique, mais l'enjeu était avant tout de coder toute la logique en JavaScript pur. L'objectif principal était d'apprendre à bien séparer les données (ce qui se passe dans la mémoire du jeu) de l'affichage (le DOM).

Ce qui a été le plus formateur n'est pas l'interface, mais bien la gestion de l'état du jeu en JS : réussir à bloquer les clics parasites du joueur pendant que les cartes se retournent et bien gérer les délais asynchrones pour ne pas casser le déroulement de la partie.

## Ce qui fait tourner le jeu
C'est un projet presque exclusivement centré sur le JavaScript.
- **JavaScript (Vanilla JS ES6)** : Le cœur du projet. J'ai tout codé à la main, sans aucun framework, pour bien assimiler la mécanique des événements et de la manipulation du DOM.
- **CSS3 (CSS Grid)** : Surtout utilisé pour structurer la grille de jeu, ce qui permet d'aligner les cartes de façon propre et réactive.
- **HTML5** : La structure de base pour accueillir le script.

## Les points techniques abordés en JS
Le cahier des charges du TD m'a fait travailler sur plusieurs mécaniques spécifiques :
- **L'algorithme de Fisher-Yates** : Je l'ai codé pour mélanger le tableau de cartes de façon mathématiquement aléatoire avant chaque nouvelle partie.
- **La gestion du temps (Asynchronisme)** : J'ai utilisé `setTimeout` pour imposer une pause de 800 millisecondes quand le joueur se trompe de paire. Pendant ce laps de temps, une variable JS verrouille complètement le plateau pour empêcher le joueur de cliquer partout.
- **La génération du DOM** : Au lieu d'écrire le code HTML des cartes à la main, c'est la fonction JS `initGame()` qui fabrique et injecte toute l'interface sur la page au démarrage.
- **L'accessibilité** : Le script ajoute dynamiquement les attributs ARIA et les propriétés `tabindex` sur chaque carte générée pour que le jeu soit navigable correctement.

## Tester sur votre machine
Si vous avez envie de jeter un œil au code ou de tester la logique JS chez vous :
1. Récupérez le projet en clonant ce dépôt ou en téléchargeant l'archive.
2. Ouvrez le dossier dans votre éditeur (VS Code par exemple).
3. Lancez simplement le fichier `index.html` via l'extension Live Server.
(La console du navigateur, accessible via F12, est très pratique pour suivre l'exécution en arrière-plan).