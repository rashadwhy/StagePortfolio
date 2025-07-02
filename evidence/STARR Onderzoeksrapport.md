**Situatie:**  
Aan het begin van mijn stage bij SECIAN kreeg ik de opdracht om een SaaS-dashboard te ontwerpen dat real-time compliance-informatie toont aan niet-technische gebruikers. Dit moest werken met cloudplatforms zoals Microsoft 365, Google Workspace en AWS. Omdat deze platformen ieder hun eigen datastructuur, terminologie en authenticatie hebben, was het probleem zowel technisch als conceptueel uitdagend.

**Taak:**  
Mijn taak was om de technische haalbaarheid te onderzoeken van een schaalbaar dashboard dat gegevens uit deze platformen veilig kon ophalen, verwerken en tonen. Hiervoor moest ik eerst bepalen welke kennis ontbrak, geschikte methoden kiezen en op basis van onderzoek gefundeerde keuzes maken voor de eerste versie van het systeem.

**Actie:**  
Ik startte met een **feasibility study**, waarbij ik via documentanalyse en testimplementaties onderzocht:

- welke API’s de benodigde data konden leveren;
    
- welke authenticatieoplossingen per platform mogelijk waren (SSO, Entra, SAML, IAM);
    
- hoe compliance-eisen (GDPR, ISO27001, SOC2) vertaald konden worden naar een baseline die automatisch geëvalueerd kon worden;
    
- hoe logs uit verschillende platformen konden worden geharmoniseerd naar één intern datatype.
    

Gedurende het proces paste ik mijn aanpak aan op basis van nieuwe inzichten. Bijvoorbeeld: lokale opslag bleek te risicovol, dus verschoof de focus naar **versleutelde opslag in DynamoDB** en **rolgebaseerd gebruikersbeheer** via Microsoft Entra. Alternatieve oplossingen (zoals open source tools) werden bekeken maar verworpen vanwege onvoldoende veiligheid of schaalbaarheid.

**Resultaat:**  
Het onderzoek resulteerde in een ALPHA-prototype met:

- veilige, schaalbare architectuur;
    
- versleutelde opslag en incrementele dataverwerking;
    
- uniforme datamodellen voor logharmonisatie;
    
- een gebruikersstructuur die aansluit bij compliance-eisen.
    

Deze keuzes zijn verwerkt in het beroepsproduct en worden als fundament gebruikt voor verdere ontwikkeling. Mijn onderzoeksrapport werd volledig goedgekeurd (zie beoordelingsformulier).

**Reflectie:**  
Het uitvoeren van praktijkgericht onderzoek heeft me geleerd dat methodisch werken essentieel is bij complexe vraagstukken. Door kennisgebrek eerst in kaart te brengen en gericht bij te vullen, kon ik sneller tot bruikbare oplossingen komen. Ik heb bewust alternatieven overwogen en waar nodig bijgestuurd. Die aanpak wil ik blijven hanteren in toekomstige opdrachten met vergelijkbare onzekerheid.