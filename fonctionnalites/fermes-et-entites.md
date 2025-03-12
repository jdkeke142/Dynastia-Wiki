# ⚙️ Fermes et entités

Sur Dynastia, par ferme nous entendons toute construction ayant pour but d'automatiser la production de certains blocs/items par le biais de l'exploitation des mécaniques des entités et/ou des systèmes Redstone.\
\
Sur le serveur, les mécaniques des entités ont subit des <mark style="color:red;">certains changements</mark>. Ces modifications sur les entités, bien que non remarquables pour un joueur lambda, peuvent avoir une importance pour un joueur qui souhaite créer des fermes. Il est donc intéressant de <mark style="color:red;">prendre ces modifications en compte</mark> si ton but est d'en créer.

{% hint style="warning" %}
Nous tentons de nous rapprocher au maximum des mécaniques Vanilla, mais certaines concessions sont obligatoires pour garder des performances correctes, et donc, une expérience de jeu convenable sur le serveur.
{% endhint %}

Cette section du Wiki en elle-même ne prétend pas t'apprendre les répercussions des changements apportés sur les entités, nous nous contenterons dans ce guide de lister les valeurs changées.

{% hint style="info" %}
Si tu souhaites connaître les répercussions du changement de chaque valeur sur le comportement des entités, [ce guide](https://paper-chan.moe/paper-optimization/), en Anglais, le fait très bien. C'est d'ailleurs selon ce guide que les valeurs sont optimisées sur le serveur.
{% endhint %}

## <mark style="color:yellow;">Distance de simulation</mark>

La distance de simulation s'exprime en chunks. Sur le serveur cette valeur est définie à <mark style="color:red;">8 chunks</mark>.

Elle n'affecte pas uniquement le comportement des entités, mais également les mécanismes Redstone. En effet toute entité, toute construction se trouvant au delà de la distance de simulation par rapport à un joueur <mark style="color:red;">ne tickera pas du tout</mark>.

{% hint style="info" %}
Dire qu'un bloc ou une entité ne "tick pas" revient à dire qu'il ou elle est totalement inactif.
{% endhint %}

## <mark style="color:yellow;">Distances de spawn</mark> <a href="#distance-spawn" id="distance-spawn"></a>

| Type de configuration                          | Valeur                     |
| ---------------------------------------------- | -------------------------- |
| Rayon de spawn des entités                     | 7 chunks                   |
| Rayon de despawn des entités (soft)            | 32 blocs                   |
| Rayon de despawn des entités horizontal (hard) | 112 blocs                  |
| Rayon de despawn des entités vertical (hard)   | 128 blocs                  |
| Rayon d'activation des entités                 | 32 blocs pour les monstres |

{% hint style="warning" %}
Les rayons en blocs représentent une forme ellipsoïdale, et non une surface plane.
{% endhint %}

{% hint style="info" %}
Au delà du rayon d'activation, les entités ne tickent que 1/4 du temps.
{% endhint %}

## <mark style="color:yellow;">Limites de spawn</mark> <a href="#limites-spawn" id="limites-spawn"></a>

Pour le spawn naturel des entités, une limite par type d'entité est appliquée <mark style="color:red;">par joueur</mark>. Quand cette limite est atteinte, les entités du type en question ne spawnent plus naturellement.&#x20;

| Type d'entité                     | Limite |
| --------------------------------- | ------ |
| Monstres                          | 56     |
| Animaux                           | 10     |
| Animaux aquatiques                | 5      |
| Créatures aquatiques ambiantes    | 20     |
| Créatures aquatiques souterraines | 5      |
| Axolotls                          | 5      |

{% hint style="info" %}
Pour savoir plus précisément quelles entités appartiennent à quel type, consulte [le guide](https://www.paper-chan.moe/paper-optimization/#mob-categories) lié plus haut.
{% endhint %}

## <mark style="color:yellow;">Limites d'entités par zone (</mark><mark style="color:green;">totalement désactivées pour le moment</mark><mark style="color:yellow;">)</mark> <a href="#limites-zone" id="limites-zone"></a>

Le serveur possède une limite d'entités par zone. Des groupes d'entités sont définis, et en cas de dépassement de la limite pour le groupe d'entités dans la zone, alors le <mark style="color:red;">surplus est automatiquement tué</mark>. Toutes les limites sont effectives dans une zone de <mark style="color:red;">320x320 blocs incluant toute la hauteur</mark>.\
\
Ci-dessous les différents groupes d'entités et leurs limites associées :

<table data-full-width="false"><thead><tr><th>Entité(s) du groupe</th><th>Limite</th></tr></thead><tbody><tr><td>Items au sol</td><td>15K</td></tr><tr><td>Bâteaux</td><td>200</td></tr><tr><td>Wagonnets à entonnoir</td><td>120</td></tr><tr><td>Poules</td><td>100</td></tr><tr><td>Arpenteurs</td><td>100</td></tr><tr><td>Renards</td><td>100</td></tr><tr><td>Tortues</td><td>100</td></tr><tr><td>Moutons</td><td>100</td></tr><tr><td>Wagonnets, Wagonnets de stockage, Wagonnets motorisé, Wagonnets à TNT</td><td>96</td></tr><tr><td>Piglins zombifiés</td><td>80</td></tr><tr><td>Poissons tropicaux, Saumons, Morues, Poisson-globes</td><td>80</td></tr><tr><td>Villageois</td><td>80</td></tr><tr><td>Pillagers</td><td>80</td></tr><tr><td>Abeilles</td><td>60</td></tr><tr><td>Grenouilles</td><td>60</td></tr><tr><td>Shulkers</td><td>60</td></tr><tr><td>Cochons</td><td>35</td></tr><tr><td>Vaches</td><td>35</td></tr><tr><td>Champimeuh</td><td>35</td></tr><tr><td>Lapins</td><td>35</td></tr><tr><td>Sniffers</td><td>30</td></tr><tr><td>Armadillos</td><td>30</td></tr><tr><td>Chèvres</td><td>25</td></tr><tr><td>Pandas</td><td>25</td></tr><tr><td>Ours Polaires</td><td>25</td></tr><tr><td>Chevaux et les variants</td><td>20</td></tr><tr><td>Dromadaires</td><td>20</td></tr><tr><td>Allays</td><td>15</td></tr></tbody></table>

