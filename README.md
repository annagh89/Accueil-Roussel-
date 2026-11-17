Markdown
# Fleurs Roussel — Artisan Fleuriste à Blois

Intégration de la page d'accueil du site **Fleurs Roussel** réalisée avec **HTML5** sémantique et **Tailwind CSS v4** (approche *mobile-first*).



## Installation et initialisation du projet

Pour installer les dépendances d'un projet déjà existant :

```bash
npm install
Étapes d'initialisation réalisées depuis zéro
Initialisation d'un nouveau projet Node.js :

Bash
npm init -y
Installation de Tailwind CSS et de son outil en ligne de commande (CLI) :

Bash
npm install tailwindcss @tailwindcss/cli
Lancement manuel du compilateur Tailwind en mode surveillance (--watch) :

Bash
npx @tailwindcss/cli -i ./src/input.css -o ./dist/output.css --watch
Configuration de package.json et compilation
Les scripts suivants ont été ajoutés dans la section "scripts" du fichier package.json :

JSON
"scripts": {
  "dev": "tailwindcss -i ./src/input.css -o ./dist/output.css --watch",
  "build": "tailwindcss -i ./src/input.css -o ./dist/output.css --minify"
}
Mode développement (surveille les modifications et met à jour ./dist/output.css automatiquement) :

Bash
npm run dev
Mode production (génère et minifie le fichier final ./dist/output.css) :

Bash
npm run build
Structure du projet
Plaintext
accueil-roussel/
├── dist/
│   └── output.css       # Fichier CSS généré par Tailwind CSS
├── images/              # Logo, illustrations et icônes SVG
├── src/
│   └── input.css        # Fichier source Tailwind (@import "tailwindcss" et @theme)
├── index.html           # Structure HTML sémantique de la page d'accueil
├── package.json         # Configuration npm et scripts de compilation
└── README.md            # Documentation du projet
Choix techniques et intégration
Thème personnalisé (@theme) : déclaration centralisée des couleurs (framboise, bordeaux, sauge, creme, petale, encre, blanc) et des polices (Playfair Display et Inter) dans src/input.css.

Responsive Design : intégration mobile-first (390 px) adaptée jusqu'aux grands écrans (1440 px) sans défilement horizontal (points de rupture sm:, md:, lg:).

Accessibilité : balises HTML5 sémantiques, textes alternatifs adaptés sur les images, contrastes conformes et états :hover et :focus-visible sur les liens et boutons.