# 🎨 Mettre en forme le chat

Certains grades te permettent d'écrire en couleur et en style dans le chat.

Le principe est toujours le même : tu écris une **balise**, et le texte qui suit prend le style.

```
<red>Ce texte est rouge
```

La balise s'applique jusqu'à la fin de ton message. Pour l'arrêter avant, referme-la avec un `/`.

```
<red>Rouge</red> puis normal
```

## <mark style="color:yellow;">Toutes les balises</mark> <a href="#resume" id="resume"></a>

| Ce que ça fait | À écrire |
| -------------- | -------- |
| Colorer | `<gold>texte` |
| Gras | `<bold>texte` |
| Italique | `<italic>texte` |
| Souligné | `<underlined>texte` |
| Barré | `<strikethrough>texte` |
| Illisible | `<obfuscated>texte` |
| Dégradé | `<gradient:gold:red>texte</gradient>` |
| Arc-en-ciel | `<rainbow>texte</rainbow>` |
| Mélange de deux couleurs | `<transition:green:red:0.5>texte</transition>` |
| Drapeau | `<pride>texte</pride>` |
| Couleur de l'ombre | `<shadow:blue>texte` |
| Changer de police | `<font:uniform>texte</font>` |
| Aller à la ligne | `<newline>` ou `<br>` |
| Texte caché sous la souris | `<hover:show_text:'Coucou !'>texte</hover>` |

## <mark style="color:yellow;">Les couleurs</mark> <a href="#couleurs" id="couleurs"></a>

Tu as les 16 couleurs du jeu :

`black` · `dark_blue` · `dark_green` · `dark_aqua` · `dark_red` · `dark_purple` · `gold` · `gray` · `dark_gray` · `blue` · `green` · `aqua` · `light_purple` · `yellow` · `white`

```
<gold>Bonjour <aqua>tout le monde
```

## <mark style="color:yellow;">Les dégradés</mark> <a href="#degrades" id="degrades"></a>

Le dégradé passe d'une couleur à l'autre le long de ton texte. Tu peux en mettre autant que tu veux.

```
<gradient:gold:red>Salut tout le monde</gradient>
```

L'arc-en-ciel fait pareil, avec toutes les couleurs.

```
<rainbow>Salut tout le monde</rainbow>
```

La transition, elle, mélange deux couleurs et applique le résultat à tout le texte d'un coup. Le nombre à la fin choisit le point du mélange, entre `0` et `1`.

```
<transition:green:red:0.5>Salut tout le monde</transition>
```

## <mark style="color:yellow;">Les drapeaux</mark> <a href="#pride" id="pride"></a>

Sans rien préciser, tu obtiens le drapeau arc-en-ciel. Tu peux aussi en choisir un autre, comme `trans`.

```
<pride>Salut tout le monde</pride>
<pride:trans>Salut tout le monde</pride>
```

## <mark style="color:yellow;">Le texte caché</mark> <a href="#hover" id="hover"></a>

Ton message affiche un texte en plus quand on passe la souris dessus.

```
<hover:show_text:'Coucou !'>Passe ta souris ici</hover>
```

{% hint style="info" %}
N'oublie pas les apostrophes autour du texte caché, sinon la balise ne marche pas.
{% endhint %}
