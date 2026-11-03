# 🛠️ Guide de la modération

Ce guide s'adresse à l'équipe de modération. Il présente tous les outils à ta disposition : les sanctions, le casier, la détection des doubles comptes, les foyers et les modes de présence discrète.

{% hint style="info" %}
Le règlement s'applique à tous, équipe comprise (R8). Toute sanction est proportionnée aux faits et aux antécédents du joueur (R3), et tu ne traites jamais un cas qui te concerne personnellement (R5).
{% endhint %}

{% hint style="warning" %}
Tu ne peux sanctionner qu'un joueur dont le grade est <mark style="color:red;">strictement inférieur</mark> au tien. Tu ne peux donc pas sanctionner un autre membre de l'équipe de même rang ou de rang supérieur. Tu ne peux pas non plus te sanctionner toi-même.
{% endhint %}

## <mark style="color:yellow;">Les sanctions</mark> <a href="#sanctions" id="sanctions"></a>

Toutes les sanctions demandent un <mark style="color:red;">motif</mark>. Sans motif, la sanction est refusée. Elles fonctionnent aussi sur un joueur hors ligne, du moment qu'il s'est déjà connecté au serveur (sauf l'expulsion, qui vise forcément un joueur connecté).

### <mark style="color:yellow;">Avertir</mark> <a href="#avertir" id="avertir"></a>

<mark style="color:yellow;">`/warn <joueur> <motif>`</mark>

Le joueur reçoit un message dans son chat, avec ton nom et le motif, qui le prévient qu'il pourra être sanctionné si l'infraction se reproduit. L'avertissement n'a aucun effet sur le jeu : il est seulement inscrit au casier.

Pour retirer un avertissement : <mark style="color:yellow;">`/unwarn <joueur> <raison>`</mark>. Cela retire le <mark style="color:red;">dernier</mark> avertissement encore actif du joueur. Il reste visible au casier, marqué comme annulé.

### <mark style="color:yellow;">Expulser</mark> <a href="#expulser" id="expulser"></a>

<mark style="color:yellow;">`/kick <joueur> <motif>`</mark>

Le joueur doit être connecté. Il est déconnecté sur-le-champ, avec un écran qui affiche ton nom et le motif. Il peut se reconnecter aussitôt. L'expulsion est inscrite au casier.

### <mark style="color:yellow;">Réduire au silence</mark> <a href="#mute" id="mute"></a>

<mark style="color:yellow;">`/mute <joueur> <durée> <motif>`</mark>

Le joueur ne peut plus écrire dans le chat ni envoyer de messages privés. Il continue à jouer normalement. S'il est connecté, il est prévenu immédiatement (modérateur, motif, durée). Chaque fois qu'il essaie d'écrire, son message est bloqué et le serveur lui rappelle le motif et le temps restant.

Pour lui rendre la parole : <mark style="color:yellow;">`/unmute <joueur> <raison>`</mark>. S'il est connecté, il reçoit « Tu peux de nouveau parler ».

{% hint style="info" %}
Quand une réduction au silence arrive à son terme toute seule, le joueur ne reçoit <mark style="color:red;">aucun message</mark> : il peut simplement reparler.
{% endhint %}

### <mark style="color:yellow;">Bannir</mark> <a href="#ban" id="ban"></a>

<mark style="color:yellow;">`/ban <joueur> <durée> <motif>`</mark>

Le joueur est déconnecté immédiatement s'il est en ligne, et ne peut plus se connecter. À chaque tentative, il voit un écran avec ton nom, le motif, le temps restant et l'invitation à contester sur le Discord.

Pour lever un bannissement : <mark style="color:yellow;">`/unban <joueur> <raison>`</mark>.

{% hint style="warning" %}
Un joueur ne peut avoir qu'<mark style="color:red;">un seul</mark> bannissement et qu'<mark style="color:red;">une seule</mark> réduction au silence en cours. Si tu veux allonger ou raccourcir une sanction en cours, ne la refais pas : modifie sa durée depuis le [casier](#gerer).
{% endhint %}

### <mark style="color:yellow;">Écrire une durée</mark> <a href="#durees" id="durees"></a>

La durée est un nombre suivi d'une unité, sans espace :

| Unité | Signification | Exemple |
| --- | --- | --- |
| `s` | secondes | `30s` |
| `m` | minutes | `30m` |
| `h` | heures | `2h` |
| `d` | jours | `7d` |
| `w` | semaines | `2w` |
| `mo` | mois (30 jours) | `3mo` |
| `y` | années (365 jours) | `1y` |

{% hint style="danger" %}
<mark style="color:red;">`m` veut dire minutes</mark>, pas mois. `/ban Pseudo 3m Triche` bannit pour 3 minutes. Pour 3 mois, écris `3mo`.
{% endhint %}

On ne combine pas les unités : `1d12h` est refusé, écris `36h`.

Une réduction au silence ou un bannissement dure <mark style="color:red;">un an au plus</mark>.

### <mark style="color:yellow;">Après une sanction</mark> <a href="#apres" id="apres"></a>

Dès qu'une sanction est appliquée :

* tu reçois une confirmation avec un bouton <mark style="color:yellow;">\[Plus d'infos]</mark>. Survole-le pour voir le résumé (joueur, type, durée, motif, modérateur), clique-le pour ouvrir directement la sanction dans le casier. Ce bouton reste utilisable pendant <mark style="color:red;">12 heures</mark> ;
* les autres membres de l'équipe connectés reçoivent la même information, avec le même bouton.

### <mark style="color:yellow;">Les listes</mark> <a href="#listes" id="listes"></a>

* <mark style="color:yellow;">`/banlist`</mark> : tous les bannissements en cours, avec pour chacun le temps restant et le motif.
* <mark style="color:yellow;">`/mutelist`</mark> : toutes les réductions au silence en cours, de la même façon.

## <mark style="color:yellow;">Le casier</mark> <a href="#casier" id="casier"></a>

<mark style="color:yellow;">`/casier <joueur>`</mark> (ou <mark style="color:yellow;">`/history <joueur>`</mark>)

Le casier est l'historique complet des sanctions d'un joueur. Il est <mark style="color:red;">permanent</mark> : une sanction terminée ou levée y reste, marquée comme telle.

### <mark style="color:yellow;">La fenêtre</mark> <a href="#fenetre" id="fenetre"></a>

* **En haut**, la tête du joueur résume son casier.
* **Au centre**, une icône par sanction : une barrière pour un bannissement, un livre pour une réduction au silence, un papier pour un avertissement, des bottes pour une expulsion. Survole une icône pour voir le détail : date, motif, modérateur, durée, et les éventuelles modifications.
* **L'entonnoir** filtre par type de sanction : clic gauche pour le type suivant, clic droit pour le précédent.
* **Le feu de camp** ouvre le [foyer](#foyer) du joueur.
* **Les flèches** changent de page quand le casier est long.

La fenêtre se met à jour toute seule toutes les 30 secondes.

### <mark style="color:yellow;">Gérer une sanction</mark> <a href="#gerer" id="gerer"></a>

Clique sur une sanction pour ouvrir sa fenêtre de gestion. Trois actions :

* <mark style="color:yellow;">**Modifier la durée**</mark> (horloge) : redéfinit la <mark style="color:red;">durée totale</mark> de la sanction, comptée depuis le jour où elle a été donnée, pas depuis aujourd'hui. L'horloge affiche la durée totale actuelle et le temps restant. Ne concerne que les bannissements et réductions au silence encore en cours. Même limite que pour sanctionner : un an au plus.
* <mark style="color:yellow;">**Modifier le motif**</mark> (livre et plume) : réécrit la raison de la sanction.
* <mark style="color:yellow;">**Annuler la sanction**</mark> (colorant vert) : met fin à la sanction avant son terme. Elle reste au casier, marquée comme annulée.

Pour chaque modification ou annulation, tu dois écrire une <mark style="color:red;">raison</mark>. Elle est conservée dans l'historique de la sanction, avec ton nom.

{% hint style="info" %}
Une sanction terminée ou déjà annulée ne peut plus être modifiée.
{% endhint %}

## <mark style="color:yellow;">Les doubles comptes</mark> <a href="#doubles-comptes" id="doubles-comptes"></a>

Le serveur retient l'adresse depuis laquelle chaque compte se connecte. Deux comptes passés par la même adresse sont considérés comme <mark style="color:red;">liés</mark> pendant <mark style="color:red;">30 jours</mark>. Au-delà, l'adresse est oubliée.

### <mark style="color:yellow;">L'alerte à la connexion</mark> <a href="#alerte" id="alerte"></a>

Quand un joueur se connecte et qu'il a des comptes liés, tous les membres de l'équipe connectés reçoivent une alerte « ⚠ Double compte », accompagnée d'un petit son.

L'alerte liste jusqu'à <mark style="color:red;">4 comptes liés</mark> ; s'il y en a plus, elle indique combien d'autres. La couleur de chaque pseudo indique sa situation :

* <mark style="color:red;">**rouge**</mark> : banni ;
* <mark style="color:purple;">**violet**</mark> : réduit au silence ;
* <mark style="color:green;">**vert**</mark> : aucune sanction en cours.

À côté de chaque compte, le degré de soupçon :

* <mark style="color:red;">**Forte possibilité**</mark> : ce compte a la même adresse que celle qu'utilise le joueur en ce moment.
* <mark style="color:yellow;">**Simple possibilité**</mark> : les deux comptes ont une ancienne adresse en commun.

Survole un compte pour voir sa sanction en cours et la date où il a partagé l'adresse ; clique dessus pour ouvrir son casier. Le bouton <mark style="color:yellow;">\[Plus d'infos]</mark> de l'alerte ouvre le foyer du joueur. Ces boutons restent utilisables pendant 12 heures.

### <mark style="color:yellow;">Consulter les comptes liés</mark> <a href="#comptes" id="comptes"></a>

<mark style="color:yellow;">`/comptes <joueur>`</mark> (ou <mark style="color:yellow;">`/alts <joueur>`</mark>) liste <mark style="color:red;">tous</mark> les comptes liés au joueur, sans limite, avec le degré de soupçon et la date du partage d'adresse. Les comptes de son foyer n'y figurent pas.

{% hint style="warning" %}
Une adresse partagée n'est pas une preuve : frères et sœurs, colocataires, ou même un réseau public peuvent donner la même adresse à des joueurs différents. L'alerte sert à <mark style="color:red;">vérifier</mark>, pas à sanctionner d'office.
{% endhint %}

## <mark style="color:yellow;">Le foyer</mark> <a href="#foyer" id="foyer"></a>

Un joueur peut jouer avec un proche du même foyer, à condition d'avoir prévenu la modération (R11). Le foyer permet de l'enregistrer : on y range les comptes de <mark style="color:red;">personnes différentes</mark> qui partagent légitimement la même connexion.

Entre comptes d'un même foyer :

* <mark style="color:green;">aucune alerte</mark> de double compte ;
* ils n'apparaissent pas dans <mark style="color:yellow;">`/comptes`</mark> l'un pour l'autre ;

### <mark style="color:yellow;">Gérer un foyer</mark> <a href="#gerer-foyer" id="gerer-foyer"></a>

Ouvre le foyer depuis le feu de camp du casier, ou depuis le bouton \[Plus d'infos] d'une alerte. La fenêtre liste les comptes du foyer, avec pour chacun le membre de l'équipe qui l'a ajouté et la date.

* <mark style="color:yellow;">**Ajouter un compte**</mark> : saisis le pseudo du proche. Le compte doit s'être déjà connecté au serveur.
* <mark style="color:yellow;">**Retirer un compte**</mark> : clique sur sa tête, puis confirme. Les alertes reprennent entre eux.

{% hint style="info" %}
Les foyers se rejoignent : si tu ajoutes Julie au foyer de Paul, puis Léo au foyer de Julie, Paul, Julie et Léo forment un seul et même foyer.
{% endhint %}

{% hint style="danger" %}
N'ajoute au foyer que des personnes <mark style="color:red;">réellement différentes</mark>, après vérification. Un double compte placé dans un foyer échappe aux alertes.
{% endhint %}

## <mark style="color:yellow;">Les modes de présence</mark> <a href="#modes" id="modes"></a>

Deux modes te permettent d'être présent sans être sollicité, ou d'observer sans être vu. Un rappel s'affiche en permanence au-dessus de ta barre d'objets tant que l'un d'eux est actif.

### <mark style="color:yellow;">Le mode AFK</mark> <a href="#afk" id="afk"></a>

<mark style="color:yellow;">`/afk`</mark> l'active ou le désactive.

C'est le mode du quotidien, pour quand tu es occupé ou absent et que tu ne veux pas être attendu. En mode AFK :

* tu disparais de la <mark style="color:red;">liste des joueurs</mark> (touche Tab) et des suggestions de pseudo ;
* un joueur qui t'envoie un message privé lit « Ce joueur n'est pas connecté » ;
* tes messages de connexion et de déconnexion ne sont pas affichés aux joueurs ;
* ton personnage reste <mark style="color:red;">visible</mark> dans le monde, et tu joues normalement.

**Tu passes en mode AFK tout seul** :

* à chaque connexion ;
* après <mark style="color:red;">20 secondes</mark> d'inactivité. Dans ce cas, le mode se retire tout seul dès que tu bouges de nouveau. Les autres membres de l'équipe sont prévenus.

{% hint style="warning" %}
Le mode AFK ne te cache pas dans le chat public : si tu y écris, tout le monde voit ton message.
{% endhint %}

### <mark style="color:yellow;">Le mode spectateur</mark> <a href="#spectateur" id="spectateur"></a>

<mark style="color:yellow;">`/vanish`</mark> (ou <mark style="color:yellow;">`/v`</mark>) l'active ou le désactive.

C'est le mode d'observation. En plus de tout ce que fait le mode AFK :

* ton personnage devient <mark style="color:red;">invisible</mark> et tu passes en mode spectateur ;
* tu peux ouvrir les coffres <mark style="color:red;">sans bruit</mark>, en lecture seule : tu vois le contenu mais tu ne peux rien prendre ni déplacer ;
* un <mark style="color:yellow;">clic droit sur un joueur</mark> ouvre son inventaire, en direct et en lecture seule.

En quittant le mode spectateur, tu retrouves le mode de jeu que tu avais avant.

<mark style="color:yellow;">**Raccourci**</mark> : quand tu es déjà en mode AFK ou spectateur, <mark style="color:yellow;">accroupis-toi deux fois rapidement</mark> pour passer de l'un à l'autre.

Désactiver le mode spectateur avec <mark style="color:yellow;">`/vanish`</mark> te rend complètement visible. Si tu veux seulement redevenir visible dans le monde tout en restant hors de la liste des joueurs, utilise <mark style="color:yellow;">`/afk`</mark> : il te ramène en mode AFK.

### <mark style="color:yellow;">Ce que voit l'équipe</mark> <a href="#vue-equipe" id="vue-equipe"></a>

Les membres de l'équipe continuent de se voir entre eux, quel que soit le mode. Ils sont prévenus quand l'un d'eux :

* se connecte ou se déconnecte en étant caché, avec <mark style="color:green;">\[+]</mark> ou <mark style="color:red;">\[-]</mark> devant son pseudo ;
* passe en mode AFK par inactivité ;
* entre en mode spectateur ou en sort.
