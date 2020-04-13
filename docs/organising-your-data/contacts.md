Contacts
========

Les contacts sont au coeur de CiviCRM. Toutes les autres interactions gravitent autour d'eux. Ce chapitre explique comment rechercher, consulter, ajouter, modifier et supprimer des contacts. Nous regarderons aussi comment créer de nouveaux types de contacts et comment les personnaliser.

Il y a trois types de contact dans la configuration par défaut :

-   **Individus / Particuliers** - toute personne sur qui vous voulez faire un suivi.
-   **Organisations** - ceci pourrait être un organisme communautaire, une entreprise, un chapitre de votre organisation ou un comité.
-   **Ménages / Foyers** - une famille ou un groupe de personnes résidant à la même adresse physique.

Chaque fiche de contact contient des informations de base à leur sujet, telles que :

- nom, surnom, salutation, titre (formalité)
- site web, adresses courriel, numéros de téléphone
- adresses postales
- mode de communication préféré (incluant ceux qui ne veulent pas être contactés).

Vous pouvez également définir des sous-types de contact, tels que « étudiants », « fermes » ou « cuisines collectives ». Chaque type de contact que vous créez est basé sur un des trois aux types de base. Par exemple, les fiches d'étudiants seraient basés sur le modèle des individus, les fermes seraient basées sur les organisations ou peut-être même sur les ménages, selon vos besoins. 

Un rapide coup d'oeil sur les contacts
--------------------------------------

Les contacts sont organisés en onglets. Le premier onglet qui s'affiche lorsque vous visualisez un contact est l'onglet **résumé**, qui contient quelques informations de base. Puis viennent les autres onglets, affichant chacun des informations correspondant à différents aspects de votre contact. Cette organisation en onglet vous permet de gérer facilement un nombre important de données qu'il est possible de collecter sur votre contact au fil du temps. 

Les onglets qui s'affichent (ou non) dépendent des composants qui sont activés et des autorisations que vous possédez. Par exemple, vous ne verrez que l'onglet Adhésions si le composant CiviMember est actif et que vous avez l'autorisation de visualisation les adhésions. Vous pouvez également définir des onglets supplémentaires capables d'afficher des champs de données personnalisés.

Nous allons voir ci-dessous les parties les plus importantes de votre écran contact.

### Actions sur les contacts 

Juste au dessus des onglets quelques boutons sont disposés. Le premier d'entre eux est le bouton **Actions** qui contient des raccourcis pratiques sur les actions les plus communes à faire avec un contact : ajouter une note, enregistrer une nouvelle contribution, inscription à un événement, etc.

![image](/img/ActionRibbon.PNG)

### Onglet résumé

L'onglet résumé vous montre les informations principales concernant votre contact. Vous y trouverez notamment ses noms, adresses et autre détails de contact ainsi que les moyens pour le contacter.

Certains champs de cet onglet sont propres au type de contact Individu / Particulier (nom, prénom...) et d'autres propres au type de contact organisation (nom de l'organisation...).

![image](/img/ContactSummary.PNG)

#### Champs propres aux individus / particuliers

Les noms des individus / particuliers sont découpés en parties : préfixe, prénom, deuxième prénom, nom, suffixe et surnom (vous n'avaez pas à tous les utiliser). Les préfixes et suffixes sont sélectionnés à l'aide d'une liste déroulante. Vous pouvez la personnaliser en allant à : **Administrer > Personnaliser les données et écrans > Listes déroulantes > Civilité** et **Suffixes**. 

#### Adresses

Vous pouvez enregistrer une ou plusieurs adresses pour un contact. Chaque adresse doit être d'un type différent de localisation (Travail, domicile...). L'une d'entre elle peut être marquée comme principale et sera utilisée pour tout publipostage. Vous pouvez choisir explicitement quel type de localisation sera l'adresse principale, ou laissez par défaut la première adresse qui sera renseignée.

Vous pouvez partager des adresses entre contacts. Par exemple, vous pourriez avoir besoin d'information entre des contacts  de type individus / particuliers et leur lieu de travail (contact de type organisation). Lorsque vous créez ou modifiez l'adresse "Travail" pour un individu / particulier, activez la case à cocher "Partager l'adresse avec". Si son employeur existe déjà dans la base de donnée, vous pouvez le sélectionner depuis la boite de recherche rapide qui apparait. Sinon, vous pouvez créer à la volée l'enregistrement de l'employeur en sélectionnant "Nouvelle organisation" depuis la liste déroulante "Créer un nouveau contact".

Si une personne effectue un paiement par carte de crédit, les informations utilisées par cette opération seront stockées dans l'adresse de facturation du contact. 

Si vous avez un fournisseur de cartographie actif, vous pouvez cliquer sur l'icône à côté de l'adresse pour voir ses coordonnées sur une carte.

#### Numéros de téléphone 

Vous pouvez stocker plusieurs numéros de téléphone pour chaque contact. Ils sont classés par localisation (travail, domicile...) et par type (filaire, mobile, fax...). Veuillez noter que n'importe quel numéro de téléphone de type "mobile" sera disponible pour l'envoi de SMS.

#### Adresses courriel

Vous pouvez stocker plusieurs adresses courriel pour chaque contact. L'une de ces adresses doit être explicitement marquée comme l'adresse recevant tous les courriels de votre organisation tels que les infolettres/newsletters, les annonces (tous les courriels envoyés depuis le composant CiviMAil). Tout courriel n'arrivant pas à son destinataire est, dans CiviMail, marqué "en suspend". Veuillez vous référer à la section Courriel pour plus d'information.

#### Préférence de communication et protection de la vie privée 

Les moyens de communication préférés des contacts (téléphone, courriel...) et les options de protection de leur vie privée (ne pas appeler, ne pas envoyer de courrier postal...) peuvent être définis. Les options de protection de la vie privée sont respectée lors de l'exécution de certaines fonctionnalités de CiviCRM : les étiquettes de publipostage ne sont pas imprimées pour les contacts ayant coché "ne pas envoyer de courrier", et les courriels ne sont pas envoyés à ceux ayant coché "ne pas envoyer de courriel".

Voici une brève explication de chaque option de protection de la vie privée disponible dans la fiche d'un contact :

-   **Ne pas appeler** : L'utilisateur a choisi de ne pas être contacté par téléphone ;
-   **Ne pas envoyer de courriel**- L'utilisateur a choisi de ne pas être contacté par courriel ;
-   **Ne pas envoyer de courrier**- L'utilisateur a choisi de ne pas être contacté par courrier postal ;
-   **Ne pas envoyer de SMS**- L'utilisateur a choisi de ne pas être contacté par SMS ;
-   **Ne pas transmettre les données personnelles**- L'utilisateur a choisi de ne pas partager ses données personnelles (que vous pourriez partager ou vendre à des organisations tierces) ;
-   **Utilisateur s'est exclu des mailings**- Cette case est cochée quand l'utilisateur a cliqué sur le lien d'exclusion fourni dans un courriel géré par CiviMail.

#### Champs de salutation et destinataire

Par défaut, les champs de salutations et destinataires sont calculés à partir des champs de nom du contact. Par exemple, la salutation dans un courrier postal pour un individu / particulier s'appelant "Jean Dupont" sera "Cher Jean".

Les salutations par défaut peuvent être configurées de manière globale en allant à **Administrer > Communications > Formules de salutation par courrier *or* Formules de salutation par courriel *or* Formats de destinataires**.

Différents formats peuvent aussi être paramétrés au niveau de chaque contact.

### Onglet Relations

Les relations sont des connexions entre des enregistrements de contacts dans votre base de donnée. Chaque connexion peut être nommée pour en décrire sa nature, et chaque contact peuvent avoir plusieurs relations avec d'autres contacts dans la base de donnée. Dans l'exemple ci-dessous, vous pouvez voir une liste de relations courantes et de relations inactives.

![Contact-RelatoinshipTab_1](/img/CiviCRM_update-CiviCore-Contact-RelatoinshipTab_1-en.png)

Vous pouvez en savoir plus sur les relations dans le chapitre *Relations* de la section *Organiser vos données*.

### Onglet Activités

L'onglet Activités affiche une liste de toutes vos interactions avec un contact, y compris toutes les activités "métier" de CiviCRM telles que les participations à des événéments, les contributions, les appels téléphoniques... ainsi que toutes les activités personnalisées que vous pourriez ajouter. Il est également possible d'y enregistrer vos interactions avec le contact : Cliquez sur la liste déroulante en haut de l'écran et sélectionnez un type d'activité (Passer un appel téléphonique, Envoyer un courriel...) vous fera afficher un écran sur lequel entrer les détails.

![Contact_ActivityTab](/img/CiviCRM_update-CiviCore-Contact_ActivityTab-en.jpg)

Pour en savoir plus sur les activités, merci de vous référer au chapitre *Activités* de cette section.

### Onglet Mailings

Cet onglet est visible uniquement si vous avez décoché **Permettre à CiviMail de créer une activité à l'envoi** dans **Administrer > CiviMail > Paramètres de composant CiviMail**. Dans ce cas, chaque courriel envoyé en masse est enregistré dans cet onglet plutôt que dans l'onglet Activités. Cela permet d'améliorer la vitesse d'affichage de ce dernier si votre organisation diffuse massivement de nombreux courriels. 

### Onglet Contributions

L'onglet Contributions affiche toutes les contributions financières faite par un contact, ainsi qu'une synthèse (montant total des contributions pour une période donnée, nombre total des contributions ou montant moyen des contributions)

Cet onglet vous permet également d'enregistrer manuellement des contributions qui n'aurait pas été faites en ligne, en utilisant le bouton **Nouvelle contribution**.

![Contact_COntribTab](/img/CiviCRM_update-CiviCore-Contact_COntribTab-en.jpg )

Pour en savoir plus sur ce sujet, veuillez vous référer au chapitre *Contributions* de ce manuel.

### Onglet Adhésions

Cet onglet affiche les adhésions du contact. Vous pouvez également y enregistrer manuellement celles qui n'auraient pas été faites en lignes, en utilisant le bouton **Ajouter une adhésion**. Vous pouvez également renouveler ou supprimer des adhésions depuis le lien "plus" à droite de chaque adhésion associée au contact.

![Contact_MembershipTabs](/img/CiviCRM_update-CiviCore-Contact_MembershipTabs-en.jpg)

Pour en savoir plus sur ce sujet, veuillez vous référer au chapitre *Adhésions* de ce manuel.

### Onglet Événement

Cet onglet affiche les événéments associés au contact. Par exemple, ceux pour lesquels le contact s'est inscrit, ou encore ceux pour lesquels il s'est porté volontaire.

Depuis cette page, vous pouvez inscrire un contact à un événement, et même enregistrer le paiement associé (ce dernier apparaitra alors dans l'onglet Contribution).

Vous pouvez également modifier les informations d'un événement associé au contact en cliquant sur le lien "Modifier". Par exemple, vous pouvez changer le statut d'un contact sur un événement de "Enregistré" à "En attente".

![Contact_Eventstab](/img/CiviCRM_update-CiviCore-Contact_Eventstab-en.jpg)

Pour en savoir plus sur ce sujet, veuillez vous référer au chapitre *Événements* de ce manuel.


### Onglet Groupes

Cet onglet affiche les groupes auxquels appartient le contact. Les groupes sont utilisés de façon très variée : liste de diffusion de courriel, gestion des autorisations d'accès...

Dans cet onglet, vous pouvez ajoutez ou retirer le contact d'un groupe, et en voir l'historique.

La colonne Statut indique l'utilisateur qui a ajouté le contact au groupe. Il est possible d'autoriser les utilisateurs à s'ajouter eux-même à un groupe. Lorsque vous paramétrez la visibilité d'un groupe à "Listes publiques", les utilisateurs peuvent s'y ajouter à travers un formulaire **Profil** (plus d'information à ce sujet dans le chapitre *Les profils* de cette section).

![Contact_GroupsTab](/img/CiviCRM_update-CiviCore-Contact_GroupsTab-en.jpg)

Pour en savoir plus sur ce sujet, veuillez vous référer au chapitre *Groupes et étiquettes* de ce manuel.

### Onglet Notes

Vous pouvez dans cet onglet enregistrer n'importe quelle information concernant le contact. En général, il est conseillé d'utiliser des champs personnalisés pour des données spécifiques que vous souhaitez collecter auprès de vos contacts. Mais dans certains cas, il peut être utile d'enregistrer quelques notes "telles quelles". Toutefois, ce type d'information n'ayant pas de structure propre, il faut rester prudent quant à son utilisation et avoir le réflexe de consulter régulièrement cet onglet. Les champs d'une note (sujet et contenu) sont libres (pas de format imposé).

Vous pouvez spécifier "Auteur uniquement" pour une note. Dans ce cas, seul l'auteur pourra la lire ou la modifier, ou quelqu'un ayant l'autorisation "Voir toutes les notes" dans CiviCRM.

![Contact_NotesTab](/img/CiviCRM_update-CiviCore-Contact_NotesTab-en.jpg)

### Onglet étiquettes

Les étiquettes sont une possibilité de classer vos contacts dans votre base de donnée (les autres moyens sont les groupes et les données personnalisées). Vous pouvez créer autant d'étiquettes que vous le souhaitez pour gérer votre organisation. Vous pouvez faire des recherches sur les étiquettes et créer des groupes dynamiques basés sur ces dernières.

![Contact_TagTab](/img/CiviCRM_update-CiviCore-Contact_TagTab-en.jpg "Contact_TagTab")

Pour en savoir plus sur ce sujet, veuillez vous référer au chapitre *Groupes et étiquettes* de ce manuel.

### Onglet Journal des modifications

Cet onglet vous donne des informations synthétiques sur les modifications faites sur l'enregistrement d'un contact : la date et l'auteur des changements, mais pas ce qui a été changé.

![Contact_ChangeLog](/img/CiviCRM_update-CiviCore-Contact_ChangeLog-en.jpg "Contact_ChangeLog")


Ajouter des contacts
--------------------

La façon la plus simple d'ajouter un seul contact dans CiviCRM est d'utiliser le menu principal et de se rendre à **Contacts > Nouvel individu**.

![Contact_createIndividual](/img/CiviCRM_update-CiviCore-Contact_createIndividual-en.jpg "Contact_createIndividual")

Veuillez noter que le menu Contacts vous propose de créer tous les types et sous-type de contacts.

Tous les formulaires de création de contact sont disposés de façon similaire, avec les informations de base (nom, courriel...) en haut et les champs plus spécifiques plus bas, regroupés par type ou sujet.

Pour tous les types de contacts, vous pouvez utiliser l'option **Vérification de concordance avec contact(s)** pour éviter de créer un doublon. Il suffit de cliquer sur ce bouton après avoir rempli tous les champs de la section.

* Pour ajouter un enregistrement de type Individu / Particulier dans la base de données, vous devez fournir soit le prénom et le nom, soit l'adresse courriel. Pour ajouter un enregistrement de type Organisation ou Ménage / Foyer, seul leur nom est obligatoire.*

Ce qui est utile de savoir lorsque vous ajoutez des contacts :

Adresses :
Vous pouvez ajouter plusieurs adresses pour un contact (domicile, travail, adresse de facturation...)

Vous avez la possibilité de partager une adresse avec un autre contact (existant ou nouveau) en activant la case à cocher associée. Si vous sélectionnez un nouveau contact, vous aurez besoin de choisir son type et une boite pop-up apparaitra pour réaliser l'opération. Quand une personne utilise l'adresse d'un autre contact, cette adresse ne peut être modifiée que depuis la fiche du contact "propriétaire".  

Les noms des pays disponibles dans la liste déroulante dépendent de ce que vous aurez paramétré dans **Administrer > Localisation > Langue, devises et localisation** dans Pays Disponibles.

Il y a peut-être des champs d'adresse dont vous n'aurez pas besoin. Leur disponiblité peut être paramétrée dans **Administrer > Localisation > Paramètres d'adresse**. Le champ spécial "Address Name", qui peut être utilisé pour labellisé une adresse particulière (par exemple "domicile d'été") est caché par défaut. Vous pouvez l'activer depuis cet écran.

Étiquettes et groupes :
Dans cette rubrique, vous pouvez spécifier les étiquettes et les groupes que vous souhaitez ajouter à votre contact. Seuls ceux déjà existants peuvent être ajoutés. Pour en savoir plus sur la création de nouveaux groupes et étiquettes, veuillez vous référer au chapitre *Groupes et étiquettes* du manuel.


Une fois que vous avez complété le formulaire, vous pouvez cliquer sur l'un des trois boutons suivants :

-   **Enregistrer** Sauvegarde le contact et vous laisse sur l'écran ;
-   **Enregistrer et nouvelle entrée** Sauvegarde le contact et affiche un nouveau formulaire d'enregistrement vierge pour en ajouter un nouveau ;
-   **Annuler** Annule le formulaire en cours et vous renvoie au tableau de bord.


Modifier des contacts
---------------------

Il est simple de modifier des informations dans l'onglet Résumé : lorsque le curseur de la souris survole un bloc, le lien **Éditer les infos** apparait en haut à droite. Cliquer dans ce bloc activera les champs qui seront alors modifiables.

Si vous avez besoin de modifier un nombre important de données pour un contact spécifique, vous pouvez mettre tout le formulaire en mode Édition en cliquant directement sur le bouton **Modifier** au dessus des onglets.

![image](/img/contact%20Screen%20-inline%20edit.png) 

En de rares occasions, il est possible que deux utilisateurs éditent une fiche contact en même temps (en particulier s'ils ouvrent la même fiche contact puis la sauvegarde en même temps). Dans ce cas, le second utilisateur sera notifié des modifications du premier et aura la possibilité de les fusionner. 


Supprimer des contacts
----------------------

Il existe le bouton **Supprimer contact**. Quand un contact est supprimé, il ne disparait pas complètement : par défaut, il est déplacé dans la corbeille. Cela offre la possibilité d'être restauré plus tard, en utilisant l'option *Rechercher dans la corbeille* de la recherche avancée.


Sous-types de contact 
---------------------

En plus des trois types de contact fournis par défaut (Individu/Particulier, Ménage/Foyer et Organisation), vous pouvez ajouter des types supplémentaires (appelés parfois sous-type) pour adapter CiviCRM à vos besoins.

Chaque sous-type que vous définissez est basé sur l'un des trois types de contact fournis par défaut. Par exemple, le type "Étudiant" serait basé sur le type "Individu/Particulier, le type "Ferme" basé sur "Organisation", ou peut-être "Ménage/Foyer" selon votre cas d'utilisation.

Les types de contacts sont très utiles pour collecter et afficher des jeux de données personnalisées. Par ex., vous pourriez souhaiter collecter et afficher le domaine et les qualifications des professeurs de votre base de donnée mais pas pour les autres individus/particuliers. Pour cela, il suffirait de créer un type "Professeur" se basant sur "Individu/particulier", puis de créer des champs personnalisés associés à ce nouveau type (voir le chapitre *Créer des champs personnalisés* dans ce manuel).

Notez que les types fournis par défaut sont mutuellement exclusifs : un contact ne peut pas être à la fois de type Individu/particulier et Organisation par exemple. Toutefois, un contact peut cumuler plusieurs sous-types personnalisés. Par exemple, un contact peut être un professeur et un parent.

Pour modifier des types de contact existant, ou pour en créer de nouveaux, aller à **Administrer > Personnaliser les données et écrans > Types de contact**. Veuillez noter que vous ne pouvez pas supprimer les types de contact fournis par défaut dans CiviCRM, mais vous pouvez changer leur nom et l'icône qui leur est associée.


Personnaliser la vue des contacts
--------------------------------

Après un certain temps à travailler sur les fiches de contacts, vous pourriez réaliser que certaines sections ou champs ne sont pas utiles pour votre organisation. Vous pouvez dans ce cas facilement les cacher en paramétrant vos préférences (droits Admin CiviCRM nécessaires) :

-   Allez à **Administrer > Personnaliser les données et écrans > Préférences d'affichage** ;
-   Désactiver la case à cocher données démographiques dans la rubrique *Informations éditables* ;
-   Cliquez sur Enregistrer.

Vous pouvez également utiliser cet écran pour réarranger l'ordre de disposition de l'information.

De manière similaire, vous pouvez supprimer ou ajouter des champs dans la section *Adresse postale* :

-   Allez à **Administrer > Localisation > Paramètres d'adresse** ;
-   Cochez ou décochez les cases dans la rubrique *Édition de l'adresse* ;
-   Cliquez sur Enregistrer.

Si vous pensez que certains onglets ne sont pas utiles, vous pouvez les désactiver en allant à **Administrer > Personnaliser les données et écrans > Préférences d'affichage**. Vous pouvez également en activant d'autres. Dans ce cas, si l'onglet n'apparait pas dans les préférences d'affichage, pensez à vérifier si vous avez bien activé le composant correspondant (par exemple, l'onglet Contributions n'apparaitra que si vous avez activé CiviContribute).
