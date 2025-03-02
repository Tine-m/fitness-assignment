# 📌 **Obligatorisk afleveringsopgave: Databasedesign af Fitnesscenter (Assignment 2 - 10 study points)**

## **🎯 Opgavens Formål**
Denne opgave har til formål at træne dig i **datamodellering**, **normalisering** og **mapping til en relationel model**. 
Du skal udarbejde en **ER-model for et fitnesscenter**, normalisere den ved at anvende **1., 2. og 3. normalform (evt. også BCNF)**, og derefter konvertere den til en **relationel model**.

---

## **📌 1️⃣ ER-Modellering**
### **📖 Baggrund**
Fitnesscentret tilbyder **medlemskaber**, **holdtræning**, og har **instruktører**, der underviser på holdene. Centret vil registrere, hvilke medlemmer der deltager på hvilke hold, samt hvilke instruktører der er tilknyttet hvilke hold.

### **🏋️ Nøglefunktioner i systemet**
- **Medlemskaber:** Basis, Premium, Elite – med forskelle i adgang til faciliteter.
- **Træningshold:** Spinning, CrossFit, Yoga m.m. – hvor medlemmer kan tilmelde sig.
- **Instruktører:** Tilknyttet hold og kan administrere deltagerlister.
- **Booking:** Medlemmer kan booke pladser på hold eller personlig træning. Hold har typisk begrænset antal pladser.
- **Betaling:** Månedsvis abonnement eller klippekort.
- **Medlemsrabatter:** Kan gives i særlige tilfælde.

📌 **Din opgave:**
1. Identificér de **entiteter**, der er relevante for fitnesscentret.
2. Definér **attributter** for hver entitet.
3. Identificér **relationer og multiplicitet** mellem entiteterne.
4. Tegn et **ER-diagram** (håndtegnet eller ved hjælp af et værktøj som dbdiagram.io, Lucidchart eller MySQL Workbench).

---

## **📌 2️⃣ Normalisering af ER-modellen**
Når du har udarbejdet din **ER-model**, skal du som kvalitetstjek (for at undgå dataredundans og opdateringsanomalier) gennemgå modellen **trinvist** fra **1. normalform (1NF)** til **3. normalform (3NF)**.

📌 **Din opgave:**
1. **1NF:** Sikr dig, at alle attributter er **atomare** og at der ikke er gentagne grupper.
2. **2NF:** Fjern **partielle funktionelle afhængigheder** (sørg for, at ikke-nøgle attributter afhænger af hele primærnøglen).
3. **3NF:** Fjern **transitive afhængigheder** (sørg for, at alle ikke-nøgle attributter kun afhænger af primærnøglen).

🔹 **Dokumentér hver normaliseringstrin med en kort forklaring og en tabel, der viser ændringerne.**

---

## **📌 3️⃣ Mapping til Relationel Model**
Når din **ER-model er normaliseret**, skal du **mappe den til en relationel model**.

📌 **Din opgave:**
1. Definér **relationer** (tabeller) med **primærnøgler (PK) og fremmednøgler (FK)** og angiv for ikke-nøgle attributter constraints som **NOT NULL** eller **unik**.
2. Identificér nødvendige **datatyper** (f.eks. INT, VARCHAR, DATE, DECIMAL).
3. Dokumentér resultatet som en **relationsmodel**, f.eks.:

```
MEMBER (member_id PK, name VARCHAR(100), start_date DATE, membertype ENUM('Basis', 'Premium', 'Elite'))
TEAM (team_id PK, description VARCHAR(50), max_participants INT, instructor_id FK)
```

---

## **📌 Aflevering**
### **📁 Du skal aflevere:**
1. **ER-diagram** (håndtegnet eller digitalt) med evt. overvejelser og kommentarer til jeres design.
2. **Dokumentation for normalisering** (fra 1NF til 3NF, inkl. forklaringer og tabeller).
3. **Den relationelle model** (relationer med PK, FK, datatyper og unikke attributter).
   

---

## **📌 Vurderingskriterier**
| **Kriterie** | **Vurdering** |
|-------------|--------------|
| ER-model | Identificering af entiteter, attributter og relationer |
| Normalisering | Rigtig anvendelse af 1NF, 2NF og 3NF |
| Relationel model | Korrekt mapping af entiteter til relationer |
| Dokumentation | Klar og præcis beskrivelse af processen |

---

🎯 **God fornøjelse med opgaven!** 🚀
