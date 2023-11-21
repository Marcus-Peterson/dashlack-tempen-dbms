# 🌐 Project-DashLack-Tempen 

**Project**: DashLack Tempen.

## 🖥️ Teknisk beskrivning av projektet


### Arkitektonisk Översikt av "DashLack Tempen"

1. **Komponenter**:
   - **Temperatursensor**: Denna enhet samlar in temperaturdata. Den är kopplad till Arduino.
   - **Arduino**: En mikrokontroller som läser av data från temperatursensorn och styr lamporna baserat på temperaturvärdena.
   - **Lampor**: Tre lampor (🟢 grön, 🔴 röd, 🔵 blå) som indikerar temperaturstatus.
   - **Webbapplikation**: Består av en front-end (byggd med Thyme Leaf) och en back-end (byggd med Spring). Webbapplikationen tar emot, lagrar och visar temperaturdata.
   - **Database**: En MySQL databas (byggd med Hibernate) som lagrar temperaturdata och relaterad information.
   - **Lokal webbserver**: Servern som hanterar kommunikation mellan alla komponenter.

2. **Dataflöde**:
   - Temperatursensorn samlar in data och skickar den till Arduino.
   - Arduino bearbetar data (tänder en av lamporna baserat på temperaturvärde) och skickar data till webbapplikationen via Java API var 5:e minut.
   - Webbapplikationens back-end tar emot data och lagrar den i MySQL-databasen.
   - Front-end av webbapplikationen hämtar data från back-end via Java API och visar den för användaren.

3. **Funktionalitet**:
   - Medeltemperaturen för de senaste 10 minuterna beräknas och visas på webbapplikationens huvudsida.
   - Om temperaturen är för hög eller för låg, visas en varning på webbapplikationen varje minut tills temperaturen är stabil.

4. **Kommunikation**:
   - Arduino kommunicerar med webbapplikationen via ett Java API.
   - Webbapplikationens front-end och back-end kommunicerar med varandra via ett Java API.
   - Webbapplikationens back-end kommunicerar med databasen direkt.

5. **Säkerhet och Felsökning**:
   - Implementera grundläggande säkerhetsåtgärder för att skydda data och förhindra obehörig åtkomst.
   - Använd loggning för att spåra systemaktivitet och underlätta felsökning.

### Avslutning:
"DashLack Tempen" är ett integrerat system som kombinerar hårdvara (Arduino, sensorer, lampor) med mjukvara (webbapplikation, databas) för att övervaka och rapportera temperaturdata i realtid. Genom att kombinera dessa komponenter erbjuder systemet en omfattande lösning för temperaturövervakning och rapportering.

Denna beskrivning ger en övergripande bild av systemets arkitektur och funktionalitet. Om det finns några specifika områden där du vill ha mer detaljerad information eller ytterligare förklaringar, låt mig veta!

### 📁 Dokumentation i mappar:
Varje mapp som innehåller kod för “Project DashLack Tempen” innehåller alltid en kort dokumentation som heter “documentation.txt” & beskrivning på vad koden gör. T.ex. vilken typ av data den hanterar, vilken data den skall returnera osv osv. Och t.ex. Hur den skall användas.

### 📐 Hårdvarudesign:
[Designlänk](https://drive.google.com/file/d/1xqUNbfdQe5wr-w1T4WkRMIye5BHBLjq7/view?usp=drive_link)

### 🛠️ Val av Tech-stack:
**Frameworks**:
   - **Thymeleaf**: Dynamiska hemsidor (Java)
   - **Hibernate**: Databashantering (Java)
   - **Spring**: API byggnationer (Java)
   - **JArduino**: Skriva arduino kod i java
