# ESD_Ressources
Documents et ressources pour aider à la préparation du diplôme **Expert en Sécurité Digitale (ESD)**  


## /!\ ATTENTION /!\
**Les ressources proposées ici ne sont pas officielles**  
Vous ne trouverez aucun cours ou documents appartenants directement à l'ESD CyberAcademy (droits de propriété intellectuelle)  
Ce qui est proposé ici sont des ressources externes qui peuvent vous aider à rédiger votre mémoire et vos annexes ou encore vous entrainer avant de passer les examens des modules.  

### Liens officiels :
Site : https://esdacademy.eu  
Github : https://github.com/ESD-academy


----------------
# Questionnaires d'entrainement aux modules

[Modules 1 & 2 : **Lead Pentester + THA**](https://docs.google.com/forms/d/18tYtlZVRFJwPD5w2JC7g3EnrOM9JvJzPlcj5r0xJXq4/prefill)  
[Module 4 : **Cyberdéfense**](https://docs.google.com/forms/d/1IcKbDws3Bu95bqQWX2mse-hRzftHvHHTu2-l35kPDBE/prefill)  
[Module 4 : **Cyberdéfense n°2**](https://docs.google.com/forms/d/1qYNV93TlbfCyRPzJ1Jfg_l4nyDabkPomjbjiCDtECNc/prefill)  
[Module 5 : **SOC Security Manager**](https://docs.google.com/forms/d/1LSHMuh8zPLBdrcTbOgUq1xUyojVs9ADlNboUNg1mf9c/prefill)  
[Module 6 : **Investigation numérique**](https://docs.google.com/forms/d/1foAX5pTkV-q0QC-yqPB1-xBZnDsd7QibUCq5syfXkb0/prefill)  
[Module 7 : **Analyse de malwares**](https://docs.google.com/forms/d/123vSiXW2CS8g2kzKH5AGxBUeVjJA0DeR1qf1oyDS_uk/prefill)  
[Module 8 : **Juridique et RGPD**](https://docs.google.com/forms/d/1IjC-fWDXb3TyUa_WpCIbffaOYNW_BpQ93QMHK_gA4KQ/prefill)  


------------
# Aide à la rédaction du mémoire
[=> Accès aux ressources](https://drive.google.com/drive/folders/1uRrSDIXJ9Qi91LRDlxym553bzyB6UbxR?usp=sharing)  

**iso-iec-27005-2022** (_2022 - 4ème Edition_)  **EN/FR**   
> _Sécurité de l'information, cybersécurité et protection de la vie privée — Conseils sur la gestion des risques liés à la sécurité de l'information_  
> Document de référence de la norme internationale strandard, qui sert de base à l'analyse de risque, pour ensuite l'exploiter avec EBIOS (ou autre méthode)  


#### liens  
[- rappel rapide du PDCA (Plan-Do-Check-Act) et schema propre](https://arcancial.fr/le-pdca-plan-do-check-act-ou-appele-aussi-roue-de-deming/)  

-------------

## Sujets de veille / idées

- [Rapport Interpol de 2024 sur l'évaluation des cybermenaces en Afrique (FR)](https://www.interpol.int/fr/content/download/21048/file/24COM005030-AJFOC_Africa%20Cyberthreat%20Assessment%20Report_2024_complet_FR%20v3.pdf)  
- [Rapport de WithSecure (Tim West) sur les risques cyber liés aux JO de Paris 2024 (EN)](https://www.withsecure.com/content/dam/with-secure/en/resources-library/202407_WithSecure_Olympics_Threat_Report_ENG.pdf) [FR ici](https://labs-withsecure-com.translate.goog/publications/olympics-cyber-threats-to-paris-2024?_x_tr_sl=auto&_x_tr_tl=fr&_x_tr_hl=fr&_x_tr_pto=wapp)  
- [Eléments publics de doctrine militaire de lutte informatique offensive](https://www.defense.gouv.fr/sites/default/files/ema/El%C3%A9ments%20publics%20de%20doctrine%20militaire%20de%20lutte%20informatique%20OFFENSIVE.pdf)
- [Lutte contre le financement du terrorisme (Dossier de presse 2015)](https://www.economie.gouv.fr/files/dpfinalluttecontrefinancementterrorisme_18mars2015.pdf)
- 



-----------


# Annexes

## Annexe 1 - Compétences en test de pénétration  
[=> Accès aux ressources](https://drive.google.com/drive/folders/1mIz66lMmvRdFnCd7Bi_q73Mu7aR_EA6n?usp=sharing)

**LFI-With-PHPInfo-Assistance** _de INSOMNIA (Brett Moore) - document de recherche_  
> Un indice pour la primo-intrusion !  



## Annexe 3 - Effectuer un audit  
[=> Accès aux ressources](https://drive.google.com/drive/folders/1wopLiRH_bHpnbjE3WK-aZ3Fu_Xsp8UuS?usp=sharing)  
**Guide d'hygiène de l'ANSSI** _Renforcer la sécurité de son système d'information en 42 mesures_  
> Utile pour déterminer le plan d'action et les mesures de remédiation



## Annexe 4 - Mise en place d'un SOC

#### Liens de référence utiles
https://www.manager-go.com/gestion-de-projet/dossiers-methodes/matrice-raci  
https://attack.mitre.org/groups/G0073
https://attack.mitre.org/groups/G1003  
https://www.crowdstrike.com/blog/who-is-ember-bear  
https://www.mandiant.com/resources/insights/apt-groups 
https://clusif.fr/wp-content/uploads/2017/03/clusif-2017-deploiement-soc_vf.pdf
https://www.enisa.europa.eu/publications/how-to-set-up-csirt-and-soc



#### Problème de démarrage de l'infrastructure  
Une fois la VM d'Elastic démarrée, vérifier que les services **elasticsearch** et **kibana** sont démarrés et fonctionnels (_sudo systemctl status elasticsearch.service_ et _sudo systemctl status kibana.service_)  
Si une erreur est présente, vérifier le contenu des fichiers suivants :  
pour **Elasticsearch** => /etc/elasticsearch/elasticsearch.yml   ligne _network.host:192.168.11.30_  
pour **kibana** => /etc/kibana/kibana.yml    lignes _server.host:_ et _elasticsearch.hosts_  
**Les IP doivent correspondre à l'IP de votre VM Elastic** (_sudo ip a_)  

Utilisez **netstat -ntaulp | grep [kibana/elastic/other]** pour vérifier les ports ouverts. Par défaut :  
**Elasticsearch** Port [http] **9200** _(affiche les aggrégations de nodes reçues par ELK)_  
**Elasticsearch** Port **9300** _(utilisé pour l'échange entre les nodes et Elastic)_  
**Kibana** Port **5601**   
**logstash** Port **5044** _(listener pour Beats)_  
**APM** Port **8200**  

_Pour aller plus loin ..._  
[- ELK Understand the default configuration](https://docs.bitnami.com/aws/apps/elk/get-started/understand-default-config/)  
Si Netstat n'est pas installé [-Debian Facile - Netstat diagnostic réseau](https://debian-facile.org/doc:reseau:netstat) 



## Annexes 5,6,7 - Investigation numérique


## Annexe 8 - Analyse de malware


## Annexe 12 - ISO/IEC 22301


## Annexe 13 - ISO/IEC 27001  
[=> Accès aux ressources](https://drive.google.com/drive/folders/1dTdLv7EPdGfhrewqp5TCMr59cIotPyI3?usp=sharing)  

**AD-27-05_-_NSAI_ISO_27001.2022_Readiness_Questionnaire_-_Rev_1_.01 (pdf)**  
> Questionnaire ISO27001:2022 - Pas particulièrement utile pour l'annexe, mais indispensable dans le cas d'un entretien préalable au début d'un audit.   


**bsi-isoiec-27001-2013 (xls)**  
> Checklist pour un audit 27001:2013. Très utile pour la synthèse avec de beaux graphiques. Permet également d'appliquer un niveau de maturité avec une échelle de 0 à 5 pour chacun des points à analyser.   


**ISO27k SOA 2013 (xls)**  
> Déclaration d'applicabilité aux normes 27001:2013, utile pour déterminer les points à mettre en lumière en fonction des objectifs de l'entreprise.

**ISO27001-v2022 (pdf)** (_3ème édition_)   
> _Sécurité de l'information, cybersécurité et protection de la vie privée — Systèmes de management de la sécurité de l'information — Exigences_   
> --> Document de référence difficile à trouver sur Internet, surtout en Français.

**ISO27001-2013-ComplianceChecklist (xls)**  
> Liste des conformités et génération de beaux graphiques pour l'annexe  


## Annexe 14 - Juridique et RGPD
[=> Accès aux ressources](https://drive.google.com/drive/folders/1H_iHcPWhDrzghiYKD_I2RCIIv5fojA07?usp=sharing)

**cnil-pia base de connaissance (pdf)**  
> Bases de connaissances sur l'analyse d'impact relative à la protection des données (PIA)  

**Modele_pour_analyse_dimpact (doc)**  
> Exemple d'analyse d'impact datant de 2022 et provenant de l'Université de Bordeaux  

**PIA_example (pdf)**  
> Exemple de rapport PIA créé puis exporté depuis l'application PIA de la CNIL  

**wp248_rev.01 (pdf)**  
> Lignes directrices concernant l'analyse d'impact relative à la protection des données (AIPD) et la manière de déterminer si le traitement est "susceptible d'engendrer un risque élevé" aux fins du RGPD




