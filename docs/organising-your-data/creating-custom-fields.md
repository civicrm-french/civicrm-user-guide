Créer des champs personnalisés
======================

Ce chapitre explique comment améliorer les données de base de CiviCRM par des champs personnalisés qui représentent les données que vous voulez acquérir en plus des données de base

Par exemple, vous pouvez compléter les informations recueillies pour les organisations par une série d'onglets que vous pouvez cocher pour chacun des clients de ces organisations. Vous pouvez aussi limiter les champs personnalisés à certains types de contacts. Vous pouvez ainsi avoir un champ personnalisé pour un type de contact, disons « étudiant », avec une liste de tous ses cours.

CiviCRM enregistre les champs de vos données personnalisées dans des "ensembles de champs personnalisés". 
Ajouter des données personnalisées implique donc deux étapes :

1.  Créer un ensemble de champs personnalisés pour un type de contact donné. Il servira ensuite de contenant pour les champs personnalisés.
2.  Ajouter les champs personnalisés pour cet ensemble. (Il peut être utile de lire d'abord les informations sur les types de champs personnalisés, mais avant de créer ces champs vous devez d'abord créer l'ensemble de champs.)

Autrement dit, un champ est une unité d'information inscrite dans la base de données : langue maternelle d'un individu, date de fins d'études, etc. Un ensemble est un regroupement de champs qui renferment des données sur un même objet ou un même domaine.

Ensemble de champs personnalisés
-----------------

Les champs personnalisés font toujours partie d'un "ensemble de champs personnalisés". Ce que recouvre chacun de ces ensembles peut être aussi large ou pointu que vous le désirez. Vous pouvez par exemple créer l'ensemble de champs personnalisés « Prescripteur " et l'associer à tous vos types de contact, en créer un deuxième baptisé « Statut logement » et l'associer à un type de contact précis (« Individus »), et ajouter un troisième ensemble associé à un composant particulièr (CiviMember ou CiviEvent) ou à un autre élément tel que Groupes ou Relations. L'étendue d'un ensemble de champs personnalisés est une des rares décisions irréversibles dans CiviCRM. Vous ne pourrez pas y apporter de modifications après l'avoir créé : il est donc important de bien réfléchir à l'avance aux champs personnalisés que vous voulez y associer.

CONSEIL : Quand vous créez des ensembles de champs personnalisés, demandez-vous :

-   Comment les champs de cet ensemble seront-ils utilisés?
-   Pour quel type de contact ou de dossier ces champs seront-ils pertinents?
-   Ces champs sont-ils susceptibles de servir dans un grand nombre de situations, ou au contraire sont-ils pertinents pour un type de contact précis, un événement particulier, un type de contribution, etc. ?

Prendre le temps de bien répondre à ces questions vous évitera de vous encombrer d'une pléthore de champs inutiles. Si votre ensemble de champs personnalisés contient un champ « Niveau d'études », il ne vous sert à rien de l'associer à des types de contact comme Organisation ou Foyer : plutôt que d'associer votre ensemble à la grande catégorie Contacts, mieux vaut simplement l'associer à Individus. Ou supposons qu'une de vos données personnalisées soit spécifique à la page d'inscription d'un événement en particulier : associez ces données personnalisées à ce type d'événement seulement.

Si vous avez beaucoup de champs personnalisés, vous pouvez les classer par sujet. Par exemple, vous avez associé 20 champs personnalisés aux individus dont 12 correspondent à un annuaire en ligne de vos membres. Plutôt que de regrouper ces 20 champs dans un seul ensemble, il vaut mieux les séparer en deux groupes : un pour les champs liés à l'annuaire, et l'autre pour le reste des détails sur les individus.

Pour créer un ensemble de champs personnalisés - et les champs personnalisés eux-mêmes – rendez-vous à :**Administrer CiviCRM > Données personnalisées > Nouvel ensemble de données personnalisées**. Ce formulaire vous permet d'assigner un titre à votre ensemble de champs, de spécifier le type de dossier auquel vous le destinez, de choisir comment il va s'afficher, et entrer le texte d'information approprié. Le formulaire apparaît sur l'image qui suit. 

![image](/img/Custom%20Field%20Set.png)

Nous allons maintenant vous décrire chacun des champs.

### Nom de l'ensemble

Ce nom va servir de légende à votre ensemble de champs si vous choisissez de faire apparaître celui-ci dans le corps du texte. Si vous optez plutôt pour un affichage par onglet, le nom de l'ensemble servira d'étiquette pour l'onglet de navigation.

### Utilisé pour

Cette option permet de vous assurer que vos champs personnalisés n'apparaissent qu'aux endroits pertinents. Voici la liste de vos choix :

- Activité : assigne vos champs à toutes les activités ou à un type d'activité, précis tel que rendez-vous ou appel téléphonique.
- Adresses : crée un bloc d'adresses, qui permet à l'utilisateur de créer des champs additionnels qui s'appliquent à une adresse.
- Contacts : assigne vos champs à tous vos contacts.
- Contributions : assigne vos champs à toutes vos contributions, ou à un type de contribution précis comme dons ou frais de participation à un événement.
- Événements : assigne vos champs à tous vos événements ou à un type d'événement précis comme Conférence ou Formation. Ces champs s'appliquent à un événement concret, et non pas au dossier d'inscription d'un participant.
- Subventions : pour les champs qui servent spécifiquement aux subventions.
- Groupes : va apparaître dans la configuration des Groupes. Prenez note que ces champs ne peuvent pas faire l'objet d'une recherche.
- Foyer : champs servant spécifiquement au type de contact foyer.
- Individu : champs servant spécifiquement au type de contact individu.
- Adhésion : champs qui serviront à tous les entrées relatives à une adhésion ou à un type d'adhésion en particulier.
- Organisation : champs servant spécifiquement au type de contact "Organisation".
- Participants : champs qui apparaissent dans le dossier d'inscription d'un participant. Vous pouvez choisir entre trois options : les champs généraux, applicables à toutes les inscriptions, les champs applicables à un rôle de participant précis et les champs qui s'appliquent aux inscriptions à un type d'événement particulier.
- Promesses de dons : champs servant spécifiquement aux promesses de dons.
- Relations : assigne vos champs à toutes les relations ou à un type de relation précis, tel que *conjoint* ou *employé par*.

### Ordre

Si vous avez créé plus d'un ensemble, le champ Ordre vous permet de déterminer l'ordre dans lequel ceux-ci vont apparaître. Les champs s'affichent par ordre croissant : 1 ou 2 va s'afficher avant 8 ou 9.

### Entrées multiples

Un champ ne contient en général qu'une seule entrée. Par exemple, une personne a les cheveux blonds ou noirs, mais pas les deux à la fois. Mais certains champs sont plus complexes, et peuvent demander plusieurs entrées différentes. Par exemple, pour un champ comme « Formation Universitaire », il faut prévoir la saisie de plusieurs diplômes, dont chacun représente une entrée distincte.

CiviCRM offre cette fonction pour les ensembles de champs attriués aux contacts (la catégorie générale, ou un type de contact en particulier). Pour utiliser cette fonction, sélectionnez l'option « Cet Ensemble de champs personnalisés accepte-t-il les entrées multiples? » 

Cette option compte plusieurs restrictions : 

- Elle s'applique à l'ensemble au complet. Vous ne pouvez pas l'appliquer à un seul champ.
- Elle doit utiliser l'affichage par onglet. L'affichage dans le corps du texte n'est pas permis.
- Vous pouvez l'utiliser uniquement pour les Contacts. Les entrées multiples ne sont pas disponibles pour les Activités, les Contributions, etc.
- Vous ne pouvez pas vous en servir pour un profil, comme ceux utilisés pour les Événements.
- Depuis juillet 2010, les entrées multiples ne peuvent pas être exportées.

### Options d'affichage

Il y a deux manières d'afficher les ensembles de champs personnalisés d'un dossier : dans le corps du texte sur la page Résumé (sous l'onglet Résumé), ou sous un nouvel onglet qui s'ajoute aux autres (Résumé,... Contribution, Groupe, etc...).
CONSEIL : Nous suggérons d'utiliser l'affichage par onglet pour les champs que vous consulterez plus rarement, ou pour les ensembles qui contiennent de nombreux champs. Vous pourrez changer cette configuration par la suite.

Vous pouvez également spécifier que vous souhaitez que le champ personnalisé défini soit «réduit» sur l'affichage initial. Si vous cochez cette case, seul le titre de ce champ est affiché lorsque la page est chargée initialement, car les champs sont masqués. Ceci est utile pour les jeux de champs qui sont rarement utilisés car ils réduisent l'espace occupé par les données lorsque la page s'ouvre. Une propriété "réduite" similaire est disponible pour l'affichage de données personnalisées dans "Recherche avancée".

Il y a deux façons d'afficher les champs dans un onglet : **Onglet** et **Onglet avec table**.

**Onglet avec table** offre un aperçu concis des données dans l'ensemble. De nouveaux enregistrements peuvent être ajoutés et les enregistrements existants peuvent être édités dans des fenêtres pop-up. Sous **plus**, il ya la possibilité de "copier un enregistrement". Pour les enregistrements consécutifs qui ont la même valeur dans de nombreux champs, cela vous permet de modifier un ou deux champs et d'enregistrer la copie en tant que nouvel enregistrement.

![image](/img/z-Sprint2014%20copy%20multli%20record.png)

**Onglet** affiche les champs de façon semblable au style par défaut.

![image](/img/z-Sprint14%20multi%20record%20old%20style%20table.png) 

### Cet ensemble de champs personnalisés est-il toujours actif ?

Si actif, cela signifie que vous pouvez consulter et modifier les champs. Si l'ensemble n'est pas actif, il ne s'affiche pas dans l'interface d'utilisateur ùais ses champs demeurent dans le système de CiviCRM. Cette option peut s'avérer utile pour la gestion de vos données, en particulier si vous effectuez une migration à partir d'une base de données pré-existante.

Il se peut par exemple que votre base de données extérieure contienne des champs que vous souhaitez transférer dans CiviCRM pour vos archives, mais vous comptez utiliser une nouvelle structure de données. Supposons par exemple que vous importiez vos listes de membres à partir d'une base de données MS Access. Chaque entrée dans Access contient un champ d'identification unique (sa clé), qui n'est d'aucune utilité dans CiviCRM. Plutôt que d'ignorer complètement ce champ, vous pouvez archiver son contenu dans un champ personnalisé, importer vos données, puis désactiver ce nouveau champ pour le rendre invisible, ce qui allégerait votre interface. Il vous suffit de ne pas cocher l'option Activer ce champ.

Bien qu'invisible pour les utilisateurs, la valeur d'un champ inactif demeure dans le système pour utilisation future. Vous pouvez le consulter si jamais il vous faut comparer la valeur d'un champ avec un document imprimé, ou vous assurer qu'il n'y a pas d'écarts entre vos archives.

Un champ que vous avez activé peut toujours être désactivé dans le formulaire qui définit ce champ.

### Aide avant et après formulaire

Si vous entrez du texte dans l'aide avant-formulaire, votre texte d'aide apparaîtra au-dessus de l'ensemble de champs personnalisés. Si vous entrez du texte dans l'aide après-formulaire, il apparaîtra en-dessous. Utilisez l'aide à ce niveau pour les instructions qui s'appliquent à tout votre ensemble de champs personnalisés.

Champs personnalisés
--------------------

Après la création d'un ensemble de champs personnalisé, vous pouvez créer les champs de données personnalisés. Cliquez sur **Afficher et modifier les champs personnalisés** suivi de **Nouveau champ personnalisé**  et vous verrez l'écran comme ci-dessous. Nous expliquerons chacune des options de cette section.

Après avoir terminé les options de configuration du champ, cliquez sur «*Enregistrer*» pour enregistrer le champ et retourner à la liste des champs de votre ensemble de champs personnalisés ou cliquez sur «Enregistrer et Nouveau» pour enregistrer le champ et commencer à définir un nouveau champ.

À l'exception des données et de la sélection du type de champ d'entrée, toutes les options de configuration peuvent être modifiées après la création initiale du champ. Vous pouvez également trouver utile de prévisualiser vos champs personnalisés, ainsi que l'ensemble des champs personnalisés, comme vous les avez définis. Cela est particulièrement utile pour vérifier la mise en page des champs de bouton radio et de case à cocher avec un grand nombre de choix.

![customdatafield.png](/img/CiviCRM-DataBasic-customdatafield-en.png "newcustomfield")

### Étiquette du champ

Le texte à côté du champ lorsqu'il est affiché à l'utilisateur. Le texte saisi ici correspond également à l'étiquette affichée lorsque vous exportez des données. Lorsque vous utilisez des champs dans un profil, vous pouvez remplacer l'étiquette de champ. Ainsi, sur cet écran, vous pouvez choisir des intitulés plus adaptés à votre activité et qui conviennent aux utilisateurs lors de leur affichage dans les profils.

### Type
Les champs personnalisés peuvent être de différents types, dont beaucoup ont probablement été rencontrés lors du remplissage de formulaires sur des sites Web. Lorsque vous créez un champ personnalisé, CiviCRM présente une liste déroulante de types de données à partir de laquelle vous pouvez sélectionner celle qui représente le mieux les données que vous souhaitez stocker. Le menu de gauche (illustré dans la figure suivante) indique le paramètre de format des données, alors que le menu de droite indique la manière dont vous souhaitez interagir avec l'utilisateur.

![datainputfieldtype.png](/img/CiviCRM-DataBasic-datainputfieldtype-en.png "datainputtype")

Les types de champs sont :

- **Alphanumérique** (champs texte et nombre) peuvent être des types suivants:
    - Texte: une zone simple dans laquelle les utilisateurs peuvent saisir du texte.
    - Sélectionnez: une liste déroulante qui limite le choix à une sélection.
    - Radio: une liste d'options où vous pouvez faire une sélection. Contrairement à une boîte de sélection, toutes les options sont visibles à l'écran en même temps.
   - Oui / Non: liste radio avec deux options contrastées.
   - Check-box: une liste d'options permettant plusieurs sélections.
    - Multi-sélection: une liste d'options dans une seule case. Vous pouvez sélectionner plusieurs sélections à l'aide de la commande + clic.
    - Multi-sélection avancée: deux listes côte à côte dans lesquelles les éléments peuvent être déplacés de l'un à l'autre.
    - Autocomplete select: un widget d'autocomplétion. L'utilisateur peut commencer à taper et lorsque le texte saisi identifie une sélection, le champ remplit automatiquement la sélection complète.    
 - **Note**: une zone de texte plus longue qui permet plusieurs lignes. Deux choix de texte :
    - texte brut
    - texte enrichi, qui affiche un éditeur WYSIWYG qui permet le HTML.
  - **Entier** : un nombre entier qui peut être affiché sous forme de:
    - Texte
    - Boite de sélection
    - Bouton radio
  - **Nombre**: tout nombre qui comprend des décimales, comme 3.1416 et peut être affiché sous forme de:
    - Texte
    - Boite de sélection
    - Bouton radio
  - **Money**: similaire à un nombre, mais traité selon la devise locale configurée dans les pages d'administration de CiviCRM et peut être affiché sous forme de:
    - Texte
    - Boite de sélection
    - Bouton radio
  - **Date**:  une valeur de date (et éventuellement de temps) à l'aide du widget de calendrier. Vous pouvez définir une plage d'années qui peut être sélectionnée avant et après la date actuelle.
  - **État / Province**: liste des lieux géographiques disponibles tels que configurés dans les paramètres de localisation de CiviCRM (Administer> Configurer> Paramètres globaux> Localisation). Peut être soit une boîte de sélection ou une boîte de sélection multiple.
   - **Pays**: liste des pays. Peut être soit une boîte de sélection ou une boîte de sélection multiple.
   - **Fichier**: l'utilisateur peut sélectionner et télécharger un fichier.
   - **Lien**: un hyperlien actif sur Internet.
   - **Contact Reference**: un widget d'autocomplétion pour un contact CiviCRM existant.

CONSEIL : Nous vous suggérons d'expérimenter la création de différents types de champs pour avoir une idée de leur comportement. Les différentes options ont des implications lors de l'utilisation. Par exemple, les cases à cocher vous permettent d'utiliser "OU" ainsi que les recherches "ET" dans la recherche avancée, alors que la sélection multiple ne le permet pas.
 
**Afficher en table ?**

Cette case à cocher n'apparaît que lorsque vous créez un champ dans un jeu de champs multi-enregistrements que vous avez choisi d'afficher sous l'onglet **avec table**. Elle est cochée par défaut. Si vous désélectionnez cette option, le champ ne sera pas affiché dans la table. Vous pouvez le faire pour les champs moins importants si vous disposez d'un nombre de données trop large pour votre écran.

![image](/img/z_sprint14_MultirowCustom3.png)

Les champs cachés dans la vue de la table seront toujours disponibles lors de l'ajout d'un nouvel enregistrement ou de l'affichage, de l'édition ou de la copie d'une ligne particulière.

![image](/img/z_sprint14_MultirowCustom2.png) 

### Taille du champ dans la base de donnée

La longueur d'un champ de base de données vous permet de spécifier le nombre de caractères que ce champ contiendra. Normalement, vous devez le laisser au maximum. Dans certains cas (par exemple si vous avez affaire à des ensembles de champs extrêmement importants), il peut être judicieux de raccourcir ce champ pour améliorer les performances et diminuer l'espace de stockage, mais la définition d'une longueur plus courte ne fera pas la différence pour la grande majorité des utilisateurs.

### Ordre

Permet de contrôler l'ordre dans lequel les champs apparaissent. Vous pouvez affecter l'ordre dans le formulaire d'édition de champ ou utiliser les icônes haut / bas de la table de liste de champs principale pour ajuster la présentation des champs. Par défaut, dans un ensemble, les nouveaux champs apparaissent au bas de la liste des champs .

### Valeur par défaut

Vous pouvez désigner une valeur par défaut pour un champ. Cette valeur sera automatiquement affichée ou sélectionnée lorsque les utilisateurs accèdent à un formulaire contenant ce champ.

### Aide avant et après formulaire

Idéalement, votre nom de champ est suffisament clair pour que les utilisiteurs sachent comment le remplir. Mais dans les cas où il ya une certaine ambiguïté, ou que vous souhaitiez préciser la façon dont un certain champ est utilisé, vous pouvez entrer le texte d'aide ici. Si vous l'entrez dans l'aide avant formulaire, votre texte d'aide s'affiche au-dessus du champ de formulaire et si vous entrez du texte dans l'aide après formulaire, il apparaît sous le champ de formulaire.

Le texte d'aide apparaît dans toutes les utilisations du champ dans les pages d'administration et est inséré comme texte d'aide par défaut lorsque des champs sont affectés à un profil (voir «profils»). La personne qui crée le profil peut supprimer ou modifier le texte d'aide sans impact sur la définition du champ personnalisé d'origine.

### Requis = (obligatoire)

Lorsque sélectionné, une valeur doit être fournie pour ce champ avant que le formulaire puisse être validé. Sinon un message d'erreur indiquera à la personne de remplir les champs requis.

Si vous souhaitez qu'un champ soit requis uniquement lorsqu'un utilisateur remplit un profil particulier, vous pouvez le désactiver et cocher la case "Requis" plus tard dans le profil.

### Ce champ est-il accessible dans la recherche ?

Affiche le champ dans un groupe de champs personnalisés dans la page "Recherche avancée" de CiviCRM. Bien que vous soyez tenté de marquer tous les champs comme pouvant être consultés, cela peut inutilement encombrer le panneau de champ personnalisé Recherche avancée, alors qu'en fait, certains champs ne seront probablement jamais utilisés de cette façon. Vous pouvez activer ou désactiver cette option à tout moment. Ne soyez donc pas trop préoccupé par l'arrivée d'une décision finale lorsque vous définissez un champ personnalisé.

### Actif

Comme pour la case à cocher "Actif" dans le formulaire définissant l'ensemble de champs personnalisé, cette zone détermine si le champ est désactivé ou activé lorsque CiviCRM l'affiche à l'utilisateur.

### Consulter seulement

Permet de désigner un champ comme visible mais non éditable. Il existe deux utilisations générales pour ce champ:

  - Pour stocker les données importées à partir d'un autre système qui puissent être consultées par un utilisateur mais que vous ne souhaitez pas qu'elles puissent être modifiées.
  - Pour stocker des données qui ne sont pas entrées directement à travers l'interface utilisateur mais plutôt par une méthode définie par votre développeur.
  
### Options à choix multiples

Pour les types de champs qui impliquent la sélection à partir d'un ensemble d'options multiples (telles que Select, Radio, Check-box, Multi-select et Advanced Multi-select), vous avez le choix soit d'utiliser un ensemble d'options existantes, déjà créé pour un autre champ personnalisé, ou créer un nouvel ensemble. Vous pouvez saisir ces valeurs lors de la création du champ ou saisir les valeurs ultérieurement. L'étiquette de l'option est affichée sur le formulaire, tandis que la valeur de l'option est stockée dans l'enregistrement de contact.

Si vous choisissez d'utiliser le même ensemble d'options pour plusieurs champs, vous serez averti lors de toute modification que cela affectera un ensemble d'options utilisé par plusieurs champs.

Lorsque vous créez un nouvel ensemble, vous avez la possibilité de saisir initialement jusqu'à dix options à choix multiples dans une table. Si vous avez besoin de plus de dix options, vous pouvez créer un nombre illimité de choix supplémentaires après avoir enregistré ce nouveau champ en utilisant le lien «Modifier les options de choix multiples». Aller à: **Administer **> ** Personnaliser**> **Données personnalisées**> **Afficher et modifier les champs personnalisés**> **Modifier les options de choix multiples**. Vous pouvez accéder à cet écran ultérieurement pour modifier l'étiquette, l'ordre et l'état actif de toute option à choix multiples, ou ajouter d'autres choix.

![CustomMultipleOptions](/img/CiviCRM-Configuring-CustomMultipleOptions-en.PNG "CustomMultipleOptions")

Si vous le souhaitez, vous pouvez également marquer l'un des choix comme option par défaut.
Les options inactives sont masquées lorsque le champ est affiché.

### Gestion des ensembles de champs personnalisés.

Vous pouvez afficher une liste de tous les champs personnalisés dans un ensemble de champs personnalisés définis à tout moment en naviguant sur **Administer> Personnaliser les données et les écrans> Données personnalisées** et en cliquant sur "Afficher et modifier les champs personnalisés" pour l'ensemble de champs choisi.

![image](/img/Move_custom_fields.PNG) 

Outre les options prévues dans les paramètres d'édition du champ , éditez les options à choix multiple (s'il y a lieu), prévisualisez, désactivez ou supprimez, vous avez également la possibilité de déplacer un champ personnalisé vers un autre ensemble de données. Vous pouvez déplacer des champs personnalisés entre les ensembles utilisés pour tous les contacts ou pour les sous-types de contacts. Vous ne pouvez déplacer des champs que dans des ensembles de données du même type.

Choisir entre champs, groupes et étiquettes
----------------------------------------
Les champs de données, les groupes et les étiquettes sont trois manières principales d'associer des informations aux contacts. Bien qu'il puisse être tentant de créer un champ de données personnalisé pour chaque attribut de vos données, prenez le temps d'étudier toutes les alternatives. Groupes et étiquettes offrent de puissantes fonctionnalités que vous pourriez occulter si vous comptez uniquement sur des données personnalisées. En outre, l'utilisation de champs de données pour les informations qui  pourraient être stockés plus efficacement dans des groupes ou des étiquettes peut ralentir votre système. Enfin, l'utilisation appropriée des groupes et des étiquettes facilite considérablement la tâche du personnel administratif pour retrouver les données.

Voici quelques conseils qui peuvent vous aider à choisir:

   - Les données pouvant prendre un large éventail de valeurs, telles que l'adresse ou la biographie d'une personne, doivent être stockées dans un champ de données personnalisé alphanumérique.
   - Les champs de données personnalisés peuvent être regroupés et affichés dans leur propre onglet sur l'enregistrement du contact.
   - Comme son nom l'indique, les groupes sont utilisés pour grouper des contacts. Par exemple, vous pouvez affecter les membres du conseil d'administration à un groupe, le personnel à un autre, les bénévoles à un autre, etc... Si vous utilisez Joomla ou Drupal, vous pouvez attribuer des autorisations en fonction de l'appartenance a un groupe. Vous pouvez également définir un groupe auquel CiviCRM ajoute automatiquement des contacts et les supprime en fonction de certaines caractéristiques. Cette fonction est appelée "Groupe dynamique".(Smart Group)
   - Si vous envisagez d'utiliser CiviMail pour les envois en masse et que vous souhaitez que certains contacts reçoivent un courrier particulier, ces contacts doivent être affectés à un groupe. Par exemple, vous aurez peut-être un communiqué de presse a adresser seulement à certains contacts : les journalistes. Ces contacts doivent être affectés à un groupe particulier. Ce groupe utilisé pourrait être alors un Groupe dynamique.   
   - Les étiquettes et les groupes peuvent être structurés hiérarchiquement. Par exemple, un groupe ou une étiquette intitulée «Régions» peut avoir un sous-groupe ou une sous-étiquette pour chaque région géographique couverte par votre organisation (voir «Etude de cas sur les balises hiérarchiques» plus loin dans cette section).
   - Les étiquettes prennent en charge des options de recherche plus puissantes que les champs de données ou les groupes. Par exemple, vous pouvez effectuer une recherche dans plusieurs variables avec les opérateurs ET et OU. Les champs de données ne prennent en charge que les listes de mots (qui sont effectivement les mêmes qu'un opérateur ET), à l'exception des champs désignés comme des cases à cocher, qui supportent les opérateurs OR.
- Les étiquettes ont une interface utilisateur plus sophistiquée que les champs de données ou les groupes. L'interface permet a l'utilisateur d'ajouter et de supprimer des étiquettes sans recharger la page en mode édition.
- Des champs de données personnalisés peuvent être affectés à un type d'enregistrement spécifique (par exemple, les Entreprises uniquement), tandis que les étiquettes seront attribués à tous les types une fois que les variables sont définies.

Limites de stockage d'un ensemble de champs personnalisés
------------------------------------

Un grand nombre d'ensembles de champs personnalisés avec un nombre très important de champs peut causer des problèmes lors de la recherche, l'exportation de données ou l'exécution de compte rendus. Il est difficile de donner des limites spécifiques au nombre d'ensembles de données que vous devez créer ou au nombre de champs que vous devez ajouter aux ensembles de champs. Cela dépend beaucoup du type de données que vous collectez et du serveur sur lequel votre installation est hébergée. En cas de doute vous devez en discuter avec votre administrateur système ou le fournisseur de services CiviCRM.




