#Ennoncé

The password for the next level is stored somewhere on the server and has all of the following properties:

    owned by user bandit7
    owned by group bandit6
    33 bytes in size

Nous commencons par nous connecter en ssh au bandit6
	
	ssh bandit6@bandit.labs.overthewire.org -p 2220
	P4L4vucdmLnm8I7Vl7jG1ApGSfjYKqJU

Nous voyons dans la consigne que le mdp est quelques part sur le serveur nous allons allons donc utiliser la même commande que dans l'excercise précédent.

	find / -user bandit7 -group bandit6 -size 33c -type f

Nous voyons que plusieurs fichiers correspondent a cette recherche, mais pas de panique, nous voyons que beaucoup de ces fichiers sont permission denied.
Il y a un seul fichier qui correspond a cette recherche et ou l'user bandit6 a les permission 
	
	/var/lib/dpkg/info/bandit7.password

Nous avons maintenant connaissance de ce fichier et nous pouvons le cat

	cat /var/lib/dpkg/info/bandit7.password
	z7WtoNQU2XfjmMtWA8u5rN4vzqu4v99S

Et voilà nous possedons le mdp pour le bandit7 !