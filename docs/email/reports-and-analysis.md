Rapports et analyse
====================

CiviMail dispose de nombreux outils pour le reporting et l'analyse ; 
le reporting est une des raisons clés pour utiliser CiviMail.

Un rapport pour chaque envoi de courriel
----------------------------------------

Vous pouvez visualiser un rapport pour chaque mail individuel depuis
**Envois en masse > Envois programmés et courriels envoyés**. Ces
rapports présentent les statistiques vivantes à propos de votre envoi ;
vous pouvez suivre vos courriels en temps réel en actualisant la page.
Chaque rapport d'envoi de courriel est découpé en quelques sections.
En fonction de votre paramétrage pour l'envoi, plus ou moins de données
sont disponibles. 

### Résumé de livraison

![report_email](/img/report_email-en.gif "report_email")

Le résumé de livraison affiche des statistiques de haut niveau à propos
de votre envoi en masse.
En cliquant sur les liens dans ce résumé, vous verrez une liste de contacts
qui ont réalisé telle ou telle action.

**Destinataires prévus** affiche le nombre de personnes prévu auquel l'envoi a été adressé.

**Ouvertures suivies** affiche le nombre de personnes qui ont ouvert le courriel, selon CiviCRM *si vous avez activé le paramètre de suivi des ouvertures*.

**Note :** Dans le monde de l'emailing, il n'existe aucun moyen fiable à 100%
de savoir quand quelqu'un a ouvert un courriel. CiviCRM utilise une astuce qui est
commune chez les fournisseurs d'envois en masse - il intègre une petite image
avec un nom unique dans chaque courriel. Lorsqu'un client affiche le courriel et
télécharge l'image, CiviCRM sait qu'il a ouvert/lu le courriel. Comme cette technique est
généralisée, pour protéger la vie privée, la plupart des clients de messagerie demandent
aux utilisateurs de confirmer s'ils souhaitent télécharger les images des courriels
qu'ils recoivent. Cela signifie que le rapport statistique vous indique plutôt le nombre
de personnes qui ont téléchargé les images que le nombre de lecteurs du courriel ;
le nombre réel de lecteurs est toujours supérieur au nombre affiché dans le rapport. 
Les statistiques d'ouvertures devraient être considérées comme indicatives, et non précises.
D'après notre expérience, un taux d'ouverture de 30% peut être considéré comme bon. C'est
évidemment différent pour chaque organisation et chaque groupe auquel vous envoyez
des envois en masse.

Ne vous focalisez pas trop sur les chiffres en valeur absolue, mais utilisez-les plutôt
comme une façon de comparer les différents envois que vous envoyez. Par exemple ils peuvent
vous permettre de comparer et expérimenter différentes dispositions, styles d'écriture
et longueurs de texte. Voyez ce qui fonctionne le mieux pour vos lecteurs.

**Ouvertures par clics** indiquent le nombre total de fois où les destinataires ont cliqué sur un lien dans votre courriel *si vous avez activé le suivi des clics*.

**Transferts** indique le nombre de fois où les destinataires ont transféré le courriel
en utilisant le lien "faire suivre" (C'est un jeton que vous pouvez inclure dans votre envoi).

**Réponses** indique le nombre de fois où des destinataires ont répondu au courriel *si vous avez activé le suivi des réponses*.

**Rebonds (bounces)** indique le nombre d'adresses de courriel en échec, qui n'ont pas pu être
livrées avec succès *si vous avez activé le traitement des rebonds (bounces)*.

**Demandes de désabonnement** indique le nombre de personnes qui ont cliqué sur un des liens de désabonnement que vous incluez dans votre courriel.

Gérer les rebonds (bounces) et les contacts avec des adresses de courriel invalides
-------------------------------------------------------------------

Si votre serveur est configuré pour traiter les rebonds, les contacts seront marqués comme
**Suspendus** lorsque leur adresse de courriel est en échec. Les messages expédiés ultérieurement à cette adresse seront supprimés. Vous pouvez lister les adresses de courriel suspendues soit à partir du rapport "Rebonds/Bounces", soit à partir de la recherche avancée, puis
chercher pourquoi les courriels rebondissent.

Vous pouvez consulter une liste de rebonds en cliquant sur le lien **Rebonds (Bounces)**
dans le Résumé de livraison. Vous pouvez y voir les raisons des rebonds individuels : adresses de courriel incorrectes (par exemple, contact@goooogle.com)... vous pouvez aussi les corriger, et supprimer leur statut "Suspendu". Vous pouvez ensuite réutiliser le mailing et simplement "EXCLURE" ces courriels invalides des listes de destinataires sur l'écran 
"Sélectionnez des Destinataires" de la configuration de l'envoi en masse.

Dans la zone "Envois en masse" de **Recherche > Recherche avancée**, vous pouvez rechercher par
type de rebond.

![image](/img/advanced_search_mailing_bounce_type.png) 

Résumé des ouvertures de clics
------------------------------

Dans cette section, les statistiques de clics sont affichées pour chaque lien.
Il existe deux statistiques, **Clics** (c'est-à-dire le nombre de fois qu'un lien a été cliqué) et **Clics uniques** (c'est-à-dire le nombre de personnes qui ont cliqué sur des liens).

![image](/img/Screen%20shot%202011-08-27%20at%2016.28.28.png)

Envoi de rapports avec CiviReport
-------------------------------

Le composant Rapports comporte quatre rapports : Rapports de Rebonds de Courriels, Synthèse des envois en masse, Rapport d'ouvertures de clics des envois en masse et Rapport d'ouvertures d'envois en masse qui utilisent les
fonctions décrites ci-dessus. Voici les principaux avantages de consulter les rapports via le composant Rapports (disponible à partir du menu **Rapports**) :

- Vous pouvez exécuter un rapport pour plusieurs envois en masse, en une fois.
- Vous avez accès à toutes les autres fonctionnalités intéressantes du composant Rapports, y compris la possibilité d'ajouter des rapports aux tableaux de bord, d'envoyer des rapports par courriel, etc.

Lisez la section *Rapports* de ce livre pour plus d'informations.