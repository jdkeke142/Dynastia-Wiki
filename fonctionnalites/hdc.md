# 📜 Hôtel des Contrats

L'Hôtel des Contrats est accessible via la commande <mark style="color:yellow;">`/hdc`</mark>. C'est un tableau d'annonces où tu peux passer commande d'une ressource : tu fixes le prix, et d'autres joueurs te la livrent contre paiement immédiat.

C'est l'inverse de l'[Hôtel des Ventes](hdv.md) : ici, tu ne vends pas ce que tu as, tu demandes ce qu'il te manque.

***

## <mark style="color:yellow;">Créer un contrat</mark>

<a href="#creer-un-contrat" id="creer-un-contrat"></a>

Depuis le tableau, clique sur « Créer un contrat ». Tu devras définir :

* **L'objet demandé** — glisse un exemplaire dans l'emplacement prévu. L'objet doit être intact, non renommé et non rempli (pas de shulker déjà pleine, par exemple).
* **L'unité** — soit **à l'item** (chaque objet compte pour 1), soit **à la shulker** (une shulker entièrement remplie de cet objet compte pour 1).
* **La quantité** — jusqu'à <mark style="color:red;">10 000 items</mark> ou <mark style="color:red;">100 shulkers</mark> selon l'unité choisie.
* **Le prix total** — c'est la somme que tu es prêt à payer pour l'ensemble de la commande. Le prix par unité est calculé automatiquement.
* **La durée** — de <mark style="color:red;">1 à 14 jours</mark>.

{% hint style="warning" %}
Une taxe de <mark style="color:red;">15%</mark> s'ajoute au prix total au moment de la publication. Cette taxe n'est jamais remboursée, même si tu annules le contrat.
{% endhint %}

Une fois tout réglé, clique sur « Publier le contrat ». L'intégralité du prix (+ taxe) est prélevée à ce moment-là : l'argent est mis de côté pour payer les livreurs.

Tu peux avoir jusqu'à <mark style="color:red;">2 contrats</mark> ouverts en même temps.

***

## <mark style="color:yellow;">Livrer un contrat</mark>

<a href="#livrer-un-contrat" id="livrer-un-contrat"></a>

Depuis le tableau, clique sur un contrat ouvert puis sur « Livrer ». Une fenêtre de dépôt s'ouvre :

* **À l'item** — dépose les objets correspondants dans la zone de dépôt.
* **À la shulker** — dépose des shulkers entièrement remplies de l'objet demandé. La shulker vidée t'est rendue.

Un bouton « Tout déposer » récupère automatiquement les objets compatibles depuis ton inventaire.

Clique sur « Livrer » pour valider. **Le paiement est immédiat** : tu reçois ta part directement, calculée proportionnellement au nombre d'unités livrées.

{% hint style="info" %}
Tu ne peux pas livrer ton propre contrat. Les adjoints non plus.
{% endhint %}

***

## <mark style="color:yellow;">Cycle de vie d'un contrat</mark>

<a href="#cycle-de-vie" id="cycle-de-vie"></a>

Un contrat passe par l'un de ces états :

* **En cours** — les livraisons sont acceptées.
* **Rempli** — toute la quantité a été livrée. Tous les livreurs sont prévenus, avec un récapitulatif de leur contribution.
* **Expiré** — le délai est écoulé sans que le contrat soit rempli.
* **Annulé** — tu l'as annulé toi-même avant la fin.

Quand un contrat expire ou est annulé, la part d'argent non encore versée aux livreurs t'est rendue automatiquement (dès que tu es connecté).

{% hint style="danger" %}
Après expiration ou annulation, tu as <mark style="color:red;">15 jours</mark> pour retirer les objets déjà livrés. Passé ce délai, ils sont définitivement supprimés.
{% endhint %}

***

## <mark style="color:yellow;">Gérer tes contrats</mark>

<a href="#gerer-tes-contrats" id="gerer-tes-contrats"></a>

Le bouton « Mes contrats » du tableau affiche tous tes contrats, filtrables par état. Chacun indique l'argent qu'il reste à verser aux livreurs, ce qu'il te reste à retirer et, s'il est terminé, la date limite pour le faire. Pour chacun, tu peux :

* **Retirer les livraisons** — récupérer les objets déjà livrés dans ton inventaire. Pour les contrats à la shulker, des shulkers vides sont prises depuis ta réserve (voir plus bas).
* **Voir les livreurs** — le classement de ceux qui t'ont livré, du plus gros au plus petit, avec pour chacun la quantité livrée, sa part de la commande, ce qu'il a gagné et sa dernière livraison.
* **Gérer tes adjoints** — voir la section suivante.
* **Copier le contrat** — créer un nouveau contrat identique (même objet, quantité et prix).
* **Annuler** — stoppe les livraisons. L'argent restant t'est rendu, mais pas la taxe.
* **Supprimer** — retire le contrat de ton historique (seulement quand il n'y a plus rien à retirer).

***

## <mark style="color:yellow;">Adjoints</mark>

<a href="#adjoints" id="adjoints"></a>

Tu peux nommer d'autres joueurs **adjoints** de ton contrat. Un adjoint peut retirer les livraisons à ta place — pratique si tu n'es pas souvent connecté.

Un adjoint **ne peut pas** annuler ou supprimer le contrat. Il peut se retirer de lui-même s'il le souhaite, et tu peux le révoquer à tout moment. Les deux parties sont prévenues par message.

Les contrats dont tu es adjoint apparaissent dans la section « Contrats confiés » du tableau.

***

## <mark style="color:yellow;">Réserve de shulkers</mark>

<a href="#reserve-de-shulkers" id="reserve-de-shulkers"></a>

Accessible depuis le tableau, la réserve est un espace de stockage personnel pour tes **shulkers vides**. Quand tu retires les livraisons d'un contrat à la shulker, les objets sont automatiquement rangés dans des shulkers prises depuis ta réserve.

Selon ton grade, ta réserve peut compter plusieurs pages.

Si ta réserve est vide, tu ne pourras pas retirer les livraisons d'un contrat à la shulker — pense à la remplir à l'avance.

***

## <mark style="color:yellow;">Le tableau</mark>

<a href="#le-tableau" id="le-tableau"></a>

Le tableau principal affiche tous les contrats ouverts. Tu peux les trier par :

* **Plus récents** — les derniers publiés en premier.
* **Mieux payés** — ceux qui rapportent le plus en premier.
* **Bientôt expirés** — ceux qui arrivent à échéance en premier.
* **Presque remplis** — ceux qui sont le plus avancés en premier.

Tu peux aussi filtrer par unité (item ou shulker), ou rechercher un objet précis par son nom.

Chaque contrat affiché montre l'objet demandé, le nom de l'auteur, le temps restant, la progression des livraisons, le prix par unité, le prix par pile et l'argent restant à gagner.

{% hint style="info" %}
Les contrats à moins de <mark style="color:red;">24 heures</mark> de l'échéance sont signalés en rouge.
{% endhint %}

***

## <mark style="color:yellow;">Commandes</mark>

<a href="#commandes" id="commandes"></a>

<mark style="color:yellow;">`/hdc`</mark> : Ouvrir le tableau des contrats.\
<mark style="color:yellow;">`/hdc help`</mark> : Afficher l'aide.
