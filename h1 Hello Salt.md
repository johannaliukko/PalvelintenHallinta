# h1 Hello Salt

Koneena Lenovo Legion Y530-15ICH, Intel Core i5-8300H CPU, 8GM RAM, Windows 11 Home Insider Preview<br>
Oracle VM VirtualBox 7.0.<br>
Ubuntu: 22.04.1 LTS, codename: jammy<br>

# Ennen tehtäviä aloitus Salt Quickstart – Salt Stack Master and Slave on Ubuntu Linux -ohjeiden mukaan

## Salt Masterin asennus

Ennen tehtävien tekemisiä päivitin tarkistin Ubuntun päivitykset (sudo apt-get update) ja asensin Saltin (sudo apt-get -y install salt-master). Otin myös hostin (hostname -I) IP:n 10.0.2.15 talteen.
<img src="salt02.PNG"><img src="salt03.PNG">

## Salt orjan asennus

Koska olin jo hetki sitten päivittänyt Ubuntun jatkoin orjan asennukseen (sudo apt-get -y install salt-minion). Vuorooon tuli sitten uudelleenkäynnistäminen sudo systemctl restart salt-minion.service komennolla. Uudelleenkäynnistämisen jälkeen avasin minion, määrittelin masterille IP:ksi 10.0.2.15 ja id:ksi tuli johannankoti. sudo salt-key -A komennolla määrittelin avaimen orjalle ja kysymykseen prosessin eteenpäin menosta vastasin Y. Vielä tarkistus, kuka olen
<img src="salt11.PNG">

# Tehtävänanto

## a) Tee Saltilla tiedosto yksittäisellä komentorivillä (state.single)

Ensiksi loin hakemiston tiedostojen tallennusta varten. Loin tiedoston nimeltä hello.sls, jonne määrittelin tietojen tulevan hello.txt
<img src="salt15.PNG"><img src="salt16.PNG">

## b) Tee saltille idempotentti, infra koodina hei maailma (siis tiedostosta, /srv/salt/foo.sls)

Loin tiedoston rokkaa.sls ja rokkaa.txt.
<img src="saltiksi.PNG">

State ei jostain syystä mennyt läpi, joten joudun sitä myöhemmin tarkistamaan.
<img src="salt-virhe.PNG">

## d) Kerää tietoa koneesta saltin avulla (grains.items)

sudo salt ‘\*’ grains.items komento antaa paljon tietoa. Kuvassa pieni pätkä.
<img src="salt19.PNG">

## Kokeile jotain toista tilaa kuin file.managed. Tärkeitä ovat pkg.installed, file.managed, service.running, file.symlink, user.present, group.present. Ohjeita saa esim "sudo salt-call --local sys.state_doc pkg.installed|less"

Asensin pkg.install httpie ja sain alla olevan tuloksen
<img src="salt13.PNG">

## Lähteet

Tätä dokumenttia saa kopioida ja muokata GNU General Public License v3.0 mukaisesti. https://www.gnu.org/licenses/why-not-lgpl.html

Pohjana Tero Karvinen 2022: "Palvelinten hallinta" kurssi
Palvelintenhallinta, terokarvinen.com: https://terokarvinen.com/2022/palvelinten-hallinta-2022p2/?from=MoodleNews#h1-hello-salt

Salt Quickstart – Salt Stack Master and Slave on Ubuntu Linux https://terokarvinen.com/2018/salt-quickstart-salt-stack-master-and-slave-on-ubuntu-linux/

Salt States – I Want My Computers Like This, terokarvinen.com: https://terokarvinen.com/2018/salt-states-i-want-my-computers-like-this/
