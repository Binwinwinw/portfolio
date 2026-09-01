# Portfolio Web - Portfolio Complet

Un site portfolio moderne et responsif showcasant tous mes projets web et applications.

🔗 **Dépôt officiel** : [https://github.com/Binwinwinw/portfolio](https://github.com/Binwinwinw/portfolio)

## 🌟 Caractéristiques

- **Design Moderne & Responsif** - Fonctionne parfaitement sur tous les appareils
- **Filtrage Dynamique** - Filtrez les projets par technologie
- **Recherche en Temps Réel** - Trouvez rapidement vos projets
- **11+ Projets** - Tous les projets listés avec descriptions, technologies et démos
- **Performance Optimale** - Léger et rapide (vanilla JS)
- **Accessibilité** - WCAG compliant

## 📂 Structure

```text
portfolio/
├── index.html              # Page principale
├── projects.json           # Données des projets
├── README.md              # Ce fichier
└── assets/
    ├── css/
    │   └── style.css      # Styles (1200+ lignes, responsive)
    └── js/
        └── script.js      # Logique et interactivité
```

## 🚀 Démarrage Rapide

### Cloner le dépôt

```bash
git clone https://github.com/Binwinwinw/portfolio.git
cd portfolio
```

### Serveur Local (Node.js)

```bash
cd portfolio
npx http-server
```

### Avec Python

```bash
python -m http.server 8000
```

### Avec PHP

```bash
php -S localhost:8000
```

## 📊 Projets Inclus

| #   | Projet            | Technologie        | Catégorie | Status        |
| --- | ----------------- | ------------------ | --------- | ------------- |
| 1   | GestionEPN v2.0   | React + Node.js    | Gestion   | ✅ Production |
| 2   | MonCoachScolaire  | Node.js + PHP + ML | Éducation | ✅ Production |
| 3   | CV-Expert         | React PWA          | Outils    | ✅ Production |
| 4   | ConvertAll        | PHP                | Outils    | ✅ Production |
| 5   | BlogoDo           | Node.js + IA       | IA        | 🔨 Dev        |
| 6   | CGTM-SOEM         | PHP                | Gestion   | ✅ Production |
| 7   | Boîte à Outils    | PHP                | Outils    | ✅ Production |
| 8   | Clash of Clans    | WordPress          | Gaming    | ✅ Production |
| 9   | Liloo             | React + Vite       | Outils    | ✅ Production |
| 10  | AI Knowledge Base | Docker + Ollama    | IA        | 📦 Template   |
| 11  | GestionEPN v1.0   | React              | Gestion   | 📦 Archive    |

## 🎨 Technologies Utilisées

### Frontend

- HTML5 sémantique
- CSS3 (Flexbox, Grid, animations)
- JavaScript vanilla (ES6+)
- Responsive design mobile-first

### Stack Représenté

- React + Vite
- Node.js + Express
- PHP 8 + MySQL
- WordPress
- Docker + Ollama
- Python + ML

## 🔧 Personnalisation

### Modifier les Projets

Éditez `projects.json` et ajoutez vos projets :

```json
{
  "id": 12,
  "name": "Votre Projet",
  "shortDescription": "Description courte",
  "fullDescription": "Description longue",
  "technologies": ["React", "Node.js"],
  "mainTech": "React",
  "features": ["Feature 1", "Feature 2"],
  "demoUrl": "https://...",
  "codeUrl": "../votre-projet",
  "status": "Production",
  "category": "Votre Catégorie"
}
```

### Changer les Couleurs

Modifiez les variables CSS dans `assets/css/style.css` :

```css
:root {
  --primary-blue: #0052a3;
  --secondary-green: #10b981;
  --accent-orange: #f59e0b;
  /* ... */
}
```

### Ajouter des Sections

Modifiez `index.html` et ajoutez vos sections. Styles responsifs inclus pour tous.

## 📱 Responsive Design

- ✅ Desktop (1200px+)
- ✅ Tablet (768px - 1199px)
- ✅ Mobile (480px - 767px)
- ✅ Small Mobile (< 480px)

## ♿ Accessibilité

- Sémantique HTML5 correcte
- Contraste de couleurs suffisant
- Navigation au clavier complète
- Optimisé pour lecteurs d'écran
- Focus visible sur tous les éléments interactifs

## 🔍 SEO

- Meta tags complets
- Titres et descriptions optimisés
- Structure sémantique
- Open Graph ready

## 📄 License

Libre d'utilisation. Modifiez selon vos besoins.

## 🤝 Support

Pour toute question ou modification, consultez le code. C'est du HTML/CSS/JS pur et simple !

---

### Portfolio Complet des Créations Web
