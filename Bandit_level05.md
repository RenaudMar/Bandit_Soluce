# Bandit 5

## Ennoncé
The password for the next level is stored in a file somewhere under the inhere directory and has all of the following properties:

    human-readable
    1033 bytes in size
    not executable
## Solution


Pour ce niveau nous commencons par se connecter par ssh sur le serveur

	ssh bandit5@bandit.labs.overthewire.org -p 2220
	lrIWWI6bB37kxfiCQZqUdOIYfr6eEeqR

Pour commencer on nous dis que le mdp se trouve dans un fichier dans le dossier inhere

	cd inhere

Ensuite nous voyons que le fichier a une taille de 1003 bytes et il n'est pas un executable. Nous allons donc utiliser la commande find avec les arguments correspondant au fichier.

	find ./ -type f -size 1033c ! -executable

		./ signifie que nous cherchons dans les dossiers présent dans le dossier inhere
		-type f signifie que nous cherchons un fichier
		-sizze 1033c signifie la taille 1033 bytes
		! rends négatif la recherche de la valeur suivante
		-executable recherche d'un executable

Le terminal nous renvoies

	./maybehere07/.file2

Nous allons cat se fichier

	cat ./maybehere07/.file2

	P4L4vucdmLnm8I7Vl7jG1ApGSfjYKqJU

Nous obtenons le mdp de bandit 6 ! Bravoo!

