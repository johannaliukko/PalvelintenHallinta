# h1 Hello Salt

Tehtävänanto alla

x) Lue ja tiivistä

<li>    Karvinen 2020: Command Line Basics Revisited</li>
<li>    Karvinen 2018: Salt States – I Want My Computers Like This</li>
<li>    Karvinen 2006: Raportin kirjoittaminen</li>

a) Tee Saltilla tiedosto yksittäisellä komentorivillä (state.single)

b) Tee saltille idempotentti, infra koodina hei maailma (siis tiedostosta, /srv/salt/foo.sls)

d) Kerää tietoa koneesta saltin avulla (grains.items)

e) Kokeile jotain toista tilaa kuin file.managed. Tärkeitä ovat pkg.installed, file.managed, service.running, file.symlink, user.present, group.present. Ohjeita saa esim "sudo salt-call --local sys.state_doc pkg.installed|less"
