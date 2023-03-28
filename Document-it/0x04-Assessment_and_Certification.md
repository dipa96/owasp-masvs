# Valutazione e certificazione

## La politica di OWASP sulle certificazioni MASVS e sui Trust Marks

OWASP, in quanto organizzazione no-profit neutrale rispetto ai fornitori, non certifica alcun fornitore, verificatore o software.

Tutte le asserzioni di garanzia, i marchi di fiducia o le certificazioni non sono ufficialmente verificati, registrati o certificati da OWASP, pertanto un'organizzazione che si affida a tale visione deve essere cauta nel riporre fiducia in qualsiasi terza parte o marchio di fiducia che rivendichi la certificazione (M)ASVS.

Ciò non dovrebbe impedire alle organizzazioni di offrire tali servizi di garanzia, purché non rivendichino una certificazione ufficiale OWASP.

## Guida alla certificazione delle applicazioni mobili

Il metodo consigliato per verificare la conformità di un'applicazione mobile con il MASVS è quello di eseguire una verifica "a libro aperto", vale a dire che ai tester viene concesso l'accesso a risorse chiave come progettisti e sviluppatori dell'applicazione, documentazione del progetto, codice sorgente e accesso autenticato agli endpoint, compreso l'accesso ad almeno un account utente per ogni ruolo.

È importante notare che il MASVS copre solo la sicurezza dell'applicazione mobile (lato client) e la comunicazione di rete tra l'applicazione e i suoi endpoint remoti, oltre ad alcuni requisiti di base e generici relativi all'autenticazione dell'utente e alla gestione della sessione. Non contiene requisiti specifici per i servizi remoti (ad esempio, servizi web) associati all'applicazione, se non un insieme limitato di requisiti generici relativi all'autorizzazione, all'autenticazione, alla verifica del controllo e alla gestione della sessione. Tuttavia, il MASVS V1 specifica che i servizi remoti devono essere coperti dal modello generale delle minacce e verificati in base a standard appropriati, come l'OWASP ASVS.

L'organismo di certificazione deve includere in qualsiasi rapporto l'ambito della verifica (in particolare se un componente chiave è fuori dall'ambito), un riepilogo dei risultati della verifica, compresi i test superati e quelli falliti, con chiare indicazioni su come risolvere i test falliti. La raccolta di documenti di lavoro dettagliati, schermate o filmati, script per sfruttare in modo affidabile e ripetuto un problema e registrazioni elettroniche dei test, come i log dei proxy e le note associate, ad esempio un elenco di operazioni di pulizia, è considerata una prassi standard del settore. Non è sufficiente eseguire uno dei tool e riportare i fallimenti; questo non fornisce una prova sufficiente che tutti i problemi a livello di verifica siano stati testati e verificati in modo approfondito. In caso di controversia, devono essere disponibili prove sufficienti a dimostrare che ogni requisito verificato è stato effettivamente testato.

### Utilizzo della Guida ai test di sicurezza delle applicazioni mobili (MASTG) di OWASP

L'OWASP MASTG è un manuale per testare la sicurezza delle applicazioni mobili. Descrive i processi tecnici per la verifica dei requisiti elencati nel MASVS. Il MASTG comprende un elenco di casi d'uso, ognuno dei quali corrisponde a un requisito del MASVS. Mentre i requisiti del MASVS sono di alto livello e generici, il MASTG fornisce raccomandazioni approfondite e procedure di test su base mobile.

### The Role of Automated Security Testing Tools

The use of source code scanners and black-box testing tools is encouraged in order to increase efficiency whenever possible. It is however not possible to complete MASVS verification using automated tools alone: Every mobile app is different, and understanding the overall architecture, business logic, and technical pitfalls of the specific technologies and frameworks being used, is a mandatory requirement to verify security of the app.

## Altri utilizzi

### As Detailed Security Architecture Guidance

Uno degli usi più comuni del Mobile Application Security Verification Standard è quello di risorsa per gli architetti della sicurezza. I due principali framework di architettura di sicurezza, SABSA o TOGAF, mancano di molte informazioni necessarie per completare le revisioni dell'architettura di sicurezza delle applicazioni mobili. Il MASVS può essere utilizzato per colmare queste lacune, consentendo agli architetti della sicurezza di scegliere controlli migliori per i problemi comuni alle applicazioni mobili.

### Come sostituto delle liste di controllo per la codifica sicura disponibili in commercio

Molte organizzazioni possono trarre vantaggio dall'adozione del MASVS, scegliendo uno dei due livelli, oppure facendo un fork del MASVS e modificando i requisiti per il livello di rischio di ciascuna applicazione in modo specifico per il dominio. Incoraggiamo questo tipo di forking, a patto che venga mantenuta la tracciabilità, in modo che se un'applicazione ha superato il requisito 4.1, ciò significhi la stessa cosa per le copie forked, man mano che lo standard si evolve.

### Come base per le metodologie di test della sicurezza

Una buona metodologia di verifica di sicurezza delle applicazioni mobili deve coprire tutti i requisiti elencati nel MASVS. La Mobile Application Security Testing Guide (MASTG) di OWASP descrive i casi di test black-box e white-box per ogni requisito di verifica.

### As a Guide for Automated Unit and Integration Tests

The MASVS is designed to be highly testable, with the sole exception of architectural requirements. Automated unit, integration and acceptance testing based on the MASVS requirements can be integrated in the continuous development lifecycle. This not only increases developer security awareness, but also improves the overall quality of the resulting apps, and reduces the amount of findings during security testing in the pre-release phase.

### Per la formazione sullo sviluppo sicuro

Il MASVS può essere utilizzato anche per definire le caratteristiche delle applicazioni mobili sicure. Molti corsi di "codifica sicura" sono semplicemente corsi di hacking etico con una leggera spalmatura di consigli di progettazione. Questo non aiuta gli sviluppatori. I corsi di sviluppo sicuro possono invece utilizzare il MASVS, con una forte attenzione ai controlli proattivi documentati nel MASVS, piuttosto che, ad esempio, ai 10 principali problemi di sicurezza del codice.
