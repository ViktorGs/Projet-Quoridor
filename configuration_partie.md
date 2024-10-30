def configurer_partie():
    # Choix du nombre de joueurs
    while True:
        nombre_joueurs = input("Choisissez le nombre de joueurs (2 ou 4) : ")
        if nombre_joueurs in ['2', '4']:
            nombre_joueurs = int(nombre_joueurs)
            break
        else:
            print("Veuillez entrer 2 ou 4 uniquement.")

    # Choix du pseudo pour chaque joueur
    pseudos = []
    for i in range(1, nombre_joueurs + 1):
        pseudo = input(f"Entrez le pseudo du joueur {i} : ")
        pseudos.append(pseudo)

    # Choix du plateau
    tailles_possibles = {'1': (9, 9), '2': (13, 13)}
    while True:
        taille = input("Choisissez la taille du plateau (1: 9x9, 2: 13x13) : ")
        if taille in tailles_possibles:
            taille_plateau = tailles_possibles[taille]
            break
        else:
            print("Veuillez entrer 1 ou 2 uniquement.")

    # Initialisation du plateau
    plateau = [[0 for _ in range(taille_plateau[0])] for _ in range(taille_plateau[1])]
    print(f"Plateau de taille {taille_plateau[0]}x{taille_plateau[1]} initialisé.")

    # Initialisation des barrières
    barrieres_par_joueur = 10 if nombre_joueurs == 2 else 5
    print(f"Chaque joueur dispose de {barrieres_par_joueur} barrières.")

    # Retourne les paramètres de la partie
    return {
        "nombre_joueurs": nombre_joueurs,
        "pseudos": pseudos,
        "taille_plateau": taille_plateau,
        "plateau": plateau,
        "barrieres_par_joueur": barrieres_par_joueur
    }

# Exemple d'utilisation
parametres_partie = configurer_partie()
print("Configuration de la partie :", parametres_partie)



