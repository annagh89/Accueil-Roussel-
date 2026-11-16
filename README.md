1. Problème constaté (Ma demande)
   Lorsque je navigue dans l'en-tête (header) du site avec la touche Tab du clavier, l'ordre du focus n'est pas logique. Après le logo « Fleurs Roussel », le focus passe directement sur le bouton « Commander » à droite, avant de revenir sur les liens du menu de navigation (« Bouquets », « Ateliers », « Livraison », « Contact »).

2. Explication du problème (Analyse)
   Ce problème vient de l'ordre des éléments dans le code HTML. Dans le code, le bouton « Commander » était écrit avant la balise <nav>, et il était déplacé à droite uniquement grâce à la classe CSS md:order-3. Cependant, le navigateur suit toujours l'ordre du code HTML pour la navigation au clavier, et non l'ordre visuel créé par le CSS.

3. Solution proposée et appliquée
   Pour corriger l'ordre du focus sans changer l'apparence visuelle sur mobile et sur ordinateur :

J'ai déplacé la balise <nav> avant le bouton « Commander » dans le code HTML.

J'ai utilisé les classes Tailwind order-3 md:order-2 sur <nav> et order-2 md:order-3 sur le bouton « Commander » pour garder la bonne mise en page sur tous les écrans.

Désormais, la navigation au clavier suit l'ordre logique : Logo → Bouquets → Ateliers → Livraison → Contact → Commander.



Problème constaté (Mobile)
Sur la version mobile (390 px), l'ordre visuel des éléments dans l'en-tête est différent de la version ordinateur : le bouton « Commander » est en haut à droite (sur la même ligne que le logo) et le menu de navigation est en dessous. Avec un seul bloc HTML, le focus du clavier (Tab) descendait d'abord sur le menu avant de remonter sur le bouton « Commander », ce qui n'était pas naturel pour l'utilisateur.

Solution appliquée
Comme le navigateur suit toujours l'ordre du code HTML pour la tabulation (Tab), j'ai séparé la structure de l'en-tête en deux versions adaptées à chaque taille d'écran :

Pour mobile (md:hidden) : L'ordre HTML suit la mise en page mobile : Logo → Commander → Menu de navigation.

Pour ordinateur (hidden md:grid) : L'ordre HTML suit la mise en page desktop : Logo → Menu de navigation → Commander.

De cette façon, l'ordre du focus au clavier correspond exactement à l'ordre visuel sur tous les écrans, sans aucun saut.