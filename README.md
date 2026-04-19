# iGEM2026

## 🔬 Überblick

Unter `\Repos\` finden sich verschiedene externe GitHub-Repositories, die für unser Projekt relevant sind.  
Diese lassen sich grob in vier Kategorien einteilen:

1. **Ultraschall Acquisition (Verasonics)**
2. **Physik & Simulation**
3. **Image Analysis & Tracking**
4. **Machine Learning / Enhancement**

Ziel ist es, diese Tools langfristig zu einer gemeinsamen Pipeline zu kombinieren:

Simulation → Verasonics Acquisition → Signal Processing → Image Analysis → ML (optional)

---

## 📁 Repositories

### 🟢 1. Ultraschall & Verasonics

#### `Acoustic plate reader`
- Quelle: Shapiro Lab  
- Inhalt: Hardware + Verasonics Setup für Ultraschallmessungen  
- Nutzen für uns:
  - Verständnis von experimentellen Setups
  - mögliche Inspiration für eigene Hardware / Messaufbau  

---

#### `xAM-imaging`
- Quelle: Maresca Lab  
- Inhalt: xAM (cross-Amplitude Modulation) Imaging für Gas Vesicles  
- Funktion:
  - selektive Visualisierung von GVs
  - unterdrückt Gewebesignal → zeigt hauptsächlich GV Signal  
- Nutzen für uns:
  - **zentral für unser Projekt**
  - ermöglicht direkte Sichtbarkeit von GV-Signalen
  - Grundlage für späteres Multiplexing (verschiedene Collapse-Drücke)

---

#### `VerasonicsPhantomSequences`
- Inhalt: Shear Wave Elastography (SWEI) Sequenzen + Auswertung  
- Funktion:
  - misst Bewegung im Gewebe
  - berechnet physikalische Parameter (z. B. Steifigkeit)  
- Nutzen für uns:
  - zeigt, wie man **physikalische Information aus Ultraschall extrahiert**
  - gute Referenz für Tracking und quantitative Analyse  

---

### 🔵 2. Simulation & Physik

#### `fem`
- Inhalt: Simulation von Gewebeverhalten unter Ultraschallkräften (ARF)  
- Funktion:
  - modelliert Bewegung durch Ultraschall
  - liefert Ground Truth (Displacement Felder)  
- Nutzen für uns:
  - Verständnis der Physik hinter Ultraschall
  - Grundlage für Simulation von GV-Verhalten  

---

#### `ultratrack`
- Inhalt: Ultraschall-Simulation + Tracking  
- Funktion:
  - generiert RF-Daten basierend auf simulierten Bewegungen
  - testet Tracking-Algorithmen  
- Nutzen für uns:
  - erlaubt Entwicklung & Validierung von Tracking-Methoden
  - kann synthetische Trainingsdaten liefern  

---

### 🟡 3. Image Analysis & Machine Learning

#### `cyclegan_verasonics`
- Inhalt: ML Pipeline (U-Net + CycleGAN) für Ultraschallbilder  
- Funktion:
  - verbessert Bildqualität (Plane-wave → klinische Qualität)
  - läuft direkt im Verasonics Workflow  
- Nutzen für uns:
  - kann Bildrauschen reduzieren
  - verbessert GV-Sichtbarkeit (optional)

---

## 🧠 Wie das alles zusammenpasst

Langfristig könnten wir folgende Pipeline aufbauen:

(1) Simulation  
    fem → ultratrack  
        ↓  
(2) Experiment  
    Verasonics + xAM-imaging  
        ↓  
(3) Analyse  
    Tracking / Segmentation  
        ↓  
(4) ML (optional)  
    cyclegan / andere Modelle  

---

## 🚀 Wichtigste Takeaways

- **xAM-imaging** ist der Schlüssel für GV-Sichtbarkeit  
- **VerasonicsPhantomSequences** zeigt, wie man Bewegung analysiert  
- **ultratrack + fem** helfen uns, Methoden vorab zu testen  
- **cyclegan** ist optional für bessere Bildqualität  

---

## 📌 Nächste Schritte (Vorschlag)

- [ ] xAM Pipeline verstehen und testen  
- [ ] einfache Tracking-Methode implementieren  
- [ ] Simulation (ultratrack) für erste Tests nutzen  
- [ ] entscheiden, ob ML notwendig ist  