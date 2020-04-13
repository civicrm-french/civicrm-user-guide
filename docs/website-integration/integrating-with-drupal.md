# Intégration avec Drupal

Des trois CMS pouvant intégrer CiviCRM, Drupal est celui ayant reçu le plus d'attention, et offrant le plus d'options d'intégration. Cela est dû en partie parce que la communauté Drupal est principalement une communauté de développeurs.

Lorsque l'on pense à l'intégration à un site web avec Drupal, il est important de comprendre le concept de *modules Drupal*. Un module peut être considéré comme une application fournissant au CMS des fonctionnalités supplémentaires. Par exemple, le module *Calendar* vous permet d'afficher des calendriers sur votre site web. La distributation Drupal de CiviCRM contient plusieurs modules Drupal facilitant son intégration, et ce de différentes façons.

## Rôles et permissions Drupal

Lorsque vous créez un nouvel *Utilisateur* sur un site Drupal et que CiviCRM y est intégré, alors ce dernier créera automatiquement un enregistrement *Contact* lui correspondant. *Utilisateur* et *Contact* possède tous deux une identification / numéro d'index différents.

*Voir également le chapitre [Autorisations et contrôle d'accès](../initial-set-up/permissions-and-access-control.md) de la section* Configuration initiale *pour une discussion générale sur le contrôle d'accès.*

Votre site Drupal vous permet de créer différents *Rôles*. Ces rôles sont assignés à des utilisateurs du site, et chaque rôle contient des *permissions* qui vous permettent de réaliser une certaine série de tâches (voir, modifier, supprimer, et administrer des contacts) ou accéder à un certain jeu d'information (contacts CiviCRM, CiviMail, CiviEvents, Drupal USers, etc.)

Pour plus d'information sur les rôles Drupal, merci de lire la documentation disponible sur drupal.org :
-   [Utilisateur : paramètres d'accès et de gestion](https://www.drupal.org/docs/8/core/modules/user/overview) ;
-   [Gérer les contrôles d'accès avec les rôles et les permissions Drupal](https://www.drupal.org/node/22275) ;

Les *permissions* Drupal vous permet de définir quelles tâches un *rôle* particulier de Drupal peut executer, et à quelles informations il a accès. Les *permissions* déterminent également le niveau d'accès qu'un certain type d'utilisateur a sur la configuration des modules, l'affichage, l'édition, les utilisateurs ou les informations de contact CiviCRM.

Pour plus d'information sur le paramétrage des permissions Drupal, veuillez lire la documentation sur drupal.org :
-   [Ajuster les permissions après l'ajout d'un module](https://www.drupal.org/node/22279) ;
-   [Références sur les permissions](https://www.drupal.org/node/132202) ;
-   [Permissions pour le module Vues](http://drupal.org/node/1089746) ;


Les rôles Drupal sont globaux et écraseront les contrôles d'accès (voir le chapitre [Autorisations et contrôle d'accès](../initial-set-up/permissions-and-access-control.md) dans la section *Configuration initiale*) définis dans CiviCRM.
Par exemple, si vous définissez un contrôle d'accès pour limiter l'accès à certains contacts mais qu'un rôle Drupal possède la permission *Accéder à tous les contacts*, alors toute personne associée à ce rôle pourra voir l'ensemble des contacts.


Taxinomies Drupal, accès au contenu ou tout autre module d'accès basé sur un rôle utilisateur
---------------------------------------------------------------------------------------------

Il existe plusieurs modules Drupal pouvant déterminer quel rôle Drupal a accès à un certain type de contenu dans votre site web. Cela peut être basé sur les taxinomies, en sélectinnant un accès à des noeux spécifiques, des paramètres sur des vues spécifiques, pages ou paneaux, ou basé sur un certain contexte ou règle. Voici ci-dessous quelques uns de ces modules :

-   [Views](https://www.drupal.org/project/views) ;
-   [Panels](https://www.drupal.org/project/panels) ;
-   [Chaos Tools Suite (ctools) and Page Manager](https://www.drupal.org/project/ctools) ;
-   [Context](https://www.drupal.org/project/context) ;
-   [Content Access](https://www.drupal.org/project/content_access) ;
-   [Taxonomy Access Control](https://www.drupal.org/project/taxonomy_access) ;

Vues Drupal
-----------

[Views](https://www.drupal.org/project/views) est un puissant module Drupal vous permettant d'afficher du contenu de site web comme, par exemple, les dernières nouvelles de votre page d'acceuil. CiciCRM intégré avec ce module permet d'afficher les données CiviCRM sur le site web. Par exemple, si vous souhaitez créer une page appelée *Organisations partenaires* et que vous souhaitez l'afficher au grand public, vous pourriez utiliser la procédure suivante :

1. Sélectionnez le critère déterminant le jeu de contacts à prendre en compte, tel que :
   * Contacts de type *Organisation* uniquement ;
   * Ceux tagués "Partenaire" dans CiviCRM ;
   * Ceux ayant un statut d'adhésion *Nouveau* ou *En cours*.
2. Choisissez quelles données seront affichées, telles que :
   * Nom de l'organisation ;
   * Région ;
   * Site web ;
   * Numéro de téléphone.
3. Choisissez le format d'affichage (table ou paragraphe) ;
4. Autorisez le public à filtrer le résultat, par exemple par région.

Il s'agit ici d'un simple exemple, les possibilités de jouer avec les vues Drupal et les données CiviCRM étant bien plus vastes.

### Configuration

Si vos bases de données Drupal et CiviCRM sont distinctes, ajouter le support CiviCRM au module *Vues* requiert un brin de configuration. Il s'agit d'indiquer aux vues où trouver les données CiviCRM.
Allez à **Administrer** > **Paramètres système** > **Intégration à la base de donnée du CMS**. Vous pourrez visualiser les lignes de code à recopier après le code du fichier *settings.php* de Drupal. En cas de problème, vous pouvez demander de l'aide dans le [forum](http://forum.civicrm.org/) or [engager un consultant](http://civicrm.org/what/experts). Si vous utilisez des jeux de données personnalisées, et à chaque fois que vous en ajouterez, vous devrez répéter le processus.

### Créer des vues utilisant des données CiviCRM

Les vues font partie de la section **Structure** du menu d'administration Drupal. Lorsque vous créez une vue, nommez-là et sélectionnez le type de données que vous souhaitez afficher.

De façon générale, si votre vue concerne des contacts, vous sélectionnerez Afficher: Contacts CiviCRM. Si vous souhaitez afficher d'autres détails comme des événements, des relations, des contributions ou des activités, il existe des options vous permettant d'enrichir votre vue.

![image](/img/Views-CiviCRM-Partner-1.png)

Quand la vue est créée, ajustez les champs, filtres, affichage et autres configurations pour adapter la page à vos besoins.

![image](/img/Views-CiviCRM-Partner-3.png "sample configuration using Views 3 in a Drupal 7 environment")  


### Ce que peuvent également faire les vues et CiviCRM

-   Liste des événements à venir ;
-   Construction de rapport sur les contributions, activités ou participants ;
-   Liste des donateurs les plus récents ;
-   Listes de comité, conseil d'administration, bureau... ;
-   Liste des membres de votre organisation ;
-   et plus encore !

Webform CiviCRM 
---------------

Tout comme les vues peuvent *sortir* les données de multiples façons, le module Webform peut les faire *entrer* exactement de la façon que vous souhaitez : vous pouvez créer et mettre à jour des contacts, des inscriptions à des groupes, à des étiquettes, des champs personnalisés et effectuer des paiement en ligne. Le module Webform offre une souplesse d'utilisation encore plus importante que l'utilisation des profils CiviCRM.

Par exemple, vous pouvez :
  - créer un formulaire pour ajouter dans vos contacts une famille complète avec toutes les relations définies ;
  - créer une nouvelle activité lorsqu'une personne complète un formulaire.
  
Le module Webform CiviCRM possède une documentation en ligne très complète. Pour plus d'information, veuillez vous référer au chapitre [Webform CiviCRM Integration](https://docs.civicrm.org/sysadmin/en/latest/integration/drupal/webform/) (en anglais) du manuel de l'administrateur système de CiviCRM.

CiviCRM Organic Groups Sync
---------------------------

Le module [Organic Groups CiviCRM](https://www.drupal.org/project/og_civicrm) permet d'intégrer les groupes organiques de Drupal aux groupes CiviCRM. Cela s'avère utile pour les groupes requérant la fonctionnalité *Groupe organique* sur le site web mais dont les changements doivent également se refléter au sein de CiviCRM. Une fois les utilisateurs Drupal d'un groupe organique intégrés à CiviCRM, le groupe peut être utilisé pour de la diffusion massive de courriel, du suivi d'activité, ou tout autre chose liée aux contacts.

Une fois le module Organic Groups CiviCRM installé et activé dans Drupal, ce dernier créé automatiquement deux groupes CiviCRM pour chaque groupe organique Drupal existant :
-   Un groupe régulier contenant un enregistrement de contact pour chaque utilisateur Drupal d'un groupe organique. Ce groupe possède le même nom que le groupe organique ;
-   un groupe ACL contenant l'enregistrement de contact de l'administrateur du groupe organique correspondant. Cela donne à ce dernier la possibilité de visualiser et de modifier les membres du groupe normal correspondant dans CiviCRM.

ATTENTION : La synchronisation de ces groupes ne se fait que dans le sens groupe organique Drupal vers les groupes CiviCRM.

Lorsqu'un nouvel utilisateur est ajouté dans un groupe organique, il est automatiquement ajouté dans le groupe CiviCRM correspondant. S'il quitte le groupe organique, il est également dissocié du groupe CiviCRM. Si un groupe organique est supprimé, les groupes CiviCRM sont également supprimés. Toutefois, l'inverse n'est pas vrai : un contact ajouté dans un groupe CiviCRM ne sera pas ajouté dans le groupe organique correspondant. Idem pour sa suppression. L'administration de ces groupe doit donc se faire du côté du site Drupal.

CiviGroup Roles Sync
--------------------

Le module CiviGroup Roles Sync permet aux administrateurs du site Drupal de gérer et paramétrer l'expérience utilisateur tel que des donateurs ou du personnel de l'organisation. Il permet notamment de :
   - autoriser aux membres du conseil d'administration, du personnel, des bénévoles un accès à du contenu spécifique, ou l'execution de tâches particulières ;
   - fournir une expérience personnalisée pour les utilisateurs d'un groupe spécifique lors de l'accès au site web. Par exemple, lorsqu'un donateur important se connecte au site web, ce dernier peut afficher une lettre du Président le remerciant pour sa contribution, ou encore fournir un accès d'inscription pour des événements particuliers.

Avant toute configuration, vous devriez passer du temps à envisager toutes les interactions que les différents utilisateurs seront amenés à faire avec le site web. Demandez-vous si l'expérience utilisateur dépend d'un groupe particulier, d'équipe, de comité ou si un contact doit remplir certains critères, ou si vous devriez appliquez manuellement des rôles à des utilisateurs.

En bref, ce module vous permet de synchroniser les utilisateurs Drupal ayant un certain rôle avec les contacts CiviCRM dans un certain groupe.

### Planification

Avant d'utiliser ce module, vous devriez avoir préparé les points suivants :
   - les groupes de votre organisation doivent avoir été créés ;
   - les rôles Drupal correspondant à chaque cas d'utilisation doivent également avoir été créés ;
   - si vous utilisez des modules supplémentaires pour affiner vos accès au contenu, ces derniers devraient préalablement être installés et configurés.

Au moment de déterminer les groupes et les rôles Drupal que vous devrez créer, il est important de garder en tête que plusieurs types de groupes peuvent être associés à un rôle Drupal, et qu'un seul groupe peut être associé à plusieurs rôles Drupal.


### Synchroniser les groupes CiviCRM avec les rôles Drupal

-   Activez le module depuis l'écran d'administration Drupal des modules ;
-   Allez à l'écran de configuration CiviGroup Role Sync ;
-   Cliquez sur **Ajouter une règle d'association**
-   Sous *Groupe CiviCRM*, sélectionnez le groupe d'utilisateurs pour lesquels vous voulez qu'un rôle Drupal particulier soit associé ;
-   Sous *Rôle Drupal*, sélectionnez le rôle Drupal à associer ;
-   Cliquez sur **Ajouter une règle d'association**.

Vous pouvez toujours modifier ou supprimer une règle ultérieurement depuis ce même écran de configuration.


CiviMember Roles Sync
---------------------

Le module CiviMember Roles Sync permet aux administrateurs Drupal de gérer et paramétrer l'expérience utilisateur pour les membres de votre organisation. Il permet notamment de :
-   Accorder automatiquement un rôle Drupal en fonction du type d'adhésion et de son statut ;
-   Permettre à un utilisateur d'accéder à du contenu réservé aux membres, ou d'executer des tâches que leur sont réservées ;
-   Restreindre à des anciens membres l'accès à ce contenu et proposer à la place un formulaire de réadhésion.

### Exemple de Scenario: Contenu réservé aux membres

L'association Retail Baker's of America (RBA) mettre en relation les fournisseurs et les propriétaires de boulangerie à travers tout le pays afin de promouvoir une communité encourageant les échanges d'affaires, les informations industrielles, et établir des standards industriels à travers des certifications, de la recherche et des programmes scolaires.

Les visiteurs de leur site web tombent dans les trois expériences utilisateur suivantes :
   - Les non-membres qui achètent du matériel et des ressources via la boutique en ligne de RBA. Un non-membre doit créer un compte utilisateur afin de procéder aux transactions, accèder à son historique d'achat, et éventuellement être contacté par l'association pour se voir proposer une adhésion ;
   - Les membres ayant une adhésion à jour, et qui ont accès aux ressources *membre uniquement* tel qu'un forum de discussion, du matériel de marketique, et une version numérique des publications de RBA.
   - Les membres ayant une adhésion expirée, en période de grâce, ou anciens membres souhaitant renouveler leur adhésion pour accèder à nouveau au contenu *membre uniquement*.
   
RBA utilise CiviMember Role Sync pour accorder le rôle Drupal "membre actif" à tout utilisateur ayant une adhésion à jour. Ce rôle est enlevé lors de la période de grâce, puis ajouté à nouveau en cas de réadhésion.

### Planification

Vous devriez passer un peu de temps à réfléchir aux différentes façons dont les utilisateurs interagissent avec votre site web. Demandez-vous s'il existe des cas d'utilisation qui dépendent de votre structure d'adhésion, ou qui dépendent plutôt de comité, équipe ou contacts remplissant certains critères (cf module précédent).

### Types d'adhésion CiviCRM

Il est important d'avoir une compréhension totale de ce que sont les types et les status d'adhésion CiviCRM. Vous trouverez les explications détaillées sur le composant CiviMember au chapitre [Définition des adhésions](../membership/defining-memberships.md) de la section *Adhésion*


### Configurer CiviMember Roles Sync

Avant de pouvoir utiliser le module CiviMember Roles Sync, vous devriez avoir préparé les points suivants :
-   Les types et les status d'adhésion de votre organisation devraient avoir été créés et configurés dans le composant CiviMember ;
-   Les rôle Drupal nécessaires à vos cas d'utilisation doivent également avoir été créés ;
-   Les contenus et les tâches accessibles uniquement à un type d'adhésion devraient avoir été identifié
-   si vous utilisez des modules supplémentaires pour affiner vos accès au contenu, ces derniers devraient préalablement être installés et configurés.

Au moment de déterminer les types d'adhésion et les rôles Drupal que vous devrez créer, il est important de garder en tête que plusieurs types d'adhésion peuvent être associés à un même rôle Drupal, et qu'un seul type d'adhésion peut être associé à plusieurs rôles Drupal.

*Dans notre scenario, l'association Retail Baker's of America possède cinq types différents d'adhésion : Sponsor d'entreprise, Boulangerie, Individu, Étudiant et Boulanger retraité. À ces cinq types d'adhésion correspondent un seul rôle Drupal, celui de "Membre actif". Ce rôle donne accès au contenu réservé aux membres. De plus, les adhérents de type Sponsor d'entreprise ont également accès à du contenu supplémentaire exclusif. RBA décide d'appeler le rôle Drupal "Membre d'entreprise". Ces utilisateurs auront donc deux rôles associés : "Membre actif" et "Membre d'entreprise".*


#### Activer le module CiviMember Roles Sync

1. Allez à la liste de vos modules Drupal :
    -   Drupal 6: **Administrer** > **Construction du Site** > **Modules** ;
    -   Drupal 7: **Modules** dans le menu d'administration Drupal ;

2. Cochez la case (mettre à "ON") à côté du module **CiviMember Roles Sync** puis cliquez sur **Enregistrer la configuration** ;

#### Synchroniser les types d'adhésion CiviCRM avec les rôles Drupal

1. Allez à l'écran de configuration CiviMember Role Sync :
    -   Drupal 6: **Administrer** > **Construction du Site** > **CiviMember Roles Sync** ;
    -   Drupal 7: **Configuration** > **CiviMember Roles Sync** ;

2. Cliquez sur **Ajouter une règle d'association** ;

3. Sous *Sélectionnez un type d'adhésion CiviMember*, choisissez celui pour lequel un rôle Drupal sera associé ;

4. Sous *Sélectionnez un rôle Drupal*, choisissez le rôle correspondant.

*Exemple: RBA souhaite que tout utilisateur ayant une adhésion en cours de type "Boulangerie" puisse être gratifié du rôle Drupal "Membre actif". Pour cela, le personnel créera une règle d'association et sélectionnera "Boulangerie" dans la section* Type d'adhésion *, et "Membre actif" dans la section* Rôle Drupal.

5. Sous *Statut en cours*, sélectionnez le statut d'adhésion pour lequel l'utilisateur devrait voir s'accorder le rôle Drupal.

*Exemple: RBA souhaite gratifier tout utilisateur dont le statut d'adhésion est soit "En cours", soit "Nouveau" soit "Période de grâce" au contenu réservé aux membres. Le personnel va donc cocher les boites correspondant à ces statuts.*

6. Sous *Statut expiré*, sélectionnez le statut d'adhésion pour lequel le rôle Drupal sera révoqué au niveau de l'utilisateur.

*Exemple: RBA souhaite s'assurer que tout utilisateur dont l'adhésion expire ou soit annulée ai leur accès au contenu réservé aux membres révoqué. Le personnel va donc cocher les boites correspondant à ces statuts.*

7. Cliquez sur **Ajouter une règle d'association** lorsque vous avez terminé.

8. Répétez les étapes 1 à 7 pour ajouter toutes les règles d'association nécessaires à votre organisation, puis passez à l'étape 9.

9. Cliquez sur l'onglet **Synchroniser manuellement**

10. Cliquez sur **Synchroniser les types d'adhésion CiviMember avec les rôles Drupal maintenant**.

#### Modifier des règles d'association existantes

1. Pour modifier ou supprimer une règle d'association, allez à l'écran de configuration CiviMember Role Sync :
    -   Drupal 6: **Administrer** > **Construction du Site** > **CiviMember Roles Sync** ;
    -   Drupal 7: **Configuration** > **CiviMember Roles Sync** ;

2. Vous devriez voir maintenant la liste des règles existantes. Si ce n'est pas le cas, cliquez sur l'onglet **List Association Rule(s)**.
    -   Pour modifier une règle :
            * positionnez-vous sur celle-ci et cliquez sur **modifier** ;
            * effectuez les changements puis cliquez sur **modifier la règle d'association**

    -   Pour supprimer une règle :
            * positionnez-vous sur celle-ci puis cliquez sur **supprimer** ;

#### Configurer les moments de synchronisation

Vous avez le choix entre différentes options pour synchroniser les types d'adhésion CiviCRM avec les rôles Drupal. Pour cela, allez dans l'écran de configuration CiviMember Role Sync habituel, puis choisissez l'une des options disponibles :

-   Synchronise lorsque quelqu'un se connecte ou se déconnecte (option par défaut) : cette méthode déclenche la synchronisation uniquement après que quelqu'un se soit connecté ou déconnecté de son compte. Vous devriez être prudent avec cette option car si vous gérez des sessions d'utilisateurs très longues, ces derniers auront accès aux contenus ou tâches  *membres uniquement* jusqu'à ce qu'ils se déconnectent ;
-   Synchronise lors d'un cron Drupal : cette méthode repose sur un cron Drupal pour déclencher la synchronisation. Vous pouvez en savoir plus sur le cron Drupal, allez à [https://www.drupal.org/docs/7/setting-up-cron/overview](https://www.drupal.org/docs/7/setting-up-cron/overview)
-   Synchronise lorsqu'une adhésion est mise à jour : cette méthode déclenche la synchronisation lorsqu'un utilisateur adhère ou renouvelle son adhésion, ou lorsque qu'un membre du personnel met à jour l'adhésion d'un contact depuis le back-office ;
-   Désactive la synchronisation automatique : uniquement si vous comptez sur un membre du personnel pour déclencher manuellement la synchronisation. Pour faire cela, allez à **CiviMember Roles Sync settings**, cliquez sur l'onglet **Synchronisation manuelle** puis cliquez sur **Synchronisez les types d'adhésion CiviMember avec les rôles Drupal maintenant**.

Assurez-vous de cliquer sur **Enregistrer la configuration** après vos changements.
