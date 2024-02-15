#Ennoncé

The password for the next level is stored in the file data.txt in one of the few human-readable strings, preceded by several ‘=’ characters.

Nous commencons par nous connecter par ssh au serveur
	
	ssh bandit9@bandit.labs.overthewire.org -p 2220
	EN632PlfYiZbn3PhVK3XOGSlNInNE00t

Nous cherchons le mdp dans un fichier qui ne possède que quelques ligne human-readable, nous allons donc utilisé la commande string et ensuite le grep car le mdp est précèdé de quelques =

	 strings data.txt | grep ===

	 x]T========== theG)"
	========== passwordk^
	========== is
	========== G7w8LIi6J3kTb8A7j9LgrywtEUlyyp6s

Nous avons le mdp pour le bandit 10 !
