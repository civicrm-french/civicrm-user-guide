Intégration comptable
======================

La fonction d'intégration comptable vous permet d'exporter toutes les transactions financières en partie double pour un lot de contributions afin que vous puissiez les importer dans votre logiciel de comptabilité. Vous pouvez créer un nouveau lot de comptabilisation, puis lui affecter des contributions existantes ou réutiliser un lot créé lors de la saisie de données par lot en tant que lot de comptabilisation.

Utiliser un lot créé via la saisie de données par lots
---------------------------------------------

La saisie par lots des transactions est traitée dans [Saisie manuelle des contributions](../contributions/manual-entry-of-contributions)

Après avoir validé et fermé un lot, il apparaîtra dans la liste des lots de la comptabilité avec le statut Fermé.

Créer un nouveau lot à partir de transactions existantes
-----------------------------------------------

### Créer le lot

Allez à **Contributions> Lots comptables** et sélectionnez **Nouveau lot.** 
Cela ouvre l'écran de création de lot dans lequel vous définissez les paramètres de lot : 

![Nouveau lot comptable](/img/civicontribute-accounting-integration-new-batch.png)

-  Entrez le nom du lot (obligatoire). CiviCRM créera un nom de lot par défaut ("lot N" + date d'ouverture), que vous pouvez modifier.
-  Vous pouvez éventuellement entrer une description du lot. 
-  Si vous souhaitez que ce lot contienne uniquement les transactions payées par un instrument de paiement spécifique, sélectionnez-le dans la liste déroulante: Carte de crédit, Carte de débit, Chèque, Espèces ou TEF, ou tout autre instrument de paiement personnalisé que vous avez configuré.     
-  Si vous connaissez à l'avance le nombre de transactions qui seront dans le lot, saisissez-le dans "Nombre de transactions". Lorsque vous fermez le lot, CiviCRM vérifie que vous avez entré un nombre correct. (Vous aurez la possibilité de modifier l'avertissement s'il ne correspond pas.)     
-  Si vous connaissez à l'avance le montant total des transactions qui seront dans le lot, entrez-le dans "Montant total". Lorsque vous fermez votre lot, CiviCRM vérifie que les totaux entrés correspondent à ce montant. (Vous aurez la possibilité de remplacer l'avertissement s'il ne correspond pas.)      
- **Enregistrez**

Vous pouvez toujours modifier ces paramètres tant que le lot reste ouvert.  

### Affecter des transactions à un lot 

Après avoir créé un nouveau lot de comptabilité ou en avoir ouvert un, vous aurez l'écran d'assignation de transaction :  

![Ecran de Transaction](/img/civicontribute-accounting-batches-transactions.png)

En haut de l'écran, les paramètres définis du lot sont affichés:  

-   créé par
-   statut (ouvert, fermé, ou exporté)
-   la description entrée lors de la création du lot 
-   l'instrument de paiement spécifié  
-   le nombre de transactions saisies  
-   le nombre de transactions attribuées   
-   le montant total saisi des transactions  
-   le montant total attribué (qui sera mis à jour lorsque vous affectez des transactions au lot)  
-   la date à laquelle le lot a été ouvert.   

Au-dessous, une liste des transactions affectées au lot qui est vide jusqu'à ce que vous affectiez des transactions au lot. Il existe également une sélection de liste déroulante d'actions qui ne sera pas disponible tant que les transactions ne seront pas affectées au lot.   

Vient ensuite l'accordéon **Editer les critères de recherche**. Cliquez pour ouvrir le volet de recherche. Si un instrument de paiement a été sélectionné lors de la création du lot, cette option sera sélectionnée par défaut. Spécifiez les critères pour les contributions que vous souhaitez ajouter au lot.

Au bas de la page se trouve la liste des résultats de la recherche. Vous pouvez assigner une seule transaction au lot en cliquant sur "Affecter" à la fin de la ligne de résultat. Ou bien vous pouvez sélectionner plusieurs transactions et utiliser le menu d'action au-dessus des résultats pour sélectionner "Affecter à un lot". Les transactions seront ajoutées à la liste des transactions affectées et seront supprimées des résultats de la liste de recherche
  

### Afficher et supprimer les transactions attribuées

Une fois que vous avez affecté des transactions au lot, elles apparaîtront dans la liste des transactions affectées au milieu de la page.
Si vous devez supprimer des transactions du lot, sélectionnez "Supprimer" à la fin d'une ligne d'une transaction, ou sélectionnez plusieurs transactions et utilisez le menu d'action au-dessus de la liste pour sélectionner "Supprimer du lot".
Vous verrez également les modifications apportées au tableau des paramètres en haut de la page, reflétant le nouveau nombre et le montant total des transactions assignées.

Si vous voulez retourner et éditer le lot plus tard, il vous suffit de retourner à la page principale du traitement par lots. L'état du lot restera "Ouvert".


## Fermer et exporter un lot terminé   

Une fois que vous avez terminé l'affectation des transactions, vous pouvez fermer le lot, ou le fermer et l'exporter. 

Si vous tentez de fermer le lot et que le nombre de transactions que vous avez indiqué ne correspond pas au nombre de transactions entrées, ou si le montant total de la transaction ne correspond pas au montant total saisi, un message d'erreur "Incompatibilité" s'affiche. Vous pouvez fermer le message d'erreur et revenir au lot pour corriger la non-concordance, ou vous pouvez cliquer sur "OK" pour remplacer l'erreur; le numéro de transaction saisi et le montant total seront mis à jour pour correspondre au numéro de transaction attribué et au montant total, et le lot sera fermé 

Si vous fermez le lot sans l'exporter, l'état du lot devient "Fermé". Vous pouvez réouvrir le lot plus tard, avant de l'exporter, ou vous pouvez exporter plus tard les transactions.

Si vous fermez et exportez le lot, vous pouvez choisir votre format d'exportation.

"CSV" produira une feuille de calcul avec les valeurs séparées par des virgules. "IIF" produira un fichier au format Intuit Interchange, qui est utilisé par les produits Intuit tels que Quickbooks pour importer des transactions. Une fois les transactions exportées, l'état du lot devient "Exporté". Un lot exporté ne peut pas être réouvert.


## Rechercher et agir sur des lots 

Allez à **Contributions> Comptabilisation des lots** et sélectionnez **Ouvrir les lots** pour accéder à la page principale du traitement comptable. Ici, vous pouvez filtrer la liste des lots affichés par statut (ouvert, fermé ou exporté), nom du lot, l'utilisateur qui l'a créé, l'instrument de paiement, le nombre entré de transactions et le montant total saisi.

Si un lot a le statut Ouvert, sélectionnez "Transactions" pour affecter ou supprimer des transactions, ou sélectionnez "Modifier" pour modifier les paramètres du lot. Sous "plus", vous pouvez choisir de fermer, exporter ou supprimer le lot.

Si un lot a le statut Fermé, sélectionnez "Transactions" pour afficher les transactions affectées, ou sélectionnez "Exporter" pour exporter les transactions affectées vers un fichier d'exportation CSV ou IFF. Sous "plus", vous pouvez choisir de réouvrir ou de supprimer le lot.

Si un lot a le statut Exporté, sélectionnez "Transactions" pour afficher les transactions affectées au lot, sélectionnez "Télécharger" pour exporter le fichier CSV ou IIF des transactions affectées ou sélectionnez "Supprimer" pour supprimer le lot. Une fois qu'un lot est exporté, il ne peut pas être réouvert.

À partir de la page de résultats de recherche, vous pouvez également effectuer des actions sur plusieurs lots. Sélectionnez tous les lots à mettre à jour et choisissez une option dans le menu déroulant des actions: Réouvrir, Fermer, Exporter ou Supprimer.


Recherche de transactions par lots
-----------------------------

Dans le volet Recherche de Contribution avancée ou dans Rechercher des contributions, vous pouvez effectuer une recherche par nom de lot. Sélectionnez un lot et les résultats renverront toutes les transactions stockées dans le lot.
