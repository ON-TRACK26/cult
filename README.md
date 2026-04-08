# Carrefour Cult' — Hub Éditorial SEO & GEO

Landing pages et articles SEO/LLM-compliant pour **Carrefour Cult'**, l'espace culture de Carrefour couvrant jeux vidéo, livres, musique, films & séries.

## Structure du projet

```
cult/
├── index.html                              # Hub principal (LP unique multi-sections)
├── articles/
│   ├── article-tomb-raider.html            # Article : Test Tomb Raider Remastered PS5/Switch
│   └── article-musso.html                  # Article : Interview Guillaume Musso — Le Crime du paradis
├── assets/
│   ├── images/
│   │   ├── hero-tomb-raider.png            # Hero Lara Croft (784KB, export Figma)
│   │   ├── mario-luigi.png                 # Mario & Luigi L'Épopée Fraternelle
│   │   ├── bad-boys.png                    # Bad Boys Ride or Die
│   │   ├── nba2k25.png                     # NBA 2K25
│   │   ├── harry-potter.png                # Harry Potter (Gallimard)
│   │   └── moi-moche-mechant.png           # Moi, moche et méchant 4
│   └── logos/
│       ├── logo-cult.png                   # Logo Cult' (dark text, apostrophe bleue)
│       └── logo-cult.svg                   # Logo Cult' vectoriel
└── README.md
```

## Architecture du hub (index.html)

Le hub est une single-page regroupant toutes les sections :

1. **Header** : logo Cult' + navigation sticky + dark mode toggle + hamburger mobile
2. **Hero** : mise en avant Tomb Raider (lien vers article)
3. **Social proof** : métriques communauté
4. **Onglets catégories** : À la une, Actualités, Livres, Jeux vidéos, Films & Séries, Musique, Cadeaux, Événements — cliquables avec ancres internes
5. **Section Livres** (`#section-livres-hub`) : Hero banner Musso, interviews, chroniques, BD/Mangas, meilleures ventes, newsletter
6. **Section Musique** (`#section-musique`) : Sélection musicale
7. **Section Films & Séries** (`#section-films-hub`) : Critiques, tops, sidebar
8. **Section Cadeaux** (`#section-cadeaux`) : Idées cadeaux culture
9. **FAQ** : 14 questions/réponses avec Schema.org FAQPage
10. **Footer** : liens et mentions

## Consignes éditoriales (SEO & LLM compliance)

Chaque page et article respecte les règles suivantes :

1. **H1 unique** par page, optimisé mot-clé principal
2. **H2 structurés** avec mots-clés secondaires et longue traîne
3. **Meta description** < 160 caractères, incitative avec mot-clé
4. **Sommaire** avec ancres internes sur les articles (navigation in-page)
5. **FAQ** de 5 Q/A minimum par article, balisée Schema.org `FAQPage`
6. **Schema.org** : `WebPage`, `Article`, `Product`, `BreadcrumbList` selon le contexte
7. **Breadcrumb** avec fil d'Ariane cliquable (retour hub)
8. **Contenu 1500+ mots** pour les articles longs
9. **Maillage interne** : tous les liens de navigation pointent vers `index.html` + ancres sections
10. **Accessibilité WCAG** : skip-link, aria-labels, focus-visible, sémantique HTML5

## Design system

```
Couleurs :
  --blue:       #0058a3   (Carrefour bleu)
  --blue-dark:  #004080
  --purple:     #5b4dff   (accent)
  --hero-bg:    #f0f4ff   (fond hero light)

Logo :
  "Cult" → #121212
  "'"    → #1E5BC6

Typographie :
  Titres : Playfair Display (italic, 700-800)
  Corps  : Inter (400-800)

Thèmes :
  Light (défaut) + Dark mode (toggle)
```

## Conventions techniques

- HTML autoportant : CSS inline + JS inline (pas de fichiers externes sauf Google Fonts)
- Mobile-first responsive : breakpoints 1024px, 768px, 480px
- Animations : IntersectionObserver scroll reveal (fallback mobile `opacity: 1 !important`)
- Smooth scroll : `html { scroll-behavior: smooth; }`
- Menu mobile : hamburger avec body scroll lock

## Convention de nommage

- Articles : `articles/article-[slug].html`
- Images produit/hero : `assets/images/[nom-descriptif].png`
- Logos : `assets/logos/logo-cult.[png|svg]`

## Images manquantes (placeholders Unsplash)

~25 images Unsplash restent à remplacer dans le hub, réparties sur :
- Livres : interviews, chroniques, BD/Mangas, meilleures ventes
- Musique : artistes et albums
- Films : posters et scènes
- Cadeaux : produits culture

## Données contextuelles

- Client : Carrefour
- Marque éditoriale : Cult'
- Créateur : OnTrack (agence SEO & GEO)
- Date de création : Mars 2026
- Langue : Français (fr_FR)
