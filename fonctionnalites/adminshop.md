# 🛒 AdminShop

L'AdminShop est un moyen principal de se faire de l'argent sur le serveur. Tu peux y vendre tes ressources, mais pas en acheter.

Il est étroitement lié aux fermes automatiques, car seulement les items considérés comme renouvelables de manière entièrement automatique (fermes AFK) y sont proposés.&#x20;

Chaque item présent dans celui-ci a une limite journalière par joueur, afin d'obliger à la diversification.

## <mark style="color:yellow;">Les PNJs du spawn</mark> <a href="#pnjs" id="pnjs"></a>

L'AdminShop est divisé en différentes catégories de shops. Chaque catégorie est accessible via un PNJ qui lui est propre, au spawn, dans la zone des stands de shops.

Dans ces PNJs tu pourras consulter le prix de vente, l'unité de vente ainsi que ton quota journalier de ventes pour chaque item.

## <mark style="color:yellow;">La vente rapide</mark> <a href="#vente-rapide" id="vente-rapide"></a>

La vente rapide te permet de vendre n'importe quel item vendable à l'AdminShop de manière plus rapide, sans devoir chercher à chaque fois le PNJ qui achète l'item en question.&#x20;

### <mark style="color:yellow;">Depuis le spawn</mark> <a href="#spawn" id="spawn"></a>

Un PNJ de vente rapide est accessible au spawn, dans la zone des stands de shops. Il a l'avantage de ne demander aucune taxe supplémentaire pour effectuer la vente rapide.

### <mark style="color:yellow;">Depuis n'importe où</mark> <a href="#nimporte-ou" id="nimporte-ou"></a>

La vente rapide est accessible depuis n'importe où sur le serveur via la commande <mark style="color:yellow;">`/qsell`</mark> , cependant, pour toute utilisation de la vente rapide via cette commande, une <mark style="color:red;">taxe de 10%</mark> sera déduite de tes ventes.

## <mark style="color:yellow;">Le SellHopper</mark> <a href="#sellhopper" id="sellhopper"></a>

Le SellHopper est un bloc prenant la forme d'un entonnoir. Il te permet d'automatiser la vente de tes fermes à l'AdminShop.  Il est achetable pour <mark style="color:red;">25,000$</mark> via la commande <mark style="color:yellow;">`/shopper`</mark> .

En entrée, il agit comme un entonnoir régulier. C'est à dire tu peux directement lier un conteneur quelconque au SellHopper. Tu peux également jeter les items sur le SellHopper, c'est d'ailleurs la manière la plus rapide de vendre, car elle n'est pas limitée par la vitesse de transit des items à travers les conteneurs.&#x20;

Lorsque l'item entre dans le SellHopper, si les conditions suivantes sont remplies:

* L'item est vendable à l'AdminShop.
* Tu n'as pas atteint ta limite journalière pour l'item en question.
* Tu n'as pas atteint la limite d'argent stockée dans le SellHopper de <mark style="color:red;">150,000$</mark>.

Alors la vente à l'AdminShop sera effectuée, avec une <mark style="color:red;">taxe de 10%</mark>. L'argent obtenu sera stocké dans le SellHopper et pourra être récupéré dans le menu de celui-ci. Une entrée de log concernant la vente sera également ajoutée dans ce même menu.

Si au moins l'une des conditions ci-dessus n'est pas remplie, alors l'item sera éjecté sous la forme d'un drop en dessous du SellHopper. Une entrée de log concernant l'échec de la vente sera également ajoutée dans le menu du SellHopper. \
\
Contrairement à l'entonnoir lambda, le SellHopper éjecte les items sous la forme de drops. Il est donc inutile de lier un conteneur directement sous le SellHopper, tu devras laisser au moins 1 bloc d'espacement sous le SellHopper et poser un entonnoir pour récupérer automatiquement les items éjectés.



