# Taawon

Taawon est un répertoire en ligne des coopératives artisanales marocaines. Le site permet de découvrir les maîtres artisans, leurs savoir-faire et leurs produits, et de les contacter directement, sans intermédiaire.

## Squad

| Nom | Rôle |
|-----|------|
| Ismail El Harouachi | Scrum Master |
| Ayoub Azdad | Développeur |
| Aissa Saidi | Développeur |

## Lien

- **Site** : https://ismailtlg.github.io/site-Tawoon/

## Pages

| Page | Description |
|------|-------------|
| `index.html` | Accueil |
| `cooperatives.html` | Répertoire des coopératives |
| `cooperative.html` | Fiche d'une coopérative : produits, répartition du prix, régions |
| `a-propos.html` | Mission, chiffres clés, piliers, charte éthique, témoignages |
| `partenaire.html` | Formulaire de candidature pour rejoindre le répertoire |
| `erreur.html` | Page d'erreur 404 |

## Installation

```bash
git clone https://github.com/ismailtlg/site-Tawoon.git
cd site-Tawoon
```

Ouvrir ensuite `index.html` dans un navigateur, ou utiliser l'extension VS Code **Live Server**.

### Commande de build

Aucune. Le projet est un site statique et Tailwind est chargé via CDN : il n'y a ni dépendance à installer, ni étape de compilation.

## Tailwind CSS

Version **4** (via `@tailwindcss/browser@4`, chargé par CDN) :

```html
<script src="https://cdn.jsdelivr.net/npm/@tailwindcss/browser@4"></script>
```

## Design tokens

### Couleurs

| Usage | Valeur |
|-------|--------|
| Primaire (boutons, lien actif) | `#556B2F` |
| Fond du pied de page | `#442A22` |
| Texte du pied de page | `#FFDDB2` |
| Titres | `#5F4828` |
| Texte courant | `#45483C` |
| Texte foncé | `#2C160E` |
| Titres de carte | `#442A22` |
| Fond de section | `#FFF1ED` |

### Autres

- **Arrondis** : `rounded-sm`, `rounded`, `rounded-xl`
- **Ombres** : `shadow-md`, `shadow-xl`
- **Survol** : opacité à 75 % avec transition de 200 ms
- **Mise en page** : flexbox et grille (`grid-cols-1` sur mobile, `md:grid-cols-3` à partir de la taille tablette)

## Accessibilité

- Structure sémantique : `header`, `nav`, `main`, `section`, `article`, `footer`
- Attribut `alt` renseigné sur toutes les images et icônes
- Champs de formulaire associés à un `label` (`for` / `id`)
- Types de champs adaptés (`email`, `tel`, `number`) et validation native (`required`, `minlength`, `pattern`)
- Liens externes ouverts dans un nouvel onglet
- Page 404 avec lien de retour vers l'accueil
- Balises `meta description` et `title` propres à chaque page

## Éco-conception

- Site statique sans framework JavaScript ni serveur
- Aucun script applicatif : uniquement du HTML et du CSS
- Pas de bibliothèque d'icônes externe : icônes locales en PNG
- Une seule dépendance externe (Tailwind via CDN)
- Pages légères, sans vidéo ni animation lourde

## Structure du projet

```
├── index.html
├── cooperatives.html
├── cooperative.html
├── a-propos.html
├── partenaire.html
├── erreur.html
├── css/
│   └── style.css
└── assets/
    ├── images/
    └── icons/
```

© 2024 Taawon. Répertoire de sauvegarde des coopératives artisanales marocaines.
