# h1 Hello Salt

Koneena Lenovo Legion Y530-15ICH, Intel Core i5-8300H CPU, 8GM RAM, Windows 11 Home Insider Preview<br>
Oracle VM VirtualBox 7.0.<br>
Ubuntu: 22.04.1 LTS, codename: jammy

## Tehtävänanto

x) Lue ja tiivistä (Tässä x-alakohdassa pelkkä luku / katselu / kuuntelu riittää, ei tarvitse tehdä testejä tietokoneella. Muutama ranskalainen viiva per artikkeli riittää)

<li>    Karvinen 2020: Command Line Basics Revisited</li>
<li>    Karvinen 2018: Salt States – I Want My Computers Like This</li>
<li>    Karvinen 2006: Raportin kirjoittaminen</li><br>

a) Tee Saltilla tiedosto yksittäisellä komentorivillä (state.single)

b) Tee saltille idempotentti, infra koodina hei maailma (siis tiedostosta, /srv/salt/foo.sls)

d) Kerää tietoa koneesta saltin avulla (grains.items)

e) Kokeile jotain toista tilaa kuin file.managed. Tärkeitä ovat pkg.installed, file.managed, service.running, file.symlink, user.present, group.present. Ohjeita saa esim "sudo salt-call --local sys.state_doc pkg.installed|less"

## x) Karvinen 2020: Command Line Basics Revisited

on käsitelty erilaisia Linux komentoja. Mainittakoon, että dollarinmerkki $ on normaali komentokehoite ja se tulee automaattisesti. Jos käyttää hash-merkkiä # on se kommenttirivi ja se ohitetaan.

<b>Muistettavia tärkeitä komentoja</b>

pwd - tulostaa työhakemiston näytölle
ls - listaa työhakemiston sisällä olevat tiedostot
cd hakemistonimi/ - siirryt tähän hakemiston
cd ..
