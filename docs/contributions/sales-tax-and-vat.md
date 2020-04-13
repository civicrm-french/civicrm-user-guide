Taxe de vente et TVA
=================

Si votre organisation facture des taxes de vente ou de la TVA, vous devez activer cette fonctionnalité.

Pour activer la taxe de vente / TVA, allez à :

**Administrer > CiviContribute > Paramètres du composant CiviContribute** 
et cochez la case "Activer les taxes et la facturation".

Dans cet écran, vous pouvez également définir certains paramètres pour la taxe de vente / TVA:

- Notes ou termes standards : Saisissez la note ou le message à afficher sur la facture PDF ou les notes de crédit
- Paramètres d'affichage des taxes : comment votre organisation veut afficher la taxe / TVA :

   - Pas de taxe / TVA, total seulement
   - Affichage en tant que prix inclusif - 120 € (incluant les taxes de 20 €)
   - Affichage comme prix exclusif - taxe de 100 € + 20 €
   
![image](/img/enable_tax_fields.png)

Ajouter un compte financier pour la taxe de vente / TVA 
---------------------------------------------

Dès que la taxe de vente / TVA est activée, vous devez créer un ou plusieurs comptes financiers dans **Administrer> CiviContribute> Compte financier**. Faites défiler vers le bas de la page et cliquez sur **Ajouter un compte financier**.

Pour créer le compte de taxe de vente, assurez-vous que le **Type de compte financier** est défini sur **Déductible des impôts ?(Liability)**. Sélectionnez **Activé** et **Taxe** et spécifiez le **Taux de taxe**. Notez que si vous utilisez **Quick Books**, le **code de type de compte** doit être défini sur **SALESTAX**. **Le compte comptable** doit être basé sur les comptes comptables spécifiques de votre organisation.

![image](/img/salestaxaccount4.jpg)

Après avoir créé le compte financier, vous pouvez l'affecter au type financier spécifique en allant à **Administrer> CiviContribute>
Types financiers**. Trouvez le type de financement auquel s'applique cette taxe de vente, puis cliquez sur **Comptes**. 
Cliquez sur **Affecter un compte**.

![image](/img/assignaccount2.jpg)

Pour la **Relation de compte financier**, choisissez **Le compte de taxe de vente est** et dans le champ **Compte financier**, sélectionnez votre compte de taxe de vente.
Cliquez sur **Enregistrer**.

![image](/img/civicontribute-sales-tax-add-account.png)

Une fois le compte financier de la taxe de vente est ajouté, vous le verrez apparaître avec les autres comptes financiers pour ce type financier spécifique.

![image](/img/salestaxadded2.jpg)

Pour une configuration plus avancée avec des logiciels de comptabilité, tels que QuickBooks, vous devez impliquer le comptable de votre organisation dans la configuration de vos types financiers et de vos comptes financiers.

