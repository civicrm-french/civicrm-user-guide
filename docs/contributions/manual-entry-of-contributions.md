# Entrée manuelle des contributions 

Lorsque votre organisation reçoit une contribution d'un contact, vous pouvez l'ajouter à son enregistrement. Ceci sera fait automatiquement si le paiement est effectué via CiviCRM (par exemple: une cotisation, un abonnement ou le règlement de frais d'événement avec une inscription en ligne) mais les paiements hors ligne (espèces, chèques, etc.) devront être enregistrés manuellement pour s'assurer que les rapports générés par CiviCRM soient précis.


## Ajouter des contributions manuellement une par une

Si le donneur n'existe pas déjà dans la base de données, vous devez d'abord créer un nouvel enregistrement de contact. Voir [Contacts](../organisation-vos-données/contacts) pour des informations sur la façon de procéder. Une fois l'enregistrement créé, vous pouvez entrer la contribution.

Pour entrer manuellement une contribution pour un contact dans votre base de données:

1. Recherchez l'enregistrement du contact à l'aide de l'un des outils de recherche de contacts, par exemple **Rechercher> Rechercher des contacts**.
2. Sélectionnez l'onglet **Contributions** du contact.
3. Cliquez sur **Enregistrer la contribution (Chèque, Espèces...)**. Si vous avez configuré un processeur de paiement qui autorise les transactions par carte de crédit directement sur votre site, vous pouvez sélectionner l'option **Soumettre la carte de crédit** et traiter le paiement immédiatement.
4. Remplissez le nouveau formulaire de contribution. La capture d'écran suivante montre le formulaire de contribution hors ligne (c'est-à-dire les contributions par chèque, espèces, etc.). Si vous avez choisi d'enregistrer une contribution par carte de crédit, le formulaire de carte de crédit est presque identique à l'exception des champs liés au paiement.

![Image](/img/New%20Contribution%20by%20Contact.png)

5. Notez le type financier, le montant, la date de réception (la date par défaut est la date du jour), la date de réception (indiquée sur le reçu généré par le système) et le statut (la valeur par défaut est Terminé). Tous les champs personnalisés pour les contributions apparaîtront également sur ce formulaire.
6. Le champ **Bénéficiaire (Soft Credit To)** fonctionne avec les Pages de Campagne Personnelles (PCP) qui exploitent la participation de vos contacts pour les campagnes. Lorsque vous saisissez un don manuellement sur le formulaire de contribution du contact, vous pouvez l'attribuer à un bénéficiaire propriétaire du PCP. Il y a plus d'informations sur les PCP et les pages de collecte de fonds de campagne dans le chapitre "Configuration" de la section CiviContribute.
7. La section **Détails supplémentaires** près du bas de l'écran offre d'autres options, y compris l'ajout d'une note sur la contribution et la saisie de la date à laquelle une lettre de remerciement a été envoyée.
8. Les deux dernières sections vous permettent d'indiquer si la contribution était en l'honneur de quelqu'un d'autre (**Renseignements sur le bénéficiaire**) et s'il y a une prime ou un cadeau associé à la contribution (**Information sur les primes**).
9. Cliquez sur **Enregistrer** ou sur **Enregistrer et Nouveau** si vous devez entrer d'autres contributions.

**!!! CONSEIL**  Si vous constatez que vous devez saisir plusieurs contributions en même temps, pensez à utiliser la méthode **Entrées de données par lot**.

## Inscription par lots de la contribution, de l'adhésion ou des paiements d'engagement

La fonction **Entrées de données par lot** vous permet d'entrer simultanément plusieurs contributions, adhésions ou dons reçus hors ligne, à l'aide d'un écran de saisie par lots  pour remplir rapidement les valeurs des champs (vous pouvez utiliser les icônes «autocopy» en haut de chaque colonne). Ceci facilite la saisie de données lorsque vous avez de nombreux paiements à enregistrer en même temps. Cela vous permet également de vérifier le montant total et le nombre par rapport aux paiements enregistrés sur votre ou vos bordereaux de dépôt à la banque.

Chaque lot peut contenir des paiements de cotisations ou des paiements d'adhésion ou des paiements de dons. Pendant la saisie des données par lot, vous pouvez créer de nouveaux contacts à la volée. Vous pouvez enregistrer le lot et revenir plus tard pour continuer à entrer les paiements. Si vous disposez des autorisations appropriées, vous pouvez également modifier le nombre total et le nombre d'éléments dans la définition du lot si nécessaire.

Voici un mémo simple pour la saisie de données en masse:

1. Créez un nouveau lot pour la saisie de données.
2. Entrez les cotisations, les cotisations ou les paiements de gage (chèque, espèces, etc.).
3. Validez et traitez les totaux du lot ou sauvegardez le lot.

Les détails de chaque étape sont énumérés ci-dessous.

### 1. Créer un nouveau lot pour la saisie de données 

Créez un nouveau lot pour conserver les multiples paiements que vous souhaitez enregistrer:  

Dans le menu, cliquez sur **Contributions> Entrée de données par lots** ou **Adhésion> Entrée de données par lots**.
 
![image](/img/New%20Data%20Entry.png)

Entrez les informations suivantes:

- **Nom du lot**: CiviCRM créera un nom de lot par défaut ("Lot N" + date d'ouverture), que vous pouvez modifier (champ obligatoire)
- **Type**: sélectionnez le type de paiement, par ex. Contribution, adhésion ou dons. Cela permet de sélectionner le profil réservé approprié à afficher dans l'écran de la grille de saisie par lots (profil d'entrée de lot de contribution, profil d'entrée de lot d'adhésion ou profil d'entrée de lot de paiement de don)
- **Statut**: la valeur par défaut sera "Ouvert" 
- **Nombre d'articles**: total des lignes de paiement dans le lot (champ obligatoire)
- **Montant total**: montant total de tous les postes de paiement du lot (champ obligatoire)

!!! Note: une fois qu'un lot a un "statut fermé", le lot ne sera plus modifiable)

Vous pouvez modifier ou supprimer des informations sur les lots ultérieurement en retournant à l'écran **Entrée de données par lots**, puis en cliquant sur **Modifier** ou **Supprimer** à côté du lot souhaité.

![image](/img/CiviCRM-Contributions-everydaytasks-batches-lists.jpg)

### 2. Saisie de paiements de contribution, d'adhésion ou don (chèque, espèces, etc.) 

Dès que vous avez entré les informations sur le lot, vous pouvez commencer à saisir des paiements sur chaque ligne.

![image](/img/CiviCRM-Contributions-everydaytasks-batchentrycontrib.jpg)

Il y a huit champs qui apparaissent pour tous les lots:

-  **Contact**. Dans cette colonne, vous pouvez:
- Commencez à entrer le nom d'un contact existant et CiviCRM renverra une liste de noms de contacts potentiels pour que vous puissiez sélectionner, OU
- créez un nouveau contact en cliquant sur la liste déroulante pour "créer un nouveau contact" et en sélectionnant le type de contact que vous souhaitez créer: **Nouveau individuel**, **Nouvelle organisation** ou **Nouveau ménage** et entrez les informations sur le contact ici.
!!! Remarque: Si des informations de contact telles que le numéro de téléphone ou l'adresse e-mail sont incluses dans la grille du profil, ces valeurs renseignées pour un contact existant peuvent être mises à jour si nécessaire.
-   **Type financier**
-   **Montant**
-   **(Statut) de paiement**
-   **Reçu - Date et heure**
-   **Envoyer un reçu: cochez la case si vous voulez envoyer un reçu par courriel**
-   **Bénéficiaire (Soft Credit)**
-   **type de Bénéficiaire (Soft Credit Type)**

Lorsque vous saisissez par lot des paiements de contribution, les champs supplémentaires du profil standard sont:

- **Source**: entrez du texte qui décrit la source du paiement
- **Payé par**: entrez le type de moyen de paiement, par ex. espèce, chèque, etc.
- **Numéro de chèque**: si payé par chèque
- **ID de facture**

Lorsque vous saisissez par lots les paiements d'adhésion, vous pouvez choisir d'ajouter un nouvel abonnement ou de renouveler un abonnement existant. Les champs supplémentaires dans le profil standard sont:

- **Type**: Pour un nouvel abonnement, vous sélectionnez l'organisation et le type d'adhésion. Pour le renouvellement, vous pouvez changer le type d'adhésion.
- **Membre depuis:**  Lorsque vous ouvrez le formulaire de saisie par lots, celui-ci est rempli avec la date actuelle. Si vous choisissez de renouveler un abonnement, il changera pour afficher la date de début de cette adhésion mais elle peut être modifié au besoin.
- **Date de début** (réservé): Ce champ est vide. Vous n'avez besoin de remplir ce champ que si vous souhaitez que la date de début soit différente de la valeur par défaut.
- **Date de fin** (réservé): Si cette case est laissée vide, CiviCRM utilisera les règles d'adhésion pour la mettre à la bonne date.
- **Source**: entrez du texte qui décrit la source du paiement
- **Payé par**: entrez le type de moyen de paiement, par ex. espèce, chèque, etc.
- **Numéro de chèque**: si payé par chèque
- **ID de facture**

Lorsque vous saisissez par lots des paiements de promesse de dons, vous pouvez affecter le paiement à l'un des engagements en attente pour ce contact. Si vous disposez des autorisations appropriées, vous pouvez également modifier le montant ou le calendrier de paiement. (Cliquez sur **Ajuster le montant du paiement** à côté du champ **Montant**.) Les champs supplémentaires dans le profil standard sont:

- **Source**: entrez du texte qui décrit la source du paiement
- **Payé par**: entrez le type de moyen de paiement, par ex. espèce, chèque, etc.
- **Numéro de chèque**: si payé par chèque
- **ID de facture**

### 3. Valider et traiter les totaux du lot ou sauvegarder le lot

Vous pouvez saisir toutes les transactions pour le lot en une seule session, ou simplement enregistrer le lot et compléter l'entrée de données ultérieurement.

Si vous souhaitez continuer à entrer des informations dans ce lot ultérieurement, cliquez sur **Enregistrer et continuer plus tard**.

Pour rechercher et ajouter ou modifier plus de transactions dans le lot ultérieurement:

- Dans le menu, cliquez sur **Contributions> Entrées de données par lot** ou cliquez sur **Cotisation> Entrées de données par lot**, puis cliquez sur **Enter Records** à côté du lot que vous voulez
Ensuite, continuez à entrer d'autres transactions dans le lot

Une fois que vous avez saisi les paiements dans le lot, cliquez sur **Valider et traiter le lot**. Le statut du lot sera défini sur "**Fermé**" et sera disponible pour les recherches et les rapports ultérieurs.

Si le nombre total ou le nombre d'éléments ne correspondent pas aux valeurs que vous avez saisies lors de la création du lot, vous serez alerté lors de la fermeture si le nombre ou le total ne correspond pas. Dans ce cas, vous:

- Vous pouvez remplacer le nombre et le total saisis en cliquant sur le bouton **Ignorer l'incohérence et traiter le lot?**, auquel cas les valeurs du lot seront mises à jour pour correspondre aux transactions du lot, puis le statut du lot est défini à "**Fermé**", OU

- Vous pouvez continuer à saisir ou modifier les paiements pour le lot, puis **Valider et traiter le lot** à nouveau.

![image](/img/CiviCRM-Contributions-everydaytasks-ignoremismatchbatch.jpg)


### Recherche de cotisations, d'adhésions ou de promesses de dons dans des lots vérifiés et traités 

Vous pouvez rechercher des contributions ou des paiements d'adhésion dans des lots vérifiés et traités de plusieurs manières:

- Dans le menu, cliquez sur **Rechercher> Rechercher des contributions**, entrez les critères pour les contributions, et sous **Nom du lot**, sélectionnez le lot que vous voulez.
- Dans le menu, cliquez sur **Rechercher> Recherche avancée**, entrez les critères du contact, puis ouvrez la section Contributions et entrez les critères de contribution, et sous **Nom du lot**, sélectionnez le lot souhaité.
- Dans le menu, cliquez sur **Contributions> Lots**, puis sélectionnez **Fermé** dans le champ **Statut**.
- Dans le menu, cliquez sur **Adhésion> Lots**, puis sélectionnez **Fermé** dans le champ **Statut**.
- Dans le menu, cliquez sur **Paiement de dons> Lots**, puis sélectionnez **Fermé** dans le champ **Statut**;
- Dans le menu, cliquez sur **Rapports> Créer des rapports à partir de modèles**, puis sur **Détails du rapport de contribution**, entrez vos critères de rapport et sous **Définir les filtres**, à côté de **Nom du lot**, sélectionnez "**est l'un des** "ou" **n'est pas un de** "et sélectionnez le (s) nom (s) du (des) lot (s) que vous voulez.


### Configuration des profils pour la saisie par lots des paiements de contribution, d'adhésion et dons 

Pour modifier le profil utilisé lorsque vous souhaitez créer un nouveau contact pour un individu, un ménage ou une organisation lors de l'enregistrement de la contribution, mettez à jour les profils réservés appelés **Nouveau individuel**, **Nouveau ménage** ou **Nouvelle organisation** en conséquence. Pour modifier les champs d'informations que vous souhaitez collecter pour ces contacts:

- Allez dans le menu et cliquez sur **Administrer> Personnaliser les données et les écrans> Profils**, puis cliquez sur l'onglet **Profils réservés**. Cliquez sur **Champs** et ensuite **Nouveau Individuel, Nouveau ménage** ou **Nouvelle organisation**.

- Vous pouvez ensuite ajouter, modifier ou réorganiser les champs comme vous souhaitez les voir apparaitre dans la grille d'entrée d'entrée par lots. Pour en savoir plus sur l'utilisation des profils, voir le chapitre "Profils" dans la section "Interface utilisateur".

**!!! CONSEIL:** Les profils réservés pour **Nouveau individuel, Nouvelle organisation** et **Nouveau ménage** sont utilisés dans d'autres domaines de CiviCRM. Sachez que, si vous modifiez ces profils pour une utilisation avec les **Lots**, les  modifications que vous faites, apparaîtront également sur d'autres écrans permettant de créer un nouveau contact en ligne.

  ![image](/img/CiviCRM-Contributions-SetUp-new-individual-profile.jpg)
  
  Ci-dessus, la configuration par défaut de CiviCRM pour le profil "Nouveau individuel", qui est utilisée lorsque vous choisissez de créer un nouveau contact individuel lors de la saisie par lot de cotisations ou de paiements d'adhésion.

Pour modifier le profil des champs d'informations que vous souhaitez collecter pour les cotisations ou les paiements d'adhésion, vous devez mettre à jour les profils réservés appelés **Contribution par lot de contribution * ou **Inscription de lot d'adhésion**:

- Allez dans le menu et cliquez sur **Administrer> Personnaliser les données et les écrans> Profils**, puis cliquez sur l'onglet **Profils réservés**. Cliquez sur **Champs** à côté du profil **Entrées de Contribution par lots** ou du profil **Entrées d'adhésion par lots**.
- Vous pouvez ensuite ajouter, modifier ou réorganiser les champs de ce profil. Par ex. vous pouvez avoir d'autres champs de contribution personnalisés que vous souhaitez afficher dans la grille d'entrée de l'entrée de lot. Pour en savoir plus, lisez [Profils](../organising-your-data/profiles)

  ![image](/img/CiviCRM-Contributions-SetUp-contribution-batch-entry-profile.jpg)
  
  Ci-dessus, la configuration par défaut de CiviCRM pour le profil "Entrées de données par lots", utilisée lorsque vous enregistrez des informations sur la contribution ou le paiement de don d'un contact.

  ![image](/img/CiviCRM-Contributions-SetUp-membership-batch-entry-profile.jpg)
  
  Ci-dessus, la configuration par défaut de CiviCRM pour le profil "Entrées d'adhésion par lots", utilisée lorsque vous enregistrez des informations sur le paiement de l'adhésion d'un contact.


## Importer des Contributions

Si vous n'avez pas importé de données auparavant, veuillez lire  [Import de données dans Civicrm](../common-workflows/importing-data-into-civicrm). 

Lors de la préparation de votre importation de données, il est utile de savoir quels champs sont requis pour l'importation. Vous devez vous assurer que ces champs sont inclus dans votre fichier d'importation CSV. Voici une liste des champs obligatoires. 
!!! Veuillez noter que vous avez seulement besoin d'un des champs marqués **(Correspondre au contact)**

  -   **Contact ID (Match to Contact)**
  -   **Email (Match to Contact)**
  -   **Identifiant Externe(Match to Contact)**
  -   **Type financier**
  -   **Montant Total**

L'outil d'importation pour les contributions est similaire à celui des contacts, mais les contributions ne peuvent être importées que si les contributeurs existent déjà dans la base de données en tant que contacts. Si vous devez importer des contributions pour des contacts qui ne sont pas encore disponibles, commencez par importer les contacts, en incluant de préférence un identifiant externe unique (le plus souvent un identifiant attribué par la base de données ou l'application à partir de laquelle vous importez des enregistrements). Il existe deux façons de faire correspondre une contribution à un contact:

- Utilisez l'ID externe du contact en incluant l'ID dans une colonne du fichier CSV (si cet ID n'a pas été importé avec les contacts, bien que vous les ayez enregistrés, une deuxième importation de contacts peut être effectuée pour mettre à jour ce champ, après quoi vous pouvez importer des contributions).
- Vous pouvez également faire correspondre les contributions aux contacts en fonction de vos règles de déduplication des contacts, par ex. en incluant le prénom, le nom et l'adresse électronique du donateur pour chaque contribution. Si un contact correspond à ces trois champs, la contribution lui sera affectée.

**!!! NOTE** N'oubliez pas que les fichiers CSV doivent avoir **une taille inférieure à 2 Mo**. Si la taille du fichier dépasse cette valeur, créez plusieurs fichiers CSV et répartissez les données entre eux.

