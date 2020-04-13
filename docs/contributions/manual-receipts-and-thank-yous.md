# Envoi de reçus et de lettres de remerciement 

## Reçus
 
Les donateurs qui effectuent des contributions via un formulaire en ligne recevront automatiquement un reçu par courriel pour leur paiement, à condition que la possibilité de les envoyer ait été sélectionnée lors de la configuration de la page de contribution. Si vous souhaitez envoyer ou renvoyer manuellement un reçu à une date ultérieure, vous pouvez le faire en éditant l'enregistrement de contribution par rapport à un contact et en cochant l'option **Envoyer reçu?**. Le reçu de contribution hors ligne sera envoyé lorsque vous cliquez sur **Enregistrer**.

Vous pouvez envoyer des reçus de contribution hors ligne à plusieurs contacts en même temps via la recherche [Rechercher des contributions](../contributions/recherche-et-visualisation-contributions). Après avoir sélectionné les contacts auxquels vous souhaitez envoyer un reçu, sélectionnez **Reçus - Imprimer ou Email** dans le menu déroulant des actions.

![ContributionReceiptsManual](/img/civicontribute-receipts-manual.PNG)

Vous avez la possibilité d'envoyer des reçus par courrier électronique ou d'éditer des reçus PDF à poster aux contributeurs. 
![image](/img/Print%20contribution%20receipt%20options.PNG)

Par défaut, l'envoi par courrier électronique ou la création de reçus PDF mettra à jour la date de réception de chaque contribution, mais vous pouvez conserver les dates de réception existantes si nécessaire. Vous pouvez également choisir de ne pas tenir compte des paramètres **Ne pas envoyer par courrier électronique/Ne pas envoyer par courrier électronique** afin que tous les contributeurs sélectionnés reçoivent un accusé de réception.

Le reçu de contribution hors ligne standard affiche des informations limitées. Il peut être personnalisé mais cela nécessite une connaissance de Smarty. Il vous sera peut-être plus facile de configurer des reçus «envoyer plus tard» en utilisant le flux de lettres de remerciements.


## Lettres de remerciements

Certaines organisations souhaitent envoyer des lettres de remerciement aux personnes qui ont fait un don pour une campagne particuliere, en les informant du montant total recueilli. D'autres organisations préfèrent envoyer un reçu à chaque contact en fin d'année fiscale couvrant tous les dons déductibles d'impôt effectués au cours de cette année. Ces deux scénarios et d'autres peuvent être réalisés à l'aide de la fonctionnalité "Lettres de remerciement pour les contributions". Cette action est disponible à partir de l'écran de résultats de recherche affichant des contributions (plutôt que des contacts). Les étapes suvantes permettent cette réalisation:

1. Utilisez **Rechercher des contributions** ou utilisez **Recherche avancée** avec **Afficher les résultats comme** défini sur **Contributions** pour votre recherche.
2. Sélectionnez les contributions pour lesquelles vous voulez des lettres de remerciement ou des reçus combinés.
3. Choisissez l'action **Lettres de remerciement - imprimer ou Email**. Les éléments suivants seront affichés:

![ContributionThankyouLettersNogrouping](/img/civicontribute-thank-you-letters-no-grouping.PNG)

4. Choisissez **Mettre à jour les dates de remerciements pour ces contributions** ou **Mettre à jour les dates de réception de ces contributions** selon les besoins. La date actuelle sera saisie dans le champ approprié.
5. Il y a trois **Options d'impression et d'email** explicites:

    - Générer des fichiers PDF pour l'impression (uniquement).
    
    - Envoyer des emails si possible. Générer des fichiers PDF imprimables pour les contacts qui ne peuvent ou ne veulent pas recevoir d'e-mails.
    
    - Envoyer des emails si possible. Générer des fichiers PDF imprimables pour tous les contacts.

6. Certaines personnes peuvent avoir plusieurs contributions. Si vous souhaitez envoyer une lettre pour chaque contribution, définissez **Contributions groupées par** à **- pas de regroupement -**. Vous pouvez également choisir d'afficher les données de contribution pour plusieurs contributions provenant du même contact à un emplacement dans le corps de votre lettre. Il y a cinq options "groupées par".
7. **Séparateur (contributions groupées)** ne s'applique que si vous avez choisi autre chose que **- aucun regroupement -** pour les contributions. Ces options seront développées ci-dessous dans *Lettres de remerciement groupées*.
8. Assurez-vous de vérifier les paramètres **Format de page**.
9. Vous pouvez utiliser un modèle existant, créer une nouvelle lettre à usage unique ou créer une nouvelle lettre et l'enregistrer en tant que nouveau modèle. [Jetons et publipostage](.../common-workflows/jetons-et-publipostage) et [Communications par courrier postal](.../common-workflows/post-mail-communications)  fournissent plus d'informations sur la création de lettres modèles
10. Lorsque vous cliquez sur **Rédiger des lettres de remerciement**, les lettres seront générées et une activité «Imprimer une lettre PDF» sera créée pour chaque lettre avec le **Sujet d'activité** que vous avez spécifié.


### Lettres de remerciement groupées

Vous pouvez envoyer des relevés de fin d'exercice ou des reçus fiscaux à vos contacts si vous choisissez une option autre que **- aucun regroupement -** pour le champ **Contributions groupées par**.

Dans une installation CiviCRM standard, les lettres par défaut qui sont être produites lorsque vous regroupez des contributions peuvent vous paraitre assez sommaire. 

Si vous choisissez **Virgule** comme **Séparateur**, les montants et / ou les dates de cotisation se suivront l'une après l'autre, séparés par des virgules. 
Par exemple "Merci pour vos généreux dons de {contribution.total_amount} reçus  {contribution.receive_date} respectivement." deviendra "Merci pour vos généreux dons de 100,00 €, 150,00 €, 325,00 € reçus le 1er janvier 2018, le 5 mars 2018, le 16 mai 2018 respectivement."
Si vous choisissez **Tabulation** comme **Séparateur**, chaque instance de contribution sera placée dans sa propre colonne de table. Par exemple:

![image](/img/Thank-you%20letters%20as%20table%20template.PNG)

aura pour résultat:

![image](/img/Thank-you%20letters%20as%20table_1.PNG)

Ce format fonctionne bien si seulement plusieurs contributions ont été reçues au cours de l'année, mais la table sera plus large que la page pour les dons mensuels, bimensuels ou hebdomadaires.

Dans aucun des deux cas, le montant total de la contribution annuelle ne peut être inclus dans la lettre.

Pour inclure le montant annuel total de la contribution dans la lettre et pour produire une lettre plus adaptée à plusieurs contributions de la même personne, vous ou votre développeur devrez activer la fonctionnalité Smarty pour vos emails. Voir ici :
([http://wiki.civicrm.org/confluence/display/CRMDOC/Smarty+in+mail+templates](http://wiki.civicrm.org/confluence/display/CRMDOC/Smarty+in+mail+templates)).
Une fois que cela a été fait, le montant annuel total de la contribution peut être inclus dans la lettre en utilisant le jeton {$ contribution_aggregate}.

Par exemple, si la source HTML pour votre lettre est:

```html
<p>Dear {contact.first_name}</p>
<p>Thank you for donating ${$contribution_aggregate} to help the arts during the 2014 financial year</p>
<p>Your donation is tax deductible and the details are given below.</p>
<p>with appreciation for your generosity,</p>
<p>the CEO</p>
  <table class="table" style="width: 500px;" border="1" cellspacing="0" cellpadding="2" align="left">
    <tbody>
      <tr>
        <th>Date</th>
        <th>Amount</th>
        <th>Receipt Number</th></tr>
    <!--
    {foreach from=$contributions item=contribution} {assign
    var="date" value=$contribution.receive_date|date_format:"%d %B
    %Y"}
  -->
      <tr>
        <td>{$date}</td>
        <td>{$contribution.total_amount}</td>
        <td>{$contribution.id}</td>
      </tr>
   <!--
    {/foreach}

 --></tbody>
  </table>
```
alors vos lettres ressembleront à:

![image](/img/Thank-you%20letters%20as%20with%20smarty%20enabled_2.PNG)
