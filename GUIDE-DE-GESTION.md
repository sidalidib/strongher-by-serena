# Guide de gestion — Site STRONGHER by Serena

Ce dossier contient ton site (`index.html` + dossier `assets/`). Voici comment le mettre en ligne et le faire vivre dans le temps. Tout ce que tu vas créer ci-dessous (comptes, formulaire) sera **à ton nom**, avec tes propres identifiants — tu seras seule à y avoir accès.

## 1. Mettre le site en ligne — Vercel (via GitHub)

Vercel ne propose pas de glisser-déposer direct : il lit tes fichiers depuis un dépôt GitHub et republie automatiquement le site à chaque mise à jour. C'est ce qui est déjà en place.

⚠️ **À savoir sur l'offre gratuite Vercel** : l'offre gratuite ("Hobby") **interdit explicitement l'usage commercial** dans ses conditions d'utilisation — un site qui vend des services, comme le tien, entre dans cette catégorie, même sans paiement en ligne direct. Dans les faits, ce n'est pas systématiquement contrôlé et beaucoup de petits sites l'utilisent sans problème, mais tu ne serais techniquement pas dans les clous. Si un jour tu préfères une alternative sans cette restriction (ex. Cloudflare Pages, gratuit aussi), dis-le-moi et je t'écris le guide de migration correspondant.

**Le workflow au quotidien** :
1. Tu modifies un fichier (dans VS Code, ou directement sur github.com).
2. Le changement est envoyé sur ton dépôt GitHub (voir section 1bis pour le "comment").
3. Vercel détecte automatiquement le changement et republie le site en quelques secondes — **tu n'as plus jamais besoin de glisser-déposer quoi que ce soit.**

✅ Ton adresse définitive est déjà configurée partout dans le site : **strongher-by-serena.vercel.app**

*Tu peux la personnaliser dans **Project Settings → Domains** sur Vercel.*

## 1bis. Gérer GitHub soi-même (commit, push, pull, conflits)

Instructions pour envoyer tes propres modifications sur GitHub, avec VS Code (le plus simple) et l'équivalent en ligne de commande.

**Le vocabulaire de base**
- **Dépôt (repository)** : le dossier du projet avec tout son historique de versions. Le tien : `github.com/sidalidib/strongher-by-serena`.
- **Commit** : une "photo" du projet à un instant donné, avec un petit message qui décrit ce qui a changé. Chaque commit reste dans l'historique pour toujours — tu peux donc toujours revenir en arrière si besoin.
- **Push** : envoyer tes commits vers GitHub (en ligne).
- **Pull** : récupérer sur ton ordinateur les changements qui existent déjà sur GitHub mais pas encore chez toi.
- **Conflit** : arrive quand le **même endroit d'un fichier** a été modifié différemment à deux endroits différents (par exemple une fois sur github.com, une fois sur ton ordinateur) sans synchronisation entre les deux. Git ne sait pas lequel des deux garder, et te demande de choisir.

**Envoyer une modification sur GitHub — avec VS Code**
1. Modifie et enregistre ton fichier normalement (Ctrl+S).
2. Ouvre l'onglet **Source Control** dans la barre de gauche (icône avec des branches, ou `Ctrl+Shift+G`). Les fichiers modifiés y apparaissent.
3. Clique sur le **+** à côté de chaque fichier (ou au-dessus de la liste pour tous les prendre) pour les mettre "en attente" (*staged*).
4. Écris une courte description du changement dans le champ de message en haut (ex. *"Mise à jour du prix de la formule Signature"*).
5. Clique sur le bouton **✓ Commit**.
6. Clique sur **Sync Changes** (ou **Push**) en bas à gauche — ça envoie ton commit vers GitHub.

→ Vercel détecte le changement et republie le site automatiquement en quelques secondes, sans rien glisser-déposer.

**L'équivalent en ligne de commande** (terminal, dans le dossier du projet) :
```
git add -A
git commit -m "description du changement"
git push
```

**Comment éviter les conflits**
La règle simple : ne jamais modifier le même fichier à deux endroits en même temps sans les synchroniser entre les deux.
- Si tu modifies un fichier directement sur GitHub (icône crayon ✏️ sur github.com), fais un **Pull** (bouton "Sync Changes" dans VS Code, ou `git pull` en ligne de commande) avant de continuer à modifier ce même fichier sur ton ordinateur.
- À l'inverse, si tu as des modifications locales en cours, envoie-les (push) avant d'aller modifier quoi que ce soit directement sur github.com.
- Dans les deux cas, l'ordre à retenir est : **synchronise avant de repartir travailler**.

**Si un conflit arrive quand même**
Rien n'est perdu. VS Code affiche le fichier concerné avec les deux versions face à face et des boutons **"Accept Current Change"** / **"Accept Incoming Change"** / **"Accept Both Changes"** directement au-dessus du texte en conflit — il suffit de cliquer sur celle à garder (ou les deux si tu veux fusionner à la main), d'enregistrer, puis de faire un commit normal pour valider la résolution. En ligne de commande, le fichier affiche les mêmes zones marquées par `<<<<<<<`, `=======`, `>>>>>>>` : il faut les modifier à la main pour ne garder que le texte final voulu, enregistrer, puis `git add` + `git commit`.

**À quoi sert le Pull dans la pratique**
Si tu ne travailles que depuis un seul ordinateur et que tu ne modifies jamais rien directement sur github.com, le Pull ne sert quasiment jamais (GitHub n'a alors jamais rien que ton ordinateur n'ait déjà). Il devient utile dans deux cas : tu as modifié un fichier directement sur github.com, ou tu récupères le projet sur un autre ordinateur (`git clone https://github.com/sidalidib/strongher-by-serena.git` la première fois, puis `git pull` ensuite).

## 2. Ajouter un nom de domaine personnalisé (optionnel)

⚠️ **Concernant un nom de domaine gratuit** : aucune plateforme sérieuse n'en propose (les rares services qui le font, comme Freenom avec des domaines `.tk`/`.ml`, sont peu fiables et donnent une image moins professionnelle — à éviter). Un vrai `.com` coûte environ 1000-1500 DZD/an chez la plupart des registrars sérieux — optionnel, à envisager plus tard si tu veux.

Si tu veux une adresse du type `strongher-serena.dz` ou `.com` :
1. Achète le nom de domaine chez un registrar (ex. Namecheap, OVH, ou un registrar algérien pour un `.dz`).
2. Dans Vercel : **Project Settings → Domains → Add**, et suis les instructions pour relier ton domaine (Vercel te donnera les enregistrements DNS à ajouter chez ton registrar).

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
4. Enregistre le fichier, puis envoie-le sur GitHub (voir section 1bis) : Vercel republie automatiquement en quelques secondes, sans rien glisser-déposer.

## 4bis. Le guide gratuit ("5 erreurs qui empêchent de progresser")

Le site propose un mini-guide gratuit en échange d'un contact (prénom + WhatsApp ou email), juste avant la section Contact.

- Le contenu du guide est dans le fichier `guide.html` (même dossier que `index.html`) — modifiable comme n'importe quel texte du site.
- Les demandes de guide arrivent dans **le même Google Sheet** que le formulaire de contact (la ligne "Message" affichera automatiquement *"📥 Demande : Guide gratuit"* pour que tu les repères facilement et ne les confondes pas avec une vraie demande de coaching).
- Le badge "Certifications ISSA vérifiables" dans la section À propos affiche maintenant le vrai logo officiel ISSA.

## 5. Modifier un texte, un tarif ou une photo

- Tous les textes sont directement dans `index.html`, lisibles même sans savoir coder (cherche le texte à changer avec Ctrl+F et remplace-le).
- Pour changer la photo d'accueil : remplace le fichier `assets/hero.jpg` par une nouvelle photo portant le même nom.
- Une fois le fichier modifié, envoie-le sur GitHub (voir section 1bis) : Vercel republie automatiquement le site en quelques secondes.

## Récapitulatif des comptes à créer (par toi, gratuits)

| Service | Usage | Lien |
|---|---|---|
| GitHub | Stocker le code du site et son historique | github.com |
| Vercel | Héberger le site en ligne (connecté à GitHub) | vercel.com |
| Google Forms + Sheets | Recevoir les demandes du formulaire | forms.google.com |
| Google Analytics 4 | Suivre les visites du site | analytics.google.com |
| Google Search Console | Faire apparaître le site sur Google | search.google.com/search-console |
| Google Business Profile | Visibilité locale + avis clients | business.google.com |
| (Optionnel) Registrar de domaine | Nom de domaine personnalisé | ex. namecheap.com |

Tous ces comptes t'appartiennent entièrement — aucun accès à transmettre entre nous, tu es propriétaire de tout dès la création.

*(Pour le détail de ce que fait chaque compte et à quelle fréquence le consulter, voir le document séparé `REFERENCE-COMPTES-ET-FICHIERS.md`.)*

## 6. Faire apparaître le site sur Google (référencement / SEO)

Le site est déjà préparé techniquement pour le référencement (titre et description optimisés, données structurées, fichier `sitemap.xml`, fichier `robots.txt`). Il reste des actions à faire une fois le site en ligne :

1. **Google Search Console** (gratuit) :
   - Va sur **search.google.com/search-console**, connecte-toi avec un compte Google.
   - Ajoute ton site (propriété de type "Préfixe d'URL", avec ton adresse Vercel ou ton domaine).
   - Vérifie la propriété (Google te propose plusieurs méthodes, la plus simple est souvent via une balise HTML).
   - Une fois vérifié, va dans **"Sitemaps"** et soumets : `sitemap.xml`
   - Utilise ensuite **"Inspection d'URL"** sur ta page d'accueil et clique **"Demander une indexation"** — Google explore ton site sous quelques jours.

2. **Ton Instagram** : mets le lien du site dans ta bio Instagram et mentionne-le dans quelques posts/stories — Google et tes visiteurs y accèdent plus vite, et ça crée un premier lien externe vers le site (bon pour le référencement).

3. **Avec le temps** : plus tu as de témoignages clients réels, de contenu récent, et de gens qui partagent ton site, mieux tu seras classée. Pas d'action magique immédiate — le référencement se construit sur plusieurs semaines/mois.

4. **Optionnel mais utile** : un nom de domaine personnalisé (`.com` ou `.dz`) est perçu comme plus crédible qu'une adresse `vercel.app`, autant par les visiteuses que par Google.

5. **Google Analytics 4** (gratuit, indispensable dès le lancement) — sans lui, tu ne sauras jamais combien de personnes visitent ton site, ni ce qu'elles font dessus :
   - Va sur **analytics.google.com** et crée un compte gratuit.
   - Crée une **propriété** pour ton site (nom au choix, ex. "STRONGHER by Serena"), fuseau horaire Algérie, devise DZD.
   - Google te donne un identifiant du type `G-XXXXXXXXXX` (onglet **Flux de données → ton flux web**).
   - ✅ Déjà fait : l'identifiant est en place dans `index.html`.

6. **Google Business Profile** (gratuit) — renforce ta crédibilité et ton référencement local, même pour un service en ligne :
   - Va sur **business.google.com** et crée une fiche gratuite.
   - Choisis "Je livre des biens et services à mes clients" / zone de service (plutôt qu'une adresse physique, puisque tu coaches en ligne) et sélectionne l'Algérie comme zone couverte.
   - Renseigne ta catégorie ("Coach sportif" ou "Coach en nutrition"), ton site, ton Instagram.
   - Une fois validée, ta fiche peut apparaître dans les résultats Google et permet de recevoir des avis clients, un vrai plus pour la confiance.
