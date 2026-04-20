# iGEM2026  

## 🔬 Overview  

Under `\Repos\`, there are several external GitHub repositories relevant to our project.  
These can be roughly divided into four categories:

1. **Ultrasound Acquisition (Verasonics)**  
2. **Physics & Simulation**  
3. **Image Analysis & Tracking**  
4. **Machine Learning / Enhancement**  

The long-term goal is to combine these tools into a unified pipeline:

**Simulation → Verasonics Acquisition → Signal Processing → Image Analysis → ML (optional)**  

---

## 📁 Repositories  

### 🟢 1. Ultrasound & Verasonics  

#### `Acoustic plate reader`  
- Source: Shapiro Lab  
- Content: Hardware + Verasonics setup for ultrasound measurements  
- Relevance for us:  
  - Understanding experimental setups  
  - Potential inspiration for our own hardware / measurement design  

---

#### `xAM-imaging`  
- Source: Maresca Lab  
- Content: xAM (cross-Amplitude Modulation) imaging for Gas Vesicles  
- Function:  
  - Selective visualization of GVs  
  - Suppresses tissue signal → primarily displays GV signal  
- Relevance for us:  
  - **Central to our project**  
  - Enables direct visibility of GV signals  
  - Foundation for future multiplexing (different collapse pressures)  

---

#### `VerasonicsPhantomSequences`  
- Content: Shear Wave Elastography (SWEI) sequences + analysis  
- Function:  
  - Measures motion in tissue  
  - Computes physical parameters (e.g., stiffness)  
- Relevance for us:  
  - Demonstrates how to **extract physical information from ultrasound**  
  - Strong reference for tracking and quantitative analysis  

---

### 🔵 2. Simulation & Physics  

#### `fem`  
- Content: Simulation of tissue behavior under ultrasound forces (ARF)  
- Function:  
  - Models motion induced by ultrasound  
  - Provides ground truth (displacement fields)  
- Relevance for us:  
  - Understanding the physics behind ultrasound  
  - Basis for simulating GV behavior  

---

#### `ultratrack`  
- Content: Ultrasound simulation + tracking  
- Function:  
  - Generates RF data based on simulated motion  
  - Tests tracking algorithms  
- Relevance for us:  
  - Enables development & validation of tracking methods  
  - Can provide synthetic training data  

---

### 🟡 3. Image Analysis & Machine Learning  

#### `cyclegan_verasonics`  
- Content: ML pipeline (U-Net + CycleGAN) for ultrasound images  
- Function:  
  - Improves image quality (plane-wave → clinical quality)  
  - Integrates directly into the Verasonics workflow  
- Relevance for us:  
  - Can reduce image noise  
  - Improves GV visibility (optional)  

