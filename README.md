# Test technique

Le but de ce test technique est de réaliser un composant Multiselect **réutilisable**, **maintenable** et **lisible** en HTML/CSS et Javascript.

Exemple de Multiselect : [https://vue-multiselect.js.org/](https://vue-multiselect.js.org/)

Ce test est divisé en plusieurs niveaux, il est très important de respecter le sens des niveaux et de ne passer au niveau suivant qu'apres avoir reussi le niveau precedent. En cas de niveau inachevé, complétez le CHANGELOG.MD du projet afin de dire ce sur quoi vous n'avez pas réussi et/ou les difficultés rencontrées.

# Différents niveaux

## Niveau I
- Le Multiselect doit posséder les propriétés suivantes : options, placeholder.
- Lors d'un clic, une liste doit se dérouler affichant le texte des différentes options
- Lors d'un clic en dehors, il doit etre possible de fermer le multiselect

## Niveau II
- Une fois le Multiselect ouvert, un clic sur une des options, referme le Multiselect et ajoute un tag en haut du Mutiselect 
- Si une option est devenue un tag, elle ne doit plus apparaitre dans la liste des options restantes
- Chaque tag possède une croix qui lui permet de l'enlever. L'option reapparait alors dans la liste du Multiselect.

## Niveau III
- Le multiselect se voit ajouter un champ de texte à la manière de ([https://vue-multiselect.js.org/](https://vue-multiselect.js.org/)). 
- Lorsque le Multiselect est ouvert, saisir du texte dans cet input, filtre la liste des options disponibles en fonction de celles qui contiennent le texte saisi
- Prévoir le cas où aucun résultat n'est trouvé dans le Multiselect apres saisie trop specifique dans le filtre texte

## Niveau IV (Bonus)
- Le Multiselect possède une propriété 'multi'
- Si le mode multi est activé, alors le fait de cliquer sur une option ne referme pas le multiselect, a la maninere de (https://vue-multiselect.js.org/)


# Règles du jeu
I. Le test technique s'effectuera sous le framework Javascript Vue.js exclusivement

II. Aucun framework CSS (Bootstrap, Material, etc) n'est autorisé. Seule l'utilisation du pré-processeur SASS est autorisée pour plus de lisibilité. (Si des icones devaient etre utilisées, une librairie comme Font-Awesome ayant un but aussi precis est autorisé).

III. Il est strictement interdit d'utiliser d'autres librairies que celles installées, le but ici est de créer quelque chose from scratch pour tester vos connaissances, alors tout écart sera sanctionné d'une élimination automatique du candidat.

IV. A chaque niveau de l'exercice, vous effectuerez un commit portant le nom de "Niveau {numero du niveau}". 

V. Une fois l'exercice terminé, vous pourrez rendre ensuite cet exercice sous la forme d'un ZIP ou d'un repo git hébergé par vos soins. (Si .ZIP, merci de ne pas inclure le dossier node_modules)

VI. Soignez votre CSS un minimum, montrez que vous savez aussi faire du beau et du joli. Impliquez-vous un minimum, faites au moins semblant 😉

# Prérequis
- Node.js ([https://nodejs.org/en/](https://nodejs.org/en/))
- NPM (inclus dans l'installation Node.js)
- Un IDE de votre choix (Je préfère VS Code personnellement)
# Installation du projet

    git clone https://github.com/elcitrovmtgrande/technical-multiselect.git test-technique
    cd test-technique
    npm install

# Lancement du projet

    npm run serve

# Ressources utiles

- https://vuejs.org/
- https://openclassrooms.com/fr/courses/5664336-create-a-web-application-with-vue-js
- https://sass-lang.com/guide