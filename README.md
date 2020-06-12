# Script per l'automazione

Questo repository contiene gli script Ansible per il deploy automatico delle
macchine del Partito Pirata.

## Prerequisiti

Per poter operare sulle macchine sono necessari i seguenti prerequisiti:
 - Ansible >=2.8
 - `hcloud_python`, installabile con `pip install hcloud`
 - il comando `ssh` deve poter essere eseguito

## Configurazione

Inserire i dati richiesti nei file della directory `secrets`.
Su alcuni sistemi potrebbe essere necessario aggiungere alcuni parametri di
configurazione in `local/vars.yml`. Per esempio su alcuni sistemi Mac OS X
per l'utilizzo di Python 3:

```yaml
---
# Utilizzo di Python 3 su MacOS X
ansible_python_interpreter: /usr/local/bin/python3
```

## Operazioni
 
 Le operazioni sono selezionabili tramite i tag. Questi i tag disponibili:
  - `create`: creazione della macchina
  - `destroy`: distruzione della macchina
 
 In mancanza di un tag esplicito l'operazione eseguita sarà `create`.

 ## Playbook disponibili

 Questi sono i playbook disponibili:
 - `jitsi.yml`: host per le videoconferenze Jitsi + Jibri

 ## Esempi

 Creazione di una macchina:

 ```bash
 ansible-playbook -i production jitsi.yml
 ```

 Distruzione di una macchina:
 
 ```bash
 ansible-playbook -i production jitsi.yml --tags destroy
 ```