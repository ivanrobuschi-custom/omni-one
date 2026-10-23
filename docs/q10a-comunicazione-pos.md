---
title: "Q10A - Configurazione carte"
date: "2026-09-02"
version: "2.00"
categoria: manuale tecnico RT
protocollo: Custom
---

<!-- categoria assegnata per inferenza: verificare -->
<!-- pagina ricostruita esclusivamente dal capitolo 4 (Configurazione carte) del manuale 0576100M000218 Rev. 2.00 -->

# Configurazione carte

Procedura del manuale di configurazione del POS **Q10A** (Custom Pay) per installare l'applicazione **CARTE** sul POS: Terminal ID, codice azienda e parametri di connessione al sistema di pagamento.

[Scarica il manuale completo (PDF)](assets/resources/0576100M000218_2.00.pdf)

## Accesso al menù di configurazione del POS

1. Accendere il registratore di cassa premendo il tasto **ON/OFF**.

    !!! note "DIS-PAY"
        Nel caso di utilizzo di un DIS-PAY, accenderlo collegando l'adattatore esterno fornito alla rete elettrica. Il dispositivo si accenderà autonomamente.

2. Sul display cliente (dispositivo POS) viene visualizzata la schermata **BENVENUTO** di Custom Pay: premere sul display **entro 30 secondi**.
3. Se il dispositivo è acceso e il display è in standby, in modo equivalente, premere **due volte nell'angolo in alto a sinistra** del display.
4. Viene visualizzata la schermata **Inserisci Password**. Tramite la tastiera numerica inserire la password `mm1gg7`, dove `mm` = mese corrente e `gg` = data odierna.
5. Premere sul tasto **OK**.

!!! tip "Esempio"
    Il 22 ottobre la password è `101227`.

---

## Configurazione


### 1. Aprire l'applicazione CARTE

1. Viene visualizzata la schermata **Configurazione** con i tasti IMPOSTAZIONI, INFORMAZIONI SOFTWARE, APPLICAZIONI e REBOOT. Premere sul tasto **APPLICAZIONI**.
2. Viene visualizzata la schermata **Applicazioni** (Calcolatrice, otg role, MAXSTORE, AirViewer, Carte, Network, PAX Tools). Premere sul tasto **CARTE**.
3. Viene visualizzata la schermata **Installazione** ("Effettua la configurazione del terminale per iniziare..."). Premere sul tasto **INIZIA**.
4. Viene visualizzata la schermata **Inserisci la password installatore**. Tramite la tastiera numerica inserire la password installatore: `06306`.
5. Premere sul tasto **OK**.

![Pagina 23 - Accesso e password](assets/images/q10a-p23.png)

![Pagina 24 - Applicazioni, CARTE, INIZIA e password installatore](assets/images/q10a-p24.png)

### 2. Terminal ID e autoconfigurazione

1. Viene visualizzata la schermata **Inserisci il Terminal ID**. Con la tastiera numerica inserire il codice del **Terminal ID di 8 cifre** e premere **OK**.
2. Viene visualizzata la schermata **Autoconfigurazione**, con le opzioni *Default* e *Personalizzata...*. Premere sull'opzione **DEFAULT**.
3. Premere sul tasto **AVANTI**.
4. Viene visualizzata la schermata **Codice azienda**. Con la tastiera numerica inserire il codice azienda `89025` e premere **OK**.

![Pagina 25 - Terminal ID, autoconfigurazione e codice azienda](assets/images/q10a-p25.png)

### 3. Connessione primaria

Viene visualizzata la schermata **Connessione primaria**, con i seguenti campi:

| Campo | Valore |
|-------|--------|
| Periferica | Ethernet |
| Protocollo di trasporto | IP Header (selezionato; l'alternativa è BT) |
| IP | `xxx.xxx.xxx.xxx` (da modificare) |
| Porta | `xxxxx` (da modificare) |

1. Con la tastiera numerica modificare i parametri **IP** con `185.198.119.196` e i parametri **Porta** con `34000`.
2. Premere sul flag **TLS**.
3. Premere sul tasto **CERTIFICATO**. Viene visualizzato l'elenco: *Certificato TLS SIA*, *NEXI (Terzi)*, *Sisal TLS*.
4. Premere sul certificato **NEXI (Terzi)**.
5. Nella schermata finale controllare i campi: IP `185.198.119.196`, Porta `34000`, TLS attivo, Certificato **NEXI (Terzi)**, *Time out attesa connessione* (da 5 a 50, valore mostrato: 30) e *Time out attesa risposta* (da 10 a 50, valore mostrato: 30).

![Pagina 26 - Connessione primaria e certificato](assets/images/q10a-p26.png)

![Pagina 27 - Riepilogo e installazione](assets/images/q10a-p27.png)

### 4. Installare

1. Premere sul tasto **INSTALLA**.
2. Attendere che il dispositivo POS completi la comunicazione con il sistema (l'operazione può richiedere alcuni secondi).

!!! note "Esito dell'installazione"
    Se l'installazione non è andata a buon fine controllare le configurazioni. Se l'installazione è andata a buon fine, il dispositivo è pronto per eseguire transazioni di pagamento.

### Riepilogo parametri

| Parametro | Valore |
|-----------|--------|
| Password dinamica di accesso | `mm1gg7` |
| Password installatore | `06306` |
| Terminal ID | codice di 8 cifre |
| Autoconfigurazione | Default |
| Codice azienda | `89025` |
| Periferica | Ethernet |
| Protocollo di trasporto | IP Header |
| IP | `185.198.119.196` |
| Porta | `34000` |
| TLS | Attivo |
| Certificato | NEXI (Terzi) |
