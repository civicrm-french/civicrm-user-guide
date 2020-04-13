Les renouvellements de cotisations
===========================
Ce chapitre traite des différentes façons dont vos contacts peuvent renouveler leur adhésion. Ceci inclus les renouvellements automatiques, les renouvellements en ligne et les renouvellements manuels soit individuellement, soit par la mise à jour par lots des membres via le profil. Tout d'abord, nous présenterons les moyens de faire savoir à vos membres que leur adhésion devrait être renouvelée.

Les concepts de renouvellement 
-------------------------

Il existe une distinction importante entre l'ajout d'une nouvelle adhésion et le renouvellement d'une adhésion existante. Si quelqu'un s'approche de sa date de fin d'adhésion et veut continuer à être membre, dans la plupart des cas, vous pourrez renouveler l'adhésion existante en utilisant le processus de renouvellement de CiviMember plutôt que de créer une nouvelle adhésion.

Les membres ont trois dates principales. **Membre depuis** qui n'est pas modifié quand une adhésion est renouvelée. **Date de début** et **Date de fin** qui peut changer en fonction du statut d'adhésion en vigueur lorsque le renouvellement est traité.

- Si le renouvellement est traité lorsque le statut de membre a **Oui** dans la colonne **membre** sur **Administrateur> CiviMember> Règles de statut d'adhésion** alors la **Date de début** ne change pas et la date de fin est prolongée par la durée du renouvellement.
- Si le renouvellement est traité lorsque le statut de membre a **Non** dans la colonne **membre** sur **Administrateur> CiviMember> Règles de statut d'adhésion**, alors la **Date de début** est modifiée à la date actuelle et **la date de fin** est calculée à partir de la nouvelle date de début.

Le cas échéant, pour le type d'adhésion, une contribution (financière) est enregistrée dans le cadre du processus de renouvellement. Cela créera un enregistrement de contribution lié au dossier d'adhésion. Au fil du temps, et après quelques renouvellements, le dossier d'adhésion sera un enregistrement d'adhésions uniques dont la date de fin est prolongée, avec plusieurs transactions financières connexes représentant chaque cotisation de renouvellement.

### Choix d'une Adhésion

L'adhésion en ligne permet aux contacts de modifier le type d'adhésion dans le cadre du processus de renouvellement. Si un contact lié à une organisation renouvelle avec un autre type d'adhésion appartenant à la même organisation, l'adhésion existante sera changée par cet autre type d'adhésion ainsi que l'historique d'adhésion associé. La date de participation et les contributions seront conservées. La date de fin existante sera prolongée par la durée du nouveau type d'adhésion. Si ce n'est pas ce que vous voulez, vous devrez lier vos types d'adhésion à différentes organisations. (cela peut être une organisation fictive créée uniquement à cette fin et invisible à l'utilisateur. Voir le chapitre **Définition des membres** pour une explication plus détaillée.)

Si vous utilisez CiviCRM pour gérer des adhésions de plusieurs organisations, notez que le type d'adhésion d'un contact ne peut pas être modifié par un type d'adhésion provenant d'une autre organisation

Rappels de renouvellement 
-----------------

Faire savoir à un membre que son adhésion est sur le point d'arriver à échéance est la première étape dans le processus de renouvellement. CiviCRM facilite les communications avec vos membres par courrier électronique ou par courrier postal.

### Rappel par courriel 

Un ou plusieurs courriels de rappel de renouvellement peuvent être envoyés automatiquement à l'aide de la fonction "Rappels programmés" (**Administration> Communications> Schedule Reminders**). Ceci est particulièrement utile quand les types d'adhésion peuvent se terminer à tout moment au cours de l'année. Reportez-vous au chapitre [Rappels de renouvellements](http://booki.flossmanuals.net/email/scheduled-reminders) dans la section *Email* de ce livre pour les étapes impliquées dans l'envoi d'un rappel planifié une fois que vous avez composé votre message .

Le texte de vos e-mails de rappel dépendra du type d'adhésion en relation avec la date de fin d'adhésion. Par exemple, les rappels de renouvellement envoyés trois mois à l'avance aux personnes qui se sont inscrites au nom des organisations (pour leur donner suffisamment de temps pour préparer un bon de commande et le paiement par leur département comptable) doivent être différents de ceux envoyés une semaine après à un contact individuel.

Toutefois, si les membres peuvent renouveler en ligne, tous les rappels par courrier électronique de renouvellement doivent contenir dans le message un lien «spécial» Civimail : {contact.checksum}, (dans ce cas-ci vers la page de renouvellement de l'adhésion). Lorsqu'une personne clique sur ce lien spécial, elle  remplira le formulaire de renouvellement avec toutes les données qui existent dans son dossier. Ce lien spécial a une durée de sept jours à compter du moment où il a été envoyé (bien que cela puisse être changé dans : **Administer> Paramètres du système> Divers (Undelete, PDF, Limits, Logging, Captcha, etc.)** Comme les pages d'adhésion sont un Type de page de contribution, le lien {contact.checksum} à utiliser dans les e-mails de renouvellement où **N** est l'identifiant de votre page de renouvellemen est :

-   Drupal:
    http://www.myorganization.org/civicrm/contribute/transact?reset=1&id=N&{contact.checksum}&cid={contact.contact_id}  
-   Joomla!:
    http://www.myorganization.org/index.php?option=com_civicrm&task=civicrm/contribute/transact&reset=1&id=N&{contact.checksum}&cid={contact.contact_id}
-   WordPress:
    http://www.myorganization.org/?page=CiviCRM&q=civicrm/contribute/transact&reset=1&id=N&{contact.checksum}&cid={contact.contact_id}
    
Comme pour tous les e-mails que vous envoyez, vous devez prévoir le temps de tester les modèles de rappels de renouvellement, surtout si vous avez des structures d'adhésions complexes et souhaitez personnaliser les messages en fonction des types de membres ou d'autres paramètres.

Rappelez-vous que, par défaut, des rappels planifiés seront envoyés à des personnes qui l'ont choisi ou pour recevoir tous les emails, sauf si vous excluez spécifiquement ces personnes. 
Si les contacts peuvent choisir de renouveler automatiquement leur adhésion, vous devez exclure les membres qui ont choisi cette option à partir des rappels planifiés.

### Rappels postaux 

Vous pouvez également envoyer des lettres à tous les membres qui doivent renouveler ou simplement envoyer des lettres à ceux qui ne possèdent pas d'adresse électronique et à ceux qui ont opté pour un envoi de tous les courriels. 
Reportez-vous à *Communications par courrier postal* dans la section *Flux de travail communs* pour trouver le moyen de générer ces lettres.

Renouvellement automatique des adhésions
---------------------------------

Pour les membres qui ont choisi cette option lorsqu'ils ont adhérés pour la première fois, le paiement sera prélevé automatiquement à partir de leur carte de crédit préautorisée à leur date de renouvellement. 
Leur date de fin d'adhésion sera mise à jour et ils recevront les remerciements et les reçus appropriés de CiviCRM. (Voir le chapitre *Définition d'adhésions* , *Adhésions en ligne* et *Entrée manuelle des adhésions*  pour les détails de la mise en place des adhésions renouvelables automatiquement.)

Renouvellements en ligne
---------------
CiviCRM utilise la même page pour les nouvelles adhésions et les renouvellements. La seule différence est que le titre de la page et le message d'introduction sont le texte que vous avez entré dans les champs de renouvellement, dans l'onglet adhésions, lors de la configuration de votre page d'adhésion en ligne. La page de renouvellement s'affiche automatiquement à la même URL que la page de jointure de membre lorsqu'elle est vue par un visiteur du site qui possède une adhésion en cours valide ou expirée.

Lorsque vous configurez des pages d'adhésion, il convient de rappeler que les membres actuels ne verront que la page de renouvellement s'ils sont connectés. S'ils ne sont pas connectées, ils verront la page d'inscription. S'ils remplissent cette page et, en fonction de leurs informations de contact, CiviCRM peut trouver leur dossier de contact existant, puis leur adhésion sera renouvelée. Si CiviCRM ne peut pas trouver son enregistrement de contact existant (peut-être dû à un changement de leur adresse de courriel), un nouvel enregistrement de contact et une nouvelle adhésion seront créés. Il s'agit d'une source de doublons dans votre base de données et vous devez minimiser les chances que cela se produise. Deux façons de le faire sont d'inclure toujours un jeton de somme de contrôle dans les courriels de rappel de renouvellement et d'ajouter du texte au message d'introduction du nouveau membre pour rappeler aux personnes qu'ils doivent se connecter avant de renouveler.

###  Page par défaut de Renouvellement d'adhésion en ligne 

Lorsqu'une adhésion est souscrite à l'aide de la page d'inscription de l'adhésion en ligne (service en libre-service), le tableau de contact de cet utilisateur contiendra un lien "renouvelable" qui pointe vers cette page. Cependant, ce lien n'apparaîtra pas pour les membres dont l'adhésion initiale a été saisie manuellement, sauf si vous configurez une **page de renouvellement d'adhésion en ligne par défaut** comme suit:

1. Si cela n'existe pas, créez une page d'adhésion qui inclut toutes les adhésions actuellement disponibles. (Vous devrez peut-être utiliser un prix établi pour cela si les frais d'adhésion doivent être attribués à plus que sur le type financier. Reportez-vous à *Gestion des tarifications* pour plus de détails.)
2. Accédez à **Administrer> CiviMember> Paramètres du composant CiviMember**
3. Pour la page par défault de Renouvellement d'adhésion en ligne, choisissez la page d'adhésion contenant tous vos types d'adhésion.

Un lien "renouvelable" qui pointe vers cette page sera alors affiché dans le tableau de bord de contact pour toute adhésion qui a été introduite manuellement.

![image](/img/z_sprint14_renewalpage.png)

Renouvellement manuel d'une adhésion pour un seul contact
---------------------------------------------------

1. Accédez à la page récapitulative du contact.
2. Cliquez sur l'onglet **Adhésions**
3. Cliquez sur **PLUS** à côté du dossier d'adhésion
4. Sélectionnez **Renouveler** pour entrer: espèces, chèque ou EFT ou **Renew-Credit Card** pour traiter le renouvellement par votre processeur de paiement en ligne.

![image](/img/z_sprint14_renewmembership_1.png)

Mise à jour par lot des adhésions via le profil
----------------------------------
Vous pouvez utiliser la fonction **Batch Update Membres via Profile** pour mettre à jour plusieurs enregistrements d'adhésion existants (ne pas confondre cela avec la fonction **Batch Data Entry** qui est utilisée pour ajouter les *nouvelles adhésions* et les paiements des membres ).

Pour utiliser la mise à jour des adhésions par lots via le profil, vous pouvez utiliser les profils réservés par défaut de CiviCRM, **Entrée des données par lot** du menu adhésion ou du menu Contribution. 
Vous pouvez aussi créer et configurer un profil contenant des champs relatifs à l'information d'adhésion que vous souhaitez afficher et mettre à jour. Vous pouvez en savoir plus sur la façon de configurer les profils dans le chapitre *Profils* de la section *Organiser vos données*.

Pour utiliser la fonction **Mise à jour par lot des adhésions via un profil**:

1. Vous trouvez les adhésions que vous souhaitez mettre à jour en sélectionnant **Adhésions** > **Rechercher des adhésions** Entrez vos critères de recherche et cliquez sur **Rechercher**.
2. Dans l'écran de résultats, sélectionnez les enregistrements d'adhésions voulus et sélectionnez **Mise à jour des lots via le profil** dans la case à cocher **- actions -** et cliquez sur **Aller**.
3. Dans l'écran d'entrée de données par lot, onglet **Select Profile**, sélectionnez le profil que vous souhaitez utiliser dans la liste déroulante et cliquez sur **Continuer**. Vous pouvez en savoir plus sur la configuration d'un profil d'adhésion pour la mise à jour par lot dans le chapitre *Profils* de la section *Organiser vos données*.
4. Dans l'écran Entrée des données du lot, vous pouvez mettre à jour les informations affichées en fonction du profil que vous avez sélectionné. Vous pouvez utiliser l'icône "auto-copie" en haut d'une colonne pour copier et coller la valeur du champ du premier enregistrement de cette colonne au reste des champs ci-dessous dans la colonne. Une fois que vous avez terminé la mise à jour, cliquez sur ** Mettre à jour les membres **.

      Vous trouverez ci-dessous un exemple d'une page "Entrée des données du lot" qui utilise un profil d'adhésion configuré pour afficher les champs **Type d'adhésion** et **Date de départ de l'adhésion** 

![image](/img/Memberships-Everydaytasks-batchupdateviaprofile-batchupdateformembers.jpg)

