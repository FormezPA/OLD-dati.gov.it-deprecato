dati.gov.it
===========
drupal e ckan utilizzati su [http://www.dati.gov.it](http://www.dati.gov.it)<br/> 
(installazione di test)

premessa
--------
il sistema prevede l'installazione di due macchine, una per drupal e una per ckan.

contenuto della distribuzione
-----------------------------

- **questo file**
	
- **datigovit-drupal.tar.gz**

il file compresso (prodotto con drush) contiene la copia di drupal<br/>
e il file datigovit.sql (il dump del database mysql).<br/>
i requisiti della macchina in cui deve girare questa installazione<br/>
sono indicati su drupal 7 [https://drupal.org/requirements](https://drupal.org/requirements).<br/>

- **hosts**

contiene i nomi e i numeri di ip provvisori utilizzati per le due macchine
	
- **httpd.conf**

contiene la sezione della configurazione di apache relativa alla macchina che ospita drupal

- **datigovit-ckan.ova**

La macchina virtuale ckan, prodotta con vmware, in formato aperto.<br/>
il file è suddiviso in 9 porzioni per un totale di circa 6GB.<br/>
Per riunire tutte le porzioni in un unico file si consiglia l'uso di 7zip [http://www.7-zip.org/](http://www.7-zip.org/)<br/>
al termine dell'operazione verrà prodotto il file datigovit-ckan.ova<br/>
La macchina è una Ubuntu 13.04 64bit

Le 9 porzioni del file sono disponibili su:

1. [https://mega.co.nz/#!DE4ngSKL!Pk1qU1fq_GxjSfF8RI1NSDO7C88PVua-NOo2GlpSK-M](https://mega.co.nz/#!DE4ngSKL!Pk1qU1fq_GxjSfF8RI1NSDO7C88PVua-NOo2GlpSK-M)
2. [https://mega.co.nz/#!CA4SgZpA!kqGHqr5iURIMvaW8EF7IKdEU3S_EiUl7OT7LeyipKzM](https://mega.co.nz/#!CA4SgZpA!kqGHqr5iURIMvaW8EF7IKdEU3S_EiUl7OT7LeyipKzM)
3. [https://mega.co.nz/#!6Yw1laxI!s9puCPMInSNaqON7-BthNfzpldAxMddUakHu0AwFDjM](https://mega.co.nz/#!6Yw1laxI!s9puCPMInSNaqON7-BthNfzpldAxMddUakHu0AwFDjM)
4. [https://mega.co.nz/#!bYhnzRBT!4eCchqFeUW6MOHb4uOaRRMFaDhcb2SvzJfDZKCMxkTY](https://mega.co.nz/#!bYhnzRBT!4eCchqFeUW6MOHb4uOaRRMFaDhcb2SvzJfDZKCMxkTY)
5. [https://mega.co.nz/#!XZIx0QKA!6BFcyJ-LtPBlCcJJv__IcDgyp-jmnC2TrAS7rCtnWKM](https://mega.co.nz/#!XZIx0QKA!6BFcyJ-LtPBlCcJJv__IcDgyp-jmnC2TrAS7rCtnWKM)
6. [https://mega.co.nz/#!WA5BVCbD!E8SAlOOzGL57vZi4stEYJr91sUM_VtIMH6Z_-mbHjGc](https://mega.co.nz/#!WA5BVCbD!E8SAlOOzGL57vZi4stEYJr91sUM_VtIMH6Z_-mbHjGc)
7. [https://mega.co.nz/#!SUJRUJjZ!r4eFVjA4x9HaJ0T-D1PwQNqx1xD2AwzAHcJaYHAJB3U](https://mega.co.nz/#!SUJRUJjZ!r4eFVjA4x9HaJ0T-D1PwQNqx1xD2AwzAHcJaYHAJB3U)
8. [https://mega.co.nz/#!CVB1mSqa!WfnpSWd7evrgY6gbx1K4fFSLFFCCbuCtcjMCcp5MDuI](https://mega.co.nz/#!CVB1mSqa!WfnpSWd7evrgY6gbx1K4fFSLFFCCbuCtcjMCcp5MDuI)
9. [https://mega.co.nz/#!mQghULSQ!609PTc3IPrJRlaQcGrIEIerawmqB1tEpm86DYbN9DhA](https://mega.co.nz/#!mQghULSQ!609PTc3IPrJRlaQcGrIEIerawmqB1tEpm86DYbN9DhA)

oppure, in alternativa, su:

1. [http://1drv.ms/1jXEbNy](http://1drv.ms/1jXEbNy)
2. [http://1drv.ms/1jXEwA4](http://1drv.ms/1jXEwA4)
3. [http://1drv.ms/1hurFQ5](http://1drv.ms/1hurFQ5)
4. [http://1drv.ms/1hurLar](http://1drv.ms/1hurLar)
5. [http://1drv.ms/1hurPXJ](http://1drv.ms/1hurPXJ)
6. [http://1drv.ms/1hus4SC](http://1drv.ms/1hus4SC)
7. [http://1drv.ms/1husdFH](http://1drv.ms/1husdFH)
8. [http://1drv.ms/1husiZU](http://1drv.ms/1husiZU)
9. [http://1drv.ms/1husl8h](http://1drv.ms/1husl8h)

per ricostruire il file datigovit-ckan.ova sono necessarie tutte le 9 porzioni.

dati per accedere ai due sistemi
--------------------------------

- accesso a drupal
http://datigovit.drupal/<br/>
usr: admin<br/>
pwd: datigovit<br/>
tutti gli account hanno la password: datigovit<br/>

- accesso alla macchina ckan e ai vari servizi attivi
<pre>servizio/porta  username   password
--------------  --------   --------
ssh/9378        formez     datigovit
ssh/9378        ckan       datigovit
postgres        postgres</pre>

- accesso a ckan anonimo in consultazione<br/>
http://datigovit.ckan/catalog/<br/>
login admin su ckan<br/>
http://datigovit.ckan/catalog/user/login<br/>
sezione di amministrazione<br/>
http://datigovit.ckan/catalog/ckan-admin/config<br/>
username: admin_formez<br/>
password: datigovit<br/>
