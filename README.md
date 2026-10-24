AccessVision Server
Backenden för AccessVision hanterar API-kommunikation mellan mobilappen, bildanalysen och Raspberry Pi-delen.

Funktioner
- Ta emot bilder för analys av registreringsskyltar.
- Bearbeta bilder och läsa registreringsnummer med OCR.
- Kontrollera registreringsnummer och status mot databasen.
- Hantera fordonsuppgifter och notiser.
- Tillhandahålla funktioner för kommunikation med appen och grindstyrningen.
- Skicka händelser i realtid via WebSocket.

Teknik
- Python
- FastAPI enligt projektets serverupplägg
- MySQL
- OpenCV och PaddleOCR
- WebSocket

Installation
1. Installera en kompatibel Python-version och MySQL.
2. Öppna mappen för serverprojektet.
3. Skapa och aktivera en virtuell miljö:
   python -m venv .venv
4. Installera beroenden enligt projektets dependency-fil, exempelvis requirements.txt om den finns.
5. Konfigurera databasanslutning och serverinställningar.
6. Starta servern med det kommando som gäller för projektets aktuella startfil.
Kontrollera startfil och beroenden i repot innan du lägger till exakta startkommandon här.

Konfiguration
Konfigurera databas, portar och adresser via miljövariabler eller lokal konfiguration. Lägg inte lösenord, tokens eller andra hemligheter i GitHub.
Kommunikation
Servern kommunicerar med appen via HTTP API och WebSocket och tar emot analysförfrågningar från andra komponenter. Se till att API-adresser och portar matchar i alla repositorier.

Säkerhet
- Använd HTTPS/WSS i produktion.
- Kräv autentisering och behörighetskontroll för administrativa API:er och grindstyrning.
- Begränsa nätverksåtkomst.
- Validera inkommande data och hantera timeout och fel.
- Rotera hemligheter som tidigare råkat publiceras.

Felsökning
- Kontrollera att databasen är igång och att anslutningsuppgifterna stämmer.
- Kontrollera serverloggar och portkonfiguration.
- Kontrollera att appen och Raspberry Pi använder rätt serveradress.
- Kontrollera att OCR-beroenden och modeller är installerade.
