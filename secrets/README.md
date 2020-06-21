Le chiavi, i token e le password devono essere inseriti in questa directory
per poter essere utilizzati direttamente. I parametri per i vari provider ed
eventuali caveat sono descritti nelle relative sezioni.

**Con l'eccezione del presente file, il contenuto di questa directory non deve essere reso pubblico.**

# Hetzner
I parametri per questo provider vanno inseriti nel file `hetzner.yml`, e sono:

| Nome                | Tipo     | Descrizione                                           |
| ------------------- | -------- | ----------------------------------------------------- |
| `jitsi_ssh_keys`    | `array`  | lista delle chiavi SSH da installare sul server Jitsi |
| `jitsi_server_ip`   | `string` | nome del __Floating IP__ da assegnare al server Jitsi |
| `jitsi_location`    | `string` | datacenter su cui creare il server Jitsi              |
| `jitsi_server_type` | `string` | tipo di server secondo le specifiche Hetzner          |
| `hcloud_token`      | `string` | __API token__ per l'accesso al Cloud Hetzner          |
