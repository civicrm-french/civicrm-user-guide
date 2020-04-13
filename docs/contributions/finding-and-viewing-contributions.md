# Tableau de bord CiviContribute  

La page principale ou tableau de bord de CiviContribute résume les contributions effectuées, y compris les listes de contributions reçues depuis le mois en cours, depuis le début de l'année et cumulativement depuis le début (tous les enregistrements de contribution de votre installation CiviCRM). Cela vous permet de parcourir facilement les contributions qui ont été enregistrées automatiquement ou ajoutées manuellement. Le tableau de bord fournit également des boutons pour gérer et ajouter des pages de contribution.

Différentes dispositions sont disponibles pour l'affichage des résumés. La capture d'écran suivante montre la contribution la plus récente à une campagne à l'aide de l'onglet "Disposition de la table"

![ContactSummary1a](/img/CiviCRM-CiviContribute-EveryDayTasks-ContactSummary1a-en.png)

Vous pouvez également afficher des diagrammes à barres ou à secteurs pour comparer les totaux de cotisations entre plusieurs mois d'une année donnée et d'une année à l'autre en cliquant sur l'onglet "Disposition du diagramme".

![ContactSummary1b](/img/CiviCRM-CiviContribute-EveryDayTasks-ContactSummary1b-en.png "ContactSummary1b")

Enfin, vous pouvez ajouter n'importe quel nombre d'instances de rapport de contribution à votre tableau de bord personnel CiviCRM. Ceux-ci peuvent inclure un résumé des histogrammes des contributions cumulées par type financier ou mensuel, une liste des 10 principaux donateurs, etc... Reportez-vous à la section _Rapports_ pour plus de détails sur l'ajout de rapports ("dashlets") à votre tableau de bord personnel.

# Rechercher des contributions 

CiviCRM fait une distinction importante entre les contributions et les personnes qui ont donné des contributions. Il est important d'apprécier la différence entre les deux lorsque vous recherchez des contributions. 
Par exemple, si vous voulez envoyer un cadeau à toutes les personnes qui ont donné une contribution au cours de la dernière année : qu'est-ce qui serait le plus approprié? Contacts ou contributions? La réponse dépend si vous voulez envoyer deux cadeaux à des personnes qui ont fait deux contributions, etc... : il n'y a pas, bien sûr, de bonne ou de mauvaise réponse ! cela dépend simplement de votre approche. Il est important d'y penser à chaque fois pour faire une recherche.

La recherche **Rechercher des contributions** vous permet d'effectuer une recherche en fonction des données de contribution et des enregistrements de contribution. Il se trouve à **Contributions> Trouver des contributions**.

![Contribution Find Screenshot](/img/contributions-find-search.png)

Vous pouvez effectuer une recherche en fonction d'un certain nombre de critères, tels que la période, le montant de la contribution, le statut de la contribution, etc... Les contributions doivent correspondre à tous les critères spécifiés pour être renvoyées. Par exemple, si vous recherchez le type de don "Type de don" et la plage de dates "1er janvier au 31 mai", les contributions répondant aux deux critères seront retournées. Les plages de dates relatives telles que "Dernier mois" ou "Dernière année" sont souvent très utiles.

En plus du sous-ensemble d'enregistrements résultant de la recherche, l'écran des résultats d'une "Recherche de contributions" affiche le montant total, le nombre de contributions, la moyenne des contributions et le mode pour les résultats de la recherche.

  ![Screen shot batch update from search](/img/contributions-find-editcriteria.png)

Vous pouvez sélectionner une action à effectuer à partir du menu **Actions** dés que vous avez sélectionné tout ou un sous-ensemble des résultats. Vous pouvez:
 
- **Mettre à jour plusieurs contributions** : Ceci est utile par exemple si vous souhaitez mettre à jour un grand nombre de contributions à la fois. Vous devez [créer le profil](/organising-your-data/profiles.md) que vous voulez utiliser *avant* d'effectuer la recherche et la mise à jour par lots.

- **Supprimer les contributions**: Ceci supprime entièrement les contributions du système, comme si elles n'avaient jamais été entrées en premier lieu. La modification des contributions et la mise à jour de leur statut sur "annulé" fournissent une meilleure piste de vérification, mais il peut arriver que vous vouliez supprimer certaines situations, par exemple une contribution saisie dans le dossier du mauvais contact.

- **Exporter les contributions**: NOTE: Ceci est une exportation de contributions. Si vous choisissez d'exporter plusieurs contributions d'un même contact, vous vous retrouverez avec une ligne pour chaque contribution dans votre fichier d'exportation. Si vous souhaitez effectuer des recherches qui renvoient un résultat par contact, utilisez la recherche avancée de contact.

- **Reçus - Impression ou Email** : Ceci vous permet de créer un fichier PDF de tous les reçus de la recherche, ou envoyer un courriel aux donateurs sélectionnés. Voir "Envoyer des lettres de remerciement" ci-dessous pour plus d'informations.

- **Email - Envoyer maintenant**: Envoyer un e-mail à tous les contacts sélectionnés ou sélectionnés dans la recherche.

- **Lettres de remerciement - imprimer ou envoyer par courriel**: Créer une lettre PDF personnalisée pour chacun des contributeurs sélectionnés, avec la possibilité de mettre à jour le reçu ou la date de remerciement pour chacun.

- **Mettre à jour le statut de la contribution en attente**: Ceci vous permet d'enregistrer les détails des paiements et de mettre à jour le statut de la contribution pour toutes les contributions en ligne «payer plus tard» ou sélectionnées. Cette action ne fonctionne que pour les contributions avec le statut En attente (Payer plus tard). Le même statut de contribution sera appliqué à toutes les contributions sélectionnées pour la mise à jour.

La **Recherche avancée** renvoie les contacts par défaut, mais vous pouvez choisir **Contributions** pour le champ **Afficher les résultats sous** pour afficher les contributions plutôt que les contacts. Les critères standard de recherche de contribution sont disponibles lorsque vous développez le volet Contributions, mais vous pouvez également filtrer vos résultats avec des critères supplémentaires ("Trouver tous les dons des membres de mon organisation" ou "Afficher tous les contacts qui ont contribué plus de 100 € l'année dernière ET qui résident en Ile de france").
 
