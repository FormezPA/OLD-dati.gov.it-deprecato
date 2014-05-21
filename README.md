dati.gov.it
===========

drupal e ckan utilizzati su dati.gov.it

premessa
--------
il sistema prevede l'installazione di due macchine, una per drupal e una per ckan

contenuto della distribuzione
-----------------------------

- questo file
	
- datigovit-drupal.tar.gz
	il file compresso contiene il folder con la copia di drupal utilizzata
	per dati.gov.it e il file datigovit.sql che contiene il dump del database mysql
	i requisiti della macchina in cui deve girare questa installazione sono gli stessi
	indicati per drupal 7
	

- datigovit-ckan.ova
	il file contiene la copia della macchina virtuale su cui gira ckan e
	i servizi correlati (jetty, solr, postgresql, apache)


- hosts
	contiene i nomi e i numeri di ip provvisori utilizzati per le due macchine
	(la macchina drupal e quella ckan)
	
- httpd.conf
	contiene la sezione della configurazione di apache relativa alla macchina
	che ospita drupal


Dati per accedere ai due sistemi
--------------------------------
- accesso a drupal
	http://datigovit.drupal/
	usr: admin
	pwd: datigovit
	tutti gli account hanno la password: datigovit


- accesso alla macchina ckan e ai vari servizi attivi

	servizio/porta  username   password
	==============  =========  =========
	ssh/9378        formez     datigovit
	ssh/9378        ckan       datigovit
	postgres	postgres
	
	accesso a ckan anonimo in consultazione
	http://datigovit.ckan/catalog/
	
	login admin su ckan
	http://datigovit.ckan/catalog/user/login
	sezione di amministrazione
	http://datigovit.ckan/catalog/ckan=admin/config
	username: admin_formez
	password: datigovit
