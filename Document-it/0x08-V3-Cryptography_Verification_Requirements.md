# V3: Requisiti per la crittografia

## Obiettivo della Sezione

La crittografia è una componente essenziale quando si tratta di proteggere i dati memorizzati su un dispositivo mobile. È anche una materia dove le cose possono andare terribilmente male, soprattutto quando non si seguono le convenzioni standard. Lo scopo dei controlli di questo capitolo è garantire che l'applicazione verificata utilizzi la crittografia secondo le migliori pratiche del settore, tra cui:

- Uso di librerie crittografiche comprovate;
- Scelta e configurazione corretta delle primitive crittografiche;
- Un generatore di numeri casuali adeguato quando è richiesta casualità.

## Requisiti per la Verifica di Sicurezza

| # | MSTG-ID | Description | L1 | L2 |
| -- | ---------- | ---------------------- | - | - |
| **3.1** | MSTG-CRYPTO-1 | L'applicazione non si basa sulla crittografia simmetrica con chiavi codificate come unico metodo di crittografia. | x | x |
| **3.2** | MSTG-CRYPTO-2 | L'applicazione utilizza implementazioni comprovate di primitive crittografiche. | x | x |
| **3.3** | MSTG-CRYPTO-3 | L'applicazione utilizza primitive crittografiche appropriate per il caso d'uso specifico, configurate con parametri conformi alle best practice del settore. | x | x |
| **3.4** | MSTG-CRYPTO-4 | L'applicazione non utilizza protocolli o algoritmi crittografici che sono ampiamente considerati deprecati ai fini della sicurezza. | x | x |
| **3.5** | MSTG-CRYPTO-5 | L'applicazione non riutilizza la stessa chiave crittografica per più scopi. | x | x |
| **3.6** | MSTG-CRYPTO-6 | Tutti i valori casuali sono generati con un generatore di numeri casuali sufficientemente sicuro. | x | x |

## Riferimenti

La OWASP Mobile Application Security Testing Guide fornisce istruzioni dettagliate per la verifica dei requisiti elencati in questa sezione.

- Android: Testing Cryptography - <https://github.com/OWASP/owasp-mastg/blob/master/Document/0x05e-Testing-Cryptography.md>
- iOS: Testing Cryptography - <https://github.com/OWASP/owasp-mastg/blob/master/Document/0x06e-Testing-Cryptography.md>

Per ulteriori informazioni, vedere anche:

- OWASP Mobile Top 10: M5 (Insufficient Cryptography) - <https://owasp.org/www-project-mobile-top-10/2016-risks/m5-insufficient-cryptography>
- CWE 310 (Cryptographic Issues) - <https://cwe.mitre.org/data/definitions/310.html>
- CWE 321 (Use of Hard-coded Cryptographic Key) - <https://cwe.mitre.org/data/definitions/321.html>
- CWE 326 (Inadequate Encryption Strength) - <https://cwe.mitre.org/data/definitions/326.html>
- CWE 327 (Use of a Broken or Risky Cryptographic Algorithm) - <https://cwe.mitre.org/data/definitions/327.html>
- CWE 329 (Not Using a Random IV with CBC Mode) - <https://cwe.mitre.org/data/definitions/329.html>
- CWE 330 (Use of Insufficiently Random Values) - <https://cwe.mitre.org/data/definitions/330.html>
- CWE 337 (Predictable Seed in PRNG) - <https://cwe.mitre.org/data/definitions/337.html>
- CWE 338 (Use of Cryptographically Weak Pseudo Random Number Generator (PRNG)) - <https://cwe.mitre.org/data/definitions/338.html>
