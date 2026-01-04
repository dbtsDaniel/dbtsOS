# dbtsOS
Ett Operativsystem för att skriva avancerad svensk lyrik med AI-Orkestrering. 


# LyrikOS – Snabbstartsguide (för 13‑åringar)

Välkommen till **LyrikOS**, ett litet program som hjälper dig skriva och organisera egna låttexter på ett smart sätt. Allt sparas i din webbläsare, så du behöver ingen inloggning och inget internet när du arbetar.

## Installera och starta

1. Packa upp ZIP‑filen du fick. Den heter t.ex. `DBTS_LyrikOS_MAXIMAL_OPTIMAL.zip`.
2. Öppna mappen `maximal_optimal_app` och dubbelklicka på `index.html`. Programmet öppnas i din webbläsare.
3. Om du vill köra via din mobil eller på nätet, följ instruktionerna i `docs/README_DEPLOY.md` för att lägga upp appen gratis på en egen subdomän.

## Så fungerar appen

### 1. Skapa en hierarki
På sidan **Hem** gör du fyra saker i tur och ordning:

1. **Värld** – Ange ett namn på din värld (t.ex. "MinDebut") och klicka *Spara värld*. Välj en redan sparad värld genom att klicka på knappen med namnet.
2. **Profil** – Skriv in ett artistnamn och spara. Kopplas alltid till den valda världen.
3. **Album** – Döp ditt album och spara. Varje album hör till en profil.
4. **Spår** – Döp låten/spåret. När du har valt spår lyser knappen *Fortsätt till wizard*.

### 2. Bank
Under **Bank** hittar du alla färdiga rader (rim, metaforer och punchlines). Du kan filtrera på tema, importera egna rader från en CSV‑fil eller exportera allt som CSV för backup. CSV-mallar ligger i mappen `data/`.

### 3. Wizard
Wizard-sidan tar dig igenom låtskrivandet med **fem knappar**:

1. **Snabb** – Minimalt flow, ger dig en enkel prompt för att skriva en rå text.
2. **Standard** – Normalt flow, genererar en prompt med rim och teman från banken.
3. **Djup** – Fördjupad version med prosodi och internrim.
4. **Experiment** – Utmana reglerna och skapa något oväntat.
5. **Felsök** – Om du fastnar. Ger en prompt som förklarar vad du gjort hittills och ber AI:n föreslå lösning.

När du klickar på en knapp skapas en text i rutan. Klicka *Kopiera prompt* för att kopiera den. Gå till din AI (ChatGPT, Claude, Gemini, etc.), klistra in prompten och kör. Kopiera sedan AI:ns svar och använd det i nästa steg eller spara det som anteckning under **Vault**.

### 4. Suno Export
Denna sida hjälper dig skapa ett paket till **Suno PRO v5**. Skriv eller klistra in:

* **Lyrics** – din text uppdelad i [VERSE], [HOOK], [BRIDGE] osv.
* **Style** – en engelsk beskrivning av sound och tempo (t.ex. "Swedish vals‑trap, 6/8, 74‑80 BPM").
* **Exclude** – negativa ord/genre som du vill undvika.
* **Notes** – personas, Reuse Prompt‑hintar eller annan metadata.

Klicka *Generera Suno-paket* och kopiera allt till Suno Custom Mode.

### 5. Vault (Dagbok)
Här kan du skriva ned anteckningar för spåret du arbetar på. Klicka *Spara anteckning* för att lägga till i listan. De tio senaste visas. Perfekt för att logga idéer eller vad AI:n svarade.

### 6. Inställningar & Backup
Här kan du exportera hela databasen som en JSON‑fil eller importera en JSON för att återställa allt. Du kan också begära *persistent lagring* (fungerar när du kör via https) för att minska risken att webbläsaren rensar data.

## Importera egna rader

Vill du lägga in egna rim/metaforer? Skapa en CSV med kolumnerna:

`id,base_text,type,themes,rewrite1,rewrite2,rewrite3,rewrite4`

Spara den som .csv och importera under Bank. Teman separeras med ett lodstreck (`|`).

## Tips för bästa resultat

* Jobba metodiskt: skapa en hierarki först, sedan bank, wizard, Suno och vault.
* Testa olika nivåer i wizard – ibland ger "Experiment" bättre idéer än "Standard".
* Exportera backup regelbundet så du inte förlorar något.
* När appen körs via en säker domän (https) kan du installera den som en app på mobilen.

Lycka till med ditt musikskapande!
