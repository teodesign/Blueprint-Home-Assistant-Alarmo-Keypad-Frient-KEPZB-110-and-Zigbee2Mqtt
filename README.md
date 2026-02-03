# Blueprint Home Assistant Alarmo - Keypad Frient KEPZB-110 and Zigbee2Mqtt
A home assistant blueprint to use a keypad Frient KEPZB-110 in Home Assistant with Alarmo addon and Zigbee2Mqtt


📋 Descrizione del Blueprint

Questo Blueprint permette di integrare la tastiera KEPZB-110 (via Zigbee2MQTT) con l'integrazione Alarmo in Home Assistant.

La particolarità di questa automazione è la gestione a "due livelli":

1) Azioni Custom: Controlla se il codice inserito corrisponde a uno dei due PIN speciali definiti dall'utente per attivare azioni personalizzate (es. aprire un cancello, accendere luci).

2) Pass-through Alarmo: Se il codice non è tra quelli custom, viene passato direttamente ad Alarmo per le normali operazioni di inserimento/disinserimento.

✨ Funzionalità Principali:

💡 Dual-Layer Security: Gestione prioritaria di 2 Codici Custom per automazioni extra.

🆘 Pulsante SOS: Azione dedicata e configurabile per la pressione del tasto di emergenza.

🚨 Feedback Tastiera Completo: Invia comandi MQTT alla tastiera per aggiornare lo stato dei LED e dei suoni in base allo stato di Alarmo (Ritardo ingresso/uscita, Armato, Disarmato, Allarme attivato).

⚠️ Sistema di Notifiche Avanzato: * Notifiche per Inserimento e Disinserimento (opzionali).

❌ Notifica di Errore Codice con alta priorità.

📲 Titoli, messaggi e livelli di priorità personalizzabili per ogni evento.

Feedback Errore Visivo: In caso di codice errato, la tastiera emette un segnale acustico/visivo di errore (3 lampeggi/suoni).

🛠 Requisiti
Alarmo: L'integrazione Alarmo deve essere installata e configurata.

Zigbee2MQTT: La tastiera deve essere collegata tramite Zigbee2MQTT (necessario per il controllo tramite Topic MQTT).

Servizio Notifiche: Un servizio attivo (es. l'app ufficiale di Home Assistant sul tuo smartphone).

🚀 Installazione
Assicurati di avere il file .yaml nella cartella blueprints/automation/ della tua istanza.

Crea una nuova automazione basata su questo blueprint.

Inserisci il Topic MQTT della tua tastiera (es. zigbee2mqtt/tastiera).

Seleziona la tua entità alarm_control_panel gestita da Alarmo.

Configura i tuoi PIN custom con le relative azioni e le notifiche desiderate.
