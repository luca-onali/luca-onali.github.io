---
# Feel free to add content and custom Front Matter to this file.
# To modify the layout, see https://jekyllrb.com/docs/themes/#overriding-theme-defaults

layout: home
---
Diagramme de classe
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

Diagramme de séquence
sequenceDiagram
    participant Utilisateur
    participant ServeurGitHub
    participant ServeurWebJekyll
    
    Utilisateur->>ServeurWebJekyll: Demande page
    ServeurWebJekyll->>ServeurGitHub: Récupère projets
    ServeurGitHub->>ServeurWebJekyll: Envoie projets
    ServeurWebJekyll->>Utilisateur: Affiche projets

