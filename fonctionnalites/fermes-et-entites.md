# ⚙️ Fermes et entités

Sur Dynastia, par ferme nous entendons toute construction ayant pour but d'automatiser la production de certains blocs/items par le biais de l'exploitation des mécaniques des entités et/ou des systèmes Redstone.\
\
Sur le serveur, les mécaniques des entités ont subit des <mark style="color:red;">changements relativement importants</mark>. Ces modifications sur les entités, bien que non remarquables pour un joueur lambda, le sont pour un joueur qui souhaite créer des fermes. Il est donc important de <mark style="color:red;">prendre ces modifications en compte</mark> si ton but est d'en créer.

{% hint style="warning" %}
Nous tentons de nous rapprocher au maximum des mécaniques Vanilla, mais certaines concessions sont obligatoires pour garder des performances correctes, et donc, une expérience de jeu convenable sur le serveur.
{% endhint %}

Cette section du Wiki en elle-même ne prétend pas t'apprendre les répercussions des changements apportés sur les entités, nous nous contenterons dans ce guide de lister les valeurs changées.

{% hint style="info" %}
Si tu souhaites connaître les répercussions du changement de chaque valeur sur le comportement des entités, [ce guide](https://paper-chan.moe/paper-optimization/), en Anglais, le fait excellemment bien. C'est d'ailleurs selon ce guide que les valeurs sont optimisées sur le serveur.
{% endhint %}

## <mark style="color:yellow;">Distance de simulation</mark>

La distance de simulation s'exprime en chunks. Sur le serveur cette valeur est définie à <mark style="color:red;">6 chunks</mark>.

Elle n'affecte pas uniquement le comportement des entités, mais également les mécanismes Redstone. En effet toute entité, toute construction se trouvant au delà de la distance de simulation par rapport à un joueur <mark style="color:red;">ne tickera pas du tout</mark>.

## <mark style="color:yellow;">Distances de spawn</mark> <a href="#distance-spawn" id="distance-spawn"></a>

| Type de configuration               | Valeur                                    | Type de valeur             |
| ----------------------------------- | ----------------------------------------- | -------------------------- |
| Rayon de spawn des entités          | 5                                         | Nombre de chunks           |
| Rayon de despawn des entités (soft) | 32                                        | Surface sphérique en blocs |
| Rayon de despawn des entités (hard) | 128 pour les monstres et 80 pour le reste | Surface sphérique en blocs |
| Rayon d'activation des entités      | 32                                        | Surface sphérique en blocs |

{% hint style="info" %}
Au delà du rayon d'activation, les entités ne tickent que 1/4 du temps.
{% endhint %}

## <mark style="color:yellow;">Limites de spawn</mark> <a href="#limites-spawn" id="limites-spawn"></a>

Pour le spawn naturel des entités, une limite par type d'entité est appliquée par joueur. Quand cette limite est atteinte, les entités du type en question ne spawnent plus naturellement.&#x20;

<table><thead><tr><th>Type d'entité</th><th data-type="number">Limite par joueur</th></tr></thead><tbody><tr><td>Monstres</td><td>35</td></tr><tr><td>Animaux</td><td>5</td></tr><tr><td>Animaux aquatiques</td><td>5</td></tr><tr><td>Créatures aquatiques ambiantes</td><td>10</td></tr><tr><td>Créatures aquatiques souterraines</td><td>5</td></tr><tr><td>Axolotls </td><td>3</td></tr></tbody></table>

{% hint style="info" %}
Pour savoir plus précisément quelles entités appartiennent à quel type, consulte le guide lié plus haut.
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


| Distance du joueur | Fréquence de tick | Expression de la distance  |
| ------------------ | ----------------- | -------------------------- |
| 16 ou moins        | 1/1               | Surface sphérique en blocs |
| 22                 | 1/2               | Surface sphérique en blocs |
| 27                 | 1/3               | Surface sphérique en blocs |
| 32                 | 1/4               | Surface sphérique en blocs |
| 45                 | 1/8               | Surface sphérique en blocs |
| 64                 | 1/16              | Surface sphérique en blocs |
| 71 ou plus         | 1/20              | Surface sphérique en blocs |

{% hint style="info" %}
Aucune mention à cette optimisation ne figure dans le guide lié plus haut, en effet cette optimisation est propre à un [Fork](https://fr.wikipedia.org/wiki/Fork\_\(d%C3%A9veloppement\_logiciel\)) plus spécifique du programme de serveur, que nous utilisons.
{% endhint %}

## <mark style="color:yellow;">Limites d'entités par zone</mark> <a href="#limites-zone" id="limites-zone"></a>

Le serveur possède une limite d'entités par zone. Des groupes d'entités sont définis, et en cas de dépassement de la limite pour le groupe d'entités dans la zone, alors le <mark style="color:red;">surplus est automatiquement tué</mark>.\
\
Ci-dessous les différents groupes d'entités et leurs limites associées :

<table><thead><tr><th>Entités du groupe</th><th data-type="number">Nombre maximum</th><th data-type="checkbox">Type "pur"</th><th>Zone</th></tr></thead><tbody><tr><td>Items au sol</td><td>15000</td><td>false</td><td>320x320 blocs</td></tr><tr><td>Bâteaux</td><td>200</td><td>false</td><td>320x320 blocs</td></tr><tr><td>Wagonnets à entonnoir</td><td>120</td><td>false</td><td>320x320 blocs</td></tr><tr><td>Autres wagonnets</td><td>96</td><td>false</td><td>320x320 blocs</td></tr><tr><td>Piglins zombifiés</td><td>80</td><td>false</td><td>320x320 blocs</td></tr><tr><td>Poissons tropicaux, Saumons, Morues, Poisson-globes</td><td>80</td><td>false</td><td>320x320 blocs</td></tr><tr><td>Allays</td><td>15</td><td>false</td><td>320x320 blocs</td></tr><tr><td>Pillagers</td><td>80</td><td>false</td><td>320x320 blocs</td></tr><tr><td>Sniffers, Armadillos</td><td>30</td><td>true</td><td>320x320 blocs</td></tr><tr><td>Shulkers, Abeilles, Grenouilles</td><td>60</td><td>true</td><td>320x320 blocs</td></tr><tr><td>Moutons, Poules, Arpenteurs, Renards, Tortues</td><td>100</td><td>true</td><td>320x320 blocs</td></tr><tr><td>Cochons, Lapins, Vaches, Champimeuh</td><td>35</td><td>true</td><td>320x320 blocs</td></tr><tr><td>Villageois</td><td>80</td><td>false</td><td>320x320 blocs</td></tr><tr><td>Chevaux et les variants, Dromadaires</td><td>20</td><td>true</td><td>320x320 blocs</td></tr><tr><td>Chèvres, Pandas, Ours Polaires</td><td>25</td><td>true</td><td>320x320 blocs</td></tr></tbody></table>

{% hint style="warning" %}
Un type est "_pur_" quand la limite est **par** type entité présente dans le groupe. Dans le cas échéant, tous les types d'entités du groupe partagent la même limite.
{% endhint %}
