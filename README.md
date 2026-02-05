<div align="center"> <a href="#italiano"><img src="https://img.shields.io/badge/Lingua-Italiano-green?style=for-the-badge" alt="Italiano" /></a> <a href="#english"><img src="https://img.shields.io/badge/Language-English-blue?style=for-the-badge" alt="English" /></a> </div>

<div id="italiano"></div>
<div align="center">
  <h1>Blueprint Home Assistant: Alarmo + Keypad Frient KEPZB-110</h1>
  <p><strong>Integrazione avanzata tramite Zigbee2Mqtt per la gestione intelligente della sicurezza.</strong></p>

  <a href="https://my.home-assistant.io/redirect/blueprint_import/?blueprint_url=https://raw.githubusercontent.com/teodesign/Blueprint-Home-Assistant-Alarmo-Keypad-Frient-KEPZB-110-and-Zigbee2Mqtt/main/frient-keypad-alarmo.yaml">
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
<strong>
  Questo blueprint permette di non avere codici visibili all'interno dell'automazione o di Home Assistant utilizzando i codici già inseriti inseriti in Alarmo rendendo il nostro sistema di domotica più sicuro!
</strong>

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

<hr />

<div id="english"></div>
<div align="center">
<h1>Blueprint Home Assistant: Alarmo + Frient KEPZB-110 Keypad</h1>
<p><strong>Advanced integration via Zigbee2Mqtt for intelligent security management.</strong></p>
​<a href="https://my.home-assistant.io/redirect/blueprint_import/?blueprint_url=https://raw.githubusercontent.com/teodesign/Blueprint-Home-Assistant-Alarmo-Keypad-Frient-KEPZB-110-and-Zigbee2Mqtt/main/frient-keypad-alarmo.yaml">
<img src="upload://seon4JUbAq1rQha8zTVY8Sil7xF.svg" alt="Import to Home Assistant">
</a>
<br /><br />
For more information, you can see the<a href="https://github.com/teodesign/Blueprint-Home-Assistant-Alarmo-Keypad-Frient-KEPZB-110-and-Zigbee2Mqtt/tree/main" target="_blank">
GitHub Repository</a>
</div>
​<hr />
​<h2>📋 Blueprint Description</h2>
<p>
This Blueprint allows you to integrate the <strong>KEPZB-110</strong> keypad (via Zigbee2MQTT) with the <strong>Alarmo</strong> integration in Home Assistant.
The unique feature of this automation is its "dual-layer" management:
</p>
<ul>
<li>
<strong>Custom Actions:</strong> It checks if the entered code matches one of two user-defined special PINs to trigger custom actions (e.g., opening a gate, turning on lights).
</li>
<li>
<strong>Alarmo Pass-through:</strong> If the code does not match the custom ones, it is passed directly to Alarmo for standard arming/disarming operations.
</li>
</ul>
<strong>
This blueprint ensures that codes remain hidden within the automation or Home Assistant by utilizing the codes already stored in Alarmo, making your smart home system more secure!
</strong>
​<h2>✨ Key Features</h2>
<ul>
<li><strong>💡 Dual-Layer Security:</strong> Priority management of 2 Custom Codes for extra automations.</li>
<li><strong>🆘 SOS Button:</strong> Dedicated and configurable action for the emergency button press.</li>
<li><strong>🚨 Full Keypad Feedback:</strong> Sends MQTT commands to the keypad to update LED status and sounds based on Alarmo's state (Entry/Exit delay, Armed, Disarmed, Alarm triggered).</li>
<li><strong>⚠️ Advanced Notification System:</strong>
<ul>
<li>Arming and Disarming notifications (optional).</li>
<li>❌ <strong>Invalid Code</strong> notification with high priority.</li>
<li>📲 Customizable titles, messages, and priority levels for every event.</li>
</ul>
</li>
<li><strong>Visual Error Feedback:</strong> In case of an incorrect code, the keypad emits an acoustic/visual error signal (3 flashes/beeps).</li>
</ul>
​<h2>🛠 Requirements</h2>
<ul>
<li><strong>Alarmo:</strong> The Alarmo integration must be installed and configured.</li>
<li><strong>Zigbee2MQTT:</strong> The keypad must be connected via Zigbee2MQTT (required for control via MQTT Topics).</li>
<li><strong>Notification Service:</strong> An active service (e.g., the official Home Assistant app on your smartphone).</li>
</ul>
​<h2>🚀 Installation</h2>
<ol>
<li>Ensure the <code>.yaml</code> file is in the <code>blueprints/automation/</code> folder of your instance.</li>
<li>Create a new automation based on this blueprint.</li>
<li>Enter the <strong>MQTT Topic</strong> of your keypad (e.g., <code>zigbee2mqtt/keypad</code>).</li>
</ol>
