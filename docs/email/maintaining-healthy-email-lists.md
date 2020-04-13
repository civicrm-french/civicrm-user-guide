Maintenir des listes de diffusion à jour
========================================

Dans le précédent chapitre, nous avons parlé de la création et du paramétrage des listes de diffusion. Dans ce chapitre, nous allons creuser un peu plus le sujet de la gestion des listes et parler conformité. Il est important de garder ses listes de diffusion avec un taux de rebonds faible et peu de désabonnements.

Il y a également le risque de la redoutée "blacklist" si vous avez un taux de rebond très élevé, ou celui d'être réprimandé par votre fournisseur smtp pour la même raison. Quoiqu'il en soit, gérer les taux de rebonds et les désabonnements représente un important et compliqué enjeu pour votre organisation.

Comprendre les rebonds de courriel
----------------------------------

Chaque fois que vous faites un envoi massif de courriels depuis CiviMail, il est possible que certains d'entre eux rebondissent, c'est à dire qu'un courriel d'erreur spécifique à un destinataire est renvoyé en retour. Les rebonds se produisent pour plusieurs raisons, certaines temporaires et d'autres permanentes.

### Pourquoi les courriels rebondissent ?

Si un courriel d'erreur est renvoyé, celui veut dire qu'il n'a jamais atteint sa destination. Les raisons peuvent être les suivantes :

1.  il y a une erreur de frappe dans l'adresse courriel ;
2.  l'adresse courriel n'existe plus ;
3.  la boite de réception du destinataire est pleine et ne peut temporairement plus accepter de messages supplémentaires ;
4.  le destinaire a configuré un message de réponse automatique (absence temporaire, etc).

CiviCRM gère ces différents types de rebonds différemment. Les rebonds temporaires n'affecte pas l'enregistrement d'un contact, et CiviCRM tentera de renvoyer le courriel plus tard. En revanche, le système mettra en **Suspendu** tout courriel de contact provoquant un rebond permanent. Dans ce cas, aucun courriel ne sera plus envoyé à cette adresse, jusqu'à ce que quelqu'un resolve le problème et retire ce statut.

Une table détaillée indiquant le nombre par type de rebonds acceptés par CiviCRM avant que ce dernier ne mette l'adresse du contact en **suspendu** est disponible dans le manuel adminsitrateur à la page [inbound mail](https://docs.civicrm.org/sysadmin/en/latest/setup/civimail/inbound/)


### Que dois-je faire si une adresse courriel est suspendue ?

Vous avez basiquement deux options : enlever le statut "suspendu" à l'adresse courriel, ou corriger/supprimer l'adresse.

Pour enlever le statut "Suspendu" :
1.  Aller dans **Recherche avancée**
2.  Dans **Critères de base**, cochez **Courriels suspendus**
![image](/img/Mailing%20Basic%20Search.png)
3.  Une fois obtenu la liste des contacts concernés, selectionnez les et choisissez l'action **Enlevez la suspension** de la liste déroulante et cliquez sur **Lancer**

Pour corriger / mettre à jour les adresses, vous devez d'abord créer un groupe (destiné à contenir les adresses en erreur), puis :
1.  Dans le menu supérieur, allez à **Rapports**
2.  Sélectionnez **Rapport des rebonds de courriels**
3.  Le rapport vous montrera la listes des contacts pour lesquels les courriels rebondissent.
4.  Vous pouvez alors ouvrir **Critères de rapport** dans la partie supérieur pour filtrer le rapport à un type précis de rebond
5.  À partir d'ici, vous pouvez ajouter les contacts issus de votre recherche au groupe précédemment créé.
6.  Listez le groupe via **Recherche avancée**, en cochant à nouveau **Courriel suspendu** au cas où des mises à jour auraient déjà été effectuées sur certains contacts.
7.  Sélectionnez **Mise à jour par lot à travers un Profil** pour que tous les résultats avec une adresse courriel incorrecte soient corrigés. Cela nécessite un profil qui contient *simplement* **Primary Email**.
8.  Sélectionnez ce profile et cliquez sur **Mettre à jour**.

### Différence entre courriels suspendus et désinscription

Les courriels dont le statut est "suspendu" sont différents des courriels pour lesquels les destinataires se sont désinscrits. Ces derniers ont cliqué sur le lien "Se désinscrire de cette newsletter". Ce lien est créé à l'aide du jeton **{action.unsubscribe}** ou **{action.unsubscribeUrl}**.

Les destinataires qui se sont désinscrits sont simplement retirés du groupe correspondant à la liste de diffusion utilisée.

### Quelle est la différence entre l'opt-out et la désinscription ?

Les destinataires de couriels peuvent également choisir de ne recevoir aucun courriel de diffusion de masse, en cliquant sur le lien fourni dans les messages de ce type. Cela s'appelle l'opt-out ou "option de retrait" en français. Vous pouvez toujours envoyer un courriel à quelqu'un ayant procédé à l'opt-out avec l'action **Envoyer courriel**, accessible depuis sa fiche contact ou en resultat de recherche. Les rappels planifiés seront également envoyés à ces personnes. Attention toutefois au courriel que vous envoyez à une personne ayant procédé à l'opt-out : vous pourriez être accusé d'envoyer du spam.

Pour procéder à l'opt-out, le destinataire du courriel peut cliquer sur le lien du courriel généré par l'un des jetons suivants : **{action.optOut}** ou **{action.optOutUrl}**

Vous pouvez inclure ces jetons directement dans le corps ou dans le pied de page de votre courriel (Plus d'information sur les jetons, rendez-vous au chapitre [Jetons, fusions et publipostages](https://docs.civicrm.org/user/fr/latest/common-workflows/tokens-and-mail-merge/). Pour en savoir plus sur les pieds de pages, rendez-vous à la rubrique [Création d'en-têtes et de pieds de page](https://docs.civicrm.org/user/fr/latest/email/set-up/#creation-den-tetes-et-de-pieds-de-page) du chapitre Configuration.

### Qu'est-ce que l'option de protection de la vie privée "ne pas envoyer de courriel" signifie ?

Si un contact a activé cette option, alors vous ne serez pas en mesure de lui envoyer des courriels individuels ou en petits volumes en utilisant l'action "Envoyer un courriel" disponible sur sa fiche contact et en résultat d'une recherche. Il ne recevra pas non plus des courriels de diffusion de masse envoyé avec CiviMail. Toutefois, il recevra toujours les courriels générés par les rappels planifiés, à moins de l'avoir exclu spécifiquement de ces rappels (ce qui est probablement une bonne chose à faire dans ce cas précis). Pour en savoir plus sur ce point, allez au chapitre [Rappels planifiés](https://docs.civicrm.org/user/fr/latest/email/scheduled-reminders/) de cette section.

### Comment puis-je être certain qu'un contact ne reçoive aucun courriel ?

Une erreur humaine est toujours possible. Pour garantir totalement qu'un contact ne reçoive plus aucun courriel, il faut dans ce cas supprimer toutes les adresses courriels de sa fiche. Toutefois, dans ce cas là, le contact ne pourra plus se connecter à votre site web.
