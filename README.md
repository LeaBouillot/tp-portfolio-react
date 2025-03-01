# TP: Intégration React  

Objectif : Le but de ce TP est d’intégrer le template HTML vers React, en adoptant une approche par composant.

## Etapes de réalisation du projet

- :white_check_mark:Initialisation d'un nouveau projet React Vite, installation des packages, création d'un nouveau Repository GitHub.  
- :white_check_mark:Insertion des données HTML, CSS et JS dans le projet React, gestion des erreurs et affichage de la page.  
- :white_check_mark:Création des premiers composants "Footer.jsx", "Hero.jsx", "Navbar.jsx".
- :white_check_mark:Installation du React Router Dom, car je ne souhaite pas réaliser le portfolio en 'single page'. Je crée donc différentes vues pour chaque page : Home, About, Resume, Services, Portfolio et Contact.
- :white_check_mark:Affichage dynamique de la barre de navigation et utilisation de props pour marquer la page active.
- :white_check_mark:Ajout de Bootstrap dans ce projet REACT [documentation de l'installation](https://react-bootstrap.github.io/docs/getting-started/introduction), 
- :white_check_mark:pour afficher correctement les barres de progression des skills et le carousel de témoignage [carousel de bootstrp](https://react-bootstrap.github.io/docs/components/carousel/).
- :white_check_mark:Gestion de l'envoi d'email via le formulaire de contact.
- :white_check_mark:Pusher le projet sur GitHub
- Mise en production du projet sur Vercel
- Envoi des liens au formateur.

## Utilisation bootstrap sur un Projet REACT  

1. Installation de bootstrap avec la commande: $pnpm install react-bootstrap bootstrap  
2. Ajout du CDN et Script Bootstrap  

```index.html
  <link
  rel="stylesheet"
  href="https://cdn.jsdelivr.net/npm/bootstrap@5.3.2/dist/css/bootstrap.min.css"
  integrity="sha384-T3c6CoIi6uLrA9TneNEoa7RxnatzjcDSCmG1MXxSR1GAsXEV/Dwwykc2MPK8M2HN"
  crossorigin="anonymous"
/>


<!-- Script Bootstrap -->
  <script src="https://cdn.jsdelivr.net/npm/react/umd/react.production.min.js" crossorigin></script>

  <script
    src="https://cdn.jsdelivr.net/npm/react-dom/umd/react-dom.production.min.js"
    crossorigin></script>
  
  <script
    src="https://cdn.jsdelivr.net/npm/react-bootstrap@next/dist/react-bootstrap.min.js"
    crossorigin></script>
  
  <script>var Alert = ReactBootstrap.Alert;</script>
<!-- Fin du script Bootstrap -->
```

3. Ajout des barres de progression de bootstrap

```About.jsx
import ProgressBar from 'react-bootstrap/ProgressBar';

export default function About() {
    return (
        <div className="progress">
            <span className="skill">Photoshop <i className="val">55%</i></span>
            <ProgressBar now={55} />
        </div>
    )
}
```

Documentation : [voire source](https://react-bootstrap.github.io/docs/components/progress/#example)
