# INGEGNERIA DEL SOFTWARE

## 1. CONCETTI FONDAMENTALI

### Tipologie di Software Professionale

SOFTWARE: insieme dei programmi e relativa documentazione (modelli di progetto, manuali utente, siti web di supporto)

- **software generico**: prodotto autonomamente, incontra la necessità di svariati clienti. Il produttore ha controllo sulle specifiche
- **software su richiesta**:sviluppato da un'organizzazione per un specifico cliente. Il produttore deve attenersi alle specifiche del cliente

### Sviluppo professionale di software di qualità

Caratteristiche qualitative di un software professionale_

- **accettabilità**: deve essere accettabile per il cliente
- **Fidatezza e Protezione**: non deve causare danni fisici e economici iun caso di malfunzionamento. Non vulnerabile ad attacchi da parte di utenti malintenzionati
- **Efficienza**: le risorse non devono essere sprecate
- **Manutenibilità**: deve poter evolvere per soddisfare nuove richieste dei clienti

### Definizione di Ingegneria del Software

Adottare approcci ingegneristici alla produzione di software, disciplina ingegneristica.

### Processi di Sviluppo del Software

**Processo software**: attività che portano a creazione/evoluzione di un software

- **Acquisizione, analisi e specifica dei requisiti**: definizione delle funzionalità e dei vincoli operativi del software
- **Progettazione e sviluppo**: progettazione e programmazione
- **Verifica e validazione**: verifica che il software soddisfi i requisiti
- **Evoluzione**: modifiche al software per correggere errori o migliorare funzionalità

Si distingue in metodi e strumnenti:

- **metodi**: approcci strutturati per sviluppare software di qualità, con costi contenuti e nei tempi previsti
- **strumenti**: sistemi software per aiutare le attività dei processi software (analisi, modellazione, debugging, testing)

Alcune sfide per processi software:

- **diversità**: metodi per produrre software su dispositivi eterogenei
- **consegna**: consentirla in tempi rapidi
- **fiducia**: tecniche che rendano il software affidabile e sicuro agli occhi del cliente
- **scala**: software distribuito su sistemi diversi

I **principi fondamentali** sono:

- metodi specifichi dipendono dal contesto del progetto
- non esistono metodi universalmente applicabili
- i concetti fondamentali sono indipendenti dal linguaggio di programmazione

(... ultime slide)

## 2. PROCESSI SOFTWARE: ATTIVITÀ FONDAMENTALI

### Code and Fix

Consiste nel

- scrivere codice
- aggiustare errori, migliorarlo, aggiungere funzionalità

Approccio **molto limitato** in contesti di grandi dimensioni

### Definizione di Processo Software

Il processo software è quell'insieme strutturato di attività che portano alla creazione di un software. Un processo di qualità migliora qualità del software, tempi di sviluppo e costi.

### Attività Fondamentali

- **Acquisizione, analisi e specifica dei requisiti**: definizione delle funzionalità e dei vincoli operativi del software
- **Progettazione e sviluppo**: progettazione e programmazione
- **Verifica e validazione**: verifica che il software soddisfi i requisiti
- **Evoluzione**: modifiche al software per correggere errori o migliorare funzionalità

**Studio di fattibilità**: stabilisce se sviluppo debba essere avviato, determinando

- se esiste un mercato
- se il progetto è tecnicamente ed economicamente fattibile

Fornisce un report con definizione problema, valutazione costi/benefici, risorse necessarie, soluzioni alternative, tempi di consegna e modalità sviluppo

### 1 - Acquisizione, Analisi e Specifica dei Requisiti

Serve a determinare **cosa** farà il software.
Specifica le **funzionalità e le qualità** che deve possedere, **senza vincolare progettazione** e implementazione.
Definisce **funzioni e vincoli** con il cliente
Un errore in questa fase è molto costoso

**Ingegneria dei Requisiti**: metodi per raccogliere, analizzare, documentare e gestire i requisiti del software

#### Deduzione e analisi dei requisiti

DEDUZIONE: spirito critico e coinvolge osservazione di sistemi esistenti, discussioni con possibili utenti

ANALISI: sviluppo di uno o più modelli e prototipi

#### Specifica dei requisiti

traduce le informazioni raccolte in un insieme di requisiti

- _requisiti di sistema_: funzionalità e caratteristiche che devono essere fornite
- _requisiti utente_: proposizioni astratte dei requisiti del sistema per i clienti

#### Convalida dei requisiti

Fase in cui si controlla che i requisiti siano realistici, coerenti e completi. Possibile rilevazione di errori nel documento dei requisiti

#### Documento dei requisiti

Documento più o meno formale contenente l'insieme dei requisiti. In questa fase viene predisposto un piano di test

**[immagine diagramma requisiti]**

### 2 - Progettazione e Sviluppo

Parte che si occupa della conversione dei requisiti in un sistema eseguibile. In due fasi:

- **progettazione**: progettare struttura software che realizzi le specifiche
- **sviluppo**: implementazione dei componenti definiti nel progetto

La distinzione o meno dipende dal tipo di processo software adottato.

#### Progettazione

Le fasi di progettazione sono intrecciate e interdipendenti, continue revisioni anche delle fasi precedenti

**input di progettazione**: requisiti, descrizione dei dati, informazioni sulla piattaforma software in cui sarà eseguito (sistema operativo, database, altre applicazioni)

##### Attività di progettazione

- **progettazione dell'architettura**: progetto alto livello, identificazione struttura complessiva e componenti principali
- **progettazione dell'interfaccia**: definizione interfaccia tra componenti, non ambigua
- **progettazione e scelta dei componenti**: scelta dei componenti già disponibili, progettazione nuovi componenti. Progetto dettagliato ma generalmente senza dettagli di implementazione
- **progettazione del database**: definizione struttura del database, tabelle, relazioni e vincoli

L'output della progettazione è un progetto software che descrive struttura, modelli e strutture dati usati dal sistema e interfacce usate.

[immagine diagramma progettazione - slide 22]

#### Sviluppo

Lo sviluppo è strettamente dipendente dal singolo programmatore, ma è possibile che ci siano standard aziendali e convenzioni condivise.

### 3 - Verifica e Validazione

**Verifica**: mostrare conformità del sistema alle specifiche

**Validazione**: mostrare che il sistema soddisfa le aspettative del cliente

Generalmente ottenute tramite **testing** medianti dati di prova ricavati dalle specifiche.

#### Testing

Suddivisibile in tre fasi:

- **test dei componenti**: test di singoli componenti in isolamento (unità o gruppi di funzioni e classi)
- **test del sistema**: testare il sistema completo, oppure in più stadi con diverse componenti integrate, verificando conformità requisiti funzionali e non funzionali
- **test del cliente**: sistema testato dal cliente con dati reali, verificando che soddisfi le sue aspettative

La fase di testing è **iterativa**, se emergono difetti può essere necessario ripercorrere le altre fasi di testing

### 4 - Evoluzione

Il software viene costantemenete riusato, evoluto e mantenuto, modificandolo ripetutamente durtante il suo ciclo di vita. Questo avviene per

- correggere errori
- migliorare funzionalità
- adattarlo a nuovi ambienti operativi

## 3. MODELLI DI PROCESSI SOFTWARE

**CSV - modello del ciclo di vita del software**: caratterizzazione descrittiva o prescrittiva di come dovrebbe essere sviluppato un software

**modello di processo software**: descrizione semplificata e astratta di un processo software

Ogni processo può essere descritto tramite

- **descrizione architetturale**: descrive la sequenza di attività senza fornire dettagli
- **data-flow**: evidenzia trasformazioni dei dati dalle attività del processo
- **role/action**: ruole e responsabilità di chi svolge le attività del processo

La descrizione del processo software include:

- **attività**: cosa deve essere fatto e in che ordine
- **prodotti**: risultati di ogni attività
- **ruoli**: chi deve svolgere le attività
- **pre e post condizioni**: condizioni che devono essere soddisfatte prima e dopo ogni attività, criteri di transizione

Ci sono diversi tipologie di modelli, tra cui:

- **plan-driven**: pianificazione dettagliata di tutte le attività prima di iniziare lo sviluppo
- **agile**: sviluppo iterativo e incrementale, con frequenti revisioni e

### Modelli a cascata

#### Modello a cascata

[immagine diagramma modello a cascata]

Si tratta di un processo:

- **plan-driven**: ciascuna fase segue quella successiva, le attività di prorocessso sono pianificate in anticipo
- **document-centric**: ogni attività produce documenti che vengono utilizzati come input per le attività successive
- **rigido**: fine di ogni fase è un milestone, gli output di una fase non sono modificabili nelle fasi successive
- **monolitico**: cliente riceve il software solo alla fine del processo

**vantaggi**: fasi e rispettivi output ben definiti

**svantaggi**:

- richiede chiarezza dei requisiti fin da subito e stabilità degli stessi
- produce notevole mole di documentazione
- poco flessibile

Pertanto il modello a cascata risulta:

- adatto a software che richiedono documentazione dettagliata
- adatto a sistemi integrati in cui software deve interfacciarsi con sistemi hardware non flessibili

**non adatto** a:

- piccoli team dove comunicazione è informale e contesti in cui i requisiti cambiano notevolmente

#### Modello a cascata con retroazione

Variazione del modello a cascata con introduzione della **retroazione**, verifica della correttezza dell'output con possibilità di ripetere le fasi precedenti, grazie all'uso di **feedback**

[immagine diagramma modello a cascata con retroazione]

- più flessibile del modello a cascata, mitigandone la monoliticità
- adatto a contesti in cui i requisiti sono poco soggetti a cambiamenti

#### Modello a V

Estensione del modello a cascata, in cui le attività di **progetto** sono collegate a quelle di **V&V (verifica e validazione)**

[immagine diagramma modello a V]

Ogni fase di progettazione è associata a una fase di V&V
La fase di V&V è guidata da un insieme di piani di test, eseguito da un team indipendente

In caso di errore nella fase V&V, si rieseguono le fasi di progettazione collegate

Permette di anticipare validazione dei requisiti da parte del cliente, rilevando precocemente eventuali errori

### Modelli evolutivi

Adatti a contesti con requisiti non chiari fin dall'inizio del processo

Due tipologie fondamentali:

- **modello a sviluppo incrementale**: lavorare con il cliente
- **modello a consegna incrementale**: realizzazione di prototipi per esplorare requisiti

**vantaggi**:

- rapido feedback del cliente su versione preliminare
- possibilità di cambiare i requisiti prima della consegna finale
- consegna di versioni preliminari con funzionalità fondamentali
- primi incrementi utili per dedurre requisiti successivi
- funzionalità con maggiore priorità testate maggiormente

**svantaggi**:

- mancanza di visibilità del processo
- sistemi mal strutturati per continui cambiamenti

**applicabilità**:

- componenti di piccole dimensioni
- sistemi a vita breve
- sistemi con requisiti che cambiano durante sviluppo

#### Modello a sviluppo incrementale

Si sviluppa una implementazione iniziale che viene esposta agli utenti e che verrà perfezionata attraverso **incrementi** ovvero versioni successive.

[immagine diagramma modello a sviluppo incrementale]

Posso partire da una descrizione sommaria dei requisiti

le varie fasi (specifica, sviluppo, convalida) sono intrecciate con feedback veloci

1. versione iniziale con requisiti fondamentali esposta agli utenti
2. feedback di proxy degli utenti finali in ambiente diverso da quello target
3. implementazioni di funzionalità e requisiti ulteriori in versioni intermedie (solitamente NON mostrate al cliente)
4. ultimo incremento è versione finale rilasciata al cliente

#### Modello a consegna incrementale

Alcuni degli incrementi sviluppati sono consegnati al clienti

[immagine diagramma modello a consegna incrementale]

**vantaggio**: feedback più realistico
**limitazione**: utenti devono aver tempo per testare adeguatamente gli incrementi rilasciati

A ogni incremento viene inclusa una parte delle funzionalità, secondo dei livelli di priorità. I requisti di un incremento sono congelati una volta consegnati

#### Modello prototipale

**prototipo**: versione iniziale di un sistema software sviluppato rapidamente, generalmente **usa e getta**. Generalmente potrebbe non rispettare aspetti fondamentali (es. prestazioni)

[immagine diagramma modello prototipale]

1. stabilire esplicitamente obiettivi del prototipo (piano di prototipazione)
2. definire quali funzionalità includere nel prototipo (definizione dello schema)
3. sviluppo del prototipo (prototipo)
4. fase di valutazione del prototipo (report valutativo)

Il prototipo necessita di formazione degli utenti sull'utilizzo, inoltre ha dei problemi di rappresentatività:

- non è parte del sistema reale (al contrario degli incrementi)
- valutatori non rappresentativi
- uso può differe da quello del sistema reale

NOTA: prototipazione può affiancare altri modelli

- durante la progettazione (modello a cascata) per valutare opzioni alternative
- durante validazione del sistema per controllarne il comportamento

### Modelli orientati al riuso

Oltre che in maniera informale, avviene mediante:

- componenti software riutilizzabili
- interi sistemi (COTS)

Sfrutta dei **framework di integrazione** per comporre **componenti riutilizzabili** e **COTS**

[immagine diagramma modello orientato al riuso]

- requisiti specificati in maniera non dettagliata
- ricerca e valutazione di componenti e sistemi che possono offrire le funzionalità richieste
- requisiti perfezionati in base alle componenti disponibili e viene aggiornata la specifica
- se disponibile sistema adeguato,configurato per il nuovo sistema
- altrimenti componenti e sistemi possono essere adeguati alle nuove richieste insieme a componenti ex novo

**vantaggi**:

- riduce quantità software ex novo
- costi e rischi ridotti
- velocità consegna

**svantaggi**:

- compromessi nei requisiti
- evoluzione delle componenti non controllate direttamente

#### Modelli trasformazionali

Le specifiche vengono definite mediante linguaggi formali (specifiche algebriche, modelli di stato)

Correttezza mediante model checking

Specifiche formali trasformate automaticamente in codice eseguibile

1. requisiti specificati formalmente in fase di analisi, compresi chiaramente e in modo non ambiguo, verificate automaticamente
2. man mano trasformati in descrizione più dettagliata e meno astratta, fino a ottenere codice eseguibile
3. può trarre vantaggio da componenti riusabili

**problemi**:

- necessarie competenze specifiche per scrivere specifiche formali
- difficile specificazione formale di alcune parti
- difficoltà da parte del cliente a convalidare i requisiti

**applicabilità**:

- NO a sistemi di grande dimensioni
- ottimo per parti critiche, dove validità va dimostrata **by construction**

## 4. SVILUPPO AGILE DEL SOFTWARE

**processi plan-driven**: con pianificazione dettagliata, ottimi per sistemi critici, con team numerosi e lontani, progetti e software di lunga durata.Poco adatti a contesti dinamici, poco flessibili.

Necessità di risposta rapida, comunicazione fra stakeholder e cliente nel processo per feedback rapido &rarr; agilità

### Caratteristiche generali

**documentazione minima**:

- focus sul codice
- no specifiche dettagliate
- overhead documentazione limitata

**consegna rapida e incrementale**:

- incrementi rilasciati frequentemente
- stakeholder coinvolti

**strumenti di supporto**:

- uso di strumenti di supporto del processo di sviluppo (es. automatizzazione test)

|processi plan-driven            |processi agili                                              |
|--------------------------------|------------------------------------------------------------|
|attività pianificate in anticipo|                   pianificazione incrementale continua     |
| fasi processo software distinte|requisiti, progettazione e implementazione contemporanemente|
| incrementi pianificati         | incrementi rapidi                                          |

Pratiche plan-driven e agili possono coesistere

### Principi agili

**coinvolgimento del cliente**: coinvolti in tutto il processo di svluppo

- valutano e validano
- forniscono nuovi requisiti e propongono modifiche
- assegnano priorità

**accettare i cambiamenti**: prodotto non pianificato rigidamente, prevedere che i requisiti cambieranno

**mantenere la semplicità**: prodotto e processo di sviluppo semplici, eliminare le complessità

**sviluppo incrementale**: software consegnato incrementalmente, cliente specifica i requisiti da includere negli incrementi

**persone, non processi**: processo di sviluppo non eccessivamente prescrittivo e rigido

#### Applicabilità

**adatto a**:

- prodotti di piccole e medie dimensioni
- prodotti personalizzati (con coinvolgimento cliente)
- pochi stakholder
- team fisicamente vicini, con comunicazione informale

**vantaggi**:

- consegne predicibili
- rapida risposta a cambiamenti
- rischi bassi grazie a cicli di consegna rapidi
- alta produttività
- clienti soddisfatti

**esempio**:

- prodotto evolve con brevi iterazioni
- iterazioni con durata fissa (es. 2 settimane)
- applicazione funzionante rilasciata a fine di ogni iterazione, aggiungendo quante più funzionalità ad alta priorità possibili
- cliente rivede ogni incremento e ridefinisce priorità
- non si fallisce una data di consegna, piuttosto si rimanda qualche feature

### Tecniche agili

#### Extreme Programming (XP)

#### Tecniche agili - Storie Utente

#### Tecniche agili - Refactoring

#### Tecniche agili - Sviluppo preceduto dai Test

#### Tecniche agili - Pair Programming

#### Tecniche agili - Scrum
