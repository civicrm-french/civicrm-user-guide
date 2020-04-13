Menu, Tableau de bord et indicateurs
============================

Ce chapitre donne un aperçu du tableau de bord de CiviCRM (sa page d'accueil) et du menu de navigation disponible pour les utilisateurs de CiviCRM.

Menu de navigation
-------------------
Le menu de navigation est une barre horizontale en haut de chaque page "back office" de CiviCRM.

![image](/img/4.5%20Menubar.png)... 

Ce menu donne accès à presque toutes les fonctions de CiviCRM et est organisé en grande partie par les Composants (tels que Contributions, Evénements et Mailings), ainsi que Recherche, Administrer et Rapports, et affiche les composants activés. 

![NavMenu_SearchPulldown](/img/CiviCRM_update-CiviCore-NavMenu_SearchPulldown-en.jpg "NavMenu_SearchPulldown")

Vous pouvez modifier le menu de navigation en allant à: **Administer**> **Customize**> **Menu de navigation**,  puis ajouter ou réorganiser les éléments de menu à l'écran. N'oubliez pas que les changements que vous apportez au menu de navigation seront visibles par tous ceux qui ont les autorisations appropriées pour voir le menu... pour le meilleur ou pour le pire ! Soyez donc prudent lorsque vous modifiez le menu de navigation.

À gauche du menu de navigation se trouve le champ de recherche rapide. Reportez-vous au chapitre Recherche pour plus de détails.

Tableau de bord et indicateurs  
-------------------------------
Lorsque vous vous connectez pour la première fois à CiviCRM, la première page que vous verrez est le tableau de bord (CiviCRM Home). Ce tableau de bord vous permet de voir des informations importantes sur votre site en affichant une série "d'indicateurs". Un Indicateur est un rapport que vous pouvez afficher sur votre tableau de bord. De nombreux indicateurs sont proposés par défaut, et vous ou votre administrateur pouvez en créer d'autres spécifiques aux besoins de votre organisation. Voici quelques exemples de tableaux de bord fournis avec CiviCRM:

-   Rapport des donateurs : un graphique à barres du montant total des contributions par mois pour les cinq derniers mois.
-   Activités : une liste des activités récentes qui ont été enregistrées par CiviCRM (cela peut inclure les courriels envoyés aux membres, les dons qui ont été faits, ou les réunions qui ont été prévues dans CiviCRM).
-   Rapport d'adhésion : un tableau résumant les informations sur les membres suivis, ventilé par mois. Cela comprend entre autre le nombre de membres de chaque type, les montants totaux des paiements effectués et le nombre de contributions versées.

![Dashboard_homescreen](/img/CiviCRM_update-CiviCore-Dashboard_homescreen-en.jpg "Dashboard_homescreen")

Vous pouvez ajouter des indicateurs à votre tableau de bord CiviCRM en cliquant sur le bouton **Configurer votre tableau de bord**. Vous verrez une liste d'indicateurs disponibles qui peuvent être déplacés dans la colonne de droite ou de gauche de votre tableau de bord.

![Dasboard_editscreen](/img/CiviCRM_update-CiviCore-Dasboard_editscreen-en.jpg "Dasboard_editscreen")

Cliquez sur **Terminé** pour enregistrer votre tableau de bord. Vous verrez les mises à jour de l'état de vos indicateurs chaque fois que vous vous connectez (si vous souhaitez vérifier et voir les modifications plus récentes, vous pouvez toujours cliquer sur **Rafraichir les données du tableau de bord** pour afficher les nouvelles informations. Pour des raisons de performance, les tableaux de bord sont mis en cache. Pour modifier la fréquence d'actualisation du tableau de bord :  **Administer**> **Paramètres système**> **Misc**,  éditer :  **Dashboard cache timeout**.

Presque tous les rapports de CiviCRM peuvent être disponibles comme indicateur.

Pour créer un indicateur, procédez comme suit:

-   Cliquez sur **Rapports> Créer un compte rendu à partir d'un modèle**.
-   Sélectionnez le modèle de rapport que vous souhaitez utiliser.
-   Choisissez les critères que vous souhaitez afficher dans votre indicateur dans les onglets "Sorting" et "Filters". Par exemple, vous pouvez vouloir que la version du tableau de bord affiche toujours les données telles que «Ce trimestre» ou «Cette année». Vous pouvez également choisir d'afficher le rapport sous forme de tableau (par défaut), de barre ou de camembert.
-   Cliquez : **View result**.
-   Puis cliquez sur l'onglet **Acces**
-   Sélectionnez  **Disponible pour le tableau de bord ?**. Les utilisateurs avec les permissions appropriées peuvent ajouter ce compte rendu à leur tableau de bord. (Consultez la section sur les autorisations pour plus d'informations)
-   Dans le menu déroulant **Action**  cliquez **Créer un compte rendu**.

Maintenant vous pouvez ajouter cet indicateur sur votre tableau de bord.
 
-   Cliquez sur **Home**  (Logo civicrm du menu) puis **Accueil Civicrm** pour accéder à votre tableau de bord.
-   Cliquez **Configurez votre tableau de bord**. 
-   Faites-le ensuite glisser de la zone "Indicateur disponibles" à la colonne (gauche - droite) où vous souhaitez qu'il apparaisse.
-   Cliquez sur **Terminé**. 

Note : Reportez-vous au chapitre "Rapports" pour plus de détails sur le fonctionnement des rapports.

