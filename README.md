# Mise en situation – Explorateur de pays

**Durée :** 1h30, en individuel
**Compétences :** C3. Réaliser des interfaces utilisateur · C4. Développer la partie dynamique des interfaces utilisateur
**Fourni :** la [maquette](https://www.figma.com/design/dEfkmkI7YYqka5NDYMSK3O) et ce starter
**Interdit :** documentation, anciens projets, IA, code d'un camarade

## Contexte

L'agence **Atlas Voyages** veut une page « Explorer le monde » : le visiteur choisit un continent et cherche un pays par son nom.

**API :** `https://countries.dev/countries` (tous les pays, sans clé)

Une seule requête au chargement. Le filtre par continent et la recherche se font ensuite sur les données récupérées.

## Le starter

| Fichier | Contenu |
| --- | --- |
| `index.html` | Le squelette de la page, avec des commentaires pour te guider |
| `style.css` | Les couleurs de la maquette en variables CSS |
| `script.js` | Les fonctions à écrire, avec un commentaire qui explique leur rôle |

Dans `script.js`, **ne renomme pas les fonctions** : écris seulement leur contenu.

| Palier | Fonctions à écrire |
| --- | --- |
| P2 | `fetchCountries()`, `createCountryCard()`, `displayCountries()` |
| P3 | `filterCountries()` |
| Bonus | `sortByPopulation()`, `showLoader()`, `showError()` |
| Démarrage | `init()` (déjà appelée en bas du fichier) |

## Les consignes, palier par palier

| Temps conseillé | Palier | Compétence |
| --- | --- | --- |
| 0 – 10 min | Démarrage | — |
| 10 – 30 min | P1. La maquette | C3 |
| 30 – 55 min | P2. L'affichage dynamique | C4 |
| 55 – 75 min | P3. Les interactions | C4 |
| 75 – 90 min | Bonus | C4 |

### Démarrage

1. Lis les commentaires des 3 fichiers du starter.
2. Observe la maquette : desktop, mobile et « États à prévoir ».
3. Crée ton dépôt GitHub `atlas-explorer`, ajoute le starter et pousse un premier commit.

### P1. La maquette (C3)

*En tant que visiteur, je vois une page claire, sur mobile comme sur ordinateur.*

1. Intègre la maquette : en-tête, titre, zone de filtres et grille de cartes.
2. Les filtres contiennent une liste déroulante des 5 continents et un champ de recherche, chacun avec une étiquette visible.
3. Écris 3 cartes en dur : drapeau, nom, capitale, population.
4. Rends la page responsive : 1 colonne sur mobile, 3 colonnes sur grand écran.
5. Commit.

### P2. L'affichage dynamique (C4)

*En tant que visiteur, je vois les pays d'Afrique dès l'ouverture de la page.*

1. Au chargement, récupère tous les pays avec `fetch`, une seule fois, et garde-les dans une variable.
2. Affiche les pays d'Afrique par défaut, une carte par pays.
3. Supprime les 3 cartes écrites en dur.
4. Commit.

### P3. Les interactions (C4)

*En tant que visiteur, je choisis un continent et je cherche un pays, sans recharger la page.*

1. Le changement de continent affiche les pays de ce continent. Les anciennes cartes disparaissent.
2. La recherche filtre par nom, sans tenir compte des majuscules : « mor » trouve « Morocco ».
3. Les deux filtres fonctionnent ensemble.
4. Un message s'affiche si aucun pays ne correspond.
5. Commit.

### Bonus

- Tri par population, du plus peuplé au moins peuplé.
- Indicateur « Chargement… » pendant la requête.
- Message d'erreur si l'API ne répond pas.

## Règles

- Écris le contenu des fonctions de `script.js` sans les renommer.
- CSS à la main ou avec un framework CSS. JavaScript sans librairie.
- Un commit par palier, avec un message clair.

## Rendu

Le lien de ton dépôt GitHub `atlas-explorer`, avant la fin des 1h30.

**Validation :** P1 et P2 complets, et au moins un filtre de P3 qui fonctionne.
