# The Mobile Application Security Verification Standard

Il MASVS può essere utilizzato per stabilire un livello di affidabilità nella sicurezza delle applicazioni mobili. I requisiti sono stati sviluppati tenendo conto dei seguenti obiettivi:

- Utilizzo come metrica - Per fornire uno standard di sicurezza rispetto al quale le applicazioni mobili esistenti possono essere confrontate da sviluppatori e proprietari di applicazioni;
- Utilizzo come guida - Per fornire una guida durante tutte le fasi di sviluppo e test delle applicazioni mobili;
- Utilizzo in fase d'acquisto: per fornire una base di riferimento per la verifica della sicurezza delle applicazioni mobili.

Il progetto MAS è tradizionalmente incentrato sulle applicazioni scaricabili e, pertanto, tutte le sue risorse fanno riferimento alle "applicazioni". Tuttavia, il progetto è applicabile anche ad altre aree del business, come le preloaded application e gli SDK. Per entrambe le categorie ci sono alcuni aspetti da considerare:

**Preloads:** Le preloaded app sono applicazioni che vengono installate sul dispositivo dell'utente al momento della creazione del dispositivo e possono avere privilegi elevati che rendono gli utenti vulnerabili alle exploitative business practices. Dato il gran numero di app precaricate sul dispositivo di un utente medio, è importante misurare il loro rischio in modo quantificabile.

There are hundreds of preloads that may ship on a device and as a result automation is critical, therefore a subset of MAS criteria that is automation friendly may be a good basis.

**SDKs:** Gli SDK svolgono un ruolo fondamentale per le app mobili, fornendo il codice di cui gli sviluppatori hanno bisogno per costruire in modo più veloce, intelligente e redditizio. Gli sviluppatori fanno grande affidamento su di essi: un'applicazione mobile media utilizza 30 SDK e il 90% del codice proviene da terze parti. Se da un lato questo uso diffuso offre vantaggi significativi agli sviluppatori, dall'altro diffonde problemi di sicurezza e protezione..

Gli SDK offrono una varietà di funzionalità e quindi non tutte le categorie MASVS si applicano a ogni singolo tipo di SDK. Di conseguenza, lo sviluppatore dell'SDK deve valutare quali categorie si applicano ai rispettivi SDK per garantire che un test possa valutarli in modo corretto.

## Mobile AppSec Model

Il MASVS definisce due livelli di verifica della sicurezza (MASVS-L1 e MASVS-L2) e una serie di requisiti di resilienza per il reverse engineering (MASVS-R). MASVS-L1 contiene requisiti di sicurezza generici che sono raccomandati per tutte le app mobili, mentre MASVS-L2 dovrebbe essere applicato alle app che gestiscono dati altamente sensibili. MASVS-R comprende controlli protettivi aggiuntivi che possono essere applicati se la prevenzione delle minacce lato client è un obiettivo di progettazione.

Soddisfacendo i requisiti di MASVS-L1 si ottiene un'app sicura che segue le best practice di sicurezza e non soffre di vulnerabilità comuni. MASVS-L2 aggiunge ulteriori controlli di difesa in profondità, come l'SSL pinning, dando vita a un'app resistente ad attacchi più sofisticati, a condizione che i controlli di sicurezza del sistema operativo mobile siano intatti e che l'utente finale non sia visto come un potenziale avversario. Soddisfare tutti o sottoinsiemi dei requisiti di protezione del software in MASVS-R aiuta a prevenire minacce specifiche sul lato client quando l'utente finale è malintenzionato e/o il sistema operativo mobile è compromesso.

**I: Sebbene si raccomandi l'implementazione dei controlli MASVS-L1 in ogni applicazione, l'implementazione o meno di un controllo dovrebbe essere una decisione basata sul rischio, presa/comunicata con i proprietari dell'azienda.**

**II: Si noti che i controlli di protezione del software elencati in MASVS-R e descritti nella OWASP Mobile Application Security Testing Guide possono essere aggirati e non devono mai essere utilizzati in sostituzione dei controlli di sicurezza. Sono invece intesi ad aggiungere ulteriori controlli di protezione specifici per le minacce alle applicazioni che soddisfano anche i requisiti MASVS in MASVS-L1 o MASVS-L2.**

![Verification Levels](images/masvs-levels-new.jpg)

### Struttura del documento

La prima parte del MASVS contiene una descrizione del modello di sicurezza e dei livelli di verifica disponibili, seguita da raccomandazioni su come utilizzare lo standard nella pratica. I requisiti di sicurezza dettagliati, insieme alla mappatura dei livelli di verifica, sono elencati nella seconda parte. I requisiti sono stati raggruppati in otto categorie (da V1 a V8) in base all'obiettivo tecnico/scopo. Nel MASVS e nel MASTG viene utilizzata la seguente nomenclatura:

- *Categoria di requisiti:* MASVS-Vx, ad esempio MASVS-V2: Archiviazione dei dati e privacy
- *Requisito:* MASVS-Vx.y, ad esempio MASVS-V2.2: "Nessun dato sensibile viene scritto nei log delle applicazioni".

### I livelli di verifica in dettaglio

#### MASVS-L1: Sicurezza standard

Un'applicazione mobile che ottiene MASVS-L1 aderisce alle migliori pratiche di sicurezza delle applicazioni mobili. Soddisfa i requisiti di base in termini di qualità del codice, gestione dei dati sensibili e interazione con l'ambiente mobile. Per verificare i controlli di sicurezza deve essere previsto un processo di verifica. Questo livello è appropriato per tutte le applicazioni mobili.

#### MASVS-L2: Difesa-in-profondità

MASVS-L2 introduces advanced security controls that go beyond the standard requirements. To fulfill MASVS-L2, a threat model must exist, and security must be an integral part of the app's architecture and design. Based on the threat model, the right MASVS-L2 controls should have been selected and implemented successfully. This level is appropriate for apps that handle highly sensitive data, such as mobile banking apps.

#### MASVS-R: Resiliency Against Reverse Engineering and Tampering

MASVS-L2 introduce controlli di sicurezza avanzati che vanno oltre i requisiti standard. Per soddisfare MASVS-L2, deve esistere un threat model e la sicurezza deve essere parte integrante dell'architettura e del design dell'applicazione. In base al threat model, devono essere stati selezionati e implementati con successo i controlli MASVS-L2 adeguati. Questo livello è appropriato per le applicazioni che gestiscono dati altamente sensibili, come le applicazioni di mobile banking.

### Utilizzo consigliato

Le applicazioni possono essere verificate rispetto al MASVS L1 o L2, in base alla valutazione del rischio precedente e al livello di sicurezza complessivo richiesto. L1 è applicabile a tutte le app mobili, mentre L2 è generalmente consigliato per le app che gestiscono dati e/o funzionalità più sensibili. MASVS-R (o parti di esso) può essere applicato per verificare la resilienza contro minacce specifiche, come il repackaging o l'estrazione di dati sensibili, *in aggiunta* a una corretta verifica della sicurezza.

In sintesi, sono disponibili i seguenti tipi di verifica:

- MASVS-L1
- MASVS-L1+R
- MASVS-L2
- MASVS-L2+R

Le diverse combinazioni riflettono diversi gradi di sicurezza e resilienza. L'obiettivo è consentire una certa flessibilità: Ad esempio, un gioco mobile potrebbe non giustificare l'aggiunta di controlli di sicurezza MASVS-L2, come l'autenticazione a due fattori, per motivi di usabilità, ma avere una forte esigenza aziendale di prevenzione al tampering.

#### Quale tipo di verifica scegliere

L'implementazione dei requisiti del MASVS L2 aumenta la sicurezza, ma allo stesso tempo aumenta il costo dello sviluppo e potenzialmente peggiora l'esperienza dell'utente finale (il classico trade-off). In generale, l'L2 dovrebbe essere utilizzato per le applicazioni ogni volta che ha senso dal punto di vista del rischio e del costo (cioè, quando la perdita potenziale causata da una compromissione della riservatezza o dell'integrità è superiore al costo sostenuto dai controlli di sicurezza aggiuntivi). La valutazione del rischio dovrebbe essere il primo passo da compiere prima di applicare il MASVS.

##### Esempi

###### MASVS-L1

- Tutte le applicazioni mobili. MASVS-L1 elenca le migliori pratiche di sicurezza che possono essere seguite con un impatto ragionevole sui costi di sviluppo e sull'esperienza dell'utente. Applicare i requisiti del MASVS-L1 per tutte le app che non si qualificano per uno dei livelli superiori.

###### MASVS-L2

- Settore sanitario: Applicazioni mobili che memorizzano informazioni di identificazione personale che possono essere utilizzate per furti di identità, pagamenti fraudolenti o una serie di truffe. Per il settore sanitario statunitense, le considerazioni sulla conformità includono le norme sulla privacy, sulla sicurezza, sulla notifica delle violazioni e sulla sicurezza dei pazienti previste dall'Health Insurance Portability and Accountability Act (HIPAA).

- Settore finanziario: Applicazioni che consentono l'accesso a informazioni altamente sensibili come numeri di carte di credito, informazioni personali o che permettono all'utente di spostare fondi. Queste applicazioni richiedono ulteriori controlli di sicurezza per prevenire le frodi. Le app finanziarie devono garantire la conformità allo standard di sicurezza dei dati dell'industria delle carte di pagamento (PCI DSS), al Gramm Leech Bliley Act e al Sarbanes-Oxley Act (SOX).

###### MASVS L1+R

- Applicazioni mobili in cui la protezione della proprietà intellettuale (IP) è un obiettivo aziendale. I controlli di resilienza elencati nel MASVS-R possono essere utilizzati per aumentare lo sforzo necessario per ottenere il codice sorgente originale e per impedire la manomissione o il cracking.

- Industria del gioco: Giochi in cui è essenziale prevenire il modding e il cheating, come i giochi online competitivi. Il cheating è un problema importante nei giochi online, in quanto una grande quantità di cheater porta a una base di giocatori scontenti e può, in ultima analisi, causare il fallimento di un gioco. MASVS-R fornisce controlli anti-tampering di base per contribuire ad aumentare le difficoltà per i cheater.

###### MASVS L2+R

- Settore finanziario: Applicazioni bancarie online che consentono all'utente di spostare fondi, dove tecniche come l'iniezione di codice su dispositivi compromessi rappresentano un rischio. In questo caso, i controlli di MASVS-R possono essere utilizzati per impedire la manomissione, alzando il livello di guardia contro per gli autori di malware.

- Tutte le app mobili che, per progettazione, devono memorizzare dati sensibili sul dispositivo mobile, e allo stesso tempo devono supportare un'ampia gamma di dispositivi e versioni del sistema operativo. In questo caso, i controlli di resilienza possono essere utilizzati come misura di difesa in profondità per aumentare lo sforzo degli aggressori che mirano a estrarre i dati sensibili.

- Le applicazioni con acquisti in-app dovrebbero idealmente utilizzare controlli lato server e MASVS-L2 per proteggere i contenuti a pagamento. Tuttavia, ci possono essere casi in cui non è possibile utilizzare la protezione lato server. In questi casi, i controlli MASVS-R dovrebbero essere applicati in aggiunta per aumentare lo sforzo di reversing e/o tampering.
