# standard-patrimoine-naturel-ou-materiel
Ce schéma permet de modéliser les différents attributs des éléments constituant notre patrimoine naturel ou matériel.

On entend par Patrimoine naturel ou matériel, les types suivants de patrimoine: 
 - Petit patrimoine
 - Patrimoine naturel
 - Patrimoine architectural
 - Patrimoine artistique

Un jeu de données basé sur ce standard devra contenir un seul type de patrimoine.

Pour chacun de ces types de patrimoines, une liste de catégories de pattrimoines a été défini. Vous retrouvez cette liste dans la description du champ "Cat&eacute;gorie du patrimoine (category)" dans la section "Description du schéma" ci-dessous.

## Contexte

Il existe un besoin d'harmonisation de la publication en open data de données essentielles produites par les administrations publiques wallonnes. En juin 2023, près de 700 jeux de données sont publiés sur le portail [Open Data Wallonie Bruxelles (ODWB)](https://www.odwb.be/explore/?sort=modified), qui sont très hétérogènes. 

Constatant la production de jeux de données disparates à l'échelle de la fédération Wallonie-Bruxelles, FuturoCité a réuni, dans le cadre d'un groupe de travail sollicité depuis mai 2021, une vingtaine de collectivités. La concertation de celles-ci a permis 1) d'identifier collectivement des jeux de données jugés prioritaires et 2) de s'accorder sur des spécifications des modèles de données. 
La standardisation de ces données prioritaires est en effet essentielle pour s'assurer de leur publication homogène et de faciliter leur exploitation (notamment leur agrégation) par les réutilisateurs. Elle facilitent l'exploitation des données publiées par les réutilisateurs (agrégation, consolidation et traitements automatiques).

## Construction du schéma de données 

Les membres du groupe de travail ont défini un schéma de données qui décrit le format des fichiers, les différents champs, les valeurs possibles… Ils se sont appuyés sur un état des lieux du patrimoine de données des collectivités wallonnes et sur une étude des modèles utilisés par des collectivités déjà productrices de ces données (notamment Liège et Namur), en prenant en compte les retours faits par les réutilisateurs de données. 

## Description du schéma

Un [gabarit au format tableur](https://github.com/FuturoCite/standard-patrimoine-naturel-ou-materiel/blob/main/Schema_patrimoine_naturel_ou_materiel_gabarit.xlsx) est également prévu pour faciliter la publication d'un jeu de données conforme au format du schéma.

Un exemple valide au format CSV est consultable [ici](https://github.com/FuturoCite/standard-patrimoine-naturel-ou-materiel/blob/main/exemple-valide.csv). 

La tableau ci-dessous donne un aperçu des champs du schéma. 

<table>
	<tbody>
		<tr>
			<td><strong>Nom</td>
			<td><strong>Remplissage obligatoire/optionnel</td>
			<td><strong>Description</td>
		</tr>
		<tr>
			<td>Identifiant (id)</td>
			<td>Obligatoire</td>
			<td>Ce champ contient un identifiant unique local. Le producteur de donn&eacute;es le g&eacute;n&egrave;re en associant&nbsp; le code INS de la commune dans laquelle se situe le patrimoine &agrave; un nombre. Ce champ permet d'&eacute;viter localement les doublons. Le code INS de la commune est accessible ici : https://statbel.fgov.be/fr/open-data/code-refnis</td>
		</tr>
		<tr>
			<td>Type de patrimoine (type)</td>
			<td>Obligatoire</td>
			<td>Ce champ indique le type de patrimoine pr&eacute;sent dans ce jeu. Les valeurs possibles sont : Petit patrimoine, Patrimoine naturel, Patrimoine architectural, Patrimoine artistique</td>
		</tr>
		<tr>
			<td>Cat&eacute;gorie du patrimoine (category)</td>
			<td>Optionnel</td>
			<td width="591">Ce champ indique la cat&eacute;gorie du patrimoine pr&eacute;sent dans ce jeu. Pour un jeu de donn&eacute;es de type Petit patrimoine, les valeurs possibles sont : "Point d&rsquo;eau", "Petit patrimoine sacr&eacute;", "Ouvertures", "Signalisation", "D&eacute;limitation", "Eclairage", "Mesure du temps et de l&rsquo;espace", "Justice et libert&eacute;s", "Repos", "Ornementation en fer", "Patrimoine militaire et comm&eacute;moratif", "Arbre remarquable", "Outil ancien", "Art d&eacute;coratif", "Bien relatif &agrave; la faune, la flore ou aux min&eacute;raux", "Transport", "Atelier". Pour un jeu de type Patrimoine naturel, les valeurs possibles sont : "Parc et jardin", "Point d'eau (lac, &eacute;tang, &hellip;)", "Terril", "R&eacute;serve naturelle et site d'int&eacute;r&ecirc;t biologique", "Bois et for&ecirc;t", "Cours d'eau", "Cascade", "Arbre remarquable", "Formation g&eacute;ologique", "Vignoble", "Autre".&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; Pour un jeu de type Patrimoine architectural, les valeurs possibles sont : "Ferme et grange", "Ch&acirc;teau", "Fortification", "Moulin", "Lieu de culte (Eglise, chapelle, abbaye, coll&eacute;giale, &hellip;)", "Fontaine et lavoir", "Sculpture et statue", "Beffroi et tour", "Habitation", "Hospice", "Commerce et Horeca", "B&acirc;timent industriel", "Four, meule, pressoir", "Cimeti&egrave;re", "Monument comm&eacute;moratif", "Ecole", "B&acirc;timent public", "Ch&acirc;teau d'eau", "Ouvrage d'art (pont, tunnel, &eacute;cluse, &hellip;)", "Gare", "Site arch&eacute;ologique", "Autre".<br />Pour un jeu de type Patrimoine artistiques, les valeurs possibles sont : "Peinture, dessin, &hellip;", "Outil", "Sculpture", "Objet d'art", "Mobilier", "Manuscrit, livre, &hellip;", "Photographie", "Gravure", "Tapisserie", "Autre"</td>
		</tr>
		<tr>
			<td>Nom (name)</td>
			<td>Obligatoire</td>
			<td>Ce champ contient le nom du patrimoine</td>
		</tr>
		<tr>
			<td>Description (description)</td>
			<td>Obligatoire</td>
			<td>Ce champ contient la description du patrimoine</td>
		</tr>
		<tr>
			<td>Photo (picture)</td>
			<td>Optionnel</td>
			<td>Ce champ contient une url renvoyant &agrave; une photo du patrimoine</td>
		</tr>
		<tr>
			<td>Nom de la commune (municipality)</td>
			<td>Obligatoire</td>
			<td>Ce champ contient le nom de la commune dans laquelle se situe le patrimoine. Le nom de la commune provient de la base de donn&eacute;es BeST Address : https://opendata.bosa.be/index.fr.html&nbsp; ou de la liste des codes INS : https://statbel.fgov.be/fr/open-data/code-refnis&nbsp;</td>
		</tr>
		<tr>
			<td>Code INS (ins_code)</td>
			<td>Obligatoire</td>
			<td>Ce champ contient le code INS de la commune o&ugrave; se situe le patrimoine. Il est accessible ici :&nbsp; https://statbel.fgov.be/fr/open-data/code-refnis&nbsp;</td>
		</tr>
		<tr>
			<td>Partie de commune (zone_address)</td>
			<td>Optionnel</td>
			<td>Ce champ continent le nom de la partie de commune o&ugrave; se situe le patrimoine, conforme &agrave; l'appelation dans StatBel : https://statbel.fgov.be/fr/propos-de-statbel/methodologie/classifications/geographie</td>
		</tr>
		<tr>
			<td>Code INS de la partie de commune (ins_zone_address)</td>
			<td>Optionnel</td>
			<td>Ce champ contient le code INS de la partie de commune o&ugrave; se situe le patrimoine. La d&eacute;coupe g&eacute;ographique de StatBel Level 5 (NIS6) liste ces codes : https://statbel.fgov.be/fr/propos-de-statbel/methodologie/classifications/geographie</td>
		</tr>
		<tr>
			<td>Nom de rue (street_name)</td>
			<td>Obligatoire</td>
			<td>Ce champ renseigne le nom de la voirie o&ugrave; se situe le patrimoine (ou de la voirie la plus proche s'il n'est pas en voirie).</td>
		</tr>
		<tr>
			<td>Code rue BeSTAddress (street_number)</td>
			<td>Obligatoire</td>
			<td>Ce champ contient le code de la voirie o&ugrave; se situe le patrimoine dans la base de donn&eacute;es BeSTAdress (ou de la voirie la plus proche s'il n'est pas en voirie) : https://opendata.bosa.be/index.fr.html</td>
		</tr>
		<tr>
			<td>Code rue national (street_number_rrn)</td>
			<td>Optionnel</td>
			<td>Code de la voirie o&ugrave; se situe le patrimoine dans le registre national (ou de la voirie la plus proche s'il n'est pas en voirie)</td>
		</tr>
		<tr>
			<td>Num&eacute;ro de police le plus proche (house_number)</td>
			<td>Optionnel (recommand&eacute;)</td>
			<td>Ce champ est recommand&eacute;. Il contient le num&eacute;ro de police (num&eacute;ro de maison) le plus proche du patrimoine</td>
		</tr>
		<tr>
			<td>Distance au point d'adresse (distance)</td>
			<td>Optionnel</td>
			<td>Ce champ indique la distance, en m&egrave;tres, entre le patrimoin et le point d'adresse le plus proche introduit via les autres champs (code_rue_bestadress, num_police, &hellip;). En cas de d&eacute;cimale, le s&eacute;parateur est le point.&nbsp;</td>
		</tr>
		<tr>
			<td>Coordonn&eacute;es (coordinates)</td>
			<td>Obligatoire</td>
			<td>Ce champ indique les coordonn&eacute;es du patrimoine. Il est au format GeoJSON (se r&eacute;f&eacute;rer au fichier csv d'exemple et/ou &agrave; la documentation pour un exemple de valeur bien format&eacute;e). S'il est impossible d'exporter la donn&eacute;e depuis un logiciel m&eacute;tier, les coordonn&eacute;es d'un lieu peuvent &ecirc;tre g&eacute;n&eacute;r&eacute;es ici : https://www.coordonnees-gps.fr/carte/pays/BE</td>
		</tr>
		<tr>
			<td>Geom&eacute;trie (geometry)</td>
			<td>Optionnel</td>
			<td>Ce champ indique la zone g&eacute;opgrahique du patrimoine gr&acirc;ce &agrave; une liste de coordonn&eacute;es. Cette liste est g&eacute;n&eacute;r&eacute;e &agrave; partir d'un fichier GPX. Ce champ est &agrave; compl&eacute;ter dans le cas d'un patrimoine s'&eacute;tendant sur une large zone tel qu'un parc, un jardin, &hellip;</td>
		</tr>
		<tr>
			<td>Contact (contact)</td>
			<td>Optionnel</td>
			<td>Ce champ contient les informations de contact. Nous recommandons d'indiquer uniquement le site web du patrimoine afin de faciliter la maintenance et mise &agrave; jour des donn&eacute;es</td>
		</tr>
		<tr>
			<td>Accessibilit&eacute; PMR (disabled_access)</td>
			<td>Optionnel</td>
			<td>Ce champ pr&eacute;cise si le patrimoine est accessible aux personnes &agrave; mobilit&eacute; r&eacute;duite. Si l'emplacement est accessible utiliser la valeur 'true'. Si non, la valeur 'false'. Si non applicable/non connu : ne pas renseigner ce champ.</td>
		</tr>
		<tr>
			<td>Description de l'accessibilit&eacute; (access_description)</td>
			<td>Optionnel</td>
			<td>Ce champ pr&eacute;cise tout information jug&eacute;e utile relative &agrave; l'accessibilit&eacute; : voiture, PMR,&nbsp;</td>
		</tr>
		<tr>
			<td>Public (public)</td>
			<td>Optionnel</td>
			<td>Ce champ pr&eacute;cise si le patrimoine appartient &agrave; une autorit&eacute; publique ou &agrave; un priv&eacute;. Les valeurs possibles sont : Public, Priv&eacute;. Si non applicable/non connu : ne pas renseigner ce champ.</td>
		</tr>
		<tr>
			<td>Class&eacute; (listed)</td>
			<td>Optionnel (recommand&eacute;)</td>
			<td>Ce champ est recommand&eacute;. Il pr&eacute;cise si le patrimoine est class&eacute;. Si le patrimoine est class&eacute; utiliser la valeur 'true'. Si non, la valeur 'false'. Si non applicable/non connu : ne pas renseigner ce champ.</td>
		</tr>
		<tr>
			<td>Class&eacute; par (listed_by)</td>
			<td>Optionnel</td>
			<td>Si le patrimoine est class&eacute;, ce champ contient le nom de l'organisme responsable de la reconnaissance.</td>
		</tr>
		<tr>
			<td>Date de cr&eacute;ation de la donn&eacute;e (created_date)</td>
			<td>Optionnel</td>
			<td>Ce champ indique la date de cr&eacute;ation de la donn&eacute;e dans le jeu. Il respecte le format ISO 8601 : ann&eacute;e-mois-jour (YYYY-MM-DD)</td>
		</tr>
		<tr>
			<td>Date de derni&egrave;re modification de la donn&eacute;e (last_modified_date)</td>
			<td>Optionnel</td>
			<td>Ce champ indique la date de la derni&egrave;re modification de la donn&eacute;e dans le jeu. Il respecte le format ISO 8601 : ann&eacute;e-mois-jour (YYYY-MM-DD)</td>
		</tr>
	</tbody>
</table>


## Format de fichier 

Le format de fichier retenu pour la publication des données est le CSV (Comma Separated Values, valeurs séparées par des virgules).

Les fichiers doivent, sauf exception et autant que possible, respecter les règles de formatage suivantes :

* l’encodage des caractères est UTF-8,
* le séparateur des colonnes est la virgule,
* le séparateur des nombres décimaux est le point,
* le séparateur de valeurs multiples dans un champ est le point-virgule,
* si un champ contient une virgule, il doit être entouré de guillemets doubles,
* chaque ligne doit avoir le même nombre de champs,
* le type MIME ou Content-Type est text/csv.

### Recommandations pour le nommage des fichiers 

Les fichiers doivent, sauf exception et autant que possible, respecter les règles de nommage suivantes :

* YYYY-MM-DD : Date de création du fichier
* idProducteur : code INS unique de la commune pour identifier le producteur
* patrimoine-naturel-ou-materiel : nom du fichier, en minuscules non accentuées
* territoire : Nom du territoire concerné, non accentué (exemple : Liege)
* extension : Si les règles de formatage sont respectées, l'extension est .csv

Exemple : 2022-10-25_62063_patrimoine-naturel-ou-materiel_Liege.csv

### Recommandations pour la mise en conformité 

Ces conseils reprennent ceux des schémas standards de données français publié par [l'initiative de data.gouv.fr](https://schema.data.gouv.fr/).

Les fichiers doivent comporter :

* Toutes les colonnes, y compris celles dont les cellules ne sont pas renseignées, dans le bon ordre, et avec des en-têtes correctement nommées sur la première ligne (nom correspondant strictement au schéma)
* Autant de lignes que nécessaire comprenant des cellules dont les valeurs peuvent être obligatoires (elles doivent être impérativement renseignées) ou optionnelles (elles sont seulement recommandées ou soumises à condition de disponibilité / pertinence)
