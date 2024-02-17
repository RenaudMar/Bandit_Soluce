# Ennoncé

The password for the next level is stored in the file data.txt, which contains base64 encoded data

## Solution


Nous commencons par nous connecter en ssh au serveur

	> ssh bandit10@bandit.labs.overthewire.org -p 2220
	> G7w8LIi6J3kTb8A7j9LgrywtEUlyyp6s

Dans l'énoncé nous voyons que le mdp est store dans le fichier data.txt nous testons un cat sur le file pour voir son contenue

	> cat data.txt

Nous savons que ca n'est pas le mdp car l'énnoncé nous dis clairement que c'est en base64 mais le terminal peut nous aider a le décoder.

	> base64 -d data.txt

cela return:

	> The password is 6zPeziLdR2RKNdNYFNb6nVCKzphlXHBM

Nous obtenons le mdp du bandit 11 et nous pouvons nous lancer vers la suite :)
