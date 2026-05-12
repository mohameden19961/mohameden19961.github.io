````markdown
# 🚀 Guide de Déploiement GitHub Pages

> Guide complet pour déployer vos projets web sur `mohameden19961.github.io`

---

## 📁 Projets disponibles

| Projet | Technologie | Lien |
|--------|-------------|------|
| my-portfolio | React + Vite | [Voir](https://mohameden19961.github.io/abdy) |
| mondesign | HTML/CSS/JS | [Voir](https://mohameden19961.github.io/mondesign) |

---

## 🌐 HTML / CSS / JavaScript

> Le plus simple — pas besoin de build !

```bash
mkdir mon-projet
cd mon-projet
touch index.html style.css script.js
git init
git remote add origin https://github.com/mohameden19961/mon-projet.git
git add .
git commit -m "first commit"
git push -u origin main
```

Ensuite aller dans **Settings → Pages → Branch: main → Save**

✅ Disponible sur : `https://mohameden19961.github.io/mon-projet`

---

## ⚛️ React + Vite

```bash
npm create vite@latest mon-projet -- --template react
cd mon-projet
npm install
npm install gh-pages --save-dev
```

**`vite.config.js` :**
```js
export default {
  base: '/mon-projet/',
  plugins: [react()]
}
```

**`package.json` :**
```json
"homepage": "https://mohameden19961.github.io/mon-projet",
"scripts": {
  "dev": "vite",
  "build": "vite build",
  "predeploy": "npm run build",
  "deploy": "gh-pages -d dist"
}
```

```bash
git init
git remote add origin https://github.com/mohameden19961/mon-projet.git
git add .
git commit -m "first commit"
git push -u origin main
npm run deploy
```

✅ Disponible sur : `https://mohameden19961.github.io/mon-projet`

---

## 🔺 Next.js

```bash
npx create-next-app@latest mon-projet
cd mon-projet
npm install gh-pages --save-dev
```

**`next.config.js` :**
```js
module.exports = {
  output: 'export',
  basePath: '/mon-projet',
  assetPrefix: '/mon-projet/',
}
```

**`package.json` :**
```json
"homepage": "https://mohameden19961.github.io/mon-projet",
"scripts": {
  "predeploy": "npm run build",
  "deploy": "gh-pages -d out"
}
```

```bash
git init
git remote add origin https://github.com/mohameden19961/mon-projet.git
git add .
git commit -m "first commit"
git push -u origin main
npm run deploy
```

✅ Disponible sur : `https://mohameden19961.github.io/mon-projet`

---

## 🅰️ Angular

```bash
npm install -g @angular/cli
ng new mon-projet
cd mon-projet
npm install gh-pages --save-dev
```

**`package.json` :**
```json
"homepage": "https://mohameden19961.github.io/mon-projet",
"scripts": {
  "predeploy": "ng build --base-href /mon-projet/",
  "deploy": "gh-pages -d dist/mon-projet/browser"
}
```

```bash
git init
git remote add origin https://github.com/mohameden19961/mon-projet.git
git add .
git commit -m "first commit"
git push -u origin main
npm run deploy
```

✅ Disponible sur : `https://mohameden19961.github.io/mon-projet`

---

## ⚙️ Comment fonctionne `npm run deploy` ?

```
npm run deploy
    │
    ├── predeploy → npm run build
    │       └── Vite/Next/Angular compile le code → dossier dist/
    │
    └── deploy → gh-pages -d dist
            └── Crée une branche gh-pages sur GitHub
                    └── GitHub Pages publie automatiquement 🚀
```

---

## 🔗 Domain principal

```
https://mohameden19961.github.io
```

Redirige vers → [github.com/mohameden19961](https://github.com/mohameden19961)
````
