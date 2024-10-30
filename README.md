Exigences techniques pour chaque fonctionnalité :  

 

Menu principal :  

Options pour démarrer une nouvelle partie : crée un nouveau fichier, si on crée une nouvelle partie on supprime la potentielle partie en pause en la remplaçant. 

Charger une partie : reprise de la partie chargée en dernier. 

Voir les scores : lié à l’historique du pseudo. 

Quitter (le jeu) : (return 0), sortie du jeu, supprime la page ouverte. 

 

Configuration de la partie :  

 

Choix du nombre de joueurs : 2 ou 4 joueurs. 

Type de joueurs (humain ou ordinateur) : si option humain sélectionnée, mise en attente du joueur pendant le temps qu’il trouve un adversaire. 

Taille du plateau : taille allant de 9x9 à 12x12. 

 

Gestion du plateau : 

 

Affichage et initialisation du plateau de jeu avec position des pions et des barrières : les pions commencent face à face sur les lignes opposées. Les barrières sont distribuées équitablement 10 pour les 2 adversaire et 5 lorsqu’il sont 4 joueurs. A l’initialisation le plateau ne contient que les pions. 

 

Placement du pion : 

 

Permet aux joueurs de placer et déplacer leurs pions sur le plateau : déplacement du pion dans les 4 directions. S’il y a un pion en face, il y a la possibilité de passer au-dessus de ce pion. Impossible de franchir un mur ainsi que de sortir du plateau. 

 

Placement de la barrière : 

 

Permet aux joueurs de placer des barrières en respectant les règles du jeu : respecte au moins une case libre par ligne ou colonne. Taille des barrières est de 2 cases. Vérifier si le nombre maximum de barrière disponible n’est pas atteint. 

 

Option de jeu : 

 

Actions comme passer son tour, mettre en pause ou abandonner la partie : sauvegarde seulement le score de la partie précédente et non le plateau de jeu. Lorsque l’on passe son tour, on invite à jouer l’adversaire. Mettre en pause affiche un menu provisoire. Abandonner la partie affiche le score et efface le fichier de jeu et redirige vers le menu principal. 

 

Fin de la partie : 

 

Vérifie la victoire : système de coordonnées pour vérifier que le pion soit arrivé en premier à la ligne opposée.                                                                                                                                          Calcule les scores : 5 points pour la victoire et 0 point pour les autres cas                                             Affiche les résultats : affiche les scores de la partie                                                                                       Sauvegarde et charge l’état du jeu pour reprise ultérieure : sauvegarde du fichier de jeu 

 

Gestion de sauvegarde : 

 

Sauvegarde et charge l’état du jeu pour reprise ultérieure : avec le fichier de jeu sauvegardé. 

 

Gestion des erreurs :  

 

Gère les erreurs de saisie et fournit des messages d’erreur : si l’on effectue une action impossible affiche le message d’erreur. 
