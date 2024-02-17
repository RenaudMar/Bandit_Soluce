# Bandit 11

## Ennoncé

The password for the next level is stored in the file data.txt, where all lowercase (a-z) and uppercase (A-Z) letters have been rotated by 13 positions

## Solution

Nous nous connectons en ssh sur le serveur avec le mdp:

	ssh bandit11@bandit.labs.overthewire.org -p 2220
	6zPeziLdR2RKNdNYFNb6nVCKzphlXHBM

Alors dans l'énnoncé nous voyons que le mdp est store dans le fichier data.txt mais que les lettres on été bougés de 13 position c'est ce qu'on appel le ROT13

nous allons cat le fichier

	cat data.txt

Nous avons plusieurs méthodes, comme des sites qui peuvent nous aider dirrectement avec le rot13, mais nous allons utilisé la commande la plus utilisé pour cela c'est le tr:

	cat data.txt | tr 'A-Za-z' 'N-ZA-Mn-za-m'

Ce que tr fais est de prendre le premier ensemble 'A-Za-z' pour qualifier l ensemble de l'alphabet

Le deuxieme ensemble est 'N-ZA-Mn-za-m' Car la 13eme lettre de l'alphabet étant N nous allons spécifié que l'odre de notre alphabet est N et que une fois arrivé a Z il doit recommencer de A jusqu'a M pour avoir l'ensemble de l'alphabet.

Mais apres cette commande nous obtenons le mots de passe mais petits bonus !

	alias rot13="tr 'A-Za-z' 'N-ZA-Mn-za-m'"

	alias rot5="tr '0-9' '5-90-4'"

Avec ces commandes nous pourrons utiliser rot13 et rot 5 pour décripter a la place de devoir refaire le tr ;)

Voila vous avez obtenues le mdp Bravooo :) ! mais la difficulté n'est pas encore présente ^^

	JVNBBFSmZwKKOP0XbFXOoW8chDz5yVRv
