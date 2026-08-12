# 2048

Le jeu 2048, en **un seul fichier HTML**. Pas d'installation, pas de compte, pas
de connexion internet : on ouvre le fichier et on joue.

## Le principe du jeu

La grille contient des tuiles portant des nombres. À chaque coup, vous poussez
**toutes** les tuiles dans une direction (← ↑ → ↓).

- Deux tuiles voisines portant **le même nombre** se rencontrent : elles
  fusionnent en une seule qui vaut le double (2 + 2 = 4, 4 + 4 = 8, etc.).
- Chaque fusion rapporte sa valeur au score.
- Après chaque coup, une nouvelle tuile (un 2, parfois un 4) apparaît sur une
  case vide.
- Une tuile ne fusionne qu'une fois par coup.
- La partie est perdue quand la grille est pleine et qu'aucune fusion n'est
  possible.

Le but : atteindre la tuile **2048**. Ensuite, rien ne vous empêche de continuer.

## Installer et jouer

**Option 1 — le plus simple**

1. [Téléchargez le dépôt en ZIP](../../archive/refs/heads/main.zip) et décompressez-le.
2. Double-cliquez sur `index.html`.

C'est tout. Le jeu s'ouvre dans votre navigateur et fonctionne **hors ligne**,
maintenant et dans dix ans.

**Option 2 — avec git**

```bash
git clone https://github.com/VOTRE-COMPTE/2048.git
```

Puis ouvrez `index.html`.

> Gardez `index.html` et `orbit-header.js` dans le même dossier : c'est le seul
> lien entre les deux fichiers. Le jeu reste jouable même sans `orbit-header.js`
> (seul le bandeau du haut disparaît).

Aucun serveur, aucun `npm install`, aucune dépendance. Rien n'est envoyé sur
internet : scores, records et réglages sont stockés dans votre navigateur.

## Les commandes

| Action | Commande |
|---|---|
| Déplacer les tuiles | Flèches du clavier, ou balayage du doigt sur mobile |
| Annuler le dernier coup | `Ctrl` + `Z` (jusqu'à 12 coups en arrière) |
| Faire jouer le bot un coup | `B` |

## Ce qu'il y a en plus

- **Grilles 3×3 à 6×6** et un mode *Objectif* (viser 128, 256, 512, 1024 ou
  2048), avec des records séparés par taille de grille.
- **Reprise de partie** : fermez l'onglet, revenez plus tard, la partie est là.
- **Historique des parties** et statistiques (coups, meilleure tuile, parties
  jouées).
- **Couleurs et animations réglables** : chaque couleur de tuile, chaque durée
  d'animation se change depuis le jeu.
- **Un bot** qui peut jouer à votre place ou vous souffler un coup, avec sa
  fonction d'évaluation, sa profondeur de recherche et son banc d'essai.
- **Des tests intégrés** : bouton *Jeu → Lancer les tests* pour vérifier le
  moteur de fusion dans votre propre navigateur.

## Mettre le jeu en ligne (facultatif)

Le dépôt est directement publiable : dans les réglages GitHub du dépôt,
*Pages → Deploy from a branch → main / root*. L'URL fournie sert le jeu tel
quel.

---

Ce jeu fait partie du réseau [Orbit](https://orbit-umber-sigma.vercel.app) : son
bandeau en haut de page est le header commun à tous les projets, servi ici depuis
le dépôt lui-même pour ne jamais dépendre du réseau.
