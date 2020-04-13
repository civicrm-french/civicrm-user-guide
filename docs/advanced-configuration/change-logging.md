Enregistrement
==============

![Screenshot of default logging](/img/configuration-default-logging.png)

CiviCRM conserve une trace des différents changements que vous réalisez sur les contacts, adhésions,activités, etc... Chaque contact possède un onglet de journal des modifications qui est mis à jour automatiquement chaque fois qu'un contact est ajouté ou modifié. Le journal des modifications indique **qui** a modifié l'enregistrement et **quand** la modification a été effectuée. Cette journalisation résumée est activée par défaut et de nombreux utilisateurs trouvent qu'elle est suffisament détaillée.
Une des principales informations manquantes cependant, est de voir  **"ce"**  qui a été changé. Mais "l'enregistrement détaillé" ajoute des informations sur ce qui a changé et fournit de nombreuses autres fonctionnalités

Enregistrement détaillé
----------------------

Une fois activée, la journalisation détaillée permet de suivre toutes les modifications apportées aux données dans CiviCRM. Chaque fois qu'un élément est mis à jour, CiviCRM conserve une historique de:

-   Quelle était la valeur avant
-   Quelle est la valeur actuelle
-   Quand le changement a été fait
-   Qui a fait le changement

Lorsque vous activez l'enregistrement détaillé, (voir écran suivant). vous pouvez consulter les détails de la modification en cliquant sur le côté gauche.

![Change log image](/img/change-log.png)

Cette journalisation s'étend à presque toutes les données existant dans CiviCRM, y compris contacts, adhésions, événements, etc., ainsi que toutes les données des composants de votre installation, telles que les types d'activité, les types de cas, les types de contribution, etc.

Avec la journalisation détaillée activée, toutes les modifications apportées à vos données peuvent être annulées, ce qui signifie que vous pourriez moins faire attention aux modifications indésirables si elles sont effectuées par votre personnel administratif ou par des contacts interagissant via votre site Web - intentionnellement ou accidentellement !

Comme vous pouvez l'imaginer, l'enregistrement de toutes les modifications apportées à la base de données peut entraîner la collecte d'un grand nombre de données et un impact négatif sur votre base de données. Pour cette raison, nous utilisons l'enregistrement par défaut dans CiviCRM et laissons le soin aux administrateurs d'activer la journalisation si tel est le besoin. Avant de décider si vous souhaitez activer la journalisation, vous voudrez peut-être avoir un aperçu d'autres façons dont la journalisation, basées sur la date, se produit dans CiviCRM :

Activités vs. Enregistrement
----------------------------

L'utilisation d'activités pour enregistrer des données dans CiviCRM est souvent utile comme alternative à l'enregistrement journalier. Chaque activité se produisant à un moment spécifique, vous pouvez ainsi afficher l'onglet activité dans un enregistrement de contact comme un journal des modifications apportées à ce contact au fil du temps. Cela ne signifie pas que chaque fois que vous modifiez un contact dans CiviCRM, vous devez enregistrer une activité. Dans certains cas d'utilisation, les données recueillies dans le journal des activités fournissent un journal suffisant des changements effectifs. De plus complété avec d'autres activités enregistrées manuellement cela peut répondre largement à vos besoins de journalisation.

Enregistrements d'adhésion
--------------------------

De la même façon que les activités, l'adhésion est un dossier historique des membres, avec un registre de toutes les contributions versées et de tout renouvellement, etc... Il est probable que cette journalisation spécifique corresponde à vos besoins, vous n'aurez pas donc besoin d'activer l'enregistrement détaillé

Annuler les modifications
-------------------------

L'un des grands avantages de l'activation de la journalisation détaillée est la possibilité de rétablir les modifications que vous apportez à vos données. Pour un grand nombre de champs de contact, nous simplifions cette tâche en affichant un bouton de retour en bas de l'écran qui montre les détails de la modification.

![Screenshot of change log revert](/img/change-log-revert.png)

Cet écran n'est pas disponible pour toutes les modifications de contact, cependant, les données sont toujours affichées. Si vous devez rétablir des données qui ne peuvent pas être renvoyées via l'interface utilisateur, vous devez contacter votre administrateur système ou obtenir l'aide d'une personne qui connaît la fonctionnalité de journalisation détaillée de CiviCRM.

