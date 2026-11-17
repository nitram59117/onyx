# ONYX

Pilotage de soirées pour clubs et discothèques : billetterie, bar, sécurité, personnel, synthèse de soirée, rapports et écran d'affichage en direct.

Ce dépôt contient la **démo** d'ONYX : une application d'une seule page (`index.html`), sans serveur.

## Ce que fait la démo

- **Tableau de bord** : EBE de la soirée, CA, entrées, bar par entrée, indicateurs clés, comparaison avec une autre soirée.
- **Billetterie** : billets par tarif et par canal, scans, import d'un export Shotgun (CSV ou Excel).
- **Bar** : CA, consommations, écarts de caisse, produits, import d'un rapport Trivec (Excel).
- **Sécurité** : main courante (recalés, interventions), affluence.
- **Personnel** : postes, heures et coûts, paliers selon la jauge.
- **Synthèse soirée** et **Rapports** (semaine, mois, année).
- **Affichage** : écran personnalisable en plein écran pour une télé (ajouter `#ecran` à l'adresse).
- **Équipe** : comptes par e-mail, mot de passe créé à la première connexion, droits selon le poste, comptes activables ou désactivables.

## Sécurité des données

- Les données d'un établissement réel sont **chiffrées (AES-256-GCM, clé dérivée par PBKDF2)** dans `index.html`. Elles ne se déverrouillent qu'avec la clé de l'établissement, qui n'est pas dans ce dépôt.
- Les mots de passe ne sont jamais conservés : seule une empreinte PBKDF2 est gardée, dans le navigateur.
- Le club « Le Hangar » est fictif et sert aux démonstrations.

## Limites de la démo

- Les données saisies restent dans le navigateur de chaque appareil.
- Les connexions directes à l'API Shotgun et à la caisse Trivec demandent la version serveur (jetons chiffrés côté serveur, synchronisation automatique).

## Mise en ligne

Activer GitHub Pages : *Settings › Pages › Deploy from a branch › main / (root)*. La démo est alors servie à l'adresse `https://nitram59117.github.io/onyx/`.

---

© ONYX — Martin Galloo. Tous droits réservés.
