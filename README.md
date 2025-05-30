![portada](https://github.com/ManuelReyes-ITB2425/Projecte-24-25/blob/main/proyecto/Fotos/part%20teorica/Manel/portada%20projecte.png)




# INDEX
## Índex
- [**Resum del projecte**](#resum-del-projecte)
- [**1 Proposta de CPD**](#1-proposta-de-cpd)
  - [1.1 Ubicació física](#11-ubicació-física)
  - [1.2 Infraestructura IT](#12-infraestructura-it)
  - [1.3 Infraestructura elèctrica](#13-infraestructura-elèctrica)
  - [1.4 Seguretat Física](#14-seguretat-física)
  - [1.5 Seguretat Lògica](#15-seguretat-lògica)
  - [1.6 Implementació a AWS](#16-implementació-a-aws)
  - [1.7 Comparació d’AWS amb altres proveïdors del núvol](#17-comparació-daws-amb-altres-proveïdors-del-núvol)
- [**2 Sostenibilitat**](#2-sostenibilitat)
- [**3 Serveis**](#3-serveis)




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

En el nostre cas, la infraestructura física principal, que allotjarà els 3 servidors físics locals, estarà ubicada en una oficina a Sant Cugat en carrer Rubí 102, instal·lat en una planta intermèdia. Aquesta infraestructura es complementarà amb tres servidors addicionals ubicats al núvol, distribuïts estratègicament pels proveïdors de cloud per optimitzar el rendiment i garantir la seguretat de les dades.

Per tant, hem de tenir en compte la ubicació física dels nostres servidors per poder aplicar un sistema de climatització adaptat per a aquest lloc. Podem aplicar diferents sistemes per poder controlar-ho; aplicarem els sistemes HVAC, que s’encarregarà de controlar la temperatura, ventilació i qualitat de l’aire. A més, per millorar l’eficiència energètica, podem utilitzar sistemes de free-cooling si les condicions climàtiques locals ho permeten en certs períodes. Per als servidors al núvol, la climatització és gestionada directament pel proveïdor del servei.


Pel que fa a la sala física, hem d’aplicar mesures per dificultar la identificació i accés, millorant la seguretat. La ubicació dins de l'oficina és essencial; és preferible ubicar-lo en plantes intermèdies i evitar plantes baixes per risc d’accessos no autoritzats i evitar també plantes superiors per l’exposició a condicions ambientals adverses. A més, de no tenir cap finestra ni senyalització evident que indiquin la ubicació o situació del CPD. El disseny de la sala també és important; utilitzarem portes i parets que no es distingeixen de la resta de l'edifici. Hem d’utilitzar materials que no destaquin i que siguin resistents per mantenir la discreció i seguretat. També tindrem rutes d’accessos no evidents que no estiguin connectades amb accessos principals.

![sala](https://github.com/ManuelReyes-ITB2425/Projecte-24-25/blob/main/proyecto/Fotos/part%20teorica/Manel/Captura%20de%20pantalla%20de%202025-05-21%2012-09-15.png) 

Per un altre costat, la distribució i gestió del cablejat per als servidors físics, la seva connexió a la xarxa i als serveis al núvol requereix atenció. És important escollir el cablejat correcte. Per connexions internes dins del CPD del lloc adaptat, utilitzarem fibra òptica monomode, ideal per llargues distàncies dins del CPD. També el cablejat estructurat Cat 7 per les connexions de servidors dins de la instal·lació, assegurant velocitats de 10 Gbps.

A causa de la necessitat de connectar-nos de manera fiable i eficient amb els servidors al núvol, utilitzarem una configuració de xarxa robusta. Això implica connexions a Internet d'alta capacitat i, potencialment, l'ús de tecnologies com SD-WAN o connexions dedicades als proveïdors de núvol, buscant principis similars als que oferirien les xarxes de fibra òptica submarina i el protocol MPLS en un escenari de múltiples CPDs físics internacionals (baixes latències i alta fiabilitat).

També, hem de separar el cablejat a la instal·lació i distribuir-lo d’una manera eficient per evitar interferències electromagnètiques, també etiquetant el cablejat per facilitar el manteniment. Hem d'assegurar també rutes alternatives de connexió a la xarxa per mantenir la connectivitat en cas de fallada.

Per optimitzar la gestió del CPD, es disposarà de terra tècnic, que permetrà la canalització del cablejat i dels sistemes de climatització de forma segura i flexible. També el sostre tècnic, per facilitar la instal·lació d’equips de ventilació, il·luminació i distribució d’aire.

Per últim, els racks per als servidors físics a Sant Cugat. Utilitzarem racks tancats, per tenir seguretat i control ambiental i d’accés. A la ubicació tindrem els racks necessaris per als 3 servidors en funcionament, amb un NAS a casa d’un treballador. Tots tenen patch panel per gestionar el cablejat, Routers i Switches.


Organització cablejat:

![cables](https://github.com/ManuelReyes-ITB2425/Projecte-24-25/blob/main/proyecto/Fotos/part%20teorica/Manel/Captura%20de%20pantalla%20de%202025-05-21%2012-11-46.png)

#

## 1.2 Infraestructura IT

La infraestructura requerirà un total de 4 servidors físics locals i 3 instàncies al núvol, amb l'objectiu de garantir l'alta disponibilitat, redundància, rendiment òptim i seguretat de les dades i serveis.

**Servidors locals**

**Servidor Windows 1 → AD + BD + Monitoratge**

[**Enllaç**](https://www.dell.com/es-es/shop/servidores-almacenamiento-y-redes/servidor-de-montaje-en-rack-poweredge-r550/spd/poweredge-r550/per5503a?configurationid=63a9139a-95e8-4626-8238-84ce2cb6448e)**:**

- **Model**: Dell PowerEdge R550
- **CPU**: Intel Xeon Silver 4310 (12 nuclis / 24 fils)
- **RAM**: 32 GB RDIMM, 3200 MT/s
- **Emmagatzematge**: 4 × 1TB SSD SATA en RAID 10
- **Xarxa**: 10GbE SFP+

**Servidor Windows 2 → FTP + DNS**

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

- 24 ports Gigabit (PoE)  

- 4 ports SFP+ per a uplinks de 10 GbE  

- Gestió avançada (QoS, VLANs, spanning-tree, etc.)  

- Compatible amb Cat.7

**Instàncies Cloud**

Hem desplegat 3 instàncies virtuals al núvol, cada una corresponent a un dels servidors principals locals:

- **Servidor Cloud 1**: Replica de Windows 1 (AD + BD + Monitoratge)
- **Servidor Cloud 2**: Replica de Windows 2 (FTP + DNS)  
- **Servidor Cloud 3**: Replica del servidor Ubuntu (streaming, audio i web)
- **Servidor Cloud 4:** Firewall

**Planell dels racks**

La nostra infraestructura està formada per tres racks interconnectats. Cada rack disposa d’un patch panel i un servidor, mentre que al rack central s’hi ubiquen el switch i el router, que actuen com a elements principals de gestió i distribució del trànsit de dades.

Els cables verds indiquen les connexions entre els servidors i els patch panels, mentre que els cables blaus mostren les interconnexions entre els diferents patch panels, que permeten establir comunicació entre els tres racks. Aquestes connexions acaben centralitzant-se al switch. El router, connectat a aquest, és l’encarregat de facilitar la connexió amb xarxes externes.

![Rack](https://github.com/ManuelReyes-ITB2425/Projecte-24-25/blob/main/proyecto/Fotos/part%20teorica/Silvia/Captura%20de%20pantalla%20de%202025-05-20%2009-10-14.png)
#

**1.3 Infraestructura elèctrica**

**Descripció general:**

**1. Alimentació elèctrica redundant.**

La infraestructura elèctrica del nostre Centre de Processament de Dades (CPD) ha estat meticulosament dissenyada per assegurar un alt nivell de disponibilitat, continuïtat de servei i eficiència energètica, adaptant-se a les necessitats operatives actuals i preveient l'escalabilitat futura. El disseny fonamental es basa en la redundància de les fonts d'alimentació principals i la protecció mitjançant Sistemes d'Alimentació Ininterrompuda (SAI) per als equips de Tecnologies de la Informació (TI) i sistemes crítics auxiliars.

**2. Sistema de Subministrament Elèctric Principal:**

Cada seu física del CPD compta amb una instal·lació elèctrica robusta, alimentada per dues escomeses elèctriques independents (Feed A i Feed B) provinents de la xarxa pública. Aquestes escomeses alimenten un Quadro General de Distribució (QGD) central, que actua com a nucli per a la distribució de l'energia dins de les instal·lacions. Aquesta configuració de doble escomesa minimitza el risc d'interrupcions totals del servei degudes a fallades en una de les línies de subministrament extern.

**3. Línies d'Alimentació Redundants (Línia A i Línia B) i Sistemes SAI:**

Des del QGD, l'energia es canalitza cap a dos circuits elèctrics principals i independents, denominats Línia A i Línia B. Cada una d'aquestes línies alimenta un Sistema d'Alimentació Ininterrompuda (SAI) dedicat (SAI A i SAI B). Aquests SAI estan dimensionats per:

- Proporcionar energia filtrada i estabilitzada als equips sensibles.
- Garantir una autonomia mínima de 20 minuts a plena càrrega operativa dels equips de IT connectats, cosa que permet un apagat controlat dels sistemes en cas d'interrupció prolongada del subministrament extern.

Per aconseguir l’autonomia mínima que volem que proporcioni el SAI, necessitarem diverses dades que necessiten valoració primer. Per al dimensionament adequat dels Sistemes d'Alimentació Ininterrompuda (SAI), és crucial estimar de manera realista el consum energètic de cada component de la infraestructura IT. A continuació, es detalla el procés i les consideracions per a determinar la càrrega aportada pels servidors i els diferents components que engloben la infraestructura elèctrica, destinat a allotjar els diferents serveis.

Aquesta és la fórmula per aconseguir quant temps d’autonomia duraria el SAI amb una bateria de capacitat coneguda:

t_a = (C_n * V_b_total * η_inv * DoD * f_p(I_d) * f_t(T) * f_e * f_c) / P_L	

Al nostre CPD volem un temps mínim de 20 minuts, per tant, necessitarem calcular la capacitat nominal de la bateria requerida per aconseguir el temps desitjat. La fórmula seria doncs:

C_n = (P_L \* t_a) / (V_b_total * η_inv * DoD * f_p(I_d) \* f_t(T) * f_e * f_c)

Per al dimensionament adequat dels Sistemes d'Alimentació Ininterrompuda (SAI), s'ha estimat el consum energètic operatiu de cada component crític que serà alimentat per aquests. La metodologia emprada consisteix a partir del consum màxim teòric de cada equip, basant-se en les especificacions documentades per a la configuració del projecte, i aplicar un Factor de Càrrega Operativa Estimada (FCOE) per reflectir la càrrega sostinguda esperada durant els 20 minuts d'autonomia requerits.

**Servidor Dell PowerEdge R550 (AD + BD + Monitoratge)**

- Consum Màxim Teòric del Servidor: S'estableix en 300 Watts. Aquest valor es basa en les estimacions prèvies per a la configuració definida al projecte i representa el pic màxim de consum previst per al sistema configurat.
- Factor de Càrrega Operativa Estimada (FCOE): 60% (0,60). Aquest factor es justifica per:
  - La naturalesa dels serveis (AD, BD, Monitoratge), que, tot i ser crítics, rarament operen al 100% de la capacitat màxima de tots els components de forma sostinguda.
- Càlcul del Consum Operatiu:

  Consum_Operatiu_R550 = 300 W * 0,60 = 180 Watts (total)

- Distribució als SAI: El R550 compta amb dues fonts d'alimentació redundants que comparteixen la càrrega.
  - Càrrega per al SAI A (via PSU1): 90 Watts
  - Càrrega per al SAI B (via PSU2): 90 Watts

**Servidor Dell PowerEdge R250 (FTP + DNS)**

- Consum Màxim Teòric del Servidor: S'estableix en 200 Watts. Factor de Càrrega Operativa Estimada (FCOE): 50% (0,50). Aquest factor es justifica per:
  - Els serveis d'FTP i DNS tenen una demanda de recursos generalment moderada.
  - Una càrrega del 50% sobre el màxim teòric es considera una estimació conservadora però adequada per a la seva operació contínua durant una contingència.
- Càlcul del Consum Operatiu:

  Consum_Operatiu_R250 = 200 W * 0,50 = 100 Watts

- Distribució als SAI: El R250 compta amb una única font d'alimentació.
  - Càrrega per al SAI A: 100 Watts

**Servidor Lenovo ThinkSystem SR630 (Àudio + Streaming + Web)**

- Consum Màxim Teòric del Servidor: S'estableix en 250 Watts. Factor de Càrrega Operativa Estimada (FCOE): 70% (0,70). Aquest factor es justifica per:
  - La potencial alta demanda dels serveis de streaming i web, que podrien requerir un percentatge significatiu dels recursos del servidor de forma sostinguda.
- Càlcul del Consum Operatiu:

  Consum_Operatiu_SR630 = 250 W * 0,70 = 175 Watts

- Distribució als SAI: S'ha definit que el SR630 comptarà amb una única font d'alimentació.
  - Càrrega per al SAI B: 175 Watts

**Switch HPE Aruba 2930F 24G PoE+**

- Consum Màxim Teòric del Switch (sense lliurar PoE): S'estableix en 75 Watts. Aquest valor s'obté de les especificacions del fabricant, restant la potència total PoE (370W) del consum màxim total d'energia del switch (445W), donant com a resultat el consum màxim de l'electrònica pròpia del switch.
- Factor de Càrrega Operativa Estimada (FCOE): 80% (0,80). Aquest factor es justifica per:
  - El switch estarà gestionant tot el tràfic de xarxa dels servidors i altres dispositius connectats, requerint un alt percentatge de la seva capacitat operativa de forma contínua.
  - No es considera càrrega PoE crítica a alimentar per aquest switch durant la contingència.
- Càlcul del Consum Operatiu:\

  Consum_Operatiu_Switch = 75 W * 0,80 = 60 Watts

- Distribució als SAI: El switch compta amb una única font d'alimentació.
  - Càrrega per al SAI A: 60 Watts

**Router (Ubiquiti EdgeRouter 4 - ER-4)**

- Consum Màxim Teòric del Router: S'estableix en 13 Watts, segons les especificacions oficials del fabricant per al model ER-4.
- Factor de Càrrega Operativa Estimada (FCOE): 80% (0,80). Similar al switch, el router gestionarà tràfic de xarxa de forma contínua, inclosa la connexió a Internet i la intercomunicació entre xarxes si s'escau.
- Càlcul del Consum Operatiu:\

  Consum_Operatiu_Router = 13 W * 0.80 = 10,4 Watts

  Arrodonit a: 11 Watts (per a una xifra més realista).

- Distribució als SAI: El router compta amb una única font d'alimentació.
  - Càrrega per al SAI B: 11 Watts

**Resum Final de Càrregues Estimades per SAI:**

- **SAI A:**
  - Del Servidor R550 (PSU1): 90 W
  - Del Servidor R250: 100 W
  - Del Switch HPE Aruba: 60 W
  - Total Càrrega Estimada SAI A = 90 + 100 + 60 = 250 Watts
- **SAI B:**
  - Del Servidor R550 (PSU2): 90 W
  - Del Servidor SR630 (1 PSU): 175 W
  - Del Router Ubiquiti ER-4: 11 W
  - Total Càrrega Estimada SAI B = 90 + 175 + 11 = 276 Watts

A continuació, continuarem amb una taula per després procedir amb els càlculs per aconseguir el temps d’autonomia desitjat.

**Fase 1: Taula Consolidada de Paràmetres per al Càlcul Teòric d'Autonomia**

Aquesta taula resumirà totes les dades que hem recopilat pel càlcul final.

**Taula de Paràmetres per al Càlcul Teòric d'Autonomia del SAI APC SMTL1500RMI3UC**

|**Paràmetre**|**Símbol**|**Valor Assignat**|**Unitats**|**Font / Mètode d'Obtenció o Estimació**|
| :- | :- | :- | :- | :- |
|**Càrregues de Disseny (amb marge de seguretat del 25%)**|||||
|Potència Càrrega SAI A|P_L_SAI_A|312,5|W|Consum total estimat dels equips connectats al SAI A (250W) + 25% marge.|
|Potència Càrrega SAI B|P_L_SAI_B|345|W|Consum total estimat dels equips connectats al SAI B (276W) + 25% marge.|
|**Paràmetres Estimats de la Bateria i SAI**||||Estimacions per al model APC SMTL1500RMI3UC|
|Voltatge Nominal Total del Banc de Bateries|V_b_total|48|V|Estimació basada en models de SAIs de liti-ió APC similars en aquest rang de potència.|
|Eficiència de l'Inversor (mode bateria)|η_inv|0,90|(0-1)|Estimació conservadora per a un SAI Line Interactive modern amb tecnologia de liti, considerant pèrdues en la conversió DC-AC.|
|Factor de Peukert (Liti-ió, descàrrega ràpida)|f_p(I_d)|0,95|(<=1)|Estimació per a bateries de liti-ió, reflectint una pèrdua de capacitat del 5% a altes taxes de descàrrega. L'efecte Peukert és menor que en plom-àcid.|
|**Dada de Referència del Fabricant (per calibració)**|||||
|Potència de Càrrega de Referència (Fabricant)|P_L_ref|350|W|Punt extret del gràfic d'autonomia d'APC per a l'SMTL1500RMI3UC.|
|Temps d'Autonomia de Referència (Fabricant)|t_a_ref|21 min 50 seg|min|Punt extret del gràfic d'autonomia d'APC per a l'SMTL1500RMI3UC (equivalent a 0.4167 hores).|
|**Paràmetres de Disseny Operatiu (Definits pel Projecte)**|||||
|Profunditat de Descàrrega (DoD) permesa|DoD|0,90|(0-1)|Decisió de disseny per optimitzar la longevitat de la bateria de liti.|
|Factor de Temperatura|f_t(T)|1,0||Assumint operació del CPD en condicions de temperatura òptimes (20-25°C).|
|Factor d'Envelliment (SAI nou)|f_e|1,0|(<=1)|Càlcul per a un SAI nou amb bateries a la seva capacitat inicial.|
|Factor d'Eficiència del Cablejat Intern DC|f_c|0,99|(<=1)|Estimació per a pèrdues mínimes (1%) en el circuit de corrent continu intern del SAI.|
|**Valor Calculat (Derivat)**|||||
|Capacitat Nominal Estimada de la Bateria|C_n|3,10 Ah|Ah|Calculada a partir de E_lliurada_ref i els paràmetres estimats (V_b_total, η_inv, f_p(I_d)). Veure detall del càlcul a la Fase 2.|
|Energia Nominal Estimada del Banc (C_n*V_b_total)|E_bat_nom|48V|Wh|Producte de C_n estimada i V_b_total estimada.|

**Fase 2: Justificació i Càlcul Detallat dels Paràmetres**

**Introducció al Càlcul Teòric:**\

L'objectiu d'aquest apartat és realitzar un càlcul teòric detallat per determinar l'autonomia esperada del SAI APC SMTL1500RMI3UC. Per a això, s'utilitzarà la fórmula general de descàrrega de bateries, desglossant i justificant cada paràmetre. Atès que el fabricant no proporciona directament tots els valors interns de la bateria (com la capacitat en Ah), es realitzarà una estimació d'aquests a partir de dades de rendiment publicades.

La fórmula general per al temps d'autonomia (t_a) en hores és:

t_a = (C_n * V_b_total * η_inv * DoD * f_p(I_d) * f_t(T) * f_e * f_c) / P_L

**Desglossament i Obtenció de Paràmetres:**

- **Potència de la Càrrega:** Les potències de disseny són P_L_SAI_A = 312,5 W i P_L_SAI_B = 345 W. Aquests valors representen la càrrega operativa màxima esperada per a cada SAI, incloent-hi un marge de seguretat del 25% sobre el consum estimat dels equips connectats. Aquest marge preveu possibles pics de consum i un creixement futur moderat.
- **Estimació de V_b_total (Voltatge Nominal del Banc de Bateries):**\ El datasheet de l'SMTL1500RMI3UC no especifica directament el voltatge del seu banc intern de bateries de liti-ió. Basant-se en l'anàlisi de productes similars d'APC dins de la mateixa família Smart-UPS Lithium-ion i rang de potència (750VA-1500VA), s'observa que un voltatge de sistema de **48V** és una configuració comuna. Per tant, s'adopta V\\_b\\_total = 48V com una estimació fonamentada per a aquest model.

- **Estimació de η_inv (Eficiència de l'Inversor en Mode Bateria):**\ L'eficiència de conversió DC-AC de l'inversor quan opera en mode bateria és un factor crucial. Els SAI porten Line Interactive moderns amb components d'alta qualitat, especialment aquells amb bateries de liti, solen presentar bones eficiències. En absència d'una corba d'eficiència específica per al mode bateria al datasheet, s'estima una eficiència del **90% (0,90)**. Aquesta xifra es considera una estimació realista i lleugerament conservadora, tenint en compte les pèrdues presents al procés de conversió d'energia.
- **Estimació de f_p(I_d) (Factor de Peukert per a Liti-ió):**\ L'efecte Peukert descriu la reducció de la capacitat efectiva d'una bateria a mesura que augmenta la taxa de descàrrega. Per a les bateries de liti-ió, aquest efecte és significativament menys pronunciat que per a les tradicionals de plom-àcid. Per a les taxes de descàrrega associades a autonomies en el rang de 15-60 minuts, s'estima un factor de Peukert de **0,95**. Això implica que s'espera poder utilitzar el 95% de la capacitat nominal de la bateria sota aquestes condicions, reflectint una pèrdua de només el 5% deguda a la rapidesa de la descàrrega.
- **Càlcul de C_n (Capacitat Nominal Estimada de la Bateria):**

[[![](https://github.com/ManuelReyes-ITB2425/pro-asixc1b-g4/blob/main/proyecto/Fotos/part%20teorica/Gerson/image%20(1).png?raw=true)

Per estimar C_n, s'utilitzarà un punt de referència del gràfic d'autonomia proporcionat per APC per a l'SMTL1500RMI3UC: a una càrrega de P_L_ref = 350 W, el SAI ofereix una autonomia de t_a_ref = 21 minuts 50 segons.

Convertim t_a_ref a hores: 21 minuts + (50/60) minuts = 21,8333 minuts.

t_a_ref_hores = 21,8333 / 60 ≈ 0,36388 hores. L'energia lliurada a la càrrega en aquest punt (E_lliurada_ref) és:

E_lliurada_ref = P_L_ref * t_a_ref_hores = 350 W * 0,36388 h ≈ 127,358 Wh.

Aquesta energia lliurada és el resultat de l'energia nominal de la bateria afectada per l'eficiència de l'inversor i l'efecte Peukert (assumint que els altres factors com DoD, ja considerats pel fabricant en aquest punt de referència per a una bateria nova).\

L'energia nominal del banc de bateries (E_bat_nom = C_n * V_b_total) es pot estimar com:\

E_bat_nom = E_lliurada_ref / (η_inv * f_p(I_d))

E_bat_nom = 127,358 Wh / (0,90 * 0,95) = 127,358 Wh / 0,855 ≈ 148,957 Wh. \

Amb el V_b_total estimat de 48V, la capacitat nominal C_n es calcula com:\

C_n = E_bat_nom / V_b_total = 148,957 Wh / 48V ≈ 3,103 Ah.

Arrodonim C_n a **3,10 Ah** per als càlculs següents.\

Aquesta C_n de 3,10 Ah és la capacitat nominal estimada del banc de bateries de 48V que, sota les eficiències i factors estimats, pot lliurar l'autonomia especificada pel fabricant.

Llavors, E_bat_nom recalculat amb C_n arrodonit: 3,10 Ah * 48V = 148,8 Wh.

- **Profunditat de Descàrrega Operativa:** Per a aquest projecte, s'estableix un DoD màxim del **90% (0,9)**. Aquesta és una decisió de disseny per no portar la bateria al seu límit absolut de descàrrega en cada cicle, buscant un equilibri entre l'aprofitament de l'energia i la promoció d'una vida útil més llarga, tot i que les bateries de liti-ió són robustes davant descàrregues profundes.
- Com s'ha detallat a la taula, s'assignen valors d'**1,0**, **1,0** i **0,99** respectivament, reflectint condicions operatives òptimes, un SAI nou i pèrdues mínimes per cablejat intern.

**Fase 3: Càlcul Teòric Manual de l'Autonomia**

Ara, amb tots els paràmetres definits i justificats, calculem l'energia neta lliurable i, posteriorment, el temps d'autonomia.

**1. Càlcul de l'Energia Neta Lliurable Planificada**\

Aquest valor representa l'energia total en Watt-hores que s'espera que el SAI pugui lliurar a la càrrega, considerant tots els factors:\

E_neta_lliurable_Wh = C_n * V_b_total * η_inv * DoD * f_p(I_d) * f_t(T) * f_e * f_c

Utilitzant C_n = 3,10 Ah i V_b_total = 48V (que dóna E_bat_nom = 148,8 Wh):

E_neta_lliurable_Wh = (3,10 Ah) * (48 V) * (0,90) * (0,90) * (0,95) * (1,0) * (1,0) * (0,99)

E_neta_lliurable_Wh = (148,8 Wh) * (0,90) * (0,90) * (0,95) * (1,0) * (1,0) * (0,99)

Calculem pas a pas:

- Energia Nominal de la Bateria: E_bat_nom = 148,8 Wh
- Energia després de l'eficiència de l'inversor: 148,8 Wh * 0,90 = 133,92 Wh
- Energia després del DoD: 133,92 Wh * 0,90 = 120,528 Wh
- Energia després del factor de Peukert: 120,528 Wh * 0,95 = 114,5016 Wh
- Energia després del factor de temperatura (1,0) i envelliment (1,0): Es manté en 114,5016 Wh.
- Energia final després de pèrdues de cablejat: 114,5016 Wh * 0,99 ≈ 113,36 W.

Per tant, E_neta_lliurable_Wh ≈ 113,36 Wh.

**Càlcul Final del Temps d'Autonomia Teòric**

\- **Per al SAI A (P_L_SAI_A = 312,5 W):**\

t_a_SAI_A [hores] = E_neta_lliurable_Wh / P_L_SAI_A\

t_a_SAI_A [hores] = 113,36 Wh / 312,5 W ≈ 0,36275 hores\

Per convertir a minuts: 0,36275 hores * 60 minuts/hora ≈ 21,77 minuts

\- **Per al SAI B ((P_L_SAI_B = 345 W):\**

t_a_SAI_B [hores] = E_neta_lliurable_Wh / P_L_SAI_B

t_a_SAI_B [hores] = 113,36 Wh / 345 W ≈ 0,32858 hores\

Per convertir a minuts: 0,32858 hores * 60 minuts/hora ≈ 19,71 minuts

**Resultats del Càlcul Teòric Manual Complet:**\

L'anàlisi teòrica detallada, amb el punt de calibratge corregit, projecta una autonomia de **21,77 minuts** per al SAI A i **19,71 minuts** per al SAI B.

**Fase 4: Comparació amb les Dades del Fabricant i Conclusió Final**

**Autonomia Segons Dades del Fabricant (Gràfic/Taula d'Autonomia APC SMTL1500RMI3UC):**

- Per a SAI A (312,5 W): Interpolant entre 300 W (25 min 25 seg. ≈ 25,42 min) i 400 W (19 min 7 seg. ≈ 19,12 min).\

  La càrrega de 312,5 W està al 12,5% del camí entre 300 W i 400 W.\

  25,42 min - ( (25,42 - 19,12) \\* 0,125 ) = 25,42 min - (6,3 \\* 0,125) = 25,42 - 0,7875 ≈ 24,63 minuts.

- Per a SAI B (345 W): Interpolant entre 300 W (25,42 min) i 400 W (19,12 min).\

  La càrrega de 345 W està al 45% del camí entre 300 W i 400 W.

  25,42 min - ( (25,42 - 19,12) \\* 0,45 ) = 25,42 min - (6,3 \\* 0,45) = 25,42 - 2,835 ≈ 22,59 minuts.

**Anàlisi Comparativa dels Resultats:**

|Identificador SAI|Càrrega de Disseny (W)|Autonomia - Càlcul Teòric Manual (min)|Autonomia - Dades Fabricant (min)|Diferència (Manual vs. Fabricant)|
| :- | :- | :- | :- | :- |
|SAI A|312,5|21,77|~24,63|-2,86 min|
|SAI B|345|19,71|~22,59|-2,88 min|

**Anàlisi de les Diferències:**\

La diferència (el nostre càlcul és uns 2,8 minuts més curt) pot ser deguda a:

1\. **Conservadorisme en les Estimacions:** Els nostres factors estimats (η_inv = 0,90, f_p = 0,95) podrien ser lleugerament més pessimistes que el rendiment real del SAI en aquests punts de càrrega. Si l'eficiència real de l'inversor fos, per exemple, del 92% en lloc del 90%, o el factor Peukert fos 0,97 en lloc de 0,95, això augmentaria l'energia nominal calculada (E_bat_nom) i, per tant, l'autonomia final.

1\. **Punt de Calibratge i No Linealitats:** Vam utilitzar el punt de 350 W (21 min 50 seg.) per estimar C_n. Aquesta és només *una* taxa de descàrrega. Com vam veure, l'energia total lliurable canvia amb la taxa. És possible que el nostre mètode de "calibratge" i aplicació de factors constants no reflecteixi perfectament el comportament a 312,5 W i 345 W.

1\. **DoD Aplicat:** El nostre DoD = 0,90 és una decisió de disseny. El fabricant potser considera un aprofitament lleugerament superior de la bateria en els seus gràfics d'autonomia per a bateries noves.

**Conclusió Final**\

L'exercici de càlcul teòric manual, amb el punt de calibratge corregit (350 W - 21 min 50 seg.), ha proporcionat estimacions d'autonomia de **21,77 minuts** per al SAI A i **19,71 minuts** per al SAI B. Aquests valors són coherents i lleugerament inferiors als derivats directament del gràfic del fabricant (aproximadament 24,63 min i 22,59 min, respectivament).

**4\. Distribució d'Energia als Racks (PDU):**

Cada un dels quatre racks destinats a equips de IT està equipat amb dues Unitats de Distribució d'Energia (PDU) independents:

\- **PDU A:** Connectada i alimentada per SAI A (Línia A).

\- **PDU B:** Connectada i alimentada per SAI B (Línia B).

Aquesta configuració de PDU duals per rack és fonamental per implementar la redundància a escala d'equip.

**5\. Alimentació dels Equips de IT:**

La connexió dels equips de IT a les PDU es realitza de la següent manera, buscant un equilibri entre redundància i optimització de recursos:

\- **Servidor amb Doble Font d'Alimentació (Dell PowerEdge R550):** Aquest servidor crític, equipat amb dues fonts d'alimentació (PSU), es connecta amb una PSU a la PDU A i l'altra PSU a la PDU B del seu rack corresponent (Rack 1). Això garanteix la màxima disponibilitat per a aquest equip, ja que pot continuar operant fins i tot amb la fallada completa d'una de les línies d'alimentació o un dels SAI.

\- **Equips amb Font d'Alimentació Única (Servidors Dell R250, Lenovo SR630; Switch HPE Aruba; Router):** Actualment, aquests equips es connecten a una única PDU (ja sigui A o B), distribuint-los estratègicament entre les dues línies per balancejar la càrrega global sobre els SAI A i B i per minimitzar l'impacte d'una fallada en una sola línia.

\- El servidor Dell R250 (Rack 2) s'alimenta de la Línia A (PDU A2).

\- El servidor Lenovo SR630 (Rack 3) s'alimenta de la Línia B (PDU B3).

\- El Switch HPE (Rack 1) s'alimenta de la Línia A (PDU A1).

\- El Router (Rack 1) s'alimenta de la Línia B (PDU B1).

**6\. Alimentació de Sistemes Auxiliars Crítics (HVAC):**

Els sistemes de climatització, tant el sistema d'aire com el de refrigeració líquida, són vitals per al correcte funcionament del CPD. Aquests sistemes es consideren càrregues d'alt consum i s'alimenten mitjançant circuits dedicats i degudament protegits directament des del Quadro General de Distribució (QGD), independents dels SAI destinats als equips de IT.

**8\. Gestió del Cablejat i Entorn Físic:**

Per optimitzar la gestió i seguretat del CPD, s'implementarà:

\- **Terra Tècnic:** Facilitarà la canalització ordenada i protegida del cablejat elèctric i de dades, així com la distribució de fluxos d'aire fred.

\- **Sostre Tècnic:** Permetrà la instal·lació d'equips de ventilació, il·luminació i altres infraestructures.

\- **Canalitzacions Separades:** Pel cablejat de potència i cablejat de dades, minimitzant interferències electromagnètiques.

\- **Etiquetatge Exhaustiu:** De tots els components elèctrics i de cablejat per facilitar la identificació, el manteniment i la resolució d'incidències.

\- **Racks Tancats:** Per millorar la seguretat física, el control ambiental i l'eficiència de la refrigeració.

[Enllaç diagrama elèctric - pàgina web interactiva](https://gersoninteriano.github.io/diagrama-infraestructura-el-ctrica/)

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

Per al monitoratge dels nostres equips Linux i Windows utilitzarem Veyon, que és un programari que permet monitorar fàcilment múltiples usuaris alhora i fins i tot controlar els ordinadors o bloquejar-los i per a monitoritzar els recursos del sistema utilitzarem ELK Stack + Metricbeat.

**Còpies de seguretat / Backups**

Per a les còpies de seguretat de Linux es poden fer servir scripts i l'ús de comandes com ara “tar” i en quant a Windows, l'ús de Windows Server Backup més scripts permet fer còpies de seguretat i passar-les a altres màquines. El destí de les còpies serà el QNAP TS-453D; aquest servidor està fora de l'edifici de l'empresa per garantir una major seguretat i, depenent de la volatilitat de les dades, es faran més o menys còpies incrementals.

[**Enllaç:**](https://docs.google.com/spreadsheets/d/1ehn85YJZ_ASM9lbmWm7qbArGI33OPLD-D0ais7v6l28/edit?usp=sharing)
![copias](https://github.com/ManuelReyes-ITB2425/pro-asixc1b-g4/blob/9c004c93fdfbdf2999a3864a88a6e38867be92e4/proyecto/Fotos/part%20teorica/Mario/Copias2.png)


**RAID**

Per al servidor de còpies, hem decidit utilitzar un NAS més un RAID 5. Amb tres discs, aquesta configuració ens proporciona una capacitat útil equivalent a dos discs per a les dades, mentre que la informació de paritat (distribuïda entre tots els discs) ens permet recuperar les dades en cas de fallada d'un d'ells. A més, aquest sistema està centralitzat, fet que simplifica molt la realització de còpies de seguretat i la compartició d'arxius. Gràcies a aquesta redundància, si un dels discs falla, podem reconstruir tota la informació, ja que el sistema està dissenyat per tolerar la pèrdua d'un disc sense perdre dades.

Per al servidor d'AC i BD, hem decidit utilitzar un RAID 10 per tenir molt d'espai per a totes les nostres dades i, a més a més, redundància. En canvi, el servidor SFTP només té un RAID 1, ja que considerem que és suficient.

**RAID 10:**

Per fer el RAID 10, el primer pas és afegir 4 discs a la màquina, ja que aquests seran els que ens caldran per a aquest RAID.

![raid10_1](https://github.com/ManuelReyes-ITB2425/Projecte-24-25/blob/90ebe3b9e4950c5c37deb1c8e7a7830f2482c180/proyecto/Fotos/part%20teorica/Mario/RAID%2010/Captura%20de%20pantalla%20de%202025-05-26%2008-47-55.png)

Una vegada tenim els 4 discs, creem dos RAIDs de tipus 1.

![raid10_2](https://github.com/ManuelReyes-ITB2425/Projecte-24-25/blob/90ebe3b9e4950c5c37deb1c8e7a7830f2482c180/proyecto/Fotos/part%20teorica/Mario/RAID%2010/Captura%20de%20pantalla%20de%202025-05-26%2008-48-08.png)
![raid10_3](https://github.com/ManuelReyes-ITB2425/Projecte-24-25/blob/90ebe3b9e4950c5c37deb1c8e7a7830f2482c180/proyecto/Fotos/part%20teorica/Mario/RAID%2010/Captura%20de%20pantalla%20de%202025-05-26%2008-48-18.png)

El procediment és el mateix per a l'altre parell de discs, una vegada acabat ens quedaria així:

![raid10_4](https://github.com/ManuelReyes-ITB2425/Projecte-24-25/blob/90ebe3b9e4950c5c37deb1c8e7a7830f2482c180/proyecto/Fotos/part%20teorica/Mario/RAID%2010/Captura%20de%20pantalla%20de%202025-05-26%2008-48-31.png)

Ja per últim, anem a l'eina de Windows per crear i formatar particions i fem clic dret a una de les dues particions i li donem a crear nou volum distribuït, seleccionem les dues particions i ja tindríem el RAID 10.

![raid10_5](https://github.com/ManuelReyes-ITB2425/Projecte-24-25/blob/90ebe3b9e4950c5c37deb1c8e7a7830f2482c180/proyecto/Fotos/part%20teorica/Mario/RAID%2010/Captura%20de%20pantalla%20de%202025-05-26%2008-48-40.png)

Aquí està l'altre RAID 10 del servidor d'Àudio i streaming que són 2 dels nostres serveis pilars.

![raid10](https://github.com/ManuelReyes-ITB2425/Projecte-24-25/blob/main/proyecto/Fotos/part%20teorica/Silvia/Captura%20de%20pantalla%20de%202025-05-21%2011-56-49.png)

**RAID 1:**

El RAID 1 és tan senzill com disposar de dos discs i, des del gestor de discs de Windows, crear un volum reflectit.

![raid1](https://github.com/ManuelReyes-ITB2425/Projecte-24-25/blob/8cb00f8999edea2ef9c4e812c92c4b38dd6c9a90/proyecto/Fotos/part%20teorica/Mario/RAID1.png)

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

Per optimitzar la longitud del cablejat i reduir pèrdues i costos, és crucial assegurar-se que la seva disposició sigui òptima. El mètode Top-of-Rack Switching (ToR) és una solució senzilla i eficaç, que consisteix a col·locar commutadors (switches) a la part superior de cada bastidor (rack), **minimitzant** així la longitud dels cables necessaris. A més, un bon disseny de cablejat estructurat des de l'inici, amb panells de connexió ben ubicats, evita cables innecessàriament llargs i en facilita la gestió i el manteniment.

**Sistemes de circulació d’aire que aprofitin condicions naturals**:  

Per estalviar electricitat en la refrigeració, es pot aplicar el sistema de free-cooling. Aquesta tècnica consisteix a aprofitar l'aire exterior, especialment en llocs amb climes freds o temperatures exteriors favorables en el nostre cas hem escollit Canadà, Nova Zelanda i Islàndia, per refredar les instal·lacions, disminuint la dependència de sistemes de refrigeració mecànica.

**Parada d’equips quan no hi ha càrrega:**  

Es poden configurar els equips de l'empresa, com ara els ordinadors, perquè s'apaguin automàticament després d'un cert període d'inactivitat. Això redueix el consum innecessari fora de les hores de màxima activitat.

## 1.6 Implementació a AWS

**Servidor 1**
![serverA](https://github.com/ManuelReyes-ITB2425/Projecte-24-25/blob/78c2ca8275d961e42828a75de5a6e4209477c865/proyecto/Fotos/part%20teorica/Mario/AWS2.png)
**Servidor 2** 
![ServerFTPDNS](https://github.com/ManuelReyes-ITB2425/Projecte-24-25/blob/main/proyecto/Fotos/part%20teorica/Manel/Captura%20de%20pantalla%20de%202025-05-28%2012-27-28.png)
**Servidor 3**
![server2](https://github.com/ManuelReyes-ITB2425/Projecte-24-25/blob/main/proyecto/Fotos/serveis/Silvia%20Web/Audio-web-streaming.png)

## 1.7 Comparació d’AWS amb altres proveïdors del núvol

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

## 2 Sostenibilitat

**1\. Identificació dels Recursos Emprats:**

- **Infraestructura Física Local (CPD de l'empresa):**
  - **Servidor Windows 1 (AD + BD + Monitoratge):** Dell PowerEdge R550 (Intel Xeon Silver 4310, 32GB RAM, 4x1TB SSD RAID10).
  - **Servidor Windows 2 (FTP + DNS):** Dell PowerEdge R250 (Intel Xeon Silver 4314, 32GB RAM, 2x480GB SSD RAID1).
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

﻿**2. Estimació del Consum Energètic i la Petjada de Carboni (Anual)**

A continuació, es detalla l'estimació del consum energètic anual de la infraestructura física local del CPD i la seva corresponent petjada de carboni.

- **Consum Energètic dels Equips de Tecnologies de la Informació (TI) al CPD:**\
  S'utilitzen els valors de consum operatiu per a cada component:
  - Servidor R550 (AD+BD+Monitoratge): 180 W
  - Servidor R250 (FTP+DNS): 100 W
  - Servidor SR630 (Ubuntu - Audio+Streaming+Web): 175 W
  - Switch HPE Aruba: 60 W
  - Router Ubiquiti ER-4: 11 W
  - **Subtotal Consum Equips TI (P\_IT): 180 + 100 + 175 + 60 + 11 = 526 Watts**
- **Consum Energètic dels Sistemes d'Alimentació Ininterrompuda (SAIs):**\
  S'utilitzen dos SAIs APC SMTL1500RMI3UC, cadascun alimentant una part de la càrrega IT. La capacitat màxima de cada SAI és de 1350W.
  - Càrrega IT connectada al SAI A (sense marge): 90W (R550/2) + 100W (R250) + 60W (Switch) = 250W.\
    Percentatge de càrrega sobre SAI A: (250W / 1350W) \* 100 ≈ 18.5%.
  - Càrrega IT connectada al SAI B (sense marge): 90W (R550/2) + 175W (SR630) + 11W (Router) = 276W.\
    Percentatge de càrrega sobre SAI B: (276W / 1350W) \* 100 ≈ 20.4%.
- Ambdues càrregues estan per sota del 25% de la capacitat del SAI. Segons el gràfic d'eficiència de l'SMTL1500RMI3UC, l'eficiència a càrregues baixes (ex: <25%) és molt alta, al voltant del **97.8%** en mode normal (online).\
  Les pèrdues energètiques dels SAIs es calculen com: Pèrdues\_SAI = P\_IT\_connectada\_al\_SAI \* (1 - Eficiència\_SAI).\
  De forma més directa, el consum total vist per la xarxa per alimentar els equips IT a través dels SAIs és: Consum\_Total\_TI\_amb\_SAIs = P\_IT / Eficiència\_Mitjana\_SAIs.
  - Assumint una eficiència mitjana del **97.8% (0.978)** per als SAIs operant a aquests nivells de càrrega:\
    Consum Total TI + Pèrdues SAIs = Subtotal\_Consum\_Equips\_TI / Eficiència\_SAIs\
    Consum Total TI + Pèrdues SAIs = 526 W / 0.978 ≈ 537.83 Watts
  - Les pèrdues són: 537.83 W - 526 W ≈ 11.83 Watts.
- **Consum Energètic dels Sistemes de Climatització (HVAC):**
  - HVAC Aire (Daikin): 450 W
  - HVAC Líquid (Chilldyne): 4500 W 
  - **Subtotal Consum HVAC: 450 W + 4500 W = 4950 Watts**
- **Consum Energètic Total de la Infraestructura Física Local del CPD:**\
  Total\_Consum\_CPD = (Consum Total TI + Pèrdues SAIs) + Subtotal\_Consum\_HVAC\
  Total\_Consum\_CPD = 537.83 W + 4950 W = 5487.83 Watts
- **Consum Anual de la Infraestructura Física Local del CPD:**\
  Consum\_Anual\_CPD = Total\_Consum\_CPD \* 8760 hores/any\
  Consum\_Anual\_CPD = 5487.83 W \* 8760 h = 48073.3908 Wh/any ≈ 48073.4 kWh/any
- **Consum Energètic Infraestructura Física Externa (Offsite - QNAP):**
  - Servidor QNAP TS-453D (còpies): 26W (mitjana)
  - Consum Anual QNAP: 26W \* 8760h = 227.76 kWh/any.
- **Total Consum Anual Infraestructura Física (Local + Offsite):**\
  48073.4 kWh + 227.76 kWh = 48301.16 kWh/any.
- **Consum Energètic Instàncies Cloud i Tràfic de Dades:**
  - Consum Anual Cloud: **1576.8 kWh/any**.
  - Consum Energètic per Tràfic de Dades (Streaming): **475 kWh/any**.
- **Consum Energètic Total Anual del Projecte:**\
  48301.16 kWh (físic) + 1576.8 kWh (cloud) + 475 kWh (tràfic) = 50352.96 kWh/any.
- **Petjada de Carboni Anual Estimada (kg CO2 eq.):**
  - Infraestructura Física (CPD Local + QNAP Offsite): 48301.16 kWh \* 0,19 kgCO2/kWh (factor Espanya) = 9177.22 kg CO2 eq.
  - Instàncies Cloud: 1576.8 kWh \* 0,10 kgCO2/kWh (factor regió verda) = 157.68 kg CO2 eq.
  - Tràfic de Dades: 475 kWh \* 0,19 kgCO2/kWh (factor conservador) = 90.25 kg CO2 eq.
  - **Petjada de Carboni Total Anual: 9177.22 + 157.68 + 90.25 = 9425.15 kg CO2 eq. (≈ 9.43 tones CO2 eq./any)**.

**3. Proposta de Mesures de Reducció o Optimització:**

- **Prioritat Màxima: Optimització Energètica de la Infraestructura Física Local (CPD):**
  - **HVAC amb Capacitat de Modulació:** En la fase de selecció final dels equips de refrigeració líquida, serà prioritari escollir unitats que ofereixin una **àmplia capacitat de modulació**. Això implica que el sistema ha de poder ajustar la seva potència de refrigeració (i, conseqüentment, el seu consum elèctric) de manera dinàmica i eficient per adaptar-se a la càrrega tèrmica real generada pels equips IT, que actualment és d'aproximadament 0.53 kW. S'evitaran sistemes que operin amb un consum mínim elevat i constant, independentment de la demanda.
  - **Dimensionament Adequat a la Càrrega Actual i Prevista:** El sistema HVAC s'haurà de dimensionar considerant no només la capacitat màxima de refrigeració necessària per a una futura expansió del CPD, sinó també l'eficiència operativa a la càrrega IT actual i a curt termini. Si es preveu un creixement gradual, solucions modulars o sistemes amb múltiples etapes podrien ser més eficients que una única unitat de gran capacitat operant constantment a un baix percentatge de la seva potència.
  - **Implementació de Controls Intel·ligents i Free Cooling:** La gestió del sistema HVAC es basarà en sensors de temperatura distribuïts estratègicament i algoritmes de control avançats per optimitzar el seu funcionament. Es reiterarà la investigació i aplicació de tècniques de **free cooling**, aprofitant les condicions climàtiques locals per minimitzar l'ús de refrigeració mecànica.
  - **Contractació d'Energia 100% Renovable:** Per al subministrament elèctric del CPD local i, si és possible, per a la ubicació del servidor QNAP offsite.
  - **Optimització del Servidor de Còpies QNAP:** Tot i ser de baix consum, assegurar que utilitza modes de repòs quan no està actiu i que els discos durs són eficients.
  - **Selecció de Regions Cloud "Verdes".**

- **Estratègies Generals d'Optimització i Sostenibilitat:**
  - **Compressió de Dades:** Per a trànsit de xarxa i emmagatzematge de còpies.
  - **Implementació d'Interruptors de Transferència Automàtica (ATS) al CPD:** Per a equips locals amb font única.
  - **Economia Circular i Conscienciació.**



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

**BD**

Per a la base de dades, hem fet servir MySQL Workbench, que ens facilita la gestió de totes les nostres dades, i phpMyAdmin per accedir-hi des de qualsevol dispositiu.

Totes les nostres taules tenen una gran quantitat de dades

![BD2](https://github.com/ManuelReyes-ITB2425/Projecte-24-25/blob/90ebe3b9e4950c5c37deb1c8e7a7830f2482c180/proyecto/Fotos/serveis/BBDD/Captura%20de%20pantalla%20de%202025-05-26%2009-00-03.png)

Hem afegit totes les relacions segons aquest esquema i tenint en compte que codi_departament i codi_nivell són claus foranes.

![BD3](https://github.com/ManuelReyes-ITB2425/Projecte-24-25/blob/90ebe3b9e4950c5c37deb1c8e7a7830f2482c180/proyecto/Fotos/serveis/BBDD/Captura%20de%20pantalla%20de%202025-05-26%2009-00-16.png)

Comprovació que des d'un client puc veure la base de dades i administrar-la.

![BD4](https://github.com/ManuelReyes-ITB2425/Projecte-24-25/blob/main/proyecto/Fotos/part%20teorica/Silvia/Captura%20de%20pantalla%20de%202025-05-26%2009-46-05.png)

Comprovació d'una consulta amb un usuari amb només permisos de select.

![BD5](https://github.com/ManuelReyes-ITB2425/pro-asixc1b-g4/blob/4560a46ba898a3987981722d466b9aa99ff8ec3e/proyecto/Fotos/serveis/BBDD/Captura%20de%20pantalla%20de%202025-05-29%2008-58-29.png)

**Monitoratge**

Per al monitoratge dels nostres equips Linux i Windows utilitzarem Veyon, i per monitoritzar els recursos del servidor utilitzarem ELK Stack + Metricbeat.

**Veyon**

El primer pas per monitoritzar és descarregar-se el programa Veyon i configurar-lo, per començar hem de seleccionar l'opció d'utilitzar claus.

![monitoratge1](https://github.com/ManuelReyes-ITB2425/Projecte-24-25/blob/90ebe3b9e4950c5c37deb1c8e7a7830f2482c180/proyecto/Fotos/serveis/Monitoratge/Captura%20de%20pantalla%20de%202025-05-26%2008-44-49.png)

El següent pas és crear el parell de claus.

![monitoratge2](https://github.com/ManuelReyes-ITB2425/Projecte-24-25/blob/90ebe3b9e4950c5c37deb1c8e7a7830f2482c180/proyecto/Fotos/serveis/Monitoratge/Captura%20de%20pantalla%20de%202025-05-26%2008-45-45.png)

I la clau pública la passem a totes les màquines que vulguem monitoritzar i aquestes l'hauran d'importar.
![monitoratge3](https://github.com/ManuelReyes-ITB2425/Projecte-24-25/blob/90ebe3b9e4950c5c37deb1c8e7a7830f2482c180/proyecto/Fotos/serveis/Monitoratge/Captura%20de%20pantalla%20de%202025-05-26%2008-46-02.png)

Ja per últim afegim la mateixa ubicació que a la màquina en la qual vam crear les claus i ja estaria per part del client.

Ara només quedaria anar a la màquina servidor i afegir l'ordinador a 'Locations & computers'.
![monitoratge4](https://github.com/ManuelReyes-ITB2425/Projecte-24-25/blob/90ebe3b9e4950c5c37deb1c8e7a7830f2482c180/proyecto/Fotos/serveis/Monitoratge/Captura%20de%20pantalla%20de%202025-05-26%2008-46-22.png)

Aquest seria el resultat.

![ELk](https://github.com/ManuelReyes-ITB2425/Projecte-24-25/blob/6c55eed3e7888f2e1ceebbd8f455ec8b2c70a61c/proyecto/Fotos/serveis/Monitoratge/Captura%20de%20pantalla%20de%202025-05-28%2009-02-31.png)

**ELK Stack**

El primer pas és instal·lar Elasticsearch i Kibana, i després configurar els seus fitxers perquè es puguin comunicar entre si i siguin accessibles des de qualsevol ordinador.
Arxiu de configuració de Elastic.

![ELk1](https://github.com/ManuelReyes-ITB2425/Projecte-24-25/blob/f1560425c2096285feeb0dab17af6d7090c060b1/proyecto/Fotos/serveis/Monitoratge/Captura%20de%20pantalla%20de%202025-05-27%2011-44-15.png)

Arxiu de configuració de Kibana.

![ELk2](https://github.com/ManuelReyes-ITB2425/Projecte-24-25/blob/cf509e1a35d490e91db432af415aa8a46c33960b/proyecto/Fotos/serveis/Monitoratge/Captura%20de%20pantalla%20de%202025-05-27%2011-46-26.png)

Després executem el setup del Metricbeat i li canviem la configuració.

![ELk3](https://github.com/ManuelReyes-ITB2425/Projecte-24-25/blob/d4a5757feb93676803662352ca79c6ab67bd0812/proyecto/Fotos/serveis/Monitoratge/Captura%20de%20pantalla%20de%202025-05-27%2011-47-50.png)

![ELk4](https://github.com/ManuelReyes-ITB2425/Projecte-24-25/blob/4b9eccf8130330bf9359efda9e5696e8ca18ee81/proyecto/Fotos/serveis/Monitoratge/Captura%20de%20pantalla%20de%202025-05-27%2011-51-03.png)

Si tot ha sortit bé hauríem de poder accedir a Metricbeat dins de Kibana.

![ELk](https://github.com/ManuelReyes-ITB2425/Projecte-24-25/blob/ddcb019313d9a1b851ef32203447dce763af1c34/proyecto/Fotos/serveis/Monitoratge/Captura%20de%20pantalla%20de%202025-05-27%2011-20-24.png)

**Active Directory**

Hem instal·lat Active Directory al Windows Server i hem creat un parell d'usuaris per simular l'entorn de l'empresa. A més, tenim un servei de còpia de seguretat que té el DNS replicat i també l'Active Directory, igual que la resta de coses.

Hem connectat un PC client des de Virtualbox.

![ad](https://github.com/ManuelReyes-ITB2425/Projecte-24-25/blob/main/proyecto/Fotos/part%20teorica/Silvia/Captura%20de%20pantalla%20de%202025-05-26%2009-12-32.png)

![AD](https://github.com/ManuelReyes-ITB2425/Projecte-24-25/blob/main/proyecto/Fotos/part%20teorica/Silvia/Captura%20de%20pantalla%20de%202025-05-26%2009-13-03.png)

També el client hem instal·lat RSAT per a poder administrar el servidor que està en el núvol.

![Rsat](https://github.com/ManuelReyes-ITB2425/Projecte-24-25/blob/main/proyecto/Fotos/part%20teorica/Silvia/RSat.png)

![Rsat](https://github.com/ManuelReyes-ITB2425/Projecte-24-25/blob/main/proyecto/Fotos/part%20teorica/Silvia/Clientrsat.png)

**DNS**

Al DNS tenim la zona del domini asixc1.itb.cat i també les zones dels serveis web d'àudio i de vídeo.

![ad](https://github.com/ManuelReyes-ITB2425/Projecte-24-25/blob/main/proyecto/Fotos/part%20teorica/Silvia/AD.png)

Aquesta configuració és, de fet, la mateixa per a les altres zones.

![DNS](https://github.com/ManuelReyes-ITB2425/Projecte-24-25/blob/9eb38b4a75ae0ae7dd3fbd2d5492ddd3b1d33996/proyecto/Fotos/serveis/DNS/Captura%20de%20pantalla%20de%202025-05-27%2011-57-59.png)


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

# Conclusió

El nostre desplegament del Centre de Processament de Dades al núvol no només respon a la demanda de contingut d'àudio i vídeo, sinó que ha establert una infraestructura digital completa. Hem implementat caracteristiques que garanteix la funcionalitat de tots els nostres serveis.

S'ha verificat la qualitat del servei de transmissió d'àudio i vídeo mitjançant proves d'amplada de banda, confirmant la capacitat de l'arquitectura per gestionar càrregues elevades de contingut digital. La infraestructura implementada inclou una robusta xarxa de serveis com DNS, Active Directory (AD), Nginx per al servei web, bases de dades (BD) i un servidor SFTP per a la transferència segura de fitxers, que col·lectivament proporcionen la base per a una operació eficient i segura. A més, la incorporació d'eines de monitorització com Elasticsearch i Veyon assegura una supervisió contínua i una gestió proactiva de la infraestructura.

Pel que fa a la seguretat, s'han aplicat mesures tant físiques com lògiques. La implementació de firewalls,còpies de seguretat redundants i RAIDs, juntament amb la monitorització constant, garanteix la protecció de les dades de clients i usuaris segons les normatives internacionals, reforçant així l'ODS 16

Per acabar, destaquem el treball en equip i l'organització dels nostres companys, que a sigut molt necessaria per poder fer realitat aquest petit projecte. 
