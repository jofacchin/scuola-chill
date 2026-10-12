# PRD Template

# PRD di ScuolaChill · Team Giorgia Facchin

<aside>
💡

**Come usare questo template**

Duplica questa pagina e compilala con il tuo team. Dove trovi del testo in *corsivo*, sostituiscilo con il vostro. I callout 💡 sono consigli per te: cancellali prima della consegna da questo markdown.

Il documento ha due parti. Nella prima scrivi **cosa** fa ScuolaChill, nella seconda **come** lo costruirai. Tienile separate. Chi legge la prima parte deve capire tutto senza sapere cos'è Spring Boot.

Un buon PRD sta fra le 15 e le 25 pagine. Se ne scrivi di più, probabilmente stai descrivendo invece di decidere.

</aside>

---

## Informazioni sul documento

|  |  |
| --- | --- |
| **Prodotto** | ScuolaChill |
| **Team** | *Giorgia Facchin (progetto individuale)* |
| **Autori** | *Giorgia Facchin* |
| **Versione** | *1.0* |
| **Data** | *25/09/2026* |
| **Stato** | *Bozza* |

### Storico delle versioni

| Versione | Data | Autore | Cosa è cambiato e perché |
| --- | --- | --- | --- |
| 1.0 | *25/09/2026* | *Giorgia Facchin* | Prima stesura |
|  |  |  |  |

<aside>
💡

Il PRD cambierà durante l'anno. Ogni modifica va registrata qui, con la sua ragione. Un PRD che dice una cosa mentre il codice ne fa un'altra è peggio di nessun PRD.

</aside>

---

# Prima parte · Il cosa

## Scopo e perimetro

### Perché esiste ScuolaChill

**Dal lato business.** *ScuolaChill è un'applicazione per scuole superiori e ITS. Offre funzionalità simili a quelle dei registri elettronici delle grandi aziende, ma è progettata da una studentessa partendo dalle richieste reali di studenti e docenti.*

**Dal lato tecnico.** *ScuolaChill riunisce in un unico posto voti, verifiche, compiti e materiale didattico, per rendere l'esperienza scolastica più semplice e meno stressante.*

### Cosa è incluso

- *Direttore: ha l'account amministratore e il pieno controllo dell'applicazione. Crea gli account dei docenti, accetta i moduli di iscrizione da cui nascono gli account degli studenti, crea le classi, vede le interazioni tra docenti e studenti, blocca i profili e reimposta le password.*
- *Docente: accede solo al proprio account. Carica materiale didattico, assegna compiti per casa, crea verifiche e inserisce i voti nella pagina Voti. Può scrivere annotazioni private rivolte a un singolo studente, visibili solo a quello studente e al direttore.*
- *Famiglia: non ha un account. Compila online il modulo di iscrizione dello studente, che il Direttore controlla e accetta.*
- *Studente: accede solo al proprio account. Consulta il materiale didattico, svolge le verifiche create dal docente, carica i compiti per casa, legge e risponde alle annotazioni di docenti e direttore e consulta i propri voti nella pagina Voti.*

### Cosa non è incluso

- *Assenze e giustificazioni.*
- *Firma di registro: il docente non registra argomenti e ore di lezione. Vede però l'elenco degli studenti della classe.*
- *Ingressi in ritardo e uscite anticipate.*
- *Comunicazioni su assenze dei docenti e scioperi.*
- *Avvisi e circolari della segreteria.*


<aside>
💡

La lista di cosa **non** è incluso è la più preziosa del documento. Ogni riga qui ti evita una settimana di discussioni più avanti.

</aside>

---

## Stakeholder

| Stakeholder | Cosa fa | Cosa gli interessa | Come lo coinvolgete |
| --- | --- | --- | --- |
| Direttore | Gestisce la scuola e gli account, approva l'adozione di ScuolaChill | Avere il controllo su utenti e classi, proteggere i dati di studenti e docenti | Interviste e revisione delle funzionalità |
| Docenti | Caricano materiale, creano verifiche, assegnano voti | Fare in fretta le operazioni quotidiane, non perdere voti e consegne | Sondaggi e interviste |
| Studenti | Svolgono verifiche, caricano compiti, consultano voti e materiale | Usare l'app facilmente dal telefono, vedere subito voti e scadenze | Sondaggi e interviste |
| Docente del corso | Valida il PRD | Che il PRD sia completo, coerente e realizzabile | Presentazione e domande |
| Collaudatori del primo anno | Usano ScuolaChill come utenti reali | Che l'app funzioni bene e sia semplice da usare | Sessioni di collaudo guidate e questionario finale |

<aside>
💡

Gli stakeholder non sono solo gli utenti. Sono anche chi approva, chi paga, chi manterrà il sistema. Chiediti chi resterebbe deluso se ScuolaChill non funzionasse.

</aside>

---

## Destinatari e contesto d'uso

### La scuola che avete immaginato

*Descrivi la scuola per cui progettate. Che tipo di istituto è, dove si trova, come si organizza la giornata. Questi dati tornano nella stima del carico, quindi scegli numeri che poi userai davvero.*

|  | Valore |
| --- | --- |
| Numero di studenti | 300 |
| Numero di docenti | 20 |
| Numero di classi | 20 |
| Orario scolastico | Lunedì–venerdì 8:00–13:20, più un giorno a settimana con 8 ore di lezione |
| Connettività | Wi-Fi scolastico con firewall che limita l'accesso degli studenti |

### Gli archetipi

Arricchisci gli archetipi della traccia.

| ID | Archetipo | Contesto d'uso | Competenze digitali | Dispositivo principale | Frequenza d'uso |
| --- | --- | --- | --- | --- | --- |
| ARC-001 | Direttore | A scuola, in ufficio | Basse | PC portatile o fisso | Giornaliera |
| ARC-002 | Docente | A scuola e a casa | Medie, in genere abituato al registro elettronico | PC | Giornaliera |
| ARC-003 | Studente | A scuola e a casa | Alte, molto pratico con telefono e computer | Smartphone o tablet | Giornaliera |

<aside>
💡

I collaudatori veri sono i ragazzi del primo anno. Usano lo smartphone in corridoio o il PC in laboratorio? La risposta cambia l'interfaccia, i requisiti di usabilità e perfino il dimensionamento.

</aside>

---

## Panoramica e casi d'uso

### ScuolaChill in poche righe

ScuolaChill è un registro elettronico interno alla scuola, nato dalle esigenze reali di studenti e docenti. Serve a semplificare e automatizzare il lavoro di tutti i giorni e a creare un canale di comunicazione diretto fra studenti, docenti e direttore.

### User flow e scenari

Per ogni ruolo, scegli **almeno tre** storie principali e descrivi il percorso completo.

**Storia:** *es. STU-02 · Svolgere una verifica*

**User flow**

1. *Lo studente accede a ScuolaChill*
2. *Apre la sezione Verifiche*
3. *…*

**Scenario principale.** *Racconta il caso in cui tutto va bene, con un personaggio e una situazione concreta.*

**Scenari alternativi.** *Cosa succede quando qualcosa va storto? Connessione che cade, scadenza superata, doppia scheda aperta…*

*Ripeti il blocco per le storie principali di Direttore e Docente.*

---

## Requisiti funzionali

### Le user story della traccia

| ID | Storia | AC aggiunti dal team | Note |
| --- | --- | --- | --- |
| DIR-01 | Creare account docente | *…* | *…* |
| DIR-02 | Creare account studente | *Come Direttore, voglio accettare i moduli di iscrizione inviati dalle famiglie, così da non dover inserire a mano i dati di ogni studente, risparmiando tempo ed evitando errori di trascrizione.<br><br>AC-DIR-02-01 · Dati mancanti. **Dato che** la famiglia sta compilando il modulo di iscrizione online, **quando** prova a inviarlo con uno o più campi obbligatori vuoti, **allora** il modulo non viene inviato e i campi mancanti vengono segnalati. Fra i campi obbligatori ci sono la mail, il numero di telefono e l'indirizzo postale di chi fa la richiesta, e l'indirizzo di studio scelto.<br><br>AC-DIR-02-02 · Ricezione. **Dato che** la famiglia ha compilato e inviato correttamente il modulo, **quando** il Direttore apre la sezione Iscrizioni, **allora** trova il modulo ricevuto con tutti i dati dello studente già compilati, pronto per essere controllato.<br><br>AC-DIR-02-03 · Accettazione. **Dato che** il Direttore ha controllato un modulo ricevuto e i dati sono corretti, **quando** accetta il modulo, **allora** viene creato l'account studente con: la mail istituzionale nel formato iniziale.cognome@mailistituzionale.it, usata per il login; la mail del genitore indicata nel modulo, usata per recuperare l'account; una password temporanea, inviata alla mail del genitore, che lo studente deve cambiare al primo accesso.<br><br>AC-DIR-02-04 · Dati da verificare. **Dato che** il Direttore sta controllando un modulo ricevuto, **quando** trova dati anagrafici errati o dubbi, **allora** può chiedere alla famiglia di inviare documenti a supporto, e il modulo resta in sospeso, senza creare l'account, finché il Direttore non lo accetta.<br><br>AC-DIR-02-05 · Studenti con lo stesso nome. **Dato che** la mail iniziale.cognome è già in uso, **quando** il Direttore accetta il modulo, **allora** il sistema crea una mail diversa seguendo FR-ISC-01.<br><br>AC-DIR-02-06 · Account non attivato. **Dato che** sono passati 3 giorni dall'invio della password temporanea, **quando** lo studente non l'ha ancora cambiata, **allora** il Direttore viene avvisato e contatta chi ha fatto la richiesta di iscrizione per telefono o per posta, usando i recapiti del modulo.<br><br>AC-DIR-02-07 · Indirizzo di studio. **Dato che** il modulo indica l'indirizzo di studio scelto, **quando** il Direttore accetta il modulo, **allora** lo studente viene collegato a quell'indirizzo e resta "da assegnare" finché il Direttore non conferma la composizione delle classi (AC-DIR-03-01).* | *Le famiglie non hanno un account: compilano solo il modulo. Dipende dal servizio email esterno (invio della password temporanea): se la mail non arriva, AC-DIR-02-06 fa da piano di riserva. Vedi FR-ISC-01 e FR-ISC-02.* |
| DIR-03 | Creare classi e comporle | *AC-DIR-03-01 · Proposta delle classi. **Dato che** ci sono studenti accettati e "da assegnare" per un indirizzo, **quando** il Direttore chiede di comporre le classi, **allora** ScuolaChill propone il minor numero di classi che non superano 26 studenti ciascuna, con gli studenti divisi in parti il più possibile uguali (al massimo 1 studente di differenza fra una classe e l'altra). Se gli iscritti sono meno di 12, propone una classe mista con un altro indirizzo dello stesso anno (FR-CLA-03).<br><br>AC-DIR-03-02 · Conferma del Direttore. **Dato che** ScuolaChill ha proposto le classi, **quando** il Direttore le rivede, **allora** può confermarle così come sono oppure cambiarle (unire, dividere, spostare studenti). Nessuna classe viene creata senza la sua conferma.<br><br>AC-DIR-03-03 · Trasferimento fra classi. **Dato che** sta iniziando un nuovo anno scolastico, **quando** il Direttore trasferisce uno studente in un'altra classe, **allora** tutti i voti già presi restano allo studente e restano visibili nella sua pagina Voti, e lo studente vede docenti, orario, materiale, compiti e verifiche della nuova classe.<br><br>AC-DIR-03-04 · Nessun trasferimento durante l'anno. **Dato che** l'anno scolastico è in corso, **quando** il Direttore prova a trasferire uno studente, **allora** il trasferimento non è permesso.<br><br>AC-DIR-03-05 · Classe di arrivo piena. **Dato che** la classe di arrivo ha già 26 studenti, **quando** il Direttore trasferisce uno studente, **allora** ScuolaChill lo avvisa e il Direttore può accettare al massimo 2 studenti in più (28 in tutto). Oltre i 28 il trasferimento non è permesso e il Direttore deve dividere la classe.* | *Esempi: 10 iscritti → classe mista con un altro indirizzo; 24 → 1 classe da 24; 30 → 2 classi da 15; 50 → 2 classi da 25; 55 → 3 classi da 18, 18 e 19. Il Direttore può sempre cambiare la proposta. Vedi FR-CLA-01.* |
| DIR-04 | Vedere tutto | *…* | *…* |
| DOC-01 | Caricare materiale didattico | *…* | *…* |
| DOC-02 | Creare le proprie verifiche | *AC-DOC-02-01 · Correzione automatica delle domande aperte. **Dato che** il docente ha creato una domanda aperta indicando le parole chiave che la risposta deve contenere, **quando** lo studente consegna la verifica, **allora** il sistema propone un colore in base a quante parole chiave (o sinonimi) la risposta contiene: rosso (probabilmente errata) se non ne contiene nessuna; arancione (da controllare) se ne contiene da 1 fino alla metà inclusa; verde (probabilmente corretta) se ne contiene più della metà. La metà si arrotonda per difetto.<br><br>AC-DOC-02-02 · Il colore è solo un suggerimento. **Dato che** il sistema ha proposto i colori, **quando** il docente corregge la verifica, **allora** vede per ogni risposta un punteggio proposto (verde = punteggio massimo, rosso = 0, arancione = da assegnare) e può cambiare il punteggio di qualsiasi risposta, di qualunque colore.* | *Esempi: 4 parole chiave → 0 = rosso, 1–2 = arancione, 3–4 = verde. 5 parole chiave → 0 = rosso, 1–2 = arancione, 3–5 = verde. Parole chiave e sinonimi li scrive il docente. Il colore può sbagliare in entrambe le direzioni: "La Rivoluzione francese non è iniziata nel 1789" contiene le parole chiave ma è sbagliata; alla domanda "Quante mogli ebbe Enrico VIII?" (parola chiave: 6) la risposta "Caterina d'Aragona, Anna Bolena, Jane Seymour, Anna di Clèves, Caterina Howard, Caterina Parr" è rossa ma giusta. In entrambi i casi decide il docente. Lo stesso vale per un sinonimo giusto che il docente non aveva previsto: la risposta resta rossa o arancione, ma il docente può darla per giusta. Vedi FR-VER-01.* |
| DOC-03 | Assegnare i voti | *AC-DOC-03-01 · Calcolo del voto di una verifica. **Dato che** il docente ha rivisto la verifica e ogni risposta ha un punteggio fra 0 e il massimo della domanda (le arancioni di AC-DOC-02-01 vanno valutate per forza, le altre si possono cambiare), **quando** il docente conferma la correzione, **allora** il voto viene calcolato in proporzione da 4 a 9 con la formula voto = 4 + 5 × (punti ottenuti ÷ punti totali), arrotondato al mezzo voto più vicino (a metà strada si arrotonda per eccesso).<br><br>AC-DOC-03-02 · Modifica manuale. **Dato che** il voto è stato calcolato, **quando** il docente lo modifica a mano, **allora** può scegliere solo un voto fra 4 e 10 a passi di mezzo voto, e viene salvato il voto scelto. È l'unico modo per assegnare 10. Un voto sotto 4 o non multiplo di 0,5 viene rifiutato.* | *Esempio: 10 domande da 1 punto. 0 punti → 4; 6 punti → 7; 10 punti → 9. Con 20 domande da 1 punto, 11 punti → 6,75 → 7. Vedi FR-VOT-01.* |
| STU-01 | Consultare il materiale didattico | *…* | *…* |
| STU-02 | Svolgere una verifica | *AC-STU-02-01 · Nessun risultato prima della correzione. **Dato che** lo studente ha consegnato la verifica, **quando** la riapre prima che il docente abbia confermato la correzione, **allora** vede solo le proprie risposte e lo stato "In correzione": nessun colore, nessun punteggio e nessun voto.* | *I colori di AC-DOC-02-01 non sono mai visibili allo studente. Vedi FR-VER-01.* |
| STU-03 | Consultare i propri voti | *…* | *…* |

<aside>
💡

Gli acceptance criteria della traccia sono il minimo. Puoi aggiungerne, non toglierne. Scrivi quelli nuovi nello stesso formato *Dato che / Quando / Allora*.

</aside>

### Le decisioni lasciate aperte dalla traccia

La traccia lascia alcune scelte a te. Ognuna diventa un requisito con il suo ID. Usa questo formato.

> **FR-[AREA]-[NN] · [Titolo]** (collegato a *ID della storia*)
*Cosa avete deciso, in modo verificabile.Motivazione:* *perché avete scelto così.*
> 

I punti che devi decidere almeno sono questi.

- [x]  La scala dei voti (DOC-03). Da quanto a quanto, con quale passo, se ammette segni come "+" e "−".
- [x]  Il trasferimento di uno studente fra classi (DIR-03). Si può fare? Cosa succede ai voti?
- [ ]  La modifica di una verifica dopo lo svolgimento (DOC-02).
- [ ]  La connessione che cade durante una verifica (STU-02).
- [x]  Il fallimento del servizio esterno (per esempio l'email delle credenziali).
- [ ]  *Altre decisioni che il team ha scoperto*

> **FR-VOT-01 · Calcolo del voto delle verifiche** (collegato a *DOC-02, DOC-03*)
Il voto di una verifica si calcola con la formula voto = 4 + 5 × (punti ottenuti ÷ punti totali), quindi va da 4 a 9. Il risultato si arrotonda al mezzo voto più vicino; a metà strada si arrotonda per eccesso (6,25 → 6,5; 6,75 → 7). Non sono previsti i segni + e −. Il calcolo parte solo quando tutte le risposte hanno un esito definitivo: quelle da correggere a mano (segnate in arancione) ricevono dal docente un punteggio fra 0 e il massimo della domanda. Il docente può poi cambiare a mano il voto finale, sempre fra 4 e 10 a passi di mezzo voto: è l'unico modo per assegnare 10. Nessun voto, calcolato o manuale, può essere sotto 4.
*Motivazione:* *partire da 4 evita voti umilianti per una verifica consegnata, e lasciare il 10 solo al docente lo riserva ai lavori davvero eccellenti.*
> 

> **FR-VER-01 · Correzione automatica delle domande aperte** (collegato a *DOC-02, STU-02, DOC-03*)
Per ogni domanda aperta il docente indica le parole chiave che la risposta deve contenere e, se vuole, i loro sinonimi. Alla consegna il sistema conta quante parole chiave (o sinonimi) sono presenti e propone un colore: rosso con 0 parole chiave; arancione da 1 fino alla metà inclusa, con la metà arrotondata per difetto; verde oltre la metà. Il colore è solo un aiuto per il docente: propone un punteggio (verde = massimo, rosso = 0, arancione = da assegnare), ma il docente decide il punteggio finale di ogni risposta e può cambiare anche verdi e rossi. Lo studente non vede colori, punteggi né voto finché il docente non conferma la correzione (FR-VOT-01).
*Motivazione:* *la correzione automatica velocizza il lavoro del docente ma non è affidabile: una risposta può contenere le parole chiave ed essere sbagliata, o non contenerle ed essere giusta. Per questo l'ultima parola è sempre del docente e lo studente vede solo il risultato confermato.*
> 

> **FR-ISC-01 · Mail istituzionale degli studenti con lo stesso nome** (collegato a *DIR-02*)
Quando accetta un modulo, il sistema controlla le mail istituzionali già esistenti e sceglie la prima libera in quest'ordine: 1) iniziale del nome + cognome; 2) iniziale del nome + prima lettera in cui il nome è diverso da quello dello studente omonimo + cognome; 3) nome intero + cognome; 4) iniziale del nome + cognome + un numero. Le mail degli studenti diplomati restano bloccate per 5 anni dal diploma e solo dopo possono essere assegnate di nuovo. Esempio: Mario Rossi è già m.rossi@mailistituzionale.it; Marco Rossi diventa mc.rossi@mailistituzionale.it (Marco e Mario si differenziano alla quarta lettera, c).
*Motivazione:* *la mail deve restare corta e riconoscibile, ma due studenti non possono mai avere lo stesso indirizzo di login. I 5 anni di blocco evitano che un nuovo studente riceva le mail destinate a un ex studente.*
> 

> **FR-ISC-02 · Password temporanea non cambiata** (collegato a *DIR-02*)
La password temporanea viene inviata alla mail del genitore. ScuolaChill non conserva mai le password in forma leggibile, nemmeno quelle temporanee: se serve, il Direttore genera una nuova password temporanea, che sostituisce la precedente e fa ripartire i 3 giorni. Se dopo 3 giorni dall'invio lo studente non l'ha cambiata, il sistema avvisa il Direttore, che contatta chi ha fatto la richiesta per telefono o per posta. Telefono e indirizzo postale sono campi obbligatori del modulo di iscrizione.
*Motivazione:* *è il piano di riserva se il servizio email fallisce o se il genitore ha scritto male la mail: nessuno studente resta senza accesso senza che la scuola se ne accorga. Non conservare le password in forma leggibile protegge gli account anche se qualcuno riuscisse a leggere i dati salvati.*
> 

> **FR-CLA-01 · Composizione delle classi** (collegato a *DIR-02, DIR-03*)
ScuolaChill propone le classi di ogni indirizzo a partire dagli studenti accettati. Una classe ha da 12 a 26 studenti (fino a 28 solo per i trasferimenti, vedi FR-CLA-02). Il sistema propone il minor numero di classi che non superano 26 studenti (numero di classi = iscritti ÷ 26, arrotondato per eccesso) e divide gli studenti in parti il più possibile uguali, con al massimo 1 studente di differenza. Se gli iscritti sono meno di 12, propone una classe mista (FR-CLA-03). La proposta diventa definitiva solo quando il Direttore la conferma, e il Direttore può modificarla prima di confermarla.
*Motivazione:* *con 20 docenti, meno classi più grandi sono più sostenibili di tante classi piccole. La scuola è piccola e il numero di iscritti per indirizzo cambia ogni anno: il sistema fa il calcolo, ma la scelta finale dipende da aule e docenti disponibili, che conosce solo il Direttore.*
> 

> **FR-CLA-02 · Trasferimento di uno studente fra classi** (collegato a *DIR-03, STU-03*)
Il Direttore può trasferire uno studente da una classe all'altra solo all'inizio del nuovo anno scolastico, mai durante l'anno. Se la classe di arrivo ha già 26 studenti, il Direttore può accettare al massimo 2 studenti in più, fino a 28; oltre, la classe va divisa. I voti appartengono allo studente, non alla classe: dopo il trasferimento restano tutti, invariati, nella sua pagina Voti. Da quel momento lo studente ha i docenti, l'orario, il materiale, i compiti e le verifiche della nuova classe.
*Motivazione:* *un voto non deve mai sparire: lo studente lo ha guadagnato a prescindere dalla classe in cui si trovava. Trasferire solo a inizio anno evita di dover gestire verifiche e compiti a metà fra due classi e due docenti.*
> 

> **FR-CLA-03 · Classi miste** (collegato a *DIR-03, DOC-01, DOC-02, DOC-03*)
Se un indirizzo ha meno di 12 iscritti in un anno, ScuolaChill propone di unirlo con un altro indirizzo dello stesso anno in una classe mista, che resta entro i 26 studenti. Il Direttore sceglie con quale indirizzo unirlo e conferma, come per FR-CLA-01. Nella classe mista le materie comuni (area umanistica e scientifica di base) si seguono insieme; le materie di indirizzo si seguono separate, ognuna solo con gli studenti del proprio indirizzo. Il docente di una materia di indirizzo vede, e può assegnare materiale, compiti, verifiche e voti, solo agli studenti del proprio indirizzo.
*Motivazione:* *una classe con pochissimi studenti non è sostenibile per una scuola con 20 docenti; unire le materie comuni mantiene la classe a una dimensione ragionevole senza rinunciare alle materie di indirizzo.*
> 

---

## Requisiti non funzionali

Ogni requisito ha una soglia, una condizione e un modo per verificarlo. Ed è collegato ad almeno una user story.

| ID | Famiglia | Requisito | Soglia e condizione | Come si verifica | Storie collegate |
| --- | --- | --- | --- | --- | --- |
| NFR-01 | Prestazioni | *es. Apertura della verifica nel picco* | *es. meno di 2 s per il 95% delle richieste, 75 utenti nello stesso minuto* | *Test di carico* | *STU-02* |
| NFR-02 | Sicurezza | *…* | *…* | *…* | *…* |
| NFR-03 | Usabilità | *…* | *…* | *…* | *…* |
| NFR-04 | Disponibilità | *…* | *…* | *…* | *…* |
| NFR-05 | Ambientale | *…* | *…* | *…* | *…* |
| NFR-06 | Supporto | *…* | *…* | *…* | *…* |
| NFR-07 | Interazione | *…* | *…* | *…* | *…* |
| NFR-08 | Conformità | *…* | *…* | *…* | *…* |

<aside>
💡

Le famiglie da coprire sono queste. **Prestazioni, disponibilità, scalabilità, sicurezza** e **conformità** vengono dalla lezione sui requisiti funzionali e non funzionali. **Usabilità, ambientali, supporto** e **interazione** vengono dalla lezione sul PRD. Se una famiglia resta vuota, scrivi perché non vi riguarda.

I requisiti trasversali della traccia (HTTPS, paginazione, OpenAPI, errori uniformi, Dev e Prod) sono già obbligatori. Riportali qui con il loro ID.

</aside>

### Requisiti impliciti

Prima di chiudere questa sezione, intervista per dieci minuti un ragazzo del primo anno. La domanda è una sola. *"Cosa daresti per scontato che un'app di questo tipo faccia sempre, o non faccia mai?"*

| Chi avete intervistato | Cosa ha detto | Requisito che ne avete ricavato |
| --- | --- | --- |
| *nome o iniziali* | *"Il voto non deve sparire, mai"* | *NFR-…* |
|  |  |  |

---

## Assunzioni, vincoli e dipendenze

### Assunzioni

Quello che date per vero senza poterlo garantire.

| ID | Assunzione | Cosa succede se è falsa |
| --- | --- | --- |
| ASS-01 | *es. La scuola ha 800 studenti e 60 docenti* | *Il dimensionamento va rifatto* |
|  |  |  |

### Vincoli

I limiti che non potete cambiare.

| ID | Vincolo | Da dove viene |
| --- | --- | --- |
| VIN-01 | *es. Il budget cloud è quello dei crediti studente* | *Traccia del progetto* |
|  |  |  |

### Dipendenze

Le cose esterne senza cui non potete andare avanti.

| ID | Dipendenza | Serve entro | Chi se ne occupa |
| --- | --- | --- | --- |
| DIP-01 | *es. Account attivo sul servizio email* | *Prima del collaudo* | *nome* |
|  |  |  |  |

---

# Seconda parte · Il come

<aside>
💡

Da qui in poi parli al tuo docente e al tuo team, non al Direttore. Ogni scelta tecnica va motivata e confrontata con almeno un'alternativa. "Lo conosciamo" è una motivazione valida, ma non può essere l'unica.

</aside>

## Stima del carico

### Utenti concorrenti

| Situazione | Utenti concorrenti | Da dove viene il numero |
| --- | --- | --- |
| Uso normale durante la giornata | *…* | *…* |
| Picco delle 9:00 (verifiche) | *…* | *…* |
| Fine quadrimestre (voti) | *…* | *…* |

### Profilo di carico

| Operazione | Frequente? | Pesante? | Critica? | Note |
| --- | --- | --- | --- | --- |
| Login | *…* | *…* | *…* | *…* |
| Apertura verifica | *…* | *…* | *…* | *…* |
| Consegna verifica | *…* | *…* | *…* | *…* |
| Dashboard del Direttore | *…* | *…* | *…* | *…* |
| Caricamento materiale | *…* | *…* | *…* | *…* |

<aside>
💡

I numeri di qui devono essere coerenti con la scuola che avete immaginato e con i requisiti non funzionali. Se dichiarate 800 studenti, non potete dimensionare per 20 utenti senza spiegare perché.

</aside>

---

## Scelte tecnologiche

| Area | Scelta | Alternativa considerata | Perché avete scelto così |
| --- | --- | --- | --- |
| Backend | *…* | *…* | *…* |
| Frontend | *…* | *…* | *…* |
| Database | *…* | *…* | *…* |
| Provider cloud | *…* | *…* | *…* |
| Servizi cloud | *…* | *…* | *…* |
| Regione | *…* | *…* | *…* |
| Servizio esterno | *…* | *…* | *…* |

---

## Architettura

### Diagramma dei componenti

*Inserisci qui il diagramma. Deve mostrare i componenti principali e come comunicano.*

### I livelli

| Livello | Cosa fa in ScuolaChill | Esempio concreto |
| --- | --- | --- |
| Presentation / API | *…* | *…* |
| Application / Business | *…* | *…* |
| Data access | *…* | *…* |

### Le dipendenze fra i livelli

*Chi può conoscere chi, e in quale direzione. Spiega come questa struttura riduce l'accoppiamento e rende il sistema testabile.*

---

## Le API

### Le risorse

*Elenca le risorse REST principali. Es. `/classi`, `/verifiche`, `/voti`.*

### Il contratto delle API principali

| Verbo | Route | Chi può chiamarla | Payload di esempio | Risposte previste |
| --- | --- | --- | --- | --- |
| `POST` | `*/api/docenti*` | *Direttore* | `*{ "nome": "…", "email": "…" }*` | *201, 400, 403, 409* |
| `GET` | *…* | *…* | *…* | *…* |
| `PUT` | *…* | *…* | *…* | *…* |
| `PATCH` | *…* | *…* | *…* | *…* |
| `DELETE` | *…* | *…* | *…* | *…* |

### Errori, validazione e paginazione

**Formato uniforme degli errori.** *Mostra un esempio di risposta di errore.*

**Validazione degli input.** *Dove avviene e con quali regole.*

**Paginazione.** *Come funziona. Parametri, dimensione di default, formato della risposta.*

**Documentazione e verifica.** *Come userete OpenAPI/Swagger e la collezione Postman.*

---

## Persistenza e modello dei dati

### Diagramma ER

*Inserisci qui il diagramma entità-relazioni con le cardinalità.*

### Identificatori

*Come vengono generati gli ID, e perché. Numeri incrementali, UUID, altro?*

### Tre modelli diversi

| Entità | Nel database | Nel dominio | Esposta dall'API | Dove differiscono e perché |
| --- | --- | --- | --- | --- |
| *es. Voto* | *…* | *…* | *…* | *…* |

### Normalizzazione e letture aggregate

*Come è normalizzato il modello. Dove serve una lettura denormalizzata, per esempio la pagina dei voti per materia o la dashboard del Direttore.*

### Accesso ai dati

*Strategia di accesso ai dati e uso delle query parametrizzate contro la SQL injection.*

---

## Sicurezza e integrazione

### Autenticazione e token

*Come si ottiene il token, cosa contiene, come viaggia il profilo utente.*

### Chi può fare cosa

| Operazione | Direttore | Docente | Studente |
| --- | --- | --- | --- |
| Creare un docente | ✅ | ❌ | ❌ |
| Caricare materiale | *…* | *…* | *…* |
| Vedere i voti di uno studente | *…* | *…* | *…* |
| *…* |  |  |  |

*Spiega dove viene fatto rispettare questo controllo. Ricorda che il frontend non basta mai.*

### L'API esterna

*Quale servizio usate, per cosa, e cosa succede quando non risponde.*

### Configurazione e segreti

*Dove vivono connection string e segreti, e come cambiano fra Development e Production.*

---

## Qualità architetturale

### Organizzazione del codice

*Struttura di progetti, moduli e cartelle, con le motivazioni.*

### Dependency inversion e IoC

*Dove li applicate e a cosa servono in ScuolaChill.*

### Testabilità

*Cosa testerete, e come separate database e API esterne per sostituirli nei test.*

### Development e Production

|  | Development | Production |
| --- | --- | --- |
| Database | *…* | *…* |
| Segreti | *…* | *…* |
| Log | *…* | *…* |
| *…* |  |  |

---

## Dimensionamento e costi

| Componente | Servizio | Taglia (CPU, RAM, storage) | Istanze | Costo mensile stimato |
| --- | --- | --- | --- | --- |
| Backend | *…* | *…* | *…* | *…* |
| Database | *…* | *…* | *…* | *…* |
| Storage dei file | *…* | *…* | *…* | *…* |
| *…* |  |  |  |  |
| **Totale** |  |  |  | ***…*** |

**Strategia di scalabilità.** *Verticale o orizzontale? Manuale o automatica?*

**Se la stima si rivela sbagliata.** *Cosa fate se gli utenti sono il doppio? E se sono la metà?*

---

## Piano di deployment

*Come ScuolaChill arriva sul cloud scelto. Come si passa da una versione alla successiva. Come vengono gestite nel tempo le modifiche allo schema del database.*

---

# Terza parte · Tempi e valutazione

## Milestone

| Milestone | Cosa è pronto | Data prevista | Responsabile |
| --- | --- | --- | --- |
| PRD validato | Questo documento | *…* | *tutto il team* |
| *Prima versione in cloud* | *…* | *…* | *…* |
| *Collaudo con il primo anno* | *…* | *…* | *…* |
| *…* |  |  |  |

<aside>
💡

Stima il tempo di ogni fase come se tutto andasse bene. Poi aggiungi un margine. Non va mai tutto bene.

</aside>

## Piano di valutazione

Come capirete che ScuolaChill funziona e come validerete che la vostra soluzione sta avendo un impatto positivo?

| Metrica | Obiettivo | Come la misurate | Quando |
| --- | --- | --- | --- |
| *es. Collaudatori che completano una verifica senza aiuto* | *90%* | *Osservazione durante il collaudo* | *Collaudo* |
| *es. Voti persi* | *0* | *Confronto fra voti inseriti e voti salvati* | *Primo mese* |
|  |  |  |  |

---

## Acceptance Criteria di questa PRD

- [ ]  Ogni parte rappresentata da questo template ha tutte le sezioni richieste senza saltare nessun punto
- [ ]  Avete deciso tutti i punti che la traccia e gli esempi lasciano aperti.
- [ ]  Ogni requisito non funzionale ha una soglia e una condizione.
- [ ]  Ogni NFR è collegato ad almeno una user story.
- [ ]  Avete inserito i requisiti impliciti emersi da interviste che avete fatto.
- [ ]  Assunzioni, vincoli e dipendenze sono separati e scritti.
- [ ]  I numeri della stima del carico sono coerenti con la scuola immaginata e con il dimensionamento.
- [ ]  Ogni scelta tecnica ha almeno un'alternativa scartata e una motivazione.
- [ ]  La prima parte non contiene scelte tecniche.
- [ ]  Lo storico delle versioni è aggiornato .