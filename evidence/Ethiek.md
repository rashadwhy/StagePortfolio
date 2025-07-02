### 1. **Toegang en gebruikersbeheer: wie mag wat?**

Bij het opzetten van het permissiesysteem en de back-end was een van de vragen: hoe strikt moet de toegang geregeld worden? Technisch gezien was het eenvoudiger om brede toegang toe te staan, maar dat zou betekenen dat gebruikers meer konden dan strikt noodzakelijk. Uiteindelijk koos ik voor een opzet waarbij toegang gebonden is aan rol en context. Dit was niet alleen veiliger, maar ook ethisch verantwoordelijker: gebruikers krijgen alleen toegang tot wat ze nodig hebben, niets meer.

---

### 2. **Data-opslag: lokale snelheid of centrale veiligheid?**

Een ander dilemma betrof het gebruik van local storage. Lokale opslag is sneller en eenvoudiger te implementeren, maar gevoelige gegevens zouden daarmee direct op de client staan, zonder controle of encryptie. Ik heb geleerd om in plaats daarvan te werken met een centrale, beveiligde API-opzet. Daarmee werd de gebruikersveiligheid zwaarder gewogen dan gebruiksgemak of ontwikkelsnelheid.

---

### 3. **Bewezen infrastructuur versus maatwerk**

In het kiezen van back-end infrastructuur was er ruimte om zelf oplossingen te bouwen of goedkopere alternatieven te gebruiken. In de context van cybersecurity vond ik dat niet verantwoord. We kozen daarom voor **bewezen en bestaande technologieën zoals AWS**—met name Cognito en DynamoDB—die niet alleen schaalbaar zijn, maar ook onderhevig zijn aan Europese en internationale regelgeving. In een vakgebied waarin veiligheid en betrouwbaarheid centraal staan, zie ik het als een ethische keuze om gebruik te maken van platforms die bescherming en compliance garanderen.

---

### 4. **Branching en versiebeheer: transparantie versus snelheid**

Tijdens het opzetten van de GitHub-structuur kon ik ervoor kiezen om simpelweg alles op de main branch te doen, zonder duidelijk onderscheid in versies. Dat zou sneller werken, maar onduidelijker zijn voor anderen. Ik koos ervoor om met een duidelijke versiehiërarchie en branches te werken, juist zodat toekomstige ontwikkelaars (of de opdrachtgever zelf) altijd kunnen zien wat er wanneer gebeurd is. Transparantie won van snelheid.

---

### 5. **Beperkte kennis opdrachtgever: grenzen aan uitvoering**

Soms merkte ik dat de opdrachtgever keuzes wilde maken op basis van beperkte technische kennis—bijvoorbeeld over het omgaan met gebruikersgegevens, of het inrichten van infrastructuur. In plaats van simpelweg uit te voeren wat er gevraagd werd, koos ik ervoor om uitleg te geven, alternatieven te bieden, en alleen die oplossingen te bouwen waar ik ook zelf achter kon staan. Ik zie dat als een ethische verantwoordelijkheid: niet alleen doen wat gevraagd wordt, maar meedenken over wat juist is.

---

### Reflectie

Veel ethiek in IT zit niet in grote schandalen, maar in kleine keuzes. Tijdens deze stage heb ik geleerd dat het belangrijk is om stil te staan bij de impact van wat je bouwt, ook als het niet verplicht wordt. Mijn aanpak was telkens: liever iets langzamer of complexer, zolang het verantwoord is. Het bewust kiezen voor bestaande en beschermde technologieën hoort daar ook bij. Ik wil die houding in toekomstige projecten vasthouden, zeker als de druk toeneemt of de belangen groter worden.

---