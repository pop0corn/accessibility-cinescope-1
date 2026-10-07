# Here starts the journey with Cinescope
Binome : 
- Samuel MARTINEZ
- Emilien DUCIEL

## First install your project
- you can copy the repo locally using `git clone`
- go to the root of the directory and run `npm i`
- run the project with `npm run dev`

## Constats
- Les cartes n'ont pas de focus visible, ne sont pas accessibles au clavier et n'ont pas de texte alternatif pour les images
- Les pastilles de disponibilité ne sont pas suffisamment explicites pour les personnes malvoyantes/daltoniennes
- L'action de favori n'ont pas de focus visible
- Aucun composant n'a de type de rôle ARIA, ce qui rend l'application difficilement accessible aux lecteurs d'écran
- La barre de recherche n'a pas de focus visible

## Impacts avant et après l'accessibilité

| Impact | Avant | Après |
| --- | --- | --- |
| **Navigation au clavier** | Les cartes sont des `<div>` cliquables : impossible de les atteindre avec `Tab` ni de choisir un film sans souris, et aucun focus n'est visible. | Les cartes sont des `<button>` : atteignables avec `Tab`, activables avec `Entrée` ou `Espace`, avec un contour de focus violet bien visible. |
| **Disponibilité des films** | L'information repose uniquement sur une pastille verte ou rouge : illisible pour une personne daltonienne et absente pour un lecteur d'écran. | La pastille est accompagnée du texte "Actuellement disponible" ou "Actuellement indisponible", lisible par tous. |
| **Lecteur d'écran** | Les affiches n'ont pas de texte alternatif et le bouton favori n'a pour libellé que le symbole "★" ou "☆". | Chaque affiche est décrite ("Affiche du film Orbite 9") et le bouton favori annonce son action ("Ajouter Orbite 9 aux favoris"). |

