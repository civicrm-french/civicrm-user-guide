# Profils

Un profil est une sélection de champs de votre base de données. Les profils sont un outil puissant qui ont de nombreuses utilisations différentes dans tous les composants de CiviCRM. Les profils sont utilisés pour collecter des données (par exemple, sur un formulaire d'inscription) et pour afficher des données à l'utilisateur (par exemple, en tant que liste de membres). Ils peuvent être utilisés à la fois en interne (par exemple, pour créer des écrans de saisie de données simplifiés pour le personnel) et à l'externe (pour afficher des informations actualisées de la base de données).

Vous pouvez ajouter tous les champs de base et personnalisés à un profil, y compris les champs personnalisés à plusieurs valeurs. Il y a également quelques autres champs spéciaux que vous pouvez ajouter aux profils, à savoir, Groupes, qui inclura toutes les cases à cocher (une pour chacun de vos groupes publics)  et des étiquettes, qui incluent toutes les étiquettes  publiques.

En créant un Profil, vous êtes en mesure de sélectionner et de choisir uniquement les champs pertinents dans un but spécifique. Le diagramme ci-dessous fournit une explication visuelle de la façon dont les champs existants deviennent une partie d'un profil.

![Profiles](/img/CiviCRM-Icons-db1-en.png "Profiles")

Cette section explique comment utiliser les profils pour collecter et partager des données ainsi que plusieurs façons d'utiliser des profils permettant de gagner du temps pour toute personne qui gère des données dans votre organisation.

## Différentes utilisations des Profils

Cette section décrit brièvement plusieurs façons dont les profils peuvent être utilisés. Vous trouverez des instructions détaillées pour créer et utiliser les profils plus loin dans ce chapitre.

### Collecte d'informations sur les pages publiques

Un profil peut être utilisé pour recueillir des informations auprès de vos membres ou du public. Les profils peuvent être affichés sur des pages autonomes ou incorporés dans des pages de contribution, d'inscription de membre ou d'enregistrement à un événement. Vous pouvez ajouter plus d'un profil sur une page. Vous pouvez également choisir les champs requis et ajouter du texte dans le profil pour aider les utilisateurs à remplir le formulaire.

Exemples:

- Un formulaire d'inscription de volontaires contenant les champs prédéfinis pour le prénom, le nom de famille, l'adresse postale et un champ personnalisé pour les motivations des volontaires.
- Un profil contenant des champs personnalisés sur les préférences alimentaires qui peut être ajouté aux pages d'inscription pour tout événement où des repas seront servis.

Dans l'exemple ci-dessous, un profil est utilisé pour recueillir des informations d'adresse sur une page de don.

![image](/img/baykeeper-profile.png)

### Affichage d'informations sur les pages publiques

Un profil peut afficher des informations, à partir de la base de données, sur des pages publiques. Cela permet d'économiser du temps, car vous n'avez plus à saisir des informations dans votre base de données, plutôt que dans votre base de données *et* sur votre site Web.

Par exemple, une organisation peut afficher un répertoire d'adhérents consultable sur son site Web, mis à jour automatiquement dès qu'un nouveau membre est enregistré. De même, une organisation qui veut remercier ses donateurs publiquement peut inscrire leurs noms sur une page Web dès que les contributions sont versées.

Une mini étude de cas: Native Americans in Philanthropy (NAP) voulait créer un répertoire d'adhérents que leurs membres pourrait utiliser pour rechercher et se connecter les uns avec les autres. Avant CiviCRM, ils créaient un répertoire d'impression annuel très coûteux et l'envoyait par la poste à chaque membre. Ce processus était long et onéreux, et certaines données étaient périmées avant que les membres ne reçoivent leur répertoire. L'utilisation d'un profil consultable sur leur site Web a généré d'importantes économies de ressources. Le site Web est devenu un portail permettant aux membres de se connecter entre eux et a contribué à faire progresser leur mission dans de meilleures conditions.

Les détails sur l'utilisation des profils de cette façon sont inclus plus loin dans ce chapitre.

### Personnalisation de votre interface utilisateur

Les formulaires de profil peuvent également être utilisés comme formulaires simplifiés de saisie de données. Si vous avez des bénévoles ou des stagiaires qui effectuent une saisie manuelle de données pour votre organisation, vous pouvez faciliter leur tâche en créant un formulaire de profil qui ne montre que les champs dont ils ont besoin pour saisir. Cela simplifie grandement la saisie des données et réduit la possibilité de saisie incorrecte des données.

Vous pouvez également utiliser un profil pour afficher les champs sélectionnés dans les résultats d'une recherche avancée. Par exemple, vous pouvez créer un profil qui inclut le champ numéro de téléphone et un champ personnalisé pour les intérêts des bénévoles. Lorsqu'il est utilisé pour afficher les résultats de recherche, il proposera une liste de contacts à appeler pour votre coordonnateur de bénévolat.

Les détails sur l'utilisation des profils de cette façon sont disponibles dans le chapitre *Personnaliser l'interface utilisateur* de *Configuration initiale*.

### Mise à jour de plusieurs enregistrements en même temps

Il est souvent nécessaire de mettre à jour un grand nombre d'enregistrements à la fois. Par exemple, après un événement, vous pouvez avoir une liste de présence importante, et vous voulez enregistrer toutes les personnes inscrites comme Présent ou Absent mais aussi mettre à jour le champ de remerciement envoyé pour une semaine de dons...cela en une seule fois 

Les actions qui vont vous permettre de mettre à jour plusieurs enregistrements en même temps sont disponibles dans le menu déroulant **Actions** pour la plupart des types de résultats de recherche. (Recherche, Recherche avancée, Rechercher des contributions, Trouver des membres, Rechercher des participants et Rechercher des activités) et des listes de participants à l'événement générées à partir de l'écran Gérer les événements.

La fonction **Update multiple ...** affiche une vue de vos résultats de recherche contenant les champs de votre profil et vous permet de modifier le contenu des champs sur un seul écran et de les enregistrer tous à la fois. Les détails sur l'utilisation de profils de cette façon sont inclus plus loin dans ce chapitre.

### Gérer les listes de courriels

Une autre utilisation de Profils est de présenter un formulaire où les personnes peuvent s'inscrire pour recevoir des courriels, newsletter et diverses infos de votre organisation. Les groupes que vous utilisez pour suivre des listes de diffusion différentes peuvent être ajoutés sous forme de cases à cocher et lorsque les visiteurs de votre site Web soumettent le formulaire, ils sont automatiquement ajoutés aux listes de courrier électronique qu'ils ont cochées.

Pour plus d'informations sur l'utilisation des profils pour gérer les listes de diffusion, reportez-vous au chapitre *Configuration* de la section *Email* de ce manuel.

## Planification de vos profils

Parce que les profils peuvent être utilisés à des fins différentes, il ya beaucoup de choix à faire et de paramètres à configurer lors de leur mise en place. Il ya des paramètres pour le profil dans son ensemble et des paramètres pour chaque champ que vous ajoutez, ainsi que le choix de ces champs. Les choix que vous faites sur un aspect affecteront les choix que vous pouvez faire sur les autres. Par exemple, certains types de profils limitent les types de champs que vous pouvez inclure et certaines combinaisons de champs ne sont autorisées dans aucun type de profil. En raison de cette complexité, il est important de comprendre les conséquences de certains paramètres et de planifier soigneusement ce que vous utiliserez dans votre profil et ce dont vous avez besoin avant de le créer. Vous devrez peut-être faire probablement quelques essais ou erreurs avant de trouver la bonne solution pour réaliser votre objectif.

Voici quelques conseils sur les champs qui peuvent être ajoutés à un profil:

- Les profils utilisés pour les affichages de recherche peuvent contenir uniquement les champs des enregistrements de contact (et les différents types de contact, par exemple individuels).
- Les champs de contact sont disponibles dans tous les profils. Toutefois, vous ne pouvez pas mélanger les champs de différents types de contact (par exemple, individuel et organisation).
- Pour ajouter des champs (comme l'adresse ou l'e-mail) qui s'appliquent à plusieurs types de contacts, choisissez les champs de Contacts plutôt que le type spécifique. Le menu des champs Organisation, par exemple, contient uniquement les champs qui ne s'appliquent pas également à d'autres types de contacts.
- Sauf dans les profils de résultats de recherche, vous pouvez combiner les champs de contact avec les champs d'un et d'un seul autre type d'enregistrement : Activité, Participants, Contributions et Adhésion.
- Si vous essayez de combiner des champs avec une combinaison non prise en charge de types d'enregistrements, vous obtiendrez une erreur lorsque vous essayez d'enregistrer le champ.

## Création et gestion de profils

La création d'un profil est un processus en plusieurs étapes. Tout d'abord, vous créez le profil et choisissez ses paramètres. Il existe des paramètres de base et des paramètres avancés. Ensuite, vous ajoutez les champs et choisissez également ses paramètres.

### Création d'un profil et compréhension des paramètres de profil

Cette section vous guide à travers tous les paramètres du profil et explique comment ils affectent le fonctionnement de vos profils. Comme vous le voyez, vous pouvez remarquer que la liste des paramètres est assez longue. Il est important de comprendre que la plupart des paramètres s'appliquent uniquement à un type d'utilisation de profil. Chaque fois que vous créez un profil, vous serez en mesure d'ignorer de nombreux paramètres, car ils ne s'appliquent pas à votre utilisation prévue.

1. Allez dans : **Administrer> Personnaliser les données et les écrans> Profils** et cliquer sur **Ajouter un profil**.
2. **Nom du profil** : Donnez au profil un nom significatif.
3. **Utilisé pour** : Vos choix sont "Formulaire ou liste autonome" ou "Vue des résultats". Vous pouvez cocher plusieurs cases dans ce champ pour rendre votre profil disponible à plusieurs utilisations. N'oubliez pas que la vérification des "Vues de résultats" limitera vos choix de champ aux enregistrements de type Contact et Contact uniquement.
4. **Numéro d'ordre** : Ce champ détermine l'ordre dans lequel les profils sont présentés lorsque plusieurs profils sont inclus dans une page. Les nombres inférieurs sont affichés devant des nombres plus élevés. Le champ est automatiquement rempli lors de la création d'un Profil. Changer le nombre si vous le souhaitez.
5. **Aide avant formulaire** et **Aide après formulaire** : Ces champs vous permettent d'écrire du texte qui apparaît avant ou après votre profil pour guider les utilisateurs à remplir les formulaires.
6. **Ce profil CiviCRM est-il actif ?** : Cette case est cochée automatiquement. C'est ce qui permet au profil d'apparaître comme options pour l'insertion dans des formulaires et l'utilisation de la fonction de mise à jour de lot. Lorsque vous créez des profils, vous devez évidemment la laisser cochée. Ultérieurement, si vous souhaitez supprimer un profil vous pouvez modifier le profil et désélectionner cette case.

### Paramètres avancés

Les profils ont un certain nombre de paramètres avancés qui sont applicables dans des contextes différents. Tout ce qui est répertorié sous Paramètres avancés s'applique à tous les profils. Certains ne s'appliquent qu'à des utilisations spécifiques du profil. Vous pouvez ignorer tous les paramètres qui ne s'appliquent pas à la façon dont vous utiliserez votre profil. Pour accéder aux paramètres avancés, cliquez sur la barre de paramètres avancés gris et un ensemble de champs apparaîtra

#### **Restreindre les listes à un groupe spécifique ?**

Ceci est important uniquement pour les profils qui seront utilisés pour afficher des informations sur votre site Web (par exemple, si vous autorisez les visiteurs Web à rechercher vos données, comme dans un répertoire d'adhésion).

1. Sélectionnez le groupe dont vous voulez afficher les informations à partir du menu déroulant de ce champ. Par exemple, si vous souhaitez afficher un répertoire de membres actifs, créez un groupe dynamique de tous les membres ayant un statut de nouveau, de courant et de grâce.
2. Choisissez le groupe intelligent dans ce champ. (Rappelez-vous que les groupes dynamiques sont des listes d'enregistrements et lors de l'ajout de nouvelles appartenances, le contact correspondant sera automatiquement inclus dans le répertoire.)
3. Si vous ne choisissez pas un groupe dans le menu déroulant de ce champ, par défaut CiviCRM permettra une recherche pour afficher chaque enregistrement de votre base de données. Dans la plupart des cas, c'est une très mauvaise idée !, car vous ne voulez probablement pas que n'importe qui, visitant votre site Web, sache qui est dans votre base de données entière.

#### **Ajouter de nouveaux contacts à un groupe**

Tous les *nouveaux* contacts qui correspondent à ce profil seront ajoutés a un groupe. Vous pouvez, par exemple, ajouter une personne qui remplit votre formulaire d'inscription à un groupe de bénévoles. Notez que, par défaut, les contacts ne reçoivent aucune confirmation quand ils ont été ajoutés à ce groupe ou quand ils doivent valider leur adresse électronique. Pour que les contacts qui remplissent le formulaire de profil reçoivent un courriel, allez à **Administer > CiviMail > CiviMail Component Settings** et cochez la case **"Activer le double opt-in pour les profils qui utilisent le paramètre "Ajouter au groupe" "**. Ils doivent répondre (opt-in) avant d'être ajoutés au groupe.

![Screen shot of dobule opt-in setting](/img/organizing-data-double-opt-in.png)

Notez que si vous souhaitez proposer plus d'un groupe, il est préférable d'utiliser le champ Profil de groupe.

#### **Notifier quand le formulaire de profil est envoyé**

Ce paramètre, qui est applicable uniquement lors de l'utilisation d'un profil en tant que formulaire d'inscription, vous permet d'envoyer un message automatiquement chaque fois que le formulaire est envoyé. Par exemple, votre coordonnateur des bénévoles peut vouloir envoyer un courriel chaque fois que quelqu'un remplit le formulaire d'inscription des bénévoles. Entrez simplement l'adresse e-mail dans le champ. Si vous souhaitez envoyer un e-mail à plusieurs adresses, séparez-les par une virgule.

#### **URL de redirection**

Ceci s'applique uniquement aux profils qui sont utilisés comme des formulaires autonomes. La redirection ne s'applique pas lorsque le profil est incorporé dans un formulaire d'inscription ou de contribution. Le champ URL de redirection vous permet de diriger les personnes vers une page Web spécifique après avoir soumis un formulaire. Par exemple, vous pouvez créer une page Web qui remercie les gens de soumettre leurs informations. Si ce champ est laissé vide, les gens seront dirigés vers une page qui affiche les informations qu'ils viennent d'entrer.

#### **Annuler l'URL de redirection**

S'exécute exactement de la même manière que l'URL de redirection, sauf qu'elle s'applique lorsque les utilisateurs annulent leur soumission de formulaire.

#### **Inclure reCAPTCHA ?**

Concerne lorsque les profils sont remplis par des utilisateurs anonymes. CAPTCHA est un type de logiciel anti-spam qui oblige le visiteur à remplir le texte affiché dans un fichier graphique. Cela empêche les robots automatisés de naviguer sur le Web et de remplir un formulaire. Il est fortement recommandé de l'inclure.

Vous devez configurer un compte reCAPTCHA et saisir quelques informations de configuration dans CiviCRM pour utiliser cette fonctionnalité. Allez dans **Administer> Paramètres système> Undelete, Logging et ReCAPTCHA** pour configurer votre compte. Les instructions d'inscription sont incluses sur cette page.

#### **Option d'enregistrement de compte utilisateur Drupal**

Ce paramètre s'applique aux profils qui sont utilisés dans les pages publiques et détermine si les personnes peuvent ou doivent utiliser votre formulaire pour avoir un compte utilisateur sur votre site Web avant de soumettre les informations du formulaire. Cela peut être utile pour s'assurer que les personnes qui doivent s'inscrire à un compte d'utilisateur peuvent devenir membre ou s'inscrire à un événement.

#### **Option d'inscription au compte utilisateur WordPress**

Comme Drupal, Wordpress permet aux profils CiviCRM de créer des comptes comme décrit ci-dessus. Dans WordPress **Paramètres> Général** "Adhésion [] N'importe qui peut s'inscrire" doit être cliqué.

#### **Que faire en cas de doublon**

Ce paramètre s'applique aux profils utilisés dans les pages publiques. Il contrôle ce qui se passe lorsque les données de contact fournies par le profil correspondent à un enregistrement déjà existant. Vous devez choisir une de ces options, par défaut «Avertissement d'émission et ne pas enregistrer» est choisi. La correspondance entre les profils est utilisée sur la règle de déduplication **non supervisée** (pour plus d'informations sur les règles de déduplication, voir le chapitre *Deduping and Merging* de la section *Travailler avec vos données*). Notez que s'il ya plusieurs contacts correspondants, le premier enregistrement correspondant est utilisé.

Voici les options et leurs effets sur le fonctionnement de votre formulaire:

- "Avertissement de problème et ne pas enregistrer" Cette option est ignorée si le Profil est incorporé dans une contribution en ligne, une inscription d'adhésion ou un formulaire d'inscription à un événement. Dans ces cas, une correspondance de contact entraîne la liaison de la transaction au contact correspondant. Dans d'autres cas, l'utilisateur reçoit un message indiquant qu'un enregistrement existe déjà dans la base de données et qu'il ne pourra pas le soumettre.
- "Mettre à jour le contact correspondant" ajoute les nouvelles informations du formulaire à l'enregistrement de contact et, s'il ya des champs de formulaire qui sont déjà remplis dans l'enregistrement, écrase les champs d'enregistrement existants. Par exemple, si le formulaire inclut des champs d'adresse, le texte que l'utilisateur entre dans le formulaire remplacera ce qui était déjà dans les champs d'adresse de la base de données.
- "Autoriser la création de contact en double" ignore les correspondances potentielles et crée un nouvel enregistrement de contact pour tous les formulaires soumis. Cela signifie que toutes les soumissions de formulaire seront enregistrées et qu'aucune donnée ne sera écrasée. Cependant, ceci peut produire beaucoup d'enregistrements en double qui devront être supprimés plus tard (voir le chapitre *Deduping and Merging* dans la section *Working with Your Data*).

#### **Recherche de proximité**

Cela s'applique si vous utilisez le profil d'un répertoire consultable. Si activé, il s'ajoute un bloc de recherche de proximité aux critères de recherche. Ce bloc contient un champ pour l'adresse de début, et un autre qui permet à l'utilisateur de définir un rayon de recherche (à quelle distance de l'adresse de départ voulez-vous rechercher). Choisissez "Aucun" si la recherche de proximité n'est pas pertinente pour votre utilisation ou "Facultatif" si vous souhaitez offrir une recherche de proximité à vos utilisateurs, et "Obligatoire" si vous souhaitez forcer l'utilisateur à saisir une adresse de début et un rayon de recherche.

#### **Activer le mappage pour ce profil?**

Cela s'applique uniquement si vous utilisez le profil d'un répertoire consultable. Une carte de localisation sera ajoutée aux résultats de la recherche.

#### **Inclure les liens d'édition de profil dans les résultats de recherche?**

Cela s'applique uniquement si vous utilisez le profil d'un répertoire consultable. Dans les listes de résultats il est ajouté un lien pour modifier les champs Profil dans les enregistrements de contact retournés. Seuls les utilisateurs ayant la permission de modifier les contacts de résultat verront ce lien

#### **Inclure les liens d'informations de compte d'utilisateur Drupal dans les résultats de recherche?**

Cela s'applique uniquement si vous utilisez le profil d'un répertoire consultable. Un lien sera inclus dans les résultats des informations de compte d'utilisateur Drupal des contacts résultants (c'est-à-dire leur page Mon compte). Ce lien sera inclus uniquement pour les contacts de résultat qui ont un compte d'utilisateur sur votre site Web.

Une fois que vous avez enregistré les paramètres de profil, vous pouvez ajouter des champs au profil. Si vous envisagez de référencer des champs personnalisés dans un formulaire de profil, assurez-vous que ces champs ont été créés.

## Ajout de champs et sélection des paramètres de champ dans les Profils

Cette section vous guide à travers tous les paramètres de champs et explique comment ils affectent la façon dont vos profils fonctionnent. Comme pour les paramètres de profil en général, il n'est pas nécessaire d'en tenir compte à chaque utilisation.

1. Cliquez sur **Ajouter champ**.
2. **Nom du champ** : Choisissez le type d'enregistrement du champ désiré dans le menu déroulant **- select -**. Cela affichera Un menu déroulant secondaire affichera tous les champs disponibles pour ce type d'enregistrement. Choisissez le champ que vous souhaitez ajouter à votre profil.
3. **Étiquette de champ** : Il s'agit de l'étiquette de champ qui s'affichera sur toutes les utilisations de votre profil. Il est initialisé avec l'étiquette de champ par défaut. Toutefois, les étiquettes de champs par défaut sont souvent déroutantes pour les utilisateurs de vos formulaires, vous pouvez donc les réécrire ici. Par exemple, le champ "Postal Code"  peut être renommé "Code postal" si vos utilisateurs sont plus familiers avec ce terme.
4. **Obligatoire?** : Cochez cette case pour rendre le champ  obligatoire chaque fois que le Profil est utilisé. Ceci est particulièrement utile lorsque vous voulez vous assurer que certaines informations (par exemple, Prénom, Nom de famille, Email) sont toujours incluses dans une soumission de formulaire. (Ceci n'est pas pertinent pour les utilisations des vues de recherche [connues sous la forme de résultats de recherche).
5. **Afficher uniquement?** : Cochez cette case pour permettre aux utilisateurs d'afficher ce champ, mais pas de le modifier. Si votre profil est utilisé pour afficher des résultats de recherche, les champs marqués View Only ne seront pas inclus. Ce paramètre n'est pas pertinent lorsqu'un Profil est utilisé uniquement pour collecter des informations.
6. **Visibilité** : Si le Profil est utilisé pour un répertoire consultable, définissez la Visibilité de tous les champs que vous souhaitez inclure dans le formulaire de recherche dans "Pages publiques" ou "Pages publiques et Liste"s. Pour les champs qui seront utilisés sur les formulaires d'inscription, définissez Visibilité sur "Utilisateur et Admin uniquement". Cela garantit que les autres visiteurs du formulaire ne peuvent pas afficher les données de la base de données. Pour utiliser les champs des vues de recherche, vous devez définir la visibilité sur les "pages publique"s ou sur les "pages et les listes publiques". Le choix de l'une des options de la page publique affiche deux paramètres supplémentaires:
      - **Interrogeable?** : Ceci s'applique uniquement aux utilisations de répertoire consultables. Cochez la case si vous souhaitez inclure le champ dans le formulaire de recherche.
      - **Colonne de résultat** : Ceci s'applique uniquement aux vues de recherche (connues sous le nom de résultats de recherche). Si choisi, le champ n'apparaîtra pas dans votre vue de recherche.
7. **Aide avant et après le champ** : Ces champs vous permettent d'écrire du texte qui apparaît dans l'interface utilisateur pour guider les gens dans le remplissage des formulaires. La pré-aide de champ apparaît en ligne. 
8. **Numéro d'ordre** : Vous pouvez utiliser ce champ pour contrôler l'ordre dans lequel les champs s'affichent dans le profil. Les nombres inférieurs sont affichés devant des nombres plus élevés.
9. **Actif?** : Laissez cette case cochée pour vous assurer que le champ s'affiche lorsque le Profil est utilisé.
10. Cliquez sur **Enregistrer et Nouvelle entrée** pour ajouter d'autres champs au Profil, ou **Enregistrer** si vous n'avez plus de champs à ajouter.

## Gestion des profils

Tous vos profils sont disponibles pour l'affichage et l'édition dans **Administer> Personnaliser les données et les écrans> Profils**. Vous pouvez ajouter des champs et modifier les paramètres du champ (dans **Champs**) et modifier les paramètres du profil (dans **Paramètres**). Vous pouvez également voir comment vos profils apparaissent, obtenir des liens et intégrer le code pour vos profils et copier les profils à utiliser comme base pour créer d'autres profils (dans ** plus **).

## Utilisation des profils

Cette section contient des instructions spécifiques pour les différentes utilisations de profil décrits ci-dessus.

### Formulaires autonomes avec profils

Dans Drupal et Joomla! il y a deux façons d'utiliser des formulaires autonomes dès que vous avez créé votre Profil conformément aux instructions ci-dessus:

- Utiliser la page créée automatiquement par CiviCRM pour contenir le profil. 
     Allez au menu : **Administrater> Personnaliser les données et les écrans> Profils**. Cliquez sur le lien **plus** de votre profil et choisissez **Utiliser le mode de création de profil** dans le menu contextuel. Vous pouvez ensuite publier ce lien où vous le souhaitez: dans un courriel, sur un blog, etc.
- Coller le code HTML du formulaire dans une page que vous avez construite sur votre site Web. 
     Pour Obtenir le code HTML allez à  **Administer> Personnaliser les données et les écrans> Profils**.  Cliquez sur le lien **plus** de votre profil et choisissez **Fragment de formulaire HTML** dans le menu contextuel. Copiez le code qui apparaît sur l'écran suivant et collez-le où vous le souhaitez.

Dans WordPress, il ya une troisième voie supplémentaire. Lors de la création ou de la modification d'un message, cliquez sur le bouton CiviCRM pour insérer un code court CiviCRM dans le message.

![image](/img/2013-09-04_15-29-47_1.png)

Dans le formulaire contextuel, sélectionnez Profil comme élément frontal souhaité.

![image](/img/2013-09-04_15-15-35.png)

Utilisez le second widget de sélection pour spécifier le profil que vous souhaitez utiliser. Enfin, sélectionnez le but du formulaire (créer, modifier ou afficher) et cliquez sur Insérer un formulaire.

![image](/img/2013-09-04_15-16-45.png)

### Champs de valeurs multiples dans les profils

Les ensembles de champs personnalisés à plusieurs valeurs vous permettent d'avoir plusieurs jeux de données personnalisées par contact. Ils sont utiles pour modéliser des données qui se répètent, par exemple, des données d'expérience de travail. Vous pouvez afficher ces champs personnalisés à plusieurs valeurs via des profils. Dans la capture d'écran ci-dessous, nous avons créé un profil qui est utilisé pour collecter les données de nom et d'expérience de travail. Notez que les données personnalisées multi-valeurs apparaissent légèrement différemment dans le profil pour faciliter l'ajout, l'édition et la suppression de plusieurs instances de ces enregistrements.

![image](/img/multi-value-profile.png)

### Création d'annuaires avec des profils

Pour mettre un annuaire (ou une liste de contats) sur votre site Web :

1. Créez votre profil comme décrit ci-dessus. Dans le profil, allez dans l'onglet des paramètres avancés. Ces paramètres sont particulièrement utiles lors de l'utilisation de profils pour les répertoires.

- **Autoriser la géolocalisation pour ce profil ?** : Cette fonctionnalité, vraiment cool, disponible dans CiviCRM donne aux visiteurs la possibilité de mapper les contacts de votre liste en utilisant les cartes Google ou Yahoo!. Ils peuvent alors obtenir des plans et itinéraires vers l'adresse d'un enregistrement de façon dynamique. Pour utiliser cette fonctionnalité, vous devez avoir activé le mappage sous **Administer> Paramètres système> Mappage et géocodage**.

- ** Inclure les liens d'édition de profil dans les résultats de recherche**  : Cochez cette case si vous souhaitez inclure un lien dans les listes pour permettre aux utilisateurs d'éditer des données dans les champs du profil. Seuls les utilisateurs ayant la permission de modifier le contact verront ce lien. Le plus souvent, vous n'aurez pas besoin d'activer ce paramètre, car il n'est pas couramment utilisé comme scénario.
 
- **Inclure les liens d'information sur le compte utilisateur (Drupal ou Joomla) dans les résultats de recherche ?** : Cochez cette case si vous souhaitez inclure un lien dans les listes de contacts pour afficher les informations de compte d'utilisateur d'un contact (par exemple, leur page "Mon compte"). Ce lien ne sera inclus que pour les contacts disposant d'un compte d'utilisateur sur votre site Web.
 
    ![profile_adv_settings](/img/CiviCRM-CapturingExposing-buildprofile-profile_adv_settings-en.jpg "profile_adv_settings")

Vous pouvez alors inclure les champs qui composeront la liste. Pour les profils utilisés comme listes, vous disposez d'un contrôle total sur les champs suivants qui:

- sont consultables dans le répertoire
- apparaissent dans les colonnes des résultats de votre recherche
- apparaissent dans la page Détails de l'enregistrement.

Les options importantes que vous devez configurer dans les champs à des fins d'annuaire sont indiquées ci-dessous:

![directory_fields](/img/CiviCRM-CapturingExposing-buildprofile-directory_fields-en.jpg "directory_fields")

- Les champs visibles de votre liste doivent être définis sur **Pages publiques** ou **Pages publiques et listes**. La différence entre ces deux options est que celles configurées en tant que Pages Publiques et Listes auront le champ en vue détaillée directement lié. ce qui  permettra à l'utilisateur de générer une recherche de suivi pour d'autres enregistrements qui ont également la même valeur de champ. Par exemple, vous pouvez définir "Ville" comme "Pages publiques et listes". Lorsque l'utilisateur effectue une recherche et affiche les détails d'un enregistrement, il peut cliquer sur la valeur de la ville et effectuer une recherche immédiate. La recherche s'exécute comme s'ils avaient sélectionné cette ville dans l'écran de recherche de profil.
- L'option **Interrogeable** détermine si les visiteurs de votre liste peuvent rechercher par ce champ. Dans les utilisations courantes d'une liste, presque tous les champs sont définis pour être recherchés. Plus vous définissez de champs de recherche, plus vous fournissez de puissance à vos visiteurs pour trouver les informations dont ils ont besoin.
- La case **Colonne des résultats** détermine si le champ est affiché sous la forme d'une colonne dans la liste des résultats. Par exemple, votre liste peut avoir un champ pour le site Web. Si vous définissez le champ du site Web pour apparaître dans la colonne des résultats, il apparaîtra bien dans le tableau des résultats. Si vous ne cochez pas la colonne des résultats, le champ apparaît toujours en mode d'affichage dans un enregistrement. En d'autres termes, la case "Colonne de résultats?" permet au champ d'apparaître dans la colonne de résultats ET en mode d'affichage de détail.

L'image ci-dessous montre le mode de recherche pour notre liste d'adhésion.

![Member Directory SearchForm](/img/CiviCRM-CapturingExposing-buildprofile-MemberDirSearchForm-en.png "MemberDirSearchForm")

Dès que vous avez lancé la recherche, vous obtenez ce jeu de résultats. Les champs de profil dont les Colonnes de Résultats ont été cochés sont affichés dans la liste..

![MemberDirResults](/img/CiviCRM-CapturingExposing-buildprofile-MemberDirResults-en.png "MemberDirResults")

En cliquant sur le lien de vue, vous obtiendrez plus de détails sur le composant, affichant tous les champs du profil.

![Profile MemberView](/img/CiviCRM-CapturingExposing-buildprofile-MemberView-en.png "MemberView")

Comme nous l'avons vu, la construction d'une liste pour votre site Web peut fournir de précieux outils à vos utilisateurs.

### **Lien vers votre liste**

Vous avez plusieurs options pour créer un lien vers votre liste et l'afficher sur votre site:

- **Drupal** : pour créer un lien vers la page de recherche d'annuaire vous pouvez utiliser ce chemin: http://www.myorganization.org/civicrm/profile?reset=1&gid=N où N est l'ID de la liste de profil.
    - Si vous ajoutez **& force = 1** à l'URL ci-dessus, vous affichez directement le résultat.
    - Si vous ajoutez **& force = 1 & search = 0**, vous masquez les critères de recherche et affichez directement le résultat.
 - **Joomla!:**  utilisez le Gestionnaire de menus pour créer un élément de menu frontal. Après avoir créé un nouvel élément de menu, sélectionnez CiviCRM et choisissez l'option de recherche de profil. Dans le volet Paramètres, choisissez le profil spécifique à utiliser.
 - **Wordpress :** cette fonctionnalité n'est pas encore implémentée.
- Vous pouvez également préremplir des critères de recherche dans l'URL. Ces options sont décrites ici:
    [http://wiki.civicrm.org/confluence/display/CRMDOC/Linking+Profiles](http://wiki.civicrm.org/confluence/display/CRMDOC/Linking+Profiles)
    
### Mise à jour de plusieurs enregistrements en même temps

Vous pouvez **Mettre à jour plusieurs adhésions** à partir des résultats d'une recherche **Trouver des adhésions** ou des résultats de recherche avancés lorsque **Afficher les résultats en tant que** est défini sur **Membres**. Vous aurez besoin d'un profil contenant uniquement les champs d'adhésion concernés.

De même, vous avez besoin de contacts, de contributions, d'activités ou de résultats de recherche de participants et de profils contenant uniquement des contacts, des contributions, des activités ou seulement des champs de participants pour mettre à jour plusieurs contacts, plusieurs contributions, plusieurs activités ou plusieurs participants respectivement.

Vous pouvez mettre à jour jusqu'à 100 enregistrements en même temps en utilisant les fonctions **Update multiple ...**.

**Exemple:**

Vous avez un champ de contact personnalisé appelé «Niveau de compétence en plongée» et vous venez d'exécuter un cours de plongée intermédiaire. Vous souhaitez définir le niveau de compétence «Plongée» à «Intermédiaire» pour toutes les personnes qui ont suivi le cours.

Accédez à l'écran **Recherche avancée** et définissez les filtres appropriés dans l'accordéon Evenement. Laissez **Afficher les résultats comme** défini sur **Contacts** comme vous souhaitez mettre à jour un champ personnalisé de contact. Cliquer sur **Rechercher**.

Vous accédez à l'écran "Mettre à jour plusieurs contacts".

  ![Update Multiple Records](/img/update-multiple-records.PNG)

Dans la liste déroulante, choisissez le Profil que vous souhaitez utiliser et cliquez sur **Continuer**.

L'écran suivant contiens une grille. Chaque ligne indique le nom du contact et les champs de votre profil. Vous devez mettre à jour les valeurs de champ pour chaque contact si besoin.

![Update Multiple Records Profile View](/img/update-multiple-records-profile.PNG)

Pour définir si un champ à la même valeur pour toutes les lignes, entrez cette valeur pour le premier contact, puis cliquez sur l'icône Copier (l'image de deux documents qui est à côté de chaque titre de colonne). La valeur sera automatiquement copiée dans tous les enregistrements affichés.

Cliquez sur **Mettre à jour les contacts** pour enregistrer vos changements ou sur **Annuler** pour annuler les modifications.
 
**Limites de mise à jour des lots**

-   Vous ne pouvez pas effectuer de mises à jour par lots pour différents types de contacts (par exemple, individus et organisations) en même temps.
-   Si vous souhaitez mettre à jour les champs des participants, vous devez effectuer la mise à jour à partir de la recherche Trouver les participants (et inclure uniquement les champs participant à votre profil).
-   Vous pouvez effectuer une mise à jour par lot pour un maximum de 100 enregistrements à la fois. Si vous constatez que la mise à jour d'un lot de 100 enregistrements prend beaucoup de temps, il peut être plus rapide de mettre à jour 4 lots de 25 enregistrements plutôt qu'un lot de 100 enregistrements.

### Afficher/Modifier un compte d'utilisateur/un nouvel enregistrement d'utilisateur avec Profils

Pour les sites Web ayant des utilisateurs connectés, vous pouvez permettre aux utilisateurs de fournir des informations supplémentaires lorsqu'ils créent un compte sur votre site Web. De même, lorsque les gens remplissent un formulaire de profil, vous pouvez les encourager à créer à un compte d'utilisateur.

Pour inclure un formulaire de profil lors du processus d'inscription de l'utilisateur:

1.  Créez un profil utilisé pour l'enregistrement d'utilisateur: 

    ![addprofile_usedfor_reg](/img/CiviCRM-CapturingExposing-buildprofile-addprofile_usedfor_reg-en.jpg "addprofile_usedfor_reg")
2.  Ajoutez les champs que vous souhaitez que les gens remplissent au fur et à mesure qu'ils s'inscrivent, en utilisant le même processus décrit ci-dessus. Assurez-vous que la visibilité est définie sur Pages publiques.    

**Inclure des profils dans l'écran Drupal "Mon compte"**

Vous pouvez intégrer un ou plusieurs profils CiviCRM directement dans l'écran Mon compte de Drupal. Cela permet aux utilisateurs connectés d'examiner et de mettre à jour leurs informations chaque fois qu'ils visitent leur page Mon compte.

Pour créer un profil à cette fin:

1.  Créez un nouveau profil ou accédez à un profil existant, puis cliquez sur Paramètres.
2.  Sélectionnez View / Edit User Account in Used For.
3.  Cliquez sur Save.
4.  Ajoutez les champs que vous souhaitez pour que les utilisateurs puissent modifier "Mon compte" à partir de leur page Drupal .

Remarque: le profil doit inclure uniquement des champs relatifs au type de contact Individuel.

**Nouvelle création de compte lors de l'inscription de profil**

Si vous voulez que les visiteurs créent un compte Drupal ou Joomla! lors du remplissage d'un profil, vous pouvez activer cette option avec l'option "Enregistrement de compte d'utilisateur" sous **Personnaliser les données et les écrans>Profils**  Cliquez sur **Paramètres** dans un profil. Les utilisateurs anonymes (non connectés) seront invités (ou obligés) de créer un compte lorsqu'ils visiteront le profil. Les utilisateurs connectés verront simplement les champs du profil.

![Profile user registration options](/img/CiviCRM-CapturingExposing-buildprofile-CMS_user_reg-en.png "CMS_user_reg")

Vous devez inclure un champ "Adresse e-mail principale" dans le profil pour que cette fonctionalité agisse correctement. C'est également vrai lorsque le profil est incorporé dans une page de contribution en ligne ou une page d'enregistrement d'événement. Par conséquent, vous pouvez inviter ou forcer les visiteurs anonymes à créer un compte lorsqu'ils s'inscrivent à un événement.

### Inclure un profil dans les formulaires des composants CiviCRM

Vous pouvez aussi définir certains champs  à inclure dans l'enregistrement des événements et les pages de contribution. La seule différence importante est que vous pouvez inclure dans votre profil des champs spécifiques aux enregistrements des participants (pour les formulaires d'inscription à l'événement) et aux contributions (pour les pages de contribution). Vous trouverez des informations sur les profils dans les pages de contribution, les pages d'inscription d'événements et les pages d'inscription des membres dans le chapitre  *Paramétrage* de *Contributions*, *Événements* et *Adhésions* .

Autres sources d'information sur les profils
-------------------------------------------

-   Dans le chapitre *Personnalisation de l'interface utilisateur* de *Configuration initiale* 
-   Dans le chapitre *Paramétrage* de *Email*
-   Dans le chapitre *Paramétrage* de *Contributions* 
-   Dans le chapitre *Paramétrage* de *Evenements* 
-   Dans le chapitre *Paramétrage* de *Adhésions* 

Alternatives aux profils
------------------------

Comme vous pouvez le constater les profils peuvent être utilisés pour de nombreuses utilisations différentes. Il convient de garder à l'esprit qu'il existe d'autres approches pour bon nombre de cas d'utilisation. Les solutions de rechange dont vous disposez dépendent du CMS (Drupal, Joomla, Wordpress) que vous utilisez et de vos compétences. Chacun présente des avantages et des inconvénients. Nous avons répertorié quelques-uns ci-dessous pour que vous puissiez vous interroger.
As you have seen, profiles can be put to a lot of different uses. It is worth bearing in mind that there are alternative approaches for many of these use cases. The alternatives available to you depend on the CMS that you are using and your skill set, and have advantages and disadvantages We've listed a few of the common ones below for you to investigate.

### Alternatives spécifiques à Drupal

-   Le module Drupal Views peut être utilisé pour réaliser des affichages sophistiqués de données CiviCRM. Par exemple, vous pouvez afficher une liste de membres sur votre site public à l'aide de Views.
-   Le module Drupal Webform-Integration est le plus puissant constructeur de formulaire pour CiviCRM et comprend de nombreuses fonctionnalités manquantes dans les profils, comme la capacité de travailler avec plusieurs contacts, événements, appartenances et relations, et offre une plus grande flexibilité dans la façon dont les formulaires sont affichés, offrant la pagination , Le mode économique, le contrôle des spams avancé, et les champs conditionnels. Pour plus d'informations, consultez le chapitre Intégration Drupal ou https://drupal.org/project/webform_civicrm](https://drupal.org/project/webform_civicrm).
-   [](https://drupal.org/project/webform_civicrm) Vous pouvez ajouter des champs directement aux comptes d'utilisateurs Drupal sans utiliser de profil intégré. Ces champs ne seront pas disponibles dans CiviCRM mais ils seront disponibles dans Drupal. Donc selon la raison pour laquelle vous collectez ces informations, cela peut vous convenir.

### L'API Civicrm

Avec quelques compétences de codage de base (si vous avez envie et quelques compétences techniques, vous pouvez être en mesure de maitriser en un ou deux jours), vous pouvez utiliser l'API pour afficher de façon flexible les données sur votre site Web. Pour une introduction à l'utilisation de l'API : voir la * Documentation du développeur wiki * [(http://wiki.civicrm.org/confluence/display/CRMDOC/Develop](http://wiki.civicrm.org/confluence/display/CRMDOC/Develop)) 

