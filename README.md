![portada]()

# PROJECTE TRANSVERSAL 
GRUP 4
Mario Alaez, Manuel Reyes, Cristhian Godoy
Gerson Interiano & Silvia Martin
ASIXc1B 29/05/2025

# INDEX
[**Objectius del projecte: 2**](#_38xkcq3hwdcu)

[**Resum del projecte 2**](#_312satv3yjia)

[**1.1 Ubicació física 3**](#_gkh25xf1rrzz)

[**1.2 Infraestructura IT: 5**](#_s6wbo29ytur9)

[**1.3 Infraestructura eléctrica: 8**](#_ql06ffml0x2n)

[**1.4 Seguretat Física 14**](#_4kjavjq8m9zf)

[**1.5 Seguretat Lògica 16**](#_3y36p8gugjk7)

[**2 Serveis 27**](#_vt3rt4lbkp18)


# Resum del projecte
InnovateTech és una empresa especialitzada en la creació i distribució de contingut digital que vol desenvolupar una arquitectura de Centre de Processament de Dades al núvol. L’objectiu principal és disposar d’una infraestructura tecnològica moderna, segura i sostenible, capaç de donar suport als serveis web i a la transmissió d’àudio i vídeo de manera eficient.

El projecte s’alinea amb els Objectius de Desenvolupament Sostenible de l’Agenda 2030, apostant per l’ús d’energies renovables, la reducció de l’impacte ambiental i la protecció de dades.

**Objectius concrets:**

* Dissenyar un CPD al núvol eficient, destral i amb baix impacti ambiental.

* Donar suport als necessitats actuals i futures del negoci.

* Garantir la qualitat del servei multimèdia amb anàlisi de l’amplada de banda.

* Complir amb les normatives internacionals de seguretat de dades.

* Optimitzar l’ús de recursos i calcular la petjada ecològica.

* Documentar el projecte en format Markdown i publicar-la GitHub.


# 1 Proposta de CPD

## 1.1 Ubicació física

En el nostre cas, la infraestructura física principal, que allotjarà els quatre servidors físics locals, estarà ubicada en una oficina a Sant Cugat, instal·lat en una planta intermèdia. Aquesta infraestructura es complementarà amb tres servidors addicionals ubicats al núvol, distribuïts estratègicament pels proveïdors de cloud per optimitzar el rendiment i garantir la seguretat de les dades.

Per tant, hem de tenir en compte la ubicació física dels nostres servidors per poder aplicar un sistema de climatització adaptat per a aquest lloc. Podem aplicar diferents sistemes per poder controlar-ho; aplicarem els sistemes HVAC, que s’encarregarà de controlar la temperatura, ventilació i qualitat de l’aire. A més, per millorar l’eficiència energètica, podem utilitzar sistemes de free-cooling si les condicions climàtiques locals ho permeten en certs períodes. Per als servidors al núvol, la climatització és gestionada directament pel proveïdor del servei.


Pel que fa a la sala física, hem d’aplicar mesures per dificultar la identificació i accés, millorant la seguretat. La ubicació dins de l'oficina és essencial; és preferible ubicar-lo en plantes intermèdies i evitar plantes baixes per risc d’accessos no autoritzats i evitar també plantes superiors per l’exposició a condicions ambientals adverses. A més, de no tenir cap finestra ni senyalització evident que indiquin la ubicació o situació del CPD. El disseny de la sala també és important; utilitzarem portes i parets que no es distingeixen de la resta de l'edifici. Hem d’utilitzar materials que no destaquin i que siguin resistents per mantenir la discreció i seguretat. També tindrem rutes d’accessos no evidents que no estiguin connectades amb accessos principals.

![sala](https://github.com/ManuelReyes-ITB2425/Projecte-24-25/blob/main/proyecto/Fotos/part%20teorica/Manel/Captura%20de%20pantalla%20de%202025-05-21%2012-09-15.png) 

Per un altre costat, la distribució i gestió del cablejat per als servidors físics, la seva connexió a la xarxa i als serveis al núvol requereix atenció. És important escollir el cablejat correcte. Per connexions internes dins del CPD del lloc adaptat, utilitzarem fibra òptica monomode, ideal per llargues distàncies dins del CPD. També el cablejat estructurat Cat 7 per les connexions de servidors dins de la instal·lació, assegurant velocitats de 10 Gbps.

A causa de la necessitat de connectar-nos de manera fiable i eficient amb els servidors al núvol, utilitzarem una configuració de xarxa robusta. Això implica connexions a Internet d'alta capacitat i, potencialment, l'ús de tecnologies com SD-WAN o connexions dedicades als proveïdors de núvol, buscant principis similars als que oferirien les xarxes de fibra òptica submarina i el protocol MPLS en un escenari de múltiples CPDs físics internacionals (baixes latències i alta fiabilitat).

També, hem de separar el cablejat a la instal·lació i distribuir-lo d’una manera eficient per evitar interferències electromagnètiques, també etiquetant el cablejat per facilitar el manteniment. Hem d'assegurar també rutes alternatives de connexió a la xarxa per mantenir la connectivitat en cas de fallada.

Per optimitzar la gestió del CPD, es disposarà de terra tècnic, que permetrà la canalització del cablejat i dels sistemes de climatització de forma segura i flexible. També el sostre tècnic, per facilitar la instal·lació d’equips de ventilació, il·luminació i distribució d’aire.


Organització cablejat:

![cables](https://github.com/ManuelReyes-ITB2425/Projecte-24-25/blob/main/proyecto/Fotos/part%20teorica/Manel/Captura%20de%20pantalla%20de%202025-05-21%2012-11-46.png)

#

## 1.2 Infraestructura IT

La infraestructura requerirà un total de 4 servidors físics locals i 3 instàncies al núvol, amb l'objectiu de garantir l'alta disponibilitat, redundància, rendiment òptim i seguretat de les dades i serveis.

**Servidors locals**

**Servidor Windows 1 → AD + BD + DNS primari**

[**Enllaç**](https://www.dell.com/es-es/shop/servidores-almacenamiento-y-redes/servidor-de-montaje-en-rack-poweredge-r550/spd/poweredge-r550/per5503a?configurationid=63a9139a-95e8-4626-8238-84ce2cb6448e)**:**

- **Model**: Dell PowerEdge R550
- **CPU**: Intel Xeon Silver 4310 (12 nuclis / 24 fils)
- **RAM**: 32 GB RDIMM, 3200 MT/s
- **Emmagatzematge**: 4 × 1TB SSD SATA en RAID 10
- **Xarxa**: 10GbE SFP+

**Servidor Windows 2 → FTP + DNS secundari**

[**Enllaç**](https://www.pccomponentes.com/dell-poweredge-r250-intel-xeon-e-2314-16gb-2tb?srsltid=AfmBOoogM6taePpGJhN4Z5b82q3D39c92tqcTq3PzmtzL-FQuVXiXv-H)**:**

- **Model**: Dell PowerEdge R250
- **CPU**: Intel Xeon Silver 4314
- **RAM**: 32 o 64 GB ECC DDR4
- **Emmagatzematge**: 2 × 480 GB SSD en RAID 1
- **Xarxa**: Dual 10GbE (SFP+ o RJ45, compatible amb Cat 7)

**Servidor Ubuntu → Audio + Streaming + Web**

[**Enllaç:**](https://www.dell.com/es-es/shop/servidores-almacenamiento-y-redes/servidor-de-montaje-en-rack-poweredge-r450/spd/poweredge-r450/per4503a?configurationid=17394b0e-9052-4f3d-8fe1-58354ca4dabb#techspecs_section)

- **Model**: Lenovo ThinkSystem SR630
- **CPU**: Intel Xeon Silver 4210R
- **RAM**: 32 GB
- **Emmagatzematge**: 4 × 1TB SSD SATA en RAID 10

S'han previst unitats idèntiques al núvol d'aquest servidors per facilitar el balanceig de càrrega i garantir redundància en cas de fallada.

**1 Servidor de còpies (offsite):**

[**Enllaç**](https://www.pccomponentes.com/qnap-ts-453d-4g-nas)**:**

- **Model**: QNAP TS-453D
- **CPU**: Intel Celeron J4125
- **RAM**: 4 GB (ampliable a 8 GB)
- **Bahies**: 4 × HDD/SSD amb RAID 5

**Infraestructura de xarxa**

**Patch Panel**

- **Model**: Lanberg Patch Panel 24 ports 1U Cat.7 FTP (PPS7-1024-B)

**Switch**

[**Enllaç:**](https://www.pccomponentes.com/hpe-2930f-switch-24-puertos-gigabit-poe-4-sfp?srsltid=AfmBOoqpqz-Sw0tID-7cbM6R5OnbXnJExzFeKCM-Kk-UCagorBP46rkQ)

**Característiques**:

- 24 ports Gigabit (PoE)  

- 4 ports SFP+ per a uplinks de 10 GbE  

- Gestió avançada (QoS, VLANs, spanning-tree, etc.)  

- Compatible amb Cat.7

**Instàncies Cloud**

Hem desplegat 3 instàncies virtuals al núvol, cada una corresponent a un dels servidors principals locals:

- **Servidor Cloud 1**: Replica de Windows 1 (AD + BD + DNS)
- **Servidor Cloud 2**: Replica de Windows 2 (FTP + DNS)  

- **Servidor Cloud 3**: Replica del servidor Ubuntu (streaming, audio i web)
- **Servidor Cloud 4:** Firewall

**Planell dels racks**

La nostra infraestructura està formada per tres racks interconnectats. Cada rack disposa d’un patch panel i un servidor, mentre que al rack central s’hi ubiquen el switch i el router, que actuen com a elements principals de gestió i distribució del trànsit de dades.

Els cables verds indiquen les connexions entre els servidors i els patch panels, mentre que els cables blaus mostren les interconnexions entre els diferents patch panels, que permeten establir comunicació entre els tres racks. Aquestes connexions acaben centralitzant-se al switch. El router, connectat a aquest, és l’encarregat de facilitar la connexió amb xarxes externes.

![Rack](https://github.com/ManuelReyes-ITB2425/Projecte-24-25/blob/main/proyecto/Fotos/part%20teorica/Silvia/Captura%20de%20pantalla%20de%202025-05-20%2009-10-14.png)
#

## 1.3 Infraestructura elèctrica

**Descripció general:**

La infraestructura elèctrica del nostre Centre de Processament de Dades ha estat dissenyada per garantir seguretat, continuïtat de servei i eficiència energètica, tenint en compte la distribució global dels nostres servidors i la seva ubicació geogràfica diferenciada.

**Alimentació elèctrica redundant**

La infraestructura elèctrica del nostre Centre de Processament de Dades (CPD) ha estat meticulosament dissenyada per assegurar un alt nivell de disponibilitat, continuïtat de servei i eficiència energètica, adaptant-se a les necessitats operatives actuals i preveient l'escalabilitat futura. El disseny fonamental es basa en la redundància de les fonts d'alimentació principals i la protecció mitjançant Sistemes d'Alimentació Ininterrompuda (SAI) per als equips de Tecnologies de la Informació (TI) i sistemes crítics auxiliars.

**2\. Sistema de Subministrament Elèctric Principal:**

Cada seu física del CPD compta amb una instal·lació elèctrica robusta, alimentada per dues acometides elèctriques independents (Feed A i Feed B) provinents de la xarxa pública. Aquestes acometides alimenten un Cuadro General de Distribución (CGD) central, que actua com a nucli per a la distribució de l'energia dins de les instal·lacions. Aquesta configuració de doble acometida minimitza el risc d'interrupcions totals del servei degudes a fallades en una de les línies de subministrament extern.

**3\. Línies d'Alimentació Redundants (Línia A i Línea B) i Sistemes SAI:**

Des del CGD, l'energia es canalitza cap a dos circuits elèctrics principals i independents, denominats Línia A i Línia B. Cada una d'aquestes línies alimenta un Sistema d'Alimentació Ininterrompuda (SAI) dedicat (SAI A i SAI B). Aquests SAIs estan dimensionats per:

- Proporcionar energia filtrada i estabilitzada als equips sensibles.
- Garantir una autonomia mínima de 15 minuts a plena càrrega operativa dels equips de TI connectats, permetent un apagat controlat dels sistemes en cas d'interrupció prolongada del subministrament extern, o bé donant temps per a la possible commutació a un grup electrogen (si n'hi hagués en una fase posterior).
- La capacitat seleccionada per a cada una de les dues unitats SAI principals (SAI A i SAI B) és d'aproximadament 2200VA (equivalent a uns 1980W reals, per exemple el **APC by Schneider Electric** compleix aquestes característiques amb un factor de potencia de 0,9). Aquest dimensionament s'ha establert considerant la càrrega màxima estimada per a cada línia:
  - **Càrrega Màxima Estimada per a SAI A: 805 Watts.** Aquesta càrrega prové principalment del Servidor R550 (PSU1), el Switch Aruba, els Sensors NetBotz (ubicats al Rack 1) i el Servidor R250 (ubicat al Rack 2).
  - **Càrrega Màxima Estimada per a SAI B: 500 Watts.** Aquesta càrrega prové principalment del Servidor R550 (PSU2), el Router Principal (ubicats al Rack 1) i el Servidor SR630 (ubicat al Rack 3).
- Aquesta capacitat individual de 2200VA per SAI proporciona un marge operatiu superior al 50% en cada línia respecte a la càrrega màxima actual, assegurant fiabilitat, una vida útil òptima de les bateries i capacitat per a futures petites expansions sense necessitat de reemplaçar els SAIs immediatament."

**4\. Distribució d'Energia als Racks (PDUs):**

Cada un dels quatre racks destinats a equips de TI està equipat amb dues Unitats de Distribució d'Energia (PDUs) independents:

- **PDU A:** Connectada i alimentada per SAI A (Línia A).
- **PDU B:** Connectada i alimentada per SAI B (Línia B).

Aquesta configuració de PDUs duals per rack és fonamental per implementar la redundància a nivell d'equip.

**5\. Alimentació dels Equips de TI:**

La connexió dels equips de TI a les PDUs es realitza de la següent manera, buscant un equilibri entre redundància i optimització de recursos:

- **Servidor amb Doble Font d'Alimentació (Dell PowerEdge R550):** Aquest servidor crític, equipat amb dues fonts d'alimentació (PSU), es connecta amb una PSU a la PDU A i l'altra PSU a la PDU B del seu rack corresponent (Rack 1). Això garanteix la màxima disponibilitat per a aquest equip, ja que pot continuar operant fins i tot amb la fallada completa d'una de les línies d'alimentació o un dels SAIs.
- **Equips amb Font d'Alimentació Única (Servidors Dell R250, Lenovo SR630; Switch HPE Aruba; Router Principal; Sensores NetBotz):** Actualment, aquests equips es connecten a una única PDU (ja sigui A o B), distribuint-los estratègicament entre les dues línies per balancejar la càrrega global sobre els SAIs A i B i per minimitzar l'impacte d'una fallada en una sola línia.
  - El servidor Dell R250 (Rack 2) s'alimenta de la Línia A (PDU A2).
  - El servidor Lenovo SR630 (Rack 3) s'alimenta de la Línia B (PDU B3).
  - El Switch HPE (Rack 1) s'alimenta de la Línia A (PDU A1).
  - El Router Principal (Rack 1) s'alimenta de la Línia B (PDU B1).
  - Els Sensors NetBotz (Rack 1) s'alimenten de la Línia A (PDU A1).

**6\. Previsió Futura: Implementació d'Interruptors de Transferència Automàtica (ATS):**

Per augmentar la resiliència dels equips crítics amb font d'alimentació única (com el Switch i el Router), es contempla com a millora futura la implementació d'Interruptors de Transferència Automàtica (ATS) a nivell de rack. Un ATS permetria connectar aquests equips a ambdues línies d'alimentació (A i B) simultàniament, commutant automàticament a la línia de reserva en cas de fallada de la línia principal, sense interrupció del servei per a l'equip connectat. Aquesta actualització es planificarà segons l'evolució de les necessitats de disponibilitat i pressupost.

**7\. Alimentació de Sistemes Auxiliars Crítics (HVAC):**

Els sistemes de climatització, tant el sistema d'aire com el de refrigeració líquida, són vitals per al correcte funcionament del CPD. Aquests sistemes es consideren càrregues d'alt consum i s'alimenten mitjançant circuits dedicats i degudament protegits directament des del Cuadro General de Distribución (CGD), independents dels SAIs destinats als equips de TI. Es realitzarà un dimensionament exhaustiu d'aquests circuits per garantir la seva capacitat i fiabilitat.

**8\. Gestió del Cablejat i Entorn Físic:**

Per optimitzar la gestió i seguretat del CPD, s'implementarà:

- **Terra Tècnic:** Facilitarà la canalització ordenada i protegida del cablejat elèctric i de dades, així com la distribució de fluxos d'aire fred.
- **Sostre Tècnic:** Permetrà la instal·lació d'equips de ventilació, il·luminació i altres infraestructures.
- **Canalitzacions Separades:** Per a cablejat de potència i cablejat de dades, minimitzant interferències electromagnètiques.
- **Etiquetatge Exhaustiu:** De tots els components elèctrics i de cablejat per facilitar la identificació, el manteniment i la resolució d'incidències.
- **Racks Tancats:** Per millorar la seguretat física, el control ambiental i l'eficiència de la refri

[Enllaç](https://drive.google.com/file/d/1eCAv05kAge5WRgztfIPfRZaM4Xw61cSj/view?usp=sharing) al diagrama del mapa elèctric

**Càlculs de consum**

S’ha fet un estudi detallat del consum energètic estimat per servidor:

| **Servidor** | **Model** | **Consum Idle** | **Consum Típic** | **Consum Màxim** | **Dissipació BTU/hr** | **UPS Recomanat** |
| --- | --- | --- | --- | --- | --- | --- |
| **Windows 1** (AD + BD) | Dell PowerEdge R550 | 50–70 W | 130–180 W | 250–300 W | Fins a 3000 BTU/hr (font de 800W) | APC SMT1500RM2UC (1440 VA / 1000 W) |
| --- | --- | --- | --- | --- | --- | --- |
| **Windows 2** (FTP + DNS) | Dell PowerEdge R250 | 40–60 W | 80–120 W | 150–200 W | Fins a 1870 BTU/hr (font de 450W) | APC SMT1000RM2UC (1000 VA / 700 W) o compartit amb R630 |
| --- | --- | --- | --- | --- | --- | --- |
| **Ubuntu** (Web + Audio + Streaming) | Lenovo ThinkSystem SR630 | 50–70 W | 100–150 W | 200–250 W | Fins a 3357 BTU/hr (font de 750W) | Eaton 5P1550iRTA (1100 W) o APC SMT1500RM2UC |
| --- | --- | --- | --- | --- | --- | --- |

| **Dispositiu** | **Model** | **Consum Idle** | **Consum Típic** | **Consum Màxim** | **BTU/hr Màxim** | **Comentaris** |
| --- | --- | --- | --- | --- | --- | --- |
| **Switch L2+ amb PoE+** | HPE Aruba 2930F 24G PoE+ | ~36,8 W | ~60–120 W (estimat) | 445 W | 1518 BTU/hr | Suporta fins a 370 W de PoE+. Ideal per alimentar APs, telèfons IP, càmeres. |
| --- | --- | --- | --- | --- | --- | --- |

| **Sistema** | **Model** | **Consum Mínim** | **Consum Típic (Rated)** | **Consum Màxim** |
| --- | --- | --- | --- | --- |
| **Aire** | Daikin FTXS20KVMA (2 kW split) | N/D | 450 W | N/D |
| --- | --- | --- | --- | --- |
| **Líquid (DLC)** | Chilldyne CF‑CDU300 (300 kW capacity) | N/D | ~4 500 W (one pump) | ~7 300 W (two) |
| --- | --- | --- | --- | --- |
| **Sensors** | APC NetBotz Rack Monitor 750 (NBRK0750) | N/D | N/D | N/D |
| --- | --- | --- | --- | --- |

Cada valor correspon als documents tècnics dels fabricants o anàlisis especialitzades citades. Les consumicions “Mitjà” no sempre es detallen en les fonts, de manera que s’indica principalment Idle i màxim per a equips IT; en sistemes UPS/HVAC s’exposa més aviat eficiència i autonomia (en minuts).

El servidor de backup **QNAP TS-453D**, segons proves i especificacions reals, consumeix entre **11,3W (idle)** i **25,98** en càrrega, depenent de discs i RAID. Es pren una mitjana **de 26W**.

| QNAP TS-453D | Nova Zelanda | Backup | 11,3 | 25,98 | 26  |
| --- | --- | --- | --- | --- | --- |

## 1.4 Seguretat Física

**1\. Elements de control d’accés**

Per controlar qui pot accedir físicament al CPD, es proposen les següents mesures:

- Portes de seguretat reforçades amb sistema electrònic (control d'accés amb registre).
- Lectors biomètrics (empremta digital o reconeixement facial) combinats amb targeta per doble verificació (doble autenticació).
- Sistema de registre d’accessos digital amb registre horari.
- Política d’accés per rols: només tècnics autoritzats poden accedir al recinte principal dels servidors.

![puerta](https://github.com/ManuelReyes-ITB2425/Projecte-24-25/blob/main/proyecto/Fotos/part%20teorica/Silvia/control-access-clercom-banner.jpg)


**2\. Videovigilància**

El CPD estarà monitoritzat en tot moment amb un sistema CCTV d’alta resolució:

- Càmeres IP de 360º amb visió nocturna a:
- Entrades i sortides.
  - Zones interiors del CPD.
  - Passadissos d’accés restringit.
- Senyalització clara de zona videovigilada (complint la normativa de protecció de dades).

![camara360](https://github.com/ManuelReyes-ITB2425/Projecte-24-25/blob/main/proyecto/Fotos/part%20teorica/Silvia/camara360.png)

**3\. Prevenció, detecció i extinció d’incendis**

Per protegir el CPD contra el foc, proposem un sistema integral format per:

**Prevenció:**

- Materials ignífugs en terres, parets i sostres.
- Cablejat certificat per evitar curtcircuits.
- Separació entre sistemes elèctrics i informàtics.
- Sistema de ventilació intel·ligent per evitar sobreescalfament.
- Portes tallafocs.

![techo](https://github.com/ManuelReyes-ITB2425/Projecte-24-25/blob/main/proyecto/Fotos/part%20teorica/Silvia/Falso%20techo.png)

![Puerta](https://github.com/ManuelReyes-ITB2425/Projecte-24-25/blob/main/proyecto/Fotos/part%20teorica/Silvia/puerta-cortafuego.png)


**Detecció:**

- Sensors de fum òptics i de calor al sostre i sota el terra tècnic.
- Sistema de detecció precoç amb aspiració d’aire que detecta partícules de fum molt abans de ser visibles.
- Termostats per tenir una mica de control si se supera la temperatura establerta.

![termo](https://github.com/ManuelReyes-ITB2425/Projecte-24-25/blob/main/proyecto/Fotos/part%20teorica/Silvia/termostato-digital-wk-010pw-gree-3igr9144.jpg)

**Extinció:**

- Sistema automàtic d’extinció amb gas Novec:
  - No danya els equips electrònics.
  - Apaga el foc sense deixar residus.
- Extintors manuals de CO₂ disponibles a les sortides.

![extintor](https://github.com/ManuelReyes-ITB2425/Projecte-24-25/blob/main/proyecto/Fotos/part%20teorica/Manel/Captura%20de%20pantalla%20de%202025-05-21%2012-14-24.png)

![gas](https://github.com/ManuelReyes-ITB2425/Projecte-24-25/blob/main/proyecto/Fotos/part%20teorica/Silvia/gas-novec.jpg)


**4\. Vies d’evacuació**

- Mínim dues sortides d’emergència senyalitzades amb llums LED.
- Portes d’emergència amb barra antipànic, fàcils d'obrir.
- Il·luminació d’emergència en cas de tall de subministrament.
- Cartells indicadors i plànols d’evacuació a cada entrada.
- Passadissos lliures d’obstacles, amb mínim 1 m d’ample.
- Simulacres semestrals per assegurar que el personal sap com actuar en cas d’incident.

![led](https://github.com/ManuelReyes-ITB2425/Projecte-24-25/blob/main/proyecto/Fotos/part%20teorica/Manel/Captura%20de%20pantalla%20de%202025-05-21%2012-50-40.png)

![Vias](https://github.com/ManuelReyes-ITB2425/Projecte-24-25/blob/main/proyecto/Fotos/part%20teorica/Manel/Captura%20de%20pantalla%20de%202025-05-21%2012-03-11.png)

Organització càmera 1:

![Camara](https://github.com/ManuelReyes-ITB2425/Projecte-24-25/blob/main/proyecto/Fotos/part%20teorica/Manel/Captura%20de%20pantalla%20de%202025-05-21%2012-11-46.png)


![Plano](https://github.com/ManuelReyes-ITB2425/Projecte-24-25/blob/main/proyecto/Fotos/part%20teorica/Silvia/Captura%20de%20pantalla%20de%202025-05-26%2010-35-18.png)


## 1.5 Seguretat Lògica

**Restricció d’accés per autorització**

Restringirem l'accés a l’usuari del CPD usant targetes identificatives, de tal forma que cada empleat amb permís tindrà la seva targeta per a accedir, que s'ha de posar al teclat. D'aquesta manera no comprometem dades biomètriques sensibles i no es podrà accedir només amb usuari i contrasenya.

**Tallafocs (Firewalls)**

Per als tallafocs (o firewalls), utilitzarem OPNsense, el qual és un tallafoc que anirà en una màquina a part al núvol i restringirà tot el trànsit maliciós.

**Monitoratge**

Per al monitoratge dels nostres equips Linux i Windows utilitzarem Veyon, que és un programari que permet monitorar fàcilment múltiples usuaris alhora i fins i tot controlar els ordinadors o bloquejar-los.

El primer pas per monitoritzar és descarregar-se el programa Veyon i configurar-lo, per començar hem de seleccionar l'opció d'utilitzar claus.
![monitoratge1](https://github.com/ManuelReyes-ITB2425/Projecte-24-25/blob/90ebe3b9e4950c5c37deb1c8e7a7830f2482c180/proyecto/Fotos/serveis/Monitoratge/Captura%20de%20pantalla%20de%202025-05-26%2008-44-49.png)

El següent pas és crear el parell de claus.
![monitoratge2](https://github.com/ManuelReyes-ITB2425/Projecte-24-25/blob/90ebe3b9e4950c5c37deb1c8e7a7830f2482c180/proyecto/Fotos/serveis/Monitoratge/Captura%20de%20pantalla%20de%202025-05-26%2008-45-45.png)

I la clau pública la passem a totes les màquines que vulguem monitoritzar i aquestes l'hauran d'importar.
![monitoratge3](https://github.com/ManuelReyes-ITB2425/Projecte-24-25/blob/90ebe3b9e4950c5c37deb1c8e7a7830f2482c180/proyecto/Fotos/serveis/Monitoratge/Captura%20de%20pantalla%20de%202025-05-26%2008-46-02.png)

Ja per últim afegim la mateixa ubicació que a la màquina en la qual vam crear les claus i ja estaria per part del client.

Ara només quedaria anar a la màquina servidor i afegir l'ordinador a 'Locations & computers'.
![monitoratge4](https://github.com/ManuelReyes-ITB2425/Projecte-24-25/blob/90ebe3b9e4950c5c37deb1c8e7a7830f2482c180/proyecto/Fotos/serveis/Monitoratge/Captura%20de%20pantalla%20de%202025-05-26%2008-46-22.png)

**Còpies de seguretat / Backups**

Per a les còpies de seguretat de Linux es poden fer servir scripts i l'ús de comandes com ara “tar” i en quant a Windows, l'ús de Windows Server Backup més scripts permet fer còpies de seguretat i passar-les a altres màquines. El destí de les còpies serà el QNAP TS-453D; aquest servidor està fora de l'edifici de l'empresa per garantir una major seguretat i, depenent de la volatilitat de les dades, es faran més o menys còpies incrementals.

[**Enllaç:**](https://docs.google.com/spreadsheets/d/1ehn85YJZ_ASM9lbmWm7qbArGI33OPLD-D0ais7v6l28/edit?usp=sharing)
![copias](https://github.com/ManuelReyes-ITB2425/Projecte-24-25/blob/727d2261fd6ccef69c5b0d17b9a25202d2b68fd3/proyecto/Fotos/part%20teorica/Mario/Copias.png)


**RAID**

Per al servidor de còpies, hem decidit utilitzar un NAS més un RAID 5. Amb tres discs, aquesta configuració ens proporciona una capacitat útil equivalent a dos discs per a les dades, mentre que la informació de paritat (distribuïda entre tots els discs) ens permet recuperar les dades en cas de fallada d'un d'ells. A més, aquest sistema està centralitzat, fet que simplifica molt la realització de còpies de seguretat i la compartició d'arxius. Gràcies a aquesta redundància, si un dels discs falla, podem reconstruir tota la informació, ja que el sistema està dissenyat per tolerar la pèrdua d'un disc sense perdre dades.

Per al servidor d'AC i BBDD hem decidit utilitzar un RAID 10 per tenir molt espai per a totes les nostres dades i a més redundància

**RAID 10:**

Per fer el RAID 10, el primer pas és afegir 4 discos a la màquina, ja que aquests seran els que ens caldran per a aquest RAID.
![raid10_1](https://github.com/ManuelReyes-ITB2425/Projecte-24-25/blob/90ebe3b9e4950c5c37deb1c8e7a7830f2482c180/proyecto/Fotos/part%20teorica/Mario/RAID%2010/Captura%20de%20pantalla%20de%202025-05-26%2008-47-55.png)

Una vegada tenim els 4 discos, creem dos RAIDs de tipus 1.
![raid10_2](https://github.com/ManuelReyes-ITB2425/Projecte-24-25/blob/90ebe3b9e4950c5c37deb1c8e7a7830f2482c180/proyecto/Fotos/part%20teorica/Mario/RAID%2010/Captura%20de%20pantalla%20de%202025-05-26%2008-48-08.png)
![raid10_3](https://github.com/ManuelReyes-ITB2425/Projecte-24-25/blob/90ebe3b9e4950c5c37deb1c8e7a7830f2482c180/proyecto/Fotos/part%20teorica/Mario/RAID%2010/Captura%20de%20pantalla%20de%202025-05-26%2008-48-18.png)

El procediment és el mateix per a l'altre parell de discos, una vegada acabat ens quedaria així:
![raid10_4](https://github.com/ManuelReyes-ITB2425/Projecte-24-25/blob/90ebe3b9e4950c5c37deb1c8e7a7830f2482c180/proyecto/Fotos/part%20teorica/Mario/RAID%2010/Captura%20de%20pantalla%20de%202025-05-26%2008-48-31.png)

Ja per últim, anem a l'eina de Windows per crear i formatar particions i fem clic dret a un dels dos discos i li donem a crear nou volum distribuït, seleccionem tots dos discos i ja tindríem el RAID 10.
![raid10_5](https://github.com/ManuelReyes-ITB2425/Projecte-24-25/blob/90ebe3b9e4950c5c37deb1c8e7a7830f2482c180/proyecto/Fotos/part%20teorica/Mario/RAID%2010/Captura%20de%20pantalla%20de%202025-05-26%2008-48-40.png)

Aquí està l'altre RAID 10 del servidor d'Àudio i streaming que són 2 dels nostres serveis pilars.
![raid10](https://github.com/ManuelReyes-ITB2425/Projecte-24-25/blob/main/proyecto/Fotos/part%20teorica/Silvia/Captura%20de%20pantalla%20de%202025-05-21%2011-56-49.png)

**Prevenció de riscos laborals:**

Risc elèctric: És fonamental que totes les instal·lacions estiguin ben fetes i revisades. No tothom pot manipular els sistemes elèctrics; només personal format i, si cal, amb equips de protecció especials.

Risc d’incendi: Hi ha d'haver detectors que avisin ràpid si hi ha fum. I si hi ha un foc, sistemes que l'apaguin automàticament, normalment amb gasos que no facin malbé els servidors, perquè l'aigua seria un desastre. A més, tothom ha de saber com utilitzar els extintors i per on sortir si hi ha una emergència.

Per últim, l'entorn de treball també compta. S'ha de procurar que no hi hagi cables per terra per evitar ensopegades, i mantenir l'ordre i la neteja. El soroll dels ventiladors i equips s'ha de controlar, i si és molt alt, cal protecció per a les orelles.

**Sostenibilitat primera part:**

**Optimitzar el consum d’energia:**  
El primer pas fonamental és monitoritzar el CPD. D'aquesta manera, podem conèixer amb precisió el seu consum energètic, identificar àrees de millora i implementar mesures per fer-lo més sostenible.

**Ús d’energia verda pel CPD:**  
Una altra mesura important és la utilització d'energia verda. Per exemple, es pot contractar una companyia elèctrica que disposi de tarifes que assegurin el subministrament d'energia provinent de fonts renovables, contribuint així a un CPD més ecològic.

**Estalvi en longitud de cablejat:**  
Per optimitzar la longitud del cablejat i reduir pèrdues i costos, és crucial assegurar-se que la seva disposició sigui òptima. El mètode Top-of-Rack Switching (ToR) és una solució senzilla i eficaç, que consisteix a col·locar commutadors (switches) a la part superior de cada bastidor (rack), minimitzant així la longitud dels cables necessaris. A més, un bon disseny de cablejat estructurat des de l'inici, amb panells de connexió ben ubicats, evita cables innecessàriament llargs i en facilita la gestió i el manteniment.

**Sistemes de circulació d’aire que aprofitin condicions naturals**:  
Per estalviar electricitat en la refrigeració, es pot aplicar el sistema de free-cooling. Aquesta tècnica consisteix a aprofitar l'aire exterior, especialment en llocs amb climes freds o temperatures exteriors favorables en el nostre cas hem escollit Canadà, Nova Zelanda i Islàndia, per refredar les instal·lacions, disminuint la dependència de sistemes de refrigeració mecànica.

**Parada d’equips quan no hi ha càrrega:**  
Es poden configurar els equips de l'empresa, com ara els ordinadors, perquè s'apaguin automàticament després d'un cert període d'inactivitat. Això redueix el consum innecessari fora de les hores de màxima activitat.

#

## 2 Sostenibilitat

**1\. Identificació dels Recursos Emprats:**

- **Infraestructura Física Local (CPD de l'empresa):**
  - **Servidor Windows 1 (AD + BD + DNS primari):** Dell PowerEdge R550 (Intel Xeon Silver 4310, 32GB RAM, 4x1TB SSD RAID10).
  - **Servidor Windows 2 (FTP + DNS secundari):** Dell PowerEdge R250 (Intel Xeon Silver 4314, 32GB RAM, 2x480GB SSD RAID1).
  - **Servidor Ubuntu (Audio + Streaming + Web):** Lenovo ThinkSystem SR630 (Intel Xeon Silver 4210R, 32GB RAM, 4x1TB SSD RAID10).
  - **Equipament de Xarxa Local:** Switch (24p GbE PoE, 4p SFP+), Patch Panel Lanberg. _(Router principal també al CPD, consum estimat prèviament)_.
  - **Infraestructura Elèctrica i Auxiliar CPD Local:** (Doble escomesa, SAIs, PDUs, HVAC - Daikin + Chilldyne, Sensors NetBotz – _els consums d'aquests ja estan detallats a la secció elèctrica_).
- **Infraestructura Física Externa (Offsite):**
  - **Servidor de Còpies:** QNAP TS-453D (Intel Celeron J4125, 4GB RAM, 4xHDD RAID5).
- **Infraestructura Cloud (Total 4 Instàncies Virtuals):**
  - **Servidor Cloud 1 (Rèplica de Windows 1):** Estimació: 4 vCPU, 16GB RAM.
  - **Servidor Cloud 2 (Rèplica de Windows 2):** Estimació: 2 vCPU, 8GB RAM.
  - **Servidor Cloud 3 (Rèplica d'Ubuntu):** Estimació: 4-8 vCPU, 16-32GB RAM.
  - **Servidor Cloud 4 (Firewall):** OPNsense. Estimació: 2 vCPU, 4GB RAM.
- **Serveis Desplegats:** Active Directory, Bases de Dades, DNS, FTP, Web, Streaming d'Àudio/Vídeo, Emmagatzematge de Còpies de Seguretat, Firewall de Xarxa.
- **Protocols Clau:** TCP/IP, HTTP/S, FTP/SFTP, DNS, LDAP, SMB, RTP/RTSP, protocols de seguretat i enrutament.
- **Previsió d'Ús:** 24/7 per a la majoria dels sistemes, tràfic principal per streaming (estimat 9,5 TB/any de sortida), web, FTP, replicacions, i trànsit gestionat pel firewall.

**2\. Estimació del Consum Energètic i la Petjada de Carboni (Anual):**

- **Consum Energètic Infraestructura Física Local (CPD de l'empresa):**
  - Servidor R550 (AD+BD): 155W (típic)
  - Servidor R250 (FTP+DNS): 100W (típic)
  - Servidor SR630 (Ubuntu): 125W (típic)
  - Switch: 90W (típic)
  - Router: 30W (estimat)
  - Sensors NetBotz: 15W (estimat)
  - **Subtotal Equips TI al CPD:** 515W
  - Pèrdues SAIs (sobre 515W, eficiència 95%): ~27,1W
  - **Consum TI + SAIs al CPD:** 542,1W
  - Consum HVAC (Daikin 450W + Chilldyne 4500W): 4950W
  - **Total Consum CPD:** 542,1W + 4950W = **5492,1W**
  - **Consum Anual CPD:** 5492,1W \* 8760h = **48.110,8 kWh/any**.
- **Consum Energètic Infraestructura Física Externa (Offsite):**
  - Servidor QNAP TS-453D (còpies): 26W (mitjana)
  - **Consum Anual QNAP:** 26W \* 8760h = **227,76 kWh/any**.
- **Total Consum Anual Infraestructura Física (Local + Offsite):**
  - 48.110,8 kWh + 227,76 kWh = **48.338,56 kWh/any**.
- **Consum Energètic Instàncies Cloud (4 instàncies):**
  - Cloud 1 (Rèplica Win1): ~0,08 kWh/hora.
  - Cloud 2 (Rèplica Win2): ~0,02 kWh/hora.
  - Cloud 3 (Rèplica Ubuntu): ~0,07 kWh/hora.
  - Cloud 4 (Firewall OPNsense): ~0,01 kWh/hora (basat en 2vCPU, 4GB RAM).
  - **Total Consum Horari Cloud:** 0,08 + 0,02 + 0,07 + 0,01 = 0,18 kWh/hora.
  - **Consum Anual Cloud:** 0,18 kWh/hora \* 8760 hores/any = **1.576,8 kWh/any**.
- **Consum Energètic per Tràfic de Dades (Streaming):**
  - Estimació (0,05 kWh/GB per 9,5TB): **475 kWh/any**.
- **Consum Energètic Total Anual del Projecte:**
  - 48.338,56 kWh (físic) + 1.576,8 kWh (cloud) + 475 kWh (tràfic) = **50.390,36 kWh/any**.
- **Petjada de Carboni Anual Estimada (kg CO2 eq.):**
  - **Infraestructura Física (CPD Local + QNAP Offsite):** 48.338,56 kWh \* 0,19 kgCO2/kWh (factor Espanya) = **9.184,33 kg CO2 eq.**
  - **Instàncies Cloud:** 1.576,8 kWh \* 0,10 kgCO2/kWh (factor regió verda) = **157,68 kg CO2 eq.**
  - **Tràfic de Dades:** 475 kWh \* 0,19 kgCO2/kWh (factor conservador) = **90,25 kg CO2 eq.**
  - **Petjada de Carboni Total Anual:** 9.184,33 + 157,68 + 90,25 = **9.432,26 kg CO2 eq. (≈ 9,43 tones CO2 eq./any)**.

**3\. Proposta de Mesures de Reducció o Optimització:**

- **Prioritat Màxima: Optimització Energètica de la Infraestructura Física Local (CPD):**
    1. **Reavaluació Crítica i Optimització del Sistema HVAC (Chilldyne):** Investigar i ajustar el consum de 4500W a la càrrega tèrmica real (515W TI). Aquesta és la mesura amb MÉS potencial d'estalvi.
    2. **Contractació d'Energia 100% Renovable:** Per al subministrament elèctric del CPD local i, si és possible, per a la ubicació del servidor QNAP offsite (encara que el seu consum és molt menor).
    3. **Monitorització Energètica Detallada del CPD:** PDUs intel·ligents, sensors de consum per a HVAC.
    4. **Optimització del Servidor de Còpies QNAP:** Tot i ser de baix consum, assegurar que utilitza modes de repòs quan no està actiu i que els discos durs són eficients.
    5. **Selecció de Regions Cloud "Verdes".**
- **Estratègies Generals d'Optimització i Sostenibilitat:**
    1. **Compressió de Dades:** Per a trànsit de xarxa i emmagatzematge de còpies.
    2. **Implementació d'Interruptors de Transferència Automàtica (ATS) al CPD:** Per a equips locals amb font única, com es preveia.
    3. **Economia Circular i Conscienciació.**

#

## Comparació d’AWS amb altres proveïdors del núvol

| **Proveïdor** | **Eficiència Energètica i Sostenibilitat** | **Solucions de CPD Administrats** | **Cobertura dels Requeriments (seguretat, escalabilitat, sostenibilitat)** |
| --- | --- | --- | --- |
| **Amazon Web Services (AWS)** | \-Té compromís per operar amb un 100% d’energia renovable per al 2025.<br><br>\- Data centers amb disseny eficient en refrigeració natural i ús d’energia solar i eòlica.<br><br>\- Índex PUE (Power Usage Effectiveness) molt baix (al voltant de 1.1-1.2). | \- Ofereix serveis com Amazon EC2, S3, RDS amb gestió completa.<br><br>\- Servei de migració i monitoratge del CPD.<br><br>\- Infraestructura robusta amb alta seguretat física i digital. | \- Compliment amb normes ISO 27001, SOC 2, GDPR.<br><br>\- Control d’accés físic i lògic estricte.<br><br>\- Arquitectures flexibles i segures.<br><br>\- Eficient i sostenible. |
| --- | --- | --- | --- |
| **Microsoft Azure** | \- Compromís per ser 100% renovable el 2025.<br><br>\- Ús intensiu de refrigeració per evaporació i dissenys amb alta eficiència PUE.<br><br>\- Programes de compensació d’emissions de carboni. | \- Azure Virtual Machines, Azure Storage, Azure SQL.<br><br>\- Solucions híbrides i multi-núvol.<br><br>\- Monitoratge i gestió automatitzada del CPD. | \- Certificacions com ISO 27001, SOC 1 i 2, HIPAA.<br><br>\- Seguretat avançada amb control d’accés multilayer.<br><br>\- Enfocament en sostenibilitat i compliment normatiu. |
| --- | --- | --- | --- |
| **Google Cloud Platform (GCP)** | \- Operació ja amb un 100% d’energia renovable des de 2017.<br><br>\- Innovacions en refrigeració líquida i intel·ligència artificial per optimitzar consum.<br><br>\- Data centers amb PUE molt baix. | \- Compute Engine, Cloud Storage, BigQuery.<br><br>\- Gestiona CPD i ofereix eines d’automatització.<br><br>\- Infraestructura amb alta disponibilitat i seguretat. | \- Compliment amb GDPR, HIPAA, ISO.<br><br>\- Controls d’accés rigorosos i auditables.<br><br>\- Sostenibilitat integrada en la planificació d’infraestructures. |
| --- | --- | --- | --- |
| **IBM Cloud** | \- Focalitzat en solucions híbrides amb optimització energètica.<br><br>\- Ús de tecnologies de refrigeració avançada i energètica verda. | \- Infraestructura gestionada i serveis cloud híbrids.<br><br>\- Seguretat física i virtual robusta.<br><br>\- Ofereix CPD dedicats i multitenant. | \- Compliment normatiu global.<br><br>\- Arquitectura segura i flexible.<br><br>\- Projectes amb orientació sostenible. |
| --- | --- | --- | --- |

# 3 Serveis

**Àudio i streaming**

El primer és instal·lar el icecast2

![Audio](https://github.com/ManuelReyes-ITB2425/Projecte-24-25/blob/main/proyecto/Fotos/part%20teorica/Silvia/Captura%20de%20pantalla%20de%202025-05-21%2009-24-11.png)

El icecast2 funciona perfectament amb el port 8000

![Icecastweb](https://github.com/ManuelReyes-ITB2425/Projecte-24-25/blob/main/proyecto/Fotos/part%20teorica/Silvia/Captura%20de%20pantalla%20de%202025-05-21%2009-28-56.png)

S’ha modificat el kernel a un Linux genèric, perquè el que tenia era d'AWS, per la qual cosa el darkice no funcionava perquè necessita una targeta de so, i per això també instal·li un mòdul snd-aloop, que és una targeta de so virtual.

![Kernel](https://github.com/ManuelReyes-ITB2425/Projecte-24-25/blob/main/proyecto/Fotos/part%20teorica/Silvia/Captura%20de%20pantalla%20de%202025-05-21%2011-32-48.png)

Fitxer de configuració de darkice.cfg

![darkice](https://github.com/ManuelReyes-ITB2425/Projecte-24-25/blob/main/proyecto/Fotos/part%20teorica/Silvia/darkice.png)

Aquí està la comprovació que sí que reprodueix so en el punt de muntatge /live.mp3

![live](https://github.com/ManuelReyes-ITB2425/Projecte-24-25/blob/main/proyecto/Fotos/part%20teorica/Silvia/Captura%20de%20pantalla%20de%202025-05-21%2011-38-56.png)

![live](https://github.com/ManuelReyes-ITB2425/Projecte-24-25/blob/main/proyecto/Fotos/part%20teorica/Silvia/Captura%20de%20pantalla%20de%202025-05-21%2011-34-19.png)

En streaming el que vam fer va ser instal·lar el gstreamer per a compartir un vídeo a un client. El servidor envia amb aquesta comanda _“gst-launch-1.0 -v filesrc location=/home/ubuntu/hola.mp4 ! decodebin ! x264enc tune=zerolatency ! rtph264pay ! udpsink host=52.202.226.208 port=5000”_

el client rep així “_gst-launch-1.0 -v \\_

_udpsrc port=5000 caps="application/x-rtp, media=video, encoding-name=H264, payload=96" ! \\_

_rtph264depay ! avdec_h264 ! videoconvert ! xvimagesink”_
![stream](https://github.com/ManuelReyes-ITB2425/Projecte-24-25/blob/main/proyecto/Fotos/part%20teorica/Silvia/Captura%20de%20pantalla%20de%202025-05-22%2008-55-30.png)

També comprovem l'amplada de banda.

Servidor _“iperf3 -s”_, client _“iperf3 -c 52.202.226.208”_

![banda](https://github.com/ManuelReyes-ITB2425/Projecte-24-25/blob/main/proyecto/Fotos/part%20teorica/Silvia/Captura%20de%20pantalla%20de%202025-05-21%2009-42-02.png)



**Web** 

El servei tracta de donar allotjament a pàgines web, per fer això hem utilitzat l’eina nginx que comporta d’una configuració bàsica per a la connexió http i també una configuració per a https amb el nostre certificat.

![Conf. http](https://github.com/ManuelReyes-ITB2425/Projecte-24-25/blob/main/proyecto/Fotos/serveis/Silvia%20Web/Captura%20de%20pantalla%20de%202025-05-22%2010-19-30.png)
![Conf. https](https://github.com/ManuelReyes-ITB2425/Projecte-24-25/blob/main/proyecto/Fotos/serveis/Silvia%20Web/Captura%20de%20pantalla%20de%202025-05-22%2010-20-26.png)

Visió del certificat: 
![Cert. 1](https://github.com/ManuelReyes-ITB2425/Projecte-24-25/blob/main/proyecto/Fotos/serveis/Silvia%20Web/Captura%20de%20pantalla%20de%202025-05-22%2010-07-07.png)
![Cert. 2](https://github.com/ManuelReyes-ITB2425/Projecte-24-25/blob/main/proyecto/Fotos/serveis/Silvia%20Web/Captura%20de%20pantalla%20de%202025-05-22%2010-10-44.png)

Disseny de la nostra pàgina web i clients del nostre servei.
![Index.html](https://github.com/ManuelReyes-ITB2425/Projecte-24-25/blob/main/proyecto/Fotos/serveis/Silvia%20Web/Captura%20de%20pantalla%20de%202025-05-22%2010-26-32.png)

Visió de la web: 
![Web IP](https://github.com/ManuelReyes-ITB2425/Projecte-24-25/blob/main/proyecto/Fotos/serveis/Silvia%20Web/Captura%20de%20pantalla%20de%202025-05-23%2008-33-48.png)

També tenim la web publicada utilitzant el nostre DNS. 
![Web DNS](https://github.com/ManuelReyes-ITB2425/Projecte-24-25/blob/main/proyecto/Fotos/serveis/Silvia%20Web/Captura%20de%20pantalla%20de%202025-05-23%2008-34-41.png)

**BBDD**

Per a la base de dades, hem fet servir MySQL Workbench, que ens facilita la gestió de totes les nostres dades, i phpMyAdmin per accedir-hi des de qualsevol dispositiu.
![BD1](https://github.com/ManuelReyes-ITB2425/Projecte-24-25/blob/90ebe3b9e4950c5c37deb1c8e7a7830f2482c180/proyecto/Fotos/serveis/BBDD/Captura%20de%20pantalla%20de%202025-05-26%2008-59-52.png)

Totes les nostres taules tenen una gran quantitat de dades
![BD2](https://github.com/ManuelReyes-ITB2425/Projecte-24-25/blob/90ebe3b9e4950c5c37deb1c8e7a7830f2482c180/proyecto/Fotos/serveis/BBDD/Captura%20de%20pantalla%20de%202025-05-26%2009-00-03.png)

Hem afegit totes les relacions segons aquest esquema i tenint en compte que codi_departament i codi_nivell són claus foranes.
![BD3](https://github.com/ManuelReyes-ITB2425/Projecte-24-25/blob/90ebe3b9e4950c5c37deb1c8e7a7830f2482c180/proyecto/Fotos/serveis/BBDD/Captura%20de%20pantalla%20de%202025-05-26%2009-00-16.png)

Comprovació que des d'un client puc veure la Base de dades i Administrar-la.

![BD4](https://github.com/ManuelReyes-ITB2425/Projecte-24-25/blob/main/proyecto/Fotos/part%20teorica/Silvia/Captura%20de%20pantalla%20de%202025-05-26%2009-46-05.png)

**Monitoratge**

Per al monitoratge hem utilitzat dues aplicacions, Speccy per al rendiment i Veyon per monitoritzar els usuaris, fins i tot controlar les seves màquines o bloquejar-les a distància.

**Speecy**



**Veyon**



**Active Directory**

Hem instal·lat Active Directory al Windows Server i hem creat un parell d'usuaris per simular l'entorn de l'empresa. A més, tenim un servei de còpia de seguretat que té el DNS replicat i també l'Active Directory, igual que la resta de coses.

![ad](https://github.com/ManuelReyes-ITB2425/Projecte-24-25/blob/main/proyecto/Fotos/part%20teorica/Silvia/AD.png)

Hem connectat un PC client des de Virtualbox.

![ad](https://github.com/ManuelReyes-ITB2425/Projecte-24-25/blob/main/proyecto/Fotos/part%20teorica/Silvia/Captura%20de%20pantalla%20de%202025-05-26%2009-12-32.png)

![AD](https://github.com/ManuelReyes-ITB2425/Projecte-24-25/blob/main/proyecto/Fotos/part%20teorica/Silvia/Captura%20de%20pantalla%20de%202025-05-26%2009-13-03.png)

També el client hem instal·lat RSAT per a poder administrar el servidor que està en el núvol.

![Rsat](https://github.com/ManuelReyes-ITB2425/Projecte-24-25/blob/main/proyecto/Fotos/part%20teorica/Silvia/RSat.png)

![Rsat](https://github.com/ManuelReyes-ITB2425/Projecte-24-25/blob/main/proyecto/Fotos/part%20teorica/Silvia/Clientrsat.png)

**DNS**

Al DNS tenim la zona del domini i també les dels serveis web d'àudio i de vídeo.


Totes les zones estan configurades amb les IPs públiques corresponents.


**SFTP**

Oferim el servei de SFTP per la transferència d’arxius de forma segura. Creem els usuaris necessaris per als usuaris que ho utilitzaran i donem aquest servei utilitzant SolarWinds.

Configuració d'usuaris:

![usuaris](https://github.com/ManuelReyes-ITB2425/Projecte-24-25/blob/main/proyecto/Fotos/serveis/Manel%20FTP/Captura%20de%20pantalla%20de%202025-05-20%2013-08-52.png)

Configuració del FTP amb el IIS:

![usuaris](https://github.com/ManuelReyes-ITB2425/Projecte-24-25/blob/main/proyecto/Fotos/serveis/Manel%20FTP/Captura%20de%20pantalla%20de%202025-05-21%2010-37-51.png)
Configuració SolarWinds per SFTP:

![usuaris](https://github.com/ManuelReyes-ITB2425/Projecte-24-25/blob/main/proyecto/Fotos/serveis/Manel%20FTP/Captura%20de%20pantalla%20de%202025-05-23%2009-15-05.png)

Resultat final:

![usuaris](https://github.com/ManuelReyes-ITB2425/Projecte-24-25/blob/main/proyecto/Fotos/serveis/Manel%20FTP/Captura%20de%20pantalla%20de%202025-05-22%2009-38-54.png)

