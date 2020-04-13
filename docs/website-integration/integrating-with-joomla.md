Intégration avec Joomla!
=======================

CiviCRM s'intègre très facilement à Joomla! En tant que composant.
Les formulaires publics CiviCRM tels que les pages de contribution en ligne et les pages d'inscription des événements peuvent être intégrés comme éléments de menu sur le front-end de votre site Joomla!, en utilisant votre thème personnel. Lorsque vous êtes connecté en tant qu'administrateur, CiviCRM est affiché comme élément de menu sous "Composants".


Création de lien de menu pour CiviCRM
-----------------------------------------------
Le contenu de CiviCRM peut être affiché sur votre site Web de deux manières différentes. La façon principale est de créer un élément de menu spécifique qui affichera les données de CiviCRM. Dans le menu administrateur de Joomla!, naviguez jusqu'à **Menu principal-> Ajouter un lien de menu**.

![image](/img/Joomla-lien-menu.PNG)

Dans cet écran sélectionner "type de lien de menu". Un nouvel écran affichera  les options ci-dessous  en cliquant sur Civicrm. 

![image](/img/Joomla-type-lien-menu.PNG)

Sélectionner la page CiviCRM correspondante à ce que vous souhaitez afficher.

- **Contribution Page :** Une contribution spécifique ou une page d'adhésion que vous souhaitez publier sur votre site.
- **Créer des pages de campagne personnelles :** Ce type de lien direct permet aux utilisateurs finaux de créer une page de campagne personnelle liée à une page de contribution spécifique pour la collecte de fonds entre pairs. Par exemple, si vous avez fait un appel de fonds annuel appelé "Support CiviCRM" et que vous vouliez permettre à vos membres de collecter de l'argent en votre nom, vous pouvez créer un élément de menu qui les relient directement
- **Voir la page de campagne personnelle **
- **Recherche personnalisée :** Les recherches des membres peuvent être créées
- **Tableau de bord CiviCRM :** La sélection de cette option permet de montrer à l'utilisateur final toutes ses informations connexes, c'est-à-dire les contributions précédentes, les adhésions actives et périmées, les enregistrements d'événements, etc. Lors de la sélection du tableau de bord CiviCRM, vous assurez-vous que le niveau d'accès pour cet élément de menu est défini comme Enregistré parce que CiviCRM doit savoir à qui afficher exactement les informations. Ainsi, l'utilisateur final en se connectant pourra voir toutes les informations spécifiquesle concernant
- **Calendrier des événements:** Cette option affiche tous vos événements actuels et les place dans une vue d'agenda pour votre utilisateur final.
- **Page d'information sur l'événement :** Ce type d'élément de menu fournit les informations récapitulatives d'un événement que vous avez sélectionné et fournit un lien pour s'enregistrer directement.
- **Liste des événements :** Affiche tous les événements à venir dans un format de liste. Vous avez la possibilité de trier par colonnes, mais il n'y a pas de fonctionnalité de recherche par défaut sur la liste des événements.
- **Formulaire d'inscription à l'événement:**
- **Liste des participants :** Si vous avez activé une liste de participants pour un événement spécifique, vous pouvez afficher qui assistera à votre événement en sélectionnant cette option.
- **Abonnement à la liste de diffusion :** Si vous avez configuré des groupes en tant que listes de diffusion et que vous avez défini la visibilité publique, les utilisateurs finaux peuvent s'inscrire à directement à ces listes de diffusion.
- **Formulaire de création de profil :** Vous pouvez collecter des informations complémentaires sur vos visiteurs
- **Formulaire d'édition de profil :** Si un utilisateur final est connecté à votre site et que vous présentez un formulaire d'édition de profil, vous pourrez visualiser les informations que votre organisation a enregistrées. En plus de cela, ils pourront modifier cette information et l'enregistrer dans CiviCRM. Par exemple, si vous présentez le profil **Nouveau Individual** sur votre site Web en tant que formulaire de modification de profil, l'utilisateur final connecté aura alors la possibilité d'afficher et de mettre à jour son prénom, son nom et son courrier électronique et l'enregistrer dans votre instance CiviCRM.
- **Formulaire de recherche de profil :** Si vous avez configuré un profil en tant que formulaire ou répertoire autonome, vous pouvez autoriser l'utilisateur final la recherche dans votre base de données via ce profil spécifique. Par exemple, si vous souhaitez fournir un répertoire de vos membres au public, vous pouvez créer un groupe appelé Membres, puis créer un profil qui limite les résultats de la recherche uniquement aux personnes ou organisations de ce groupe.
- **Formulaire de vue du profil:** Ce type d'élément de menu vous permet d'afficher les informations que vous avez enregistrées pour un utilisateur connecté. Par exemple

Niveau d'accès sur les liens de menu de CiviCRM
-------------------------------------------

Certains des types d'éléments de menu ci-dessus nécessitent que l'utilisateur final soit connecté à votre site afin que CiviCRM puisse savoir quelles informations d'enregistrement de contact soient présentées. Par exemple, si John Smith vient sur votre site Web et navigue sans être connecté et que vous ayez spécifié le **Formulaire de vue du profil**  avec un niveau d'accès public, CiviCRM ignorera complètement que John Smith est sur votre site et ne pourra donc lui retourner ses informations personnelles. Dans ce cas, CiviCRM présenterait l'erreur suivante:

![image](/img/z_sprint14_wordpress_error.png)

Pour chaque utilisateur Joomla!, CIVICRM crée un contact correspondant. Ainsi, lorsque quelqu'un se connecte à Joomla! avec ses  informations d'identification, CiviCRM peut rechercher les informations de contact à afficher. Les types d'élément de menu CiviCRM suivants nécessitent la connexion d'un utilisateur final à Joomla!. Lors de la création de ces types spécifiques, il doit y avoir un niveau d'accès minimum défini sur "Enregistré".

- Formulaire d'édition de profil
- Formulaire de vue de profil
- Tableau de bord CiviCRM

Des modules complémentaires sont disponibles pour étendre et modifier le comportement CiviCRM. Cependant, les intégrateurs de Joomla ont un accès complet aux API et au système de connexion CiviCRM, et il existe un certain nombre d'outils tiers conçus pour résoudre des problèmes spécifiques et faciliter les personnalisations.
 
Pour plus d'informations, les développeurs peuvent se référer à la liste des modules tiers sur le wiki :

[http://wiki.civicrm.org/confluence/display/CRMDOC/Joomla!+Extensions+for+CiviCRM+(3rd+party)](http://wiki.civicrm.org/confluence/display/CRMDOC/Joomla!+Extensions+for+CiviCRM+%283rd+party%29)

 ... ainsi que sur le Guide de développement :
 
[http://wiki.civicrm.org/confluence/display/CRMDOC/Develop](http://wiki.civicrm.org/confluence/display/CRMDOC/Develop)
