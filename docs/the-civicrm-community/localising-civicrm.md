Régionalisation de CiviCRM
==================

Le code, les interfaces et la documentation de CiviCRM ont été initialement développés en anglais. Cependant, le logiciel a été conçu pour pouvoir s'adapter à toutes les organisations peu importe où elles sont. Ces organisations doivent pouvoir adapter le logiciel selon leurs circonstances, sans qu'il soit nécessaire de modifier le code d'origine.

Pour régionaliser CiviCRM (ou tout autre logiciel), il ne suffit pas de simplement pouvoir changer la langue des textes affichés à  l'écran. Considérons par exemple, la devise monétaire utilisée dans un pays (USD ou $ aux États-Unis, GBP ou £ au Royaume-Uni), le format de la date et de l'heure (le 16 novembre 2016 pourrait être écrit sous la forme de 11/16/2016 aux États-Unis, mais 16.11.2016 en Russie) ou le format des chiffres (1 234 567,89 en Slovakie ou Hongrie, mais 1,234,567**.**89 au Japan ou aux États-Unis).

CiviCRM offre plusieurs fonctionnalités pour s'adapter aux besoins qui peuvent varier selon la langue et selon la région. L'équipe de développement de CiviCRM développe régulièrement de nouveaux outils pour simplifier ce processus. L'écran de Régionalisation (ou Localisation) affiché dans la saisie d'écran ci-dessous permet de configurer les bons paramètres de préférences régionales de CiviCRM. Pour y accéder, se rendre à Administrer > Localisation > Langue, devises et localisation.

![2](/img/CiviCRM_update-CiviCore-2-en.png "2")

Si vous souhaitez utiliser CiviCRM dans une autre langue que l'anglais, il est important de choisir cette langue lors de l'installation. En installant directement en français, par exemple, CiviCRM s'assurera que toutes les configurations par défaut et modèles de messages soient en français. Si vous changez la langue à un autre moment, il faudra manuellement traduire ces configurations. Il y a également quelques subtilités à prendre en compte si vous souhaitez utiliser CiviCRM dans plus d'une langue (le mode multi-lingue).

Traductions
------------

CiviCRM peut s'adapter à plusieurs langues, cependant l'équipe de développement dépend de la communauté pour traduire les textes qui sont affichés à l'écran.

Un certain nombre de traductions sont déjà disponibles. Certaines traductions sont complétées à 90%, d'autres seulement 5%. Vous pouvez consulter le résumé du projet CiviCRM sur Transifex ([http://www.transifex.net/projects/p/civicrm/](http://www.transifex.net/projects/p/civicrm/)) pour voir l'état de la traduction d'une langue. Vous pouvez télécharger et installer la traduction dans votre instance de CiviCRM pour évaluer si cela répondra à vos besoins ou [consulter un site démo](https://civicrm.org/demo) s'il y en a un de disponible dans votre langue.

En français, il y a deux traductions de CiviCRM: une plus générale qui devrait répondre aux besoins de la France, de la Belgique, de la Swisse et des autres pays francophones, et une autre traduction qui est mieux adaptée aux besoins du Québec/Canada.

Il peut arriver que dans certaines situations, la traduction soit correcte, mais que vous auriez préféré utiliser un autre terme dans votre contexte. Dans ce cas, nous vous recommandons d'entrer en contact avec les autres traducteurs pour en discuter. Pour les traductions françaises, vous pouvez poster sur le [forum francophone](https://forum.civicrm.org/index.php?board=58.0).

Installation de CiviCRM en français
-----------------------------------

Nous recommandons de configurer CiviCRM en français dès l'installation initiale. Il est possible de changer la langue après l'installation, mais ceci ne reconfigurera pas les nombreuses configurations de CiviCRM (liste de types d'adresses, types d'activités, modèles de messages, etc). Les étapes ci-dessous sont pour le français, mais s'appliquent également pour toute autre langue.

Pour installer CiviCRM en français:

1 - Téléchargez la distribution de traductions - civicrm-(version)-l10n.tar.gz - sur la [page de téléchargement de CiviCRM](https://www.civicrmfr.org/telecharger). Cette archive contient tous les fichiers des dernières traductions disponibles. Les langues sont incluses dans ce fichier quand elles atteignent 20% d'achèvement.

2 - Décompresser l'archive, vous verrez un répertoire appelé civicrm, contenant deux sous-répertoires appelés `l10n` et `sql`. Le répertoire l10n contient un ensemble de sous-répertoires nommés à l'aide de leurs codes de langue. Par exemple: le fichier de traduction pour le français du Canada sera situé dans `/civicrm/l10n/fr_CA/civicrm.mo`. Le fichier des configurations initiales sera dans `/civicrm/sql/civicrm_data.fr_CA.mysql`.

3 - Copiez ces répertoires `l10n` et `sql`, ainsi que tous leurs sous-répertoires dans votre répertoire racine CiviCRM comme indiqué ci-dessous. (Note: si vous créez manuellement le dossier "l10n", il doit s'écrire : "(elle minuscule)-dix-n", c'est une abréviation commune pour le mot « localisation »)

-   Pour Joomla : `site_root/administrator/component/com_civicrm/civicrm`. Ex : Si vous voulez la langue `fr_FR`, vous devriez avoir : `site_root/administrator/components/com_civicrm/civicrm/l10n/fr_FR/civicrm.mo` et `site_root/administrator/components/com_civicrm/civicrm/sql/civicrm_data.fr_FR.mysql`.
-   Pour Drupal : `site_root/sites/all/modules/civicrm`. Ex : Si vous voulez la langue `fr_FR` : `site_root/sites/all/modules/civicrm/l10n/fr_FR/civicrm.mo` et `site_root/sites/all/modules/civicrm/sql/civicrm_data.fr_FR.mysql`.
-  Pour Wordpress : `site_root/wp-content/plugins/civicrm/civicrm`. Notez le double civicrm! Donc si vous voulez la langue fr_FR, vous aurez : `site_root/wp-content/plugins/civicrm/civicrm/l10n/fr_FR` et `site_root/wp-content/plugins/civicrm/civicrm/sql/civicrm_data.fr_FR.mysql`.

Mise à jour de vos fichiers de traduction
-----------------------------------------

Les fichiers "civicrm-(version)-l10n.tar.gz" sont mis à jour lors d'une nouvelle version de CiviCRM.

Mais vous pouvez avoir besoin de mettre à jour vos fichiers de traduction avant la prochaine version pour diverses raisons:

-  Vous participez à l'amélioration de la traduction de CiviCRM dans votre langue.
-  Une chaîne a été mal traduite et vous êtes impatient de la corriger.
-  Une chaîne avec un mauvais balisage (ex: la syntaxe du lien ou la variable placeholder a été mal saisie, causant des bugs, en particulier bugs javascript impair, des parties de l'écran qui ne peut pas être chargé, etc).

Si tel est le cas, la meilleure façon de mettre à jour vos traductions régulièrement est d'utiliser l'extension "l10n update" : [https://github.com/cividesk/com.cividesk.l10n.update/](https://github.com/cividesk/com.cividesk.l10n.update/)

L'extension "l10n update" effectuera une vérification quotidienne pour mettre à jour les fichiers de traduction pour le noyau CiviCRM, ainsi que pour les extensions.

Vous pouvez aussi faire la mise à jour manuellement. Tous les jours, à 10h00, heure du Pacifique, le site Web CiviCRM met à jour les fichiers de traductions. Ils sont disponibles à l'adresse suivante: `https://download.civicrm.org/civicrm-l10n-core/mo/xx_XX/civicrm.mo`.

Par exemple:

- fr_FR: https://download.civicrm.org/civicrm-l10n-core/mo/fr_FR/civicrm.mo
- fr_CA: https://download.civicrm.org/civicrm-l10n-core/mo/fr_CA/civicrm.mo

Pour plus d'information vous pouvez consulter la page wiki : [https://wiki.civicrm.org/confluence/display/CRMDOC/i18n+Administrator's+Guide%3A+Using+CiviCRM+in+your+own+language](https://wiki.civicrm.org/confluence/display/CRMDOC/i18n+Administrator's+Guide%3A+Using+CiviCRM+in+your+own+language) (en anglais).

Les aides à la traduction
-------------------------

Bien que certaines traductions soient encore en cours de développement, un certain nombre d'aides dans CiviCRM soutiennent la communauté dans ses efforts de traduction. Notamment :

1.  Transifex est un outil en ligne qui permet aux groupes de traducteurs de traduire des chaînes de texte et de garder un aperçu de ses progrès. [Inscrivez-vous](https://www.transifex.com/signup/), recherchez votre langue, rejoignez l'équipe ou, si votre langue n'est pas disponible, commencez à traduire.
2.  Un glossaire 
    ([http://wiki.civicrm.org/confluence/display/CRM/Glossary+for+translations](http://wiki.civicrm.org/confluence/display/CRM/Glossary+for+translations))  
    Le wiki de CiviCRM vous aidera à maintenir la cohérence de vos traductions. Il vous aidera également à obtenir un aperçu de la quantité de travail à fournir pour traduire les chaînes de texte que vos utilisateurs verront le plus souvent et qu'il serait donc le plus utile à traduire.
3.  Une page wiki sur les astuces 
    ([http://wiki.civicrm.org/confluence/display/CRMDOC/Localisation+community+building+howto](http://wiki.civicrm.org/confluence/display/CRMDOC/Localisation+community+building+howto))
    Explique comment aborder le processus de localisation. 
4.  Une « foire aux questions »
    ([http://wiki.civicrm.org/confluence/display/CRMDOC/Internationalisation+FAQ)](http://wiki.civicrm.org/confluence/display/CRMDOC/Internationalisation+FAQ). Cette page wiki de CiviCRM couvre les questions les plus fréquentes sur la localisation.

Comment commencer une traduction ? 
---------------

Vous souhaitez aider la communauté à traduire CiviCRM dans une nouvelle langue ou améliorer la traduction en cours? Voici comment le faire (à condition d'avoir un peu d'expérience technique) :

1.  Aller sur transifex.net et créer un compte.
2.  Recherchez votre langue sur  
    [http://www.transifex.net/projects/p/civicrm/teams/](http://www.transifex.net/projects/p/civicrm/teams/)
    ...et rejoignez une équipe, ou demandez la création d'un nouveau language si nécessaire.
3.  Commencez à traduire!

### Un travail d'équipe

Le flux de travail de traduction de CiviCRM est encore en cours jusqu'à ce que le processus devienne plus mature, vous pouvez  vous référer à cette page pour de plus récentes instructions : 
[http://wiki.civicrm.org/confluence/pages/viewpage.action?pageId=88408149](http://wiki.civicrm.org/confluence/pages/viewpage.action?pageId=88408149)

Le travail de traduction est fortement basé sur le travail d'équipe. J'espère que vous avez déjà une équipe de traducteurs pour votre langue. Cette équipe doit construire un glossaire, lancer un jeu de traduction, réviser vos traductions et apporter une critique constructive. Si une telle équipe n'existe pas encore, c'est l'occasion de créer la vôtre.

Composants et fichiers
--------------------

Il ya beaucoup de chaînes (phrases) à traduire dans CiviCRM. Pour faciliter la traduction de la partie qui vous intéresse (espérons celle que vous connaissez le mieux), les chaînes qui ont besoin de traduction ont été divisées en *composants*, qui sont des plugins de CiviCRM (CiviCRM, CiviMail, CiviContribute, etc. .). Un composant distinct est disponible pour chaque version de CiviCRM, à partir de la version 3.2 

Chaque composant contient un certain nombre de fichiers, qui contiennent eux-mêmes les chaînes à traduire. Le composant principal "CiviCRM" (le *noyau*) contient près de 20 fichiers (pour *Pays*, *Provinces*, *Menu*, etc.).

Outils et détails techniques
---------------------------

Vous avez deux processus pour effectuer la traduction : en ligne ou hors ligne selon votre choix. La traduction en ligne ne nécessite pas l'installation d'un logiciel. La traduction hors ligne se fait en téléchargeant les fichiers à partir du site de traduction, avec un logiciel qui offre plus de fonctionnalités que le système en ligne.

### Traduction en ligne 

Transifex est l'outil à utiliser pour la traduction en ligne. Il n'a pas autant de fonctionnalités qu'un outil hors ligne tel que PoEdit, mais c'est la manière la plus simple de contribuer aux traductions et de faire des corrections rapides et occasionnelles. Chaque traducteur doit avoir un compte sur le site Transifex, car les équipes de traduction utilisent les forums et le système de messagerie pour coordonner leur travail.

Les étapes de base de la traduction en ligne sont les suivantes:

1.  Sélectionnez un composant sur  
    [http://www.transifex.net/projects/p/civicrm/](http://www.transifex.net/projects/p/civicrm/). 
    Cela affiche la liste des équipes linguistiques pour ce composant.
2.  Cliquez sur l'icône dans la colonne Options à côté de la langue qui vous intéresse. Cela vous amène à la liste des fichiers de ce composant.
3.  Cliquez sur l'icône "crayon et papier". Cela vous amène à l'écran de traduction en ligne, qui répertorie toutes les chaînes traduisibles dans ce fichier.
4.  Pour chaque chaîne, vous pouvez saisir une traduction.
5.  Lorsque vous avez terminé, cliquez sur le bouton «Envoyer pour examen» à la fin de la page.

### Construire une mémoire de traduction

PoEdit et d'autres logiciels de traduction vous aideront à construire une mémoire de traduction pour votre langue. Cette mémoire de traduction peut soit être restreinte aux traductions effectuées dans CiviCRM, soit inclure des traductions d'autres projets. Si vous incluez d'autres projets, la traduction automatique peut traduire plus de chaînes, mais vous perdrez la cohérence et la plupart des chaînes seront marquées comme floues. Cela pourrait être cependant un moyen de démarrer une nouvelle traduction.

Construire une mémoire de traduction basée sur des mots du glossaire peut être un travail assez long pour assurer la cohérence du travail de votre équipe.
 
### Utilisation du contrôle de version (principalement pour les programmeurs)

Transifex conserve les fichiers dans un système de contrôle de version : 
[http://github.com/civicrm/l10n](http://github.com/civicrm/l10n). Ceci est utile à certains utilisateurs qui trouvent l'interaction avec le site Github plus facile que le téléchargement de chaque fichier séparément par Transifex. 

### Cohérence et consensus 

Afin d'assurer une bonne cohérence dans la traduction, chaque équipe est encouragée à construire et à utiliser un glossaire et à utiliser l'examen par les pairs. Vous pouvez trouver un glossaire de termes communs sur
[http://wiki.civicrm.org/confluence/display/CRM/Glossary+for+translations](http://wiki.civicrm.org/confluence/display/CRM/Glossary+for+translations). 
Vous devez absolument traduire ces termes dans votre langue et vous assurer que votre équipe parvienne à un consensus sur tous les termes définis.

Construire et partager une mémoire de traduction commune est comme un glossaire spécialisé qui peut être utilisé automatiquement par des outils de traduction contribue également à assurer la cohérence. Le système d'aide de PoEdit explique comment construire cette base de données (la plupart des autres logiciels de traduction en font autant).

Esprit d'équipe et réunion participative
----------------------------------------
Une bonne façon de faire des progrès dans la traduction est d'organiser des *réunions de traduction*. Cela implique d'amener autant de personnes que possible dans la même salle pour traduire autant de documents que possible. Voici quelques points à garder à l'esprit lors de l'organisation d'une réunion de traduction:


- Choisissez un bureau agréable, où vos collègues pourront se connecter en ligne (suffisamment d'ordinateurs pour tout le monde, ou des pupitres pour installer des ordinateurs portables avec une bonne connexion Internet).
-  Donnez au préalable des instructions sur la façon d'installer un outil de traduction hors ligne tel que PoEdit, et avoir des personnes prêtes à aider les autres pour l'installer et l'utiliser.
- Créez le glossaire avant la réunion et imprimez une quantité suffisante de copies. Présentez le glossaire, discutez des termes qui n'ont pas de consensus.
- Déterminez les objectifs de la réunion : quel composant sera traduit et quel pourcentage votre équipe essaie d'atteindre.
- Créez des sous-équipes avec des objectifs clairs: par composant ou fichier ou une partie de celui-ci.
- Si vos traducteurs ne sont pas familiers avec CiviCRM, faites une démonstration des fonctionnalités que votre équipe est sur le point de traduire.
- Désignez clairement quelqu'un qui peut être interrompu pour répondre aux questions.
- Assurez-vous que vous avez en réserve suffisamment de café, de thé, de chocolat, etc... pour que tout le monde passe la nuit !
- A la fin de la réunion, présentez le résultat de la traduction dans une installation de démonstration CiviCRM .
- Débattez pour savoir si l'équipe a atteint son objectif et comment l'améliorer.


