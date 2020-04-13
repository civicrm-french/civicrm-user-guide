Pages personnelles de campagne
==============================

Les fonctionnalités standards de CiviCRM  permettent à vos utilisateurs de créer leurs propres pages de collecte de fonds et ensuite de solliciter le public pour financer leur cause. Ces pages sont appelées pages de campagne personnelles ou «PCP».

Une page de campagne personnelle permet à vos membres de personnaliser une action de collecte de fonds, un événement, une manifestation etc., en développant leurs raisons personnelles et / ou leurs expériences d'un évènement sur leur propre page personnelle. En outre, vos contributeurs peuvent à leur tour envoyer les pages de leur campagne personnelle à leur cercle d'amis. Vous pouvez activer la fonctionnalité "En parler à un ami" pour aider quelqu'un à partager encore plus sa page de Campagne.

Des exemples de cette fonctionnalité peuvent être : "Parrainez ma marche de 100 km", "Aidez-nous à financer notre voyage scolaire" ou «Levons des fonds pour construire une école...».

Fonctions de l'administrateur
----------------------

Les administrateurs qui gérent les pages de collecte de fonds peuvent utiliser les fonctionnalités suivantes via la configuration de la page de contribution:

- Exiger l'approbation avant qu'une page de collecte de fonds nouvellement créée devienne active.
- Activer ou non "Transférer à un ami" afin que les collecteurs de fonds puissent envoyer un courriel à d'autres personnes. 
- Définir une adresse e-mail pour informer l'administrateur lorsqu'une nouvelle page est créée.
- Permettre aux propriétaires de PCP de, toujours, parfois ou jamais, recevoir une notification lorsqu'un don est fait via leur page.
- Choisir un profil de champs d'informations à recueillir auprès des partisans du PCP.
- Personnaliser le texte dans le bouton Créer.

Une fois que les pages PCP sont actives, les administrateurs peuvent:

- Désactiver ou refuser des pages de contribution personnelle
- Modifier le contenu PCP
- Voir le montant collecté par chaque PCP
- Exécuter des rapports (en utilisant CiviReport) montrant un résumé de la collecte de fonds PCP
- Saisir les contributions "hors ligne" (chèques, espèces) et créditer l'argent à un PCP

Caractéristiques de la collecte de fonds 
---------------------

Pour personnaliser une PCP les utilisateurs peuvent paramétrer:

- Un titre de leur choix
- Un texte descriptif
- Sélectionner un objectif financier à atteindre
- Télécharger une image qui apparaitra sur leur page
- Choisir si un «tableau d'honneur» des noms des participants s'affichera sur leur page
- Possibilité d'afficher un «thermomètre» montrant les évolutions vers leur objectif
- Créer un nom d'utilisateur (ou se connecter en utilisant un nom d'utilisateur déjà enregistré) afin qu'ils puissent éditer leur PCP ultérieurement

Limitations
-----------

- La fonctionnalité PCP de CiviCRM ne permet pas la gestion d'équipe. Par exemple, le responsable de la collecte de fonds qui recrute des membres dans une équipe ne peut gérer les membres de son équipe ni le palmarès des meilleurs membres ayant le plus collecté. Ces fonctionnalités ne sont pas soutenues par CiviCRM actuellement.

- Il y a une limite d'une seule image téléchargée à un PCP pour la collecte de fonds. L'image n'est pas automatiquement redimensionnée.

- L'apparence du thermomètre et du tableau d'honneur peut être modifiée, mais les modifications sont appliquées à toutes les pages. Ces personnalisations ne peuvent pas être faites sans l'expertise d'un développeur.

- Les e-mails automatisés (messages système) envoyés à l'administrateur PCP et au propriétaire de la page, à différentes étapes d'une campagne, peuvent être modifiés. Une connaissance pratique de Smarty 2 ([http://www.smarty.net/](http://www.smarty.net/)) est requise. 
La notification par défaut pour le propriétaire du PCP lorsqu'un don est reçu est:

![image](/img/PCP%20owner%20notificationV2.PNG)

**Création**

Toutes les pages de campagne personnelle *doivent* être liées à une page ou un événement de contribution en ligne créé dans CiviCRM en accédant à: **Contributions> Nouvelle page de contribution** ou **Événements> Nouvel événement**. Dès qu'une page de contribution ou un événement a été généré, pour la modification des paramètres, accédez à l'onglet **Campagnes personnelles** et cliquez sur "Activer les pages de campagne personnelles". Un certain nombre d'autres options peuvent ensuite être configurées, notamment:

- **Approbation requise**: cochez cette option pour modérer toutes les demandes de création PCP. Un administrateur doit approuver la page avant qu'elle ne devienne active, après quoi l'utilisateur sera averti par e-mail et pourra la promouvoir. (assurez-vous que "notifier e-mail" est également utilisé pour informer un administrateur lorsque des pages PCP sont en attente de révision).
- **Notification Email**: Chaque fois qu'un nouveau PCP est créé, un email sera envoyé aux administrateurs nommés (séparer plusieurs adresses e-mail par des virgules).
- **Profil Supporter**: sélectionnez un profil de champs à collecter auprès de l'utilisateur qui crée le PCP.
- **Notification par email du propriétaire:** un email peut être envoyé automatiquement au propriétaire du PCP à chaque fois qu'un don est fait sur sa page. Vous pouvez choisir si les e-mails seront toujours ou jamais envoyés automatiquement pour toutes les pages PCP créées sous cet événement particulier ou cette page de contribution. Vous pouvez également autoriser le propriétaire du PCP à choisir lors du processus de configuration de la page s'il souhaite ou non recevoir une notification des dons effectués via sa page.
- **Autoriser la fonctionnalité "informer un ami"**: le propriétaire du PCP peut envoyer des courriels à ses contacts, les encourageant à visiter sa page et y contribuer.
- **Type de campagne**: lorsque vous activez des PCP pour un événement, vous pouvez donner au participant à l'événement la possibilité de créer son propre événement de collecte de fonds ou de page de contribution (par exemple, pour recueillir des fonds).

Une fois la création d'une PCP activée, il existe deux façons de créer un PCP:

- Une personne faisant un don sur une page de contribution ou s'inscrivant à un événement a la possibilité de créer son propre PCP via un bouton sur la page «merci».
- Si une personne oublie de cliquer sur le lien lors d'un don, ou si vous souhaitez donner à tous les visiteurs l'opportunité de créer un PCP sans avoir à faire un don ou s'enregistrer, vous pouvez donner un lien direct à vos participants. Ce lien pourra être envoyé par courrier électronique, incorporé dans une page ou ajouté en tant qu'élément de menu. 

!!! Notez :
**Le bouton d'invitation:**

![image](/img/pcp-contribute-thank-you.png)

**Le lien invitation:**

http://*YOUR-SITE.ORG*/civicrm/contribute/campaign?action=add&reset=1&pageId=*CONTRIBUTION_OR_EVENT_ID*&component=*EVENT_OR_CONTRIBUTE*

Pour utiliser ce lien, remplacez les éléments suivants:

-   \*YOUR-SITE.ORG*: entrez l'adresse de votre domaine
-   \*CONTRIBUTION_OR_EVENT_ID*: donnez le numéro d'identification de l'événement ou de la page de contribution. Ceci peut être obtenu en naviguant sur «Gérer les événements» ou «Gérer les pages de contribution» et en recherchant l'ID de l'élément choisi.
-   \*EVENT_OR_CONTRIBUTE\*: Si l'invitation concerne une page de campagne personnelle à l'appui d'une page de contribution, utilisez *component=contribute*. Si l'invitation prend en charge un événement, utilisez *component=event*.

Gestion les pages de campagne personnelles
---------------------------------

Lorsqu'une personne clique sur le bouton «Créer sa propre page de collecte de fonds» ou un lien direct, elle recevra un formulaire pour remplir ses informations, notamment: un titre, un message, le montant de l'objectif et le texte du bouton. Elle peut également joindre une photo, activer une barre de progression (thermomètre), inclure un rôle d'honneur de leurs donateurs qui n'ont pas choisi d'être anonymes, et si la campagne est active (ils peuvent choisir de l'activer plus tard).

Si la modération PCP a été activée (option «approbation requise»), un administrateur doit se connecter au backend CiviCRM et activer la page **Contributions> Pages de campagne personnelles** avant que la personne puisse l'utiliser. Recherchez le PCP dans la liste, regardez à la fin de la ligne et cliquez sur «Approuver», «Rejeter» ou «Supprimer» (si une date ultérieure est mentionnée vous pouvez aussi activer/désactiver le PCP en cliquant sur le lien «Plus») . La personne recevra un courriel de confirmation et pourra continuer à l'utiliser. Assurez-vous que les administrateurs sont toujours alertés de cette étape en saisissant une adresse e-mail de notification dans les paramètres de la page de contribution (voir "Configuration" ci-dessus).

Après l'approbation, le propriétaire du PCP recevra un courriel décrivant comment il peut commencer à promouvoir sa page et à la modifier, pourvu que l'accès lui soit accordé. L'utilisateur et l'administrateur peuvent modifier les paramètres PCP à tout moment via l'élément de menu: **Contributions> Pages de campagne personnelles**> cliquez sur **Modifier**, **Supprimer** ou **Désactiver/Activer**.

