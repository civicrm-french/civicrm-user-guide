Gestion des tarifications
=====================
Ce chapitre décrit comment configurer la gestion des tarifications afin que vos contacts puissent:
 
-   S'inscrire à plusieurs sortes d'adhésion en même temps.
-   S'inscrire à plusieurs adhésions en une seule transaction (par exemple, adhésions nationales et locales).
-   Sélectionner des options publiques, non membres, telles que les brochures d'information lorsqu'elles souscrivent à une adhésion.

Voici un exemple de la façon dont une tarification d'adhésion, qui offre toutes ces options, peut ressembler:

![image](/img/4.5_membership_price_sets_complete_price_set.PNG) 
 
La tarification **du Club de natation de Donwell Swim** se compose de cinq **champs de tarif** : 
Adhésion à l'association nationale, Adhésion annuelle au club, Boutique du club, Billets de tombola et dons.

Il y a deux types d'adhésions possible:

![image](/img/4.5_membership_price_sets_types_1.PNG) 
 
Ces types d'adhésions doivent être définis avant de créer la tarification.
(Voir le chapitre *Définition des adhésions*)..

Vous devez définir tous les types financiers dont vous aurez besoin avant de pouvoir créer une tarification. (Reportez-vous à la section *Contributions* pour obtenir des informations sur les types financiers)

La tarification des adhésions peut être utilisée dans les pages de jointure ou de renouvellement en ligne ou pour les nouvelles inscriptions de membres traitées manuellement via le système de back office CiviCRM. Cependant, vous ne pouvez pas l'utiliser pour des renouvellements traités manuellement. Chaque adhésion doit être renouvelée individuellement (voir le chapitre *Renouvellements*) et en plus, vous devrez créer un ensemble de prix de contribution composé des éléments de prix que vous proposez aux public non membres . En outre, vous ne pouvez pas combiner des adhésions avec renouvelement automatique et des adhésions sans renouvellement automatique ou avec des éléments non membres.

Les tarifications peuvent être configurés de plusieurs façons. Vous devez toujours tester une tarification définie avant de l'utiliser directement sur votre site afin de vous assurer que vous l'avez configurée de la manière qui vous convient le mieux.

Créer une nouvelle tarification 
------------------------

![image](/img/4.5_membership_price_sets_new_new_price_set_1.PNG) 

1.  Menu **Adhésions> Nouvelle tarification** ou **Administrer > CiviMember> Nouvelle tarification**.
2.  Entrez le nom de cette tarification **Titre**. Ce nom sera affiché à la fois au public dans le cadre du tarif proposé et au personnel administratif lorsqu'il doit choisir entre les ensembles de tarifs. Assurez-vous que le nom soit suffisamment descriptif pour les deux types d'utilisateurs.
3.  Utilisé pour : choisir  **Adhésion**
4.  Définissez le **Type d'opération par défaut** Le choix que vous faites a des implications comptables. Vous devez vous référer à la section *Contributions* pour plus d'informations.
5.  Ajoutez un texte d'aide pré ou post-formulaire si vous le souhaitez.
6.  Assurez-vous que cette tarification soit active et **Enregistrer**

Un formulaire  s'affiche ensuite pour créer le premier **Champ de tarif** de votre **Tarification**

![image](/img/4.5_membership_price_sets_new_new_price_field_1.PNG) 

### Creation d'un nouveau champ de tarif 

1.  Entrez un nom dans **Intitulé du champ**. Ce nom sera affiché au public. 

2.  Selectionnez **Type de champ de saisie**. Il y a 4 types d'entrée disponibles pour les tarifs

    -   **Quantité/texte numérique:** Permet de définir une unité **Prix**
        Lorsque le jeu de tarif est affiché, il affiche une zone de texte où une quantité peut être saisie. La quantité saisie est multipliée par le prix unitaire pour calculer le montant.
    -   **Selection:** Affiche un menu déroulant où une option peut être sélectionnée.
    -   **Bouton radio:** Affiche plusieurs options dans une liste, une option peut être sélectionnée.    
    -   **Cases à cocher:** Affiche plusieurs options dans une liste. Des sélections multiples sont autorisées.

   Chacun des ces types d'entrées sera utilisé dans un exemple de ce chapitre 

3.  **Type d'opération** : Sera réglé sur **Type financier par défaut** choisi lorsque ce tarif a été créé. Vous pouvez remplacer cette valeur si nécessaire.

4.  **Afficher le montant ?** : Ceci affiche le montant du tarif à côté de l'étiquette. Si votre étiquette de champ inclut le montant, cela peut être décoché. Sinon, il doit rester coché.

5.  **Numéro d'ordre**, **Aide à propos du champ**, **Obligatoire** et **Actif le** sont suffisament explicites et ont une aide adéquate fournie sur le formulaire.

6.  **Actif le** et **Expire le** :  peuvent être réglés de sorte que le champ de tarif ne soit pas visible jusqu'à la date **Actif le**, et non visible après la date **Expire le** ou n'est que visible entre les dates **Actif le** et **Expire le**.
-  *Par exemple, vous pouvez utiliser ces champs pour augmenter le tarif à 12h00 le 1er janvier 2017 en définissant le tarif avec les anciens tarifs à **Expire le** 12/01/2017 12:00 am et le champ de prix avec les nouveaux prix soit **Actif le**  1/12/2017 12:00 am.***

7.  La **Visibilité** peut être définie sur **Public** (visible sur votre site Web pour ceux qui ont accès à la page d'inscription de membre) ou **Admin** (visible uniquement en back-end et uniquement pour les utilisateurs avec les autorisations appropriées).

Conditions d'adhésion multiples :
-------------------------
La configuration du champ "National Membership" affiche le type de champ **Radio** ce qui illustre comment vous pouvez autoriser les contacts à s'inscrire à plusieurs types d'adhésions en même temps et .

![image](/img/4.5_membership_price_sets_multi-term_1.PNG) 

Dans le champ **Type d'adhésion**, vous sélectionnez l'option souhaitée dans une liste déroulante parmi les types d'adhésion que vous avez configuré. Lorsque vous sélectionnez un type d'adhésion spécifique, **le nombre de périodes** est rempli automatiquement à 1, **Montant** et **Type financier** sont automatiquement remplis en fonction de la définition du **Type d'adhésion**. Toutes ces valeurs peuvent être modifiées au besoin. *Le type d'adhésion de l'Association nationale des associations a une durée de 1 an avec un droit minimum de 100 $.*

La définition du **Nombre de périodes** à 2 donnera : 2 ans d'adhésion. ***L'étiquette*** devra être modifiée si vous avez plus d'une option car chaque option doit avoir une ***étiquette*** différente. Le **Montant** peut être modifié à la valeur souhaitée. Cela vous permet d'offrir une concession et des frais standard pour le même nombre de périodes.

Comme nous n'avons pas inclu le tarif de chaque option dans son **Label**, nous devrions avoir **Afficher le Montant?** cochée.

Définir un champ de tarif de cette façon réduira le nombre de types d'adhésion que vous devez créer. Vous n'avez besoin que d'un type d'adhésion à l'Association nationale d'un an avec un minimum de 100 $ pour ce champ de tarif, au lieu de trois types d'adhésion. Cependant, vous devez être conscient que vos membres ne pourront pas renouveler automatiquement si vous utilisez ce type de configuration pour plusieurs périodes.

Membre de plusieurs organisations
----------------------------------------

En plus des frais d'association nationale, les contacts peuvent s'inscrire à l'adhésion au club de natation. Le type de champ **Selection** a été choisi pour ce champ.

![image](/img/4.5_membership_price_sets_second_organisation_1.PNG) 

Rappel, lorsque vous sélectionnez un type d'adhésion spécifique dans une liste déroulante, **le nombre de périodes** est rempli automatiquement à 1 , **Montant** et **Type financier** sont auto-remplis en fonction de la définition du type d'adhésion. Vous pouvez modifier l'une de ces valeurs comme vous le souhaitez.
Comme nous n'avons pas inclu le tarif de chaque option dans son **Label**, nous devons avoir **Afficher le montant?** coché.

La combinaison des deux champs de tarif décrits jusqu'à présent permettra à quelqu'un de s'inscrire pour un minimum de 1 et un maximum de 2 adhésions. Rappelez-vous que les deux membres doivent être liés à deux organisations différentes car un contact ne peut avoir qu'une seule adhésion active avec une organisation spécifique. (Voir le chapitre *Définition des membres* pour plus d'informations.)

Champs de tarif hors adhésion
-----------------------------

Vous pouvez également configurer les champs de tarif pour offrir des services supplémentaires, des abonnements ou d'autres options au public non membres.

- Il existe trois champs de prix hors adhésion dans notre exemple. Le premier offre une sélection de matériel de natation de marque club. Le type de champ **checkbox** permet aux personnes de choisir plusieurs éléments parmi les options proposées.

![image](/img/Membership%20Pricesets%20non-member%20field_1.PNG) 

Comme ce sont des produits plutôt que des adhésions, les champs **Type d'adhésion** et **Nombre de périodes** restent vides. Vous devez définir le **Label**, **Montant** et **Type financier** pour chaque option.

Comme nous n'avons pas inclu le tarif de chaque option dans son **Label**, nous aurons **Afficher le montant?** coché.

Si vous regardez les captures d'écran précédentes des trois champs de prix développés jusqu'à présent, vous devriez remarquer qu'ils contiennent tous les mêmes champs bien qu'ils correspondent à trois types de champs de saisie différents ; **Radio** et **Sélection**. Les types d'entrée sont interchangeables, vous permettant de choisir une seule option et peuvent être utilisés pour les options d'adhésion ou de non-adhésion. **Case à cocher** doit être utilisé si vos contacts sont autorisés à choisir plus d'une option dans un champ de prix unique. Il peut également être utilisé pour les options d'adhésion ou de non-adhésion.

Le quatrième type de champ de saisie est **Texte/Quantité numérique** et il ne peut être utilisé que pour des options hors adhésion. Avec ce type de champ, vous incluez habituellement le **prix unitaire** de l'article offert dans l'étiquette. Comme indiqué dans l'exemple suivant ou dans l'aide du **champ**. Cela signifie que **Afficher le Montant?** ne devrait pas être coché.

![image](/img/4.5_membership_price_sets_raffle_dates_fields_used.PNG)

Ce qui affichera : 

![image](/img/membership_price_set_raffle_preview_1.PNG)

Ce champ de prix ne sera visible que entre les dates **Actif le** et **Expire le**  nous permettant de nous assurer que les tickets de tombola ne peuvent être achetés que pendant la période de vente autorisée selon les règlements en vigueur.

Le champ de prix final est configuré pour permettre aux visiteurs de donner un don. Notez que le **Prix unitaire** est égal à 1 et qu'il n'est pas inclus dans l'intitulé du champ bien que le symbole de la devise y soit (€). La case **Afficher le Montant?** n'est pas coché. C'est la meilleure configuration pour permettre de choisir le montant des dons par les visiteurs.

![image](/img/4.5_membership_price_sets_donation.PNG)

Pour rappel, voici comment tous ces champs apparaissent sur l'écran final:

![image](/img/Membership%20priceset%20final.PNG) 
