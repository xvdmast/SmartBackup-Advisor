## Background

In enterprise environments, backup configurations are vaak handmatig, foutgevoelig en inconsistent met bedrijfsbeleid. Dit leidt tot risico’s zoals onvoldoende retentie, overbodige opslagkosten, of ongeldige back-ups.  

Persoonlijk werk ik met Veeam, VMware en monitoringtools zoals LibreNMS en The Dude. Ik zie regelmatig problemen zoals:
* Retentie-instellingen die niet aansluiten bij klantwensen
* Niet-gedocumenteerde afwijkingen tussen beleid en configuratie
* Onvolledige bescherming van VMs door vergeten taggings of policies

Dit project automatiseert het herkennen en verbeteren van deze afwijkingen met behulp van AI.

## How is it used?

SmartBackup Advisor draait als een achtergrondservice of periodieke analyse-tool in het netwerk van een IT-dienstverlener.  

**Gebruikers:**  
- IT engineers / beheerder
- Compliance officers
- MSP-platformbeheerders  

**Gebruikssituaties:**  
- Dagelijkse compliance check
- Detectie van afwijkingen na wijzigingen in vSphere of Veeam
- Automatisch genereren van aanpassingsadviezen

<img src="https://upload.wikimedia.org/wikipedia/commons/thumb/f/f4/Veeam_logo.svg/2560px-Veeam_logo.svg.png" width="300">

## Data sources and AI methods

De tool gebruikt:
* De Veeam Backup & Replication REST API
* VM-metadata via vSphere Tags
* Klantwensen opgeslagen in een SQLite of PostgreSQL-database

AI-methodes:
* Decision Trees of Rulesets voor afwijkingsdetectie
* NLP voor interpretatie van klantbeleid (optioneel)
* Reinforcement learning voor auto-optimalisatie van back-up schemas

Eventueel gebruik ik [LangChain](https://www.langchain.com/) voor het koppelen van policy-instructies aan acties, en [Scikit-learn](https://scikit-learn.org/) voor modeltraining.

## Challenges

- Niet alles is uit API’s op te vragen: sommige context komt uit handmatig beleid of externe systemen
- AI kan alleen adviseren, niet automatisch aanpassen zonder menselijke validatie
- Data moeten correct en up-to-date zijn: garbage in = garbage out
- Privacy en security (bijvoorbeeld bij multitenant MSP-omgevingen)

## What next?

- Integratie met GitLab CI/CD of Ansible voor geautomatiseerde correcties
- Front-end UI bouwen (met React of HTMX)
- Ondersteuning voor meerdere back-upsystemen (Commvault, Rubrik, etc.)
- Dataset publiceren als open source voor modelverbetering

Ik heb vooral hulp nodig bij UX-design en integratie met grotere CI/CD-platforms. Een community die bijdraagt aan policy-rulesets zou ideaal zijn.

## Acknowledgments

* Idee geïnspireerd door mijn werk in managed services
* [Veeam REST API v12 docs](https://helpcenter.veeam.com/docs/vbr/rest/)  
* [LangChain open source](https://github.com/hwchase17/langchain)
* Gebruikt de Elements of AI projectstructuur en Building AI format
