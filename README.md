**WORKSHOP CSS**

**SUJET**

[**Consignes de
travail**](https://moodle.cesi.fr/pluginfile.php/23045/mod_resource/content/6/co/_3_-_Prosit_CSS.html)

Le but de ce workshop est de reprendre le site web réalisé dans le
prosit précédent, via la corbeille d\'exercices, et de le modifier afin
d\'appliquer des styles graphiques en utilisant le CSS.

Si vous n\'avez pas eu le temps de finaliser cette réalisation, vous
pouvez vous appuyer sur la correction.

 

[**Énoncé**](https://moodle.cesi.fr/pluginfile.php/23045/mod_resource/content/6/co/_3_-_Prosit_CSS.html)

**INTRODUCTION**

**Structure des dossiers**

En reprenant votre travail de la corbeille précédente (HTML), vous devez
avoir la structure suivante et nom de ressources suivants ou s\'y
rapprochant :

www

  index.html

  a-propos.html

  avis.html

  connexion.html

  contact.html

  index.html

  inscription.html

  +images

    logo.png

 

**MISE EN PLACE**

**Création de la feuille de style**

La première étape va consister à créer la feuille de style.

Pour cela vous allez créer à la racine de votre site un dossier
« assets » puis y ajouter un fichier style.css

 

**Ajout de la feuille de style**

Editez la page d\'accueil de votre site (fichier index.html) et ajouter
la définition suivante dans le header de la page (avant la fermeture de
la balise \<head\>)

CTRL+C pour copier, CTRL+V pour coller

1

\<link rel=\"stylesheet\" href=\"assets/style.css\"\>

 

Faites la même chose pour toutes les pages de votre site.

 

► Généralement une seule feuille de style est réalisée pour l\'entièreté
du site Web. Il peut toutefois y avoir des variantes, notamment pour
appliquer des thèmes visuels différents

 

*Q1. Quelles sont les 3 méthodes qui permettent d\'ajouter des
déclarations CSS à un document HTML ?*

 

**Vérification du bon fonctionnement**

Ouvrez le fichier style.css avec votre éditeur préféré.

Ajoutez la déclaration suivante, qui va simplement provoquer de changer
la couleur de fond de tout le site en gris clair :

CTRL+C pour copier, CTRL+V pour coller

1

body

2

{

3

background-color: \#f3f3f3;

4

font-family: Helvetica;

5

}

 

► Dans cette exemple, un code hexadécimal est utilisé pour définir la
couleur. Cette propriété accepte également de spécifier entre autres le
nom de couleur (par exemple « red ») ou un code rgb/rgba. Plus
d\'informations
ici : <https://developer.mozilla.org/fr/docs/Web/CSS/background-color>

    La seconde propriété permet d\'appliquer une police différente de
celle par défaut à tout le document.

 

Enregistrez le fichier et rechargez votre page pour voir la modification
apparaître.

Si rien ne se passe, assurez-vous que le chemin pointant vers votre
fichier css est correct.

Attention la couleur choisie est assez claire, en fonction de la
définition de votre écran elle pourrait apparaître différemment.
N\'hésitez pas à la changer.

 

► Il pourra parfois arriver que rien ne se passe suite à des
modifications apportées à votre fichier css. Cela peut provenir du cache
de votre navigateur, qui conserve l\'ancienne version du fichier. Pour
remédier à ce problème vous pouvez rafraîchir et vider le cache de votre
navigateur en utilisant les méthodes citées
ici : <https://navio.fr/comment-rafraichir-votre-navigateur-web-et-vider-le-cache/>

 

**RÉALISATION**

**Utilisation des outils de développement**

Vous allez pouvoir commencer à effectuer vos modifications de style.

Bien que celles-ci se définissent dans le fichier css, vous pouvez en
amont à but de tests faire des modifications sur la page en cours sans
avoir d\'impact sur votre fichier source. Bien sûr ces modifications
seront perdues au prochain chargement de la page.

Pour cela vous pouvez utiliser les outils de développement qui sont
disponibles dans chaque navigateur. L\'exemple ci-après représente celui
de Google Chrome mais pouvez utiliser celui d\'un autre navigateur, les
informations délivrées seront relativement identiques.

Pour ouvrir positionnez-vous sur la page de votre site puis appuyez sur
F12 (sous Windows) ou cliquez sur l\'icone des 3 points en haut à droite
du navigateur puis sélectionnez « Plus d\'outils \> Outils de
développement ». Vous devriez voir apparaître la fenêtre suivante :

![](media/image1.png){width="4.90625in" height="2.1145767716535433in"}

1.  La partie à gauche représente toute l\'arborescence HTML.

2.  La partie à droite représente toutes les définitions CSS qui sont
    appliquées à la partie sélectionné à gauche.

3.  Il s\'agit ici du nom de la feuille de style qui est concernée par
    cette définition, et la ligne à partir de laquelle commence la
    déclaration. Les définitions par défaut fournies par le navigateur
    sont nommées « user agent stylesheet »

4.  La partie en bas représente la branche sélectionnée

Vous pouvez ensuite modifier, supprimer ou ajouter des définitions CSS
(et du code HTML). Cela permet de faire quelques tests au préalable pour
voir le rendu avant de les faire dans le fichier source.

Vous pouvez par exemple modifier la couleur du background en mettant
« red » à la place du code en hexadécimal.

 

**Partie 1 - Header**

La première modification visuelle va consister à modifier le header de
votre site.

 

► Attention à ne pas confondre le header du contenu de la page,
représenté par la balise sémantique \<header\>, avec la
balise \<head\> de votre fichier HTML qui contient les informations non
visibles directement par le client (à part le titre et les icones) mais
qui servent au référencement et l\'inclusions de fichiers css.

 

Le principe va consister dans la partie \<header\> à :

-   supprimer les balises obsolètes \<center\> pour les remplacer par
    une définition CSS équivalente au moyen d\'une classe ;

-   retirer les balises \<hr\> permettant à l\'origine de tracer des
    lignes horizontales ;

-   retirer les sauts de ligne pour les remplacer par des marges
    intérieures ou extérieures.

 Ouvrez l\'une des pages de votre site, par exemple index.html, dans
votre éditeur de texte.

Repérez la partie contenant le header. Dans la correction précédente le
contenu était le suivant :

CTRL+C pour copier, CTRL+V pour coller

1

\<header\>

2

\<div\>\<center\>\<img src=\"./images/logo-lbp-header.png\"
alt=\"Lebonplan - Le meilleur site d\'annonces en
ligne\"\>\</center\>\</div\>

3

\<br\>

4

\<hr\>

5

\<nav\>Accueil&nbsp;\|&nbsp;\<a href=\"a-propos.html\"\>A
propos\</a\>&nbsp;\|&nbsp;\<a
href=\"inscription.html\"\>Inscription\</a\>&nbsp;\|&nbsp;\<a
href=\"connexion.html\"\>Connexion\</a\>&nbsp;\|&nbsp;\<a
href=\"avis.html\"\>Avis\</a\>&nbsp;\|&nbsp;\<a
href=\"contact.html\"\>Contact\</a\>\</nav\>

6

\<hr\>

7

\</header\>

 

L\'idée est ainsi de modifier votre fichier HTML, et de créer les
définitions CSS qui vont permettent de transformer votre header pour
qu\'il ressemble à celui-ci :

![](media/image2.png){width="6.3in" height="1.00625in"}

Pour cela vous devez donc, en plus des modifications à faire au
préalable dans le HTML :

-   Créer une classe « .text-center » dans votre fichier css puis
    l\'appliquer dans une balise HTML afin de centrer l\'image

-   Créer une classe « .navbar » à appliquer à la balise \<nav\> qui
    permettra :

    1.  d\'appliquer une marge interne de 10px en haut et en bas, et de
        15px sur les côtés ;

    2.  de mettre la couleur de fond du bandeau de navigation en noir ;

    3.  de mettre la couleur du texte en blanc ;

    4.  d\'appliquer la police de caractères « Century Gothic ».

-   Ajouter une définition pour les liens de cette barre de navigation
    afin :

    1.  de mettre la couleur des liens en blanc ;

    2.  de supprimer le soulignement sous les liens ;

    3.  de faire apparaître les soulignements au passage de la souris
        (via une pseudo-classe) et les mettre en gras ;

    4.  de mettre le texte en gras et orange pour la page active
        (utiliser un élément \<span\> couplé à un classe).

 

*Q2. Quels sont les différents type de sélecteurs ?*

 

► Vous pouvez cibler plus particulièrement un élément pour appliquer une
classe. Par exemple au lieu de créer seulement la classe .navbar, vous
pouvez décider de ne l\'appliquer qu\'à des éléments positionnés sous
les balises \<header\> : header .navbar{ \... }

► Le nommage des classes est important pour la clarté et la
compréhension ! Veuillez à utiliser des termes anglophones et en lien
avec la définition css. Pour le nommage des classes, tout se fait en
minuscule, un tiret en guise de séparateur pour les noms composés que ce
soit un bloc, un élément ou un modificateur.

► N\'hésitez pas à commenter votre code CSS en utilisant la syntaxe /\*
\*/ pour que vous, ou ceux qui reprendront votre code, soient capable de
tout comprendre.

 

*Q3. Comment sont gérées les priorités dans des déclarations CSS ?*

 

Une fois que vous êtes satisfait de vos modifications du header, vous
pouvez les appliquer à chacune de vos pages HTML.

 

**Partie 2 - Footer**

La seconde modification qui concerne tout le site est celle du footer.

Vous allez devoir ici retirer les balises obsolètes ou non appropriées
(saut de ligne, ligne horizontale\...) pour le remplacer par des
définitions CSS afin d\'avoir la représentation suivante :

-   la couleur de fond en noir ;

-   la couleur du texte en blanc et italique ;

-   une marge externe haute de 50px ;

-   une taille de police égale à 0.8em

 

Q4. Quelles sont les unités de mesure existantes pour définir la taille
d\'un texte ? Lesquels privilégier ?

 

 

**Partie 3 - Page d\'accueil**

Appliquez les modifications suivantes à votre page d\'accueil
(modification des balises ou attributs HTML + déclarations CSS) :

-   dans la partie « Catégories » changez la disposition de la liste
    (vous devrez créer une classe spécifique à appliquer à cette liste )
    afin de :

    -   supprimer les bullets ;

    -   mettre les éléments côte-à-côte ;

    -   ajouter un séparateur ( « - ») pour chaque élément de la liste
        sauf pour le dernier. Pour cela vous pouvez utiliser des
        pseudo-classes ;

-   dans la partie « Derniers articles ajoutés » modélisez le tableau
    afin d\'avoir :

    -   une entête en noir avec du texte blanc ;

    -   pas de bordure ;

    -   une ligne sur deux dans une autre couleur en utilisant une
        pseudo-classe.

 

Vous devriez avoir une page ressemblant à ça :

![](media/image3.png){width="6.3in" height="3.1819444444444445in"}

 

**Partie 4 - A propos**

Modifiez la page a-propos.html afin créez des définitions CSS permettant
d\'obtenir la représentation suivante :

![](media/image4.png){width="5.052083333333333in"
height="4.3877165354330705in"}

Vous devez ainsi :

-   supprimer les balises obsolètes et/ou les remplacer par des
    définitions CSS équivalentes ;

-   créer les classes et les ajouter dans le fichier HTML afin de
    positionner les blocs côte à côte ;

 

*Q5. Quels sont les différentes méthodes permettant de positionner des
blocs ?*

 

 

**Partie 5 - Formulaires**

Modifiez les autres pages contenant des formulaires (inscription.html,
connexion.html, avis.html et contact.html) pour moderniser les champs et
les boutons :

-   retirez les bordures des champs de saisie, ajoutez des marges
    internes et des bords arrondis ;

-   faire de même avec les listes déroulantes ;

-   enlevez la possibilité de redimensionner le champs texte ;

-   modifiez les boutons de soumission de formulaire et de
    réinitialisation en appliquant deux styles pour les différencier.

Un exemple de rendu pour la page avis.html pourrait être celui-ci :

![](media/image5.png){width="6.3in" height="3.859722222222222in"}

 

**Partie 6 - Responsive Web Design**

► La consultation de sites Internet se fait majoritairement aujourd\'hui
en utilisant un smartphone. Ceux-ci ont une résolution et/ou une taille
d\'affichage inférieure à celle d\'un ordinateur de bureau, il faut donc
que le site consulté soit capable de s\'adapter à ces environnement
hétérogènes. Le RWD, grâce au CSS3, permet de s\'affranchir du
développement de plusieurs versions d\'un même site Internet afin qu\'il
soit consultable sur différents équipements.

 

*Q6. Quelle syntaxe permet de définir des propriétés CSS différentes en
fonction du type d\'équipement et de sa résolution ?*

 

 

*Q7. Quels sont les différents type de média ?*

 

 

*Q8. Quels sont les seuils de déclenchement approximatifs pour chaque
type d\'équipement (smartphone, tablette, ordinateur de bureau\...) ?*

 

 

Si vous réduisez la taille de la fenêtre de votre navigateur, vous allez
vite vous rendre compte que les éléments de votre site vont se
superposer, se chevaucher voir disparaître par manque de place. La
taille des polices de caractères peut également ne plus être adaptée.

La prochaine étape va consister à modifier votre site en ajoutant des
règles de média pour qu\'il puisse correctement s\'afficher quel que
soit la résolution de l\'écran du client.

 

► Afin de simuler la résolution d\'un équipement, vous pouvez vous
appuyez sur la fonctionnalité de simulation des équipements intégrée aux
outils de développement de Chrome. Il suffit d\'activer l\'Inspecteur
d\'élément de Google Chrome de la façon habituelle puis de cliquer sur
le bouton \'*Toggle device mode*\" **,** juste à côté du
bouton *\"Elements\"* :

![](media/image6.png){width="6.3in" height="3.1694444444444443in"}

1.  Liste déroulante du choix de l\'équipement. De nombreux
    périphériques sont disponibles, la résolution change
    automatiquement.

2.  Choix de la résolution en pixel CSS

3.  Sélection du pixel ratio

4.  Sélection de la vitesse de connexion. Cette option permet de simuler
    des vitesses de connexion généralement plus faibles afin de tester
    la rapidité d\'affichage. Il est également possible de tester ses
    pages en mode hors ligne.

5.  Sélection de l\'orientation de l\'affichage (portrait ou paysage)

6.  Menu des options, il est conseillé d\'activer les paramètres
    permettant d\'afficher les « rulers » et les « media
    queries ». Cette dernière est très pratique car vous verrez
    apparaître ici toutes vos règles de média contenues dans le CSS.

 

En manipulant cette outil vous allez remarquer que l\'affichage n\'est
pas du tout adapté aux résolutions moins élevées comme celles des
smartphones.

Le principe va donc consister à créer des classes ou « surcharger » les
existantes afin que les nouvelles déclarations soient prises en compte
dès qu\'un déclencheur est atteint.

L\'objectif est que votre site soit agréable à consulter quelle que soit
la résolution choisie. Vous devez ainsi :

-   modifier le menu de la barre de navigation (cacher celui prévu pour
    les résolutions plus élevées et en afficher un autres plus adapté
    pour les autres, ou modifier la taille de la police) ;

-   adapter la taille de la police de caractères et de tous les éléments
    (tableaux, images\...) en fonction de la résolution ;

-   faire en sorte que les blocs qui sont côte à côte passent les uns en
    dessous des autres ;

Un exemple de rendu pour la page a-propos.html pourrait être celui-ci :

![](media/image7.png){width="4.072916666666667in"
height="5.903753280839895in"}

 

**FINALISATION**

Si vous avez terminé les modifications demandées dans le cadre de ce
workshop, vous pouvez vous entraîner en effectuant des modifications de
style supplémentaires et plus poussées.

 

Pensez également à passer vos pages HTML dans le [validateur
W3C](https://validator.w3.org/#validate_by_input) afin de s\'assurer que
toutes les balises obsolètes ont été retiré et que des erreurs ne se
sont pas glissées.

Vous pouvez également faire de même avec le [validateur
CSS](https://jigsaw.w3.org/css-validator/#validate_by_input).

 

La prochaine étape consistera à rendre votre site interactif en
produisant du code JavaScript.[\
](https://moodle.cesi.fr/pluginfile.php/23045/mod_resource/content/6/co/_2_-_Prosit_Creation_site_web_statique.html)
