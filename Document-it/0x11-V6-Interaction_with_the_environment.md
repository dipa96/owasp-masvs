# V6: Requisiti di Interazione con la Piattaforma

## Obiettivo della Sezione

I controlli di questo gruppo garantiscono che l'applicazione utilizzi le API della piattaforma e i componenti standard in modo sicuro. Inoltre, i controlli comprendono anche le comunicazioni tra le applicazioni (IPC).

## Requisiti per la Verifica di Sicurezza

| # | MSTG-ID | Description | L1 | L2 |
| -- | ---------- | ---------------------- | - | - |
| **6.1** | MSTG-PLATFORM-1 | L'applicazione richiede solo il set minimo di autorizzazioni necessarie. | x | x |
| **6.2** | MSTG-PLATFORM-2 | Tutti gli input provenienti da fonti esterne e dall'utente vengono convalidati e, se necessario, sanitizzati. Ciò include i dati ricevuti tramite l'interfaccia utente, i meccanismi IPC come gli intent, gli URL personalizzati e le risorse di rete. | x | x |
| **6.3** | MSTG-PLATFORM-3 | L'applicazione non esporta funzionalità sensibili tramite schemi di URL personalizzati, a meno che questi meccanismi non siano adeguatamente protetti. | x | x |
| **6.4** | MSTG-PLATFORM-4 | L'applicazione non esporta funzionalità sensibili attraverso strutture IPC, a meno che questi meccanismi non siano adeguatamente protetti. | x | x |
| **6.5** | MSTG-PLATFORM-5 | JavaScript è disabilitato nelle WebView, a meno che non sia esplicitamente richiesto. | x | x |
| **6.6** | MSTG-PLATFORM-6 | Le WebView sono configurate in modo da consentire solo il set minimo di handler di protocollo richiesti (idealmente, è supportato solo https). Gli handler potenzialmente pericolosi, come file, tel e app-id, sono disabilitati. | x | x |
| **6.7** | MSTG-PLATFORM-7 | Se i metodi nativi dell'applicazione sono esposti a una WebView, verificare che la WebView esegua solo il rendering di JavaScript contenuto nel pacchetto dell'applicazione. | x | x |
| **6.8** | MSTG-PLATFORM-8 | La deserializzazione degli oggetti, se presente, è implementata utilizzando API di serializzazione sicure. | x | x |
| **6.9** | MSTG-PLATFORM-9 | L'applicazione si protegge dagli attacchi di overlay dello schermo. (Solo Android) |  | x |
| **6.10** | MSTG-PLATFORM-10 | La cache, la memoria e le risorse utilizzate (JavaScript, ecc.) di una WebView devono essere cancellate prima che la WebView venga distrutta. |  | x |
| **6.11** | MSTG-PLATFORM-11 | Verificare che l'applicazione impedisca l'uso di tastiere personalizzate di terze parti ogni volta che vengono immessi dati sensibili (solo iOS). | | x |

## Riferimenti

La OWASP Mobile Application Security Testing Guide fornisce istruzioni dettagliate per la verifica dei requisiti elencati in questa sezione.

- Android: Testing Platform Interaction - <https://github.com/OWASP/owasp-mastg/blob/master/Document/0x05h-Testing-Platform-Interaction.md>
- iOS: Testing Platform Interaction - <https://github.com/OWASP/owasp-mastg/blob/master/Document/0x06h-Testing-Platform-Interaction.md>

Per ulteriori informazioni, vedere anche:

- OWASP Mobile Top 10: M1 (Improper Platform Usage) - <https://owasp.org/www-project-mobile-top-10/2016-risks/m1-improper-platform-usage>
- OWASP Mobile Top 10: M7 (Poor Code Quality) - <https://owasp.org/www-project-mobile-top-10/2016-risks/m7-client-code-quality>
- CWE 20 (Improper Input Validation) - <https://cwe.mitre.org/data/definitions/20.html>
- CWE 79 (Improper Neutralization of Input During Web Page Generation) - <https://cwe.mitre.org/data/definitions/79.html>
- CWE 200 (Information Leak / Disclosure) - <https://cwe.mitre.org/data/definitions/200.html>
- CWE 250 (Execution with Unnecessary Privileges) - <https://cwe.mitre.org/data/definitions/250.html>
- CWE 672 (Operation on a Resource after Expiration or Release) - <https://cwe.mitre.org/data/definitions/672.html>
- CWE 749 (Exposed Dangerous Method or Function) - <https://cwe.mitre.org/data/definitions/749.html>
- CWE 772 (Missing Release of Resource after Effective Lifetime) - <https://cwe.mitre.org/data/definitions/772.html>
- CWE 920 (Improper Restriction of Power Consumption) - <https://cwe.mitre.org/data/definitions/920.html>
- CWE 925 (Improper Verification of Intent by Broadcast Receiver) - <https://cwe.mitre.org/data/definitions/925.html>
- CWE 926 (Improper Export of Android Application Components) - <https://cwe.mitre.org/data/definitions/926.html>
- CWE 927 (Use of Implicit Intent for Sensitive Communication) - <https://cwe.mitre.org/data/definitions/927.html>
- CWE 939 (Improper Authorization in Handler for Custom URL Scheme) - <https://cwe.mitre.org/data/definitions/939.html>
