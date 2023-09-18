This is a composer based installer for the [Comune Silfi](https://www.drupal.org/project/comune_silfi).

# Prerequisites

1. [Composer](https://getcomposer.org/download/)

It's just composer, isn't it awesome? :)

## Installazione
Per installare il CMS Comune procedi così
1) Installa il codice:
```shell
$ composer create municipes/comune_template project-name --no-install
$ cd project-name
$ composer require drush/drush --no-install
$ composer install
```
2) Configura Drupal eseguendo [setup_step02](scripts/setup_step02__configure_drupal.sh)
3) Configura Comune eseguendo [setup_step03](scripts/setup_step03__configure_municipes.sh)

Se usi ddev puoi installare tutto con un unico comando, esegui [ddev_installer](scripts/municipes_ddev_installer.sh)
```shell
bash <(curl -s -H "Cache-Control: no-cache" "https://raw.githubusercontent.com/municipes/comune_template/10.x/scripts/municipes_ddev_installer.sh")
```

### **Da dove iniziare**

I siti Drupal presentano una serie di tipologie di contenuto (content type) che sono in relazione tra loro. Ogni tipologia di contenuto viene creata attraverso una “scheda” nel backend di Drupal, che presenta i vari campi dove aggiungere i contenuti per creare la pagina.

Consigliamo di cominciare a creare i diversi contenuti in questo ordine:

- punti di contatto;
- persone pubbliche;
- luoghi;
- unita organizzative;

Una volta iniziato il lavoro sulle prime 4 tipologie di contenuto suggerite, si può continuare con:

- documenti pubblici;
- dataset;
- eventi;
- notizie;
- fasi;
- servizi;


#### **Relazioni tra i contenuti**

L'impostazione per tipologie di contenuto (content type) permette di combinare i vari elementi per la creazione delle pagine, così che i contenuti vengano creati soltanto una volta e poi riutilizzati, se necessario, in varie parti del sito. Una volta comprese le relazioni tra le tipologie di contenuti, sarà facile creare le pagine del sito.

Alcune relazioni tra tipologie di contenuti, sono:

Unità Organizzative - Servizi
Incarichi - Persone Pubbliche
Unità Organizzative - Luoghi
Servizi - Documenti Pubblici

Questo significa, ad esempio, che ogni pagina di un'unità organizzativa può presentare una relazione con contenuti come i luoghi e i servizi.

**Attenzione!** Dal punto di vista pratico, è necessario che i contenuti che si vuole collegare vengano creati in un ordine preciso: prima i content type che fungono da contenuti di dettaglio e poi il content type contenitore (es. prima le persone, il luogo e punti di contatto e solo dopo l'evento che raggruppa persone, luogo e punti di contatto creati in precedenza).

Per collegare tra loro diverse tipologie di contenuto, quindi:

1.	crea la scheda o le schede dei contenuti di dettaglio (ad esempio, il luogo “Palazzo Baldini” che verrà associato ad un'unità organizzativa);
2.	crea la scheda del contenuto contenitore (ad esempio, la scheda della unità organizzativa “Assessorato al Turismo”);
3.	Associa, tramite l’apposito campo, le schede contenuto di dettaglio alla scheda contenuto (ad esempio, il luogo “Palazzo Baldini” all'unità organizzativa “Assessorato al Turismo”).

Per associare nuovi contenuti di dettaglio ad altri già esistenti:

1.	Crea la nuova scheda di contenuto di dettaglio (ad esempio, la scheda servizio “Iscrizione alla Scuola dell’infanzia” da associare alla scheda del contenuto contenitore “Assessorato all'Educazione”).
2.	Entra nella scheda del contenuto contenitore e, tramite l’apposito campo, associa la scheda del contenuto di dettaglio (la scheda servizio “Iscrizione alla Scuola dell’infanzia” alla scheda “Assessorato all'Educazione”).


Nella maggior parte dei casi questa correlazione è bidirezionale e automatica. Quando si crea, ad esempio, una relazione tra un luogo e una struttura, questa verrà mostrata sia nel dettaglio del luogo che in quello della struttura.



## Installation of Comune Silfi

```
composer create municipes/comune_template:10.x DIRECTORY --no-interaction
```

Composer will create a new directory called DIRECTORY.
The installed folders will contain all Drupal related files in the `web`
directory and any third-party dependencies in the composer `vendor` directory.
Drupal core will be installed to `web/core`. Inside you will find the
html directory with the entire code base of the [Comune Silfi distribution](https://www.drupal.org/project/comune_silfi).
Install your Comune Silfi site like any other Drupal website using the `install.php` script or `drush`.

## Learn more about Composer for Drupal

Checkout this [presentation](https://docs.google.com/presentation/d/1gxcxT6o47xVrfsZ7ZSQKjBRT-gfE54A1Z9kjvvGHwCo/edit#slide=id.p) from @ModsUnraveled.

## Issues

### Install issues for Comune Silfi
[documentation](https://www.drupal.org/docs/8/distributions/comune-silfi/installing-and-updating)

### Comune Silfi issues & Support
For any issues with the platform we kindly ask you to use the [drupal.org](https://www.drupal.org/project/issues/comune_silfi) issue queue.
This way we can centralise all the information and make the feedback available
for other users for documentation purposes. Next to giving people the credit they deserve.

