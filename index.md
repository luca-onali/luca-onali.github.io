<head>
<script type="module" src="https://cdn.jsdelivr.net/npm/mermaid/dist/mermaid.esm.min.mjs"></script>
<script>
    mermaid.initialize({ startOnLoad: true });
</script>
</head>
---
layout: default
title: "Accueil - Mon Portfolio"
---

# Bienvenue sur mon Portfolio

Bienvenue dans mon portfolio ! Retrouvez ici mes projets, mon parcours et mes informations de contact.

---

## Navigation
- [À propos](about.md)
- [Contact](contact.md)

---

## Diagramme de classe

```mermaid
classDiagram
    class Portfolio {
        +String titre
        +String description
        +String theme
    }

    class Page {
        +String nom
        +String contenu
    }

    class Projet {
        +String nom
        +String description
        +String url
    }

    class CV {
        +String fichier
    }

    Portfolio "1" --> "*" Page : contient
    Portfolio "1" --> "*" Projet : contient
    Portfolio "1" --> "1" CV : contient
