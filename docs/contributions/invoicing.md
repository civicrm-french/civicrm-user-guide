Facturation
=========

La facturation fonctionne pour tous les types financiers et statuts de contributions terminés et en attente. Elle doit être activée. Pour activer la facturation, accédez à **Administrer> CiviContribute> Paramètres du module CiviContribute** et cochez la case "Activer les taxes et la facturation".

Dans cet écran, vous pouvez également définir certains paramètres pour les factures:

- ajouter un préfixe pour les factures
- l'intervalle de jours, semaines ou années jusqu'à la date d'échéance
- des notes personnalisées ou des conditions standard que vous souhaitez voir apparaître sur votre facture

![image](/img/civicontribute_comp_settings.png)

Créer une facture
--------------------

Une fois la facturation activée, vous pouvez facilement imprimer des factures ou les envoyer par courrier électronique pour les contributions complètes ou en attente à partir de l'onglet **Contribution** d'un contact.

1. Accédez à l'onglet "Contribution" du Contact
2. Affichez l'enregistrement pour lequel vous souhaitez créer une facture

![image](/img/contribution_summary.png)

1. Dès que vous consultez le dossier du contact, vous avez la possibilité d'imprimer la facture ou l'envoyer par courriel. L'impression d'une facture génèrera un pdf et envoyer une facture par email affichera un écran "Options supplémentaire".

![image](/img/contributiion_view_Screen.png)

1. Une fois que vous avez choisi l'option Facture par Email vous avez des options avant d'envoyer:

- De : l'adresse e-mail

- Taper un message supplémentaire si besoin

![image](/img/email_invoice.png)

Voici un exemple de facture imprimée. Les factures peuvent être personnalisées.

![image](/img/invoice.png)

Personnalisation de facture
-----------------------

Le code du modèle prérempli renseigne le nom de l'organisation, l'adresse et les informations du site Web figurant en haut à droite des factures, directement à partir de l'adresse de l'organisation et des informations de contact. Pour apporter des modifications à ces informations, vous pouvez y accéder à l'adresse **Administer Console> Liste de contrôle de la configuration> Adresse de l'organisation et informations de contact**.

L'aspect de la facture et de l'image de la facture peut être modifié et personnalisé dans **Administrer> CiviCRM> Modèles de messages> Messages de flux de travail système> Contributions-Facture.**

Pour changer l'image sur la facture, vous devrez modifier le code sur la ligne 10, en remplaçant la source de l'image (img src).

```html
<td><img src = "{$resourceBase}/i/civi99.png" height = "34px" width
= "99px"></td>
```

Pour une configuration plus avancée avec des logiciels de comptabilité tels que QuickBooks, vous devez impliquer le comptable de votre organisation pour la configuration de vos types et comptes financiers.

Voir "Intégration comptable" et la page Wiki pour plus d'informations.
