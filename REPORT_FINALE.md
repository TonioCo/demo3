#RELAZIONE TECNICA FINALE

##Indice

1. Introduzione
2. Modello concettuale
3. Requisiti specifici  
4. Architettura
5. System Design  
6. Riepilogo del test    
7. Manuale utente
8. Processo di sviluppo e organizzazione del lavoro
9. Analisi retrospettiva
 

## 1. Introduzione
 
 Slack è un software  della categoria degli strumenti di collaborazione aziendale, usato per inviare messaggi, in modo istantaneo ai membri del team, per condivisione di file con possibilità di integrazione con varie applicazioni.
 I messaggi sono pubblici all’interno dei canali pubblici dell’azienda e/o organizzazione, con possibilità di avere canali privati composti da due o più membri per i vari team di sviluppo; Per facilitare, dunque, la comunicazione all’interno del team. 
 Si riceve una notifica quando si viene menzionati, con possibilità di indicare una persona specifica (@nome), l’intera organizzazione(@everyone), o il singolo team(@team).
 La SNA (dall'inglese Social Network Analysis) studia la società  come rete di relazioni.
 Il programma in questione è una versione semplificata con command-line interface (CLI) di SNA4Slack che consente agli utenti di visualizzare reti sociali basate su conversazioni Slack all'interno dei canali.
 Le reti sociali viste aventi come nodi i membri dei team di Slack, variando a seconda dello scambio di comunicazioni considerato.Un esempio di rete sociale basata sulle citazioni o mentions degli utenti, si ottiene considerando come nodi i membri dei team con archi diretti ,specificati dalla citazione che vanno dall’autore al destinatario di essa, con possibilità di avere come peso il  numero di citazioni
 L’utente puo’ visualizzare vari aspetti della rete sociale, tra cui: l’elenco dei membri, nomi dei canali e le interazioni tra gli utenti(@mention).

## 2. Modello concettuale
 ![modelloconcettuale](drawings/modelloconcettuale.png)

## 3. Requisiti specifici  

 In qualità di utente voglio visualizzare la lista dei Member issue#3
 Criteri di accettazione:
 
 -Verificare che sia possibile fare la richiesta da linea di comando
 -Verificare che l'output sia visualizzato su standard output
 -Verificare che sia possibile specificare il workspace
 -Verificare che ci sia un file esportato associato al workspace
 -Verificare che i Member siano visualizzati uno per riga
 -Verificare che i Member del workspace siano tutti presenti
 -Verificare che non siano visualizzati Member estranei al workspace

 In qualità di utente voglio visualizzare la lista dei Channel issue#4
 Criteri di accettazione:
 • Verificare che sia possibile fare la richiesta da linea di comando
 • Verificare che l'output sia visualizzato su standard output
 • Verificare che sia possibile specificare il workspace
 • Verificare che ci sia un file esportato associato al workspace
 • Verificare che i Channel siano visualizzati uno per riga
 • Verificare che i Channel del workspace siano tutti presenti
 • Verificare che non siano visualizzati Channel estranei al workspace

 In qualità di utente voglio visualizzare la lista dei Member raggruppati per Channel issue#5
 Criteri di accettazione:
 • Verificare che sia possibile fare la richiesta da linea di comando
 • Verificare che l'output sia visualizzato su standard output
 • Verificare che sia possibile specificare il workspace
 • Verificare che ci sia un file esportato associato al workspace
 • Verificare che i Member e Channel siano visualizzati uno per riga
 • Verificare che sia possibile distinguere quale nome è un "Member" e quale è un Channel
 • Verificare che i Channel siano tutti presenti
 • Verificare che non siano visualizzati Channel estranei al workspace
 • Verificare che i Member di un Channel siano tutti presenti
 • Verificare che non siano visualizzati Member estranei al Channel

 In qualità di utente voglio visualizzare la lista dei Member di un Channel issue#6
 Criteri di accettazione:
 • Verificare che sia possibile fare la richiesta da linea di comando
 • Verificare che l'output sia visualizzato su standard output
 • Verificare che sia possibile specificare il workspace
 • Verificare che ci sia un file esportato associato al workspace
 • Verificare che sia possibile specificare il Channel
 • Verificare che i Member siano visualizzati uno per riga dopo il Channel specificato
 • Verificare che i Member del Channel specificato siano tutti presenti
 • Verificare che non siano visualizzati Member estranei al Channel specificato

 In qualità di utente voglio poter avere informazioni di help issue#7
 Criteri di accettazione:
 • verificare che l'help possa essere richiesto digitando il nome del programma senza parametri aggiuntivi
 • verificare che l'help sia suggerito se un comando digitato non è valido
 • verificare l'help sia mostrato su standard output
 • verificare che siano presenti i comandi per tutte le funzionalità

 In qualità di utente voglio visualizzare la lista dei @mention issue#34
 Criteri di accettazione:
 • Verificare che per ogni @mention sia visualizzata una riga con la coppia (From, To) dove From è lo User che scrive il messaggio con il @mention e To è lo User menzionato.
 • Verificare che le coppie (From, To) non siano ripetute
 • Verificare che le coppie (From, To) corrispondenti a un @mention siano tutte presenti
 • Verificare che siano visualizzate solo coppie (From, To) corrispondenti a un @mention
 • Verificare che sia possibile specificare il Channel e, nel caso sia specificato, la lista sia ristretta ai soli @mention del Channel
 In qualità di utente voglio visualizzare la lista dei @mention che partono da uno User issue#35
 Criteri di accettazione:
 • Verificare che sia possibile specificare lo User da cui partono i @mention 
 • Verificare che per ogni @mention sia visualizzata una riga con la coppia (From, To) dove From è lo User specificato nel comando e To è lo User menzionato.
 • Verificare che le coppie (From, To) non siano ripetute
 • Verificare che le coppie (From, To) corrispondenti a un @mention siano tutte presenti
 • Verificare che siano visualizzate solo coppie (From, To) corrispondenti a un @mention
 • Verificare che sia possibile specificare il Channel e, nel caso sia specificato, la lista sia ristretta ai soli @mention del Channel

 In qualità di utente voglio visualizzare la lista dei @mention che arrivano a uno User issue#36
 Criteri di accettazione:
 • Verificare che sia possibile specificare lo User a cui arrivano i @mention
 • Verificare che per ogni @mention sia visualizzata una riga con la coppia (From, To) dove è lo User che scrive il messaggio con il @mention e To è lo User menzionato e specificato nel comando.
 • Verificare che le coppie (From, To) non siano ripetute
 • Verificare che le coppie (From, To) corrispondenti a un @mention siano tutte presenti
 • Verificare che siano visualizzate solo coppie (From, To) corrispondenti a un @mention
 • Verificare che sia possibile specificare il Channel e, nel caso sia specificato, la lista sia ristretta ai soli @mention del Channel

 In qualità di utente voglio visualizzare la lista pesata dei @mention issue#37
 Criteri di accettazione:
 • Verificare che per ogni @mention sia visualizzata una riga con la tripla (From, To, Weight) dove From è lo User che scrive il messaggio con il @mention, To è lo User menzionato, e Weight (peso associato che riporta il numero di mention da From a To)
 • Verificare che le triple (From, To, Weight) non siano ripetute
 • Verificare che le triple (From, To, Weight) corrispondenti a un @mention siano tutte presenti
 • Verificare che siano visualizzate solo triple (From, To, Weight)* corrispondenti a un @mention
 • Verificare che sia possibile specificare il Channel e, nel caso sia specificato, la lista sia ristretta ai soli @mention del Channel
 In qualità di utente voglio visualizzare la lista pesata dei @mention che partono da uno User issue#38

 Criteri di accettazione:
 • Verificare che sia possibile specificare lo User da cui partono i @mention
 • Verificare che per ogni @mention sia visualizzata una riga con la tripla (From, To, Weight) dove From è lo User specificato nel comando e To è lo User menzionato, e Weight il numero di mention.
 • Verificare che le triple (From, To, Weight) non siano ripetute
 • Verificare che le triple (From, To, Weight) corrispondenti a un @mention siano tutte presenti
 • Verificare che siano visualizzate solo triple (From, To, Weight) corrispondenti a un @mention
 • Verificare che sia possibile specificare il Channel e, nel caso sia specificato, la lista sia ristretta ai soli @mention del Channel
 In qualità di utente voglio visualizzare la lista pesata dei @mention che arrivano a uno User issue#39
 Criteri di accettazione:
 • Verificare che sia possibile specificare lo User a cui arrivano i @mention
 • Verificare che per ogni @mention sia visualizzata una riga con a tripla (From, To, Weight) dove From è lo User specificato nel comando e To è lo User menzionato, e Weight il numero di mention.
 • Verificare che le triple (From, To, Weight) non siano ripetute
 • Verificare che le triple (From, To, Weight) corrispondenti a un @mention siano tutte presenti
 • Verificare che siano visualizzate solo triple (From, To, Weight) corrispondenti a un @mention
 • Verificare che sia possibile specificare il Channel e, nel caso sia specificato, la lista sia ristretta ai soli @mention del Channel
 



## 4. Architettura
  - Stile architetturale adottato

 Per il programma, versione semplificata con command-line interface di SNA4Slack, lo stile architetturale adottato è: Pipe and Filter.
 I sottosistemi elaborano i dati ricevuti in input e mandano l’output in input ad altri sottosistemi:
 –Filter: è un sottosistema (inclusi programmi indipendenti)
 –Pipe: è un’associazione tra sottosistemi (realizzata dal sistema operativo o da un tool) si limitano a trasportare i dati da un canale di output di un sottosistema a un canale di input dell’altro
 –Pipeline è una sequenza lineare di filtri

  ![pipeline](drawings/pipeline.png)
  ![organization1](drawings/organization1.png)
  ![organization2](drawings/organization2.png)


  - Diagramma dei package
 
 ![package](drawings/diagrammapackage.png)
 
  - Diagramma dei componenti
  
 ![diagrammacomponenti](drawings/diagrammacomponenti.png) 
  
  - Commentare le decisioni prese

Dopo varie ricerche abbiamo deciso di utilizzare la libreria Gson perchè rispecchiava, grazie alle funzionalità che offre, le esigenze di estrazione e di elaborazione dei file .json


## 5. System Design  
  - Per ogni requisito funzionale: diagramma delle classi e diagramma di sequenza
 
  ### Sprint1
 ![classisprint1](drawings/classisprint1.png) 
 ![DiagrSeqSprint1](drawings/DiagrSeqSprint1.png) 
  ### Sprint2
 ![classisprint2](drawings/classisprint2.png)  
 ![DiagrSeqSprint2](drawings/DiagrSeqSprint2.png) 
  ### Sprint3
 ![classisprint3](drawings/classisprint3.png)  
 ![DiagrSeqSprint3](drawings/DiagrSeqSprint3.png)
 

  - Menzionare l'eventuale applicazione di design pattern
  
  La struttura del nostro programma si avvicina, alla struttuta, prevista per il Design Pattern, Factory Method ma non aderisce completamente.
  
  - Giustificare le segnalazioni rimaste aperte di PMD e Commentare le decisioni prese 

 L’errore con codice 1: preferiamo non modificarlo poiché scatenerebbe di conseguenza un errore Findbugs.
 Gli errori con codice 2, 3, 4, 5, 98 ,104, 110, 116, 122: l'oggetto iter è un iteratore, ed essendo usato più volte, non può essere sostituito con la funzione .next(), perché porterebbe indesideratamente il puntatore avanti di una posizione ad ogni ciclo, Map.entry non è una classe implementata da noi, quindi non possiamo creare una funzione che rimedi alla legge di Demetra provocata.
 L’errore con codice 6: abbiamo individuato una soluzione atta a risolvere la legge di Demetra provocata, ma abbiamo preferito la soluzione successiva per avere maggiore leggibilità di codice
 ///Soluzione Trovata///
 for (int lung = 1; lung <= mdc.getMembersByChannel(iter.getKey()).length; lung++) {			
 buf.append(" - " + mdc.getUtente(mdc.getMembersByChannel(iter.getKey())[lung]) + " -\n");		
 }
 ///Soluzione scelta///			
 for (final String id: mdc.getMembersByChannel(iter.getKey())) {		
 buf.append(" - " + mdc.getUtente(id) + " -\n");		
 }

 Leggi di Demetra riscontrate:
 Le possibili violazioni di Demetra, che non sono state risolte, avrebbero implicato uno dei seguenti problemi:
 - la creazione in locale di copie di oggetti, ma questo scatenerebbe altre leggi di Demetra;
 - oppure la modifica di classi di libreria (util, lang, Gson) alle quali non abbiamo accesso.

 ////////MainMenu////////
 Non abbiamo abbassato la complessità ciclomatica per una migliore compattezza e leggibilità del codice
 Codice errore 16: Abbiamo evitato l'uso del varargs per non aggiungere ulteriori controlli sull'attributo args e non aumentare ulteriormente la complessità ciclomatica

 ////////MentionUtility//////// 
 Non abbiamo abbassato la complessità ciclomatica per una migliore compattezza e leggibilità del codice
 Leggi di Demetra: creazine locale di oggetti (user e text) per una migliore leggibilità del codice.

 ///////UnzipUtility///////
 Le leggi di Demetra violate non sono state corrette, poichè la classe UnzipUtility estrae i contenuti dei Json, utilizzando la libreria Gson, che impedisce una diversa implementazione, risulta quindi inevitabile la creazione di oggetti in locale, dato che la libreria stessa utilizza una metodologia di estrazione in singola apertura e singola lettura di ogni file, si ritiene quindi necessario un ciclo per poter visitare tutto il workspace all'interno dello zip.

 //////PMD nei test/////
 Leggi di Demetra riscontrate:
 Le possibili violazioni di Demetra che non sono state risolte avrebbero implicato uno dei seguenti problemi:
 - la creazione in locale di copie di oggetti, ma questo scatenerebbe altre leggi di Demetra;
 - oppure la modifica di classi di libreria (util, lang, Gson) alle quali non abbiamo accesso.

 Codice errore 55: La classe MainMenuTest contiene tutti i metodi per testare la classe MainMenu in tutti i casi possibili (corretti o di errore), ma essendo superiori a 10 viene segnalato come PMD.



## 6. Riepilogo del test    
  - Riportare la tabella riassuntiva di coveralls (o jacoco), con dati sul numero dei casi di test e copertura del codice
  ![reportjacoco](drawings/reportjacoco.png)

## 7. Manuale utente
L'elenco dei comandi a disposizione per le operazioni eseguibili dall’utente da command-line interface sono:

| COMANDO                                                  | DESCRIZIONE                                                                |
|:---------------------------------------------------------|---------------------------------------------------------------------------:|
| help or sna4slack                                        | Stampa la lista dei comandi                                                |
| -w <nome del workspace>                                  | Imposta il workspace su cui lavorare                                	|
| -m                                                       | Stampa la lista di Membri                                                  |
| -c                                                       | Stampa la lista dei Channel                                                |
| -m -c                                                    | Stampa la lista dei Membri divisi per tutti i Channel                      |
| -c <nome del channel>                                    | Stampa la lista dei Membri del Channel selezionato                         |
| mention                                                  | Stampa la lista globale delle mention                                      |
| mention -c <nome del channel>                            | Stampa la lista dei mention presenti in quel channel                       |
| mention -f <nome_display utente>                         | Stampa la lista globale dei mention che partono dall'utente                |
| mention -f <nome_display utente> -c <nome del channel>   | Stampa la lista dei mention che partono dall'utente in quel channel        |
| mention -t <nome_display utente>                         | Stampa la lista globale dei mention che arrivano all'utente                |
| mention -t <nome_display utente> -c <nome del channel>   | Stampa la lista dei mention che arrivano all'utente in quel channel        |
| pmention                                                 | Stampa la lista globale pesata delle mention                               |
| pmention -c <nome del channel>                           | Stampa la lista pesata dei mention presenti in quel channel                |
| pmention -f <nome_display utente>                        | Stampa la lista globale pesata dei mention chepartono dall'utente          |
| pmention -f <nome_display utente> -c <nome del channel>  | Stampa la lista pesata dei mention che partono dall'utente in quel channel |
| pmention -t <nome_display utente>                        | Stampa la lista globale pesata dei mention che arrivano all'utente         |
| pmention -t <nome_display utente> -c <nome del channel>  | Stampa la lista pesata dei mention che arrivano all'utente in quel channel |


## 8. Processo di sviluppo e organizzazione del lavoro 

  Per i vari Sprint, dopo l'assegnamento dei Done c'era la ripartizione dei compiti all'interno del gruppo. Prevalentemente per la durata del progetto, abbiamo lavorato solitamente en pair, poichè lavorare in "sottogruppi da due" risultava più semplice, poichè suddividere ulteriormente il lavoro singolarmente risultava più difficile anche sotto il punto di vista di spiegare il codice e di dover essere per forza tutti e 4 presenti contemporaneamente; effettuando daily Sprint di 10-15 minuti, prima di iniziare a lavorare; Quando non era possibile incontrarsi, si lavorava in coppie da due, e i Daily Meeting avvenivano su Skype per coordinare il lavoro, le comunicazioni interne avvenivano su Slack.  Committando da soli due pc, il backoffice organizzativo non visibile su GitHub, in quanto i vari reports, di ogni Sprint, (non sono stati caricati di pari passo). alla fine di ogni Sprint, della durata di circa 10giorni, effettuavamo lo Sprint Review interno tra i membri del team per poter procedere alla consegna. dopo la cosegna seguiva lo Sprint Retrospective in aula e successivamente  l' assegnazione dei nuovi Done.


## 9. Analisi retrospettiva
  - Cosa ha funzionato bene e rifarei in futuro: in ogni Sprint avere poche nuove features, in modo da concentrarsi anche sulla documentazione e sui test
  - Cosa non ha funzionato bene e non rifarei in futuro : la configurazione tutta all' inizio, nel primo Sprint; Le risoluzioni dei Reports e dei test in uno Sprint Separato e /o dedicato, poichè ha tolto del tempo rallentando così quelle che erano le tempistiche degli altri Sprint
  - Cosa farei di nuovo: Lavorare di nuovo en pair con il backoffice non visibile
