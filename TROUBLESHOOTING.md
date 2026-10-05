# 🔧 Troubleshooting Handoff

## 🔴 Je ne vois rien quand j'ouvre index.html

### Problème
Page blanche ou erreur

### Solutions
1. **Vérifie le chemin fichier**
   ```bash
   # Assure-toi d'être dans le bon dossier
   cd handoff
   ls index.html
   # Si pas trouvé = tu es au mauvais endroit
   ```

2. **Double-clique sur index.html**
   - Doit ouvrir dans le navigateur
   - Si ça ouvre en éditeur: Clique droit → "Open with Browser"

3. **Utilise un serveur local**
   ```bash
   # Python 3
   python -m http.server 8000
   # → Va sur http://localhost:8000
   
   # Node
   npx http-server
   # → Va sur http://localhost:8080
   ```

---

## 🔴 "fatal: not a git repository"

### Problème
Tu n'es pas dans le bon dossier ou git n'est pas initié

### Solution
```bash
# Navigue au bon dossier
cd handoff

# Vérifie qu'il existe
ls index.html

# Si tu viens de cloner, tu es déjà bon
# Sinon, initialise:
git init
git remote add origin https://github.com/TON_USERNAME/handoff.git
```

---

## 🔴 "permission denied" ou "access denied" en pushing

### Problème
GitHub te refuse l'accès

### Solutions

#### A. Clé SSH (recommandé)
```bash
# Crée une clé SSH
ssh-keygen -t ed25519 -C "ton.email@example.com"

# Ajoute à l'agent SSH
eval "$(ssh-agent -s)"
ssh-add ~/.ssh/id_ed25519

# Copie la clé publique
cat ~/.ssh/id_ed25519.pub
# → Colle sur https://github.com/settings/keys
```

#### B. GitHub Token (plus simple)
1. Va sur https://github.com/settings/tokens/new
2. Crée un token avec access "repo"
3. Copie le token
4. Quand Git te demande un password: Colle le token

---

## 🔴 Vercel dit "Build failed"

### Problème
Vercel essaye de compiler et échoue

### Solution
Assure-toi que `vercel.json` contient:
```json
{
  "name": "handoff",
  "buildCommand": "echo 'No build needed'",
  "outputDirectory": ".",
  "public": true
}
```

Ou en plus simple, crée `package.json`:
```json
{
  "name": "handoff",
  "version": "1.0.0"
}
```

---

## 🔴 "Repository not found"

### Problème
Vercel ne trouve pas ton repo GitHub

### Causes
1. **Repo est privé** → Rends-le public
2. **Pas d'accès** → Re-connecte avec GitHub
3. **Mauvais nom** → Vérifie l'URL

### Solution
```
Sur GitHub: Tu dois être owner du repo
Repo: Doit être PUBLIC
GitHub: Doit être connecté à Vercel
```

Redéploie:
1. Va sur https://vercel.com/dashboard
2. Clique "Remove Project"
3. Clique "New Project"
4. Sélectionne le bon repo
5. Clique "Deploy"

---

## 🔴 Les données disparaissent après refresh

### Pourquoi?
**C'est NORMAL en v1.0!** 

Données stockées en localStorage = **par navigateur**
- Ouvre sur Safari? Données perdues (besoin Chrome)
- Vide cache? Données perdues
- Autre PC? Données perdues

### Solution
**C'est prévu pour v2.0 avec Supabase**

Pour maintenant:
- 📥 **Export** les handoffs en PDF avant les pertes
- 📋 Prends des notes en parallèle
- ⏰ **À court terme**: Attends v2 (janvier 2025)

---

## 🔴 "Uncaught ReferenceError: X is not defined"

### Problème
Erreur JavaScript dans la console

### Solutions
1. **Ouvre DevTools** (F12)
2. **Onglet Console**
3. **Regarde le message d'erreur**
4. **Ouvre une Issue sur GitHub** avec:
   - Le message exact
   - Ton navigateur (Chrome/Firefox/Safari)
   - Tes étapes pour reproduire

---

## 🟡 Vercel donne une URL bizarre

### Exemple
```
https://handoff-git-main-myusername.vercel.app
```

### Pourquoi?
C'est normal si ton projet a un vrai nom. Change-le:

1. Va sur https://vercel.com/dashboard
2. Sélectionne ton projet
3. "Settings" → "Domains"
4. Change le nom en "handoff"
5. Attends 5 min
6. Va sur https://handoff.vercel.app

---

## 🟡 Couleurs bizarres / Design cassé

### Problème
Styles CSS ne s'appliquent pas

### Causes courantes
1. **Cache navigateur** → Ctrl+Shift+R (hard refresh)
2. **CSS vieux** → Mets à jour index.html
3. **Zoom bizarre** → Reset: Ctrl+0

### Solution
```bash
# Sur Vercel
1. Vai sur https://vercel.com/dashboard
2. Clique "Redeploy"
3. Attends 30s
4. Hard refresh: Ctrl+Shift+R
```

---

## 🟡 Mobile ne fonctionne pas bien

### Problème
Le design n'est pas responsive

### Vérification
1. Ouvre sur téléphone
2. Site → Menu → "Developer Options"
3. Désactive le zoom mobile
4. Le site doit être lisible

### Solution
Dans `index.html`, ici doit être:
```html
<meta name="viewport" content="width=device-width, initial-scale=1.0">
```

Si manquant, ajoute juste après `<title>`.

---

## 🟢 "C'est slow" / "Page met du temps à charger"

### Problème
App lente au démarrage

### Raison
- localhost sans serveur = slow
- Vercel gratuit = ressources limitées

### Solution
1. **Utilise http-server**:
   ```bash
   npx http-server
   ```

2. **Attends 10 sec** après déploiement Vercel

3. **Vide le cache**:
   - DevTools → Network → Disable cache
   - Puis refresh

---

## 📞 Problèmes non listés?

1. **Ouvre DevTools** (F12)
2. **Onglet Console**
3. **Copie l'erreur**
4. **Crée une issue GitHub**:
   - Titre: "Issue: [description courte]"
   - Body: L'erreur complète
   - Pièces jointes: Screenshots si utile

---

## 💡 Tips utiles

### Hard refresh (cache clear)
- **Windows/Linux**: Ctrl+Shift+R
- **Mac**: Cmd+Shift+R

### Tester le site offline
```bash
# Ouvre DevTools → Network → Offline
# Actualise → Ton app reste accessible
```

### Test sur vrai mobile
```bash
python -m http.server 8000
# Va sur http://IP_TON_PC:8000 depuis téléphone
```

### Backup des données
1. Mode "Consulter"
2. Ouvre chaque handoff
3. Clique "Export PDF"
4. Sauvegarde les PDFs

---

## 🆘 J'ai vraiment besoin d'aide

### Outils
1. **Google** (99% des erreurs déjà résolues)
2. **Stack Overflow**: Tag `javascript`, `vercel`
3. **GitHub Issues**: Crée une issue

### Format idéal pour une issue

```markdown
## Description du problème
[Décris ce qui se passe]

## Étapes pour reproduire
1. J'ai fait X
2. Puis Y
3. Z s'est produit

## Résultat attendu
[Qu'est-ce qui devrait se passer]

## Informations
- Navigateur: Chrome 120
- OS: Windows 11
- URL: https://handoff.vercel.app
- Erreur console: [Copie/colle le message]

## Screenshots
[Si utile, ajoute des images]
```

---

## ✅ Tout fonctionne! Et après?

Félicitations! 🎉

Prochaines étapes:
1. **Customise** les couleurs/textes
2. **Partage** avec ton équipe
3. **Récupère du feedback**
4. **Suggère** des features via Issues
5. **Contribue** à l'open-source si tu veux!

---

**Besoin de plus d'aide? Crée une Discussion sur GitHub!**
