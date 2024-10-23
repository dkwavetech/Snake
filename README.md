# Jeu du serpent - Family Day

Le jeu du serpent est un jeu vidéo où le joueur contrôle un serpent qui doit manger des objets pour grandir tout en évitant de heurter les murs et son propre corps.

le jeu Snake est libre de droits et est souvent utilisé comme exemple pour l’apprentissage de la programmation.

Ce code crée un jeu de serpent simple où le joueur peut utiliser les touches fléchées pour contrôler le serpent, manger de la nourriture pour gagner des points. 
Dans cette version, il  n'y a pas de collisions avec les murs ou le propre corps du serpent.

# Accompagnement de l'enfant

**1- Présenter les fonctions principales du script js**
- créer le serpent
- dessiner

but consiste à expliquer à l'enfant la construction des éléments de base, reposant sur le plan cartésien.
Les enfants n'ayant pas tous le même niveau en mathématiques, représenter sur une feuille un plan 2d illsutrant deux axes perpendiculaires, l'abscisse et l'ordonnée. Indiquer ensuite à l'enfant que chaque case du jeu aura un abscisse et une ordonnée, et sera ensuite remplie d'une couleur pré définie.

Lors de la présentation des fonctions précédentes, se focaliser uniquement sur les valeurs attribuées aux coordonnées cartésiennes.

**2- Présenter la fonction de contrôle du serpent**

Le but est d'essayer un bout de code 

**3- Jouer**

Quelques minutes seront accordées à l'enfant pour profiter du jeu et s'amuser.


## Pédagogie

### Créer le serpent: ~ 2 minutes

        function creerSerpent() {
                var longueurDepart = 5; 
                serpent = [];
                for (var i = longueurDepart - 1; i >= 0; i--) {
                    serpent.push({x: i, y: 0});
                }
        }

On dessinera sur une feuille la longueur = 5 cm, et la largeur 1 cm.
Puis on expliquera le code brièvement à l'enfant en lui indiquant où se trouve l'initialisation de la longueur.
serpent.push({x: i, y: 0}); => permet d'incrémenter la longueur à partir de 0 jusqu'à atteindre 5 cm.
On peut s'arrêter à ce niveau d'information.

### Créer la nourriture: ~ 1 minute

Ensuite, expliquer à l'enfant qu'il s'agit du même process pour créer la nourriture.

Les explications suivantes ne sont pas nécessaires, sauf si l'animateur les juge utiles. 

On marquera de manière aléatoire positionner la nourriture à n'importe quel endroit du tableau de jeu, et la nourriture aura comme valeur x=1 & y=1.
Indiquer à l'enfant qu'on peut changer la taille des cases.

 
       function creerNourriture() {
                nourriture = {
                    x: Math.round(Math.random() * (LARGEUR - 20) / TAILLECASE),
                    y: Math.round(Math.random() * (HAUTEUR - 20) / TAILLECASE)
                };
        }

### Dessiner ~ 2 minutes

Montrez à l'enfant comment on peut changer la couleur du serpent et de la nourriture, en changeant directement la couleur à la ligne 373 et 376 (fonction appelante "actualiser").
Tester le changement de couleur: rouge = ff334c | violet = f633ff


### Contrôle du serpent ~ 5 minutes


        $(document).keydown(function (e) {



Expliquer à l'enfant qu'on écoute les évènements du clavier.
Chaque touche dispose d'un identifiant, lorsqu'on appuie sur une touche, on vérifie dans quelle direction le serpent doit être orienté.
Le jeu se base sur les touches "flèches" (haut, bas, gauche, droite), mais on peut tout à fait changer, et définir par exemple la touche 'g' comme notre touche gauche, et la touche 'h' comme notre touche droite.
Pour info: https://e-3d-dc1.capgemini.com/confluence/display/P001594/IDFM+PRIM+Home
**G : 71**
**H : 72**


        else if (key == "71" && direction != "gauche" && !touchePressee) {
            direction = "droite";
            touchePressee = true;
        }

Tester avec l'enfant en changeant l'identifiant dans le code.
L'enfant pourra ajouter un else pour l'action sur une touche supplémentaire. 


### Jeu ~ 2 à 5 minutes

Laisser l'enfant jouer quelques minutes pour s'amuser, en restant à ses côtés pour l'aider s'il souhaite apporter des modifications au code source.




  
