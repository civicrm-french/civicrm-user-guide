Ce que vous avez besoin de savoir
=================================

Afin de pouvoir utiliser CiviPledge, vous devez l'activer pour votre installation si ce n'est pas encore le cas. Aller à **Administrer** > **Paramètres système** > **Composants**, et déplacez CiviPledge dans la colonne de droite.

Nouvelles promesses de don
--------------------------

Pour créer une nouvelle promesse de don au nom d'un contact, aller à **Contributions** > **Promesses de don** > **Nouvelle promesse de don** (notez qu'un particulier peut faire lui-même sa promesse de don : cf. le chapitre [Contributions en ligne](../contributions/online-contributions.md) pour plus de détails.).

Les options suivantes sont disponibles :

-   **Sélectionnez le contact** : entrez le nom d'un contact existant, ou créez-en un nouveau avant de renseigner la promesse de don (une nouvelle fenêtre s'ouvrira) ;
-   **Montant total de la promesse de don** : entrez le montant total qui sera donné ;
-   **À payer en**: spécifiez le nombre de versements et, s'il est supérieur à un, leur périodicité ;
-   **Les paiements sont dûs le** : choisissez le jour de la période auquel chaque versement est fait (par ex. le deuxième jour de la semaine / mois / année) ;
-   **Promesse de don faite le** : sélectionnez la date à laquelle la promesse de don a été faite ;
-   **Début des paiements** : indiquez la date de départ du premier versement ;
-   **Envoyez accusé de réception ?** : si les courriels sortants sont configurés, et que le contact dispose d'une adresse courriel, vous pouvez activer cette case à cocher pour lui envoyer une notification ;
-   **Date de réception** : date à laquelle le contact a été notifié de la création de sa promesse de don (remplie automatiquement si un courriel a été envoyé - cf. option précédente) ;
-   **Type d'opération** : choisissez le type financier pour les paiements liés à cette promesse de don (don, abandon de frais...) ;
-   **Campagne** : Si elle est disponible, vous pouvez associer la promesse de don à une campagne de levée de fond ;
-   **Page de paiment en ligne** : donne au donateur la possibilité de faire lui-même le paiement à travers un formulaire de paiment en ligne ;
-   **Contributions faites en l'honneur de %1** : vous pouvez également donner le nom de la personne à qui vous dédiez votre promesse de don ;


![image](/img/new_pledge2.png)

Rappels de paiement
-------------------

Un ou plusieurs rappels de paiement peuvent être envoyés par courriel au donateur avant leur date d'échéance. Si une page de paiement en ligne a été renseignée, le courriel inclura un lien pointant sur cette dernière.

Pour que les rappels puissent être envoyés :

1.  La tâche planifiée *Process Pledges (process_pledge)* doit être active afin d'automatiquement mettre à jour le statut des promesses de don et envoyer les rappels de paiement par courriel. Ou bien un cronjob peut être planifié pour faire tourner cette tâche en dehors des autres tâches planifiées. Pour plus d'information, veuillez vous référer au chapitre [Travaux programmés](../initial-set-up/scheduled-jobs.md) ;
2.  Le donateur doit avoir une adresse courriel valide et ne pas avoir coché l'option "Ne pas envoyer de courriel" dans sa fiche contact ;

Une fois ces pré-requis satisfaits, vous pouvez paramétrer les rappels de paiement d'une promesse de don à l'aide des champs suivants :
-   **Envoyer un rappel initial**: entrez le nombre de jours en amont de la date d'échéance du paiement pour l'envoi du rappel ;
-   **Envoyer jusqu'à**: spécifiez le nombre maximum de rappels à envoyer pour chaque paiement planifié ;
-   **Envoyer des rappels supplémentaires**: paramétrez l'intervale de temps (en nombre de jours) entre les rappels ;

Rechercher des promesses de don
-------------------------------

Pour rechercher des promesses de don dans la base de donnée, allez à **Contributions** > **Promesses de don** >  **Rechercher des promesses de don**. Vous pouvez effectuer une recherche en fonction du nom ou du courriel du donateur, ou tout autre critère disponible pour chaque promesse (date de début, etc.) La page de résultat vous listera les promesses de don répondant à vos critères de recherche, et des options de visualisation, modification et suppression seront disponible pour chaque enregistrement. Si le statut d'une promesse de don est *en cours*, une option d'annulation de la promesse de don sera également disponible.

![image](/img/pledge_menu.png)

Tableau de bord
---------------

Vous pouvez visualiser une synthèse des promesses de don récentes (dans le mois courant et sur la dernière année) sur le tableau de bord. Il suffit d'aller à **Contributions** > **Promesse de don** > **Tableau de bord**.

![image](/img/pledge%20table.png)
