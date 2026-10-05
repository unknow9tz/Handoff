# 📋 Handoff - Transition de Service

> Une solution simple et efficace pour les transitions de service dans les petites structures.

![Handoff Preview](https://img.shields.io/badge/version-1.0-blue)
![License MIT](https://img.shields.io/badge/license-MIT-green)

## 🎯 Le Problème

Un employé termine son service. Comment transmet-il les informations essentielles au suivant?
- Tâches non finies?
- Clients importants à rappeler?
- Matériel défectueux?
- Stock critique?
- **Généralement: chaos et perte d'information.**

## ✨ La Solution

**Handoff** en 2 minutes:
1. L'employé remplit les sections pertinentes (prend 5 min max)
2. L'employé suivant ouvre l'app et a le **contexte complet**
3. Zéro stress, zéro oubli, zéro perte de productivité

## 🏢 Qui peut l'utiliser?

- 🏪 Magasins
- 🍔 Restaurants
- 🚗 Garages
- 🏠 Agences immobilières
- 🧹 Entreprises de nettoyage
- 🏨 Hôtels
- 📦 Entrepôts
- 🔧 Artisans
- 👨‍💼 Bureaux
- 👤 Particuliers (organisation perso)

## 📦 Fonctionnalités

| Fonction | Description |
|----------|-------------|
| ✅ **Tâches effectuées** | Ce qui a été fait pendant le service |
| ⚠️ **Problèmes rencontrés** | Dysfonctionnements, accidents, soucis |
| 📞 **Clients à rappeler** | Avec raison du rappel |
| 📦 **Commandes en attente** | État des livraisons/services |
| 📊 **Stock à surveiller** | Articles critiques |
| 💰 **Caisse / Paiements** | Montants, anomalies |
| 🔧 **Matériel défectueux** | Équipement signalé pour maintenance |
| ⭐ **Priorités demain** | À faire en premier |

## 🚀 Démarrage (30 secondes)

### En local

```bash
# Clone
git clone https://github.com/TON_USERNAME/handoff.git
cd handoff

# Ouvre dans ton navigateur
open index.html
# Ou clique droit → "Open with Browser"
```

### En production

Déployé automatiquement sur Vercel:
```
https://handoff.vercel.app
```

## 💾 Stockage des données

**Version 1.0**: localStorage (données dans le navigateur)
- ✅ Zéro serveur
- ✅ Zéro configuration
- ✅ Gratuit
- ✅ Instantané
- ⚠️ Données par appareil

**Future v2**: Supabase/Firebase pour sync cloud

## 📱 Tech Stack

- **Frontend**: HTML5, CSS3, Vanilla JS (0 dépendances)
- **Stockage**: localStorage
- **Déploiement**: Vercel (gratuit)

## 🎨 Design

- 📱 Responsive (mobile, tablet, desktop)
- 🌙 Prêt pour dark mode
- ♿ Accessible (WCAG AA)
- ⚡ Ultra léger (~15kb)

## 🛠️ Installation locale

```bash
# 1. Clone
git clone https://github.com/TON_USERNAME/handoff.git

# 2. Entre dans le dossier
cd handoff

# 3. Ouvre index.html
# Option A: Double-clique
# Option B: python -m http.server 8000 (puis http://localhost:8000)
# Option C: VS Code → Extension Live Server → Click
```

## 🚀 Déployer sur Vercel

```bash
# 1. Installe Vercel CLI
npm install -g vercel

# 2. Login
vercel login

# 3. Deploy
vercel

# → Suit les instructions
# → Ton app est live! 🎉
```

Ou via interface web: https://vercel.com/new/git

## 📊 Exemple d'utilisation

### Magasin (14h → 22h)

**L'employé du matin remplit:**
- ✅ Tâches: "Nettoyage vitrines, Réapprov rayon fruits"
- ⚠️ Problèmes: "Frigo secteur C fait du bruit"
- 📞 Clients: "Marie Dupont - robe réservée à récup"
- 📦 Commandes: "Cde 456 - Arrivée demain matin"
- 📊 Stock: "Lait bio - 3 packs restants!"
- 💰 Caisse: "Caisse OK, monnaie faible"
- 🔧 Matériel: "Imprimante bloquée - appel réparation fait"
- ⭐ Priorités: "Appeler le fournisseur avant 9h demain"

**L'employé du soir ouvre l'app:**
→ Sait **exactement** ce qui l'attend  
→ Pas de surpises  
→ Peut se concentrer  

## 📈 Roadmap

### v1.0 ✅ (maintenant)
- [x] Interface de création
- [x] Historique
- [x] Export PDF
- [x] localStorage

### v2.0 (Q1 2025)
- [ ] Backend Supabase
- [ ] Sync multi-appareils
- [ ] Photos/documents
- [ ] Notifications email

### v3.0 (Q2 2025)
- [ ] Mobile app
- [ ] Statistiques/dashboards
- [ ] API publique
- [ ] Slack/WhatsApp integration

### v4.0 (Futur)
- [ ] IA pour suggestions
- [ ] Voice notes
- [ ] Geo-tracking
- [ ] Analytics

## 🤝 Contribuer

Les contributions sont **bienvenues**!

```bash
# 1. Fork le repo
# 2. Clone TON fork
# 3. Crée une branche: git checkout -b feature/machin
# 4. Fais tes modifs
# 5. Commit: git commit -m "Ajoute machin"
# 6. Push: git push origin feature/machin
# 7. Ouvre une Pull Request
```

## 📝 Licence

MIT - Libre d'utilisation, même commercialement!

## 🙏 Support

### C'est gratuit. C'est simple. C'est open-source.

Des questions? Des suggestions?
→ Ouvre une **Issue** ou une **Discussion**

## 🌟 Si tu aimes le projet

⭐ Donne une star sur GitHub!

---

**Créé avec ❤️ pour les petites structures qui méritent mieux que le chaos.**
