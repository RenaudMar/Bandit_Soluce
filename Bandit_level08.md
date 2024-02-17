#Ennoncé
The password for the next level is stored in the file data.txt and is the only line of text that occurs only once

Nous commencons par nous connecter par ssh sur le serveur

	ssh bandit8@bandit.labs.overthewire.org -p 2220
	TESKZC0XvTetK0S9xNwm25STk5iWrBvP

Nous voyons que le mdp est une ligne ne se répétant pas dans le fichier, nous allons utiliser sort et uniq qui vont nous aider a retrouver cette ligne unique

nous allons donc utiliser la commande suivante

	sort data.txt| uniq -c

Nous obtenons la liste de toutes les lignes avec les nombres de fois qu'elles se répètent
Nous pouvons donc améliorer notre recherche avec un grep

	sort data.txt | uniq -c | grep '^ *1 '

	    ^: C'est un ancrage qui spécifie le début d'une ligne. Ainsi, la recherche sera effectuée au début de chaque ligne.

    *: Cela signifie zéro ou plusieurs occurrences de l'espace précédent. En d'autres termes, il recherche zéro ou plusieurs espaces au début de la ligne.

    1: Recherche le chiffre 1.

    (espace après le 1): Recherche un espace après le chiffre 1.

Nous obtenons donc 
	
	1 EN632PlfYiZbn3PhVK3XOGSlNInNE00t

nous avons le mdp de l'user bandit9 !
EN632PlfYiZbn3PhVK3XOGSlNInNE00t
