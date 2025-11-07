# jeu
**Principe du jeu :**

Vous venez de lancer votre PC et vous avez été attaqué par un hacker qui veut vous tester.
Pour ce faire il a lancer un programme malveillant camouflé parmis vos fichiers et a caché un mot de passe dans un autre.

**Votre mission :**
  1) Neutraliser la menace : identifier, localiser et arrêter le fichier malveillant.
  2) Récuperer le mot de passe

**Résolution du jeu :**
  1) Identification et localisation du fichier : utilisation de pas aux, pipe et grep pour récuperer le PID du fichier 
  2) Neutralisation : utilisation de kill
  3) Récuperation du mot de passe : utilisation de tail

**Détails techniques :**
  
**initialisation :**
    - Nettoie les anciennes parties pour assurer la rejouabilité du jeu grâce (killall, rm)
    - Affiche les instructions du jeu (echo)
    
 **malware_simule :**
    - Crée le fichier malveillant à l'aide d'une boucle infinie avec une pause (while true et sleep)
    - Génere un code aléatoire et l'écrit dans un fichier de référence et dans un log public ($RANDOM et /tmp/...)

**verif :**
  - Vérifie que le PID cible est mort (kill -0)
  - Demande le code secret au joueur (read)
  - Compare le code de référence au code secret du joueur

***/!\ Attention ! Pensez bien à donner des permissions à initialisation et verif avant de commencer le jeu (chmod +x <fichier>) /!\***
