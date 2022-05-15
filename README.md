Academia de Studii Economice București     	  	 	  	  	  
Facultatea de Cibernetică, Statistică și Informatică Economică 
An universitar: 2021-2022 
Semestrul II
 
 
       
 
 
   
 
 
 
Proiect Cloud Computing 
 
 
 
 
 
 
 
 
 	 	 	 	 	 Nume: Ene Elena-Alexandra
           Grupa: 1117





Introducere

În termeni simpli, cloud computing înseamnă închirierea componentelor IT, în loc de achiziționarea acestora. În loc să investească masiv în baze de date, software și hardware, companiile aleg să utilizeze puterea de calcul a acestora prin internet sau în cloud și să plătească pentru aceasta pe măsură ce o utilizează. Aceste servicii cloud includ acum, dar nu se limitează la acestea, servere, spațiu de stocare, baze de date, rețele, software, analize și business intelligence. Cloud computingul oferă viteza, scalabilitatea și flexibilitatea care permit companiilor să se dezvolte, să inoveze și să susțină soluții IT de afaceri.
În concluzie, cloud computing este un model de prelucrare a datelor care constă în punerea la dispoziția utilizatorului, prin intermediul resurselor web și a serviciilor furnizorului, a puterii de calcul, spațiului de disc, bazelor de date, serviciilor de analiză și inteligenței artificiale.
Deși nu ne dăm seama, folosim serviciile cloud computing zilnic și în mod involuntar, acestea reușind să ne îmbunătățească și să eficientizeze munca. Câteva exemple de utilizare a cloud-ului în viața de zi cu zi – cele pe care le utilizăm noi și cele pe care le poate utiliza o firmă.

•	Stocarea fișierelor pe un cloud drive, în locul unui computer sau a unei unități USB, ceea ce va permite accesul comod la materiale de la nivelul unui browser web și va proteja împotriva pierderii de date (disponibil, de ex., pe Google Drive sau în serviciul GCP Cloud Storage);

•	Editarea în echipă a documentelor text, prezentărilor sau foilor de calcul; modificările aduse fișierelor din cloud sunt salvate automat și sunt vizibile imediat pentru alți oameni (aplicațiile Google Docs, Sheets sau Slides disponibile în pachetul Google Workspace);

•	Îmbunătățirea comunicării între oameni datorită instrumentelor încorporate, cum ar fi chat-ul sau platforma pentru videoconferințe (Chat și Meet disponibile în pachetul de aplicații de afaceri Google Workspace);

•	Construirea și dezvoltarea aplicațiilor cu utilizarea serviciilor cloud avansate – inclusiv o putere de calcul enormă, instrumente de analiză BigData sau modele de învățare automată.
 


Descrierea problemei

Având ca referinţă aplicaţia dezvoltată la seminar, de a avea mailuri traduse în mai multe limbi, m-am gândit cum ar putea fi aceasta folosită pentru ceva şi mai practice, astfel a prins contur aplicaţia Rose Letters. Aceasta îşi propune să ajute cuplurile care sunt din ţări diferite să comunice, practic să aducă un strop de fericire în vieţile îndrăgostiţilor. Tocmai în ideea aceasta este creată şi interfaţa, având nuanţe de roz şi roşu. Mesajele trimise sunt şi stocate într-o bază de date, astfel că acestea nu se vor pierde, iar cuplurile vor putea să le revadă oricând.

Pentru a putea stoca textul mailurilor s-a folosit o bază de date SQL în cloud, folosind Google Cloud Platform, iar definirea bazei de date s-a făcut prin MySQL Workbench. În plus, mailurile  se pot trimite întrucât am utilizat SendGrid, iar traducerea lor se face printr-un API Google, mai exact Cloud Translation API. 


Descriere API

Cloud Translation API foloseşte tehnologia de traducere automată de la Google pentru a traduce imediat texte în diverse limbi. 

Printre funcţiile folosite în proiect se numără detect, o funcţie care identifică limba în care este scris un text şi translate, funcţia ce face posibilă traducerea textului. Ambele funcţii primesc un parametru text pe care îl au de analizat, iar funcţia din urma şi un parametru de limbă, astfel identificând în ce limbă să se facă traducerea.

Flux de date

În cadrul proiectului am utilizat următoarele metode, ilustrate şi în capture de ecran din Visual Studio Code, dar şi executate în Postman:

•	GET
Această metodă HTTP facilitează selectarea tuturor mesajelor din baza de date în funcţie de ID:
 ![image](https://user-images.githubusercontent.com/105549783/168493437-eb3dcab3-2237-4b9d-8b43-3b04555e088b.png)
![image](https://user-images.githubusercontent.com/105549783/168493440-148ec2d4-362f-4689-be1e-b246b3929f86.png)

 
De asemenea, putem căuta toate mesajele din baza de date: 
 ![image](https://user-images.githubusercontent.com/105549783/168493449-0fba31c1-d636-4f93-a4c8-a79b9e7b3eaf.png)
![image](https://user-images.githubusercontent.com/105549783/168493456-0033ab42-7488-4118-9cfe-1b94accfda32.png)

 

•	DELETE 
Prin această metodă este posibilă ştergerea unei înregistrări după ID:
 ![image](https://user-images.githubusercontent.com/105549783/168493458-bfb7355a-bdff-4038-b638-b0bb6908afd5.png)
![image](https://user-images.githubusercontent.com/105549783/168493464-4fd6f477-c857-435b-bf60-15d92b07d89a.png)

 
•	POST 
Prin metoda POST putem introduce noi întregistrări în baza de date, care mai apoi pot fi actualizate, dar şi pentru a traduce mesaje şi a le trimite pe mail:
 ![image](https://user-images.githubusercontent.com/105549783/168493471-f1e4515f-f872-431e-b3a4-81d30388e674.png)
![image](https://user-images.githubusercontent.com/105549783/168493476-9eb543de-8063-41a1-b1b2-d468ddccf779.png)
![image](https://user-images.githubusercontent.com/105549783/168493479-6d685028-1e50-4bf1-b59a-d0264aa60685.png)
![image](https://user-images.githubusercontent.com/105549783/168493483-96630d92-d38e-4725-a7fb-dae09c7bf1f7.png)
![image](https://user-images.githubusercontent.com/105549783/168493485-2c5046aa-d80c-40de-98e4-748b8d4d0cf7.png)
![image](https://user-images.githubusercontent.com/105549783/168493490-8b4445f5-9aea-46f8-88cc-abcc474b64f5.png)

 
 
 
 
 

•	PUT
Am folosit această metodă pentru a actualiza înregistrări deja prezente în baza de date:
 ![image](https://user-images.githubusercontent.com/105549783/168493495-74154019-08de-434d-bfd9-21c31b3d684f.png)
![image](https://user-images.githubusercontent.com/105549783/168493505-df92a363-07d8-4b15-ac46-97a98f0f6a40.png)

 







Front-End

Aplicaţia la prima vedere arată astfel:
 ![image](https://user-images.githubusercontent.com/105549783/168493512-3204a2e0-e1d7-4ef6-87f0-b8945fcfc80f.png)

Putem introduce numele destinatarului, e-mailul acestuia şi mesajul pe care ne dorim să îl transmitem:
![image](https://user-images.githubusercontent.com/105549783/168493515-63be1df0-656f-40d2-9f78-d6517b9057bf.png)



Să presupunem că vrem să trimitem mesajul în franceză. Atunci vom apăsa pe respectivul buton, iar aplicaţia ne dă un pop-up cu mesajul nostru:
![image](https://user-images.githubusercontent.com/105549783/168493521-9abdbbd6-10e3-43ef-a080-9fe39110c4d2.png)

 
De asemenea, istoricul mesajelor se actualizează:
 ![image](https://user-images.githubusercontent.com/105549783/168493522-535f0214-990f-489b-8ef2-fb30451af336.png)




Referinţe

https://tailwindcss.com/
https://cloud.google.com/translate
https://dashboard.heroku.com/apps
https://gurita-alexandru.gitbook.io/cloud-computing-2022-simpre/


Linkurile unde se află proiectul:

•	Github BackEnd: https://github.com/elenaene/ProiectCloudComputing 
•	Github FrontEnd: https://github.com/elenaene/ProiectCloudComputing2 
•	Aplicaţie: https://fast-mesa-92544.herokuapp.com/ 
•	Youtube: https://youtu.be/xTsL724dSX4 

