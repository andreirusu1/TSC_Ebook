# TSC_Ebook
Descriere Proiect
OpenBook este un proiect open source care isi propune sa creeze un e-book reader accesibil si usor de produs. Dispozitivul este conceput pentru a afisa carti digitale, oferind o experienta de lectura similara cu cea a unei carti tiparite, dar cu avantajele tehnologiei moderne. Proiectul meu se bazeaza pe o proiectare simpla si eficienta, iar in aceasta etapa s-au dezvoltat schema electronica, PCB-ul si plasarea componentelor pe placa.


Pentru a transforma aceasta viziune in realitate, am parcurs urmatoarele etape:

1)Engineering Validation (EVT): Am proiectat schema electronica si am creat PCB-ul, asigurandu-ne ca fiecare conexiune este optimizata pentru performanta si fiabilitate.

2)Modelare 3D: Am verificat plasarea componentelor pe placa intr-un mediu 3D, garantand ca designul se integreaza perfect in cadrul final al dispozitivului.

3)Partea de display, baterie si modelele 3D complete ale dispozitivului nu au fost dezvoltate inca. Acest repository se concentreaza pe proiectarea schematica, realizarea PCB-ului si plasarea componentelor pe placa in mediul 3D.


Diagrama Bloc

Mai jos se prezinta o diagrama bloc schematica a principalelor componente si a interconexiunilor acestora:
![diagrama](https://github.com/user-attachments/assets/beb14f03-0eaf-43f4-b607-428d83303f6e)


Bill Of Materials (BOM)
Nr.	Componenta	Datasheet URL	Link site pt procurare

1	ESP32-C6-WROOM-1-N8	[Datasheet](https://www.espressif.com/sites/default/files/documentation/esp32-c6-wroom-1_wroom-1u_datasheet_en.pdf)	[link](https://www.digikey.com/en/products/detail/espressif-systems/ESP32-C6-WROOM-1-N8/17728866?utm_source=snapeda&utm_campaign=buynow&utm_medium=aggregator)

2	Micro-SD	[Datasheet](https://www.attend.com.tw/data/download/file/112A-TAAR-R03_Spec.pdf)	[link](https://www.digikey.com/en/products/detail/attend-technology/112A-TAAR-R03/17633923)

3	Inductor (68µH)	[Datasheet](https://www.we-online.com/components/products/datasheet/784373170680.pdf)	[link](https://ro.mouser.com/ProductDetail/Wurth-Elektronik/784373170680?qs=sGAEpiMZZMv126LJFLh8yzGkpireax1GgDeN9GF1EUQ%3D)

4	LED	[Datasheet](https://www.bridgelux.com/sites/default/files/resource_media/DS51_Rev%20F%20Bridgelux%20SMD%203030%20Data%20sheet.pdf)	[link](https://www.digikey.com/en/products/detail/bridgelux/BXEM-27E0000-0-000/6618599)

5	Buttons	[Datasheet](https://configured-product-images.s3.amazonaws.com/Datasheets/TL3315.pdf)	[link](https://www.digikey.com/en/products/detail/e-switch/TL3315NF250Q/1870396)

6	Capacitor 	[Datasheet](https://eu.mouser.com/datasheet/2/40/cx5r_KGM-3223198.pdf)	[link](https://ro.mouser.com/ProductDetail/KYOCERA-AVX/0402YD104MAT2A?qs=4PckX6MNpMErOINbbZj3Cw%3D%3D&srsltid=AfmBOorRllqAGFDVGSlUxRe1HCu5DEMiSSNplU-KeE2woDnCuT1J4_ia)

7	Rezistori	[Datasheet](https://www.yageo.com/upload/media/product/products/datasheet/rchip/PYu-RC_Group_51_RoHS_L_12.pdf)	[link](https://www.digikey.com/en/products/detail/yageo/RC0402JR-07100KL/726416)

8	Diode (Schottky Rectifier)	[Datasheet](https://datasheets.kyocera-avx.com/schottky.pdf)	[link](https://www.digikey.com/en/products/detail/kyocera-avx/sd0805s020s1r0/3749517)

9	Connector USB (Type-C)	[Datasheet](https://gct.co/files/drawings/usb4110.pdf)	[Mouser](https://ro.mouser.com/ProductDetail/GCT/USB4110-GF-A?qs=KUoIvG%2F9IlYiZvIXQjyJeA%3D%3D&utm_id=6470900573&utm_source=google&utm_medium=cpc&utm_marketing_tactic=emeacorp&gad_source=1)

10	Test Pad 	[DataSheet](https://cdn-shop.adafruit.com/product-files/3825/3825_diagram.PDF) [link](https://componentsearchengine.com/prices/3825?manufacturer=Adafruit)

 Aceasta lista este orientativa. Componentele si specificatiile pot fi ajustate pe parcursul dezvoltarii.

Functionalitatea Hardware
Proiectul se bazeaza pe microcontroller-ul ESP32-C6, iar designul hardware a fost gandit pentru a optimiza functionalitatea si integrarea componentelor. Principalele aspecte includ:

Alimentare: Dispozitivul este alimentat printr-un regulator de tensiune care transforma 5V in 3.3V, necesar pentru functionarea corecta a ESP32-C6.

Conectivitate: ESP32-C6 pune la dispozitie mai multe interfete de comunicatie (UART, SPI, I2C), esentiale pentru conectarea senzorilor si a altor periferice.

Plasare Componentelor: Schematicul si PCB-ul au fost proiectate pentru a asigura o dispunere eficienta a componentelor, reducand interferentele electromagnetice si facilitand asamblarea manuala sau automatizata.

Verificare 3D: Modelul 3D realizat in Fusion360 (exportat ca .step) a fost folosit pentru a verifica plasarea corecta a componentelor pe placa.

Configurarea Pinilor ESP32-C6
Mai jos sunt detaliate functiile pinilor utilizati in proiect:

Pin	    Functie	          Descriere
GPIO1	  TX	            Transmiterea datelor catre periferice
GPIO3	  RX	            Receptionarea datelor de la periferice
GPIO12	I2C             SDA	Linie de date pentru comunicatia I2C
GPIO13	I2C             SCL	Linie de ceas pentru comunicatia I2C
GPIO14	Buton/Resetare	Functie de resetare a dispozitivului
Nota: Configuratia pinilor poate fi ajustata in functie de cerintele finale ale sistemului.


Testare si Validare: Schematicul si PCB-ul au fost validate prin simulatii si prototipare, asigurand performanta optima a dispozitivului.

Planuri de Dezvoltare: Etapele urmatoare includ integrarea componentelor pentru display, alimentare prin baterie si dezvoltarea completa a modelului 3D al dispozitivului pentru validarea finala.
