# 🚀 Guide de déploiement Handoff (GitHub + Vercel)

## Étape 1: Créer le repo GitHub (2 minutes)

### 1.1 Sur GitHub.com
```bash
1. Accéder à github.com → Cliquer sur "+"
2. "New repository"
3. Nom: "handoff"
4. Description: "Transition de service fluide pour petites structures"
5. Public (important pour Vercel gratuit)
6. Cocher "Add a README file"
7. Créer le repo
```

### 1.2 Sur ton ordinateur
```bash
# Clone le repo
git clone https://github.com/TON_USERNAME/handoff.git
cd handoff

# Copier l'index.html que tu as créé dans ce dossier
```

## Étape 2: Structurer le projet

```bash
handoff/
├── index.html              # Le fichier qu'on a créé
├── README.md               # Explique le projet
├── .gitignore              # Fichiers à ignorer
├── vercel.json             # Config Vercel
└── public/
    └── (images, icons, etc si besoin)
```

## Étape 3: Créer les fichiers de config

### 3.1 README.md
```markdown
# Handoff 📋

**Transition de service fluide et complète pour petites structures.**

## Cas d'usage
- 🏪 Magasins
- 🍔 Restaurants  
- 🚗 Garages
- 🏠 Agences immobilières
- 🧹 Entreprises de nettoyage
- 🏨 Hôtels
- 📦 Entrepôts
- 🔧 Artisans

## Fonctionnalités

✅ Tâches effectuées  
✅ Problèmes rencontrés  
✅ Clients à rappeler  
✅ Commandes en attente  
✅ Stock à surveiller  
✅ Caisse / Paiements  
✅ Matériel défectueux  
✅ Priorités pour demain  

## Démarrage rapide

```bash
# 1. Clone
git clone https://github.com/TON_USERNAME/handoff.git
cd handoff

# 2. Ouvre simplement index.html dans ton navigateur
# (ou utilise "Open with Live Server" dans VS Code)
```

## Déployer sur Vercel

1. Va sur https://vercel.com
2. Connecte-toi avec GitHub
3. "Import Project"
4. Sélectionne "handoff"
5. Clique sur "Deploy"
6. C'est tout! 🚀

## Points de sauvegarde

- Les données sont sauvegardées dans **localStorage** du navigateur
- Pour un backup: Mode "Consulter" → Export PDF
- Pour plus tard: Version Firebase/Supabase en cours

## Stack

- HTML5
- CSS3 (responsive)
- Vanilla JavaScript
- localStorage

## Feuille de route

- [ ] Firebase/Supabase pour cloud sync
- [ ] App mobile (React Native)
- [ ] Notifications
- [ ] Statistiques
- [ ] API OpenAI pour suggestions
- [ ] Multilingue

## Licence

MIT - Utilise-le librement!

## Contribuer

Les PRs sont bienvenues! Forke, modifie, et propose tes améliorations.
```

### 3.2 vercel.json
```json
{
  "name": "handoff",
  "buildCommand": "echo 'No build needed'",
  "outputDirectory": ".",
  "public": true
}
```

### 3.3 .gitignore
```
node_modules/
.DS_Store
*.log
.env
.env.local
.vercel
dist/
```

## Étape 4: Push sur GitHub

```bash
git add .
git commit -m "Initial commit: Handoff app"
git push origin main
```

## Étape 5: Déployer sur Vercel

### Option A: CLI (Recommandé)
```bash
# Install Vercel CLI
npm install -g vercel

# Deploy
vercel
# → Suis les instructions
# → Sélectionne le dossier racine
# → Valide la config
```

### Option B: Interface web
```
1. Va sur https://vercel.com/new
2. Connecte GitHub
3. Importe "handoff"
4. Clique "Deploy"
```

## Étape 6: Ton app est live! 🎉

Vercel te donne une URL comme:
```
https://handoff.vercel.app
```

## Mettre à jour l'app

Chaque fois que tu modifies index.html:

```bash
git add index.html
git commit -m "Description de la modif"
git push origin main
```

✅ Vercel redéploie automatiquement en 30 secondes!

---

## Prochaines étapes (futures versions)

### Version 2: Backend avec Supabase

```
handoff/
├── index.html
├── api/
│   ├── saveHandoff.js      # POST /api/saveHandoff
│   ├── getHandoffs.js      # GET /api/getHandoffs
│   └── deleteHandoff.js    # DELETE /api/deleteHandoff
└── supabase/
    └── migrations/
        └── 001_create_table.sql
```

### Version 3: App React

```
handoff/
├── frontend/               # React app
├── backend/                # Node/Express
├── database/               # Supabase config
└── docker-compose.yml
```

Mais pour l'instant, cette version vanille suffisante et 100% gratuite! 🚀
