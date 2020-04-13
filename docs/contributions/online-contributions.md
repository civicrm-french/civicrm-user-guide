Création de pages de contribution
-----------------------------

Cette section décrit la mise en place de pages de contribution en ligne dans lesquelles les visiteurs de votre site Web peuvent contribuer à votre organisation.
CiviContribute est très flexible, adaptable et inclut de nombreux champs et fonctionnalités optionnelles tels que des contributions récurrentes, des promesses de dons et des pages de campagne personnelle. Cela peut rendre la mise en place de pages de contribution comme une tâche lourde, mais pas insurmontable comme le montrent les deux premières procédures ci dessous.


## La page de contribution la plus simple (réçu envoyé uniquement par le processeur de paiement.)

1. Assurez-vous d'avoir un [processeur de paiement configuré](../contributions/payment-processors).
2. Allez à **Contributions> Nouvelle page de contribution**.
3. Entrez le **titre** de la page pour votre site Web.
4. Sélectionnez le **type financier** approprié.
5. Cliquez sur **Continuer**.
6. Sur la page suivante, laissez tout tel quel, sauf en cochant la case **Autoriser d'autres montants** et en réglant les montants **minimum * et / ou **maximum** si vous le souhaitez.
7. Cliquez sur **Enregistrer et Terminer**.
8. Suivez les étapes de votre CMS pour [afficher cette page sur votre site web](#publicizing-your-contribution-page).  


## Une page de contribution très simple incluant l'accusé de réception 

1. Assurez-vous d'avoir un [processeur de paiement configuré](../contributions/payment-processors).
2. Allez à **Contributions> Nouvelle page de contribution**.
3. Entrez le **titre** de la page pour votre site Web.
4. Sélectionnez le **type financier** approprié.
5. Cliquez sur **Continuer**.
6. Sur la page suivante, laissez tout tel quel, sauf en cochant la case **Autoriser d'autres montants** et en réglant les montants **minimum * et / ou **maximum** si vous le souhaitez.
7. Cliquez sur **Enregistrer**.
8. Sélectionnez l'onglet **Reçu**.
9. Entrez le **titre** pour votre page de remerciement.
10. Cochez **Reçu de courrier électronique au contributeur**.
11. Entrez l'adresse email "DE" dans **Reçu From Email**.
12. Cliquez sur **Enregistrer et Terminer**.

Suivez les étapes de votre CMS pour [afficher cette page sur votre site](#publicizing-your-contribution-page).


## Mise en place d'une page de contribution - détails complets.

Accédez à **Contribution> Nouvelle page de contribution**. (**Contribution> Gérer les pages de contribution> Ajouter une page de contribution**) vous amène à cet écran :

![New Contribution Page](/img/civicontribute-new-contribution-page.png)

- Le titre de la page et le type financier sont les seuls champs obligatoires. CiviCRM est livré avec quatre types financiers standards, mais vous pouvez en [créer plus](../contributions/concepts-clés-et-configurations) pour répondre aux besoins comptables de votre organisation :
- Lier cette page de contribution à une [campagne](../campaign/what-is-civicampaign). (Optionnel)
- Composez votre message d'introduction. (optionnel)
- Composez votre message de pied de page. (optionnel)
- Définir un montant d'objectif. (optionnel)
- Cette page de contribution doit être activée ou désactivée manuellement, mais vous pouvez définir une **date de début** et une **date de fin** qui s'appliqueront pour un widget de contribution et [Pages de campagne personnelles](../contributions/personnel-campaign-pages). (optionnel)
- Choisissez si vous acceptez ou non : [Créditer un bénéficiaire](../contributions/soft-credits)
- Choisissez d'utiliser une page de confirmation où les utilisateurs peuvent vérifier que tous les détails sont corrects ou de traiter le paiement dès que le formulaire de contribution est soumis.
- Choisissez d'afficher ou non les liens de médias sociaux sur les pages en ligne et dans le reçu automatiquement envoyé par courriel (s'il est envoyé).
- Décidez si la page de contribution doit être active ou non.
- Cliquez sur **Continuer**. (C'est à ce moment que votre nouvelle page de contribution est enregistrée pour la première fois.) Vous pourrez revenir en arrière et modifier tous les aspects de cette page à tout moment en cliquant sur l'onglet **Titre** et Paramètres.

Vous allez ensuite à l'onglet (Contributions) **Montants**. Toutes les autres fonctionnalités sont alors visibles dans les onglets en haut de page. Nous les explorons une à une ci-dessous.


### Onglet Montants 

![Contributions Amounts Page](/img/civicontribute-online-contribution-amounts.png)

- La case **Exécuter les transactions monétaires en temps réel** est cochée par défaut.
Vous devez décochez cette case si vous utilisez cette page de contribution pour une inscription gratuite ou pour solliciter des dons en nature (non monétaires) ou si vous voulez que tous les utilisateurs ** soumettent leurs paiements hors ligne.
- Sélectionnez la **Devise** monétaire.
- Sélectionnez un ou plusieurs [Processeurs de paiement](../contributions/processeurs de paiement) préalablement configurés pour cette page. Certaines organisations trouvent que c'est une bonne idée d'offrir un choix de processeurs. Vous pouvez le faire en configurant plusieurs processeurs et en cochant les cases correspondantes sur ce formulaire.
- Cochez la case **Payer plus tard** si vous souhaitez donner aux utilisateurs la possibilité de réaliser un paiement hors ligne (par exemple, envoyer un chèque par la poste, payer par virement ou carte de crédit, etc.). Si vous autorisez le paiement des contributions à venir, vous devrez choisir une étiquette à cocher, à afficher à vos utilisateurs, et les instructions pour soumettre ces paiements différés.
- Si vous désélectionnez la Section **Montants des contributions**, les champs restants de cette page disparaîtront. Vous ne pourrez accepter que des frais d'adhésion à montant fixe ou, si vous configurez un ensemble de prix d'adhésion, des frais d'adhésion à montant fixe et d'autres contributions comme spécifié dans le tarif fixé lors d'une transaction **unique**.
- Sélectionnez un **Tarif** prédéfini (pour les options de paiement plus complexes) OU entrez jusqu'à 10 montants de cotisations fixes dans le tableau au bas de la page.
- Vous pouvez sélectionner **Contributions récurrentes** si votre processeur de paiement et son intégration avec CiviCRM prennent en charge la facturation récurrente et que vous souhaitiez autoriser cette fonctionnalité. (Il existe des restrictions sur les paiements récurrents lorsque [les frais d'adhésion](../adhésion/définition-adhésions) sont payés.) Si vous cochez **Contributions récurrentes** d'autres paramètres deviennent visibles.
- Cochez la case **Promesses de dons** pour donner aux utilisateurs la possibilité de [promettre des paiements futurs](../pledges/what-is-civipledge).
- Décidez de l'étiquette de la zone "Montant de la contribution" sur votre page.
- Cochez **Autoriser d'autres montants** pour donner aux utilisateurs la possibilité de payer le montant qu'ils choisissent. Vous pouvez définir un montant minimum et maximum pour les contributions «Autres montants» si vous le souhaitez.
- Cliquez sur **Enregistrer et Terminer**.

### Onglet Adhésions 

Cet onglet est traité en détail dans [Adhésions](../memberships/online-membership-sign-up).

### Onglet Profil

Si vous souhaitez recueillir des informations auprès des contributeurs au-delà des champs standards requis pour apporter une contribution, tels que l'âge, les intérêts et les compétences, vous pouvez inclure les Profils CiviCRM existants au début ou à la fin d'une page de contribution. Vous pouvez également créer de nouveaux profils.

Les profils utilisés dans une page de contribution ne peuvent contenir que des champs appartenant aux:
- dossiers de contact
- dossiers de contribution

Les profils qui incluent des champs associés à d'autres types d'enregistrements ne sont pas disponibles.

Les pages de contribution incluent toujours un champ d'adresse e-mail obligatoire, quelque soit les autres champs inclus dans vos profils.

1. Accédez à **Gérer les pages de contribution** puis, pour la page que vous souhaitez configurer, cliquez sur **Configurer> Inclure les profils**.
2. Sélectionnez un profil CiviCRM dans le menu déroulant, à inclure en haut et / ou en bas de la page de contribution. Vous pouvez ensuite prévisualiser vos sélections, modifier un profil existant, copier un profil existant ou créer un nouveau profil.

Lorsque vous modifiez ou créez un nouveau profil, vous pouvez utiliser l'interface glisser-déposer du profil représentée ici.

![image](/img/Contribution-page-edit-profile2.gif)
    
!!! AVERTISSEMENT: Si vous modifiez un profil existant lors de la configuration de votre page Contribution, les modifications que vous apportez s'appliqueront partout où ce profil est utilisé. Ainsi, sauf si un profil existant **correspond exactement à vos besoins, copiez le profil, puis renommez et modifiez la copie selon les besoins.    

3. Cliquez sur **Enregistrer** ou **Enregistrer et Terminer** ou **Enregistrer et Suivant**.

Pour plus d'informations, lisez [Profils](../organising-your-data/profiles).

Enregistrement automatique des contributions
--------------------------------

Peu importe la façon dont les donateurs accèdent à votre page de contribution, CiviCRM enregistre automatiquement leurs dons, libérant ainsi votre personnel de la saisie manuelle des données. Si les donateurs existent déjà dans la base de données, CiviCRM ajoute la contribution à leur dossier. S'ils n'existent pas, CiviCRM crée un nouvel enregistrement pour eux.

Dans les cas où les utilisateurs ont plusieurs adresses e-mail ou si plus d'une personne partage une adresse e-mail, il est possible que les contributions soient créditées au mauvais contact. Pour limiter ce risque, vous pouvez ajuster les règles de correspondance des doublons par défaut de CiviCRM. Pour obtenir les instructions sur la façon de procéder, lisez [Dedoublonner et fusionner](../common-workflows/deduping-and-merging).


### Onglet Reçu et remerciement

Dès que votre page de contribution est créée, vous pouvez personnaliser les e-mails de remerciement et de reçu envoyés aux contributeurs.

1. Accédez à **Administrer> CiviContribute> Gérer les pages de contribution**.
2. Utilisez le lien **Configurer** sur le côté droit d'une page de contribution pour accéder à la page et la modifier.
3. Cliquez sur **Remerciements et reçus**. Entrez les informations que vous souhaitez voir apparaître dans le courriel de remerciement. Les donneurs s'attendent généralement à recevoir un reçu dès que leur transaction est terminée. Il est donc recommandé d'activer le reçu de courrier électronique automatique.
4. Cliquez sur **Enregistrer et Terminer**.


## Publier votre page de contribution

Maintenant que vous avez créé votre page de contribution, il est temps d'amener les gens sur la page afin qu'ils puissent contribuer. Vous voudrez probablement afficher un lien vers la page d'accueil de votre site Web via un bouton de don ou un élément de menu. Voici quelques conseils supplémentaires pour promouvoir une page de contribution dans différentes configurations de CiviCRM:


### Élément de menu dans Joomla!

La façon la plus directe d'afficher votre page de contribution ou votre page d'inscription / de renouvellement d'adhésion sur le devant de votre site Web consiste à créer un élément de menu.

1. Accédez à un menu et créez un nouvel élément CiviCRM.
2. Dans la liste des options de menu, choisissez Contributions.
3. Dans la section Paramètres de base, sélectionnez la page de contribution que vous souhaitez afficher dans le menu déroulant.
4. Enregistrez l'élément de menu et vérifier votre site Web pour confirmer la fonctionnalité de la page.


### Option de menu dans Drupal

Dans la liste des pages de contribution, sélectionnez Page en direct pour afficher la page terminée. Vous pouvez ensuite copier l'URL et l'inclure dans une page de contenu ou l'affecter à un élément de menu.


### Page ou Post dans WordPress

Vous pouvez facilement intégrer votre page de contribution dans un article ou une page sur votre site Web WordPress.

1. Connectez-vous au tableau de bord d'administration de votre site WordPress.
2. Cliquez sur **Pages** ou **Publications> Ajouter nouveau**.
3. Cliquez sur l'icône CiviCRM à côté de Upload / Insert
4. Sélectionnez Page de contribution en tant qu'élément Frontend
5. Sélectionnez la page de contribution souhaitée
6. Sauvegardez la page ou la publication. Votre page de contribution sera automatiquement intégrée au thème de votre site sur cette page.


### URLs "simplifiées"

Les pages de contribution ont des URL un peu "compliquées" - en d'autres termes, elles sont difficiles à retenir. Un exemple est *: *www.myorganization.org/civicrm/contribute/transact?reset=1&id=1*

D'un autre côté, les URL "plus simples" sont beaucoup plus faciles à retenir et à utiliser, par exemple:
*www.myorganization.org/donate*

Ce genre d'URL est simplement une redirection d'URL (amenant automatiquement les gens d'une page de votre site web à une autre). Drupal fournit un module utile appelé Redirection de chemin ([http://drupal.org/project/path_redirect](http://drupal.org/project/path_redirect)) qui vous permet de créer des redirections d'URL à partir de l'interface utilisateur sans configuration compliquée du serveur Web. 
Pour Joomla!, les utilisateurs ont également une solution de rechange si les URL "conviviales" pour les moteurs de recherche sont activées dans les paramètres globaux. Vous pouvez ensuite créer un lien de menu vers la page de contribution et définir une URL "simplifiée" en utilisant le champ alias.


### Email personnalisé

L'envoi par e-mail aux contacts enregistrés est un autre moyen essentiel de diffuser vos campagnes de dons, vos évènements,.... Le composant CiviMail de CiviCRM vous permet d'envoyer des e-mails ciblés à n'importe quel groupe de contacts de votre base de données. Dans un message CiviMail, vous pouvez inclure des liens vers le formulaire de contribution et utiliser la fonction de statistiques de CiviMail pour voir combien de personnes ont cliqué sur ce lien.

Une façon éprouvée d'augmenter les contributions ou les dons est d'envoyer à chaque contact ciblé un courriel personnalisé avec un lien vers le formulaire de contribution dans lequel toutes les coordonnées seront déjà remplies. Cela leur évite d'avoir à le remplir et augmente les chances qu'ils fassent un don. Vous pouvez utiliser cette fonctionnalité en créant un lien spécial dans le corps de votre message CiviMail qui inclut une *valeur de contrôle*. Une valeur de contrôle (checksum) est un nombre unique et pseudo-aléatoire attribué à chaque destinataire de l'envoi qui pointe vers ses informations de contact, stockées de manière sécurisée dans votre base de données.

Si les utilisateurs cliquent sur le lien spécial, CiviCRM les recherche dans la base de données et remplit à l'avance les champs du formulaire de contribution (champs principaux ou champs affichés via un profil) avec toutes informations nécessaires de leur fiche de contact. Pour en savoir plus sur la façon de procéder et sur le chemin du lien, visitez:
[http://wiki.civicrm.org/confluence/display/CRMDOC/Tokens](http://wiki.civicrm.org/confluence/display/CRMDOC/Tokens)
