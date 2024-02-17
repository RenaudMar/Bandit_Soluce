# Ennoncé

The password for the next level is stored in a hidden file in the inhere directory.

## Solution

Nous devons nous connecter en ssh sur le serveur avec l'username et le mdp de bandit3

	ssh bandit3@bandit.labs.overthewire.org -p 2220
	aBZ0W5EmUfAf7kHTQeOwd8bauFJ2lAiG

Dans l'énnoncés nous voyons que le dossier est caché dans le dossier inhere dans le home de l'utilisateur bandit3.
Nous allons nous rendre dans le fichier avec la commande cd

	cd inhere

Ensuite, nous devons faire la commande ls avec quelques arguments supplémentaires pour voir les fichiers ou dossiers cachés.

	ls -la

Ce qui nous montres un fichiers caché du nom de .hidden
Nous allons procéder a ce que les anciens level nous ont appris avec la commande cat et certain nom de fichier

	cat < .hiden

et voilà nous avons le mdp de bandit4

	2EW7BBsr6aMMoJ2HjW067dm8EgX26xNe

Nous nous rendons donc au prchain niveau ! LET'S GOOO !!! 