<div align="center">
  <h1>Blueprint Home Assistant: Alarmo + Keypad Frient KEPZB-110</h1>
  <p><strong>Integrazione avanzata tramite Zigbee2Mqtt per la gestione intelligente della sicurezza.</strong></p>

  <a href="https://my.home-assistant.io/redirect/blueprint_import/?blueprint_url=https://github.com/teodesign/Blueprint-Home-Assistant-Alarmo-Keypad-Frient-KEPZB-110/blob/main/frient-keypad-alarmo.yaml">
    <img src="https://my.home-assistant.io/badges/blueprint_import.svg" alt="Importa in Home Assistant" />
  </a>
</div>

<hr />

<h2>📋 Descrizione del Blueprint</h2>
<p>
  Questo Blueprint permette di integrare la tastiera <strong>KEPZB-110</strong> (via Zigbee2MQTT) con l'integrazione <strong>Alarmo</strong> in Home Assistant. 
  La particolarità di questa automazione è la gestione a "due livelli":
</p>
<ul>
  <li>
    <strong>Azioni Custom:</strong> Controlla se il codice inserito corrisponde a uno dei due PIN speciali definiti dall'utente per attivare azioni personalizzate (es. aprire un cancello, accendere luci).
  </li>
  <li>
    <strong>Pass-through Alarmo:</strong> Se il codice non è tra quelli custom, viene passato direttamente ad Alarmo per le normali operazioni di inserimento/disinserimento.
  </li>
</ul>

<h2>✨ Funzionalità Principali</h2>
<ul>
  <li><strong>💡 Dual-Layer Security:</strong> Gestione prioritaria di 2 Codici Custom per automazioni extra.</li>
  <li><strong>🆘 Pulsante SOS:</strong> Azione dedicata e configurabile per la pressione del tasto di emergenza.</li>
  <li><strong>🚨 Feedback Tastiera Completo:</strong> Invia comandi MQTT alla tastiera per aggiornare lo stato dei LED e dei suoni in base allo stato di Alarmo (Ritardo ingresso/uscita, Armato, Disarmato, Allarme attivato).</li>
  <li><strong>⚠️ Sistema di Notifiche Avanzato:</strong>
    <ul>
      <li>Notifiche per Inserimento e Disinserimento (opzionali).</li>
      <li>❌ Notifica di <strong>Errore Codice</strong> con alta priorità.</li>
      <li>📲 Titoli, messaggi e livelli di priorità personalizzabili per ogni evento.</li>
    </ul>
  </li>
  <li><strong>Feedback Errore Visivo:</strong> In caso di codice errato, la tastiera emette un segnale acustico/visivo di errore (3 lampeggi/suoni).</li>
</ul>

<h2>🛠 Requisiti</h2>
<ul>
  <li><strong>Alarmo:</strong> L'integrazione Alarmo deve essere installata e configurata.</li>
  <li><strong>Zigbee2MQTT:</strong> La tastiera deve essere collegata tramite Zigbee2MQTT (necessario per il controllo tramite Topic MQTT).</li>
  <li><strong>Servizio Notifiche:</strong> Un servizio attivo (es. l'app ufficiale di Home Assistant sul tuo smartphone).</li>
</ul>

<h2>🚀 Installazione</h2>
<ol>
  <li>Assicurati di avere il file <code>.yaml</code> nella cartella <code>blueprints/automation/</code> della tua istanza.</li>
  <li>Crea una nuova automazione basata su questo blueprint.</li>
  <li>Inserisci il <strong>Topic MQTT</strong> della tua tastiera (es. <code>zigbee2mqtt/tastiera</code>).</li>
</ol>
