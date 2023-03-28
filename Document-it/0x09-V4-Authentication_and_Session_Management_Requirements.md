# V4: Requisiti di autenticazione e gestione delle sessioni

## Obiettivo della Sezione

Nella maggior parte dei casi, l'accesso degli utenti a un servizio remoto è parte integrante dell'architettura complessiva dell'applicazione mobile. Anche se la maggior parte della logica avviene nell'endpoint, MASVS definisce alcuni requisiti di base per la gestione degli account utente e delle sessioni.

## Requisiti per la Verifica di Sicurezza

| # | MSTG-ID | Description | L1 | L2 |
| -- | ---------- | ---------------------- | - | - |
| **4.1** | MSTG-AUTH-1 | Se l'applicazione fornisce agli utenti l'accesso a un servizio remoto, viene eseguita una forma di autenticazione, come l'autenticazione con nome utente/password, presso l'endpoint remoto. | x | x |
| **4.2** | MSTG-AUTH-2 | Se si utilizza la gestione delle sessioni stateful, l'endpoint remoto utilizza identificatori di sessione generati casualmente per autenticare le richieste del client senza inviare le credenziali dell'utente. | x | x |
| **4.3** | MSTG-AUTH-3 | Se si utilizza un'autenticazione stateless basata su token, il server fornisce un token firmato con un algoritmo sicuro. | x | x |
| **4.4** | MSTG-AUTH-4 | L'endpoint remoto termina la sessione esistente quando l'utente si disconnette. | x | x |
| **4.5** | MSTG-AUTH-5 | Un criterio di password esiste e viene applicato all'endpoint remoto. | x | x |
| **4.6** | MSTG-AUTH-6 | L'endpoint remoto implementa un meccanismo di protezione contro l'invio di credenziali dopo un numero eccessivo di volte. | x | x |
| **4.7** | MSTG-AUTH-7 | Le sessioni vengono invalidate dall'endpoint remoto dopo un periodo predefinito di inattività e i token di accesso scadono. | x | x |
| **4.8** | MSTG-AUTH-8 | L'autenticazione biometrica, se presente, non è vincolata agli eventi (cioè utilizza un'API che restituisce semplicemente "vero" o "falso"). Si basa invece sullo sblocco di keychain/keystore. | | x |
| **4.9** | MSTG-AUTH-9 | L'endpoint remoto dispone di un secondo fattore di autenticazione e il requisito 2FA viene applicato in modo coerente.  | | x |
| **4.10** | MSTG-AUTH-10 | Per le transazioni critiche è necessaria un'autenticazione supplementare (step-up). | | x |
| **4.11** | MSTG-AUTH-11 | L'applicazione informa l'utente di tutte le attività sensibili con il suo account. Gli utenti possono visualizzare un elenco di dispositivi, visualizzare informazioni contestuali (indirizzo IP, posizione, ecc.) e bloccare dispositivi specifici. | | x |
| **4.12** | MSTG-AUTH-12 | I modelli di autorizzazione devono essere definiti e applicati all'endpoint remoto. | x | x |

## Riferimenti

La OWASP Mobile Application Security Testing Guide fornisce istruzioni dettagliate per la verifica dei requisiti elencati in questa sezione.

- General: Authentication and Session Management - <https://github.com/OWASP/owasp-mastg/blob/master/Document/0x04e-Testing-Authentication-and-Session-Management.md>
- Android: Testing Local Authentication - <https://github.com/OWASP/owasp-mastg/blob/master/Document/0x05f-Testing-Local-Authentication.md>
- iOS: Testing Local Authentication - <https://github.com/OWASP/owasp-mastg/blob/master/Document/0x06f-Testing-Local-Authentication.md>

Per ulteriori informazioni, vedere anche:

- OWASP Mobile Top 10: M4 (Insecure Authentication) - <https://owasp.org/www-project-mobile-top-10/2016-risks/m4-insecure-authentication>
- OWASP Mobile Top 10: M6 (Insecure Authorization) - <https://owasp.org/www-project-mobile-top-10/2016-risks/m6-insecure-authorization>
- CWE 287 (Improper Authentication) - <https://cwe.mitre.org/data/definitions/287.html>
- CWE 307 (Improper Restriction of Excessive Authentication Attempts) - <https://cwe.mitre.org/data/definitions/307.html>
- CWE 308 (Use of Single-factor Authentication) - <https://cwe.mitre.org/data/definitions/308.html>
- CWE 521 (Weak Password Requirements) - <https://cwe.mitre.org/data/definitions/521.html>
- CWE 604 (Use of Client-Side Authentication) - <https://cwe.mitre.org/data/definitions/604.html>
- CWE 613 (Insufficient Session Expiration) - <https://cwe.mitre.org/data/definitions/613.html>
