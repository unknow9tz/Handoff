# ⚡ QUICK START - Handoff en 10 minutes

## ✅ Checklist rapide

```
[ ] 5 min - Créer repo GitHub
[ ] 3 min - Push les fichiers
[ ] 2 min - Déployer sur Vercel
[ ] = LIVE! 🎉
```

---

## 🔴 ÉTAPE 1: Créer le repo GitHub (5 min)

### 1️⃣ Sur github.com

1. Ouvre **github.com** (crée compte si pas déjà)
2. Clique **"+"** (haut droit) → **"New repository"**
3. Remplis:
   - **Repository name**: `handoff`
   - **Description**: `Transition de service simplifiée`
   - **Public** (cocher)
4. Cocher: **"Add a README file"**
5. Clique **"Create repository"** ✅

### 2️⃣ Sur ton ordinateur

Ouvre **Terminal** (Mac/Linux) ou **PowerShell** (Windows):

```bash
# Navigue où tu veux
cd Desktop

# Clone le repo
git clone https://github.com/TON_USERNAME/handoff.git

# Entre dedans
cd handoff

# Vérifie que tu vois index.html
ls
```

---

## 🟡 ÉTAPE 2: Ajouter les fichiers (1 min)

Tu as reçu ces fichiers:
- `index.html` ← Copie-le dans le dossier `handoff`
- `README.md` ← Remplace celui créé auto
- `vercel.json` ← Ajoute aussi
- `.gitignore` ← Ajoute aussi

Tes fichiers doivent ressembler à ça:

```
handoff/
├── index.html
├── README.md
├── vercel.json
└── .gitignore
```

---

## 🟢 ÉTAPE 3: Push sur GitHub (2 min)

Dans le même Terminal:

```bash
# Ajoute les fichiers
git add .

# Commit (sauvegarde)
git commit -m "Initial commit: Handoff app"

# Push (envoie sur GitHub)
git push origin main
```

✅ **Ferme la tab GitHub et recharge** → Tu vois tes fichiers!

---

## 🔵 ÉTAPE 4: Déployer sur Vercel (2 min)

### Option A: Super rapide (recommandé)

1. Va sur https://vercel.com
2. Clique **"Sign Up"** (avec ton compte GitHub)
3. Sélectionne le repo `handoff`
4. Clique **"Deploy"**
5. **Attends 30 secondes** ⏳

✅ C'est live! Tu as une URL comme:
```
https://handoff.vercel.app
```

### Option B: Via CLI

```bash
# Install Vercel CLI
npm install -g vercel

# Deploy
vercel

# Suis les questions (appuie Enter pour default)
```

---

## 🎉 TU AS FINI!

Ton app est maintenant:
- ✅ Accessible en ligne: `https://handoff.vercel.app`
- ✅ Sur GitHub: `github.com/TON_USERNAME/handoff`
- ✅ Gratuitement hébergée
- ✅ Avec déploiement auto (les modif se publient seules)

---

## 🔧 Customiser ton app

### Changer la couleur de base

Dans `index.html`, cherche:
```css
background: linear-gradient(135deg, #667eea 0%, #764ba2 100%);
```

Change les couleurs hex:
```css
/* Exemple: Bleu + Rose */
background: linear-gradient(135deg, #0088ff 0%, #ff0088 100%);

/* Exemple: Vert + Orange */
background: linear-gradient(135deg, #00ff88 0%, #ff8800 100%);
```

### Ajouter une section

Cherche la section "Priorités" et duplique-la avec un nouveau thème.

### Changer le titre/description

```html
<h1>📋 Handoff</h1>
<p>Transition de service fluide et complète</p>
```

---

## 📤 Mettre à jour l'app

Chaque fois que tu modifies `index.html`:

```bash
git add .
git commit -m "Description de ta modif"
git push origin main
```

**Vercel redéploie automatiquement en 30 secondes!**

---

## 🐛 Troubleshooting

### "GitHub repo pas trouvé"
→ Verify: le repo existe et est PUBLIC

### "Vercel dit error"
→ Vérifie que `index.html` est bien racine du dossier

### "Les données disparaissent au reload"
→ C'est normal! localStorage = données locales à chaque PC
→ v2.0 aura un vrai backend

### "Je veux personnaliser plus"
→ Voir le guide complet `DEPLOYMENT_GUIDE.md`

---

## 🚀 Prochaines étapes (futurs)

1. **v1.5**: Ajouter export JSON
2. **v2.0**: Backend avec Supabase (données persistantes)
3. **v3.0**: App mobile React Native

---

## 💡 Tips

- 📱 Ouvre ton app sur téléphone → Design responsive!
- 🖨️ Imprime depuis "Export PDF" → Handoff sur papier aussi
- 📸 Ajoute des emojis perso dans les sections
- 🎨 Change les couleurs pour la marque de ton entreprise

---

**C'est vraiment tout! Tu as une app pro et gratuite.** ✨

Des questions? Crée une issue sur GitHub!
