# L'Arquitectura del Coneixement del Projecte Arca

Aquest document defineix l'estructura fonamental i els protocols que governen l'organització del coneixement dins del projecte. És una guia essencial per a tots els col·laboradors.

## 1. El Sistema d'Identificació de Lloses (ID Únic)

Cada llosa té un identificador únic seguint el format jeràrquic: **`SEC.SUB.ID`**.

*   **`SEC` (Secció):** Un número de 01 a 12 que correspon a les categories principals del projecte (01-Llenguatge, 02-Supervivència, , etc.).
*   **`SUB` (Subsecció):** Un número que agrupa un tema concret dins d'una secció (p. ex., 03.01 per a Aritmètica dins de Matemàtiques).
*   **`ID` (Identificador):** Un número seqüencial per a cada llosa dins de la seva subsecció.

Aquest sistema garanteix que cada peça de coneixement tingui un lloc clar i escalable.

## 2. El Graf de Coneixement: Dependències

El projecte no és un llibre lineal, sinó un **graf de coneixement**. Per entendre una llosa, cal haver assimilat els conceptes de les seves lloses "mare" o dependències.

*   **Definició:** Cada arxiu de llosa ha d'incloure una secció de metadades ("front matter") al principi, on s'especifiquen les seves dependències.
*   **Sintaxi:**
    ```yaml
    ---
    id: [ID_de_la_llosa_actual]
    title: "[Títol de la llosa]"
    dependencies:
      - [ID_de_la_primera_dependencia]
      - [ID_de_la_segona_dependencia]
    ---
    ```
*   **Objectiu:** Aquesta estructura permetrà, en un futur, generar mapes visuals d'aprenentatge i garantir la cohesió lògica del projecte.

## 3. Tipus de Contribucions

*   **Proposta de Llosa:** Una proposta completa per a una nova llosa, seguint la plantilla corresponent a les "Issues". Ha d'incloure un ID proposat i una llista de dependències.
*   **Proposta de Concepte:** Una idea més petita que no constitueix una llosa sencera (un pictograma, una metàfora visual, etc.). Es proposa mitjançant una "Issue" amb l'etiqueta `concepte` per a la seva discussió.
*   **Millora o Error:** Un canvi sobre una llosa ja existent. Es gestiona a través de la seva plantilla d'Issue.

---
*Aquest document és un document viu i pot ser modificat mitjançant el consens de la comunitat.*

[Tornar a l'inici](/wiki/)
