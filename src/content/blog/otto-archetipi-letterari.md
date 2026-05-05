---
title: "Il profilo letterario: archetipi, DNA stilistico e Goodreads"
description: "Chi sei, quando scrivi? I profili stilistici che Chief Editor usa per calibrare le sue analisi."
pubDate: 2026-05-03
tags: ["profilo Chief Editor", "archetipi", "voce letteraria"]
series: "Come funziona Chief Editor"
seriesOrder: 4
pinned: false
---
## Introduzione al profilo e gli archetipi

Alla radice del rapporto tra editor e scrittore ci sono la conoscenza reciproca e la fiducia. Per questo per usare al meglio Chief Editor è utile compilare il proprio profilo.

Il profilo letterario è la funzione che trasforma Chief Editor da strumento generico a editor personale.

Senza profilo, la critica è buona: analizza le cinque dimensioni, identifica punti di forza e aree da sviluppare, suggerisce un esercizio. Ma è generica — potrebbe essere scritta per chiunque.

Con il profilo, il Chief Editor conosce chi sei come scrittore: da quale tradizione vieni, a quali voci ti confronti, quale archetipo stilistico stai costruendo. La critica diventa calibrata. I riferimenti letterari diventano pertinenti. L'esercizio diventa specifico.

Gli otto archetipi di Chief Editor non sono categorie rigide né test della personalità. Sono strumenti di lettura — modi per nominare qualcosa che è sempre difficile da vedere in sé stessi.

Il Profilo stilistico dell'utente è diviso nelle sezioni: Dna Stilistico, Correnti filosofiche, Tendenze inconsce, Linguaggio letterario, Zone d'ombra, Percorso di crescita. Di seguito uno screenshot e lo stralcio di alcune sezioni di un profilo di esempio. 

![Screenshot Profilo](/profilo.png)

<div align="center"><em>screenshot del profilo avanzato: lo scrutatore dell'anima</em></div>
<br />

>**DNA Stilistico:** Il tuo DNA stilistico è costruito su tensioni irrisolte e produttive. Ami la prosa che porta i segni del corpo — la fatica, il dolore, il desiderio — ma che non si abbandona mai al sentimentalismo. Sei attratto dalla scrittura che lavora per sottrazione (Parise, Hemingway) quanto da quella che lavora per accumulo e pressione ritmica (Céline, Faulkner). La frase breve e definitiva ti convince quanto il periodo lungo e avvolgente, purché entrambi abbiano quella qualità di inevitabilità, di non poter essere scritti altrimenti. Cerchi stili che abbiano un rapporto fisico con il mondo: la prosa come corpo che si muove nello spazio;

>**Linguaggio Letterario** Appartieni a una tradizione che potremmo chiamare del realismo visionario: scrittori che partono dal dato concreto e reale per arrivare a qualcosa che lo trascende senza abbandonarlo. La tua genealogia letteraria va da Dostoevskij attraverso il modernismo americano (Faulkner, Hemingway), si innesta nel grande romanzo europeo del Novecento (Céline, Conrad) e trova radici italiane specifiche in quella letteratura del Sud e del margine (Ortese, Parise, Sapienza) che è tra le più originali del secondo Novecento. Sei erede di una scrittura che non separa etica ed estetica: la forma è già una posizione morale.

>**Zone d'ombra** Il tuo profilo rivela alcune zone d'ombra significative. Sei probabilmente poco attratto dalla letteratura sperimentale pura, da quella che mette la forma davanti all'umano — rischi di perdere Beckett nella sua dimensione più radicale, o Perec, o il nouveau roman. Hai una tendenza a privilegiare la prosa rispetto alla poesia, e questo potrebbe impedirti di vedere quanto certi tuoi autori preferiti siano fondamentalmente poeti travestiti da narratori. C'è poca letteratura non occidentale nel tuo pantheon: rischi di avere un punto cieco su tradizioni che lavorano sugli stessi temi con strumenti completamente diversi. E hai probabilmente una resistenza verso la letteratura apertamente politica o satirica.

>**Percorso di crescita** 1. Esplorare la letteratura latinoamericana non nel filone magico-realistico mainstream ma in quello più oscuro e visionario: Juan Rulfo, Felisberto Hernández, Onetti — che condividono il tuo DNA ma aprono geografie interiori diverse. 2. Avvicinarsi alla grande poesia novecentesca come estensione naturale della tua prosa preferita: Celan, Montale, Brodsky lavorano sugli stessi abissi con strumenti che potrebbero rivelarti nuove dimensioni nei tuoi autori amati. 3. Aprire un dialogo con la letteratura dell'Europa dell'Est — Schulz, Hrabal, Bernhard — che condivide la tua tensione tra tragicommedia e oscurità esistenziale ma la porta in territori stilisticamente inesplorati per il tuo profilo attuale.

## Biodiversità stilistica: come ottenerla

Gli autori e i titoli indicati nel profilo sono la base per costruire un [grafo](https://it.wikipedia.org/wiki/Grafo) che permette alla AI di espandere l'orizzonte di riferimento per le analisi stilistiche. 

La Ai se no opportunamente istruita tende ad essere iterativa, a fare riferimento sempre agli stessi autori indicati e alle stesse indicazioni critiche. Per questo ho inventato il concetto di biodiversità stilistica da imporre alla AI nei propri ragionamenti. 

Chief editor sfrutta un semplice algoritmo impostato anche per garantire una __biodiversità__ dell'approccio critico secondo questo schema.

Rotazione critica giornaliera (biodiversità)
daySeed = giorno del mese % 4 — ogni giorno il Chief Editor riceve una prospettiva diversa su come scegliere i riferimenti:

Giorno pari 0: tradizioni e lingue lontane dal profilo
Giorno pari 1: autori contemporanei non canonici, voci non occidentali
Giorno pari 2: registro opposto allo stile (se sei lirico → autori asciutti)
Giorno pari 3: voci marginali, dimenticati, inaspettati

2 — Grafo degli autori adiacenti (nel profilo)
Quando si rigenera il profilo, include ora un campo 'autori vicini' con tre cluster:

- *Affini non ovvi* — stessa sensibilità, meno ovvi (pillole viola)
- *Per contrasto produttivo* — stilisticamente distanti ma illuminanti (pillole blu)
- *Da scoprire* — probabilmente sconosciuti, ma pertinenti al DNA (pillole verdi)

Il grafo è visibile nel profilo come sezione con pill colorate. Nelle analisi successive, il Chief Editor usa questo grafo come serbatoio di riferimenti invece degli autori dichiarati.

3 — Autori dichiarati esclusi dai riferimenti finali

Istruzione esplicita al modello: "Nei references usa autori dal grafo espanso — mai gli autori dichiarati." Gli autori del profilo restano come contesto per capire il DNA stilistico, non come termine di confronto.

4 — Score calibration rigorosa

Tabella di calibrazione nel prompt: 1-4 = problemi strutturali seri, 5-6 = potenziale non espresso, 7-8 = buona qualità, 9-10 = eccellenza rara. Istruzione esplicita: "Non assegnare score alti per incoraggiare."

5 — Critica diretta nella nota critica di Chief Editor

Chief Editor ha un obbligo esplicito: inserire "almeno una frase che identifichi il problema principale senza attenuarlo — non concludere con incoraggiamento generico."

![screenshot grafo](/grafo.png)
<div align="center"><em>screenshot grafo del profilo avanzato</em></div>

## Come costruire il profilo

Nella sezione PROFILO inserisci:

- **Fino a 3 generi letterari** tra dieci opzioni disponibili: narrativa contemporanea, romanzo storico, poesia, saggistica, noir/thriller, fantascienza/fantasy, memoir, letteratura di viaggio, drammaturgia, racconto breve
- **Fino a 10 autori preferiti** (campo libero — qualsiasi letteratura, qualsiasi epoca, qualsiasi lingua)
- **Fino a 5 titoli preferiti** (campo libero)

Non devi riempire tutto. Anche solo tre autori producono un profilo significativo. Quello che conta è che la lista sia onesta — non gli autori che pensi si dovrebbe citare, ma quelli che ami davvero, quelli che hai riletto, quelli che senti come parenti.

## Cosa produce l'AI

A partire da questi input, l'AI genera:

**Archetipo letterario** — uno degli otto archetipi disponibili che meglio rappresenta la tua voce di scrittore. Non è un'etichetta rigida: è un punto di partenza per la conversazione con il Chief Editor.

**Descrizione dell'archetipo** — tre o quattro frasi che spiegano le caratteristiche dello scrittore con quel profilo: la sua postura verso il materiale, il suo rapporto con il linguaggio, i rischi specifici della sua voce.

**DNA stilistico** — analisi del tuo approccio alla scrittura basata sui riferimenti: quali qualità stilistiche emergono dalla costellazione di autori che hai scelto.

**Correnti filosofiche** — le tradizioni di pensiero che emergono dai tuoi autori. Non necessariamente esplicite nelle loro opere, ma presenti come substrato.

**Percorso di crescita** — tre indicazioni concrete per sviluppare la tua voce, basate sull'archetipo identificato e sui suoi punti ciechi specifici.

## Gli otto archetipi

**Lo Scrutatore dell'Anima** — scrive per capire, non per raccontare. Il suo  materiale è l'interiorità. Genealogia: Dostoevskij, Woolf, Bernhard, Ferrante, ecc..

**Il Cronista Visionario** — ha uno sguardo sul mondo che non lascia le cose come le trova. Osserva e documenta, ma il suo documento è trasfigurato da un punto di vista preciso. Genealogia: Kapuściński, Didion, Carrère, Aleksievič.

**Il Narratore Epico** — pensiain grande. Architetture narrative ampie, personaggi che portano il peso di forze più grandi di loro. Genealogia: Tolstoj, García Márquez, Hilary Mantel, McCarthy.

**Il Poeta del Quotidiano** — trova il sacro nell'ordinario. Il dramma è già lì, nella superficie delle cose. Genealogia: Chekhov, Carver, Munro, Natalia Ginzburg.

**Il Filosofo Nascosto** — le sue storie pensano. I personaggi portano idee nel corpo, le trame esplorano domande senza risposta. Genealogia: Camus, Musil, Yourcenar, Saramago.

**Il Testimone Empatico** — scrive dall'interno delle vite degli altri. La sua scrittura è un atto di restituzione. Genealogia: Toni Morrison, Chimamanda Ngozi Adichie, Gurnah, Goliarda Sapienza.

**Il Visionario Simbolico** — il suo mondo ha un doppio fondo. Costruisce mitologie personali, sistemi simbolici propri. Genealogia: Borges, Calvino, Angela Carter, Kafka.

**Il Costruttore di Mondi** — costruisce universi. Non necessariamente fantastici: anche un quartiere, una famiglia, un'azienda può essere un mondo costruito mattone per mattone. Genealogia: Elsa Morante, Donna Tartt, David Mitchell, Vasily Grossman.

## Integrazione Goodreads

Se usi Goodreads, puoi importare le tue letture per arricchire il profilo automaticamente.

Il processo è semplice:

1. Su Goodreads: **My Books → Export** (in basso a destra nella pagina) → scarica il file CSV
2. In Chief Editor: **Profilo → sezione Goodreads** → incolla il contenuto del file
3. Clicca **Analizza libreria**

L'AI identifica i generi dominanti, gli autori più letti, e produce un'analisi del tuo DNA di lettura. Questo si aggiunge — non sostituisce — il profilo manuale.

## Il profilo non è un destino

L'archetipo si aggiorna. Se cambiano i tuoi autori di riferimento, se le letture dell'utente lo portano altrove, se la sua  scrittura si sposta — il profilo si può rigenerare. Non è un'etichetta permanente: è una mappa che si ridisegna mentre cammini.

Rigenerare il profilo ogni tre o sei mesi. Confrontare gli archetipi: vedere come cambia (o come non cambia) dice qualcosa sulla traiettoria come scrittore.
