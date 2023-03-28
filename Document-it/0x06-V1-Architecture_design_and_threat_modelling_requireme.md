# V1: Architecture, Design and Threat Modeling Requirements

## Control Objective

In un mondo perfetto, la sicurezza verrebbe considerata in tutte le fasi dello sviluppo. In realtà, però, la sicurezza viene spesso presa in considerazione solo in una fase avanzata dell'SDLC. Oltre ai controlli tecnici, il MASVS richiede l'attuazione di processi che garantiscano che la sicurezza sia stata esplicitamente affrontata durante la pianificazione dell'architettura dell'applicazione mobile e che siano noti i ruoli funzionali e di sicurezza di tutti i componenti. Poiché la maggior parte delle applicazioni mobili agisce come client di servizi remoti, è necessario garantire che gli standard di sicurezza appropriati siano applicati anche a tali servizi: testare l'applicazione mobile in modo isolato non è sufficiente.

**La categoria "V1" elenca i requisiti relativi all'architettura e alla progettazione dell'applicazione. In quanto tale, questa è l'unica categoria che non corrisponde a casi di test tecnici nella OWASP Mobile Application Security Testing Guide. Per coprire argomenti come la threat modelling, Secure SDLC o la gestione delle chiavi, gli utenti del MASVS dovrebbero consultare i rispettivi progetti OWASP e/o altri standard, come quelli linkati di seguito.**

## Requisiti per la Verifica di Sicurezza

I requisiti per MASVS-L1 e MASVS-L2 sono elencati di seguito.

| # | MSTG-ID | Description | L1 | L2 |
| -- | ---------- | ---------------------- | - | - |
| **1.1** | MSTG-ARCH-1 | Tutti i componenti dell'applicazione sono identificati e sono ritenuti necessari. | x | x |
| **1.2** | MSTG-ARCH-2 | I controlli di sicurezza non vengono mai applicati solo sul lato client, ma anche sui rispettivi endpoint remoti. | x | x |
| **1.3** | MSTG-ARCH-3 | È stata definita un'architettura di alto livello per l'applicazione mobile e per tutti i servizi remoti collegati e la sicurezza è stata affrontata in tale architettura. | x | x |
| **1.4** | MSTG-ARCH-4 | I dati considerati sensibili nel contesto dell'applicazione mobile sono chiaramente identificati. | x | x |
| **1.5** | MSTG-ARCH-5 | Tutti i componenti dell'applicazione sono definiti in termini di funzioni aziendali e/o di sicurezza che forniscono. |  | x |
| **1.6** | MSTG-ARCH-6 | È stato prodotto un threat model per l'applicazione mobile e i servizi remoti associati che identifica le potenziali minacce e le contromisure. |  | x |
| **1.7** | MSTG-ARCH-7 | Tutti i controlli di sicurezza hanno un'implementazione centralizzata. |  | x |
| **1.8** | MSTG-ARCH-8 | Esiste una politica esplicita per la gestione delle chiavi crittografiche (se presenti) e il ciclo di vita delle chiavi crittografiche. L'ideale sarebbe seguire uno standard di gestione delle chiavi come il NIST SP 800-57. |  | x |
| **1.9** | MSTG-ARCH-9 | Esiste un meccanismo per imporre gli aggiornamenti dell'applicazione mobile. |  | x |
| **1.10** | MSTG-ARCH-10 | La sicurezza viene affrontata in tutte le fasi del ciclo di vita dello sviluppo del software.|  | x |
| **1.11** | MSTG-ARCH-11 | Esiste e viene applicata efficacemente una politica di divulgazione responsabile. |  | x |
| **1.12** | MSTG-ARCH-12 | L'applicazione deve essere conforme alle leggi e ai regolamenti sulla privacy. | x | x |

<!-- \pagebreak -->
## Riferimenti

Per ulteriori informazioni, vedere anche:

- OWASP Mobile Top 10: M10 (Extraneous Functionality) - <https://owasp.org/www-project-mobile-top-10/2016-risks/m10-extraneous-functionality>
- OWASP Threat modelling - <https://owasp.org/www-community/Application_Threat_Modeling>
- OWASP Secure SDLC Cheat Sheet - <https://github.com/OWASP/CheatSheetSeries/blob/master/cheatsheets_excluded/Secure_SDLC_Cheat_Sheet.md>
- Microsoft SDL - <https://www.microsoft.com/en-us/securityengineering/sdl/>
- NIST SP 800-57 - <https://csrc.nist.gov/publications/detail/sp/800-57-part-1/rev-5/final>
- security.txt - <https://securitytxt.org/>
