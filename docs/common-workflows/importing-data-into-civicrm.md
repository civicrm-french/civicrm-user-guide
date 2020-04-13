Importer des données dans CiviCRM
=================================

Beaucoup d'organisations possèdent des données dont la source ne provient pas de CiviCRM, telle que des plateformes de base de données utilisées à l'origine, des feuilles de calcul créées à la volée pour des événements spécifiques ou pour d'autres besoins, et des annuaires d'adresses courriel. Parce qu'entrer manuellement une grande quantité de données peut être fastidieux, CiviCRM fournit un moyen d'importer des données en masse si la source peut être exportée dans un format répandu tel qu'un fichier CSV (Comma Separated Value).

L'importation peut également être utilisée pour mettre à jour des données existantes. Ce point sera abordé dans la dernière section de ce chapitre.

Considérations avant d'importer
-------------------------------

Pour plus de détails sur la façon d'organiser vos données avant de les importer dans CiviCRM, merci de lire la section "Organiser vos données", et plus particulièrement "Comment organiser vos données".

Preparer les données à importer
-------------------------------

Importer des données requiert un soin et une attention extrêmes, nous allons par conséquent vous présenter certains concepts que vous devriez connaître avant de commencer votre première importation. Vous pouvez importer des données métier CiviCRM ainsi que des données personnalisées pour les contacts, mais aussi des données concernant la participation à des événements, des activités, des adhésions et des contributions. Ce chapitre se focalisera sur le processus d'importation pour les contacts. Les processus pour les autres données sont similaires.

Il existe deux façons d'importer des données :

-   Depuis des fichiers CSV. La plupart des bases de données et des applications de feuille de calcul (par ex. OpenOffice.org Calc, Google Spreadsheets, Microsoft Excel) peuvent créer et manipuler des fichiers dans ce format. Il est souvent plus facile de visualiser et nettoyer vos données lorsqu'elles sont dans un fichier CSV plutôt qu'encore enregistrées dans votre vieille base de données.

    Chaque colonne de votre fichier CSV doit correspondre à un champ de CiviCRM, assurez-vous donc d'associer une colonne propre à chaque type d'information.

    Selon votre pays ou région, les champs de votre fichier CSV peuvent être séparés par des points-virgules (;) à la place des virgules (,). Si c'est le cas, vous aurez besoin de changer la valeur du champ Séparateur de champs pour l'import / export dans les paramètres de localisation en allant dans le menu de navigation et en choisissant Administrer > Configurer > Paramètres généraux > Localisation.

-   Depuis une autre base de donnée SQL ou MySQL stockée sur le même serveur, en utilisant une requête SQL (cette option n'est à considérer que par les utilisateurs avancés maitrisant les techniques d'administration des serveurs et des bases de données). 

Si vous ne maîtrisez pas parfaitement la structure de vos données existantes et comment les faire correspondre aux champs CiviCRM, vous rencontrerez frustrations et problèmes durant vos essais d'importation. Merci de vous renseigner sur le type de chaque donnée dans les autres sections de ce manuel CiviCRM et de visiter la documentation en ligne de CiviCRM pour plus d'information :
[http://wiki.civicrm.org/confluence/display/CRMDOC/Importing+Data](http://wiki.civicrm.org/confluence/display/CRMDOC/Importing+Data)

Les règles et recommandations suivantes vous aideront à importer vos données en minimisant les problèmes :

-   Testez toujours l'importation de vos données avec un échantillon représentatif de vos enregistrements. Après avoir effectué le test, vérifiez vos enregistrements dans CiviCRM et assurez-vous que les données ont été importées et fonctionnent telles que vous l'escomptiez.    
-   Il peut être utile de créer un contact de test qui possède tous les attributs que vous avez définis dans votre jeu de données existant. Importez ensuite votre contact et vérifiez le résultat pour vous assurer que toutes les données sont correctement affichées dans CiviCRM.    
-   Lorsque, durant l'importation, vous faites correspondre les colonnes ou les champs de vos données sources vers les champs CiviCRM, ce dernier peut sauvegarder cette correspondance en tant que *table de correspondance* pour une utilisation future. Cela s'avère pratique si vous avez de multiples fichiers à importer ayant la même structure. Pour sauvegarder une table de correspondance pour une utilisation future, cliquez sur la case à cocher "Sauvegarder cette correspondance" en bas de l'écran Correspondance de champ de l'assistant d'importation et entrez un nom approprié et une description. Pour réutiliser une correspondance d'importation, sélectionnez-la depuis le menu déroulant Load Saved Field Mapping sur l'écran Import des données (étape 1) de l'assistant d'importation.    
-   Si vos importations dépasse le temps autorisé ou prennent trop de temps, essayez de découper vos fichiers en des lots plus petits. Si vous avez les autorisations adéquates sur votre serveur web, vous pouvez également augmenter les valeurs memory_limit et max_execution_time dans le fichier php.ini.
    
-   Vous pouvez ajouter lors d'un import des nouveaux (ou existants) groupes ou étiquettes à tous vos contacts importés. Tous les contacts au sein d'une même importation se verront attribués les mêmes groupes et étiquettes. Cette limitation a un double effet sur votre importation :
    -   Soyez sûr d'attribuer des groupes et des étiquettes qui soient applicables à chaque contact de votre jeu de données à importer. Si vous avez besoin d'attribuer des groupes ou des étiquettes contact par contact, importez-les par petits lots distincts dans lesquels tous les contacts partagent des groupes et des étiquettes identiques. Ou alors, vous pouvez créer des champs de données personnalisées dans CiviCRM contenant les noms des groupes et étiquettes que vous souhaitez attribuer à chaque contact. Après l'importation, vous pouvez ensuite effectuer des recherches par rapport à ces champs et utiliser les actions de traitements par lot "Ajouter Contacts au Groupe" ou "Étiquetter les contacts" sur les résultats de recherche.
    -   Vous pouvez utiliser cette fonctionnalité pour gérer vos importations. Ajoutez des contacts à un nouveau groupe ou une nouvelle étiquette indiquant de quel lot d'importation vos contacts font partie. Cela vous permettra d'identifier facilement quand un contact a été importé et supprimer une importation entière si nécessaire.
-   CiviCRM stocke les prénoms et noms dans deux champs séparés, ils devraient donc apparaître dans deux colonnes distinctes dans votre fichier CSV. C'est la même chose pour le nom de ville et code postal. La plupart des feuilles de calcul contiennent des outils qui automatise le processus de séparation d'une chaine de caractère en deux champs distincts.
-   Assurez-vous que vos noms de pays soient de la même forme que ceux stockés dans CiviCRM, par ex., "États-Unis" et non "États-unis d'Amérique", et "Royaume-Uni" et non pas "Grande-Bretagne".
-   Si vous importez plusieurs adresses de contact, la première adresse sera paramétrée comme adresse principale. Vous voudrez peut-être déplacer vos colonnes pour vous assurer que la bonne adresse devienne l'adresse principale. Vous aurez peut-être également besoin de séparer votre fichier d'importation de telle sorte que certains enregistrements aient telle adresse principale, tandis que d'autres en aient une différente.
-   Si vous importez des données dans des champs personnalisés de choix multiples (par ex. des cases à cocher ou des boutons radio), la source de vos données peut soit utiliser le libellé (que l'utilisateur peut voir sur le front end de CiviCRM) ou la valeur (qui est la valeur véritablement stockée dans la base de donnée par rapport au libellé). CiviCRM saura reconnaitre la donnée et l'importera de façon appropriée. Lorsque vous importez des champs métier de données à choix multiple, vous ne pouvez que spécifier la ou les valeurs dans votre source de données, et non le libellé.
-   Si vous mettez à jour des options à choix multiples, les nouvelles valeurs écraseront totalement le champ. Par exemple, si vous mettez à jour la valeur du champ Couleurs sur "orange" pour un contact qui a actuellement paramétré Couleurs sur "bleu", il en résultera que Couleurs sera paramétré sur orange et non orange et bleu.
-   Assurez-vous que la source de vos données utilise un format de date valide et que vous ayez sélectionné le même format de date dans la rubrique Format de date de l'assistant d'importation.  
-   Assurez-vous que tous les préfixes et suffixes de nom que vous utilisez aient été paramétrés dans l'interface d'administration (aller à Administrer > Listes déroulantes**** dans le menu de navigation).
-   Si vous prévoyez de faire des importations additionnelles de données liées à vos données de contact, par ex. des données de contribution, de participation à des événements, d'adhésion, vous pouvez vous faciliter la tâche en vous assurant que vos enregistrements de contact possèdent un identifiant unique qui soit également associé à vos données liées. Au moment de l'importation initiale de vos données de contact, importez ces identifiants uniques et faites les correspondre au champ ID externe de CiviCRM, vous pourrez ainsi utiliser ces identifiants pour importer ultérieurement des données liées aux enregistrements des contacts.
-   Master Address Belongs To est un champ d'importation spécial qui ne fonctionne qu'avec CiviCRM_Address.id. L'information à renseigner dans ce champ n'est disponible que directement depuis les tables de la base de données MySQL. Elles n'apparaissent nulle part dans CiviCRM, y compris dans les écrans de données, les liens urls, les profils et les exports. [De l'information sur la façon d'utiliser ce champ spécial est disponible sur le Wiki](http://wiki.civicrm.org/confluence/display/CRMDOC/Importing+Data+-+Notes "CiviCRM Wiki - Importing Data").

Champs obligatoires pour l'importation de contacts
--------------------------------------------------

Lorsque vous préparez vos données à importer, il est utile de savoir quels sont les champs obligatoires pour l'import. Il faudra être sûr que ces champs soient inclus dans votre fichier CSV. Vous trouverez ci-dessous une liste des champs requis. Ils sont marqués d'une étoile rouge dans l'interface. Au cas où vous avez peu de données, **sélectionner un champ suffit**. Le champ ID externe est le seul champ indispensable si vous souhaitez mettre à jour des contacts existants. Veuillez noter que le champ avec l'identifiant **(Correspond à Contact) est obligatoire pour des questions de dédoublonnage**.

-   **Courriel (Correspond à Contact)**
-   **Identifiant externe**
-   **Prénom**
-   **Nom**

Préparer un fichier CSV pour l'importation
------------------------------------------

Exemple de format .csv d'une feuille de calcul

![student_sample](/img/CiviCRM-student_sample-en.png)

Lorsque vous réfléchissez à la création de votre feuille de calcul, pensez aux données que vous allez collecter et planifiez l'en-tête de vos colonnes. Gardez en tête que vous pourriez avoir besoin de créer plus d'un fichier CSV et de faire plusieurs importations avant d'en avoir terminé.

Si vous prévoyez d'importer des données qui dépendent d'un contact spécifique, par ex. les informations de participation à un événement, les données de contributions, etc., vous aurez besoin de vous assurer que chaque enregistrement de contact possède un identifiant unique ou qu'il contienne au moins le prénom, le nom et l'adresse courriel pour pouvoir lier des données associées à ce contact dans de futures importations. Si vous utilisez un identifiant unique, vous pourrez le faire correspondre à l'identifiant externe de CiviCRM durant l'importation.

Lancer une importation
----------------------

La processus d'importation se déroule en quatre étapes.

### Étape 1 : Import des données

Dans cette rubrique, vous devez spécifier les informations de base de votre importation, et notamment la source de vos données. Ces dernières peuvent provenir soit d'un fichier CSV, soit d'une requête sur une base de donnée SQL de votre serveur. Une case à cocher vous permet d'indiquer si la première ligne de votre fichier doit être considérée ou non comme des en-têtes de colonne.

![image](/img/Screen%20Shot%202015-04-29%20at%203.54.21%20PM.png)

Notez que par défaut, le processus d'importation utilise la règle **non-supervisé** pour décider si un contact est ou non un doublon (vous pouvez vous référer au chapitre *Dedoublonnage et fusion* de cette section pour plus d'information sur les règles de détection de doublons dans CiviCRM). Vous pouvez spécifier ce que le système doit faire si un doublon est détecté lors d'une importation :

-   **Passer**: passe le contact en doublon, l'enregistrement original est laissé tel quel ;
-   **Mettre à jour**: met à jour l'enregistrement original avec les données importées. Les champs originaux qui n'apparaissent pas dans les données importées ne sont pas modifiés.
-   **Remplir**: remplit avec les champs vides ou manquants de l'enregistrement original avec les données importées. Ceux contenant déjà une ou plusieurs valeurs ne sont pas modifiés.
-   **Pas de vérification des doublons**: Tous les enregistrements valides importés sont systématiquement insérés dans la base de données CiviCRM sans qu'aucune vérification de doublons ne soit faite..

![image](/img/Import%20Options.png)

**Charger la carte de correspondance** indique comment les champs de données de votre fichier d'importation doivent correspondre aux champs de CiviCRM. La première fois que vous importez des données depuis une source particulière, il peut être utile de cocher la case "Sauvegarder cette carte de correspondance" en bas de la page avant de continuer. Cette dernière peut alors être facilement réutilisée la prochaine fois qu'une importation similaire est faite.

### Étape 2: Correspondance des champs
Si vous avez des en-têtes de colonne dans votre fichier, ces derniers apparaitront dans la première colonne du côté gauche de votre tableau de correspondance. Les deux colonnes suivantes affichent deux lignes d'enregistrements de valeurs qui seront importées, et la quatrième colonne indique les champs CiviCRM correspondants. Si vous avez chargé une carte de correspondance dans l'étape précédente, vous y retrouverez vos choix. Vous pouvez les modifier s'ils ne sont pas pertinents pour cet import.

![ImportMatchFields](/img/CiviCRM_update-CiviCore-ImportMatchFields-en.png "ImportMatchFields")

les champs CiviCRM correspondants incluent des données CiviCRM standards telles que Prénom et Nom, mais aussi des champs de données personnalisées que vous auriez au préalable configurés pour l'utilisation de vos contacts sur votre site. Faites correspondre les champs en cliquant sur les listes déroulantes et en sélectionnant la donnée appropriée. Par exemple, si l'en-tête de votre donnée importée est Nom de famille, vous pourriez choisir Nom comme champ CiviCRM correspondant.

Sélectionner "- ne pas importer -" pour toute colonne du fichier de données que vous ne souhaitez pas prendre en compte lors du processus d'importation dans CiviCRM.

Si vous avez sauvegardé une carte de correspondance pour un jeu particulier de colonnes de feuille de calcul et que ce dernier a changé (par exemple, vous avez ajouté des colonnes correspondant à des champs de données supplémentaires), vous pouvez modifier la carte et la sauvegarder à nouveau. Dans ce cas précis, pour faciliter l'importation de données supplémentaire, nous vous conseillons de mettre les nouvelles colonnes à droite des colonnes d'origine. Cela vous permet de retrouver les correspondances sauvegardées et d'en sélectionner ensuite les nouvelles.

![Step2d](/img/CiviCRM-AddingImporting-Step2d-en.png "Step2d")

Dans le cas contraire, si vous n'avez pas positionné vos nouvelles données dans des colonnes APRÈS les colonnes d'origine, vous ne pourrez pas utiliser les cartes de correspondance sauvegardées et vous devrez les refaire manuellement.

Une fois que vous avez fait correspondre les champs, vous pouvez éventuellement mettre à jour la sauvegarde de la carte de correspondance en cochant la case "Mettre à jour la carte de correspondance" pour y inclure les nouveaux changements.

### Étape 3: Prévisualisation

Cet écran vous affiche une prévisualisation des résultats de vos données importées, le nombre de lignes importées, et vous permets de faire une double vérification de vos correspondances de champs.

Si des lignes de votre feuille de calcul contiennent des données qui ne remplissent pas les prérequis de CiviCRM pour un ou plusieurs champs, vous verrez alors un message d'erreur avec le nombre de ligne non-valides (cf la capture d'écran ci-dessous). Vous pouvez cliquer sur le lien Télécharger les erreurs et voir le détail des problèmes dans le fichier ainsi téléchargé. Vous avez donc la possibilité de réparer les problèmes avant l'importation définitive.

![ImportPreviewErrs](/img/CiviCRM_update-CiviCore-ImportPreviewErrs-en.png "ImportPreviewErrs")

En bas du formulaire, vous pouvez choisir d'ajouter les contacts à un groupe existant, importer un nouveau groupe, créer une nouvelle étiquette, ou associer une étiquette existante. Nous vous recommandons fortement d'importer les enregistrements dans un groupe particulier afin de pouvoir facilement les retrouver et, si le besoin se présente, les effacer et les ré-importer.

![Step3b_1](/img/CiviCRM-AddingImporting-Step3b_1-en.png "Step3b_1")

### Step 4: Résumé

L'écran final affiche les importations réalisées avec succès, ainsi que les erreurs et les contacts en doublon. Si vous avez paramétré l'importation pour ajouter tous les nouveaux contacts à un groupe spécifique, vous pouvez cliquer dessus pour visualiser vos nouveaux enregistrements.

![Step4a_2](/img/CiviCRM-AddingImporting-Step4a_2-en.png "Step4a_2")

À ce stade, vous devriez vérifier que votre importation a fonctionné comme vous l'attendiez. Recherchez les contacts que vous venez d'importer et examinez leurs données standards et personnalisées.

Importer les données associées
------------------------------

Nous venons de décrire le processus d'importation d'un fichier de données. Mais comment faire pour importer des données liées aux contacts, telles que les adresses professionnelles, les activités, les contributions, etc. ? Vous aurez besoin d'importer un fichier CSV propre à chaque type de données.

CiviCRM possède des outils spécifiques pour importer des données liées à des contacts, et un jeu d'outil particulier pour l'importation des contributions, des adhésions, des participations à des événements, etc. (les informations détaillées sur l'utilisation de ces outils sont disponibles dans leur chapitre respectif). Pour importer des relations, vous pouvez lancer des importations de contact multiple.

Par exemple, si nous voulons importer des données sur des enfants et de leur deux parents, nous devons lancer trois imports : un pour l'enfant, un pour le père et un pour la mère.

Tout d'abord, nous importons les données enfant en pensant à bien inclure un identifiant externe. Puis nous importons les données père, et ensuite les données mère, en tant que contacts associés à l'enfant en utilisant l'identifiant externe de ce dernier.

Dans l'exemple ci-dessous, nous avons un fichier CSV qui contient les informations de la mère et du père. Nous utilisons ce même fichier deux fois pour l'importation. Regardez bien les champs ci-dessous pour comprendre ce qui se passe.

![Parent1a](/img/CiviCRM-AddingImporting-Parent1a-en.png "Parent1a")

![Parent1b](/img/CiviCRM-AddingImporting-Parent1b-en.png "Parent1b")

Nous lions le père à l'enfant en utilisant l'identifiant externe et ainsi importons le nom du père en utilisant le type de relation "Enfant de ".

Quand l'importation est réalisée, vérifiez les données en recherchant les parents et en examinant l'onglet Relations. Il devrait y avoir un lien de relation les connectant à l'enfant.

Vous pouvez répéter ce processus pour la mère, et tout autre type de relation si besoin.

Normalisation des adresses
--------------------------

Pour beaucoup d'organisations, un élément important concernant le nettoyage et la fiabilité des données est la normalisation des adresses. En France, cela signifie se conformer aux standards définis par l'Afnor dans sa norme NF Z10-011 (norme 38). Aux États-Unis, les normes sont définies par les Services Postaux des États-Unis (USPS).
Renseigner des adresses normalisées dans CiviCRM vous permet d'obtenir des résultats plus précis lorsque vous effectuez une recherche via une adresse. CiviCRM peut en effet faire la recherche en respectant les standards USPS si vous choisissez d'activer cette option. Pour plus de renseignement, merci de vous référer au chapitre *Installation et paramétrage* de la section *Configuration*.

Importer les activités
----------------------

Lorsque vous préparez vos données à importer, il est utile de savoir quels sont les champs indispensables à remplir, afin de les inclure dans votre fichier CSV. Vous en trouverez ci-dessous une liste. Le champ Identifiant de contact est utilisé pour lier l'activité au contact concerné. Il est donc important qu'il corresponde précisement. 

-   Date de l'activité
-   Identifiants du type d'activité
-   Libellé du type d'activité
-   Identifiant de contact (Correspond au contact)
-   Sujet

L'outil d'importation des activités est semblable à celui des contacts, mais un prérequis doit être respectés avant de lancer le processus. Les activités ne peuvent être importées que si les contacts associés et les types d'activités existent déjà dans CiviCRM. Pensez donc à réaliser l'importation des contacts en premier, en n'oubliant pas de leur associer un identifiant externe unique (cf plus haut).

N'oubliez pas que les fichiers CSV doivent avoir une taille inférieure à 2Mo. Si besoin, découpez votre fichier en plusieurs morceaux.

Importer les contributions
--------------------------

Vous pouvez ajouter ou mettre à jour des contributions.

Si vous voulez **ajouter des nouvelles contributions**, votre fichier CSV doit contenir au moins les champs suivants :

-   Identifiant de contact, ou Identifiant externe, ou tout champ utilisé dans votre règle de doublons non superviséé (pour faire correspondre à un contact existant)
-   Compte
-   Montant total

Si vous souhaitez **mettre à jour des contributions existantes**, votre fichier CSV doit contenir au moins les champs suivants :

-   Identifiant de transaction, ou de facture, ou de paiement (pour faire correspondre à une contribution existante)
-   Compte
-   Montant total

Vous pouvez aussi utiliser **mettre à jour des contributions  existantes** pour importer des nouvelles données ou en modifier des existantes dans des champs contribution standards ou personnalisés. En faisant cela, vous aurez besoin d'inclure un identifiant pour faire correspondre une contribution existante, ainsi que le compte et montant total dans votre fichier CSV, même si ces valeurs ne sont pas différentes des valeurs déjà présentes dans votre base de donnée.

Importer les adhésions
----------------------

Vous pouvez ajouter ou mettre à jour des adhésions.

Si vous voulez **ajouter des nouvelles adhésions**, votre fichier CSV doit contenir au moins les champs suivants :

-   Identifiant de contact, ou Identifiant externe, ou tout champ utilisé dans votre règle de doublons non superviséé (pour faire correspondre à un contact existant)
-   Type d'adhésion
-   Date de début d'adhésion

Si vous souhaitez **mettre à jour des adhésions existantes**, votre fichier CSV doit contenir au moins les champs suivants :

-   Identifiant d'adhésion (pour faire correspondre à l'adhésion existante)
-   Type d'adhésion
-   Date de début d'adhésion

Vous pouvez aussi utiliser **mettre à jour des adhésions existantes** pour importer des nouvelles données ou en modifier des existantes dans des champs adhésion standards ou personnalisés. En faisant cela, vous aurez besoin d'inclure un identifiant d'adhésion pour faire correspondre une adhésion existante, ainsi que le type d'adhésion et la date de début d'adhésion dans votre fichier CSV, même si ces valeurs ne sont pas différentes des valeurs déjà présentes dans votre base de donnée.

Importer des participants
-------------------------

Pour chaque session d'importation, vous pouvez soit ajouter des nouvelles inscriptions, soit mettre à jour des participations existantes.

Si vous voulez **ajouter des nouvelles inscriptions**, vous devrez soit limiter à une seule inscription par événement et par personne (sélectionnez **sur entrées en doublon** sur **passer**), soit autoriser les doublons d'inscriptions (sélectionnez **sur entrées en doublon** sur **pas de vérification de doublon**). Dans les deux cas, votre fichier CSV doit contenir au moins les champs suivants :

-   Identifiant de contact, ou Identifiant externe, ou tout champ utilisé dans votre règle de doublons non superviséé (pour faire correspondre à un contact existant)
-   Identifiant de l'événement
-   Statut du participant

Si vous souhaitez **mettre à jour des inscriptions existantes**, vous devez sélectionner **sur entrées en doublon** sur **Mettre à jour**. votre fichier CSV doit contenir au moins les champs suivants :

-   Identifiant de participant (pour faire correspondre à l'inscription existante)
-   Identifiant ou Titre d'événement
-   Statut du participant

Vous pouvez aussi utiliser **mettre à jour des inscriptions existantes** pour importer des nouvelles données ou en modifier des existantes dans des champs participant standards ou personnalisés. En faisant cela, vous aurez besoin d'inclure un identifiant de participant pour faire correspondre une inscription existante, ainsi que l'Identifiant (ou Titre) de l'événément et le statut du participant dans votre fichier CSV, même si ces valeurs ne sont pas différentes des valeurs déjà présentes dans votre base de donnée.

Importer des étiquettes
-----------------------

CiviCRM n'inclue pas encore dans son système un moyen d'importer ou de mettre à jour des étiquettes. Vous pouvez cependant utiliser [cette extension](https://civicrm.org/extensions/api-csv-import-gui "API csv Import GUI").

Si vous souhaitez assigner des étiquettes durant l'importation de vos contacts, vous pouvez vous referer au début de ce chapitre.
