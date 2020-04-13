Configuration de la messagerie électronique
===========================================

Ce chapitre traite de la configuration système nécessaire pour que CiviCRM puisse envoyer et recevoir des courriels. Il s'agit d'une tâche complexe qui nécessite des compétences du niveau administrateur système. La configuration correcte de votre système de courrier électronique est cruciale pour empêcher votre serveur de recevoir des spams ou être black listé.

Reportez-vous à la "Section des courriers électroniques" au chapitre "Configuration des tâches" pour configurer l'envoi des messages après que les paramètres de configuration du courrier électronique soient effectués.

Certaines parties de la configuration sont une fonctionnalité native de CiviCRM (envoi et réception de courriels de base) alors que d'autres (envoi groupé) nécessitent l'activation du composant CiviMAIL.

Vous aurez peut-être besoin de modifier la configuration de votre DNS, créer des comptes de messagerie, configurer une tâche cron, lire les en-têtes des messages électroniques et éventuellement modifier la configuration de votre serveur SMTP.

Ce chapitre suppose que vous exécutez CiviCRM sur un serveur Linux et que vous êtes à l'aise pour travailler avec le shell et exécuter des commandes simples. La plupart de ces étapes seront similaires sur d'autres systèmes d'exploitation, mais vous devrez les adapter à votre système et à vos outils.

La configuration décrite ici fonctionne bien pour les envois jusqu'à environ 10 000 personnes. Si vous prévoyez d'envoyer des courriels à des centaines de milliers de contacts, vous devrez comparer plusieurs options d'hébergement et envisager un serveur SMTP dédié. Cette configuration plus complexe est en dehors de la portée de ce livre, mais vous pouvez trouver des instructions fournies par la communauté sur le wiki de documentation CiviCRM : ([http://wiki.civicrm.org/confluence/display/CRMDOC/CiviMail+Installation](http://wiki.civicrm.org/confluence/display/CRMDOC/CiviMail+Installation)).

Dans ce chapitre, nous utiliserons pour l'exemple une adresse de boîte aux lettres Gmail externe pour tester la configuration. Donc, la première étape est de créer un compte Gmail si vous n'en avez pas. Vous pouvez également utiliser une autre adresse pour tester les procédures de ce chapitre, mais vous devrez pouvoir afficher la source des messages reçus

Une fois que votre système est correctement configuré, nous allons utiliser un cron CiviCRM dans  **Travaux programmés**  et s'assurer que vos envois programmés sont bien envoyés.

Configuration du service de messagerie sortant
----------------------------------------------
Les paramètres de messagerie sortante sont configurés dans : **Administer> Paramètres système> Courriel sortant (SMTP / Sendmail)**.  Les choix sont : 

![image](/img/Fr_courrier_sortant.PNG)

-   **mail()**: C'est l'option par défaut et si elle fonctionne pour vous, vous devez l'utiliser.
-   **SMTP**: Si vous avez un serveur de messagerie externe dédié, veuillez en spécifier les détails ici. Les messages de rebond générés avec SMTP sont légèrement plus complets que ceux de mail(), mais il n'y a aucun avantage pratique à utiliser SMTP si vous pouvez utiliser mail().
-   **Sendmail**: Cette option est conservée pour la compatibilité avec les anciennes versions CiviCRM.
-   **Désactiver l'envoi de courriels**: Fonctionne comme indiqué.
-   **Redirection vers base de données**: Tous les e-mails seront enregistrés comme des envois archivés au lieu d'être envoyés. Ils peuvent être trouvés dans la table civicrm_mailing_spool de la base de données CiviCRM.

Après avoir fait votre choix, envoyez un email de test à votre adresse sur Gmail et vérifiez que vous le recevez bien.

Si vous recevez le message d'erreur suivant, vous devrez configurer une adresse de courrier électronique "DE" par défaut (Voir chapitre sur la configuration de CiviMail).

```
Sorry. A non-recoverable error has occurred.
The site administrator needs to enter a valid 'FROM Email Address' in
Administer -> Configure -> Domain Information.
The email address used may need to be a valid mail account with your email service provider.

```
Dès que vous avez reçu le courrier électronique, vous devrez consulter la source. Dans Gmail cliquez sur "Afficher l'original" dans l'e-mail que vous avez reçu. Le courrier électronique doit contenir une en-tête qui ressemblent à ce qui suit :

```
Received: from yourmailserver.example.org (xxx.example.org
[12.45.120.30])
by mx.google.com with ESMTP id e31si4519230wej.3.2010.04.26.00.38.16;
Mon, 26 Apr 2010 00:38:17 -0700 (PDT) Received-SPF: pass
google.com: best guess record for domain of
[youremail@example.org](mailto:youremail@example.org) designates
12.45.120.30 as permitted sender) client-ip=12.45.120.30

```
Explications : 

*"Received: from..."* Doit correspondre à votre serveur de messagerie et être correctement configuré. Il se peut que cette entête contienne des informations sur votre fournisseur d'hébergement au lieu de votre nom de domaine. Ce n'est pas un problème tant que le serveur de messagerie est correctement configuré. Si vous avez une adresse IP dédiée à votre serveur, vous devez essayer de configurer un DNS inverse qui représente votre organisation au lieu du nom par défaut.

*"Received-SPF"*  L'en-tête doit indiquer "pass" ou "neutral". Sender Policy Framework (SPF) est décrit plus loin en détail.

L'envoi de courrier en nombre important nécessite beaucoup de ressources. Nous ne recommandons pas d'envoyer des messages électroniques à partir de fournisseurs d'hébergement "low-cost". Le temps que vous passerez en dépannage coûtera souvent plus cher que l'abonnement chez un hôte plus professionnel. Vérifiez avec votre fournisseur d'hébergement les limitations du nombre d'envoi par 24 heures ou par heure et s'il exécute PHP en mode sans échec.

Certains serveurs de messagerie de vos destinataires utilisent DNSBL (services de liste noire) et conservent une liste noire d'adresses IP susceptibles d'envoyer du spam. Le courrier de ces serveurs sera marqué comme spam et n'atteindra pas sa destination. Si votre serveur est mis en liste noire (par exemple, parce que un nombre suffisant de destinataires ont marqué votre courrier électronique comme du spam, ou parce qu'un autre site Web sur votre serveur a été marqué comme spam), vous devrez contacter les hébergeurs qui vous ont mis en liste noire et les convaincre de votre bonne foi.

Il existe plusieurs sites Web qui vous aident à tester si vous êtes dans un DNSBL. Une recherche sur le Web pour "blacklisting email" va transformer certains envois. Testez régulièrement pour savoir si vous êtes sur une liste noire.

Configuration du Sender Policy Framework (SPF)
----------------------------------------------

Par défaut, Internet permet à tout serveur de messagerie d'envoyer un courrier électronique prétendant appartenir à n'importe qui. Cela permet aux spammeurs de fabriquer facilement des adresses et d'envoyer du spam à l'aide de votre adresse de courrier électronique (ou de tout autre). SPF vous permet de créer un enregistrement DNS spécial répertoriant les adresses IP des serveurs de messagerie qui peuvent légitimement envoyer des e-mails à partir de @*votredomaine.org*

Si votre nom de domaine a déjà un enregistrement SPF, assurez-vous qu'il inclut l'adresse IP de votre serveur de messagerie CiviCRM (qui peut être différent de l'hôte utilisé pour le serveur Web ou de vos serveurs de messagerie). Si ce n'est pas le cas, ajoutez cette adresse IP.

Si vous n'avez pas d'enregistrement SPF, pensez à en ajouter un. Vous devrez ajouter au moins votre serveur de messagerie et le serveur CiviCRM (s'ils sont différents) à l'enregistrement SPF.

Vous pouvez en savoir plus sur le SPF ici : [http://www.openspf.org](http://www.openspf.org)

## Configuration du traitement des e-mails entrants

Cette section explique la configuration du traitement des rebonds et la réception automatique des courriels entrants. La configuration de **Tâches planifiées** pour effectuer le traitement des rebonds réels est développée plus loin dans ce chapitre.

### Traitement des rebonds

CiviCRM peut recevoir automatiquement la [notification d'email renvoyé](http://en.wikipedia.org/wiki/Bounce_message) selon le [type de rebond](http://tools.ietf.org/html/rfc3463) signalé par le serveur du destinataire et impactant vos contacts en conséquence. Pour ce faire, vous devrez configurer une boîte aux lettres de messagerie pour recevoir des e-mails non reçus ainsi qu'un calendrier **job - Bounces Fetcher**  qui lira périodiquement cette boîte aux lettres et mettra à jour vos contacts dans CiviCRM.

Administration> Paramètres système> Travaux planifiés :

![image](/img/Fr_taches_periodiques.PNG)

L'adresse e-mail de rebond est une adresse e-mail "invisible" que l'on voit uniquement dans les champs cachés qui précèdent les en-têtes et le message ajouté par l'utilisateur. Choisissez un nom significatif pour cela. Dans cet exemple, nous avons choisi *return*. l'adresse email que nous devons configurer sur un serveur de messagerie *example.org*  est *return@example.org*.

Pour chaque e-mail envoyé via la fonctionnalité d'envoi massif de CiviMail, une nouvelle adresse d'expéditeur "invisible" unique est créée à l'aide du [chemin de retour d'enveloppe variable ou VERP](http://en.wikipedia.org/gwki/Variable_envelope_return_path).

Lorsque CiviCRM reçoit un rebond, il regarde l'adresse de l'expéditeur invisible pour décider quel email a rebondi. 

CiviCRM examine ensuite le modèle et le type de rebond pour décider de l'action à entreprendre. Les types de rebond se répartissent en deux catégories de base: les défaillances permanentes (hard bounce) et les défaillances transitoires (soft bounce). Un seul défaut permanent déclenche une action de CiviCRM pour définir l'adresse e-mail du contact en attente. Pour les défaillances transitoires, CiviCRM attend plusieurs rebonds avant de définir l'email du contact en attente.

Le [seuil spécifique pour chaque type de rebond](http://wiki.civicrm.org/confluence/display/CRMDOC43/Bounce+Handling) se trouve dans les tables :  "civcirm_mailing_bounce_pattern" et "civicrm_mailing_bounce_type". Plusieurs motifs de réponse de rebond différents sont liés à un type et un seuil donné.

### **Traitement des E-mails en tant qu'activité**

CiviCRM peut récupérer automatiquement le courrier électronique d'une boîte de réception spécifiée et l'inclure comme une activité d'email dans les contacts de type "Individuel" correspondant à l'expéditeur et aux destinataires de l'email. De nouveaux contacts individuels seront créés pour les adresses électroniques qui ne sont pas déjà affectées aux personnes de la base de données.

**NOTE**: Cette fonction est active uniquement pour les types de contacts individuels. Si le courrier entrant provient d'une adresse e-mail déjà enregistrée pour une organisation, un nouveau contact individuel avec cette même adresse e-mail sera créé et l'activité sera enregistrée pour ce nouveau contact individuel, et non dans l'organisation.

Il existe deux façons de faire (l'une ou l'autre ou les deux méthodes peuvent être configurées en même temps):

-   **Adresse e-mail spéciale :**  Configurez une adresse e-mail spéciale pour votre organisation. ( Exemple :  Civiemails@example.com). Les utilisateurs peuvent ensuite ajouter cette adresse dans le champ Cci pour vos e-mails sortants. Ils seront automatiquement déposées dans CiviCRM comme décrit ci-dessus. La personne qui reçoit le courrier électronique ne verra cette adresse spéciale si le champ Cci est utilisé. 
-   **Dossier IMAP :**  Configurez un dossier dans votre boîte de réception IMAP où vous pourrez glisser les e-mails que vous voulez archivér dans CiviCRM. Cela fonctionne avec les emails entrants et sortants (cela nécessite bien entendu, que votre courrier électronique soit configuré en utilisant IMAP).

### Adresse e-mail spéciale pour les e-mails entrants

Il existe plusieurs façons de configurer votre boîte aux lettres entrante:

-   **Sous-adressage :** Votre service de messagerie peut vous permettre d'ajouter un + *tag*  ou - *tag*  pour qualifier votre adresse e-mail (par exemple, *retour+test@example.org*). Plusieurs serveurs de messagerie, y compris Gmail, Yahoo! et Postfix fournissent ce sous-adressage par défaut.
    Essayez de vous envoyer un e-mail en ajoutant une balise +*tag*  or -*tag*. Si vous avez reçu le courrier envoyé avec une étiquette, cela signifie que vous pouvez utiliser directement la boîte aux lettres que vous avez créée (*return@example.org* dans notre exemple) comme [VERP](http://en.wikipedia.org/Wiki//Variable_envelope_return_path).
  
-  **Compte "Catch-all" :** Si le sous-adressage ne fonctionne pas sur votre serveur de messagerie, vous devez définir le compte de messagerie que vous avez créé (*return@example.org*) comme compte "catch-all" . Tous les courriers envoyés à une adresse qui n'est pas un compte de messagerie réel finiront là, y compris tous les messages électroniques retournés.

-  **Adresse externe** : Si aucune des méthodes précédentes ne fonctionne, envisagez de créer un nouveau compte sur un service tel que Gmail et de l'utiliser pour recevoir les emails renvoyés. Vous devrez définir des filtres dans ce compte afin qu'il ne détourne pas en tant que spam tous les emails retournés qu'il recevra.

### Ajout d'un compte de messagerie entrant pour le traitement des retours et/ou le courrier électronique

Une fois que vous avez créé votre compte de messagerie pour recevoir des retours ou des courriers électroniques pour le dépôt automatique, vous devez configurer CiviMail pour qu'il sache comment le lire en tant qu'adresse de messagerie par défaut : **Administer> CiviMail> Comptes courriel** : 

![Screen shot of the email box selection screen](/img/administer-civimail-mailaccount.png)

![image](/img/Fr_creer_compte_courriel.PNG)

-   Spécifiez le serveur ** :  IP serveur, Nom d'utilisateur et le mot de passe** que vous avez utilisés lors de la création du compte.
-   La **Partie locale** est facultative et n'est pertinente que si vous avez pu configurer un compte en utilisant un sous-adressage. Il doit s'agir du compte que vous avez créé avec '+' ou '-' ajouté, par exemple, "return+" ou "return-".
-   Le **Domaine Internet** est le domaine de l'adresse courriel (la partie après @) de votre adresse de courrier électronique (exemple.org).
-   Vous pouvez laisser **Adresse de retour** vide.
-   Si votre serveur de messagerie le supporte, spécifiez IMAP dans **Protocole** et vérifiez **SLL**, sinon utilisez POP.
-   Vous pouvez spécifier un dossier IMAP dans le champ **Source** en utilisant la syntaxe INBOX.CiviMail. **Remarque :** Certains serveurs d'échange peuvent ne pas être configurés de manière compatible. Dans ce cas, vous pouvez configurer un script comme fetchmail et utiliser Maildir.
-   Dans le champ **Utilisé pour?**, vous pouvez choisir d'utiliser le compte de messagerie pour le **Traitement de rebond ** ou  le **Traitement de courrier électronique** (ou Archivage automatique). Vous pouvez avoir plusieurs comptes spécifiés pour le dépôt automatique, mais un seul pour le traitement de rebond. C'est le mode par défaut.

Une fois que la boîte de dialogue **Bounce Processing** est configurée, vous devez configurer CiviMail pour la vider, lire tous ces messages renvoyés et identifier les contacts renvoyés. Ceci est effectué par la fonction "Travaux programmés" de CiviCRM.

Nous vous recommandons de tester le processus de retour en exécutant le processus manuellement avant de configurer CiviCRM pour traiter les messages électroniques renvoyés automatiquement. Cela peut se faire dans **Administer> Paramètres système> Travaux programmés**, option : **Fecht bounces** et sélectionnez **Plus> Exécuter maintenant**. Vérifiez le journal des travaux pour les messages d'erreur.
Une fois que vous avez vérifié que CiviCRM peut traiter correctement le rebond, vous pouvez le configurer pour traiter automatiquement les réponses et les rebonds de façon régulière.

### Planification du traitement du courrier entrant et sortant

Comme indiqué dans le chapitre précédent, le traitement du courrier et d'autres tâches peuvent être automatisés via la page d'administration des "Travaux programmés". La gamme complète des options est développée dans le wiki [Gérer les travaux programmés](http://wiki.civicrm.org/confluence/display/CRMDOC43/Managing+Scheduled+Jobs). Vous trouverez ci-dessous des exemples spécifiques permettant d'activer le traitement de courrier CiviCRM.

### Planification à l'aide de la page d'administration des Travaux programmés

Les envois de masse sont générés via l'interface Web de CiviMail et sont mis en file d'attente pour être envoyés à leurs destinataires. Pour planifier le traitement régulier de cette file d'attente et tous les retours reçus, allez dans **Administer> Paramètres système> travaux programmés** et recherchez **Fetch Bounces** et **Send Scheduled Mailings** . Modifiez-les à tour de rôle, en définissant leur **Fréquence d'éxécution** programmée à "Hebdomadaire", "Quotidien" ou "Chaque lancement de la tâche planifiée." Les valeurs par défaut doivent être correctes pour les petites installations. Sélectionnez ensuite  **Plus> Activer** pour chaque tâche.

Dans cet exemple, en utilisant la fréquence par défaut des jobs tels que le [cron configuré pour s'exécuter à des intervalles de 15 minutes](http://wiki.civicrm.org/confluence/display/CRMDOC/Managing+Scheduled+Jobs), les envois programmés seront envoyés tous les 15 minutes et les rebonds seront récupérés et traités chaque heure.

Si vous devez envoyer un e-mail immédiatement, sans attendre la tâche cron, vous pouvez déclencher le processus d'envoi en allant à : **Administer> Paramètres système> travaux programmés**  puis sélectionner **Plus> Exécuter maintenant**. Utilisez cette capacité avec modération car cela pourrait utiliser beaucoup de ressources serveur et causer un ralentissement sensible. Les paramètres d'administration pour l'envoi d'e-mails sont généralement configurés pour minimiser la charge du serveur. La planification du travail est un moyen plus efficace d'envoyer des courriels de masse.

### Planification des tâches de messagerie à l'aide de l'interface de ligne de commande

Comme alternative sur Linux et autres systèmes Unix, des travaux cron individuels peuvent être utilisés pour planifier le traitement du courrier entrant et sortant plutôt que la page **Scheduled Jobs**. Cette approche donne aux administrateurs système expérimentés un contrôle plus précis de ces processus en configurant des jobs cron spécifiques en dehors des autres tâches planifiées.

Le travail cron doit s'exécuter à l'aide d'un compte reconnu par votre CMS.

Créez un compte dédié à cette tâche (par exemple *mailprocess, civimail, cronmail, etc...*), donnez-lui un mot de passe long et sécurisé (par exemple *seol-lzprm42amv-psyc*) et affectez-le à CiviCRM, CiviMail et permettez-lui d'afficher tous les contacts. Ne modifiez pas le mot de passe du compte sans modifier le mot de passe dans les fichiers de configuration de cette tâche cron.

Pour configurer une tâche cron, vous devez savoir si php-cli est installé. À partir du shell, tapez *php -v*. Si vous voyez **(cli)** dans le résultat, tel que :
```
PHP 5.2.3-1ubuntu6.5 (cli) (built: Feb 11 2009 19:55:53) Copyright (c)
1997-2007
The PHP Group Zend Engine v2.2.0, Copyright (c) 1998-2007
Zend Technologies with eAccelerator v0.9.5.3, Copyright (c) 2004-2006
eAccelerator, by eAccelerator

```
Ceci signifie que php-cli est installé et que vous devriez l'utiliser, car il présente plusieurs avantages:

-   Vous pouvez exécuter un script PHP à une priorité inférieure à celle de votre serveur Web, de sorte que, même si cela prend beaucoup de CPU, cela n'interfère pas avec les utilisateurs réguliers de votre site.
- Vous pouvez définir des limites de mémoire différentes pour le processus php-cli et le processus PHP utilisé par votre serveur Web.
- Vous évitez les charges du serveur Web et de la couche HTTP.
- Vous n'aurez pas de problèmes de timeout.

Voici la configuration cron complète pour gérer les exigences de courrier de CiviCRM:

```
# This must be set to the directory where civicrm is installed.
CIVI_ROOT=/var/www/civicrm

# Comment: I believe these two lines are unnecessary.
# USER=www-data
# MAILTO="you@example.org"

# Location of the PHP Command Line Interface binary.
# nice -19 forces to run at a lower priority than the web server

PHP=nice -n19 /usr/bin/php

# line to be modified according to the informations below
# like this: PARAMS= -j -s<default or domain> -u<user>
-p<password> -e Job -a process_mailing

PARAMS= -j -sdefault -umailprocess -pseol-lzprm42amv-psyc -e Job -a
process_mailing
PARAMSBOUNCE= -j -sdefault -umailprocess -pseol-lzprm42amv-psyc -e Job
-a fetch_bounces

# cronjob send
# m h dom mon dow command
*/5 * * * * cd $CIVI_ROOT; $PHP bin/cli.php $PARAMS
*/15 * * * * cd $CIVI_ROOT; $PHP bin/cli.php $PARAMSBOUNCE

```
L'utilisateur qui exécute les scripts (*www-data* dans cet exemple) doit pouvoir écrire dans le dossier temporaire. Votre configuration peut spécifier un utilisateur différent.
Vous n'avez pas à exécuter les deux scripts à la même fréquence. Le fichier crontab précédent vérifie toutes les 5 minutes si les e-mails doivent être envoyés, mais seulement toutes les 15 minutes si les e-mails renvoyés doivent être traités.

**PARAMS=**  contient :
1.  Le site que vous utilisez, qui est **- sdefault**  sur Drupal. Si vous exécutez plusieurs sites CiviCRM sur un seul serveur, vous devez spécifier le domaine de votre site, tel que **- sexample.org**.
2.  Le compte d'utilisateur : (**-umailprocess**).
3.  Le mot de passe que vous avez défini : (**-pseol-lzprm42amv-psyc**).
