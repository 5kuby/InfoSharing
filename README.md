# InfoSharing
Questo repository traccia le attività del gruppo operativo per la sperimentazione di un meccanismo di Info Sharing della community [Cyber Saiyan](https://www.cybersaiyan.it)

Il gruppo è stato avviato a seguito di una web conf tenuta il giorno 8 Novembre 2018 il cui [resoconto è disponibile qui](https://docs.google.com/document/d/13PCWGlVvdOy226GXaWcnzkvl-7WfCyIUXTYGknrd9bg/edit).

L'obiettivo è quello di creare una community italiana che funzioni da collettore degli indicatori "pregiati" già disponibili e condivisi da fonti autorevoli (get di indicatori) e al contempo possa contribuire con le proprie expertise all'arricchimento della rete di condivisione (push indicatori sulla rete).

Di seguito l'architettura di COMMUNITY che si è implementata, che prevede due componenti distinte
* la componente PRODUCER realizzata attraverso il software [OpenTAXII](http://www.opentaxii.org/en/stable/) su cui è stata configurata una collection denominata _community_ su cui è abilitato il PUSH autenticato di IoC in formato STIX 1.2
* la componente CONSUMER realizzata attraverso il software [Minemled](https://www.paloaltonetworks.com/products/secure-the-network/subscriptions/minemeld) che effettua periodicamente il POLL degli IoC dalla collection _community_ di OpenTAXII e "ribalta" tali indicatori su due feed distinti (testo e STIX/TAXII)

Di seguito è illustrata l'architettura implementata

![l'architettura implementata](img/architettura.png)

Le componenti CONSUMER del servizio sono accessibili all'indirizzo https://infosharing.cybersaiyan.it 
* [STIX/TAXII](IoC-STIX_TAXII.md)
* [TEXT](IoC-text.md)

La guida all'installazione del server e del software di base è [disponibile qui](INSTALL/Server_software.md).
Le configurazioni dei software (OpenTAXII e Minemeld) saranno descritte in un file a parte [TODO].

### Community
Il progetto è un'iniziativa volontaria portata avanti dalla community di Cyber Saiyan.
E' stato creato un [gruppo Telegram](https://t.me/joinchat/Av4DDFjVkRC60YH_Lq-WVw) per coordinare l'evoluzione del progetto.
