# Référence — Fichiers du projet & comptes utilisés

Document de contrôle : à quoi sert chaque fichier du projet, et à quoi sert chaque compte/plateforme externe. À garder sous la main pour t'y retrouver, surtout au début.

---

## Partie 1 — Les fichiers du projet

| Fichier | À quoi il sert |
|---|---|
| `index.html` | **La page principale du site.** Tout ce qu'une visiteuse voit en arrivant : hero, à propos, mon histoire, services, formules et prix, guide gratuit, contact. C'est le fichier à modifier pour 95% des changements (texte, prix, liens). |
| `guide.html` | La page du mini-guide gratuit *"5 erreurs qui empêchent de progresser"*, offerte en échange d'un contact (prénom + WhatsApp/email). Séparée de `index.html` pour ne pas alourdir la page principale. |
| `assets/hero.jpg` | La photo d'accueil (bandeau photo à gauche du haut de page). La remplacer suffit à changer l'image, sans toucher au code. |
| `assets/issa-logo.png` | Le logo officiel de l'ISSA, affiché dans la section "À propos" comme preuve de certification. |
| `robots.txt` | Un fichier technique qui dit aux moteurs de recherche (Google...) quelles pages ils ont le droit d'explorer. Pas de changement nécessaire sauf cas particulier. |
| `sitemap.xml` | La liste des pages du site à indexer, transmise à Google Search Console pour l'aider à toutes les trouver. |
| `_headers` | Fichier de configuration lu automatiquement par l'hébergeur (Vercel) pour ajouter des protections de sécurité de base (empêche par exemple que le site soit caché dans un autre site). Invisible pour les visiteuses, aucune action de ta part. |
| `GUIDE-DE-GESTION.md` | Le mode d'emploi complet, étape par étape : mise en ligne, formulaire, ajout de témoignages, SEO, etc. |
| `REFERENCE-COMPTES-ET-FICHIERS.md` | Ce document — la vue d'ensemble de contrôle. |

---

## Partie 2 — Les comptes/plateformes utilisés

| Compte | À quoi il sert | Quand le consulter | Quoi faire concrètement une fois dessus |
|---|---|---|---|
| **GitHub** | Stocke le code du site et tout son historique de versions — la "source de vérité" du projet. | Rarement, sauf pour vérifier un historique de changement. | Onglet **"Commits"** : vérifier que le dernier commit correspond bien au dernier changement fait. |
| **Vercel** | Héberge le site et le rend accessible publiquement. Connecté à GitHub : republie automatiquement à chaque mise à jour. | **Après chaque modification envoyée sur GitHub**, pour confirmer la mise en ligne. | Onglet **"Deployments"** : le dernier doit être marqué **"Ready"** (vert). S'il est **"Failed"** (rouge/erreur), cliquer dessus pour voir le message d'erreur, ou revenir vers l'assistance technique avec une capture d'écran. |
| **Google Forms** | Reçoit toutes les demandes envoyées via les formulaires du site (devis de coaching + demandes de guide gratuit). | Seulement si tu changes un jour les questions du formulaire. | Modifier les questions, puis récupérer un nouveau lien pré-rempli (voir section 3 du `GUIDE-DE-GESTION.md`) pour remettre le site à jour. |
| **Google Sheets** | Le tableau où toutes les réponses du Google Form s'accumulent automatiquement, ligne par ligne. | **Tous les jours**, idéalement. | Repérer les nouvelles lignes (nouvelles demandes) et les lignes surlignées (doublons, voir section 3bis du guide), puis **recontacter chaque nouvelle prospecte** par téléphone/WhatsApp/email dans les 24-48h. |
| **Google Analytics 4** | Mesure le trafic du site : nombre de visiteurs, d'où ils viennent (Instagram, Google, direct...), quelles pages ils consultent. | **Chaque semaine.** | Regarder si le nombre de visiteurs progresse et d'où vient le trafic. Si une source (ex. Instagram) amène beaucoup de visites, refaire du contenu similaire pour l'alimenter. |
| **Google Search Console** | Surveille comment Google "voit" ton site : pages indexées, erreurs éventuelles, requêtes qui amènent des visiteurs jusqu'à toi. | **1 fois par mois**, plus souvent juste après une mise en ligne importante. | Vérifier l'onglet **"Pages"** (pas d'erreur d'indexation). Si une page pose problème, utiliser **"Inspection d'URL" → "Demander une indexation"**. |
| **Google Business Profile** | Fiche gratuite pouvant apparaître dans les résultats Google/Maps, avec avis clients. | **Dès qu'un avis arrive** (Google envoie un email de notification). | Lire l'avis et y **répondre** (même en 2 lignes, positif ou négatif) — ça montre que le compte est actif et suivi. |
| **Instagram** (`@serena.inspires`) | Canal principal de contenu et de preuve sociale, relié au site dans les deux sens. | Usage habituel. | Garder le lien du site en bio et le rementionner de temps en temps en story — le site vient en complément, pas en remplacement. |
| **Registrar de domaine** *(optionnel, pas encore actif)* | Si un nom de domaine personnalisé (`.com`/`.dz`) est acheté un jour, à la place de l'adresse `vercel.app` par défaut. | Seulement au moment de l'achat. | Suivre la section 2 du `GUIDE-DE-GESTION.md` pour relier le domaine à Vercel. |

*(Les liens directs vers chacun de ces comptes sont dans `LIENS-UTILES.xlsx`.)*

---

## Repère rapide : "quoi checker, à quelle fréquence, et pourquoi"

- **Tous les jours** → Google Sheet : recontacter les nouvelles prospectes.
- **Toutes les semaines** → Google Analytics : suivre l'évolution du trafic et sa source.
- **Tous les mois** → Google Search Console : s'assurer que le site reste bien indexé sans erreur.
- **À chaque avis reçu** → Google Business Profile : répondre à l'avis.
- **À chaque modification du site** → Vercel : confirmer que le déploiement est "Ready".
