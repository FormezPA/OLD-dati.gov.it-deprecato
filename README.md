dati.gov.it
===========
	drupal e ckan utilizzati su dati.gov.it

premessa
--------
	il sistema prevede l'installazione di due macchine, una per drupal e una per ckan.

contenuto della distribuzione
-----------------------------

1) **questo file**
	
2) **datigovit-drupal.tar.gz**

	il file compresso contiene il folder con la copia di drupal utilizzata su dati.gov.it
	e il file *datigovit.sql* che contiene il dump del database mysql.
	i requisiti della macchina in cui deve girare questa installazione sono gli stessi indicati per drupal 7

3) **hosts**

	contiene i nomi e i numeri di ip provvisori utilizzati per le due macchine (la macchina drupal e quella ckan)
	
4) **httpd.conf**

	contiene la sezione della configurazione di apache relativa alla macchina che ospita drupal


5) **datigovit-ckan.ova**

	La macchina virtuale ckan, prodotta con vmware, in formato aperto.
	il file è suddiviso in 9 porzioni per un totale di circa 6GB.
	Per riunire tutte le porzioni in un unico file si consiglia l'uso di 7zip http://www.7-zip.org/
	al termine dell'operazione verrà prodotto il file datigovit-ckan.ova

Le 9 porzioni del file sono disponibili su:

	1) https://mega.co.nz/#!DE4ngSKL!Pk1qU1fq_GxjSfF8RI1NSDO7C88PVua-NOo2GlpSK-M
	2) https://mega.co.nz/#!CA4SgZpA!kqGHqr5iURIMvaW8EF7IKdEU3S_EiUl7OT7LeyipKzM
	3) https://mega.co.nz/#!6Yw1laxI!s9puCPMInSNaqON7-BthNfzpldAxMddUakHu0AwFDjM
	4) https://mega.co.nz/#!bYhnzRBT!4eCchqFeUW6MOHb4uOaRRMFaDhcb2SvzJfDZKCMxkTY
	5) https://mega.co.nz/#!XZIx0QKA!6BFcyJ-LtPBlCcJJv__IcDgyp-jmnC2TrAS7rCtnWKM
	6) https://mega.co.nz/#!WA5BVCbD!E8SAlOOzGL57vZi4stEYJr91sUM_VtIMH6Z_-mbHjGc
	7) https://mega.co.nz/#!SUJRUJjZ!r4eFVjA4x9HaJ0T-D1PwQNqx1xD2AwzAHcJaYHAJB3U
	8) https://mega.co.nz/#!CVB1mSqa!WfnpSWd7evrgY6gbx1K4fFSLFFCCbuCtcjMCcp5MDuI
	9) https://mega.co.nz/#!mQghULSQ!609PTc3IPrJRlaQcGrIEIerawmqB1tEpm86DYbN9DhA

oppure in alternativa, su:

	1) http://1drv.ms/1jXEbNy
	2) http://1drv.ms/1jXEwA4
	3) http://1drv.ms/1hurFQ5
	4) http://1drv.ms/1hurLar
	5) http://1drv.ms/1hurPXJ
	6) http://1drv.ms/1hus4SC
	7) http://1drv.ms/1husdFH
	8) http://1drv.ms/1husiZU
	9) http://1drv.ms/1husl8h

per ricostruire il file datigovit-ckan.ova sono necessarie tutte le 9 porzioni.

dati per accedere ai due sistemi
--------------------------------

1) accesso a drupal

        http://datigovit.drupal/
        usr: admin
        pwd: datigovit
        tutti gli account hanno la password: datigovit

2) accesso alla macchina ckan e ai vari servizi attivi

	servizio/porta  username   password
	==============  =========  =========
	ssh/9378        formez     datigovit
	ssh/9378        ckan       datigovit
	postgres        postgres

	accesso a ckan anonimo in consultazione
	http://datigovit.ckan/catalog/

	login admin su ckan
	http://datigovit.ckan/catalog/user/login
	sezione di amministrazione
	http://datigovit.ckan/catalog/ckan-admin/config
	username: admin_formez
	password: datigovit
