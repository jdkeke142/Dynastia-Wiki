# 🛠️ Guide de la modération

Ce guide présente les outils de l'équipe de modération : sanctionner, suivre le casier d'un joueur, repérer les doubles comptes et rester discret en jeu.

{% hint style="info" %}
Toute sanction est proportionnée aux faits et aux antécédents du joueur (R3). Tu ne traites jamais un cas qui te concerne personnellement (R5).
{% endhint %}

## <mark style="color:yellow;">Les commandes</mark> <a href="#commandes" id="commandes"></a>

| Commande | Ce qu'elle fait |
| --- | --- |
| **Sanctionner** | [Détails](#sanctionner) |
| `/warn <joueur> <motif>` | Avertit le joueur par un message. Aucun effet sur le jeu. |
| `/kick <joueur> <motif>` | Déconnecte le joueur, qui peut revenir aussitôt. Il doit être en ligne. |
| `/mute <joueur> <durée> <motif>` | L'empêche d'écrire dans le chat et d'envoyer des messages privés. |
| `/ban <joueur> <durée> <motif>` | Le déconnecte et l'empêche de revenir avant la fin de la durée. |
| `/unwarn <joueur> <raison>` | Retire son dernier avertissement. |
| `/unmute <joueur> <raison>` | Lui rend la parole. |
| `/unban <joueur> <raison>` | Lève son bannissement. |
| **Suivre** | |
| `/casier <joueur>` | Ouvre l'historique de ses sanctions. Raccourcis : `/c`, `/history`. [Détails](#casier) |
| `/banlist` | Ouvre la liste des bannissements du serveur. [Détails](#listes) |
| `/mutelist` | Ouvre la liste des réductions au silence du serveur. [Détails](#listes) |
| `/comptes <joueur>` | Liste ses comptes liés (même adresse). Raccourci : `/alts`. [Détails](#doubles-comptes) |
| **Rester discret** | [Détails](#modes) |
| `/afk` | Active ou désactive le mode AFK. |
| `/vanish` | Active ou désactive le mode spectateur. Raccourci : `/v`. |

Ajoute `help` après une commande pour afficher son aide en jeu, par exemple `/ban help`.

## <mark style="color:yellow;">Sanctionner</mark> <a href="#sanctionner" id="sanctionner"></a>

Le joueur sanctionné voit toujours ton nom et le motif. Un joueur banni voit aussi le temps restant à chaque tentative de connexion, et l'invitation à contester sur le Discord. Un joueur réduit au silence voit le temps restant chaque fois qu'il essaie d'écrire. Quiconque lui envoie un message privé est prévenu qu'il ne pourra pas répondre.

Une fois la sanction appliquée, toute l'équipe connectée en est informée. Un bouton <mark style="color:yellow;">\[Plus d'infos]</mark> ouvre directement la sanction dans le casier.

{% hint style="warning" %}
* Le <mark style="color:red;">motif</mark> est obligatoire.
* Tu ne peux sanctionner qu'un joueur de grade <mark style="color:red;">strictement inférieur</mark> au tien.
* Un joueur n'a qu'un seul bannissement et qu'une seule réduction au silence en cours. Pour changer la durée, modifie la sanction depuis le [casier](#casier) au lieu d'en donner une nouvelle.
{% endhint %}

Une sanction fonctionne aussi sur un joueur hors ligne, s'il s'est déjà connecté au serveur. Seule l'expulsion demande qu'il soit en ligne.

### <mark style="color:yellow;">Les durées</mark> <a href="#durees" id="durees"></a>

Un nombre suivi d'une unité, sans espace : `30m`, `2h`, `7d`, `2w`, `3mo`, `1y`.

| `s` | `m` | `h` | `d` | `w` | `mo` | `y` |
| --- | --- | --- | --- | --- | --- | --- |
| secondes | minutes | heures | jours | semaines | mois | années |

{% hint style="danger" %}
<mark style="color:red;">`m` veut dire minutes.</mark> Pour des mois, écris `mo`. Les unités ne se combinent pas : écris `36h` plutôt que `1d12h`.
{% endhint %}

Une sanction dure <mark style="color:red;">un an au plus</mark>.

## <mark style="color:yellow;">Le casier</mark> <a href="#casier" id="casier"></a>

`/casier <joueur>` ouvre l'historique de toutes les sanctions du joueur. Rien ne s'efface : une sanction terminée ou annulée reste visible, avec son état.

En haut, le **bilan** du joueur indique depuis quand il est connu, combien de sanctions il a reçues de chaque type, et s'il est banni ou réduit au silence en ce moment (avec le temps restant). L'entonnoir trie les sanctions par type.

Chaque sanction affiche son motif, sa date, son auteur et son état : <mark style="color:red;">en vigueur</mark>, <mark style="color:green;">actif</mark> (avertissement), ponctuelle (expulsion), expirée ou annulée. Une sanction modifiée montre sa version d'origine et sa version actuelle.

### <mark style="color:yellow;">Gérer une sanction en cours</mark> <a href="#gerer" id="gerer"></a>

Clique sur une sanction en cours pour :

* <mark style="color:yellow;">**modifier sa durée**</mark> : la nouvelle durée est la <mark style="color:red;">durée totale</mark>, comptée depuis le jour de la sanction et non depuis aujourd'hui ;
* <mark style="color:yellow;">**modifier son motif**</mark> ;
* <mark style="color:yellow;">**l'annuler**</mark> : elle prend fin, mais reste au casier.

Chaque changement demande une <mark style="color:red;">raison</mark>, conservée avec ton nom. Si un autre membre de l'équipe a modifié la même sanction juste avant toi, ton changement est refusé : rouvre-la pour voir sa version à jour.

### <mark style="color:yellow;">Les listes</mark> <a href="#listes" id="listes"></a>

`/banlist` et `/mutelist` ouvrent la liste des bannissements et des réductions au silence de tout le serveur. Le tri permet d'afficher toutes les sanctions, celles en cours, celles annulées ou celles modifiées. Clique sur une sanction en cours pour la gérer.

## <mark style="color:yellow;">Les doubles comptes</mark> <a href="#doubles-comptes" id="doubles-comptes"></a>

Deux comptes connectés depuis la même adresse restent <mark style="color:red;">liés pendant 30 jours</mark>.

Quand un joueur ayant des comptes liés se connecte, l'équipe reçoit une alerte « ⚠ Double compte » avec un son. Chaque compte lié y apparaît en <mark style="color:red;">rouge</mark> s'il est banni, en <mark style="color:purple;">violet</mark> s'il est réduit au silence, en <mark style="color:green;">vert</mark> sinon, avec le degré de soupçon :

* **Forte possibilité** : même adresse que celle qu'il utilise en ce moment ;
* **Simple possibilité** : une ancienne adresse en commun.

Clique sur un compte pour ouvrir son casier. `/comptes <joueur>` affiche la liste complète des comptes liés.

{% hint style="warning" %}
Une adresse partagée n'est pas une preuve : une famille, des colocataires ou un réseau public peuvent la partager. L'alerte sert à <mark style="color:red;">vérifier</mark>, pas à sanctionner d'office.
{% endhint %}

### <mark style="color:yellow;">Le foyer</mark> <a href="#foyer" id="foyer"></a>

Un joueur peut jouer avec un proche vivant sous le même toit s'il a prévenu la modération (R11). Le foyer sert à l'enregistrer : les comptes d'un même foyer ne déclenchent plus d'alerte entre eux.

Ouvre-le depuis le feu de camp du casier, ou depuis le bouton \[Plus d'infos] d'une alerte. Tu peux y ajouter un compte par son pseudo, ou en retirer un en cliquant sur sa tête. Si deux comptes ont déjà chacun un foyer, les ajouter l'un à l'autre réunit les deux foyers en un seul.

{% hint style="danger" %}
N'ajoute au foyer que des personnes <mark style="color:red;">réellement différentes</mark>, après vérification : un double compte placé dans un foyer n'est plus signalé.
{% endhint %}

## <mark style="color:yellow;">Rester discret</mark> <a href="#modes" id="modes"></a>

### <mark style="color:yellow;">Le mode AFK</mark> <a href="#afk" id="afk"></a>

`/afk` l'active ou le désactive. Pour les joueurs, tu as l'air déconnecté :

* tu disparais de la liste des joueurs, et tu n'es pas compté dans le nombre de joueurs connectés ;
* ton pseudo ne leur est pas proposé quand ils tapent un nom ;
* ils ne voient pas ton message de connexion ni de déconnexion ;
* un joueur qui t'écrit en privé lit « Ce joueur n'est pas connecté ».

Ton personnage reste pourtant visible dans le monde, et tu joues normalement.

Tu passes en mode AFK automatiquement à chaque connexion, et après <mark style="color:red;">5 minutes</mark> d'inactivité. Dans ce second cas, il se retire dès que tu bouges.

{% hint style="warning" %}
Le mode AFK ne te cache pas dans le chat public : si tu y écris, tout le monde te lit.
{% endhint %}

### <mark style="color:yellow;">Le mode spectateur</mark> <a href="#spectateur" id="spectateur"></a>

`/vanish` l'active ou le désactive. En plus du mode AFK, ton personnage devient invisible et tu passes en spectateur. Tu peux ouvrir les coffres sans bruit et regarder l'inventaire d'un joueur d'un clic droit, sans pouvoir rien y prendre.

En le quittant, tu retrouves ton mode de jeu habituel, même si le serveur a redémarré entre-temps.

<mark style="color:yellow;">**Raccourci**</mark> : une fois caché, accroupis-toi deux fois rapidement pour passer du mode AFK au mode spectateur, et inversement.

### <mark style="color:yellow;">Entre membres de l'équipe</mark> <a href="#equipe" id="equipe"></a>

Les membres de l'équipe continuent de se voir. Dans la liste des joueurs, <mark style="color:yellow;">\[A]</mark> signale un membre en mode AFK et <mark style="color:yellow;">\[S]</mark> un membre en mode spectateur. L'équipe est aussi prévenue quand l'un d'eux se connecte ou se déconnecte caché, entre en mode spectateur ou en sort, ou passe en AFK par inactivité.
