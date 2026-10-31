# 🛡️ Claims

Un claim est une zone protégée qui t'appartient. À l'intérieur, personne ne peut construire, casser, ouvrir tes coffres ou interagir avec tes mécanismes sans ta permission. Les explosions, le feu et les dégâts causés par les créatures y sont également bloqués par défaut.

Tu peux créer autant de claims que tu veux, tant que tu as les fonds nécessaires.

{% hint style="info" %}
Les claims ne peuvent être créés que dans le [monde survie](monde-survie.md) et ses dimensions. Le spawn ne permet pas la création de claims.
{% endhint %}

## <mark style="color:yellow;">Créer un claim</mark> <a href="#creer" id="creer"></a>

### <mark style="color:yellow;">Obtenir l'outil</mark> <a href="#outil" id="outil"></a>

La commande <mark style="color:yellow;">`/claim tool`</mark> te donne une pelle en bois spéciale. C'est ton outil de sélection et de visualisation : en la tenant en main, tu verras les bordures des claims existants autour de toi grâce à des particules colorées.

* <mark style="color:green;">**Vert**</mark> : un claim dont tu es propriétaire.
* <mark style="color:blue;">**Bleu**</mark> : un claim dont tu es membre.
* <mark style="color:red;">**Rouge**</mark> : un claim qui ne t'appartient pas.

### <mark style="color:yellow;">Sélectionner la zone</mark> <a href="#selection" id="selection"></a>

Avec l'outil en main, fais un **clic gauche** sur un premier coin de ta future zone, puis un **clic droit** sur le coin opposé. Tu n'as besoin de sélectionner que deux coins au sol : le claim s'étendra automatiquement du ciel jusqu'à la bedrock.

Une fois les deux points posés, tu peux vérifier le coût de ta sélection avec <mark style="color:yellow;">`/claim selection cost`</mark>.

### <mark style="color:yellow;">Confirmer la création</mark> <a href="#confirmer" id="confirmer"></a>

Quand ta sélection te convient, utilise <mark style="color:yellow;">`/claim create`</mark> pour créer le claim. Tu peux aussi lui donner un nom directement : <mark style="color:yellow;">`/claim create Mon château`</mark>.

### <mark style="color:yellow;">Combien ça coûte ?</mark> <a href="#cout" id="cout"></a>

La création d'un claim coûte <mark style="color:red;">0,50 $</mark> par bloc de surface. La surface, c'est la longueur multipliée par la largeur de ta sélection.

Par exemple, un claim de 100 × 100 blocs = 10 000 blocs de surface, soit **5 000 $**.

{% hint style="info" %}
Si tu supprimes un claim, tu récupères l'intégralité de l'argent dépensé pour sa création.
{% endhint %}

{% hint style="warning" %}
Un claim ne peut pas dépasser <mark style="color:red;">6 250 blocs</mark> de côté.
{% endhint %}

## <mark style="color:yellow;">Gérer ton claim</mark> <a href="#gerer" id="gerer"></a>

### <mark style="color:yellow;">Le menu</mark> <a href="#menu" id="menu"></a>

Place-toi dans ton claim et utilise <mark style="color:yellow;">`/claim here`</mark> pour ouvrir le menu de gestion. Tu peux aussi l'ouvrir depuis n'importe où avec <mark style="color:yellow;">`/claim menu <nom>`</mark>.

Depuis ce menu, tu peux :

* Gérer les **membres** et leurs rôles.
* Configurer les **protections naturelles** (explosions, feu, etc.).
* Modifier les **droits d'action** de chaque rôle.
* Créer et gérer des **sous-claims**.
* **Renommer** ton claim ou changer son **icône**.
* **Supprimer** ton claim (et récupérer ton argent).

### <mark style="color:yellow;">Membres et rôles</mark> <a href="#roles" id="roles"></a>

Tu peux inviter d'autres joueurs dans ton claim et leur attribuer un rôle. Chaque rôle donne des droits différents, du plus restreint au plus large :

| Rôle | Ce qu'il peut faire par défaut |
|---|---|
| **Membre** | Construire, ouvrir les coffres, interagir avec les portes et mécanismes. |
| **Recruteur** | Tout ce qu'un Membre peut faire, et inviter de nouveaux membres. |
| **Gestionnaire** | Tout ce qu'un Recruteur peut faire, et gérer le rôle des membres existants. |
| **Admin** | Tout ce qu'un Gestionnaire peut faire, et configurer les protections et les sous-claims. |

Les joueurs qui ne sont pas membres de ton claim peuvent le traverser librement, mais ne peuvent ni construire, ni ouvrir tes coffres, ni interagir avec quoi que ce soit.

{% hint style="info" %}
Chaque rôle est entièrement personnalisable depuis le menu du claim. Tu peux, par exemple, autoriser les non-membres à ouvrir les portes tout en leur interdisant l'accès aux coffres.
{% endhint %}

### <mark style="color:yellow;">Protections naturelles</mark> <a href="#protections" id="protections"></a>

Par défaut, ton claim te protège contre la plupart des dangers :

* Les **explosions** de Creepers, de TNT, de Withers et de Ghasts ne détruisent rien.
* Le **feu** ne se déclenche pas et ne se propage pas.
* Les **Endermen** ne déplacent pas de blocs.
* Les **Zombies** ne cassent pas les portes.

Tu peux activer ou désactiver chacune de ces protections individuellement depuis le menu des flags naturels. Par exemple, si tu veux utiliser de la TNT dans ton claim, tu peux activer les dégâts de TNT.

{% hint style="warning" %}
Activer les dégâts de TNT ou de feu rend ton claim vulnérable aux attaques depuis l'extérieur. Fais-le en connaissance de cause.
{% endhint %}

## <mark style="color:yellow;">Sous-claims</mark> <a href="#sous-claims" id="sous-claims"></a>

Un sous-claim est une zone à l'intérieur d'un claim existant, avec ses propres règles. C'est utile pour créer des espaces aux droits différents au sein d'un même terrain.

Par exemple, tu peux avoir un grand claim pour ta base et créer un sous-claim autour de ta salle au trésor, où seul toi as accès aux coffres.

Pour créer un sous-claim, sélectionne la zone avec l'outil (comme pour un claim normal), puis utilise <mark style="color:yellow;">`/claim subclaim create <nom>`</mark>.

{% hint style="info" %}
Contrairement aux claims principaux, les sous-claims peuvent être étendus en hauteur avec <mark style="color:yellow;">`/claim selection expand`</mark>, ou rester limités à la zone sélectionnée. Par défaut, ils s'étendent du ciel à la bedrock.
{% endhint %}

## <mark style="color:yellow;">Commandes</mark> <a href="#commandes" id="commandes"></a>

<mark style="color:yellow;">`/claim tool`</mark> : Obtenir l'outil de sélection et de visualisation.\
<mark style="color:yellow;">`/claim create [nom]`</mark> : Créer un claim avec la sélection actuelle.\
<mark style="color:yellow;">`/claim here`</mark> : Ouvrir le menu du claim à ta position.\
<mark style="color:yellow;">`/claim menu <nom>`</mark> : Ouvrir le menu d'un claim par son nom.\
<mark style="color:yellow;">`/claim list`</mark> : Afficher la liste de tes claims.\
<mark style="color:yellow;">`/claim near <distance>`</mark> : Lister les claims aux alentours.\
<mark style="color:yellow;">`/claim selection cost`</mark> : Voir le prix de la sélection actuelle.\
<mark style="color:yellow;">`/claim selection remove`</mark> : Annuler ta sélection.\
<mark style="color:yellow;">`/claim redefine <nom>`</mark> : Redéfinir les bordures d'un claim existant.\
<mark style="color:yellow;">`/claim subclaim create <nom>`</mark> : Créer un sous-claim.\
<mark style="color:yellow;">`/claim help`</mark> : Afficher la liste des commandes en jeu.
