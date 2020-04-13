Trouver et afficher des adhésions
===============================

Ce chapitre décrit comment afficher et rechercher vos enregistrements d'adhésion.

Affichage de vos adhésions
------------------------

Pour voir un résumé de l'état de vos adhésions ainsi que les détails de ces adhésions au cours des derniers mois, vous pouvez utiliser le tableau de bord des adhésions ou consulter une adhésion dans le dossier individuel de chaque contact 

### Le Tableau de bord des adhésions

Le tableau de bord des adhésions permet d'afficher rapidement vos adhésions récentes, utilisez  : **Adhésions> Tableau de bord**. Cet écran contient deux blocs d'informations qui affichent un résumé des adhésions récentes, classées selon le type et la plage de dates, et une liste de l'activité récente des membres.

![image](/img/CiviCRM-CiviMember-Memebership-Summary_2.jpg)

Ce tableau présente un résumé des nouvelles adhésions et des renouvellements d'adhésion et inclut des raccourcis pour voir les détails. Il suffit donc de cliquer sur un nombre pour analyser et afficher une liste des membres qui ont adhérés ou renouvelés au cours des deux derniers mois ou de l'année courante, ou qui sont considérés comme actifs en fonction des définitions de statut de l'adhésion. À partir de cette liste de membres, vous pouvez effectuer des actions supplémentaires sur les adhésions, telles que Supprimer, Modifier, Exporter, Envoyer un courriel.

### Affichage des enregistrements d'adhésion d'un contact

Une autre façon de voir les enregistrements d'adhésion est de consulter un enregistrement de contact et d'examiner l'onglet Adhésion. Remarque: si l'adhésion d'un interlocuteur est "En attente", l'adhésion apparaîtra lorsque l'onglet sera cliqué, mais il ne sera PAS comptabilisé dans l'onglet.
- Après avoir trouvé le contact que vous souhaitez, cliquez sur l'onglet "**Adhésion**" pour afficher un résumé des enregistrements d'adhésion du contact.

![image](/img/CiviCRM_update-CiviCore-Contact_MembershipTabs-en.jpg)

Les dossiers d'adhésion apparaissent sous forme de liste avec les adhésions actives (celles ayant un statut actuel) et suivies des adhésions anciennes ou annulées.

Vous pouvez modifier les enregistrements d'adhésion existants, renouveler une adhésion ou créer un nouvel enregistrement d'adhésion. Si vous avez configuré un processeur de paiement par carte de crédit en ligne dans CiviCRM, vous verrez deux options pour créer ou renouveler une adhésion: une pour la gestion d'un enregistrement hors ligne (pas de transaction en temps réel) et une pour la gestion d'un enregistrement en ligne (En utilisant une transaction en carte de crédit en temps réel), qui peut également être utilisé pour configurer le renouvellement automatique si le processeur le prend en charge. L'interface pour chaque processus est très similaire, sauf que l'option de carte de crédit comprend les options de traitement de paiement et d'enregistrement.

Si vous affichez un enregistrement de contact, en tant que membre principal pour un type d'adhésion, vous verrez une liste du contact qui a bénéficié de l'adhésion.

![image](/img/membership%20everyday%20for%20limited%20inherited.png)

Dans ce cas, un maximum de deux adhésions héritées sont autorisées pour les personnes qui sont des employés de l'organisation du membres principal. Si l'une des adhésions héritées disponibles n'est pas attribuée correctement à l'employé, vous pouvez cliquer sur **Supprimer** pour ce contact. Cela libérera une adhésion héritée pour attribuer une correspondance en sélectionnant **Créer**

### ![image](/img/membership%20everyday%20for%20limited%20inheritedp2.png)

Envoi de courriel aux membres
-------------------------

Après avoir recherché vos enregistrements, vous pouvez envoyer un courriel aux contacts sélectionnés et y inclure des jetons de champs de données pour personnaliser le message électronique. Pour en savoir plus sur le courrier électronique et les jetons dans CiviCRM, consultez la section intitulée «Email».

Pour envoyer un courriel aux membres :

-   Cliquez sur **Adhésion> Trouver des membres>** saisissez vos critères, puis **Rechercher**
-   Sur l'écran "Rechercher des adhésions", sélectionnez les enregistrements que vous souhaitez traiter et dans le menu déroulant **Actions**, sélectionnez **Courriel-envoi immédiat**.

Recherches basées sur les données d'adhésion
----------------------------------

CiviCRM fait une distinction importante entre les contacts et les adhésions, ce qui est flou lorsque nous parlons de «membres». Considérons la question suivante: «Combien de membres avons-nous?» Cela pourrait signifier «combien de contacts avons-nous qui sont membres?», Ou «combien d'adhésions avons-nous accordés aux contacts?». La réponse à ces questions est souvent la même, mais que se passe-t-il si l'un de vos contacts compte plusieurs membres? La réponse est que vous aurez deux adhésions mais un seul contact.  
Il n'y a pas de bonne ou de mauvaise réponse à la question si nous examinons les contacts ou les adhésions. Cela dépend simplement de ce qui vous intéresse. Il est important de prendre cela en considération lors de la recherche.

La recherche **Rechercher des membres** vous permet de rechercher en fonction des données d'adhésion et d'afficher les données d'adhésion.

-   Cliquer sur **Adhésion > Rechercher des adhésions>**, renseignez vos critères : "membre depuis le"
-   Cliquer sur le bouton **Rechercher**.

![image](/img/memberships%20find%20memberships.JPG)

La **Recherche avancée** vous permet également de rechercher en fonction de certaines informations d'adhésion (combinées avec d'autres informations de contact) et d'afficher des listes de contacts. Vous pouvez également choisir Adhésion dans la colonne **Vue pour l'affichage de contacts** afin d'afficher les membres plutôt que les contacts. Pour en savoir plus sur l'utilisation de la recherche avancée, reportez-vous au chapitre "Recherche".

![image](/img/z_sprint14_display%20Results%20as_1.png)

Dès que vous avez trouvé les informations d'adhésion en fonction de vos critères, les résultats de vos recherches vous affichent certains détails d'adhésion. Vous pouvez ensuite effectuer d'autres actions sur vos résultats de recherche ou un sous-ensemble plus petit d'enregistrements sélectionnés, tels que **Couriel-Envoi immédiat** ou **Contact-Exporter** en cliquant sur le menu déroulant **Actions**.

