# abir-ia.github.io

Site personnel d'Abir Ismaili Alaoui, publié avec GitHub Pages : <https://abir-ia.github.io>

## Comment modifier le site

Tout se fait depuis github.com : ouvrir le fichier, cliquer sur le crayon, modifier, puis « Commit changes ».
Le site se met à jour tout seul en une à deux minutes.

| Je veux changer…                                   | Fichier à modifier            |
|----------------------------------------------------|-------------------------------|
| Mon nom, mon titre, mon labo, mon e-mail, mes liens | `_config.yml`                 |
| Ajouter une publication                            | `_data/publications.yml`      |
| Ajouter un cours ou une année d'enseignement       | `_data/teaching.yml`          |
| Le menu                                            | `_data/navigation.yml`        |
| Le texte de la page d'accueil                      | `index.html`                  |
| Projets, encadrement, exposés, services            | `projects.html`, `supervision.html`, `talks.html`, `services.html` |
| Le CV                                              | remplacer `CV/AbirAlaoui-cv.pdf` (garder le même nom) |
| La photo                                           | remplacer `images/abir-ismaili-alaoui.jpg` (image carrée) |
| Les couleurs et les polices                        | le bloc `:root` en haut de `styles.css` |

Le nom, le titre, le menu et le pied de page ne sont écrits qu'une seule fois (dans `_config.yml`
et `_layouts/default.html`) : ils sont identiques sur toutes les pages. La date « Last updated »
se met à jour automatiquement à chaque modification.

### Ajouter une publication

Dans `_data/publications.yml`, copier un bloc existant, le coller en haut de la liste et le modifier :

```yaml
- type: "conference"          # journal, conference ou thesis
  authors: "Abir Ismaili Alaoui, Prénom Nom"
  title: "Titre de l'article"
  venue: "Nom de la conférence ou de la revue"
  year: "2026"
  link: "https://adresse-du-pdf"
```

Garder les guillemets autour de chaque valeur et les espaces en début de ligne.
Les trois publications les plus récentes (hors thèse et articles « Submitted ») s'affichent
automatiquement sur la page d'accueil.

### En cas d'erreur

Si une modification contient une erreur de syntaxe, GitHub envoie un e-mail « build failed » et le
site reste simplement sur sa version précédente : rien n'est cassé. Il suffit de corriger le fichier.

## Technique

- Site statique généré par Jekyll (intégré à GitHub Pages), sans dépendance externe.
- Polices IBM Plex Sans et IBM Plex Serif (licence SIL Open Font License), hébergées dans `assets/fonts`.
