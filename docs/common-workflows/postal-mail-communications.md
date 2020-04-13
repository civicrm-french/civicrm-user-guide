Communications par courrier postal
==================================

Ce chapitre aborde les différents moyens qu'utilise CiviCRM pour vous aider dans votre gestion des courriers postaux et de leurs campagnes. Il est recommandé d'avoir au préalable une bonne compréhension de certaines fonctionnalités du système, telles que les champs personnalisés, les activités, les profils et comment faire des fusions de documents à l'aide d'un logiciel de traitement de texte.

Plannifier vos courriers
------------------------

Avant de commencer toute activité de communication, prenez le temps d'identifier vos objectifs et de planifier vos étapes. Pour vous aider, voici quelques questions clés auxquelles il vous faut répondre avant d'envoyer vos courriers postaux :

-   Quels type de courrier envoyez-vous à vos contacts ?
-   Vos courriers sont-ils toujours envoyés à l'ensemble de vos contacts, ou ciblez-vous régulièrement un groupe spécifique ?
-   Comment saluez-vous vos destinataires (ex: "Chère Jane" ou "Chère Jane Doe") ?

Il existe trois façon d'utiliser CiviCRM pour vos courriers postaux :

1.  Générer des étiquettes : il s'agit d'imprimer les étiquettes d'adresse lorsque vous n'avez pas besoin de personnaliser le contenu du courrier (ex : envoi d'une brochure) ;
2.  Exporter des contacts et les fusionner via un traitement de texte (tel qu'OpenOffice ou Microsoft Word). Pour cela, veuiller vous référer au chapitre [Exporter vos contacts](exporting-your-contacts.md) ; 
3.  Utiliser la fonctionnalité d'impression des lettres PDF de CiviCRM pour réaliser la fusion directement dans le système.

Beaucoup d'organisation à but non-lucratif aux États-Unis ont besoin de trier les destinataires par code postal pour des besoins de publipostage. Si cela est également votre cas, nous vous recommandons d'effectuer ce tri en utilisant un logiciel de traitement de texte, dans lequel vous pouvez facilement contrôler l'ordre des contenus, plutôt que dans CiviCRM.

Paramétrer les salutations
--------------------------

Vous pouvez paramétrer un format de salutation spécifique à chaque contact. Il existe plusieurs options allant de la plus amicale ("Cher John") à la plus formelle ("Cher Monsieur John Doe"). Vous pouvez également créer une salutation personnalisée ("Votre Royale Majesté"). Les salutations de courrier postal peuvent être éditées dans la section **Préférences de communication** du formulaire d'édition du contact. Si vous avez besoin de paramétrer ou de réinitialiser les salutations de courrier postal en masse, veuillez vous référer au chapitre [Automatiser les tâches](automating-tasks.md).

Imprimer les lettres PDF
------------------------

Le processus consiste à sélectionner en premier les contacts cibles de vos courriers, puis de générer via un traitement par lot les lettres en PDF. Ce format vous permettra de les imprimer facielement par la suite.

Pour créer la lettre :

1.  Aller à **Rechercher > Rechercher des contacts** ou **Rechercher > Recherche avancée** ;
2.  Exécuter votre recherche selon vos critères (groupe, type de contact...) ;
3.  Selectionner les contacts qui recevront la lettre
4.  Depuis le menu déroulant **Actions**, choisissez **Print / merge document** ;
5.  Sélectionner éventuellement un modèle de document et / ou paramétrez les options de mise en page dans la rubrique **Format de la page** ; 
6.  Entrez / modifiez votre texte, mettez-le en forme, insérez une image... ;
7.  Vous pouvez personnaliser votre lettre en ajoutant des champs de fusion : positionnez le curseur à l'endroit où vous souhaitez insérer le champ, puis sélectionnez-le depuis le menu déroulant *Champs de fusion* en haut à droite.

    ![PostalGreetingToken](/img/CiviCRM_update-CiviCore-PostalGreetingToken-en.png "PostalGreetingToken")

8.  Avant d'aller plus loin, vous pouvez décider de sauvegarder le document en tant que nouveau modèle. Dans ce cas, activez la case à cocher en bas de l'éditeur et donnez un titre à votre modèle ;
9.  Choisissez le format de document que vous souhaitez générer (pdf, docx, html...) ;
10. Vous pouvez cliquer sur le bouton Prévisualiser pour vérifier votre document, puis ensuite cliquer sur le bouton "Download document" pour le sauvegarder sur votre ordinateur et en faire une impression future.


Générer des étiquettes d'adresse
--------------------------------

Il s'agit d'une fonction à la fois simple et utile.

1.  Répétez les étapes 1 à 3 de l'impression des lettres PDF pour sélectionner vos contacts cibles ;
2.  Choisissez **Étiquettes pour la poste - Imprimer** depuis le menu déroulant **Actions** ;
3.  Sélectionnez un format d'étiquette ;
4.  Sélectionnez le type d'adresse (principal, facturation...) ;
5.  Choisissez parmi les options disponibles si :

    a.  Si vous voulez exclure les contacts ayant activé "ne pas envoyer de courrier" dans leur préférence de communication (option active par défaut et recommandée) ;
    
    b.  Si vous voulez fusionner les étiquettes des contacts avec la même adresse ;
    
    c.  Si vous voulez fusionner les étiquettes des contacts partageant le même ménage / foyer.

Ces deux dernières options vous permettent d'éviter des doublons inutiles (et par la même occasion d'économiser des frais d'affranchissement). Lorsque des fusions d'adresse sont réalisées, les noms des contacts correspondants sont listés sur une ligne séparée de l'étiquette.

Pour savoir comment personnaliser vos étiquettes d'adresse, veuillez vous référer au paragraphe **Paramètre d'adresse** de la rubrique [Configuration](../initial-set-up/installation-and-basic-set-up.md#configuration) du chapitre [Installation et paramétrage](../initial-set-up/installation-and-basic-set-up.md)
