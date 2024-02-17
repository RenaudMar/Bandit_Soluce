# Ennoncé
The password for the next level is stored in a file called - located in the home directory

## Solution
Pour ce level nous nous connectons au ssh avec le username bandit1 avec le mdp recus précédement

	> ssh bandit1@bandit.labs.overthewire.org -p 2220
	> NH2SXQwcBdpmTEzi3bvBHMM9H66vVXjL

Comme dis dans l'énnoncé le mdp devrait se trouvé dans le fichier nommé "-", mais nous ne pouvons pas cat un fichier -
il y a deux manière de cat ce genre de nom de fichier avec 


	> cat ./-
	> cat < -

Et grace a cette commande nous allons avoir accès au contenue du fichier 

	> rRGizSaX8Mk1RTb1CNQoXTcYZWU6lgzi