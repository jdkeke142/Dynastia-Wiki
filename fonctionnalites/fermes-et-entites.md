# ⚙️ Fermes et entités

Sur Dynastia, par ferme nous entendons toute construction ayant pour but d'automatiser la production de certains blocs/items par le biais de l'exploitation des mécaniques des entités et/ou des systèmes Redstone.\
\
Sur le serveur, les mécaniques des entités ont subit des <mark style="color:red;">changements relativement importants</mark>. Ces modifications sur les entités, bien que non remarquables pour un joueur lambda, le sont pour un joueur qui souhaite créer des fermes. Il est donc important de <mark style="color:red;">prendre ces modifications en compte</mark> si ton but est d'en créer.

{% hint style="warning" %}
Nous tentons de nous rapprocher au maximum des mécaniques Vanilla, mais certaines concessions sont obligatoires pour garder des performances correctes, et donc, une expérience de jeu convenable sur le serveur.
{% endhint %}

Cette section du Wiki en elle-même ne prétend pas t'apprendre les répercussions des changements apportés sur les entités, nous nous contenterons dans ce guide de lister les valeurs changées.

{% hint style="info" %}
Si tu souhaites connaître les répercussions du changement de chaque valeur sur le comportement des entités, [ce guide](https://paper-chan.moe/paper-optimization/), en Anglais, le fait très bien. C'est d'ailleurs selon ce guide que les valeurs sont optimisées sur le serveur.
{% endhint %}

## <mark style="color:yellow;">Distance de simulation</mark>

La distance de simulation s'exprime en chunks. Sur le serveur cette valeur est définie à <mark style="color:red;">6 chunks</mark>.

Elle n'affecte pas uniquement le comportement des entités, mais également les mécanismes Redstone. En effet toute entité, toute construction se trouvant au delà de la distance de simulation par rapport à un joueur <mark style="color:red;">ne tickera pas du tout</mark>.

{% hint style="info" %}
Dire qu'un bloc ou une entité ne "tick pas" revient à dire qu'il ou elle est totalement inactif.
{% endhint %}

## <mark style="color:yellow;">Distances de spawn</mark> <a href="#distance-spawn" id="distance-spawn"></a>

| Type de configuration               | Valeur                                          |
| ----------------------------------- | ----------------------------------------------- |
| Rayon de spawn des entités          | 5 chunks                                        |
| Rayon de despawn des entités (soft) | 32 blocs                                        |
| Rayon de despawn des entités (hard) | 128 blocs pour les monstres et 80 pour le reste |
| Rayon d'activation des entités      | 32 blocs                                        |

{% hint style="warning" %}
Les distances en blocs sont des sphères, et non des surfaces planes.
{% endhint %}

{% hint style="info" %}
Au delà du rayon d'activation, les entités ne tickent que 1/4 du temps.
{% endhint %}

## <mark style="color:yellow;">Limites de spawn</mark> <a href="#limites-spawn" id="limites-spawn"></a>

Pour le spawn naturel des entités, une limite par type d'entité est appliquée <mark style="color:red;">par joueur</mark>. Quand cette limite est atteinte, les entités du type en question ne spawnent plus naturellement.&#x20;

| Type d'entité                     | Limite |
| --------------------------------- | ------ |
| Monstres                          | 35     |
| Animaux                           | 5      |
| Animaux aquatiques                | 5      |
| Créatures aquatiques ambiantes    | 10     |
| Créatures aquatiques souterraines | 5      |
| Axolotls                          | 3      |

{% hint style="info" %}
Pour savoir plus précisément quelles entités appartiennent à quel type, consulte [le guide](https://www.paper-chan.moe/paper-optimization/#mob-categories) lié plus haut.
{% endhint %}

## <mark style="color:yellow;">Plage d'activation dynamique des entités</mark> <a href="#dear" id="dear"></a>

Le serveur bénéficie d'une optimisation nommée "_Plage d'activation dynamique des entités_". Cela limite la fréquence à laquelle une entité décide de faire quelque chose en fonction de la distance qui la sépare d'un joueur. Les entités concernées par cette optimisation sont celles avec un "cerveau" (qui ont une notion de mémoire) et sont les suivantes :

* Villageois
* Axolotls
* Hoglin
* Piglins zombifiés
* Chèvres
* Grenouilles

Pour ces entités, la fréquence de tick du cerveau en fonction de la distance est la suivante :\


| Distance du joueur | Fréquence de tick |
| ------------------ | ----------------- |
| 16 blocs ou moins  | 1/1               |
| 22 blocs           | 1/2               |
| 27 blocs           | 1/3               |
| 32 blocs           | 1/4               |
| 45 blocs           | 1/8               |
| 64 blocs           | 1/16              |
| 71 blocs ou plus   | 1/20              |

{% hint style="warning" %}
La distance en blocs est une sphère, et non une surface plane.
{% endhint %}

{% hint style="info" %}
Aucune mention à cette optimisation ne figure dans le guide lié plus haut, en effet cette optimisation est propre à un [Fork](https://fr.wikipedia.org/wiki/Fork\_\(d%C3%A9veloppement\_logiciel\)) plus spécifique du programme de serveur, que nous utilisons.
{% endhint %}

## <mark style="color:yellow;">Limites d'entités par zone</mark> <a href="#limites-zone" id="limites-zone"></a>

Le serveur possède une limite d'entités par zone. Des groupes d'entités sont définis, et en cas de dépassement de la limite pour le groupe d'entités dans la zone, alors le <mark style="color:red;">surplus est automatiquement tué</mark>. Toutes les limites sont effectives dans une zone de <mark style="color:red;">320x320 blocs incluant toute la hauteur</mark>.\
\
Ci-dessous les différents groupes d'entités et leurs limites associées :

<table data-full-width="false"><thead><tr><th>Groupe</th><th>Limite</th><th data-type="checkbox">"Pur"</th></tr></thead><tbody><tr><td>Items au sol</td><td>15K</td><td>false</td></tr><tr><td>Bâteaux</td><td>200</td><td>false</td></tr><tr><td>Wagonnets à entonnoir</td><td>120</td><td>false</td></tr><tr><td>Autres wagonnets</td><td>96</td><td>false</td></tr><tr><td>Piglins zombifiés</td><td>80</td><td>false</td></tr><tr><td>Poissons tropicaux, Saumons, Morues, Poisson-globes</td><td>80</td><td>false</td></tr><tr><td>Allays</td><td>15</td><td>false</td></tr><tr><td>Pillagers</td><td>80</td><td>false</td></tr><tr><td>Sniffers, Armadillos</td><td>30</td><td>true</td></tr><tr><td>Shulkers, Abeilles, Grenouilles</td><td>60</td><td>true</td></tr><tr><td>Moutons, Poules, Arpenteurs, Renards, Tortues</td><td>100</td><td>true</td></tr><tr><td>Cochons, Lapins, Vaches, Champimeuh</td><td>35</td><td>true</td></tr><tr><td>Villageois</td><td>80</td><td>false</td></tr><tr><td>Chevaux et les variants, Dromadaires</td><td>20</td><td>true</td></tr><tr><td>Chèvres, Pandas, Ours Polaires</td><td>25</td><td>true</td></tr></tbody></table>

{% hint style="warning" %}
Un type est "_pur_" quand la limite est **par** type d'entité à l'échelle d'un groupe. Dans le cas échéant, tous les types d'entités du groupe partagent la même limite.
{% endhint %}

{% hint style="warning" %}
Chaque ligne du tableau est un groupe, quoi qu'il advienne, les limites ne sont jamais partagées entre différents groupes.
{% endhint %}

