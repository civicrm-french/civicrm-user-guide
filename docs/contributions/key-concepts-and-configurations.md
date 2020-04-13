# Concepts clés et configurations
---------------------------------

Cette section explique les concepts clés de CiviContribute et décrit la configuration nécessaire à sa performance.

Avant de commencer, il est utile d'énumérer les types de contributions que votre organisation reçoit (ou souhaite recevoir) et bien identifier celles que vous souhaitez gérer en utilisant CiviCRM.

## Types financiers, comptes financiers et comptes comptables

Les organisations qui utilisent CiviCRM ont des besoins différents en termes de compte rendus financiers. Certains veulent juste savoir le total des dons ou le montant total des adhésions enregistrées dans CiviCRM, alors que d'autres veulent être en mesure d'exporter un ensemble complet d'opérations financières en parties double dans leur logiciel de comptabilité.

CiviCRM répond à ces besoins en utilisant des **types financiers** pour simplifier la complexité de la comptabilité en parties double aux personnes non initiées, tout en enregistrant les opérations comptables pour les organisations qui en ont besoin.

Chaque **type financier** est lié à un certain nombre de **comptes financiers** qui peuvent effectuer le suivi des recettes, des actifs, des charges et des subventions (le cas échéant), tel qu'indiqué pour les quatre types financiers par défaut de l'image suivante.

![image](/img/Fr_contribution_type_financier.PNG)

Les **Comptes financiers** doivent être basés sur le plan comptable de votre organisation. Dans CiviCRM, chaque contribution doit être affectée à un type financier. Lorsque la contribution est enregistrée, les débits et crédits appropriés sont automatiquement enregistrés dans les comptes financiers liés à ce type financier. (Si vous utilisez des ensembles de tarif ou de prix, chaque option doit être liée à un type financier différent et CiviCRM enregistrera toujours les débits et crédits appropriés pour tous les comptes financiers liés).

Il est souhaitable que vous consultiez votre comptable avant de créer ou de modifier les types financiers et les comptes Comptables existants.

### Types Financiers

Les types financiers standard inclus dans CiviCRM sont les tarifs d'événement, les cotisations des membres, les dons et les contributions de campagne comme indiqué dans l'image ci-dessus, mais vous pouvez modifier les comptes existants ou mettre en place de nouveaux types financiers pour répondre à vos besoins.

Généralement, vous aurez besoin d'un type financier pour chaque type de recettes que vous enregistrez dans CiviCRM pour suivre vos comptes. Donc, si vous faites un compte rendu des appels de dons non imposable, les dons pour les manifestations et les dons récurrents séparément, alors le fait de n'avoir qu'un seul type de financement «Dons» dans CiviCRM ne fonctionnera pas, vous aurez besoin d'un type financier appelé «Appel dons défiscalisés», Un autre appelé «Dons récurrents»....

Pour créer un nouveau type financier, allez :  **Administer> CiviContribute> Types financiers**, puis cliquez sur **Ajouter Type financier**

![image](/img/Fr_contribution_creer_type_financier.PNG)

Lorsque vous créez un nom spécifique pour un Type financier, CiviCRM crée automatiquement un compte de recette similairement nommé et l'affecte ainsi que les comptes par défaut pour l'actif, les dépenses et le coût des recettes au nouveau type financier. Pour modifier les comptes attribués à un type financier, vous pouvez le faire en cliquant sur **Comptes** à droite du type financier approprié puis **Administer> CiviContribute> Types financiers**. Le but de ce processus en deux étapes est de simplifier le cas d'utilisation courante où une organisation ne dispose que d'un compte de banque de dépôts, de comptes débiteurs et de comptes fournisseurs, mais offre plus de flexibilité pour des configurations avancées.

![Editing accounts linked to financial type](/img/civicontribute-financial-types-linked-accounts.png)

### Comptes financiers 

Comme pour les types financiers, la liste des comptes financiers préconfigurés répond aux besoins de nombreuses organisations, mais elle peut également être personnalisée si votre organisation nécessite des modifications ou des ajouts. (N'oubliez pas que chaque nouveau type financier ajoutera un nouveau compte de recettes portant le même nom.)

Pour modifier les comptes financiers aller à :  **Administer> CiviContribute> Comptes financiers**.

Les seuls champs obligatoires sont Nom et Type de compte financier. Les comptes de recettes sont définis lorsque vous créez le type financier.

![image](/img/Fr_contribution_creer_compte_financier.PNG)

Les autres champs que vous créez seront déterminés par votre organisation comptable. Si vous prévoyez d'exporter des transactions financières de CiviCRM dans votre logiciel de comptabilité, vous aurez besoin du code comptable (sans espace supplémentaire ou manquant). Si vous utilisez Quickbooks, vous aurez également besoin du code de type de compte.

REMARQUE: la modification du nom du compte financier modifiera également le nom du type financier.

## **Processeurs de paiement**

CiviCRM vous offre la possibilité d'accepter des paiements en ligne sur votre site Web. Vous pouvez autoriser des paiements en ligne pour une variété de raisons, y compris les campagnes de collecte de fonds, les cotisations des membres et la participation à certains événements.

Pour commencer à accepter des paiements en ligne, vous devez [configurer un processeur de paiement](../contributions/processeurs de paiement) qui va connecter votre site à l'infrastructure bancaire et de carte de crédit qui traite effectivement le paiement.

## **Méthodes de paiement**

Allez à **Administer> CiviContribute> Méthodes de paiement**  pour modifier les options existantes qui peuvent être utilisées pour les contributions ou pour ajouter une nouvelle option : **Ajouter des méthodes de paiement**. Les options courantes - carte de crédit, espèces, chèque, carte de débit et EFT - sont installées par défaut. Vous devez demander à votre comptable de confirmer que chaque méthode de paiement est liée au compte approprié.

![image](/img/Fr_contribution_moyen_de_paiement.PNG)

## **Cartes de Crédit Acceptées**

Allez à **Administer> CiviContribute> Cartes de crédit acceptées** pour modifier les cartes de crédit acceptables existantes ou définir une nouvelle option via **Ajouter carte de crédit accepté**.

Remarque: Si les informations de facturation sont collectées sur le site Web du processeur de paiement, vous devrez configurer les cartes de crédit / les méthodes de paiement acceptées sur ce site.

![image](/img/Fr_contribution_carte_de_paiement.PNG)

## Besoin de champs de données supplémentaires

CiviContribute dispose d'un ensemble de champs prédéfinis pour suivre les informations sur les contributions. Si vous devez suivre plus d'informations sur les contributions, vous pouvez le faire en définissant de nouveaux champs de données personnalisés. Ces données peuvent être utiles pour mieux catégoriser vos contributions ou suivre des informations supplémentaires.

**!!! Conseil** : Notez toutes les informations que vous souhaitez suivre sur vos contributions, y compris les compte rendus (décrits plus loin dans ce chapitre), puis comparez vos besoins de données aux champs prédéfinis de CiviCRM. Une façon simple de le faire est de regarder l'écran pour ajouter, si nécessaire, une nouvelle contribution. Beaucoup de fonctionnalités utiles sont déjà intégrées dans les champs de contribution de base, il est donc inutile de les dupliquer avec des champs personnalisés, mais votre organisation peut avoir des besoins spécifiques qui nécessitent des champs personnalisés.

Si vous devez créer des champs personnalisés pour répondre à vos besoins, lisez : [Création de champs personnalisés](../organizing-your-data/creating-custom-fields).

