---
title: 'Connettersi a un’istanza Public Cloud'
slug: prima-connessione
legacy_guide_number: 1787
excerpt: 'Scopri come connettersi a un’istanza Public Cloud'
section: 'Per iniziare'
hidden: true
---

**Ultimo aggiornamento 06/12/2019**

## Obiettivo

Per connettersi a un’istanza Public Cloud OVH, il procedimento da seguire è simile quello di una connessione «normale» a un server dedicato (VPS, server dedicato, ecc…), ma in questo caso con un utente specifico.

**Questa guida ti mostra come connettersi a un’istanza Public Cloud OVHcloud con Windows e Linux.**

## Prerequisiti

* Avere accesso allo [Spazio Cliente](https://www.ovh.com/auth/?action=gotomanager&from=https://www.ovh.it/&ovhSubsidiary=it){.external}
* Aver creato un’[istanza Public Cloud OVH](https://www.ovhcloud.com/it/public-cloud/){.external}

## Procedura

### Connettersi a un’istanza Linux da un ambiente Linux/Mac

Utilizza il seguente comando SSH per eseguire la connessione alla tua istanza Public Cloud:

```sh
ssh*utente*@IP_istanza
```

Nel Public Cloud, l’utente varia in base alle distribuzioni utilizzate. Ecco una tabella (non esaustiva) degli utenti in base alle distribuzioni:

|Distribuzioni|Utente|
|---|---|
|Arch Linux|arch|
|CentOS 6|CentOS 7|
|CentOS 7|CentOS 7|
|CoreOS|core|
|Debian 7|Debian 7|
|Debian 8|Debian 7|
|Debian 9|Debian 7|
|Fedora 25|Fedora 29|
|Fedora 26|Fedora 29|
|FreeBSD 11.0 ZFS|FreeBSD|
|Ubuntu 14.04|ubuntu|
|Ubuntu 16.04|ubuntu|
|Ubuntu 16.10|ubuntu|
|Ubuntu 17.04|ubuntu|

> [!primary]
>
> Se ti connetti direttamente, avrai i diritti dell’utente standard. Se vuoi usufruire dei privilegi da super-utente, utilizza il comando sudo -i o sudo su.
>


**Avviso sul certificato digitale del server SSH remoto:**


Al momento della prima connessione, dovrai confermare l’autenticità dell’host cliccando su `yes`.

```sh
The authenticity of host 217.xxx.xxx.98 (217.xxx.xx.98) cant be established.
ECDSA key fingerprint is f4:95:09:ce:b6:63:73:ea:54:db:76:5e:64:f1:5e:6d.
Are you sure you want to continue connecting (yes/no)?`
```


### Connettersi a un’istanza Linux da un ambiente Windows

Per connetterti a un’istanza Linux da Windows, è sufficiente utilizzare un programma di tipo [PuTTY](https://www.putty.org/){.external} o - per le ultime versioni di Windows 10 - utilizzare le [funzioni predefinite](https://docs.microsoft.com/en-us/windows/wsl/about){.external}. Basterà poi seguire gli stessi passaggi descritti in precedenza per Linux.


### Connettersi a un’istanza Windows

#### Completare l’installazione

Dopo aver creato la tua istanza, è necessario portare a termine il cosiddetto *sysprep*.  Per fare ciò, avvia la console VNC dal tuo [Spazio Cliente OVH](https://www.ovh.com/auth/?action=gotomanager&from=https://www.ovh.it/&ovhSubsidiary=it){.external}:

![VNC console](images/vnc_console.png)

Durante il primo step, puoi scegliere il tuo Paese, la lingua desiderata e la lingua della tastiera. Poi clicca su `Next`{.action}:

![Scegli la lingua in sysprep](images/sysprep_first_step.png)

In seguito, scegli la password per l’utente *administrator*:

![Scegli la password in sysprep](images/sysprep_password.png)

Non ti resta che confermare la tua scelta cliccando su `Finish`{.action}. L’istanza si riavvierà e potrai connetterti al server Windows.


#### Connettersi a Windows

La connessione alla tua istanza Windows avviene direttamente attraverso la funzione `Desktop remoto` da Risorse del computer in ambiente Windows:

![Scegli la password in sysprep](images/remote_desktop.png)

Negli step successivi basterà precisare l’IP della tua istanza (primo step della tua connessione tramite il desktop remoto) e poi aggiungere il tuo nome utente (administrator) e la password che hai scelto.

![Remote desktop - Login](images/remote_desktop_connection_IP.png)

![Remote desktop - User login](images/remote_desktop_connection_user.png)

Un messaggio ti chiederà di confermare la connessione:  clicca su `Sì`{.action}.

![Login confirmation](images/connection_validation.png)

Da questo momento sei connesso alla tua istanza.

> [!primary]
>
> In caso di problemi di connessione alla tua istanza Windows, verifica che il firewall Windows autorizzi la connessione RDP. Per maggiori informazioni consulta questa [guida](https://docs.ovh.com/it/vps/windows-first-config/){.external}. 
> 


## Per saperne di più 

Contatta la nostra Community di utenti all’indirizzo <https://community.ovh.com/en/>.