Relations entre contacts
=============

CiviCRM vous permet de représenter les connexions entre les contacts en créant des relations. Exemple, si une mère et son fils sont tous les deux dans votre base de données, il peut être utile de pouvoir regarder l'un ou l'autre des dossiers et voir qu'ils sont liés l'un à l'autre.

Vous pouvez également suivre les relations entre les organisations, ou entre les contacts individuels et les organisations. Par exemple, la saisie d'une organisation dans le domaine de l'employeur actuel de l'enregistrement d'un contact individuel crée automatiquement une relation «employé de l'individu à l'organisation", et une relation «employeur de l'organisation à l'individu".

Créer des relations entre contacts
---------------------------------------

![image](/img/4.5%20Add%20Relationship.png)

1. Accédez à l'un des enregistrements que vous souhaitez relier.
2. Cliquez sur **Ajouter une relation** dans le bouton **Actions** du résumé de contact ou dans l'onglet Relations
3. Sélectionnez le type de relation. Dans ce cas, ce serait soit «Enfant de» ou «Parent de».
4. Commencez à saisir le nom de famille de la ou des personne(s) concernée(s). Si le contact que vous souhaitez connecter n'existe pas encore dans la base de données, vous pouvez créer un nouveau contact à partir de cet écran.
5. Vous pouvez également saisir des informations supplémentaires, notamment la date de début et la date de fin (dans le cas où la relation est limitée dans le temps), la description et les notes. Il existe également deux options d'autorisation, qui permettent aux utilisateurs de la base de données de modifier cet enregistrement. Enfin, la zone Activé, qui est cochée par défaut, indique que la relation est active, .
6. Lorsque vous avez effectué les modifications souhaitées, cliquez sur **Enregistrer la relation**.

Relier les employés et les employeurs
-------------------------------------

Une façon rapide de relier les employés (qui sont stockés dans CiviCRM en tant qu'individus) aux employeurs (stockés en tant qu'organisations) consiste à utiliser le champ Employeur actuel dans le dossier d'une personne. Cela définira le champ employeur actuel dans l'enregistrement de contact et créer une relation entre les contacts.

1. Accédez à l'enregistrement de l'individu que vous souhaitez connecter à une organisation.
2. Cliquez sur le bouton Modifier pour modifier l'enregistrement de l'individu.
3. Commencez à taper le nom de l'organisation dans le champ Employeur actuel. Au fur et à mesure que vous tapez, les noms correspondants des organisations qui existent déjà en tant que contacts dans CiviCRM apparaissent dans une liste déroulante de saisie semi-automatique sous le champ Employeur actuel. Si l'organisation est déjà un contact dans CiviCRM, vous pouvez la sélectionner dans la liste déroulante en appuyant sur la flèche vers le bas ou en cliquant dessus. Si l'organisation n'existe pas déjà en tant que contact CiviCRM, entrez simplement le nom complet de l'organisation.
4. Une fois que le nom complet de l'organisation est entré dans le champ Employeur actuel, appuyez sur la touche Entrée ou cliquez sur le bouton Enregistrer. Si l'organisation est un contact préexistant, une relation Employé / Employeur sera créée entre le particulier et l'organisation. Si l'organisation n'existe pas déjà, un nouveau contact d'organisation sera créé et la relation sera créée entre l'individu et l'organisation. Vous pouvez cliquer sur l'onglet Relations pour afficher votre relation nouvellement créée et voir les relations existantes.

Ajout de contacts aux organisations
-----------------------------------

1. Sélectionnez les contacts souhaités dans vos résultats de recherche comme décrit ci-dessus.
2. Sélectionnez **Ajouter une relation - à l'organisation dans le menu déroulant** dans le menu Actions.
3. Dans l'écran **Ajouter des contacts à l'organisation**, sélectionnez **Type de relation** dans le menu déroulant.
4. Entrez une partie du nom de l'organisation souhaitée dans le champ **Rechercher l'organisation cible**, puis cliquez sur **Rechercher**.
5. Les organisations qui correspondent à votre recherche apparaîtront dans la zone **Marquez les contacts cibles pour cette relation** située sous les boutons Rechercher et Annuler. Si l'organisation que vous recherchez apparaît dans cette liste, cliquez sur le bouton radio en regard de cette organisation, puis cliquez sur le bouton **Ajouter à l'organisation** ci-dessous. Si l'organisation que vous recherchez n'apparaît pas dans cette liste, essayez d'entrer quelque chose de différent dans le champ **Trouver une organisation cible** et de cliquer sur **Rechercher** à nouveau. Si vous ne parvenez toujours pas à trouver votre organisation souhaitée, elle peut ne pas exister. Cliquez sur **Annuler**, ajoutez une nouvelle organisation et réessayez.
6. Une fois que vous avez choisi une organisation et cliquez sur le bouton **Ajouter à l'organisation**, vous devriez voir un message indiquant que le nombre de participants que vous avez sélectionné a été ajouté à l'organisation.
7. Cliquez sur **Terminé** pour revenir aux résultats de votre recherche.

Ajout de contacts aux ménages
-----------------------------

1. Sélectionnez les contacts souhaités dans vos résultats de recherche comme décrit ci-dessus.
2. Sélectionnez **Ajouter une relation - au ménage** dans le menu déroulant **Actions**.
3. Sélectionnez le **Type de relation** dans le menu déroulant. Notez que si CiviCRM ne vous empêche pas d'ajouter plusieurs contacts comme **chef de ménage** pour un seul ménage, cela peut causer des problèmes plus tard dans toute situation où vous attendez **chef de ménage** de se référer à un seul Par ménage. Par conséquent, l'option **membre du ménage de** peut être le meilleur choix dans la plupart des situations.
4. Entrez une partie du nom du ménage auquel vous ajoutez des contacts (tel qu'un nom de famille partagé par les membres du ménage) dans le champ **Rechercher ménage cible**, puis cliquez sur **Rechercher**.
5. Les ménages qui correspondent à votre recherche apparaîtront dans la zone **Marquez les contacts cibles pour cette relation** située sous les boutons Rechercher et Annuler. Si le ménage que vous recherchez apparaît dans cette liste, cliquez sur le bouton radio en regard de ce ménage, puis cliquez sur le bouton **Ajouter au ménage** ci-dessous. Si le ménage que vous recherchez n'apparaît pas dans cette liste, essayez d'entrer quelque chose de différent dans le champ **Rechercher un ménage cible** et de cliquer **Recherche** à nouveau. Si vous ne trouvez toujours pas le ménage désiré, il peut ne pas exister. Cliquez sur le bouton **Annuler**, ajoutez un nouveau ménage et réessayez.
6. Une fois que vous avez choisi un ménage et cliqué sur le bouton **Ajouter au ménage**, vous devriez voir un message indiquant que le nombre de participants que vous avez sélectionné a été ajouté au ménage.
7. Cliquez sur **Terminé** pour revenir aux résultats de votre recherche.

Création de nouveaux types de relations
---------------------------------------

CiviCRM fournit par défaut une liste de types de relations répandus qui peut être utilisée pour indiquer les relations entre les contacts. Si vous avez besoin de définir d'autres types de relations entre vos contacts, vous pouvez créer vos propres types de relation.

1.  Dans le menu de navigation, allez à **Administrer > Personnaliser les données et écrans > Types de relations**.
2.  Réexaminez la liste des types de relations existants pour vous assurez que vous n'allez pas créer un doublon.
3.  Si le type de relation dont vous avez besoin n'existe pas déjà, cliquez sur le bouton **Ajouter un type de relation**.
4.  Renseignez les libellés de description pour le type de relation que vous êtes en train de créer dans les champs **Libellé de type de relation A vers B** et **Libellé de type de relation B vers A**. Le **Libellé de type de relation A vers B** décrit la relation du contact A par rapport au contact B ; le **Libellé de type de relation B vers A** décrit la relation du contact B par rapport au contact A**.  
      -  Certaines relations peuvent être décrites de la même façon quelque soit le sens ; Dans ce cas, vous pouvez décrire la relation uniquement dans le champ **Libellé de type de relation A vers B**. Par exemple, pour décrire la relation entre deux collègues de travail nommés Sylvia et Audre, vous pouvez dire que Sylvia est "collègue de" Audre et que Audre est "collègue de" Sylvia. Par conséquent, il suffira d'écrire "collègue de" uniquement dans le champ **Libellé de type de relation A vers B**, et laisser **Libellé de type de relation B vers A** vide.
      -  Dans d'autres situations, il n'est pas possible d'appliquer une description unique qui fonctionne dans les deux sens ; Dans ce cas, vous aurez besoin d'entrer une description différente dans chaque champ. Par exemple, vous pouvez dire que Yuki est la "grand-mère de" Kiyoshi, mais vous ne pouvez pas dire que Kiyoshi est "la grand-mère de" Yuki. Par conséquent, il faudra écrire "grand-mère de" dans le champ **Libellé de type de relation A vers B** et "petite fille de" dans le champ **Libellé de type de relation B vers A**.
7.  Utilisez les champs **Type de contact A** et "Type de contact B** pour indiquer quels types de contacts sont concernés par votre relation. N'oubliez pas de vérifier que les types de contacts que vous selectionnez pour Contact A et Contact B soient cohérents par rapport aux libellés de description correspondants.
8.  Renseignez éventuellement le champ **Description de la relation" pour ce type de relation. Cela est particulièrement utile si l'objectif voulu de ce type de relation peut ne pas être évident pour tout le monde.
9.  Laissez active la case à cocher **Le type de relation est actif** à moins que vous n'ayez l'intention de créer ce type de relation sans toutefois permettre aux autres utilisateurs de l'utiliser avant une certaine date.
10. Cliquez sur le bouton **Enregistrer**. Vous verrez un message vous indiquant que le type de relation a été sauvegardé et il apparaitra dans la liste en dessous.


Désactiver ou supprimer des types de relation inutiles
------------------------------------------------------

Si un type de relation n'est plus utile ou pertinent pour votre organisation, vous pouvez soit le désactiver, soit le supprimer pour qu'il ne fasse ainsi plus partie des options dans les nouvelles relations. Désactiver plutôt que de supprimer un type de relation présente deux avantages majeurs : vous serez toujours capable de visualiser les données utilisant toujours ce type de relation, et vous pouvez facilement réactiver ce type de relation si le besoin s'en fait à nouveau sentir.

1.  Dans le menu de navigation, allez à **Administrer > Personnaliser les données et écrans > Types de relations**.
2.  Cliquez sur le lien **plus** de la ligne du type de relation que vous souhaitez désactiver ou supprimer.
3.  Dans le menu contextuel, sélectionnez **Désactiver** ou **Supprimer**.
4.  Si vous sélectionnez **Désactiver**, une bulle de demande de confirmation apparaitra. Si vous sélectionnez **Supprimer**, vous serez redirigé vers un nouvel écran qui vous affichera un avertissement plus sérieux et vous demandera une confirmation. Vérifiez les informations fournies et si vous êtes sûr de vouloir continuer cette action, cliquez sur le bouton **Supprimer**. Dans le cas contraire, cliquez sur **Annuler**.
5.  Si vous avez choisi de désactiver un type de relation, il apparaitra en gris dans la liste Types de relations et les relations sont toujours visibles dans l'affichage des contacts. Si vous avez choisi de supprimer le type de relation, il n'apparaitra plus dans la liste Types de relations et dans les données de relation des contacts. De plus, les utilisateurs ne pourront plus créer de nouvelles relations de ce type.
6.  Pour activer un type de relation précédemment désactivé, suivez les étapes 1 et 2 ci-dessus puis sélectionnez **Activer** du menu contextuel **plus**.
