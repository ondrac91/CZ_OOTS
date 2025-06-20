# Prerekvizity k připojení

Níže jsou uvedeny požadavky pro připojení k CMS a komunikaci s AIS v rámci systému OOTS.

## 1. Připojení k CMS

- Základní požadavek pro zahájení komunikace v rámci systému OOTS. Respektive pro komunikaci ISSS.

## 2. Certifikáty pro komunikaci s ISSS (RAZR)

- Je nutné zajistit platné certifikáty pro zabezpečenou komunikaci s informačním systémem sdílených služeb (ISSS).
(
## 3. Požádat o práva pro komunikaci s AIS 10339  
_(Vyřešeno centrálně pro všechny VVŠ)_
- Ty jsou aktuálně z důvodu testování nahlášené pro agendu A3791 a činnostní roli CR44328

## 4. Testování připojení

- Pro ověření nastavení a komunikace lze využít aplikaci **Testovací AIS**.
- Je třeba použít činnostní roli CR44328, agendu A3791 a kontext kód A12251.1

> ⚠️ **Je třeba mít přiřazenou roli v JIP** (Jednotný identitní prostor).



# Postup pro testovací připojení k OOTS-CZ přes CMS

Tento návod shrnuje doporučený postup pro nastavení testovacího připojení k systému OOTS-CZ přes rozhraní ISSS. Doporučujeme zároveň sledovat dostupnou videoukázku, která celý proces ilustruje nejpřehledněji.

## 📋 Postup

1. **Připravte si ID vašeho AIS v systému RPP**  
   Spolu s tím i číslo OVM – tedy **IČ organizace**.

2. **Získejte testovací certifikát pro komunikaci s CMS**  
   Certifikát musí být určen pro přístup do testovacího prostředí CMS.

3. **Cílový AIS**  
   Pro účely volání využijte identifikátor AIS: **10339**

4. **Používaná agenda a kontext**  
   - **Agenda:** `A3791`  
   - **Činnostní role:** `CR44328`  
   - **Kontextový kód:** `A12251.1`

5. **Volání přes CMS**  
   Pro testování doporučujeme používat tzv. **testovací AIS**, který je dostupný v rámci CMS. Příklady volání naleznete ve složce [📂 Složka s příklady](examples/)

6. **Přihlašování přes NIA (testovací režim)**  
   Využívejte **testovací identity** dostupné v rámci NIA testovacího prostředí.

---

🛈 Tento návod slouží k základní orientaci a doporučené praxi pro vývoj a integraci. Detailní implementační instrukce jsou dostupné ve videoukázce.
