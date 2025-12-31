Monitoring certifikátů webu SPOSDK.CZ pomocí Vagrant a Zabbix

____________________________________________________

Tento projekt slouží k monitorování certifikátů webu sposdk.cz pomocí Zabbix serveru běžícího na Ubuntu, nasazeného přes Vagrant.
Struktura projektu:

= Vagrantfile – konfigurace virtuálního stroje

= server-install.sh – skript pro instalaci Zabbix serveru a MySQL

= hostImport.sh – skript pro import hosta (volitelný)

= klic.pub – veřejný SSH klíč pro přihlášení

= zabbix.conf.php – konfigurační soubor Zabbix web GUI

____________________________________________________

Instalace a spuštění

cd Vagrant
vagrant up

potom, go to this web
http://localhost/zabbix/

Importujte hosta pro monitoring webu sposdk.cz

Soubor hosta může být ve formátu YAML nebo XML (sposdk.yaml / sposdk.xml)

Import se provádí přes Zabbix web GUI.

____________________________________________________

Skript server-install.sh automaticky nainstaluje:

MariaDB

Zabbix server a agenty

Apache + PHP

Inicializuje databázi Zabbix

Autor
Kucheriavyiy
