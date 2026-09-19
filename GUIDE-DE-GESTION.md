# Guide de gestion — Site STRONGHER by Serena

Ce dossier contient ton site (`index.html` + dossier `assets/`). Voici comment le mettre en ligne et le faire vivre dans le temps. Tout ce que tu vas créer ci-dessous (comptes, formulaire) sera **à ton nom**, avec tes propres identifiants — tu seras seule à y avoir accès.

## 1. Mettre le site en ligne (gratuit, sans code) — Netlify

1. Va sur **netlify.com** et crée un compte gratuit (avec ton email).
2. Une fois connectée, cherche l'option **"Deploy manually"** / glisser-déposer un dossier ("Add new site" → "Deploy manually").
3. Glisse le dossier complet du site (celui qui contient `index.html` et `assets/`) dans la zone indiquée.
4. En quelques secondes, ton site est en ligne avec une adresse du type `ton-nom.netlify.app`.
5. Tu peux renommer cette adresse dans **Site settings → Change site name**.

*Alternative équivalente : GitHub Pages, si tu préfères — dis-le-moi et je t'écris le guide correspondant.*

## 2. Ajouter un nom de domaine personnalisé (optionnel)

Si tu veux une adresse du type `strongher-serena.dz` ou `.com` :
1. Achète le nom de domaine chez un registrar (ex. Namecheap, OVH, ou un registrar algérien pour un `.dz`).
2. Dans Netlify : **Site settings → Domain management → Add custom domain**, et suis les instructions pour relier ton domaine (Netlify te donnera les enregistrements DNS à ajouter chez ton registrar).

## 3. Formulaire de contact (Google Forms) — ✅ connecté

Le formulaire du site est maintenant relié à ton Google Form. Il ne te reste qu'une chose à faire :

1. Ouvre ton Google Form → onglet **Réponses → icône Sheets (verte)** pour créer le tableau centralisé.
2. Toutes les demandes envoyées depuis le site arriveront automatiquement dans ce tableau Google Sheets, consultable à tout moment (ordinateur ou téléphone), sans avoir besoin de vérifier ta boîte mail.

**Avant de publier le site**, envoie une vraie demande de test depuis le site (section Contact) et vérifie qu'elle apparaît bien dans ton Google Sheet quelques secondes après. Si ce n'est pas le cas, reviens vers moi.

Si un jour tu modifies les questions de ton Google Form (ajout, suppression, renommage), les identifiants changeront et il faudra me redonner un nouveau lien pré-rempli (voir méthode ci-dessous) pour remettre le site à jour.

<details>
<summary>Comment récupérer un nouveau lien pré-rempli si besoin</summary>

1. Ouvre ton Google Form en aperçu (icône 👁️).
2. Clique sur les **trois points verticaux (⋮)** → **"Obtenir le lien pré-rempli"**.
3. Remplis chaque champ avec un mot simple (ex: `TESTNOM`), clique **"Obtenir le lien"**, copie-le et envoie-le-moi.
</details>

## 3bis. Repérer les doublons (une même prospecte qui envoie plusieurs fois)

Le site est un simple site statique relié à ton Google Form : il n'y a pas de "base de données" qui empêche une même personne d'envoyer sa demande plusieurs fois (par exemple si elle clique deux fois par impatience). Deux garde-fous sont en place :

1. **Le bouton se désactive automatiquement** dès le premier clic ("Envoi en cours...") — ça évite déjà la quasi-totalité des doubles envois accidentels.
2. **Repérer les doublons restants dans ton Google Sheet**, en 2 minutes, une fois :
   - Ouvre ton Google Sheet de réponses.
   - Sélectionne toute la colonne du numéro de téléphone (clique sur la lettre de la colonne, ex. "B").
   - Menu **Format → Mise en forme conditionnelle**.
   - Choisis **"Formule personnalisée"** et entre : `=COUNTIF(B:B,B1)>1` (remplace `B` par la lettre de ta colonne téléphone).
   - Choisis une couleur de fond (ex. jaune) et valide.
   - Désormais, toute ligne dont le numéro de téléphone apparaît plusieurs fois se colore automatiquement — tu la repères d'un coup d'œil et tu supprimes les lignes en trop.

Si un jour le volume de demandes devient important et que ça devient pénible à gérer manuellement, on pourra automatiser cette détection avec un petit script (Google Apps Script) qui bloque ou signale les doublons tout seul — mais ce n'est pas nécessaire pour démarrer.

## 4. Ajouter un témoignage

La section "Témoignages" reste invisible tant qu'elle est vide. Pour en ajouter un :
1. Ouvre `index.html`.
2. Cherche le bloc `var testimonials = [` (tout en bas du fichier).
3. Ajoute une ligne comme celle-ci (en gardant la virgule à la fin de chaque ligne sauf la dernière) :
   ```
   { text: "Le texte de l'avis de la cliente...", name: "Prénom, âge" },
   ```
4. Enregistre le fichier, puis remets-le en ligne sur Netlify (glisser-déposer à nouveau le dossier, ou "drag and drop" la mise à jour).
5. Si tu préfères, envoie-moi simplement le témoignage et je te renvoie le fichier mis à jour.

## 4bis. Le guide gratuit ("5 erreurs qui empêchent de progresser")

Le site propose un mini-guide gratuit en échange d'un contact (prénom + WhatsApp ou email), juste avant la section Contact.

- Le contenu du guide est dans le fichier `guide.html` (même dossier que `index.html`) — modifiable comme n'importe quel texte du site.
- Les demandes de guide arrivent dans **le même Google Sheet** que le formulaire de contact (la ligne "Message" affichera automatiquement *"📥 Demande : Guide gratuit"* pour que tu les repères facilement et ne les confondes pas avec une vraie demande de coaching).
- Le badge "Certifications ISSA vérifiables" dans la section À propos est pour l'instant un badge générique que j'ai dessiné (pas ton vrai logo/badge officiel ISSA). Si tu as ton badge numérique officiel (reçu par email de l'ISSA, ou un badge Credly), envoie-le-moi et je le mets à sa place — ce sera plus crédible qu'un badge générique.
- La section **FAQ** (5 questions/réponses) se modifie directement dans `index.html` en cherchant le texte de la question avec Ctrl+F.

## 5. Modifier un texte, un tarif ou une photo

- Tous les textes sont directement dans `index.html`, lisibles même sans savoir coder (cherche le texte à changer avec Ctrl+F et remplace-le).
- Pour changer la photo d'accueil : remplace le fichier `assets/hero.jpg` par une nouvelle photo portant le même nom.
- Pour toute modification plus importante, tu peux toujours revenir vers moi avec ta demande, je te renverrai les fichiers mis à jour.

## Récapitulatif des comptes à créer (par toi, gratuits)

| Service | Usage | Lien |
|---|---|---|
| Netlify | Héberger le site en ligne | netlify.com |
| Google Forms + Sheets | Recevoir les demandes du formulaire | forms.google.com |
| (Optionnel) Registrar de domaine | Nom de domaine personnalisé | ex. namecheap.com |
| Google Search Console | Faire apparaître le site sur Google | search.google.com/search-console |

Tous ces comptes t'appartiennent entièrement — aucun accès à transmettre entre nous, tu es propriétaire de tout dès la création.

## 6. Publier la version finale sur Netlify

1. Va sur **netlify.com**, connecte-toi à ton compte.
2. Si c'est ta première mise en ligne : **"Add new site" → "Deploy manually"**, puis glisse le dossier complet (`index.html`, `assets/`, `robots.txt`, `sitemap.xml`).
3. Si le site existe déjà : va sur ton site dans Netlify → onglet **"Deploys"** → glisse à nouveau le dossier complet dans la zone de dépôt : ça remplace automatiquement l'ancienne version.
4. Netlify te donne une adresse `xxxx.netlify.app`. Tu peux la personnaliser dans **Site settings → Change site name**.

✅ Ton adresse définitive est déjà configurée partout dans le site : **strongherbyserena.netlify.app**

## 7. Faire apparaître le site sur Google (référencement / SEO)

Le site est déjà préparé techniquement pour le référencement (titre et description optimisés, données structurées, fichier `sitemap.xml`, fichier `robots.txt`). Il reste des actions à faire une fois le site en ligne :

1. **Google Search Console** (gratuit) :
   - Va sur **search.google.com/search-console**, connecte-toi avec un compte Google.
   - Ajoute ton site (propriété de type "Préfixe d'URL", avec ton adresse Netlify ou ton domaine).
   - Vérifie la propriété (Google te propose plusieurs méthodes, la plus simple est souvent via une balise HTML ou ton compte Netlify DNS si tu as un domaine).
   - Une fois vérifié, va dans **"Sitemaps"** et soumets : `sitemap.xml`
   - Utilise ensuite **"Inspection d'URL"** sur ta page d'accueil et clique **"Demander une indexation"** — Google explore ton site sous quelques jours.

2. **Ton Instagram** : mets le lien du site dans ta bio Instagram et mentionne-le dans quelques posts/stories — Google et tes visiteurs y accèdent plus vite, et ça crée un premier lien externe vers le site (bon pour le référencement).

3. **Avec le temps** : plus tu as de témoignages clients réels, de contenu récent, et de gens qui partagent ton site, mieux tu seras classée. Pas d'action magique immédiate — le référencement se construit sur plusieurs semaines/mois.

4. **Optionnel mais utile** : un nom de domaine personnalisé (`.com` ou `.dz`) est perçu comme plus crédible qu'une adresse `netlify.app`, autant par les visiteuses que par Google.

5. **Google Analytics 4** (gratuit, indispensable dès le lancement) — sans lui, tu ne sauras jamais combien de personnes visitent ton site, ni ce qu'elles font dessus :
   - Va sur **analytics.google.com** et crée un compte gratuit.
   - Crée une **propriété** pour ton site (nom au choix, ex. "STRONGHER by Serena"), fuseau horaire Algérie, devise DZD.
   - Google te donne un identifiant du type `G-XXXXXXXXXX` (onglet **Flux de données → ton flux web**).
   - Ouvre `index.html`, cherche `G-XXXXXXXXXX` (il apparaît 2 fois, tout en haut du fichier) et remplace-le par ton propre identifiant aux deux endroits.
   - Remets le site en ligne (Netlify) : après quelques heures, tu peux suivre tes visites en temps réel dans Google Analytics.

6. **Google Business Profile** (gratuit) — renforce ta crédibilité et ton référencement local, même pour un service en ligne :
   - Va sur **business.google.com** et crée une fiche gratuite.
   - Choisis "Je livre des biens et services à mes clients" / zone de service (plutôt qu'une adresse physique, puisque tu coaches en ligne) et sélectionne l'Algérie comme zone couverte.
   - Renseigne ta catégorie ("Coach sportif" ou "Coach en nutrition"), ton site, ton Instagram.
   - Une fois validée, ta fiche peut apparaître dans les résultats Google et permet de recevoir des avis clients, un vrai plus pour la confiance.

## 8. Plateforme d'hébergement recommandée

Netlify pousse vers un forfait payant selon l'usage. Voici les alternatives gratuites, reconnues et professionnelles.

⚠️ **Concernant un nom de domaine gratuit** : aucune plateforme sérieuse n'en propose (les rares services qui le font, comme Freenom avec des domaines `.tk`/`.ml`, sont peu fiables et donnent une image moins professionnelle — à éviter). Un vrai `.com` coûte environ 1000-1500 DZD/an chez la plupart des registrars sérieux — optionnel, à envisager plus tard si tu veux.

### ⚠️ À savoir avant de choisir Vercel

Vercel est très reconnu et pro, mais son offre gratuite ("Hobby") **interdit explicitement l'usage commercial** dans ses conditions d'utilisation — un site qui vend des services, comme le tien, entre dans cette catégorie, même sans paiement en ligne direct. Dans les faits, ce n'est pas systématiquement contrôlé et beaucoup de petits sites l'utilisent sans problème, mais tu ne serais techniquement pas dans les clous. **Cloudflare Pages n'a pas cette restriction** (gratuit pour un usage commercial) et reste tout aussi reconnu — à toi de voir selon ton niveau de tolérance à ce risque.

### Option A — Vercel (via GitHub, en 2 étapes)

Vercel ne propose pas de glisser-déposer direct comme Netlify : il faut passer par un dépôt GitHub (gratuit, juste pour stocker tes fichiers), que Vercel viendra lire automatiquement.

**Étape 1 — Mettre tes fichiers sur GitHub**
1. Va sur **github.com**, crée un compte gratuit (tu peux directement l'utiliser pour te connecter à Vercel ensuite).
2. Clique **"New repository"**, nomme-le par exemple `strongher-site`, coche **"Public"**, puis **"Create repository"**.
3. Clique **"Add file" → "Upload files"**, glisse ton dossier complet (`index.html`, `assets/`, `robots.txt`, `sitemap.xml`), puis **"Commit changes"**.

**Étape 2 — Connecter Vercel à ce dépôt**
1. Va sur **vercel.com**, clique **"Sign Up"** → **"Continue with GitHub"** (utilise le compte que tu viens de créer).
2. Sur ton tableau de bord, clique **"Add New..." → "Project"**.
3. Trouve `strongher-site` dans la liste et clique **"Import"**.
4. Vercel détecte automatiquement un site statique — laisse les réglages par défaut (Framework Preset : "Other").
5. Clique **"Deploy"**. Après ~30 secondes, ton site est en ligne à une adresse du type `strongher-site.vercel.app`.

**Pour republier après une modification** : va sur ton dépôt GitHub → ouvre le fichier à modifier → icône crayon (✏️) pour éditer directement dans le navigateur, ou "Upload files" pour remplacer un fichier → **Commit changes**. Vercel redéploie automatiquement en quelques secondes, sans que tu aies besoin de revenir sur son site.

### Option B — Cloudflare Pages (gratuit sans restriction commerciale)

1. Va sur **dash.cloudflare.com** et crée un compte gratuit.
2. Dans le menu de gauche : **Workers & Pages → Create → Pages → Upload assets**.
3. Donne un nom à ton projet (ex. `strongher-serena`).
4. Glisse-dépose ton dossier complet (`index.html`, `assets/`, `robots.txt`, `sitemap.xml`).
5. Clique **Deploy site**. Tu obtiens une adresse du type `strongher-serena.pages.dev`.
6. Pour republier après une modification : reviens sur le projet → onglet **Deployments** → **Create deployment**, et glisse à nouveau le dossier.

### Option C — GitHub Pages (gratuit à vie, aucune restriction, aucune limite gênante)

1. Reprends le dépôt GitHub créé à l'Option A (étape 1) — ou crées-en un si tu ne fais pas Vercel.
2. Va dans **Settings → Pages** (menu de gauche du dépôt).
3. Sous "Source", choisis la branche **main** et le dossier **/ (root)**, puis **Save**.
4. Après 1-2 minutes, ton site est en ligne à une adresse du type `ton-nom.github.io/strongher-site`.

**Dans tous les cas** : une fois ton site en ligne, envoie-moi l'adresse définitive — je remettrai à jour les liens SEO (`canonical`, `og:url`, `sitemap.xml`, `robots.txt`), comme je l'ai fait pour Netlify.
