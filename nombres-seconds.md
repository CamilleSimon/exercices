# Après les nombres premiers : les nombres seconds !
Exercice provenant de l'Université de Technologie de Belfort Montbéliard (UTBM) - UTBM

Eratosthène, mathématicien grec du IIIème siècle avant notre ère, inventa un procédé de calcul des nombres premiers, dénommé crible d'Eratosthène, qui est une définition algorithmique des nombres premiers. Son principe est :
- **A.** On considère les nombres entiers plus grands que 1. Le ***premier*** de ces nombres, par définition, est un "nombre ***premier***".
- **B.** Nommons ensuite "nombre *premier*" le ***premier entier*** non divisible par un nombre premier déjà trouvé et plus grand que ceux déjà trouvés.
- **C.** Recommençons l(opération précédente tant que cela est possible. Cela définit la suite des nombres *premiers*.

Prenons l'ensemble des entiers plus grands que 1 :

| Nb      |  2 |  3 |  4 |  5 |  6 |  7 |  8 |  9 | 10 | 11 | 12 | 13 | 14 | 15 | 16 | 17 | 18 | 19 | 20 | 21 | 22 | 23 | 24 | 25 | 26 |
| :------ | :- | :- | :- | :- | :- | :- | :- | :- | :- | :- | :- | :- | :- | :- | :- | :- | :- | :- | :- | :- | :- | :- | :- | :- | :- |
| Couleur |  N |  N |  N |  N |  N |  N |  N |  N |  N |  N |  N |  N |  N |  N |  N |  N |  N |  N |  N |  N |  N |  N |  N |  N |  N |
| Nb      | 27 | 28 | 29 | 30 | 31 | 32 | 33 | 34 | 35 | 36 | 37 | 38 | 39 | 40 | 41 | 42 | 43 | 44 | 45 | 46 | 47 | 48 |    |    |    |
| Couleur |  N |  N |  N |  N |  N |  N |  N |  N |  N |  N |  N |  N |  N |  N |  N |  N |  N |  N |  N |  N |  N |  N |    |    |    |

Marquons en bleu (lettre B) le premier de ces nombres, 2 ; ce sera le plus petit nombre premier.

| Nb      |  2 |  3 |  4 |  5 |  6 |  7 |  8 |  9 | 10 | 11 | 12 | 13 | 14 | 15 | 16 | 17 | 18 | 19 | 20 | 21 | 22 | 23 | 24 | 25 | 26 |
| :------ | :- | :- | :- | :- | :- | :- | :- | :- | :- | :- | :- | :- | :- | :- | :- | :- | :- | :- | :- | :- | :- | :- | :- | :- | :- |
| Couleur |  B |  N |  R |  N |  R |  N |  R |  N |  R |  N |  R |  N |  R |  N |  R |  N |  R |  N |  R |  N |  R |  N |  R |  N |  R |
| Nb      | 27 | 28 | 29 | 30 | 31 | 32 | 33 | 34 | 35 | 36 | 37 | 38 | 39 | 40 | 41 | 42 | 43 | 44 | 45 | 46 | 47 | 48 |    |    |    |
| Couleur |  N |  R |  N |  R |  N |  R |  N |  R |  N |  R |  N |  R |  N |  R |  N |  R |  N |  R |  N |  R |  N |  R |    |    |    |

Marquons en rouge (lettre R) les autres multiples de 2 qui ne pourront pas être des nombres premiers (nous pourrions aussi les éliminer de la liste, mais nous préférons les garder en rouge pour bien visualiser la méthode et sa génération).

D'après B., le nombre 3 (le **premier** nombre resté noir situé après 2) est un nombre **premier**. Marquons-le en bleu et marquons en rouge tous les multiples de 3 non déjà marqués.

| Nb      |  2 |  3 |  4 |  5 |  6 |  7 |  8 |  9 | 10 | 11 | 12 | 13 | 14 | 15 | 16 | 17 | 18 | 19 | 20 | 21 | 22 | 23 | 24 | 25 | 26 |
| :------ | :- | :- | :- | :- | :- | :- | :- | :- | :- | :- | :- | :- | :- | :- | :- | :- | :- | :- | :- | :- | :- | :- | :- | :- | :- |
| Couleur |  B |  B |  R |  N |  R |  N |  R |  R |  R |  N |  R |  N |  R |  R |  R |  N |  R |  N |  R |  R |  R |  N |  R |  N |  R |
| Nb      | 27 | 28 | 29 | 30 | 31 | 32 | 33 | 34 | 35 | 36 | 37 | 38 | 39 | 40 | 41 | 42 | 43 | 44 | 45 | 46 | 47 | 48 |    |    |    |
| Couleur |  R |  R |  N |  R |  N |  R |  R |  R |  N |  R |  N |  R |  R |  R |  N |  R |  N |  R |  R |  R |  N |  R |    |    |    |

Toujours d'après B., le nombre 5 (le **premier** nombre resté noir situé après 3) est un nombre **premier**. Nous le marquons en bleu.

En poursuivant, nous obtenons en bleu la liste des nombres premiers.
2, 3, 5, 7, 11, 13, 17, 19,...
Eric Angelini a proposé de suivre la définition milléaire A-B-C en remplaçant le mot **premier** par le mot **second** ou le mot **troisième**, etc.. Cette généralisation élémentaire de la définition des nombres premiers conduit donc aux définitions des nombres **seconds**, des nombres **troisièmes**, etc., définitions qui, très étrangement, ne semble avoir été envisagées par personne avant novembre 2006 !

Examinons les nombres **seconds**. Leur définition est donnée par la généralisation du crible d'Eratosthène.
- *A-* On considère les nombres entiers plus grands que 1. Le **second** de ces nombres, par définition est un "nombre **second**".
- *B-* Nommons ensuite "nombre **second**" le **second** entier non divisible par un nombre **second** déjà trouvé et plus grand que ceux déjà trouvés.
- *C-* Recommençons l'opération précédente tant que cela est possible. Cela définit la suite des nombres **seconds**.

Au départ, on a l'ensemble des entiers plus grands que 1, tous marqués en noir

| Nb      |  2 |  3 |  4 |  5 |  6 |  7 |  8 |  9 | 10 | 11 | 12 | 13 | 14 | 15 | 16 | 17 | 18 | 19 | 20 | 21 | 22 | 23 | 24 | 25 | 26 |
| :------ | :- | :- | :- | :- | :- | :- | :- | :- | :- | :- | :- | :- | :- | :- | :- | :- | :- | :- | :- | :- | :- | :- | :- | :- | :- |
| Couleur |  N |  N |  N |  N |  N |  N |  N |  N |  N |  N |  N |  N |  N |  N |  N |  N |  N |  N |  N |  N |  N |  N |  N |  N |  N |
| Nb      | 27 | 28 | 29 | 30 | 31 | 32 | 33 | 34 | 35 | 36 | 37 | 38 | 39 | 40 | 41 | 42 | 43 | 44 | 45 | 46 | 47 | 48 |    |    |    |
| Couleur |  N |  N |  N |  N |  N |  N |  N |  N |  N |  N |  N |  N |  N |  N |  N |  N |  N |  N |  N |  N |  N |  N |    |    |    |

On marque en bleu le second de ces nombres, 3, ce sera un nombre **second**, et on marque en rouge tous les multiples de 3, ils ne pourront pas être des nombres seconds.

| Nb      |  2 |  3 |  4 |  5 |  6 |  7 |  8 |  9 | 10 | 11 | 12 | 13 | 14 | 15 | 16 | 17 | 18 | 19 | 20 | 21 | 22 | 23 | 24 | 25 | 26 |
| :------ | :- | :- | :- | :- | :- | :- | :- | :- | :- | :- | :- | :- | :- | :- | :- | :- | :- | :- | :- | :- | :- | :- | :- | :- | :- |
| Couleur |  N |  B |  N |  N |  R |  N |  N |  R |  N |  N |  R |  N |  N |  R |  N |  N |  R |  N |  N |  R |  N |  N |  R |  N |  N |
| Nb      | 27 | 28 | 29 | 30 | 31 | 32 | 33 | 34 | 35 | 36 | 37 | 38 | 39 | 40 | 41 | 42 | 43 | 44 | 45 | 46 | 47 | 48 |    |    |    |
| Couleur |  R |  N |  N |  R |  N |  N |  R |  N |  N |  R |  N |  N |  R |  N |  N |  R |  N |  N |  R |  N |  N |  R |    |    |    |

Le **second** nombre non marqué en rouge placé au-delà de 3 est 5. Par définition, il s'agit d'un nombre **second**. On le marque en bleu et on marque en rouge tous les multiples de 5 non déjà marqués.

| Nb      |  2 |  3 |  4 |  5 |  6 |  7 |  8 |  9 | 10 | 11 | 12 | 13 | 14 | 15 | 16 | 17 | 18 | 19 | 20 | 21 | 22 | 23 | 24 | 25 | 26 |
| :------ | :- | :- | :- | :- | :- | :- | :- | :- | :- | :- | :- | :- | :- | :- | :- | :- | :- | :- | :- | :- | :- | :- | :- | :- | :- |
| Couleur |  N |  B |  N |  B |  R |  N |  N |  R |  R |  N |  R |  N |  N |  R |  N |  N |  R |  N |  R |  R |  N |  N |  R |  R |  N |
| Nb      | 27 | 28 | 29 | 30 | 31 | 32 | 33 | 34 | 35 | 36 | 37 | 38 | 39 | 40 | 41 | 42 | 43 | 44 | 45 | 46 | 47 | 48 |    |    |    |
| Couleur |  R |  N |  N |  R |  N |  N |  R |  N |  R |  R |  N |  N |  R |  R |  N |  R |  N |  N |  R |  N |  N |  R |    |    |    |

Le **second** nombre non marqué en rouge placé au-delà de 5 est 8. Par définition, il s'agit d'un nombre second. On le marque en bleu et on marque en rouge tous les multiples de 8 non déjà marqués...
On obtient ainsi la liste en bleu des nombres **seconds** : 3, 5, 8, 13, 17, 22, 28, 31,...
La définition des nombres troisièmes - on recopie les régles A-B-C en remplaçant premier par toisième - conduit de la même façon à un marquage des entiers en bleu, rouge et noir.

## Objectifs du programme dont vous ferez les algorithmes :

Déterminer et afficher la liste des nombres permiers, ou seconds, ou etc...

Pour ce faire on enregistre la couleur associée à un nombre dans un tableau de caractères. L'indice du tableau permettra bien évidemment d'accéder aux nombres, la case d'indice 1 ne sera pas utilisé. La case d'indice i contient la couleur associée au nombre i. On n'utilisera pas de tableau dédié au stockage des nombres.

1. Ecrire une fonction _noircir_ qui permet de mettre la couleur noir (i.e. que le contenu de la case du tableau sera le caractère 'N') dans chaque case d'un tableau de taille *n*.
2. Ecrire une fonction _affichage_, prenant en parametre le tableau et une couleur et affichant tous les nombres de cette couleur. 
3. Ecrire une fonction _multiple_ permettant de colorier en rouge (i.e. affecter 'R') les nombres multiples du paramètre *nb*.
4. Ecrire une fonction dont l'entête est : *function nbsuivant (t:tableau, n:Integer, type:Integer, derniernb:Integer):Integer* permettant de mettre en bleu ('B') le nombre permier, second, etc. suivant et de retourner sa valeur.
5. Ecrire un programme principal qui affichera la liste des nombres demandés par l'utilisateur en faisant appel aux fonctions précédentes. Le choix du type de nombre sera stocké sous forme numérique (*Type=1* pour les nombres premiers, *Type=2* pour les nombres seconds, *Type=3* pour les nombres troisièmes, etc.) avec 1<=Type<=10. L'utilisateur indiquera la borne supérieure pour la recherche des nombres, Maxi : 500. 
