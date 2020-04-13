
Exporter vos contacts
=======================

L'exportation vous permet de partager vos données avec des applications externes en copiant les valeurs de vos champs CiviCRM dans un fichier CSV (comma separated value). Ce format répandu peut être visualisé et modifié dans des applications de feuille de calcul, importé dans d'autres bases de données, ou encore fusionné avec un autre document à l'aidre d'un traitement de texte.

Vous pouvez soit exporter un jeu de donné prédéfini, soit créer votre propre jeu que vous pourrez sauvegarder et réutiliser.

La fonctionnalité d'exportation de CiviCRM est disponible :

-   dans n'importe quel outil de recherche ;
-   lors de la visualisation des contacts dans un groupe ;
-   dans les résultats de recherche basée sur les composants, quand les résultats correspondent à des données propres au composant et non-pas aux données standards de contact. Par exemple, depuis la recherche **Contributions > Trouver les contributions**, vous pourriez exporter vos donateurs, leur adresse de contact et le montant de leur donation pour créer une lettre de remerciement.

Voici comment importer vos informations de contact :

1.  Effectuez une recherche de contacts (vous trouverez des informations dans [Rechercher](../the-user-interface/searching).

2.  Sélectionnez les contacts que vous souhaitez importer (soit la totalité, soit une partie en cliquant sur les cases à cocher à gauche de chaque enregistrement).

3.  Depuis le menu déroulant **- actions -**, sélectionnez **Exportez les contacts** tel qu'indiqué dans la figure ci-dessous. Cela ouvrira l'assistant d'exportation.

    ![ExportFromSearch](/img/CiviCRM_update-CiviCore-ExportFromSearch-en.png "ExportFromSearch")

4.  **Tout exporter ou uniquement les champs sélectionnés**.  

    -  Choisissez entre exporter les champs principaux ou selectionnez votre propre jeu de champs.

    ![ContactExportOptions](/img/contact-export-options.PNG "ContactExportOptions")

    Il existe 80 champs dans une exportation de champs principaux (les champs standards de contact tels que le courriel, le téléphone et l'adresse principaux). Il est souvent préférable de décider quel champs exporter, et cela vous permet également de prendre en compte les champs tels que courriel, téléphone et adresse secondaires de vos contacts, ainsi que leurs champs personnalisés. Vous pouvez également choisir d'utiiser une carte de correspondance d'exportation que vous auriez précédemment sauvegardé.

    -  Si vous faites une exportation en vue d'un publipostage, vous pouvez décider de n'exporter qu'un seul enregistrement par ménage/foyer ou un seul par adresse. Si vous choisissez cette dernière solution, vous pouvez dans ce cas préciser le format de l'adresse postale ainsi que la salutation.
    
    -  Vous pouvez exclure les contacts ayant coché "Ne pas envoyer de courrier", ceux sans adresse postale et ceux décédés.

    -  Vous pouvez ajouter des contacts à exporter d'un ou plusieurs autres groupes.

5.  Lorsque vous cliquez sur **Continuer**, si vous avez sélectionné *Exporter les champs principaux*, l'exportation est lancée et vous pouvez passer directement à l'étape 7.

6.  **Selectionner les champs à exporter**

    ![ContactExportFieldSelection](/img/contact-export-field-selection.PNG "ContactExportFieldSelection")  

    -  Si vous avez choisi d'utiliser une carte de correspondance sauvegardée, les champs de cette correspondance seront affichés. Vous pouvez alors l'utiliser telle quelle ou la modifier. Dans le dernier cas, il est bien sûr possible de mettre à jour la sauvegarde ou d'en créer une nouvelle.
    
    -  Une fois la correspondance à votre convenance, vous pouvez éventuellement la sauvegarde en cliquant sur **Sauvegarder cette correspondance de champ** pour l'utiliser plus tard.

    -  Quand tout est correct, cliquez sur **Exporter**.

7.  Vous obtenez un fichier au format CSV. Par défaut, une virgule (,) est utilisée pour séparer les valeurs. Vous pouvez modifier ce paramètre en allant dans **Administrer > Localisation > Langues, devises et localisations** et en sélectionnant le bon **Séparateur de champ d'importation/exportation**.
