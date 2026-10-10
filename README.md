Better-Internet 🚀

Un set di configurazioni e tweak focalizzati sull'ottimizzazione delle prestazioni di rete e sulla riduzione al minimo della latenza (lags/ping spikes) su sistemi Windows.
📄 Panoramica del file better.int.conf

Il file better.int.conf raccoglie i parametri chiave per la configurazione avanzata della scheda di rete (NIC). Questa configurazione è pensata specificamente per scenari in cui la reattività della connessione e la stabilità sono prioritarie rispetto al risparmio energetico (es. gaming competitivo, streaming intensivo o ambienti professionali).
⚙️ Principali Ottimizzazioni Applicate

    Disabilitazione del Risparmio Energetico: Tutti i meccanismi di risparmio energetico (come Energy-Efficient Ethernet, Green Ethernet, Power Saving Mode e Advanced EEE) sono disabilitati per impedire alla scheda di rete di entrare in stati di basse prestazioni o introdurre micro-latenze alla riattivazione.

    Gestione della Latenza e degli Interrupt:

        Interrupt Moderation: Disabilitata, per fare in modo che la scheda notifichi immediatamente la CPU all'arrivo di ogni pacchetto, riducendo al minimo il ritardo di risposta.

        Receive Side Scaling (RSS): Abilitato (impostato su 4 code) per bilanciare efficacemente il carico di rete sui core del processore.

    Buffer di Rete Ottimizzati:

        Receive Buffers: Impostati a 512

        Transmit Buffers: Impostati a 1024 (o fino a 2048) per gestire flussi di dati intensi senza perdita di pacchetti.

    Disabilitazione Wake-on-LAN (WOL): Rimossi i consumi e i circuiti attivi in background per il risveglio remoto (WOL, Magic Packet, S0ix power state), garantendo una configurazione pulita e focalizzata unicamente sulle performance attive.

🛠️ Come Utilizzare il File

    Clona o scarica il repository:
    Bash

    git clone https://github.com/LeonardoTaddei04/Better-Internet.git

    Fai riferimento al file better.int.conf per applicare manualmente o tramite script i parametri desiderati sulle proprietà avanzate del tuo controller di rete Ethernet da Gestione Dispositivi (Device Manager) in Windows.
