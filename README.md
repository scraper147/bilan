# Bilan des ventes · Chlorophylle Night

Page qui rassemble les exports de ventes des Caisses Bar et en fait le bilan de la soirée.
Adresse : https://scraper147.github.io/bilan/

## Utilisation

1. Sur chaque caisse : **⋮ → Exporter les ventes du jour** (ou **Ventes des jours précédents → Télécharger**). Un fichier `ventes_AAAA-MM-JJ_bar-x.json` est créé par bar et par jour.
2. Ouvrir la page du bilan et y **glisser tous les fichiers** (ou **Choisir des fichiers**). Les fichiers restent sur l'appareil : rien n'est envoyé sur internet.
3. Choisir la soirée et, si besoin, un bar. **Imprimer** donne un bilan papier ou PDF ; **Exporter pour Excel** télécharge deux fichiers CSV (articles et détail des ventes).

## Règles de calcul

- **Soirée** : une vente faite avant 6 h du matin compte dans la soirée de la veille (les caisses découpent leurs exports à minuit).
- **Ventes annulées** : listées à part avec leur motif, comptées dans aucun total.
- **Paiement mixte** : réparti entre cash et Bancontact.
- **Doublons** : si le même bar et le même jour sont chargés deux fois, seul l'export le plus récent est pris en compte. Une vente n'est jamais comptée deux fois (identifiant unique).
- **Contrôle** : total des articles − remises sur ticket = total des ventes. Une alerte signale aussi un bar sans aucune vente pour une soirée où les autres en ont.

## Mise en ligne (déjà faite)

Fichiers à la racine du dépôt `bilan` : `index.html` et `README.md`. GitHub Pages : **Settings → Pages → Deploy from a branch → main → / (root)**.
La page est indépendante de la Caisse Bar (pas de service worker, aucune donnée gardée sauf le choix du thème clair / sombre).
