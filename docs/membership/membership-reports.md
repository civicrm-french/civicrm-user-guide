Rapports sur les adhésions 
==================

Il existe plusieurs techniques pour obtenir un rapport et analyser vos adhésions.

Le tableau de bord des membres donne un résumé rapide de vos adhésions actuelles, affichant des informations pour chaque type d'adhésion, telles que le total actuel des membres, une ventilation pour le dernier mois, le mois en cours et les totaux de l'année en cours. Vous pouvez également rechercher des détails d'adhésions en utilisant **Recherche avancée** ou **Trouver des membres**. Pour en savoir plus sur le tableau de bord des adhésions et comment utiliser les fonctions de recherche pour trouver une adhésion, consultez le chapitre «Trouver des membres».

Ce chapitre vous montrera comment afficher et créer des rapports d'adhésion ainsi que d'exporter ces informations afin que vous puissiez effectuer d'autres analyses.

Affichage des rapports d'adhésion
--------------------------
CiviCRM est livré avec plusieurs rapports d'adhésions conçus pour vous permettre une analyse de vos adhésions:

![image](/img/membership%20report%20list_1.PNG) 

Le rapport  **Membership Summary** affiche des informations sur les membres regroupés selon une fréquence de date que vous spécifiez, comme le mois, la semaine, le trimestre, l'année. Par exemple, vous pouvez consulter le nombre de membres qui vous ont rejoint chaque mois pendant une période, des types d'adhésion ou toute autre donnée personnalisée que vous collectez à leur sujet.

![image](/img/membership%20summary%20report.PNG)

Si vous cliquez sur un champ en surbrillance, vous verrez le rapport **Membership Detail** correspondant pour cette ligne. par exemple si vous cliquez sur **Mai 2015** pour le type d'adhésion **Général** ceci vous donnera:

![image](/img/membership%20detail%20from%20summary%20report.PNG)

Le rapport **Membership Detail** affiche des informations pour chaque adhérent en fonction des critères sélectionnés.

![image](/img/membership%20detail%20report.PNG) 
 
Le rapport **Lapsed Memberships** fournit une liste des adhésions qui ont expiré ou seront caduques avant la date que vous avez spécifiée.

![image](/img/membership%20lapsed%20report.PNG) 

Le rapport **Contribution et Membership Details** affiche les informations détaillées des contributions ainsi que les contributions liées à une adhésion en fonction des critères sélectionnés.

![image](/img/membership%20contribution%20report.PNG) 

Création de nouveaux rapports d'adhésions
-------------------------------

Vous pouvez créer de nouveaux rapports sur les adhésions si vous estimez que les modèles standards ne vous conviennent pas. Voici comment proceder :

-   Cliquez sur **Tous les rapports>Nouveau compte rendu** cliquez sur le bouton **Member report templates**
-   Dans cette fenêtre, cliquez sur l'un des modèles de rapport d'adhésion et commencez à entrer vos critères dans les onglets "Colonnes, Groupement, Trier, Filtres"

![image](/img/memberships%20create%20new%20membership%20report_1.JPG)

-   Dès que vous avez saisi vos critères, cliquez sur **Voir les résultats** pour vérifier vos résultats.
-   Si vous êtes satisfait du résultat, vous pouvez alors enregistrer ce rapport en tant que nouveau rapport d'adhésion en cliquant sur **Créer un rapport**, dans le menu déroulant "Action > Créer un compte rendu" puis donner un nom en tant que nouveau rapport d'adhésion.

Pour en savoir plus sur le fonctionnement des rapports, consultez la section "Comptes rendus".

Export des informations d'adhésion
----------------------------

Vous pouvez choisir d'exporter des enregistrements d'adhésion afin que vous puissiez effectuer plus d'analyses, effectuer des fusion de courrier de documents ou créer un type spécifique de rapports externe à CiviCRM. L'exportation d'enregistrements d'adhésion vous permet de sélectionner un ensemble de champs primaires par défaut ou de choisir des champs spécifiques à l'enregistrement d'adhésion en vue de l'exportation.

Vous devrez d'abord rechercher les enregistrements d'adhésion spécifiques que vous souhaitez exporter. Pour en savoir plus sur la recherche de dossiers d'adhésion, consultez le chapitre «Trouver des membres».

Pour exporter les enregistrements d'adhésion:

-   Cliquez sur **Adhésion> rechercher des adhésions**, entrez vos critères de recherche. 
-   Sur l'écran de résultats de recherche "Trouver des adhésions", sélectionnez les enregistrements que vous souhaitez exporter et dans le menu déroulant **- actions -**, sélectionnez **Exporter les membres**.
-   Vous pouvez sélectionner **Exporter les champs PRINCIPAUX** ou **Sélectionner les champs à exporter** et cliquez sur le bouton **Suivant**
  
![image](/img/memberships%20export%20memberships%20screen.JPG)

- Si vous avez sélectionné **Exporter les champs PRINCIPAUX**, un fichier appelé CiviCRM_Member_Search.csv sera créé contenant les enregistrements d'adhésion en fonction de vos critères de recherche
- Si vous avez sélectionné **Sélectionnez les champs à exporter**, incluez les champs que vous souhaitez exporter, cochez la case **Sauvegarder cette correspondance de champs** si vous souhaitez réutiliser ce mappage de champ pour une exportation future, Puis cliquez sur le bouton **Exporter**. Un fichier appelé CiviCRM_Member_Search.csv sera créé contenant les enregistrements d'adhésion en fonction de vos critères de recherche et des champs que vous avez sélectionnés.

![image](/img/memberships%20select%20fields%20to%20export.JPG)
