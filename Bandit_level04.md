#Ennoncé

The password for the next level is stored in the only human-readable file in the inhere directory. Tip: if your terminal is messed up, try the “reset” command.

Nous nous connectons au serveur avec le ssh sur le serveur

	ssh bandit4@bandit.labs.overthewire.org -p 2220
	2EW7BBsr6aMMoJ2HjW067dm8EgX26xNe

Dans ce level nous avons plusieurs fichiers présent dans le dossier inhere.
Nous pouvons soit cat chaque fichiers car il y en a 10 mais nous pouvons aussi faire une autre méthode car nous savons que le fichier que l'on recherche est le seul a être Human-Readable

file ./-file*

Avec cette commande nous allons demander de voirce que sont les différents fichiers nommé -file

Nous voyons que un fichier utilise un ascii text.
Nous allons donc le cat car il est le seul que nous pouvons lire 

cat ./-file007
lrIWWI6bB37kxfiCQZqUdOIYfr6eEeqR

