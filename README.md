# GazetteerMacin
Gazetteer-ul plășii Măcin pentru anul 1896.

Formatul datelor este text delimitat de tab-uri în codificare utf8.
**Scara** recomandată pentru utilizarea datelor este **1:120000** 

## Fișiere: ##
**Gazetteer.csv**   : toponimele și caracteristicile pentru acestea organizate pe coloane, precum ID, ORT_ANT, NUME_ALT, LIMBA, COD1, COD2, COD3, UAT, UAT_ACT, LAT_WGS84, LONG_WGS84, X_STEREO, Y_STEREO.  
**Clasificare.csv**      : codul, numele și descrierea pentru clasele de caracteristici, unde "CODx" este codul clasei de caracteristici corespunzător celui din tabelului Gazetteer; "TIP1" reprezintă clasa toponimului, "TIP2" este o categorisire a acestor clase, iar "TIP3" este elementul.  
**Geoname_v1.gpkg** : idem Gazetteer.csv + informația geospațială.

Tabelul principal ***Gazetter*** are următoarele câmpuri:  

**ID**: identificatorul unic al înregistrării în baza de date Gazetteer, numeric(5,0)  
**TOPONIM**         : numele punctului geografic, (utf8), varchar(50)  
**ORT_ANT**         : ortografiile anterioare, separate prin virgulă, a numelui punctului geografic (utf8), varchar(50), identificat pe alte hărți sau în diverse documente  
**NUME_ALT**        : nume alternative, care s-au schimbat în timp, separate prin virgulă, varchar(50)  
**LIMBA**           : originea/etimologia toponimului, varchar(10)  
**COD1**            : codul identificatorului unic corespunzător clasei toponimului, numeric(3,0)  
**COD2**            : codul identificatorului unic corespunzător pentru categoria clasei, numeric(4,0)    
**COD3**            : codul identificatorului unic corespunzător elementului, numeric(3,0)    
**UAT**             : unitatea administrativ-teritorială în care se afla elementul la acea vreme, varchar(50)  
**UAT_ACT**         : unitatea administrativ-teritorială în care se află elementul la momentul actual (anul 2022), varchar(20)  
**LAT_WGS84**       : latitudinea în grade zecimale (WGS84), numeric(8,6)  
**LONG_WGS84**      : longitudinea în grade zecimale (WGS84), numeric(8,6)  
**X_STEREO**        : latitudinea în metri (Stereo70 - EPSG:3844), numeric(10,4)    
**Y_STEREO**        : longitudinea în metri (Stereo70 - EPSG: 3844), numeric(10,4)  

În acest tabel, doar coloanele **ORT_ANT** și **NUME_ALT** permit valori nule.  

Tabelul secundar ***Clasificare***:

**COD1**            : codul identificatorului unic corespunzător clasei toponimului, numeric(3,0)  
**TIP1**            : denumirea clasei toponimului, varchar(10)  
**COD2**            : codul identificatorului unic corespunzător pentru categoria clasei, numeric(4,0)  
**TIP2**            : denumirea categoriei clasei toponimului, varchar(70)  
**COD3**            : codul identificatorului unic corespunzător elementului, numeric(3,0)  
**TIP3**            : denumirea elementului, varchar(40)  

În acest tabel, nicio coloană nu permite valori nule.  

### Sursa datelor   :  
Dicţionarul geografic statistic şi istoric al judeţului Tulcea-Dănescu, Grigore, 1896  
Harta Dobrogei ridicată pe scala 1:10000 în anii 1880-1883 sub domnia Majestății Sale Carol I rege al României de Marele Stat Major al Armatei, Redcțiune la 1:200000, Bucuresci, 1887  
Planul Director de Tragere, foaia 5354, anul 1950-1954 pentru toponimul "Coada Caprinei"  
Planul Director de Tragere, foaia 5553, anul 1950-1954 pentru toponimele "Balta Caprinei", "Pădurea Lată", "Pădurea Jidanului"   

**Cheia primară** se face pe coloana *COD3* din tabelul *Clasificare*, iar **cheia străină** se face pe coloana *COD3* din tabelul *Gazetteer*.
                  
## Descrierea elementelor:

***pârâu***                          : apă curgătoare cu dimensiuni mici (albie îngustă, debit redus), care uneori poate seca.  
***gârlă***                          : depresiune alungită în lunca unui râu, acoperită permanent sau temporar cu apă, făcând legătura între râu și lacurile de luncă.  
***baltă***                          : lac natural, de dimensiuni mai mici, cu adâncime mică, format în sectoare mai joase în luncile râurilor.  
***lac***                            : o întindere de apă stătătoare, strânsă într-o scobitură a uscatului.  
***braț***                           : curs secundar care se desprinde dintr-un râu sau fluviu  
***deal***                           : formă pozitivă de relief cu aspect de culme rotunjită încadrată de văi, care se desfășoară între 300 și 1000 m.  
***grind***                          : formă de relief pozitivă, formată din acumulările de pietriș și nisip, situată în albia majoră a râurilor sau de-o parte și de alta a brațelor deltaice.  
***movilă***                         : ridicătură de pământ, mai mică și mai rotunjită decât dealul, care se află de obicei în regiunile de câmpie sau de podișuri joase.  
***vârf de deal***                   : formă de relief cu aspect conic, ce reprezintă partea superioară a unor culmi deluroase.  
***ostrov***                         : un pământ înconjurat pe toate părțile cu apă, format prin acumularea de aluviuni pe cursul unei ape curgătoare sau stătătoare, precum lacul.  
***vale***                           : formă de relief negativă rezultată preponderent prin acțiunea unei ape curgătoare.  
***câmpie***                         : o întindere mare de loc, cu o suprafață aproape netedă și joasă.  
***pisc***                           : vârf ascuțit și stâncos, caracteristic regiunilor muntoase și deluroase, de obicei fără vegetație, cu pante repezi, dominând o vale sau o depresiune.  
***culme deluroasă***                : partea superioară alungită și relativ îngustă a unor dealuri.  
***șir de dealuri***                 : o înlănțuire de dealuri, despărțite de șei înguste.  
***șir de movile***                  : o înlănțuire de movile, despărțite de văi înguste.  
***pădure***                         : suprafață mare de teren pe care cresc în stare sălbatică specii de arbori și arbuști, specii de plante erbacee, mușchi și diferite specii de animale.  
***sat***                            : forma cea mai veche a așezărilor umane, care se caracteizează prin modul de grupare a gospodăriilor, prin îndeletniciri specifice, activității economice proprii; este mai mare decât un cătun și mai mic decât un oraș.  
***comună rurală***                  : așezare rurală cu funcție administrativ teritorială care cuprinde populația rurală unită prin comunitate de interese și tradiții, fiinnd alcătuită din unul sau mai multe sate, în funcție de condițiile economice, social-culturale, geografice și demografice.  
***comună urbană***                  : așezare urbană cu funcție administrativ teritorială care cuprinde populația rurală unită prin comunitate de interese și tradiții, fiinnd alcătuită din unul sau mai multe sate, în funcție de condițiile economice, social-culturale, geografice și demografice.  
***ruinele unui sit religios***      : loc de importanță religioasă distrus sau degradat care nu mai este funcțional.  
***ruinele unui pichet de graniță*** : loc a cărui populație este angajată în paza unui sector al graniței, în prezent abandonat și degradat.  
***ruine de cetate***                : loc cu rol de apărare al țării, în prezent abandonat și degradat.  
***locuință izolată***               : construcție locuită plasată la o distanță considerabilă față de restul locuințelor care alcătuiesc așezarea.  
***câșlă de oi***                    : așezare stabilă, mai ales în timpul iernii, unde se adăpostesc oile și ciobanii și unde se prepară produsele din laptele oilor.  
***cetate***                         : construcție înconjurată de ziduri cu rol de apărare.  
***fort***                           : lucrare de fortificație construită din zidărie, cu contur poligonal, care face parte dintr-un sistem de întărituri și care este menită să apere un centru important sau o linie strategică.  
***monument funerar***               : mormântul unui tătar.  
***mănăstire***                      : locul unde trăiesc împreună într-o formă de viață monastică mai mulți monahi sau monahii.  

### Sursa definițiilor           :  
Stamatescu, F., *România și cele-l-alte țări locuite de români*, Editura "Librăriei Școalelor", Bucuresci  
Ilinca, L., *Geodex: dicționar de termeni geografici*, Editura Tiparg, Pitești, 2015

                  
