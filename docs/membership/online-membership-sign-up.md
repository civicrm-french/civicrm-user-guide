Adhésion des membres en ligne
=========================

Ce chapitre explique comment permettre aux visiteurs de votre site Web de s'inscrire en tant que membres de votre organisation. Nous examinerons les étapes nécessaires pour créer des pages d'abonnement d'adhésion, certains éléments sont à considérer lors de cette opération, y compris le test de vos pages d'adhésion et la façon dont vous pouvez integrer les pages d'adhésion sur votre site public.    

Avant de lire ce chapitre, il est souhaitable d'avoir pris connaissance du chapitre *Définir les adhésions* qui donne un panorama utile à de nombreux concepts (comme les types d'adhésion, les statuts de l'adhésion, etc.).

À propos des pages d'adhésion
-------------------------------------------

Les pages d'adhésions sont créées de la même manière que les pages de contribution en ligne. Essentiellement, vous créez une page de contribution en ligne, puis ajoutez à cette page la possibilité d'adhésion. La raison pour laquelle nous faisons cela est parce que la méthode réelle pour devenir membre d'une organisation est normalement assez similaire à la méthode de contribution financière à une organisation. Les lier ensemble permet aux pages d'adhésion de profiter d'une grande partie de la fonctionnalité qu'ont les pages de contribution, par exemple, vous pouvez offrir des gratuités ou cadeaux dans le cadre de nouvelles adhésions.

Notez que, même si votre adhésion est gratuite, vous devez toujours utiliser une page de contribution pour l'adhésion en ligne (voir les adhésions gratuites ci-dessous pour obtenir les instructions sur la façon de le faire).

Les pages de contribution sont très puissantes et ont de nombreuses options regroupées en onglets. Dès que vous avez donné un nom à votre page de contribution, ces onglets sont affichés en haut de la page lorsque vous travaillez dans le reste du processus de configuration.

![image](/img/membership-tabs.png)

Dans ce chapitre, nous nous concentrerons sur les onglets et les options des pages de contribution qui sont les plus utiles pour les adhésions. Quelques onglets méritant d'être mis en évidence incluent l'onglet Adhésions, contenant la majeure partie de la configuration de l'adhésion. L'onglet Profils vous permet de collecter des informations sur les personnes ou les organisations qui remplissent votre formulaire d'adhésion.

Nous vous recommandons également de consulter les chapitres sur la création de [pages de contribution en ligne](.../ contributions/contributions en ligne) qui vous permettront de mieux comprendre tous les outils dont vous disposez lors de la création de pages d'adhésion.
- Menu : Adminitrer>civi contribute>Nouvelle page de contribution

### L'onglet Titre  

L'onglet titre (c'est la première page que vous voyez lorsque vous créez une nouvelle page d'adhésion) vous permet de définir le titre de la page d'adhésion et de définir certaines informations de base comme le type financier, etc., qui seront enregistrées pour les adhésions qui sont réalisées par cette page.

Cet onglet vous permet également d'inclure un message d'introduction à afficher sur votre page d'adhésion. Vous pouvez inclure des images et du code HTML simple dans ce texte d'introduction.

### Cotisation au nom d'une organisation

L'onglet titre contient une case à cocher "*Permettre aux individus de contribuer et/ou d'adhérer au nom d'une organisation*" qui  permet  aux utilisateurs d'identifier une organisation comme donateur ou adhérent, ce qui est la manière recommandée d'offrir des adhésions aux organisations. La contribution ou l'adhésion sera attribuée à cette organisation. Lorsque cette case est activée, l'utilisateur est invité à sélectionner un profil (voir le chapitre des profils pour plus d'informations) utilisé pour collecter des informations sur l'organisation. Cette inscription pour une organisation peut être facultative ou obligatoire.
Une fois cette page remplie cliquer sur **Suivant**

![image](/img/Title%20settings%201%20.jpg)

### L'onglet Montant 

L'onglet des montants vous permet de définir diverses options financières, y compris le processeur de paiement qui est utilisé sur la page. Notez que vous pouvez sélectionner plus d'un processeur de paiement pour donner le choix aux personnes qui acceptent. Pour plus d'informations sur la configuration des processeurs de paiement et sur les points à considérer lors du choix d'un processeur de paiement, voir le chapitre *Processeurs de paiement*.

![image](/img/contribution%20amounts.jpg)

Notez que l'onglet des montants *n'est pas* l'endroit où les frais d'adhésion sont configurés : ils sont configurés dans l'onglet Adhésions. Si vous souhaitez utiliser cette page pour collecter des montants d'adhésion et *ne* souhaitez pas solliciter des contributions supplémentaires, laissez la case **Section des montants de contribution activée** non cochée. Si vous *désirez solliciter des contributions en plus des frais d'adhésion*, cochez la case et ajoutez des options de contribution proposées ou configurez un ensemble de prix de contribution*.

### Adhésions gratuites

Si vous offrez **Adhésions gratuites**, vous devez laisser la boîte "Exécuter des transactions monétaires en temps réel" non cochée et choisir un type d'adhésion avec un tarif minimum de valeur zéro.

### L'onglet Adhésions

Puisque nous utilisons cette page de contribution pour l'inscription et le renouvellement des adhésions, nous devons vérifier la **Section d'adhésion activée** pour utiliser cette page de contribution pour les adhésions.

Les zones de texte (Message d'introduction — Nouvelles adhésions et Message d'introduction — Renouvellements) vous permettent d'ajouter du texte qui sera affiché lorsque cette page est utilisée pour l'inscription initiale et pour les renouvellements. Lorsqu'un utilisateur enregistré avec une adhésion actuelle ou expirée affiche la page d'inscription de membre, CiviCRM remplace automatiquement la page d'inscription de membre par une page de renouvellement d'adhésion qui contient le texte de la zone de renouvellement.

![image](/img/membership%20signup%201.jpg)

Après ces zones de texte, vous trouverez quelques options que vous pouvez utiliser pour configurer les types d'adhésion disponibles sur le formulaire d'adhésion.

![image](/img/MembershipTabOnlineCintribConfiguration.PNG)

Envisagez d'abord les cas d'utilisations simples. Sélectionnez les types d'adhésion qui devraient être disponibles sur la page, ceux qui devraient être par défaut et qui peuvent être renouvelés automatiquement (vous devrez configurer vos types d'adhésion comme renouvellement automatique avec un processeur de paiement qui supporte les paiements périodiques automatiques).

Si vous activez le renouvellement automatique pour une adhésion, puis sur la page Web, les utilisateurs verront "Veuillez renouveler mon abonnement automatiquement". (*Vos frais d'adhésion initiaux seront traités une fois que vous aurez terminé l'étape de confirmation. Vous pourrez annuler les renouvellements automatiques à tout moment en vous connectant à votre compte ou en nous contactant*)". Les e-mails de réception de paiement d'adhésion incluent un lien pour que le membre annule le renouvellement automatique.

Si vous le souhaitez, vous pouvez avoir une inscription d'adhésion optionnelle. Ceci est souvent utile si vous avez une page de contribution sur laquelle vous souhaitez offrir la possibilité de devenir membre, mais que vous ne l'exigiez pas (vous devrez cocher la case "Section des montants des contributions activés" dans l'onglet Montants). Vous pouvez décider si ces paiements sont enregistrés séparément des paiements des frais d'adhésion.

Si vous ne pouvez pas réaliser ce dont vous avez besoin en utilisant les "Types d'adhésion" (par exemple, si vous souhaitez offrir un abonnement à deux adhésions en même temps ou créer des inscriptions avec plusieurs statuts d'adhésion), vous devez utiliser un ensemble de prix d'adhésion (voir le chapitre *Gestion des tarifications*).

Ce que vous pouvez faire avec la Gestion des tarifications :

-   Permettre  aux utilisateurs de s'inscrire à plusieurs types d'adhésion en même temps(par exemple, les adhésions «nationales» et «locales») 
-   Permettre aux utilisateurs de se connecter à plusieurs statuts d'adhésion en même temps
-   Offrir d'autres options telles que la souscription à des options payantes en plus de l'adhésion. 

### L'onglet Réception

Une fois que le visiteur du site a complété le formulaire d'inscription ou de renouvellement de l'adhésion, il sera redirigé vers une page de remerciement et pourra recevoir un reçu électronique généré et envoyé automatiquement. Cette quatrième étape vous permet de configurer cette option. Vous pouvez personnaliser le message qui s'ajoute au reçu d'adhésion sur cette page et l'adresse électronique d'envoi du reçu. Si vous souhaitez personnaliser davantage le modèle de courrier électronique de réception, vous pouvez le faire en utilisant l'écran **Civimail> Modèles de messages**.

Vous pouvez également choisir l'envoi "CC ou BCC" pour chaque reçu d'adhésion à un membre du personnel afin qu'ils soient alerté immédiatement chaque fois que quelqu'un devient membre.

![image](/img/membership%20page%20receipt%201.jpg)

![image](/img/membership%20page%20receipt%202.jpg)

### L'onglet Recommander à un ami

CiviCRM vous permet d'ajouter une fonction "Recommander à un ami" à la page de remerciement.  
La page permet à vos membres de partager des informations sur votre organisation avec leurs amis en leur envoyant un lien vers votre site. Les amis qui sont ainsi informés de l'inscription et l'adhésion seront également ajoutés à CiviCRM s'ils n'existent pas déjà et leur champ source montrera qu'ils ont été ajoutés via une recommandation d'un ami. 

![image](/img/tell%20a%20friend.jpg)

###Collecte d'informations dans le cadre de l'adhésion (onglet Profils)  

Vous pouvez utiliser des profils pour recueillir des informations sur les membres qui remplissent le formulaire d'inscription. Par défaut, les pages de contribution ne comprennent qu'un champ de courrier électronique. L'ajout d'un profil au formulaire de contribution ajoutera, si besoin, plusieurs champs que CiviCRM affichera dans le formulaire d'inscription de membre. Vous pouvez utiliser des profils pour recueillir des informations supplémentaires sur le contact, par exemple leur adresse, leurs intérêts, etc. Si la personne qui s'inscrit pour devenir membre est connectée, ses champs de profil seront remplis avec les données de CiviCRM, le cas échéant. N'ajoutez pas de profil d'adhésion. La collecte de cette information se produit automatiquement pendant la procédure d'inscription en ligne.

![image](/img/membership-profiles.png)

L'onglet profil vous permet de sélectionner un profil existant à inclure sur votre page d'adhésion, et si vous avez la permission, de modifier un profil existant ou de créer un nouveau profil à ajouter sur cette page.

**ATTENTION :** Si vous modifiez un profil existant ici, il sera modifié dans tous les endroits où ce profil est utilisé.

###L'onglet Primes 

Les primes sont des cadeaux et des incitations offerts aux personnes qui font un don à votre organisation. Ils sont le plus souvent associés à des niveaux de dons échelonnés (par exemple, donnez 50 € pour recevoir un T-shirt) mais peuvent également être utilisés conjointement avec vos pages d'adhésion. Avant d'inclure les primes sur une page de contribution, vous devez les configurer par le biais de **Contributions> Primes (cadeaux de remerciement)**.

L'onglet Primes de l'assistant de la page de contribution contrôle le texte d'introduction, les informations de contact et les autres détails liés aux primes.



![image](/img/membership-profiles.png)

Test des pages d'adhésion  
--------------------------------
Dès que  la configuration de votre page d'adhésion est terminé, il est conseillé de tester le processus afin de vous assurer que tout est correct. Si vous souhaitez tester pour rechercher ou supprimer des adhésions, vous pouvez le faire en cliquant sur la case à cocher «Évaluer» **Trouver des membres**. La fonctionnalité de test est disponible sur **Contributions> Gérer les Pages de Contribution**, cliquez sur **Liens** à côté de votre page d'inscription / renouvellement de membre et cliquez sur **Test-drive**. Toutes les données d'adhésion que vous envoyez via le formulaire en mode test seront ajoutées à CiviCRM en tant que données de test et ne seront pas incluses dans les statistiques ou lors de la recherche d'adhésion.

Essayez de vous mettre à la place de quelqu'un qui veut devenir membre de votre organisation et testez le processus plusieurs fois, avec différentes combinaisons de champs à chaque fois. Assurez-vous que les données apparaissent comme prévu dans CiviCRM. Une fois que vous avez testé le processus et que vous avez apporté les modifications nécessaires, faites à nouveau tester le processus par les autres membres du personnel ou des amis de votre organisation.

Lorsque vous utilisez l'option test d'enregistrement de l'adhésion par le processeur de paiement, vous voyez les mêmes pages d'inscription que les utilisateurs, mais le paiement en ligne n'est pas totalement débité de votre carte (voir *Processeurs de paiement* pour plus d'informations sur les processeurs fictifs et les détails de la carte que vous pouvez utiliser pour les transactions de test).

Il est intéressant de vérifier et tester périodiquement votre processus d'adhésion pour vous assurer qu'il est aussi harmonieux que possible. Vous recevrez des commentaires indirects de vos membres au fur et à mesure qu'ils utilisent le formulaire. S'ils n'entrent pas dans les données comme vous l'avez voulu, vous devrez apporter des modifications. De temps à autre, vous devez solliciter des commentaires directs de la part de personnes qui ont récemment adhérées pour vérifier si la procédure est facile à utiliser pour devenir membre. Vous pouvez aussi leur demander leur avis sur la façon dont vous pourriez améliorer votre formulaire.

Ajouter les pages d'inscription à votre site
-----------------------------------------------

Une fois que vous avez créé votre page de contribution, vous devez la rendre visible sur votre site. La méthode dépend du CMS. Les instructions pour chaque CMS sont ci-dessous :

Les pages d'inscription aux membres sont conçues pour hériter du thème de votre site Web. Vous pouvez inclure des images sur les zones de texte HTML de la page pour les rendre plus attrayantes. De nombreuses organisations améliorent l'apparence de leurs pages d'adhésion afin d'augmenter les taux de participation. Les méthodes de modifications et de conceptions de ces pages ne sont pas traitées dans cette documentation, mais un concepteur de site Web qui connaît votre CMS et CiviCRM pourra vous aider.

### Dans Drupal
Accédez à **Contributions**> **Gérer les Pages de Contribution**> cliquez sur **Liens** à côté de votre page d'inscription / renouvellement de membre> cliquez sur **Live Page** pour afficher la page terminée. Vous pouvez ensuite copier l'URL et l'inclure dans une page de contenu ou l'affecter à un élément de menu

### Dans Wordpress
Accédez à **Contributions**> **Gérer les Pages de Contribution**> cliquez sur **Liens** à côté de votre page d'inscription / renouvellement de membre> cliquez sur **Live Page** Copiez l'URL et insérez-la dans un lien HTML ou un menu.

*Ou* utilisez un plugin tel que Page Links pour créer une URL 'slug'.

*Ou* cliquez sur l'icône de raccourci Wordpress pour insérer un formulaire dans n'importe quelle page.

![image](/img/Wordpress-Shortcodes-small.png)

### Dans Joomla!
La façon la plus directe d'afficher votre page d'inscription/renouvellement d'adhésion sur votre site Web dans Joomla est en créant un élément de menu.

- Accédez à un menu et créez un nouvel élément CiviCRM.
- Dans la liste des options de menu, choisissez Contributions.
- Dans la section des paramètres de base, sélectionnez la page de contribution que vous souhaitez afficher dans le menu déroulant.
- Enregistrez l'élément de menu et affichez le site Web pour vérifier les fonctionnalités de la page.

Autorisations requises pour l'inscription en ligne et le renouvellement.
---------------------------------------------------------
Les rôles anonymes et authentifiés nécessitent les autorisations CMS suivantes pour pouvoir adhérer ou renouveler en ligne:

- Listes et formulaires de profil: pouvoir collecter les informations de contact de base (nom, adresse, etc.) lorsque les personnes s'inscrivent.
- Accéder à toutes les données personnalisées: accepter cette autorisation pour collecter des données personnalisées.
- Autoriser les contributions en ligne: Cette autorisation doit être accordée à moins que vos membres aient des cotisations gratuites et que vous n'ayez pas intérêt à accepter des dons lorsque les personnes s'inscrivent ou renouvelent.
