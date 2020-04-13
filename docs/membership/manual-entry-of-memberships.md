Entrée manuelle des adhésions
===========================

CiviCRM fournit un ensemble d'outils permettant aux contacts une interaction directe sur le site Web pour devenir membres sans intervention nécessaire de la part du personnel administratif (ce qui est une fonction très puissante permettant un gain de temps au personnel administratif). Il existe de nombreuses situations dans lesquelles les adhésions doivent être traitées manuellement. Ce chapitre décrit les différentes façons dont le personnel administratif (ou les utilisateurs autorisés) peuvent créer et traiter manuellement des adhésions, y compris:

- Créer de nouveaux enregistrements d'adhésion un par un (y compris les adhésions gratuites où le paiement provient d'un contact différent)
- Entrér des données des membres par lots 
- Importer des adhésions   

Contrôle d'accès à CiviMember
-------------------------

Comme pour les autres fonctions de CiviCRM, **Administer> User & Permissions> Permissions** vous permet de contrôler l'accès à diverses fonctionnalités de CiviMember.

Pour les utilisateurs qui doivent créer,chercher et afficher les adhésions :
- Attribuez l'autorisation à **CiviMember: access CiviMember** et **CiviContribute: access CiviContribute**, etc... Si des paiements sont concernés et assurez-vous que l'utilisateur est autorisé à afficher les contacts pour l'enregistrement associé.

Pour plus de précision sur les permissions voir : 
[http://wiki.civicrm.org/confluence/display/CRMDOC/Default+Permissions+and+Roles](http://wiki.civicrm.org/confluence/display/CRMDOC/Default+Permissions+and+Roles)

Création d'un nouveau dossier d'adhésion
--------------------------------

Vous pouvez créer un nouvel enregistrement d'adhésion de deux façons : directement dans le contact ou dans le menu **Adhésions**. L'utilisation du menu **Adhésions** est pratique car vous pouvez créer un nouveau contact en même temps que l'ajout du nouvel enregistrement d'adhésion :**Nouvelle adhésion**

Un des avantages de créer une nouvelle adhésion directement à partir d'un contact existant est que si vous avez configuré un processeur de paiement qui autorise les transactions par carte de crédit sur votre site, vous pouvez sélectionner l'option **Soumettre une carte de crédit** et traiter le paiement de l'adhésion immédiatement.

Lorsque vous utilisez le menu **Adhésions** pour créer une nouvelle adhésion, vous n'avez pas la possibilité de soumettre des informations sur la carte de crédit, mais vous pouvez enregistrer d'autres types de paiements comme les chèques et les espèces.

### Via un enregistrement de contact existant

- À partir du dossier d'un contact, cliquez sur l'onglet **Adhésions** puis cliquez sur "Ajouter Adhésion". Si vous avez configuré un processeur de paiement qui autorise les transactions par carte de crédit directement sur votre site, vous pouvez sélectionner l'option **Soumettre une carte de crédit** et traiter immédiatement le paiement.

![image](/img/manual-add-membership.png) 

Sur le formulaire **Nouvelle adhésion**  plusieurs champs seront complétés automatiquement s'ils sont laissés en blanc. 
Ces champs sont:

-   **Organisation et type d'adhésion:** Sélectionnez le nom de l'organisation avec laquelle le contact adhére et le type d'adhésion ***OU***

-   **Choisir une tarification**: Sélectionnez "Choisir une tarification" plutôt que l'organisation et le type d'adhésion si vous disposez de diverses structures tarifaires pour différentes catégories d'adhésion. (Voir le chapitre *Gestion des tarifications* pour plus de détails)

-   **Nombre de périodes :** Entrez le nombre de périodes d'adhésion associées à ce statut d'adhésion. La date de fin d'adhésion sera alors définie à une date de fin en fonction du nombre de périodes (cette option est cachée lors de l'utilisation de la "Gestion des tarifications")

-   **Source**: Si elle est laissée vide, le système complète les détails concernant l'enregistrement : transaction hors ligne ou en ligne et le nom de la personne qui a rempli l'enregistrement.

-   **Campagne**: Si l'adhésion est associée à une campagne d'action spécifique, sélectionnez le nom de la campagne. Pour en savoir plus, consultez la section *Campagne*.

-   **Membre depuis le**: La date à laquelle l'adhésion a été créée sera rempli automatiquement, mais peut être remplacé si nécessaire. Par défaut: date de saisie.

-   **Date de début**: Si le type d'adhésion est une adhésion "glissante", la date actuelle sera remplie automatiquement. Si le type d'adhésion est une période fixe, CiviCRM déterminera la date de début appropriée en fonction de la configuration du type d'adhésion. Cela peut être remplacé si nécessaire.

-   **Date de fin**: Ce champ est automatiquement calculé à partir de la date de début et rempli en fonction des paramètres du type d'adhésion. Cela peut être annulé si nécessaire.

-   **Auto-renouvellement**: Ce champ n'est affiché que si vous avez choisi un type d'adhésion qui a une fonction de renouvellement automatique définie dans le type d'adhésion et utilise l'option "Soumettre une carte de crédit" pour créer l'adhésion.

-   **Forcer le statut?**: Cochez cette case pour définir manuellement un statut pour l'enregistrement de membre. Comme indiqué par le titre, il remplace l'état automatiquement fourni. Vous devriez faire preuve de prudence avec ce champ car le réglage empêchera l'état de se mettre à jour automatiquement en fonction des statuts de l'adhésion que vous avez configurés (voir le chapitre *Définir les adhésions*)

-   **Enregistrer le paiement de la cotisation ?**: En cochant cette case et en remplissant les champs de transaction affichés, vous enregistrerez le versement de l'adhésion. Un enregistrement de contribution est créé automatiquement en plus du dossier d'adhésion. Après avoir enregistré l'adhésion, vous pourrez voir le dossier d'adhésion et voir l'enregistrement de contribution correspondant.

    -   **Enregistrer le paiement d'un contact différent ?**: le plus souvent utilisé pour les attributions de gratuité
    -   **Montant**: Entrez le montant du paiement de l'adhésion.
    -   **Reçu**: Entrez la date et l'heure (heure : facultatif) de réception du paiement.
     -  **Type d'opération**: Sélectionnez le type financier approprié pour ce paiement.
    -   **Méthode de paiement**: Sélectionnez le moyen de paiement par lequel ce paiement a été reçu, par exemple en espèces ou en chèque. Vous pouvez en savoir plus sur la configuration des instruments de paiement dans la section *Contributions*.
     -   **Numéro de chèque**: Si le paiement a été reçu par chèque, entrez le numéro de chèque, si désiré.
     -   **ID de Transaction**: Si vous disposez d'un processeur de paiement, CiviCRM stockera un identifiant de transaction généré automatiquement. Pour les transactions manuelles, vous pouvez entrer un identifiant de transfert bancaire ou un autre identifiant, le cas échéant.
     -   **Etat du paiement**: Sélectionnez le statut du paiement de l'adhésion reçue. Vous pouvez en savoir plus sur la configuration des instruments de paiement dans la section *Contributions*.

     -   **Envoi Confirmation et reçu ?:** Cochez cette case pour envoyer un courriel au contact confirmant son adhésion
     -   **Réception de :** sélectionnez l'adresse email dont le reçu de confirmation provient de. Si l'adresse e-mail que vous souhaitez utiliser n'est pas répertoriée, vous pouvez l'ajouter en allant dans **Mailings> From Emails**.
    -   **Réception a :** Sélectionnez l'adresse d'envoi du courriel de confirmation . Si l'adresse e-mail que vous souhaitez utiliser n'est pas répertoriée, vous pouvez l'ajouter en allant dans **Mailings> From Emails**.
    -   **Message de réception:** vous pouvez entrer le texte ici pour envoyer un message spécial au membre. Si vous ne saisissez pas de texte, le message de confirmation et de réception par défaut sera utilisé.
  
### **Auto-renouvellement des adhésions via le Back end**

Pour créer manuellement une adhésion qui se renouvellera automatiquement, reportez-vous à l'écran récapitulatif du contact, sélectionnez l'onglet **Adhésions** et cliquez sur **Soumettre l'adhésion par carte de crédit**. Si vous sélectionnez un type d'adhésion qui est configuré pour être récurrent, une case à cocher intitulée **Adhésion renouvelée automatiquement** sera affichée.

Si vous cochez "Renouvellement automatique", une demande de paiement récurrente (souscription) sera soumise au processeur de paiement sélectionné. Si la demande est validée, cette adhésion sera automatiquement renouvelée le dernier jour de la période d'adhésion jusqu'à ce que le paiement soit annulé. Les courriels de réception de paiement d'adhésion comprendront un lien pour que le membre annule, éventuellement, le renouvellement automatique.

### Via le menu **Adhésion** 

-   Naviguez vers **Adhésions** ** puis sélectionnez le contact ou créez un nouveau contact: **Nouveau membre**, 

![image](/img/memberships%20add%20membership%20new%20contact.JPG)

- Remplissez le formulaire "Nouveau Membre" avec l'adhésion appropriée et les informations de paiement comme dans *Via un enregistrement de contact existant* ci-dessus.

![image](/img/memberships%20add%20membership%20via%20menu.JPG) 

Adhésions gratuites 
----------------

Lorsque vous entrez une adhésion manuellement, vous pouvez sélectionner **Enregistrer le paiement à partir d'un contact différent?** pour enregistrer une adhésion offerte par quelqu'un d'autre. La personne qui paie l'adhésion peut être un contact existant ou un nouveau contact créé pendant le processus. Le paiement sera enregistré sur le dossier du payeur, mais l'adhésion sera crédité au destinataire. Le reçu sera envoyé au payeur. Vous devrez envoyer un courriel ou une lettre distincte pour informer le destinataire de la réception de son adhésion offerte par le payeur.

![image](/img/gift%20membership.PNG)

Saisie de lot de paiement d'adhésion 
---------------------------------------

CiviCRM offre une fonctionnalité **Entrée de données par lots** (dans le menu **Adhésions**) qui peut être utilisé pour entrer des lots de paiements d'adhésion qui ont été reçus sur des formulaires papier ou électronique. Il peut être utilisé pour les contacts nouveaux et existants et comprend la vérification du montant total et du nombre d'enregistrement par rapport aux paiements que vous avez enregistrés sur votre bordereau de dépôt.

Cette fonction comporte un écran d'entrée de grille d'entrée par lots, et des outils que vous pouvez utiliser pour accélérer le traitement lorsque vous avez beaucoup d'adhésions à traiter en même temps. Il comprend une fonction de copie pour définir tous les champs à la même valeur et vous permet de créer de nouveaux contacts sans quitter l'écran de saisie du lot.

Les champs d'informations que vous souhaitez collecter dans la grille d'entrée de lot sont déterminés par plusieurs profils réservés à CiviCRM. Si vous souhaitez collecter d'autres types d'informations qui ne sont actuellement pas inclus dans ces profils, vous devrez modifier ces profils pour refléter les champs que vous souhaitez afficher.

Pour plus de détails sur cette fonctionnalité consultez le chapitre *Mise en place* de la section *Contributions*.

Importer des adhésions
-----------------------

Cette fonctionnalité est très utile si vous disposez d'un grand nombre d'enregistrements d'adhésion provenant d'une source extérieure (fichier csv). Elle peut également être utilisée pour mettre à jour les adhésions existantes avec de nouvelles informations.

Il est important de lire le chapitre *Importation de données* dans la section *Flux de travail commun*, avant de commencer à importer des adhésions, car cela donne des informations générales pertinentes. Voici quelques détails spécifiques à l'importation d'adhésion qu'il faut connaître :

- Les enregistrements de contact doivent exister avant d'importer des données d'adhésion. Si vous souhaitez importer des adhésions pour les contacts qui n'existent pas encore dans CiviCRM, vous devez d'abord importer les contacts. Vérifiez que les données de contact ont une ID externe afin que vous puissiez inclure cette ID avec vos données d'adhésion pour associer ces enregistrements aux contacts correspondants. Si vous importez des données d'adhésion pour des contacts qui existent déjà, vous aurez besoin de l'ID de contact interne ou des champs de votre Règle de correspondance sans duplication pour lier les données d'adhésions au contact correctement.

- L'importation de votre fichier de données d'adhésions DOIT contenir obligatoirement le type d'adhésion ET la date de début. Les types d'adhésions répertoriés doivent correspondre exactement aux types d'adhésion établis par votre administrateur CiviCRM. La date de début doit utiliser le format de date spécifié pour votre installation CiviCRM. Si votre fichier d'importation ne contient pas ces champs, vous ne pourrez l'importer.

- Vous devez importer des données d'adhésion par types de contacts différents séparément. L'importation de fichiers avec plus d'un type de contact ne fonctionnera pas. (Vous devez également importer séparément les nouvelles adhésions et renouvellements ).

Tout ceci étant bien vérifié, vous êtes prêt maintenant à importer vos données d'adhésion:

Accédez à **Adhésions> Importer des adhésions**.

1. Ecran Import:

    -   Sélectionnez votre fichier de données d'importation. Il doit s'agir d'un fichier CSV.
    -   Sélectionnez la case à cocher si vos données source contiennent des intitulés de colonnes.
    -   Spécifiez le type de contact que vous importez : Particulier, Foyer, Organisation. 
    -   Indiquez le format de date que vous utilisez.
    -   Cliquez sur **Suivant**.
    
2. Ecran Correspondance des champs

    -   Faites correcpondre vos données d'adhésion avec les champs CiviCRM appropriés sous la colonne "Faire correspondre aux champs CiviCRM". Notez que vous pouvez **Sauvegarder cette correspondance de champs** afin que vous puissiez la réutiliser pour des importations futures, puis cliquez sur **Suivant**.

3. Ecran Prévisualisation

    -   Vous voyez l'aperçu des résultats de votre importation. Il existe une table qui répertorie les lignes totales dans le fichier téléchargé, le nombre de lignes en erreurs et le nombre de lignes valides. Si vous continuez l'importation, les lignes avec des erreurs seront ignorées. Vous pouvez télécharger un fichier avec les enregistrements en erreurs et continuer l'importation. Vous pouvez ensuite éditer les erreurs et corriger les erreurs dans le fichier CSV d'origine ou utiliser le fichier des erreurs modifié et recommencer l'importation.

4. S'il n'y a pas d'erreurs ou si vous ne souhaitez pas corriger les erreurs trouvées, cliquez sur **Importer maintenant**. Vous verrez la progression de l'importation jusqu'à ce qu'elle soit terminée. Lorsque l'importation est terminée, vous verrez un résumé de l'activité d'importation et ses résultats.


