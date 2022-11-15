# h1 Hello Salt

Koneena Lenovo Legion Y530-15ICH, Intel Core i5-8300H CPU, 8GM RAM, Windows 11 Home Insider Preview
Oracle VM VirtualBox 7.0.
Ubuntu: 22.04.1 LTS, codename: jammy

# Tehtävänanto

x) Lue ja tiivistä (Tässä x-alakohdassa pelkkä luku / katselu / kuuntelu riittää, ei tarvitse tehdä testejä tietokoneella. Muutama ranskalainen viiva per artikkeli riittää)

<li>    Karvinen 2020: Command Line Basics Revisited</li>
<li>    Karvinen 2018: Salt States – I Want My Computers Like This</li>
<li>    Karvinen 2006: Raportin kirjoittaminen</li><br>

a) Tee Saltilla tiedosto yksittäisellä komentorivillä (state.single)

b) Tee saltille idempotentti, infra koodina hei maailma (siis tiedostosta, /srv/salt/foo.sls)

d) Kerää tietoa koneesta saltin avulla (grains.items)

e) Kokeile jotain toista tilaa kuin file.managed. Tärkeitä ovat pkg.installed, file.managed, service.running, file.symlink, user.present, group.present. Ohjeita saa esim "sudo salt-call --local sys.state_doc pkg.installed|less"

## x) Karvinen 2020: Command Line Basics Revisited

on käsitelty erilaisia Linux komentoja.
Komentokehotteella pystyy näppärästi käyttämään tietokonetta. Sen avulla liikutaan hakemistojen välillä ylös- tai alaspäin, listataan tiedostoja ja hallitsemaan erilaisia operaatioita.

<b>Muistettavia tärkeitä komentoja</b>

### Hakemistoihin ja tiedostoihin liittyvät

pwd tulostaa työhakemiston näytölle
ls listaa työhakemiston sisällä olevat tiedostot
cd hakemistonimi/ siirryt tähän hakemiston
cd .. siirrytään yhtä ylemmäs hakemistoon
mkdir luodaan uusi hakemisto
mv nimetään vanha hakemisto tai tiedosto uudelleen
cp kopioidaan tiedosto
rm poistetaan tiedosto ja rmdir poistetaan hakemisto, mutta rm -r poistaa hakemiston ja sisällön ilman varoituksia (käytettävä varauksella ja ajatuksella)

### SSH yhteys - turvallinen, salattu yhteyden muodostus etäkoneeseen

Kirjoitetaan ssh käyttäjätunnus@omadomain.fi ja yhteys muodostetaan. Lopetus tapahtuu kirjoittamalla exit ja palaat omalle koneellesi.

### Apua ja lisäinfoa

man ls listaa yleisimmät komennot ja niiden lyhennykset, paina h ja saat lisäapua, q kirjain lopettaa
ls --help listaa tiedostojen nimet, tarkoitukset ja lyhenteet
wget -h antaa apuja verkkoasetuksiin

### Nimppelitietoa

Caps lockin yläpuolella oleva tabulaattori on erinomainen apuväline komentojen kirjoittamiseen. Ne näyttää seuraavat käytettävissä olevat vaihtoehdot ja näin vältytään usein tulevista näppäily- eli kirjoitusvirheistä. Esimerkiksi ls /etc/re[tab][tab] antaisi tulokseksi reportbug.conf resolvconf/ resolv.conf
Se voi antaa ehdotukseksi myös tiedoston nimen päätteen.
Suositeltavaa onkin käyttää tabulaattoria eteenkin pitkissä komentosarjoissa.

### Pääkäyttäjän oikeudet

sudo apt-get update (kysyy myös salasanan) tekee tarkistuksen jos on uusia päivityksiä käyttöjärjestelmälle saatavilla.
sudo apt-get upgrade päivittää käyttöjärjestelmän
sudo apt install (ohjelma) lataa ja asentaa ohjelman

## Salt States – I Want My Computers Like This

Voit Saltin avulla hallita useampia koneina. Sillä on kaksi pääkomponeittia, jolla käsittelee infrastuktuurin solmuja (master ja minions) ja hallintajärjestelmä pitää kaikki infrastuktuurin solmut määritellyssä tilassa. Tosin sanoen master eli pääpalvelin hallitsee alempia koneita toimimaan halutun mukaisesti. Ainoastaan master pitää olla julkinen palvelin ja osoite.

## Raportin kirjoittaminen

Mietitäänpä hetki raportin kirjoittamista. Se voi tuntua työläältä, kun sitä tehdään eri teknillisissä vaiheessa samalla. Kun siinä kertoo täsmällisestii ja tapahtumat vaiheittain on helpompi myöhemmin löytää virhe(eet) ja korjata. Mitä yksityiskohtaisemmin raportin teet, sen parempi. Silloin toistettavuus säilyy.
Väliotsikoita on hyvä käyttää. Se selkeyttää asioita ja on helpommin luettavissa.
Hyviin tapoihin kuuluu, että viittaukset laitetaan näkyville ja merkitään oikeaoppisesti.
Teksti, joka on muiden henkilöiden tekemää ja kopioit ilmoittamatta lähdettä on plagiointia ja loukkaa tekijänoikeuksia.

## Lähteet

Tätä dokumenttia saa kopioida ja muokata GNU General Public License v3.0 mukaisesti. https://www.gnu.org/licenses/why-not-lgpl.html

Pohjana Tero Karvinen 2022: "Palvelinten hallinta" kurssi
Palvelintenhallinta, terokarvinen.com: https://terokarvinen.com/2022/palvelinten-hallinta-2022p2/?from=MoodleNews#h1-hello-salt

Command Line Basics Revisited, terokarvinen.com: https://terokarvinen.com/2020/command-line-basics-revisited/

Salt States – I Want My Computers Like This, terokarvinen.com: https://terokarvinen.com/2018/salt-states-i-want-my-computers-like-this/

Raportin kirjoittaminen, terokarvinen.com: https://terokarvinen.com/2006/raportin-kirjoittaminen-4/?fromSearch=raportin%20kirjoittaminen
