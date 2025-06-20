# Postup pro testovací připojení k CZ-OOTS přes CMS

Tento návod shrnuje doporučený postup pro nastavení testovacího připojení k systému CZ-OOTS přes rozhraní ISSS. Doporučujeme zároveň sledovat dostupnou videoukázku, která celý proces ilustruje nejpřehledněji.

## 📋 Postup

1. **Připravte si ID vašeho AIS v systému RPP**  
   Spolu s tím i číslo OVM – tedy **IČ organizace**.

2. **Získejte testovací certifikát pro komunikaci s CMS**  
   Certifikát musí být určen pro přístup do testovacího prostředí CMS.

3. **Cílový AIS:** `10339`

4. **Používaná agenda a kontext**
   - Agenda: `A3791`
   - Činnostní role: `CR44328`
   - Kontextový kód: `A12251.1`
   - Formulář: `G1(gsbCtiData)`

5. **Volání přes CMS (testovací AIS)**  
   Pro testování doporučujeme používat tzv. **testovací AIS**.  
   Příklady volání naleznete ve složce [📂 examples](/examples/)

   - V 1. requestu žádáme o vytvoření procedurálního portálu. Důležité vstupní parametry:
     - `sdg:ProceduraSdg` – zatím dostupná pouze testovací procedura s kódem `00`
     - `sdg:CallBackAddress` – adresa, kam bude uživatel po dokončení procesu přesměrován

   - Výstupem tohoto requestu je:
     - `sdg:SdgRequestId` – unikátní identifikátor žádosti
     - `sdg:RedirectUrl` – URL pro přesměrování uživatele

   - Uživatel následně projde procedurálním portálem (využijte **testovací identity NIA**)

   - Po dokončení procesu následuje 2. request:
     - Parametr `sdg:SdgRequestId` opět použijeme ke zjištění stavu a stažení důkazů

---

🛈 Tento návod slouží k základní orientaci a doporučené praxi pro vývoj a integraci. Detailní instrukce jsou dostupné ve videoukázce.
