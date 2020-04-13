Définition des adhésions
====================

Ce chapitre décrit comment configurer un ou plusieurs types d'adhésion que vous pouvez utiliser pour gérer les membres de votre organisation. Cela explique également le concept des statuts d'adhésion et la façon dont votre organisation peut les utiliser pour définir un cycle de vie d'adhésion.

Types d'adhésions
----------------

Les types d'adhésion sont un élément de base pour la gestion des membres dans CiviCRM. En règle générale, une organisation mettra en place un type d'adhésion pour chacune des différentes adhésions qu'elles offrent. Pour les structures d'adhésion les plus simples, un type d'adhésion peut suffire. Pour des structures d'adhésions plus complexes, il est peut-être nécessaire d'utiliser plusieurs types d'adhésion. Par exemple, une organisation peut définir trois types d'adhésion pour les membres «Actifs», «bénévoles» et «Honoraires». Une organisation peut aussi choisir d'utiliser les types d'adhésions comme des abonnements ou souscriptions à leurs différentes publications, gratuites ou payantes.

Plusieurs options peuvent être configurées pour un type d'adhésion, et celles-ci sont paramétrées en fonction du formulaire de type d'adhésion. Une compréhension solide des options vous aidera à décider du nombre de types d'adhésion dont votre organisation a besoin et de la manière dont elles doivent être configurées.

Dans ce chapitre, nous couvrirons la configuration la plus courante pour les types d'adhésion. Certaines organisations, avec des structures d'adhésion plus complexes, ont des exigences qui vont au-delà de ce qui est disponible avec les types d'adhésion seuls. 
Ces organisations trouveront dans le chapitre sur **les Ensembles de prix d'adhésion** la flexibilité supplémentaire dont ils ont besoin. Les ensembles de prix d'adhésion sont un sujet avancé, ils sont expliqués dans le chapitre "*Ensembles de prix d'adhésion*".

Si vous rencontrez des problèmes pour modéliser votre structure d'adhésion dans CiviCRM, demandez sur le forum CIVICRM la réponse aux problèmes que vous rencontrez. Il peut y avoir d'autres façons de modéliser vos données, ou des modifications simples que vous pouvez apporter au comportement de CiviCRM pour mieux répondre à vos besoins.

Pour démarrer la configuration sur les types d'adhésions :

1.  Allez à : **Adminitrer>CiviMember>Types d'adhésion**.
2.  Selectionner : **Ajouter un type d'adhésion**

![image](/img/new-membership-type.png)

-   **Nom**:
Le nom est affiché dans tout le système, tant sur les pages publiques que dans les pages de backend. Passez donc un peu de temps à penser à un nom qui est approprié aux deux publics. Il peut être changé ultérieurement (bien que cela puisse entraîner un travail supplémentaire dans la mise à jour des reçus d'adhésion s'ils ont été personnalisés en fonction des noms d'adhérents)

- **Description**:
Ceci n'est pas obligatoire, mais vous pouvez indiquer à quel type de contacts il est destiné, etc.

- **Organisation pour l'adhésion**: 
CiviCRM est capable de gérer les adhésions de plusieurs organisations, c'est-à-dire qu'un club sportif local pourrait utiliser une seule instance de CiviCRM pour gérer les adhésions d'un club de tennis, d'un club de golf et d'un club de judo.
Pour cette raison, lors de la définition d'un type d'adhésion, vous devez spécifier l'organisation pour laquelle le contact deviendra membre. Chaque organisation doit déjà exister en tant que contact dans CiviCRM. De nombreuses d'organisations souhaitent seulement modéliser les adhésions de leur propre organisation. Dans ce cas, vous pouvez simplement choisir l'organisation par défaut.

    Si vous souhaitez activer les inscriptions ou les renouvellements en ligne, le modèle de données CiviCRM exige qu'un contact ne puisse avoir qu'une seule adhésion active avec une seule organisation à un moment donné. Cependant, certaines organisations peuvent vouloir que les gens aient deux membres ou plus à la même organisation simultanément. Par exemple, une organisation axée sur la santé des enfants pourrait vouloir offrir une adhésion aux parents qui comprend un magazine pour les parents et une adhésion aux professionnels de la santé qui comprend un journal professionnel et des réductions pour les événements de formation. Les parents qui sont des professionnels de la santé peuvent vouloir les deux adhésions.
    Une "solution de contournement" pour cela, consiste à créer des organisations "fictives" pour chacune des adhésions simultanées possibles. Dans ce cas particulier, nous devrions créer une organisation supplémentaire pour les professionnels de la santé. Notez que vous ne devez pas exposer l'organisation fictive à vos membres sur le site, uniquement pour des raisons administratives.
   
-   **Cotisation minimum**: Pour des adhésions gratuites, vous devez entrer 0 (zéro) dans ce champ.
Sinon, vous devez entrer le montant minimum qui doit être payé pour ce type d'adhésion. La raison pour laquelle nous appelons ce champ le montant *minimum* est que nous avons une option pour encourager les gens à payer plus que le minimum pour une adhésion s'ils le souhaitent.

-   **Type d'opération**: Le type financier par défaut pour un type d'adhésion est **Cotisations**

Le type par défaut "Cotisation" convient à de nombreuses organisations. Toutefois, si vous avez des besoins comptables plus complexes, vous pouvez spécifier différents types financiers qui vous permettront de comptabiliser différents paiements d'adhésion de différentes façons. Pour plus de détails, consultez le chapitre *Intégration comptable* dans la section *Contributions*. Si vous avez besoin de plus de contrôle fin par rapport aux types financiers, vous voudrez peut-être regarder *les jeux de prix*.

    Notez que le type financier peut être remplacé par des pages d'inscriptions 
    spécifiques pour des contacts publics, ainsi que lors de l'enregistrement 
    d'une adhésion dans le back-end. CiviCRM gère les adhésions payées en liant 
    les enregistrements d'adhésion aux documents de contribution. Un dossier 
    d'adhésion documente la "relation" d'un contact avec l'organisation, tandis
    que la transaction financière correspondante indique la valeur monétaire 
    associée à cette adhésion..
    
![image](/img/membership_contribution.png)

    CiviCRM respecte cette distinction en enregistrant le dossier d'adhésion
    sous l'onglet adhésion, l'opération financière sous la rubrique Contribution,
    et crée un lien entre les eux enregistrements

-   **Option de renouvellement automatique**: CiviCRM offre une fonctionnalité de renouvellement automatique qui soumettra automatiquement une transaction répétée au processeur de paiement lorsque l'adhésion actuelle expire. Cela peut être un bon moyen de retenir les membres. Cette fonctionnalité n'est pas disponible pour tous les processeurs de paiement, de sorte que vous devrez vérifier si le vôtre est configuré pour les paiements récurrents avant de sélectionner l'une des options de renouvellement automatique ici. Vous devrez sélectionner et configurer un service de paiement supporté (Authorize.net, PayPal Pro ou PayPal Website Standard) afin de permettre aux membres de renouveler automatiquement leur adhésion.  Pour plus d'informations sur les processeurs de paiement, voir

[http://wiki.civicrm.org/confluence/display/CRMDOC/Payment+Processors.](http://wiki.civicrm.org/confluence/display/CRMDOC/Payment+Processors)

    Vous pouvez autoriser ou nécessiter un renouvellement automatique pour un type d'adhésion.
    Toutefois le renouvelement automatiquement des adhésions ne peut être permis que pour les 
    adhésions qui ont un une durée d'un an ou moins.

-   **Unité de durée pour le type d'adhésion**: Dans le champ **Durée** vous devez entrer 
le nombre de jours, de mois ou d'années auxquels votre adhésion sera active chaque fois que 
quelqu'un s'inscrit ou renouvelle. (par exemple : 30 jours, 2 mois, 5 ans, à vie)

-   **Periode type**: Les options pour le type de période sont Glissante et Fixe.
      **Glissante**: Les adhésions commencent le jour où le membre s'inscrit.
      **Fixe**: Les adhésions commencent à la date de calendrier particulière que vous avez spécifiée.

         Lorsque vous définissez le type de période sur la liste, des champs supplémentaires 
         apparaîtront selon la durée que vous avez spécifiée. 
  
    Si la durée est spécifiée en **années**, deux champs supplémentaires seront affichés:

    -  Le champ **Fixed Period Start Date** est la date à laquelle toutes les adhésions commencent 
    (par exemple, 1er janvier ou 15 avril).

    -  Le champ **Fixed Period Rollover Date** Détermine la date de fin de l'adhésion 
    lorsqu'une personne s'inscrit partiellement au cours de votre année d'adhésion. 
    Son utilisation est mieux illustrée par un exemple : Considérez un type d'adhésion 
    avec **Durée** d'un an, et **Date de début de la période fixe** du 1er janvier 
    et **Date de retour de la période fixe** du 1er septembre

     - Toute personne ayant signé entre le 1er janvier 2017 et le 
         31 août 2017 aura une date de fin d'adhésion au 31 décembre 2017.
     - Toute personne qui s'inscrit à compter du 1er septembre 2017 aura 
         une date de fin d'adhésion au 31 décembre 2018. (c.-à-d. Ils auront 
         jusqu'à 15 mois d'adhésion pour le prix de 1 an).
         
Si la durée est spécifiée en **mois** un champ supplémentaire sera affiché :
    
    - La "Date de prorogation de la période fixe" détermine si la durée de l'adhésion 
    commence au début du mois civil ou au début du mois calendaire suivant. 
    
    Considérez un type d'adhésion de 6 mois avec "Date de prorogation de la période fixe" réglé à 15:
    - La "Date de prorogation de la période fixe" détermine si la durée de l'adhésion 
    commence au début du mois civil ou au début du mois calendaire suivant. 
    
    Considérez un type d'adhésion de 6 mois avec "Date de prorogation de la période fixe" réglé à 15:
       
        - Quelqu'un qui s'inscrit entre le 1er et 14 janvier aura une fin d'adhésion au 30 juin

        - Quelqu'un qui s'inscrit entre le 15 et le 31 janvier aurait une fin d'adhésion au 31 juillet.
        
     Exemple: si "Durée = 12 mois", "Type de période = Fixe, et "Date de prorogation...= 1", 
     alors quiconque inscrit en août 2017 aura une date d'expiration du 31 août 2018.
   

-   **Type de relation** : les membres peuvent être **"héritiers"** d'un contact à l'autre. Exemple : une organisation commerciale professionnelle enregistrée en tant que membre (principal) veut que les employés de la société reçoivent les avantages de l'adhésion.

Afin de supporter cette fonctionnalité, nous définissons un **Type de relation** pour lequel le statut d'adhérent peut être attribué automatiquement aux contacts en relation
     - L'écran d'aide contextuelle donne des exemples de types de relation à sélectionner pour cette fonctionnalité.
     - Une fois que vous avez sélectionné un type de relation, vous entrez un nombre dans le champ **Max de relations** pour définir le nombre maximum d'adhésions héritées liées à chaque membre principal. Il serait utile, dans l'exemple ci-dessus, de limiter le nombre d'employés qui peuvent devenir membres en raison de leur emploi à 10 maximum.
   
 ![image](/img/Membership_relationship_type.png) 

    Avec les adhésions héritées, nous distinguons le membre principal et les membres 
    qui héritent de leur appartenance en raison de leur relation avec le membre principal.
    
- **Visibilité**: Choisir **Public** signifie que ce type d'adhésion pourra être sélectionné pour être inclus sur les formulaires d'inscription en ligne. Si certains types d'adhésion ne doivent être gérés que manuellement par un administrateur (par exemple, adhésions honoraires et à vie), vous devez choisir **Administrateur** ici.
- **Order**: Détermine si ce type d'adhésion apparaît dans une liste d'options déroulantes des types d'adhésion ou sur les pages d'inscription des membres.
- **Activé**: Si vous avez des types d'adhésion qui ne sont plus d'actualité ou qui ne sont pas encore disponibles, vous pouvez désactiver cette case. Cela éliminera ces adhésions de l'interface utilisateur. Il ne supprimera pas les données d'adhésion et ce type d'adhésion pourra être réactivé à une date ultérieure.


Règles des statuts d'adhésion 
-------------------------
Les règles de statut d'adhésion vous permettent de déclencher la prise en charge initiale d'une adhésion. Ces règles sont définies en fonction de la date d'inscription, de début ou de fin de l'adhésion. Examinons d'abord ce que signifient ces dates.

Les membres ont trois dates principales: la date d'inscription, la date de début et la date de fin. La **date d'inscription** est la date à laquelle le contact s'est inscrit ou est inscrit en vue d'une adhésion à votre organisation. À moins qu'elle ne soit modifié manuellement, cette date ne changera jamais. La **date de début** est la date où la *période continue* de l'adhésion a commencé. La **date de fin** est le dernier jour de l'adhésion actuelle.

Par défaut, les statuts d'adhésion sont les suivants:

-   **En attente:** quelqu'un qui a demandé l'adhésion mais n'a pas payé.
    Ce statut ne peut pas être modifié manuellement, ce qui signifie que vous ne pouvez pas modifier le statut "En attente" vers   "Nouveau", sauf si vous mettez à jour le dossier de contribution associé. 
    Par exemple, si vous avez l'option "paiement plus tard" activée pour l'adhésion de Joe Smith, le statut de son adhésion ne sera changé en "nouveau" jusqu'à ce que vous modifiez l'état de cotisation de son paiement à "Complète".
-   **Nouveau**: le membre vient de s'inscrire pour une adhésion ou un paiement en attente est régularisé. Par défaut, le délai est de 3 mois après la date de début de l'adhésion.
-  **Courant**: les nouveaux membres passent à ce statut après la fin de la nouvelle période. Comme on pouvait s'y attendre le statut actuel dure jusqu'à la date de fin d'adhésion.
- **Grace**: lorsque la fin de la période d'adhésion est atteinte, quelqu'un qui n'a pas renouvelé l'adhésion est inscrit avec ce statut pour une période de temps. Ils sont toujours comptés comme membres.   
- **Expiré**: lorsque le délai de grâce expire, le membre passe à ce statut et n'est plus considéré comme membre.
- **Décédé**: ce statut conserve un dossier de contact "décédé" dans le système, mais supprime le contact de toutes communications. Cet état est défini automatiquement en fonction du drapeau décédé d'un contact.

Vous pouvez forcer un statut d'adhésion en sélectionnant **Forcer le statut** sur un enregistrement d'adhésion et en choisissant un statut. Donc, une adhésion avec une modification de statut restera dans ce statut et ne sera pas mise à jour conformément aux règles d'état de l'adhésion décrites ci-dessus.

Sous **Administer> CiviMember> Règles des statuts d'adhésion**, vous trouverez un résumé des règles d'état existantes.

![image](/img/z-sprint14-membership%20status.png)

Pour décider quel statut doit être appliqué, CiviCRM cherche à voir si l'adhésion a un statut prioritaire. Si c'est le cas, cela s'applique à ce statut. Si ce n'est pas le cas, le système liste les statuts en commençant par le haut de la page "Règles de statut d'adhésion" jusqu'à ce qu'il en trouve un qui est valide. C'est-à-dire, si la date du jour se situe entre le début et la fin de l'état de l'adhésion en haut de la liste. Si c'est le cas, il applique ce statut, sinon il passe au prochain état et répète ce processus jusqu'à ce qu'il trouve un état qui correspond.

Lorsque vous modifiez ou ajoutez un nouveau statut de membre, le formulaire suivant apparaît.

![image](/img/Fr_statut_adhesion.png) 

Vous pouvez ajouter de nouveaux statuts et modifier les statuts existants (à l'exception de En attente et Décédé) en utilisant ce formulaire. Pour créer un nouveau statut, vous devez préciser quand le statut doit commencer et arrêter. Cela se fait par rapport à un événement d'adhésion (c'est-à-dire la date d'inscription, la date de début ou la date de fin). Par exemple. «Un mois après la date de début de l'adhésion serait configuré avec «date de début» et «1 mois» ou «cinq jours avant la date de fin d'adhésion» serait configuré avec «date de fin» et «-5 jours».

Vous pouvez spécifier également si les contacts avec ce statut d'adhésion doivent être considérés comme des membres ou des non-membres en cochant ou en désélectionnant la case à cocher "L'adhésion actuelle". (Il en résulte un Oui ou Non dans la colonne Membre sur la page récapitulative des règles de statut.) 
- Renouveler les contacts avec un statut qui les définit affectera une date de fin d'adhésion existante prolongée par la durée du renouvellement. 
- Renouveler les contacts avec un statut qui les définit comme non-membres leur donnera une nouvelle date de début en vue de leur adhésion et une date de fin en fonction de cette nouvelle date de début.

Maintenir les statuts d'adhésion à jour
----------------------------------------

Lorsqu'une adhésion est ajoutée ou renouvelée, l'état de l'adhésion est défini automatiquement en fonction de vos règles d'état. Par exemple, une adhésion nouvellement créée recevra le statut "Nouveau" par défaut. Si vos statuts d'adhésion ne se mettent pas à jour automatiquement, assurez-vous que le travail **Mise à jour des statuts d'adhésion** est activé et s'exécute au moins une fois par jour.
 -Reportez-vous au chapitre [Travaux programmés](http://booki.flossmanuals.net/initial-set-up/scheduled-jobs) pour les détails de la configuration ou consultez votre administrateur système, le cas échéant.
 
Collecte d'informations supplémentaires sur vos membres
-------------------------------------------------------
Parfois, vous souhaitez collecter des informations supplémentaires sur vos membres. Vous pouvez créer un ou plusieurs ensembles de champs personnalisés pour cela. Les ensembles de champs personnalisés peuvent être créés pour toutes les adhésions ou les types d'adhésion spécifiques. Si les informations que vous souhaitez collecter varient selon le type d'adhésion, vous devez configurer plusieurs champs personnalisés pour les associer aux différents types d'adhésion. (Reportez-vous au chapitre *Champs personnalisés* dans la section *Organiser vos données*

