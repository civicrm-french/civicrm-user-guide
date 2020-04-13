Groupes dynamiques
====================

Les groupes dynamiques sont considérés comme étant des **«recherches enregistrées»**. Ils sont utiles pour suivre les groupes de contacts répondant à certains critères, par exemple « toutes les cotisations versées en 2015». 
La création d'un groupe dynamique est simple : Menu **Recherche** : vous effectuez une recherche en fonction de vos critères, puis choisissez «Créer un groupe dynamique». Une fois le groupe dynamique créé, chaque fois que vous demandez de voir les contacts de ce groupe, CiviCRM effectuera une recherche et affichera les contacts qui répondent aux critères que vous avez spécifiés.

Les groupes dynamiques sont une partie vraiment puissante et utile de CiviCRM et dans de nombreuses situations. Passez du temps à bien en comprendre le fonctionnement et comment vous pouvez être en mesure de les utiliser.

Quand puis-je utiliser un groupe dynamique ?
-------------------------------
Voici deux exemples :

### Groupes et profils dynamiques: une liste d'adhésions 

Un groupe dynamique peut être utilisé en association avec un profil pour afficher une liste de membres sur votre site Web. Pour ce faire, créez un groupe dynamique qui inclut les membres de votre organisation et créez un profil qui inclut les champs que vous souhaitez afficher dans votre liste. Vous devez alors configurer le profil pour qu'il affiche uniquement les contacts qui se trouvent dans ce groupe dynamique. Lorsqu'un contact devient membre - par exemple, lorsqu'il remplit votre formulaire d'adhésion et paye en ligne - il sera automatiquement ajouté au groupe dynamique et sera donc publié dans votre liste de membres.

###  Groupe dynamique utilisé comme liste de diffusion pour la newsletter: 

Supposons qu'une personne se soit inscrite ou a participé à un événement et souhaite recevoir notre newsletter d'événements. Nous pouvons créer un groupe dynamique qui comprend toutes les personnes qui se sont inscrites ou qui ont participé à un événement et qui indique que ce groupe dynamique est une liste de diffusion. Il sera alors disponible dans CiviMail et nous pouvons l'utiliser pour envoyer la newsletter des événements. Comme les personnes s'inscrivent pour assister à un événement - ou sont marquées comme ayant assisté à un événement - elles seront ajoutées automatiquement au groupe dynamique et donc abonnées à la newsletter. Les groupes dynamiques respectent les préférences des abonnés. Si les personnes se désabonnent de la newsletter, elles seront supprimées du groupe dynamique.

Création de groupes dynamiques
--------------------------------
Des groupes dynamiques peuvent être créés à partir des résultats de recherche générés par de nombreux formulaires de recherche de CiviCRM. 

Nous pouvons créer un groupe dynamique de tous les donateurs à qui nous n'avons pas encore envoyé une lettre de remerciement, pour nous aider à gérer notre flux de travail d'envoi de remerciement aux donateurs. Après l'envoi des lettres, les donateurs qui les reçoivent quitteront automatiquement le groupe dynamique, ce qui nous permettra d'avoir une liste toujours précise de personnes à qui envoyer des lettres.

Vous pouvez utiliser la "Recherche multicritères" pour créer ce groupe dynamique (vous pouvez le tester sur le site de démonstration  [http: //demo.civicrm.org] (http://demo.civicrm.org) ...si vous n'avez pas encore de contributions dans votre installation CiviCRM).

1.  Allez dans **Rechercher> Recherche avancée**  
2.  Faites défiler jusqu'à la section **Contributions**.
3.  Cochez **Date reçue** : -n'importe laquelle - et choisissez **Donation** dans le menu déroulant **Type d'opération**.
4.  Cliquez sur **Rechercher** en bas de la page.
5.  Sélectionnez tous les enregistrements
6.  Dans le menu déroulant **Actions**, sélectionnez **Groupe - créer un groupe dynamique**.
7.  Donner au groupe dynamique un nom, une description et éventuellement le désigner comme "liste de diffusion" et indiquer  un groupe parent. Cliquez sur **Enregistrer le groupe dynamique**.

Votre groupe dynamique s'affiche maintenant aux endroits habituels avec les groupes.

Essayez maintenant de modifier un contact dans le groupe dynamique afin qu'ils ne corresponde plus aux critères sélectionnés. Vous verrez qu'il est supprimé du groupe dynamique.
Si le contact n'est pas supprimé immédiatement, il se peut que la mise en cache de groupe dynamique soit activée (voir *Mise en cache de groupe dynamique ci-dessous)*.

Modification des critères des groupes dynamiques
--------------------------------------------------
Vous voudrez peut-être aussi affiner les critères que votre groupe dynamique utilise pour sélectionner des contacts. Par exemple, vous voudrez peut-être modifier un groupe dynamique composé de tous les membres  *actuels*  pour inclure  *les nouveaux* membres également. Vous pouvez faire ceci à partir du menu "Gestion des groupes" :

Cliquez sur **Gestion des groupes**. Pour modifier les critères de recherche d'un groupe particulier, cliquez sur **Paramètres** à droite de ce groupe.

![image](/img/Groups&tags_updatecriteria_1.png)

Dans l'écran des paramètres de groupe, cliquez sur **Modifier les critères de groupe dynamique** en bas à gauche.

 ![image](/img/Groups&tags_edit%20Smart%20Group%20criteria.png)
 
Cela affichera un écran semblable à celui que vous avez utilisé à l'origine pour créer le groupe dynamique avec les résultats de recherche affichés. Cliquez sur la barre en haut de l'écran pour afficher les critères que vous avez utilisés pour définir le groupe dynamique. Vous pouvez ensuite mettre à jour les critères et, dès que vous êtes satisfait des résultats, sélectionnez tous les enregistrements et choisissez **Update Smart Group** dans le menu déroulant "Actions".

![image](/img/Groups&tags_actions%20Update.png)

Votre groupe dynamique repose maintenant sur les nouveaux critères.

Mise en cache de groupes dynamiques
-------------------------------------

Pour des raisons de performances, les groupes dynamiques sont souvent mis en cache, c'est-à-dire que les contacts répondant aux critères du groupe dynamique sont enregistrés en mémoire pendant un certain temps.

Cette vitesse de traitement augmente car CiviCRM n'a pas besoin d'exécuter la recherche chaque fois que vous souhaitez utiliser le groupe dynamique. Si votre demande est simple et n'implique qu'un petit nombre de contacts, la vitesse peut ne pas être significative. Si elle est complexe et implique de nombreux contacts, elle peut être très importante et même nécessaire.
L'inconvénient de la mise en cache est que vous devez attendre quelques minutes pour que la requête soit mise à jour. Selon la façon dont vous utilisez des groupes dynamiques, cela peut ne pas être un problème.

Le délai d'expiration par défaut pour un groupe dynamique dans les versions récentes de CiviCRM est de 5 minutes par défaut. Vous pouvez ajuster le cache de requêtes de groupe dynamique («timeout»), c'est-à-dire le temps que le cache considére comme une mémorisation valide du groupe dynamique dans **Administer> Personnaliser les données et les écrans> Préférences de recherche**.

