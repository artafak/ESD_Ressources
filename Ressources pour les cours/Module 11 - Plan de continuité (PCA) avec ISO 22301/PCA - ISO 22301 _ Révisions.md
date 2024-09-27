## 1. Cadrage et terminologie

### 1. Terminologie et Définitions

- **PCA** (Plan de continuité d'activité)
- **PRA** (Plan de reprise d'activité)
- **PCI** /**PRI** (Plan continuité/reprise informatique)

La différence entre continuité et reprise d'activité est primordiale, tout comme PCA/PRA et PCI/PRI. L'informatique est vitale pour les entreprises, mais la reprise d'activité concerne l'ensemble des activités, pas seulement l'informatique. Une confusion commune lie reprise d'activité à reprise informatique.

![[ESD/Documents/Images/Pasted image 20230828092247.png]]

### 2. Continuité vs Reprise d'activité les différences 

Lorsqu'une entreprise met en place une gestion de sa continuité ou reprise d'activité plusieurs termes doivent apparaître :
- **RPO** (Recovery point objective)
- **RTO** (Recovery time objective)
- **WRT** (Work recovery time) 
- **MTD** (Maximum tolerable downtime) -> RTO + WRT 
L'ensemble de ces notions seront donc nécessaires à la compréhension du futur PCA/PRA.

![[ESD/Documents/Images/Pasted image 20230828092726.png]]

##### Pourquoi un PCA/PRA ? 
Le PCA/PRA va au-delà de la récupération de données, visant la reprise des activités essentielles. Motivations : réglementations, contrats, alignement, anticipation. Les coûts et retours diffèrent des projets classiques. L'objectif : minimiser pertes, restaurer activités selon les plans.

### 3. Les erreurs courantes liés au PCA/PRA
Elles incluent : confusions conceptuelles, risques assurantiels, absence de stratégie de continuité, désengagement de la direction, PCA/PRA non mis à jour, négligence des obligations légales et contractuelles, modifications architecturales, BYOD, etc. Prévenir ces erreurs est crucial pour le succès du projet.

## 2. PCA et entreprise
### 2.1. PCA et Stratégie d'Entreprise
Mettre en place un PCA/PRA sans contexte néglige l'essence de l'entreprise. La stratégie englobe le PCA en fonction du périmètre.
### 2.2. Liaison Risques SI et PCA
Le lien PCA et gestion des risques SI est crucial. Sans cela, des scénarios critiques peuvent être omis.
> Contrats et partenariats influent sur les besoins de disponibilité.
### 2.3. Assurance des Biens
L'évaluation moderne des actifs intangibles est complexe. Le PCA aide à quantifier les impacts financiers et facilite l'assurance et les investissements.
## 3. Etude de la norme ISO 22301

### 3.1. PCA et Conformité Normative
L'ISO 22301 définit les exigences pour les systèmes de gestion de la continuité d'activité (**SMCA**). Les obligations légales en France varient, mais le règlement européen sur la protection des données exige des mesures de sécurité adaptées, y compris un PCA.
### 3.2. Norme ISO 22301
La norme ISO 22301 présente ses clauses, avantages (compétitivité, risques, réglementations), et ses liens avec ISO 27001.
### 3.3. Système Intégré
Les systèmes intégrés offrent des avantages mais nécessitent une délimitation claire. 
### ISO 22301 “4-Contexte”
Répondre aux besoins d'information, attentes des parties, exigences légales, et définir le périmètre du SMCA pour la conformité à ISO 22301.

## 4 Contexte de l'organisation 
### 4.1. Contexte Organisationnel
Identifier les influences internes et externes essentielles au SMCA. Documenter activités, partenariats, liens avec politiques, intégrés à la politique de continuité.
### 4.2. Parties Prenantes et Exigences
Identifier parties prenantes, leurs besoins implicites/explicites. Mettre en place procédure pour exigences légales/réglementaires. Informer régulièrement les parties prenantes.
### 4.3. Domaine d'Application du SMCA
- Définir limites, enjeux et parties prenantes.
- Inclure produits, services, besoins des parties.
- Documenter exclusions sans affecter continuité.
### 4.4. Système de Management de la Continuité d'Activité
- Établir, mettre en œuvre, améliorer SMCA et processus selon ISO 22301.

## ISO 22301 " 5-Leadership"
### 5.1 Engagement de la Direction
- La Direction démontre le leadership envers le SMCA.
- Établit politiques et objectifs en alignement stratégique.
- Fournit ressources et communique sur l'importance du SMCA.
- Désigne responsables, mène revues et encourage l'amélioration continue.
### 5.2 Politique
- La Direction crée une politique de continuité adaptée.
- Engage à satisfaire exigences et amélioration continue.
- Communique, revisite et conserve la politique documentée.
### 5.3 Rôles, Responsabilités et Autorités
- La Direction attribue responsabilités et autorités.
- Garantit conformité au SMCA et rapports à la Direction.
## ISO 22301 “ 6-Planification”
### 6.1 Actions face aux risques et opportunités 
- L'organisation intègre les enjeux, exigences et évalue les risques et opportunités.
- Planifie des actions pour atteindre les résultats attendus, prévenir les effets indésirables et améliorer continuellement.
- Intègre ces actions dans les processus du SMCA et évalue leur efficacité.
### 6.2 Objectifs de continuité d'activité et plans

- La Direction établit et communique les objectifs de continuité d'activité.
- Objectifs cohérents avec la politique, mesurables et tenant compte des exigences.
- Ils guident les actions pour assurer la fourniture minimale de produits/services.
- L'organisation conserve des informations documentées sur les objectifs et détermine responsabilités, ressources, échéances et évaluation des résultats.
## ISO 22301 “7-Support”

##### 7.1 Ressources 
- Identifier et fournir les ressources nécessaires pour le SMCA.
##### 7.2 Compétences
- Déterminer les compétences requises.
- S'assurer que les personnes sont compétentes via formation et expérience.
- Acquérir et évaluer les compétences si nécessaire.
##### 7.3 Sensibilisation
- Sensibiliser les personnes à la politique et leur rôle.
- Conscience des effets positifs de l'amélioration.
- Comprendre les implications de la non-conformité.
- Conscience du rôle en cas d'incidents.
##### 7.4 Communication
- Identifier les besoins de communication interne et externe.
- Établir des procédures pour communiquer avec parties intéressées, employés, clients, partenaires, médias et autorités.
- Assurer disponibilité des moyens de communication en cas d'incident.
- Tester les capacités de communication en cas de perturbation.
##### 7.5 Informations documentées 
###### Généralités 
- Le SMCA doit inclure les informations requises par la norme et celles jugées nécessaires.
- La pertinence dépend de la taille, de la complexité et de la compétence de l'organisation.
###### Création et mise à jour 
- Les informations doivent être appropriées en termes d'identification, description, format et caractère adéquat.
###### Maîtrise des informations documentées
- Les informations exigées doivent être disponibles et protégées contre toute perte ou usage inapproprié.
- Activités incluent distribution, accès, stockage, contrôle des versions, durée de conservation, etc.
- Les informations externes nécessaires doivent aussi être maîtrisées et protégées.

### ISO 22301 “8-Fonctionnement”
#### 8.1 Planification opérationnelle et maîtrise
- L'organisation doit planifier, mettre en œuvre et maîtriser les processus pour satisfaire aux exigences en 6.1.
- Cela implique d'établir des critères, de les suivre, et de conserver des informations documentées.
#### 8.2 Analyse des impacts et appréciation du risque
##### Généralités
- Un processus documenté doit analyser les impacts des perturbations et évaluer les risques.
- Il doit prendre en compte les exigences légales et autres.
- Il doit prioriser les traitements de risques en fonction de leur impact et coût.
##### Analyse des impacts
- L'analyse évalue les impacts des interruptions, fixe les délais de reprise prioritaires, et identifie les dépendances.
##### Catégories d'impacts
- Les impacts financiers directs et indirects.
- Impacts sur l'image, la réputation, le juridique, le réglementaire.
> La gestion des risques et des impacts est cruciale pour assurer la continuité des opérations et la résilience de l'organisation.

L'EBCA (Expression en Besoin de Continuité d'Activités) consiste en des entretiens avec les responsables opérationnels pour collecter des informations essentielles

##### Appréciation du Risque
Un processus formalisé d'appréciation des risques identifie, analyse et évalue les risques d'incidents perturbateurs.
L'organisation doit :
- Identifier les risques pour les activités clés, les ressources et partenaires ;
- Analyser systématiquement les risques ;
- Évaluer les risques nécessitant action ;
- Définir des actions adaptées aux objectifs de continuité et au risque accepté.
#### 8.3 Stratégie de Continuité
Une stratégie basée sur l'analyse d'impact et l'appréciation du risque est nécessaire.
L'organisation doit élaborer une stratégie pour :
- Protéger les activités clés ;
- Stabiliser, reprendre ou rétablir ces activités ;
- Atténuer les impacts.

Elle doit déterminer les besoins en ressources, envisager des mesures de protection, choisir des actions en accord avec son seuil de risque. La stratégie intègre des éléments tels que l'analyse d'impact, les besoins de continuité, la politique de continuité, sous la direction de la Direction Générale.

#### 8.4 Etablissement et mise en œuvre de procédures de continuité d'activité

L'organisation doit établir, mettre en œuvre et tenir à jour des procédures de continuité d'activité lui permettant de gérer un incident perturbateur et de poursuivre ses activités, selon les objectifs de reprise identifiés lors de l'analyse des impacts sur l'activité.

L'organisation doit documenter Les procédures (y compris les dispositions nécessaires) lui permettant d'assurer la continuité des activités et de management d'un incident perturbateur.

Les procédures doivent :
- établir un protocole de communications internes et externes approprié ;
- être précis concernant les mesures immédiates devant être prises pendant une perturbation ;
- être souples pour répondre à des menaces non prévues et à des conditions internes et externes variables ;
- se concentrer sur l'impact d'événements pouvant potentiellement perturber les opérations
- être développées sur la base d'hypothèses établies et d'une analyse des interdépendances ; et 
- être efficaces dans la réduction des conséquences par la mise en œuvre de stratégies d'atténuation appropriées

###### Structure de réponse à un incident

L'organisation doit établir, documenter et mettre en œuvre des procédures et une structure de management lui permettant de répondre à un incident perturbateur en faisant appel à un personnel ayant les responsabilités, l'autorité et les compétences nécessaires pour gérer l'incident.

La structure de réponse doit :
- identifier les seuils d'impact justifiant le déclenchement d'une réponse formelle 
- évaluer la nature et l'étendue d'un incident perturbateur ainsi que son impact potentiel, 
- activer une réponse appropriée en termes de continuité d'activité ...
- disposer de processus et de procédures pour l'activation, le fonctionnement, la coordination et la communication dé la réponse 
- disposer des ressources disponibles pour soutenir les processus et les procédures de gestion d'un incident perturbateur afin d'en réduire au minimum l'impact ; et
- communiquer avec les parties intéressées et les autorités ainsi qu'avec les médias 

En considérant la sécurité des personnes comme la première priorité et en consultation avec les parties intéressées concernées, l'organisation doit décider de communiquer ou non, en externe, sur ces risques et impacts significatifs et étayer sa décision par des
documents.

Si l'organistion décide de communiquer, elle doit alors établir et mettre en œuvre des procédures pour cette communication externe, des alertes et des avertissements auprès des médias si besoin. 

##### Avertissement et communication
L'organisation doit définir, mettre en œuvre et tenir à jour des procédures pour :
-  détecter l'incident ; …
- surveiller régulièrement l'incident ; 
- gérer la communication interne au sein de l'organisation et la réception, la documentation et la réponse à une communication émanant des parties intéressées ;
- garantir la disponibilité des moyens de communication au cours d'un incident perturbateur

L'organisation doit définir, mettre en œuvre et tenir à jour des procédures pour :
- faciliter une communication structurée avec les services d'urgence ;
- effectuer l'enregistrement des informations critiques concernant l'incident, les actions entreprises et les décisions prises, et les éléments suivants doivent également être considérés et mis en œuvre lorsque cela est approprié :

- l'alerte des parties intéressées potentiellement touchées par un incident perturbateur réel ou imminent ;
- l'assurance de l'interopérabilité des multiples services d'urgence et le personnel de l'organisation 
- le fonctionnement d'une installation de communication. Les procédures de communication et a d'avertissement doivent faire l'objet d'exercices réguliers.

##### Plans de continuité d'activité
Les plans de continuité d'activité doivent généralement contenir :
- les rôles et les responsabilités définis des personnes et des équipes ayant autorité pendant et après un incident 
- un processus d'activation de la réponse 
- les détails permettant de gérer Les conséquences immédiates d'un incident perturbateur en tenant dûment compte:

- du bien-être des individus ; 
- des options stratégiques, tactiques et opérationnelles pour répondre à la perturbation ;
- de la prévention de toute perte ou indisponibilité supplémentaire d'activités prioritaires ;

Les détails concernant la manière et les circonstances dans lesquelles l'organisation communiquera avec des employés et leurs proches, les parties intéressées clés et les personnes à contacter en cas d'urgence 

- la manière dont l'organisation poursuivra ou reprendra ses activités prioritaires dans les délais prédéterminés ;
- les détails de la réponse de l'organisation aux médias à la suite d'un incident, y compris :
	- une stratégie dé communication
	- l'interface préférée avec les médias
	- des lignes directrices ou un modèle de rédaction d'une déclaration pour les médias ; et
	- des porte-parole appropriés ;

- un processus de sortie une fois que l'incident est terminé.
Chaque plan doit définir :
- le but et le domaine d'application 
- les objectifs
- les critères et les procédures d'activation 
- les procédures de mise en œuvre 
- les rôles, les responsabilités et les autorités 
- les exigences et les procédures de communication 
- les interdépendances et interactions internes et externes 
- les exigences en termes de ressources
- les processus relatifs au flux d'information et à la documentation.

##### Reprise
L'organisation doit disposer de procédures documentées lui permettant de rétablir et de reprendre ses activités en s'appuyant sur des mesures temporaires adoptées pour répondre aux exigences métier habituelles après un incident.

##### Exercices et tests
L'organisation doit procéder à des exercices et des tests de ses procédures de continuité d'activité afin de s'assurer qu'elles sont cohérentes avec ses objectifs de continuité d'activité.

L'organisation doit mener des exercices et des tests qui :
- sont cohérents avec le périmètre et les objectifs du SMCA 
- reposent sur des scénarios appropriés qui sont bien planifiés avec des buts et des objectifs clairement définis
- cumulés au fil du temps, valident l'ensemble de ses dispositions en matière de continuité d'activité, en impliquant les parties concernées
- minimisent le risque de perturbation des opérations 
- permettent de produire, après les exercices, des rapports formalisés contenant les résultats, des recommandations et des actions pour mettre en œuvre des améliorations 
- sont revus dans le cadre d'une promotion de l'amélioration continue ; et
- sont menés a des intervalles planifiés et lorsque des changements significatifs interviennent au sein de l'organisation ou dans l'environnement dans lequel elle opère.

### ISO 22301 " 9-Evaluation des performances”

1. Surveillance, mesurage
2. Analyse et évaluation
3. Audit interne du SMCA
4. Mise en place de revue de direction

##### 9.1 Supervision, mesurage, analyse et évaluation

###### Généralités
L'organisation doit déterminer :
- ce qu'il est nécessaire de surveiller et mesurer
- les méthodes de supervision, de mesurage, d'analyse et d'évaluation, selon le cas, pour assurer la validité des résultats
- quand la surveillance et la mesure doivent être effectuées ; et
- quand les résultats de la surveillance et de la mesure doivent être analysés et évalués.

L'organisation doit conserver des informations documentées pertinentes comme preuves des résultats.
L'organisation doit évaluer les performances du SMCA, ainsi que l'efficacité du SMCA 

En outre, l'organisation doit :
- agir, lorsque cela est nécessaire, pour remédier aux évolutions ou résultats-négatifs avant l'apparition d'une non-conformité ;
- conserver des informations documentées appropriées comme preuves des résultats.

Les procédures de supervision des performances doivent prévoir 
- D'établir des mesures de performances adaptées aux besoins de l'organisation 
- De surveiller dans quelle mesure la politique, les objectifs et les cibles de continuité d'activité de l'organisation sont respectés/atteints ; 
- Les performances des processus, des procédures et des fonctions qui protègent ses activités prioritaires
- De surveiller la conformité à la présente Norme internationale et aux objectifs de continuité d'activité 
- De surveiller les preuves historiques de performances insuffisantes du SMCA ; et
- D'enregistrer les données et les résultats de la surveillance et des mesures pour faciliter Les actions correctives ultérieures.

##### Evaluation des procédures de continuité d'activité 

L'organisation doit mener des évaluations de ses procédures et de ses capacités en matière de continuité d'activité pour s'assurer qu'elles demeurent pertinentes, adéquates et efficaces 

Ces évaluations doivent être réalisées par le biais de revues périodiques, d'exercices, de tests, de rapports post-incident et d'évaluations des performances. Les changements significatifs intervenus doivent être pris en compte en temps opportun dans la ou les procédures. 

- L'organisation doit évaluer périodiquement la conformité aux exigences légales et réglementaires applicables, aux meilleures pratiques de son secteur ainsi que la conformité à sa propre politique de continuité d'activité et aux objectifs associés; et ,
-  l'organisation doit mener des évaluations à des intervalles planifiés et lorsque des changements significatifs interviennent.

Lorsqu'un incident perturbateur se produit et entraîne l'activation de  ses procédures de continuité d'activité, l'organisation doit procéder à une revue après l'incident et enregistrer les résultats. 

##### Audit interne 

L'organisation doit réaliser des audits internes à des intervalles planifiés afin de recueillir des informations permettant de déterminer si le système de management de la continuité d'activité.
est conforme :
- aux exigences propres de l'organisation concernant son SMCA 
- aux exigences de la présente Norme internationale 
- est efficacement mis en œuvre et tenu à jour. 

L'organisation doit :

- Planifier, établir, mettre en œuvre et tenir à jour un (des) programme(s) d'audit, couvrant notamment la fréquence, les méthodes, les responSabilités, es exigences de planification et de comptes rendus. Le(s) programme(s) d'audit doi(ven)t tenir compte de l'importance des processus concernés et des résultats des audits précédents,
- Définir les critères d'audit et le périmètre de chaque audit 
- Sélectionner des auditeurs et réaliser des audits pour assurer l'objectivité et l'impartialité du processus d'audit
- S'assurer qu'il est rendu compte des résultats des audits à la Direction concernée :et
- Conserver des informations documentées comme preuves de la mise en œuvre du programme d'audit et des résultats d'audit.

Le programme d'audit, quel que soit le moment où il est conduit, doit reposer sur les résultats des évaluations du risque des activités de l'organisation et sur les résultats des audits précédents.

Les procédures d'audit doivent englober le périmètre, la fréquence, les méthodologies et les compétences, ainsi que les responsabilités et les exigences applicables à la conduite des audits et à la rédaction d'un rapport présentant les résultats

Le management responsable du domaine audité doit assurer que toutes les corrections et actions correctives nécessaires sont entreprises sans délai indu pour éliminer les non-conformités détectées et leurs causes. 

Les actions de suivi doivent inclure la vérification des actions entreprises et le compte-rendu des résultats de cette vérification.

##### Revue de direction

À des intervalles planifiés, La Direction doit procéder à La révision du SMCA de l'organisation, afin de s'assurer qu'il est toujours approprié, adapté et efficace.

La revue de Direction doit prendre en compte :
- L'état d'avancement des actions décidées lors des revues de direction précédentes ;
- Les modifications des enjeux externes et internes pertinents pour le système de management de la continuité d'activité ;
- les informations sur Les performances en matière de continuité d'activité, y compris les tendances concernant :
	- les non-conformités et Les actions correctives 
	- les résultats de l'évaluation de la supervision et du mesurage ; et
	- Les résultats des audits 
- les axes d'amélioration continue. 

Les revues de direction doivent prendre en compte les performances de l'organisation, y compris :
- Le suivi des actions décidées lors des revues de direction précédentes ;
- la nécessité d'apporter des modifications au SMCA, y compris la politique et les objectifs ;
- les axes d'amélioration ;
- Les résultats des audits et des révisions du SMCA, y compris ceux des fournisseurs et partenaires clés le cas échéant 
- Les techniques, les produits ou les procédures, qui pourraient être utilisés dans l'organisation pour améliorer les performances et l'efficacité du SMCA 
- L'état d'avancement des actions correctives 
- Les résultats des exercices et des tests
- Les risques ou les questions qui n'ont pas été traités de manière appropriée lors d'une précédente évaluation des risques
- Tous les changements pouvant affecter le SMCA, qu'ils soient internes ou externes au périmètre du SMCA 
- L'adéquation de la politique 
- Les recommandations d'amélioration 
- Les leçons tirées et les actions découlant d'incidents pertufbateurs ; et
- Les bonnes pratiques et lignes directrices qui apparaissent.

Les conclusions de la revue de direction doivent inclure les décisions relatives aux axes d'amélioration continue et aux éventuels changements nécessaires à apporter au SMCA, et comprendre les éléments suivants :
- les variations apportées au périmètre du SMCA 
- l'amélioration de l'efficacité du SMCA 
- la mise à jour de l'évaluation des risques, du bilan d'impact sur les activités, des plans de continuité d'activité et des procédures associées 
- la modification des procédures et des contrôles pour répondre à des événements,internes ou externes qui peuvent influer sur le SMCA, y compris les changements apportés aux : 
1) exigences métier et opérationnelles 
2) exigences de réduction des risques et de sécurité
3) conditions et processus opérationnels 
4) exigences légales et réglementaires 
5) obligations contractuelles 
6) niveaux de risque et/ou critères d'acceptation des risques
7) besoins en termes de ressources 
8) exigences en matière de financement et de budget

la manière dont l'efficacité des contrôles est mesurée.

L'organisation doit conserver des informations documentées attestant des conclusions des revues de direction.

L'organisation doit :
- Communiquer les conclusions de la revue de direction aux parties intéressées concernées ; et … 
- Entreprendre l'action appropriée en relation avec ces conclusions. ...

### ISO 22301 "10-Amélioration”

1. Etudes des non-conformités
2. Actions correctives
3. Amélioration continue

##### 10.1 Non conformité et actions correctives 

Lorsqu'une non-conformité se produit, l'organisation doit
- identifier la non-conformité 
- réagir à la non-conformité, et le cas échéant : 
	- agir pour la maîtriser et la corriger
	- faire face aux conséquences 

Evaluer s'il est nécessaire de mener une action pour éliminer les causes de la non-conformité, de sorte qu'elles ne se reproduisent pas, au même endroit ou ailleurs, en :
- révisant la non-conformité 
- déterminant les causes de la non-conformité ;
- déterminant si des non-conformités similaires existent, ou pourraient potentiellement se produire 
- évaluant le besoin d'entreprendre des actions correctives pour s'assurer que les non-conformités ne se reproduisent pas, au même endroit ou ailleurs 
- déterminant et mettant en œuvre les actions correctives nécessaires ;
- révisant l'efficacité de toute action corrective mise en œuvre ;
- modifiant, si nécessaire, le SMCA

Lorsqu'une non-conformité se produit, l'organisation doit
- mettre en œuvre toutes les actions nécessaires ;
- réviser l'efficacité de toute action corrective mise en œuvre ;
- modifier, si nécessaire, Le système de management de la continuité d'activité. 

Les actions correctives doivent être à la mesure des effets des non-conformités rencontrées. 
L'organisation doit conserver des informations documentées comme preuves :
- de la nature des non-conformités et de toute action subséquente ;
- des résultats de toute action corrective.

##### 10.2 Amélioration continue 

L'organisation doit continuellement améliorer la pertinence, l'adéquation et l'efficacité du SMCA. 

![[ESD/11-Plan de continuité (PCA) avec ISO 22301/Canvas_ISO_22301.canvas|Canvas_ISO_22301]]


# Divers
https://openclassrooms.com/fr/courses/6227526-mettez-en-place-un-plan-de-continuite-dactivite-pca/6674416-definissez-la-continuite-dactivite
https://www.clubpca.eu/

- La continuité d’activité a pour vocation de **réduire** une situation de **crise en situation d'urgence**.  
- Elle ne s’intéresse qu’aux événements perturbateurs **non maîtrisables** dans un délai défini comme **grave**.
- Le **plan de continuité d'activité** est l'ensemble des mesures qui permettent de sortir d'une situation d'urgence pour rétablir l'activité au plus vite, souvent en mode dégradé.
## la norme ISO 22301
_**système de management de la continuité d’activité, ou SMCA**._
**ISO** **22301** est une norme qui spécifie les exigences pour **planifier,** **établir,** **mettre en œuvre, exploiter, surveiller, revoir, maintenir et améliorer en continu** un système de management de la continuité d’activité.

![[ESD/Documents/Images/15916254178999_Chapitre 1.3 Schema chapitre 1.4 SMCA_2.jpg]]

- Pour mettre en place un système de management de la continuité d’activité (SMCA), appuyez-vous sur la norme certifiante **ISO 22301**. 
- La norme certifiante ISO 22301 et d’autres normes afférentes vous assurent de bénéficier des **meilleures conditions de réussite** de la mise en place de votre SMCA.
- La certification d’une partie des activités de votre entreprise est une démarche **progressive** qui vous assure une **reconnaissance** de vos clients, fournisseurs, et des régulateurs.

-  Le **soutien** de votre Direction générale est essentiel pour entreprendre un SMCA. 
- Grâce à la **note d'intention**, votre Direction pourra démontrer sa volonté d'action, la personne responsable et les ressources allouées, et prévenir l'ensemble des parties prenantes. 
- C'est ensuite à vous d'être **diplomate** et **bon communicant** pour intégrer ces parties prenantes : leur implication est cruciale pour la réussite de votre projet.
- La **sensibilisation** a pour objet d'attirer l'attention et de faire évoluer les habitudes. La sensibilisation est destinée à toucher les **émotions** et les **comportements**.
- La **formation** est destinée à acquérir des compétences, c’est-à-dire des aptitudes à mettre en pratique du savoir, du savoir-faire et du savoir-être.
- Un **vocabulaire commun** et une **réunion de lancement** avec le sponsor du projet vont vous aider à partir du bon pied.   
- **Formation** et **sensibilisation** sont les deux éléments clés pour vous assurer que votre PCA soit appliqué efficacement. 
- Soyez **rigoureux** dans vos plans de formation et de sensibilisation, pour vous assurer que les parties prenantes soient bien **formées** et **aptes** à agir lors d'un sinistre.

**bilan d’impact sur l’activité ou _BIA_ (ou en anglais, _Business Impact Analysis_)**
Pour chaque activité, le BIA évalue trois paramètres :
- le **délai maximal d’interruption admissible (DMIA)**. Par exemple 4 heures, 24 heures, etc. Le DMIA classe les **activités par priorité** de reprise d’activité ; 
- la **PMDT,** **c’est-à-dire la perte maximale de données tolérable**. Par exemple, aucune perte de données, 24 heures de perte de données, etc. Cela dépend de la dernière prise de **sauvegarde de recours** externalisée nécessaire à la reprise d’activité ;
- l’**OMCA,** **c’est-à-dire l’objectif minimal de continuité d’activité**. Par exemple, l’activité peut travailler avec la moitié de l’effectif nominal à la fin du DMIA qui marque le début de la reprise d’activité de l’activité.

- Pour effectuer un BIA, vous devez garder en tête les questions suivantes :
    - Quelles sont vos activités critiques ?
    - Quelles sont leurs durées d’interruption maximales ?
    - Quels sont les niveaux de dégradation de service acceptables ?
    - Quels sont les ressources/moyens nécessaires pour fonctionner, dont les parties intéressées ? 

- À la fin de ce BIA, vous disposez de plusieurs éléments :
    - la **liste** **de vos activités prioritaires** à redémarrer en cas d’arrêt, validée par la Direction générale ;
    - l’**explicitation** et la **justification** des **besoins** de continuité d’activité (contractuelles, réglementaires, d'image, etc.) ;
    - l’indication des **ressources minimales** nécessaires pour satisfaire aux exigences de continuité d’activité ;
    - la liste des **activités** liées et des parties intéressées.