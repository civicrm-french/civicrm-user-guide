Crédits indirects
============

Les crédits indirects sont un concept familier dans le cas de collectes de fonds, et sont utiles pour une meilleure compréhension des sources de contributions reçues par votre organisation. Ils vous permettent d'attribuer le crédit d'un don à une ou plusieurs personnes qui ne sont pas le donateur.

Types de Crédits indirects
-----------------

Le Crédit indirect de CiviCRM permet aux utilisateurs d'attribuer des types de crédits indirects aux contributions. L'attribution d'un type de crédit indirect réservé ou personnalisé permet aux administrateurs d'attribuer correctement les contributions reçues par le biais d'un ou de plusieurs types de contributions charitables (fonds versés par un donateur, bourses d'études, legs familiaux, etc.) qu'elles soient sollicitées (P2P) ou non.

CiviCRM utilise les types de crédits indirects réservés suivants:

-   En l'honneur de..
-   En mémoire de 
-   Sollicité
-   Page de campagne personnelle
-   Cadeau

Supposons que l'objectif d'un membre très actif de votre organisation était de contacter 10 autres personnes pour obtenir une contribution. Les crédits indirects vous permettent de créditer cette personne et les donateurs réels, sans comptabiliser la contribution deux fois.

Vous pouvez donc utiliser le crédit indirect de CiviCRM pour créditer les parties d'un don à plusieurs personnes.

Dans la capture d'écran ci-dessous, vous pouvez voir que nous avons crédité la contribution de Magan Cooper de 1 500 $ à trois personnes différentes.

![image](/img/soft-credit-donation-1.png)

CiviCRM peut également gérer des scénarios plus complexes. Par exemple, Joe est un membre actif d'une fondation communautaire qui contribue régulièrement à votre organisation. Joe a sollicité une contribution de Jane au nom de la fondation communautaire. Votre organisation recevrait donc un chèque de la fondation communautaire. En utilisant des types de crédits souples, les utilisateurs peuvent attribuer correctement le crédit sans dupliquer les contributions. Dans ce cas:

- La fondation communautaire est le donateur.
- Joe recoit le crédit indirect sollicité.
- Jane recoit le crédit indirect de donateur

Ce scénario est illustré dans la capture d'écran ci-dessous.

![image](/img/soft-credit-donation-2.png)

En plus d'enregistrer les crédits indirects, nous pouvons également en faire le rapport. Le rapport détaillé des contributions comporte des colonnes optionnelles qui en affichent les détails. Lorsque cette case est cochée, quatre colonnes supplémentaires s'affichent dans CiviReport, et peuvent être utilisées pour afficher les informations sur le crédit indirect.

![image](/img/z_sprint14_contributions_soft_credit.PNG)

Section remerciements et profils
---------------------------------

Lorsque vous créez une page de contribution, vous avez la possibilité d'autoriser vos utilisateurs finaux à faire une contribution pour le compte d'une personne remerciée. Pour ce faire, vous devez sélectionner la case à cocher **Section Remerciements activée**

Cela affichera des champs supplémentaires qui vous permettront de spécifier les types d'honneur et le profil à inclure dans cette section.

![image](/img/z-sprint14_honoree_section.PNG)

Une fois enregistrés, les utilisateurs finaux pourront entrer des informations honorifiques pour les contributions en ligne. CiviCRM vérifiera si la personne remerciée existe dans CiviCRM en utilisant déjà les règles de vérification des doublons par défaut sur votre site, si un doublon n'est pas trouvé, un nouvel enregistrement de contact sera créé. Un crédit indirect sera ajouté au dossier de contact du candidat.

![image](/img/soft-credit-honoree-info.png)

Crédits indirects et Pages de Campagne Personnelles
----------------------------------------

Le concept de crédit indirect est étroitement lié à [personal campaign page](../contributions/personal-campaign-pages).
Lorsque quelqu'un fait un don sur une page de campagne personnelle, son don est crédité au propriétaire de la page de la campagne personnelle.

