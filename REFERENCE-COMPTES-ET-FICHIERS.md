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

| Compte | À quoi il sert | Qui l'utilise / quand le consulter |
|---|---|---|
| **GitHub** | Stocke le code du site et tout son historique de versions — la "source de vérité" du projet. Chaque mise à jour part de là. | Rarement à consulter toi-même ; c'est l'étape technique gérée à chaque modification. |
| **Vercel** | Héberge le site et le rend accessible publiquement sur internet. Connecté à GitHub : republie automatiquement le site à chaque mise à jour. | À vérifier après une modification, pour confirmer que le site est bien à jour en ligne. |
| **Google Forms** | Reçoit toutes les demandes envoyées via les formulaires du site (devis de coaching + demandes de guide gratuit). | Pas besoin d'y retourner une fois configuré — tout passe par le Google Sheet. |
| **Google Sheets** | Le tableau où toutes les réponses du Google Form s'accumulent automatiquement, ligne par ligne. | **À consulter très régulièrement (idéalement tous les jours)** — c'est ta liste de prospectes à recontacter. |
| **Google Analytics 4** | Mesure le trafic du site : nombre de visiteurs, d'où ils viennent (Instagram, Google, direct...), quelles pages ils consultent. | À consulter chaque semaine pour voir si le trafic progresse et d'où il vient. |
| **Google Search Console** | Surveille comment Google "voit" ton site : pages indexées, erreurs éventuelles, requêtes qui amènent des visiteurs jusqu'à toi. | À consulter une fois par mois environ, plus souvent juste après la mise en ligne. |
| **Google Business Profile** | Fiche gratuite pouvant apparaître dans les résultats Google/Maps, avec avis clients. Renforce la crédibilité locale même pour un service 100% en ligne. | À consulter dès qu'un avis client arrive, pour le voir et éventuellement y répondre. |
| **Instagram** (`@serena.inspires`) | Canal principal de contenu et de preuve sociale, relié au site dans les deux sens (lien dans le site, lien en bio Instagram). | Ton usage habituel — le site vient en complément, pas en remplacement. |
| **Registrar de domaine** *(optionnel, pas encore actif)* | Si tu achètes un jour un nom de domaine personnalisé (`.com`/`.dz`) plutôt que l'adresse `vercel.app` par défaut. | À activer seulement si/quand tu veux franchir cette étape. |

---

## Repère rapide : "quoi checker, à quelle fréquence"

- **Tous les jours** : Google Sheet (nouvelles demandes)
- **Toutes les semaines** : Google Analytics (trafic)
- **Tous les mois** : Google Search Console (référencement)
- **À chaque avis reçu** : Google Business Profile
- **À chaque modification du site** : vérifier que Vercel a bien republié la nouvelle version
