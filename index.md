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
```
## Diagramme de séquence

```mermaid
sequenceDiagram
    participant Utilisateur
    participant ServeurGitHub
    participant ServeurWebJekyll
    
    Utilisateur->>ServeurWebJekyll: Demande page
    ServeurWebJekyll->>ServeurGitHub: Récupère projets
    ServeurGitHub->>ServeurWebJekyll: Envoie projets
    ServeurWebJekyll->>Utilisateur: Affiche projets
```
