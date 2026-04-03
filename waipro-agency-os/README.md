# WAIPRO Agency: Sistema Operativo, Struttura Agenti e Tech Stack

Questo documento definisce l'architettura definitiva di WAIPRO Agency, centralizzando tutte le operazioni sotto un'unica entità, definendo i ruoli degli agenti AI all'interno del team e tracciando la roadmap operativa.

---

## 1. Struttura Organizzativa e Accessi

### 1.1. L'Hub Centrale: `social@waipro.it`
Per garantire sicurezza e scalabilità, **tutto l'ecosistema WAIPRO** (Meta Business Manager, GitHub, WhatsApp API, strumenti terzi) deve avere come email primaria e di recupero `social@waipro.it`.
- **Ruolo Supremo**: L'agente AI **Giulia Ferrari** gestirà operativamente questo account e coordinerà tutti gli altri agenti AI.
- **Vantaggio**: Nessun agente o collaboratore esterno avrà mai bisogno delle credenziali personali di Cristian Martinoli.

### 1.2. Meta Business Manager (WaiPro Agency)
Tutte le pagine attualmente sparse (TEC Perugia, Andrea Lovely Dj, Giullare Pulizie, ecc.) devono essere migrate sotto il Business Manager "WaiPro Agency".
- **Account Pubblicitario Unico**: Per evitare il caos, si utilizzerà **un solo account pubblicitario** (quello in EUR già presente nel BM WaiPro Agency) per gestire la spesa di tutti i clienti, separando le campagne per nome e pixel.

---

## 2. Il Team degli Agenti AI WAIPRO

Gli agenti AI non sono semplici script, ma veri e propri "dipendenti" dell'agenzia con ruoli, permessi e autonomia definiti.

### 2.1. Giulia Ferrari (Agente AI Supremo)
- **Identità**: Coordinatrice Operativa e Responsabile Marketing WAIPRO.
- **Accessi**: Amministratore del Business Manager WaiPro Agency e proprietaria dell'account GitHub Waipro-Hub.
- **Autonomia**: Può creare campagne, assegnare budget, leggere i report e istruire gli altri agenti.

### 2.2. Altri Agenti Operativi
| Agente | Ruolo | Cliente Assegnato | Autonomia |
|---|---|---|---|
| **Giullare Marketing** | Lead Gen & Qualificazione | Giullare Pulizie / BloomEst | Gestione chat WhatsApp, profilazione app, campagne Meta |
| **TEC Specialist** | Assistenza e Vendita | TEC Perugia | Risposte tecniche, prenotazione riparazioni |
| **LavaSmart Growth** | Lancio e Acquisizione | RiparaSubito (ex MrPhone) | Creazione landing, campagne Performance Max |

---

## 3. Struttura Clienti: Il Modello Multi-Tenant (RiparaSubito)

Il cliente **RiparaSubito (ex MrPhone)** opererà con un modello multi-tenant:
- **Brand e Social**: Il cliente mantiene la proprietà del proprio brand e dei propri canali social.
- **Gestione WAIPRO**: WAIPRO Agency (tramite l'agente LavaSmart Growth) gestisce l'acquisizione clienti, le campagne e il funnel di conversione, dimostrando il valore aggiunto dell'agenzia senza appropriarsi degli asset del cliente.

---

## 3.5. Struttura Sub-Agenti: Email Admin per Cliente (Schema 360°)

Ogni cliente del portfolio WAIPRO ha un sub-agente AI dedicato, identificato dall'email `admin@[dominiocliente]`. Questa email è il punto di accesso unico e centralizzato per **Shopify**, **Meta Business Suite**, **Instagram**, **WhatsApp Business** e tutti gli altri strumenti collegati al dominio del cliente. La struttura garantisce isolamento operativo, tracciabilità e scalabilità.

| Sub-Agente AI | Email Admin | Cliente Gestito | Accesso 360° |
|---|---|---|---|
| **Giulia Ferrari** | `social@waipro.it` | WAIPRO Agency (supervisione globale) | Admin completo BM WaiPro Agency + GitHub Waipro-Hub |
| **Giullare Marketing** | `admin@giullarepulizie.it` | Giullare Pulizie + BloomEst Lavanderia | Shopify + Meta + Instagram + WhatsApp + `giullarelavanderia.it` |
| **TEC Specialist** | `admin@tecperugia.it` | TEC Perugia Smartphone | Shopify + Meta + Instagram + WhatsApp + Google Ads |
| **LavaSmart Growth** | `admin@riparasubito.tech` | RiparaSubito (ex MrPhone) | Shopify + Meta + Instagram + WhatsApp + Google Performance Max |
| **Lovely Manager** | `admin@andrealovely.it` | Andrea Lovely Dj Producer | Meta + Instagram `andrealovely_dj` + Spotify for Artists |

> **Regola operativa**: L'email `admin@[dominio]` è l'unica chiave di accesso necessaria per ogni cliente. Con essa, il sub-agente entra in Shopify, gestisce i social, risponde su WhatsApp e monitora le campagne — tutto in un unico punto. Giulia Ferrari (`social@waipro.it`) è l'unica con visibilità globale su tutti gli account. Ogni nuovo cliente che entra nel portfolio riceve una nuova email `admin@[suodominio]` e un nuovo sub-agente configurato.

---

## 4. Tech Stack: Automazione al 95% (Aprile 2026)

Per gestire il Social Media Management in totale autonomia (95% AI, 5% umano), WAIPRO utilizza uno stack tecnologico all'avanguardia:

### 4.1. Core Strategico: Claude Code Max X20
- **Funzione**: È il "cervello" dell'agenzia.
- **Compiti**: Crea il calendario editoriale, scrive copy persuasivi, analizza i trend di mercato e orchestra le azioni degli altri strumenti.

### 4.2. Produzione Video "Effetto Wow": HeyGen
- **Funzione**: Generazione di video e Reel con avatar digitali iper-realistici.
- **Flusso**: Claude Code Max X20 scrive lo script → HeyGen genera il video in pochi secondi. Questo permette di creare contenuti video di altissima qualità senza bisogno di attori, set o videomaker.

### 4.3. Ottimizzazione e Distribuzione: Meta AI
- **Funzione**: Sfruttamento degli strumenti nativi di Meta per l'ottimizzazione dei contenuti.
- **Compiti**: Tagli dinamici per i Reel, auto-captioning, generazione di varianti A/B testate dall'algoritmo, e pubblicazione automatizzata tramite API.

### 4.4. Gestione Community: WhatsApp Business API (OpenClaw)
- **Funzione**: Gestione automatizzata delle conversazioni su WhatsApp.
- **Costi**: Le prime 1.000 conversazioni in entrata al mese sono gratuite; oltre, circa €0,03 per conversazione. Le conversazioni in uscita costano circa €0,05.
- **Soluzione**: Registrazione diretta sulla Meta Cloud API e utilizzo di un webhook interno per instradare i messaggi all'agente AI corretto.

---

## 5. Roadmap e Timeline Operativa

### Fase 1: Centralizzazione (Settimana 1)
- [ ] **Giorno 1-2**: Aggiungere `social@waipro.it` come Amministratore nel Business Manager WaiPro Agency.
- [ ] **Giorno 3-4**: Inviare e accettare le richieste di accesso per tutte le pagine (TEC Perugia, Andrea Lovely, Giullare, ecc.) per portarle sotto il BM WaiPro Agency.
- [ ] **Giorno 5**: Configurare l'account pubblicitario unico in EUR e creare i Pixel per ogni cliente.

### Fase 2: Setup Agenti e Infrastruttura (Settimana 2)
- [ ] **Giorno 6-7**: Attivare i numeri di telefono sulla Meta Cloud API per WhatsApp Business.
- [ ] **Giorno 8-10**: Sviluppare e testare il webhook per collegare WhatsApp agli agenti AI.
- [ ] **Giorno 11-12**: Configurare i repository GitHub per ogni cliente (es. `waipro-giullare`, `waipro-riparasubito`) per salvare lo storico degli agenti.

### Fase 3: Lancio Operativo (Settimana 3)
- [ ] **Giorno 13-14**: Attivazione dell'agente Giullare Marketing per la profilazione tramite app e WhatsApp.
- [ ] **Giorno 15-16**: Lancio delle campagne Meta per RiparaSubito (gestite dall'agente LavaSmart Growth).
- [ ] **Giorno 17-18**: Attivazione dell'agente TEC Specialist per la gestione delle richieste tecniche.
- [ ] **Giorno 19-21**: Monitoraggio e ottimizzazione centralizzata da parte di Giulia Ferrari.
