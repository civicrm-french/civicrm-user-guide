Groupes et étiquettes
===============

Les groupes et les étiquettes sont deux méthodes clés d'organisation des données dans CiviCRM. Lorsqu'elles sont utilisées correctement, les deux permettent une segmentation puissante et une recherche aisée dans votre base de données.

Les  groupes et les étiquettes sont des méthodes de catégorisation et il peut être difficile de déterminer si une étiquette ou un groupe est plus approprié dans une situation donnée. Identifier les différences dans leurs fonctionnalités vous aidera à décider quoi utiliser.

Il faut différencier ces deux concepts. Bien qu'il existe différentes approches sur la façon dont les étiquettes et les groupes devraient être utilisés, une façon logique de procéder est que les étiquettes doivent être utilisées pour les catégories descriptives de contacts, les activités et les dossiers, alors que les groupes devraient être utilisés pour regrouper les personnes au sein d'une entité qui doit être traitée comme une unité cohérente (pour envoyer des envois à..., par exemple). Ainsi des dénominations comme *bénévolat*, *partenaire*, *végétarien* et *musicien* seraient des étiquettes avec lesquelles vous pourriez catégoriser les contacts. Mais  *Comité de soutien, Autres associations, Institutions, Public accueilli* ... seraient des groupes auxquels vous pourriez ajouter des contacts.

Groupes
------

Les groupes sont une fonctionnalité très importante au sein de CiviCRM. En plus de leur utilisation fondamentale en tant qu'unité de contacts ayant des caractéristiques communes. Ils jouent un rôle essentiel dans CiviMail et Profils. Ils peuvent être utilisés pour configurer des droits d'accès avancés (Joomla et Drupal). Des groupes bien définis sont l'un des outils les plus importants disponibles lors de la segmentation de votre base de données CiviCRM.

Il existe deux types de groupes :  **Groupes (régulier)** et **Groupes intelligents**.

-  Les groupes réguliers sont simplement appelés **Groupes**. Vous y placez et supprimez manuellement des contacts.  Par exemple, vous pouvez affecter manuellement les membres du conseil d'administration de votre organisation à un groupe "Conseil d'administration". Vous pourrez ensuite facilement envoyer des courriels liés à votre conseil d'administration à chaque personne qui en est membre sans avoir à les chercher et les sélectionner individuellement.

- **Les groupes intelligents** sont des groupes remplis automatiquement et qui sont configurés pour inclure des contacts qui partagent un certain ensemble de caractéristiques ou d'activités. Lorsque des contacts sont ajoutés ou modifiés, CiviCRM les vérifie automatiquement et les ajoute aux groupes intelligents s'ils correspondent aux caractéristiques que vous avez configurées. Par exemple, vous pouvez créer un groupe intelligent pour «Adhérents 2016 de Paris» qui comprend les contacts qui ont versé une contribution en 2016 (une activité) et ont une adresse à Paris (une caractéristique). Lorsque de nouveaux contacts de Paris apportent leur contribution en 2016, ils sont automatiquement ajoutés à ce groupe. Un autre exemple est un groupe intelligent de tous les donateurs qui n'ont pas encore reçu de lettre de remerciement. Lorsque vous envoyez vos lettres, les donateurs qui les reçoivent quitteront automatiquement le groupe intelligent, vous permettant d'avoir toujours une liste exacte pour travailler.

### Paramètres des groupes et fonctionnalités

Chaque groupe doit avoir un nom de groupe clair et facilement compréhensible, ainsi qu'une description de son but afin que les autres utilisateurs de la base de données puisse le comprendre. Le nom et la description doivent permettre aux utilisateurs de déterminer rapidement ce que certains groupes font lorsqu'ils travaillent dans différents contextes (par exemple, CiviMail). Cette clarté et cette spécificité sont particulièrement importantes lorsque votre organisation gère de nombreux groupes différents. Si un groupe est créé pour une personne spécifique au sein de votre organisation, il est préférable de mentionner le nom du propriétaire du groupe dans la description afin que, dans le futur, quelqu'un puisse vérifier si ce groupe est toujours utilisé ou s'il peut être supprimé.

Les types suivants peuvent être affectés aux groupes:

- **Mailing List** :  si vous envisagez d'utiliser ce groupe comme liste de diffusion dans CiviMail. Ce type de groupe est disponible pour les groupes réguliers et intelligents.
- **Contrôle d'accès** : (Joomla,Drupal) permet d'attribuer des autorisations d'accès CiviCRM à un ensemble de contacts. Seuls les groupes réguliers peuvent se voir attribuer le type de groupe Contrôle d'accès.

Il est possible de créer des types de groupes supplémentaires pour refléter vos besoins spécifiques. Cela est particulièrement utile si votre organisation compte des centaines de groupes, car le type de groupe peut être utilisé comme filtre dans l'écran "Gérer les groupes". Pour créer d'autres types de groupe, allez dans **Administer> Paramètres système> Liste de choix ** et sélectionnez **Type de groupe**.

### Visibilité

La visibilité détermine les autorisations pour voir et supprimer les contacts des groupes. Sélectionnez "Utilisateur et administrateur seulement" si l'appartenance à ce groupe n'est contrôlée que par des utilisateurs autorisés de CiviCRM. Sélectionnez «Pages publiques» si vous souhaitez autoriser les contacts à se joindre et à se retirer de ce groupe via les formulaires d'inscription et de profil de compte en ligne.

Certaines organisations trouvent utile de créer une hiérarchie de groupes. Dans CiviCRM, cela se fait en créant un ou plusieurs groupes parents, puis en leur assignant d'autres groupes. Lorsqu'un utilisateur envoie un courriel à un groupe parent ou recherche des contacts dans un groupe parent, tous les contacts dans les groupes enfants associés sont automatiquement inclus.

-   Par exemple, une organisation dotée d'un bureau national et de cinq bureaux régionaux attribue les membres de chaque région dans leur propre groupe. Ensuite, ils créent un groupe national qui est assigné comme groupe parent pour tous les groupes régionaux. Le bureau national peut alors envoyer des courriels au groupe national, sachant que tous les contacts dans les groupes régionaux qui sont des enfants du groupe national seront inclus.

### ID des groupes 

CiviCRM attribue un ID numérique unique à chaque groupe. Ces ID de groupe peuvent être utilisés pour diverses opérations. Par exemple, l'ID de groupe peut être utilisé pour définir une URL pour les enregistrements de groupe. Vous pouvez trouver cet ID  en cochant la colonne ID dans la liste des groupes affichée à **Menu de navigation> Contacts> Gérer les groupes**.

Etiquettes
---------
**Les étiquettes** sont utilisés pour classer les contacts, les activités et les dossiers dans CiviCRM. Vous pouvez créer autant de étiquettes que nécessaire pour classifier les contacts dans votre base de données. Il est conseillé d'éviter la duplication des étiquettes existantes ou d'en ajouter qui ne seront pas vraiment nécessaires. 
Il peut être utile de créer une procédure standard pour créer et utiliser les étiquettes au sein de votre organisation... afin d'éviter certains doublons.

Groupes vs Etiquettes 
---------------------
C'est une question courante pour tout projet. La philosophie décrite dans l'introduction de ce chapitre est une ligne directrice, mais ces règles peuvent être adaptées selon la façon dont vous avez l'intention d'utiliser votre segmentation de contacts.

Un avantage indéniable d'avoir des groupes et des étiquettes est que vous pouvez effectuer des recherches plus fines en utilisant AND et OR. 
Par exemple, si vous avez des groupes de journalistes, de bénévoles et de membres et que vous utilisez des étiquettes pour identifier des centres d'intérêt tels que le développement, l'art et l'histoire, vous pouvez trouver tous les journalistes qui sont intéressés par l'art ou le développement, tous les bénévoles ou membres qui sont intéressés par l'histoire. Toute autre combinaison est possible.

Les groupes disposent de certaines fonctionnalités que les étiquettes n'ont pas:

-  Les groupes sont intégrés dans plusieurs autres fonctions de CiviCRM (notamment CiviMail).
-  Les contacts peuvent être ajoutés automatiquement aux groupes intelligents en fonction de leurs caractéristiques.
-  Les groupes peuvent être associés aux "Drupal Organic Groups" et groupe d'utilisateur Joomla

Observez cette règle : les étiquettes peuvent être appliquées aux contacts, aux activités et aux dossiers, alors que les groupes ne peuvent être composés que de contacts.

Ce qui suit décrit les avantages et les inconvénients des groupes et des étiquettes

#### Avantages des étiquettes
-   Facile à configurer et à utiliser
-   Facilité de recherche par étiquettes (en Recherche de base ou avancée) 
-   Facile à combiner avec d'autres propriétés (comme domicile / code postal) pour créer des groupes intelligents

#### Limitation des étiquettes

-   Vous ne pouvez pas créer d'étiquettes UNIQUEMENT pour être utilisées avec des types de contacts spécifiques (individuels)
-   Lorsque vous exportez des étiquettes, elles sont toutes attribuées à un enregistrement et sont exportées dans une seule "cellule" en tant que liste (par exemple, «Professeur, bénévole»)
-   Les étiquettes permettent des sélections multiples - ce qui peut ne pas convenir à des caractéristiques mutuellement exclusives (par exemple, «Démocrate», «Républicain», «Parti Vert»)
-  Vous ne pouvez pas cacher de manière sélective ou autoriser les étiquettes dans les formulaires intégrés ou Profil et créer et modifier des formulaires (vous obtenez TOUTES les étiquettes TOUT LE TEMPS sur les formulaires d'édition)

#### Avantages des groupes
-  Les groupes sont le moyen le plus souple de segmenter vos contacts à des fins très variées.
-  Les groupes facilitent les tâches récurrentes telles que l'envoi d'une lettre d'information, l'impression d'étiquettes postales, etc.
-  Les groupes vous permettent de limiter l'accès aux groupes de contacts dits "spéciaux"
 - Les groupes prennent en charge les actions "d'abonnement" et "désabonnement"  de l'utilisateur final - un historique de ces actions est conservé dans le système
-  Les paramètres de visibilité vous permettent de décider quels groupes sont affichés aux utilisateurs finaux selon les formulaires de profil (c'est-à-dire que certains groupes peuvent être "privés")
-  Vous pouvez créer des groupes intelligents qui combinent des membres du groupe A + groupe B

#### Limitations des Groupes

-  Tous les groupes existants sont répertoriés sous "Gérer les groupes" et dans les formulaires de recherche. Cela peut entraîner des «surcharges» de groupe si vous en avez trop créé.
-  Les groupes utilisés pour les projets à court terme doivent être «purgés» lorsqu'ils ne sont plus nécessaires
-  Lors de l'exportation des enregistrements de contact, tous les groupes auxquels un contact appartient sont exportés sous la forme d'une seule liste séparée par des virgules (par exemple : "Administrateurs, Abonnés à la Newsletter")

Vous pouvez ajouter des contacts aux groupes de plusieurs façons:

-  A travers la section étiquettes et groupes de l'écran d'édition des détails de contact
-  Via l'onglet Groupe du contact
-  En utilisant l'action "Ajouter des contacts au groupe / étiqueter des contacts" après avoir effectué une recherche
-  En cliquant sur le lien Contacts d'un groupe dans **Menu Navigation> Contacts> Gérer les groupes**.

Les deux premières méthodes permettent également de supprimer des contacts individuels d'un groupe. Les deux dernières méthodes permettent d'ajouter plusieurs contacts à plusieurs groupes à la fois.

Les contacts individuels peuvent être ajoutés à un groupe soit dans l'écran d'édition de contact, soit via l'onglet Groupes. Plusieurs contacts peuvent être ajoutés simultanément à un groupe en effectuant une recherche, puis en sélectionnant Ajouter des contacts à un groupe à l'aide du menu déroulant  "Action". La deuxième méthode vous permet d'ajouter plusieurs contacts à un groupe en allant dans Gestion des groupes, en sélectionnant Membres pour le groupe concerné, puis en utilisant l'option "Ajouter des membres à ce groupe" en haut de l'écran.

Les contacts peuvent également être ajoutés à un groupe à la suite du remplissage d'un profil (voir ci-dessous).

Gestion des groupes
---------------
Pour afficher et gérer tous les groupes, accédez à: **Menu de navigation> Contacts> Gérer les groupes**

![image](/img/ManageGroups.png)

Vous pouvez  utiliser le formulaire "Rechercher des groupes" en haut de l'écran "Gérer les groupes" pour rechercher des groupes par nom, type, visibilité et si le groupe est activé ou désactivé. Vous pouvez également faire défiler ou parcourir la liste de groupes dans l'écran "Gérer les groupes". Cette liste comprend les groupes réguliers et les groupes intelligents.

Vous pouvez :

-   Ajoutez des contacts à un groupe en cliquant sur le lien "Contacts" dans la ligne du groupe
-   Modifier le groupe en cliquant sur le lien Paramètres
-   Désactiver ou supprimer un groupe en utilisant les liens dans le menu contextuel "Plus".
-   Voir le nombre de contacts actuel dans chaque groupe.

Trouver des contacts dans un groupe
-----------------------------------

La page Contacts de chaque groupe comprend un formulaire pour trouver des contacts dans le groupe. Vous pouvez rechercher des contacts au sein d'un groupe par nom, adresse e-mail, type de contact, statut de groupe (ajouté, supprimé ou en attente) ainsi que les étiquettes

![Groups_searchwithin](/img/CiviCRM_update-CiviCore-Groups_searchwithin-en.jpg "Groups_searchwithin")

Groupes et ACL
--------------
Les listes de contrôle d'accès (ACL) fournissent une autorisation plus fine que celle disponible dans les autorisations et les rôles de Joomla et Drupal. La configuration des listes de contrôle d'accès nécessite une bonne connaissance du concept, qui est expliqué en détail dans la documentation CiviCRM en ligne:

[http://wiki.civicrm.org/confluence/display/CRMDOC/Access+Control](http://wiki.civicrm.org/confluence/display/CRMDOC/Access+Control%20)

Comme pour de nombreux processus, la clé du succès est de s'assurer que vous avez réuni toutes les pièces avant d'essayer d'aller plus loin. En l'occurence, vous devez configurer les groupes, groupes de données personnalisés, profils et rôles requis avant de pouvoir les utiliser dans les ACL.

Travailler avec les étiquettes
------------------------------
Pour afficher les étiquettes, accédez à: **Contacts> Gérer les étiquettes** dans le menu de navigation.
Une étiquette peut être éditée ou supprimée en utilisant les liens respectifs dans sa ligne. Vous pouvez créer de nouvelles étiquettes en cliquant sur le bouton "Ajouter une étiquette" ou en allant dans "Contacts> Nouvelle étiquette" dans le menu de navigation.

![admin_tags](/img/CiviCRM_update-CiviCore-resized_600x158_admin_tags-en.png "admin_tags")

Chaque étiquette doit avoir un nom clair et unique et une description explicative pour aider les utilisateurs à comprendre le but de l'étiquette. Les étiquettes peuvent être structurées hiérarchiquement et désignées comme sous-étiquettes d'une étiquette existante en sélectionnant une étiquette Parent dans la liste déroulante.

Des étiquettes peuvent être utilisées pour les contacts, les activités et / ou les dossiers. Si une étiquette est destinée à être utilisée pour les contacts, elle sera disponible pour tous les types et sous-types de contact. Les étiquettes ne peuvent pas être spécifiquement désignées pour être utilisées pour un seul type de contact.

Les étiquettes sont un outil flexible et chaque utilisateur peut en créer autant que nécessaire. Les étiquettes très importantes peuvent être verrouillées pour empêcher qu'elles ne soient modifiées ou supprimées par les utilisateurs qui n'ont pas l'autorisation "administrer les étiquettes réservées".

Les balises peuvent être attribuées aux contacts, aux activités et aux dossiers de la manière suivante:

-  Lors de la création ou de la modification de l'enregistrement
-  Tout en créant ou en éditant l'enregistrement 
-  À partir de l'onglet Résumé des étiquettes de contact
-  À l'aide de l'action "Tag Contacts" après avoir effectué une recherche. 
Vous pouvez également utiliser les deux premières méthodes pour supprimer les étiquettes.

Ensemble d'étiquettes
--------
Les ensembles d'étiquettes sont une forme libre de classement des contacts et sont semblables aux étiquettes ordinaires, mais ils diffèrent principalement par : 

-  Ils agissent en tant que «container» pour vous permettre de regrouper des étiquettes (c'est-à-dire un ensemble d'étiquettes comme «logement social», «Hébergé» ou «logement zone rurale»)
-  Ils permettent de créer des étiquettes à la volée sans avoir à accéder à la page "Gérer les étiquettes" 
-  Ils permettent d'ajouter un champ de recherche supplémentaire dans la section "Critères de base" de la "Recherche avancée"

Pour créer un ensemble d'étiquettes dans le menu de navigation allez à : **Contacts> Gérer les étiquettes**  cliquez sur le bouton "Ajouter un jeu d'étiquettes". Attribuez un nom, une description et indiquez si le jeu d'étiquettes s'appliquera aux contacts, aux activités ou aux dossiers.

![image](/img/Tag%20Set%20-%20Create.png)

Si vous cliquez sur la case "Réservé?", l'étiquette est définie de façon permanente. Cela empêche qu'un groupe d'étiquettes soit supprimé par une personne sans autorisation de l'administrateur. (Pour en savoir plus sur les autorisations, voir le chapitre *Permissions et contrôle d'accès* de la section *Configuration initiale*).

Vous pouvez maintenant utiliser l'ensemble d'étiquettes pour classifier librement un contact, une activité ou un enregistrement de dossier.

Lorsque vous créez un nouvel ensemble d'étiquettes, un nouveau champ apparaît sur les pages d'édition des activités ou des dossiers ainsi que dans l'onglet "Etiquette" pour les contacts. Par exemple, si vous créez un ensemble d'étiquettes intitulé «Contacts hors secteur»  associé aux Contacts, vous verrez l'étiquette définie la prochaine fois que vous accéderez à l'onglet "Etiquette" de l'enregistrement d'un contact.

![image](/img/Tag%20Set%20-%20Creating%20tags%20on%20the%20fly.png)

Il s'agit là d'un champ de saisie semi-automatique: lorsque vous commencez à taper, CiviCRM recherche les étiquettes correspondantes dans ce jeu d'étiquette et affiche les correspondances sous le champ. Vous pouvez sélectionner une variable existante ou en créer une nouvelle en tapant la variable entière et en appuyant sur la touche Entrée. L'étiquette s'affiche alors dans le champ dans une zone. En cliquant sur le X, vous annulerez l'enregistrement que vous éditez (contact, dossier ou activité)

Les étiquettes créées dans un ensemble d'étiquettes apparaîtront automatiquement dans la liste **Contacts> Gérer les étiquettes (catégories)** et peuvent être consultées et éditées à partir de là. Toutefois, les balises créées dans un ensemble d'étiquettes ne seront disponibles que dans ce jeu d'étiquettes spécifique.


### Note sur la recherche des étiquettes et ensemble d'étiquettes 

Pour chaque jeu d'étiquettes que vous créez, un nouveau champ apparaît dans la section "Critères de base" de la **Recherche multicritères**. Vous pouvez uniquement rechercher des étiquettes qui existent déjà dans ce jeu d'étiquettes.

La recherche dans le champ "Toutes les étiquettes" vous permettra de trouver des enregistrements avec des étiquettes contenant un mot ou une phrase complete ou partielle. EXEMPLE: Si vous avez plusieurs balises contenant le mot 'Donateur', vous pouvez trouver des contacts étiquetés avec l'un d'entre eux en entrant 'Donateur' dans ce champ.

Lisez attentivement l'utilisation de la **Recherche multicritères**  dans la section **Recherche**.



