# V5: Requisiti per la Comunicazione di Rete

## Obiettivo della Sezione

Lo scopo dei controlli elencati in questa sezione è quello di garantire la riservatezza e l'integrità delle informazioni scambiate tra l'applicazione mobile e gli endpoint del servizio remoto. Come minimo, un'applicazione mobile deve impostare un canale sicuro e crittografato per la comunicazione di rete utilizzando il protocollo TLS con le impostazioni appropriate. Il livello 2 elenca ulteriori misure di difesa in profondità, come il pinning SSL.

## Requisiti per la Verifica di Sicurezza

| # | MSTG-ID | Description | L1 | L2 |
| -- | ---------- | ---------------------- | - | - |
| **5.1** | MSTG-NETWORK-1 | I dati vengono crittografati in rete utilizzando il protocollo TLS. Il canale sicuro viene utilizzato in modo coerente in tutta l'applicazione. | x | x |
| **5.2** | MSTG-NETWORK-2 | Le impostazioni TLS sono in linea con le attuali best practice, o il più vicino possibile se il sistema operativo mobile non supporta gli standard raccomandati. | x | x |
| **5.3** | MSTG-NETWORK-3 | L'applicazione verifica il certificato X.509 dell'endpoint remoto quando viene stabilito il canale sicuro. Sono accettati solo i certificati firmati da una CA affidabile. | x | x |
| **5.4** | MSTG-NETWORK-4 | L'applicazione utilizza il proprio archivio di certificati o memorizza il certificato o la chiave pubblica dell'endpoint e quindi non stabilisce connessioni con endpoint che offrono un certificato o una chiave diversi, anche se firmati da una CA affidabile. |   | x |
| **5.5** | MSTG-NETWORK-5 | L'applicazione non si affida a un unico canale di comunicazione insicuro (e-mail o SMS) per le operazioni critiche, come le iscrizioni e il recupero degli account. |  | x |
| **5.6** | MSTG-NETWORK-6 | L'applicazione è basata solo su librerie di connettività e sicurezza aggiornate. |  | x |

## Riferimenti

La OWASP Mobile Application Security Testing Guide fornisce istruzioni dettagliate per la verifica dei requisiti elencati in questa sezione.

- General: Testing Network Communication - <https://github.com/OWASP/owasp-mastg/blob/master/Document/0x04f-Testing-Network-Communication.md>
- Android: Testing Network Communication - <https://github.com/OWASP/owasp-mastg/blob/master/Document/0x05g-Testing-Network-Communication.md>
- iOS: Testing Network Communication - <https://github.com/OWASP/owasp-mastg/blob/master/Document/0x06g-Testing-Network-Communication.md>

Per ulteriori informazioni, vedere anche:

- OWASP Mobile Top 10: M3 (Insecure Communication) - <https://owasp.org/www-project-mobile-top-10/2016-risks/m3-insecure-communication>
- CWE 295 (Improper Certificate Validation) - <https://cwe.mitre.org/data/definitions/295.html>
- CWE 296 (Improper Following of a Certificate's Chain of Trust) - <https://cwe.mitre.org/data/definitions/296.html>
- CWE 297 (Improper Validation of Certificate with Host Mismatch) - <https://cwe.mitre.org/data/definitions/297.html>
- CWE 298 (Improper Validation of Certificate Expiration) - <https://cwe.mitre.org/data/definitions/298.html>
- CWE 308 (Use of Single-factor Authentication) - <https://cwe.mitre.org/data/definitions/308.html>
- CWE 319 (Cleartext Transmission of Sensitive Information) - <https://cwe.mitre.org/data/definitions/319.html>
- CWE 326 (Inadequate Encryption Strength) - <https://cwe.mitre.org/data/definitions/326.html>
- CWE 327 (Use of a Broken or Risky Cryptographic Algorithm) - <https://cwe.mitre.org/data/definitions/327.html>
- CWE 780 (Use of RSA Algorithm without OAEP) - <https://cwe.mitre.org/data/definitions/780.html>
- CWE 940 (Improper Verification of Source of a Communication Channel) - <https://cwe.mitre.org/data/definitions/940.html>
- CWE 941 (Incorrectly Specified Destination in a Communication Channel) - <https://cwe.mitre.org/data/definitions/941.html>
