Jetons, fusions et publipostages
================================

Vous pouvez utiliser les données stockées dans votre base CiviCRM pour paramétrer des fusions et des publipostages de courriers, qu'ils soient électroniques ou imprimés (lettres et étiquettes). Cette fonctionnalité s'appuie sur le principe des jetons, qui représente chacun un élément de la base de données. Ce chapitre vous explique comment ces derniers fonctionnent et comment les utiliser pour générer du matériel imprimé.

Jetons
------

Les jetons dans CiviCRM sont l'équivalent des champs de fusion de courrier. Cela signifie qu'il est possible d'insérer des informations provenant de la base de donnée dans un courriel ou une lettre qui soient propres à chaque destinataire. Par exemple, utilisez le jeton Postal Greeting pour inclure une formule de salutation qui corresponde à chaque destinataire de votre document PDF. La plupart des champs de contacts, y compris les champs personnalisés, peuvent être utilisés en tant que jetons. Vous pouvez voir ceux qui sont disponibles en cliquant sur le lien **Insérer un jeton** dans le coin en haut à droite de votre éditeur de message.

Si la plupart des jetons affichent une donnée de la base, d'autres sont conçus pour remplir une tâche particulière dans les courriels, tels qu'un lien vers une page de désinscription. Certains jetons ne sont disponibles que pour la diffusion massive de courriel, tel que celui fournissant un lien vers la page en ligne du message. 

![image](/img/Tokens-4.5.png)

### Jeton de contrôle

Un jeton particulièrement utile est le jeton de contrôle (checksum). Ce jeton vous permet de fournir aux destinataires un lien vers un formulaire de contribution, profil, pétition et inscription à un événement avec des champs pré-remplis avec leurs données personnelles de contact.

Seuls les champs de contact et les actions peuvent être insérés dans vos courriels par l'intermédiaire des jetons. Les données associées, telles que le nom d'un événement pour lequel le contact est inscrit, ne peut être affiché. Toutefois, vous pouvez toujours fournir un lien vers un tableau de bord fournissant tous les détails dont la personne a besoin (une fois cette dernière connectée à CiviCRM).

Vous trouverez de plus amples informations sur le jeton de contrôle à cette page : [http://wiki.civicrm.org/confluence/display/CRMDOC/Tokens](http://wiki.civicrm.org/confluence/display/CRMDOC/Tokens).

### Jetons personnalisés

Il est également possible d'utiliser des jetons personnalisés créés par un développeur (par exemple, le montant total des contributions d'un contact). Pour en savoir plus à ce sujet, vous pouvez jeter un oeil au wiki :
[http://wiki.civicrm.org/confluence/display/CRMDOC/Tokens](http://wiki.civicrm.org/confluence/display/CRMDOC/Tokens).

Une autre tâche pour un développeur est de pouvoir créer une condition if/then pour la fusion de courrier. Cela est possible en utilisant le langage smarty template décrit ici : [http://www.smarty.net/docs/en/language.function.if.tpl](http://www.smarty.net/docs/en/language.function.if.tpl).
