# 📤 Instructions pour Pusher vers GitHub

## Étape 1️⃣ : Créer un repo GitHub vierge

1. Va sur **https://github.com/new**
2. Remplis :
   - **Repository name** : `ultrasharex-otp`
   - **Description** : `UltraShareX OTP Verification - Phone Number Consent Page`
   - **Public** : ✅ Coché (important !)
   - **Add README** : ❌ NON (on l'a déjà)
3. Clic **Create Repository**

## Étape 2️⃣ : Initialiser le repo local et pusher

Ouvre PowerShell dans le dossier `ultrasharex-otp` et execute :

```powershell
# Configure Git (première fois seulement)
git config --global user.name "Ton Nom"
git config --global user.email "ton@email.com"

# Initialise le repo local
git init

# Ajoute les fichiers
git add .

# Crée le premier commit
git commit -m "Initial commit: UltraShareX OTP verification page"

# Renomme la branche (si besoin)
git branch -M main

# Ajoute la remote GitHub
git remote add origin https://github.com/[TON-USERNAME]/ultrasharex-otp.git

# Pousse vers GitHub
git push -u origin main
```

**Remplace `[TON-USERNAME]` par ton username GitHub !**

## Étape 3️⃣ : Activer GitHub Pages

1. Va sur ton repo GitHub : `https://github.com/[TON-USERNAME]/ultrasharex-otp`
2. Clique **Settings** (en haut à droite)
3. Scroll gauche → **Pages**
4. Sous "Build and deployment" :
   - **Source** : Deploy from a branch
   - **Branch** : Select `main`
   - **Folder** : Select `/ (root)`
5. Clic **Save**

## Étape 4️⃣ : Attendre & Tester

Attends **1-2 minutes**, puis teste le lien :

```
https://[ton-username].github.io/ultrasharex-otp/otp-verification.html
```

✅ Si tu vois la page → C'est OK !

## 🔗 Ton URL définitive pour Azure

Une fois confirmée sur GitHub Pages :

```
https://[ton-username].github.io/ultrasharex-otp/otp-verification.html
```

👉 C'est cette URL que tu rentreras dans Azure

---

## ❓ Problèmes courants

| Erreur | Solution |
|--------|----------|
| `fatal: not a git repository` | Lance `git init` d'abord |
| `Permission denied (publickey)` | Configure SSH key GitHub ou utilise token PAT |
| 404 sur la page | Attends 2-3 min après activation Pages |
| Page blanche | Vérifier le chemin : `/otp-verification.html` |

---

💡 **Besoin d'aide ?** Mets à jour le fichier `UPDATE_TRACKER.md` dans le workspace parent une fois live !
