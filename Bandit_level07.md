# Bandit 7

## Ennoncé

The password for the next level is stored in the file data.txt next to the word millionth

## Solution

Pour commencer nous nous connectons au serveur ssh encore une fois!

	ssh bandit7@bandit.labs.overthewire.org -p 2220
	z7WtoNQU2XfjmMtWA8u5rN4vzqu4v99S

Quand nous sommes connecté si on fais un ls dans le dossier home de l'user bandit7 (l'endroit ou nous somme présent quand nous nous connectons) nous voyons le fichier data.txt
Comme dis dans l'énnoncé le mdp est situé a coté du mot millionth, nous allons donc utilisé la commande grep

	grep millionth data.txt
	millionth TESKZC0XvTetK0S9xNwm25STk5iWrBvP

Voilà nous avons obtenue le mdp de l'user bandit8 

	TESKZC0XvTetK0S9xNwm25STk5iWrBvP

GAS ! GAS ! GAS to the next LEVEL !!