# Anuvad 🌐 🗣️ : The bridge between you and the world.
A Gemini-Nano-Based Translations App

![Anuvad - Logo](https://github.com/user-attachments/assets/23a1565d-68ab-44c1-986d-27dbaa2852bb)

# Problem Statement 🛠️
In an increasingly globalized world, seamless translation across languages is essential for communication, accessibility, and collaboration. However, most translation applications rely heavily on cloud-based models, leading to latency, privacy concerns, and the need for constant internet connectivity. There is a growing need for a fast, reliable, and offline-capable translation solution that leverages on-device AI to offer instant results with enhanced privacy.

# Proposed Solution 💡
Anuvad is an innovative translations app powered by the on-device Gemini Nano model (supported in Chrome 127+). Anuvad allows users to translate both text and voice inputs without the need for an active internet connection, ensuring:

- **Low Latency**: Instant translations without network delays.  
- **Enhanced Privacy**: Data never leaves the device, ensuring user privacy.  
- **Accessibility**: Usable even in offline environments where connectivity is limited or unavailable.

# How Does It Work? 📸
1. **On-Device AI Model**:  
   Anuvad uses the **Gemini Nano** model, which runs directly on your device. This eliminates the need for cloud-based processing.  

2. **Text and Voice Input**:  
   - Users can input text for translation.  
   - Alternatively, users can speak into the app, and it will detect, process, and translate the voice input.  

3. **Chrome Compatibility**:  
   - The app requires **Chrome version 127 or higher** with AI preview features enabled.

## **Technology Stack 🔧**  
**Anuvad** leverages cutting-edge technologies to deliver an optimized translation experience:
- 🤖 **Gemini Nano Model**: On-device language model for translation.
- 🌐 **Chrome API (v127+)**: Provides access to the AI and optimization guides.
- 💻 **JavaScript**: Handles core functionality and interaction with the AI model.
- 🎨 **HTML & CSS**: Provides a user-friendly interface for text and voice input.
- 🎙️ **Web Speech API**: Captures and processes voice input for translation.
- 🛠️ **Chrome DevTools**: Verifies and manages the AI model's capabilities.


## **Quick Implementation**  

### **Prerequisites**  
1. **Chrome Version**:  
   Install **Chrome 127+** (available in Dev or Canary channels). Stable release expected on **July 17, 2024**.  

### **Enable Necessary Flags**  
To enable on-device AI, follow these steps:  

1. Open **Chrome Flags** (`chrome://flags/`) and enable the following:  
   - `#prompt-api-for-gemini-nano`: **Enabled**  
   - `#optimization-guide-on-device-model`: **Enabled (BypassPrefRequirement)`  
   
2. Navigate to **chrome://components/** and click on **Optimization Guide On Device Model** to download the model.  

3. Disable the Text Safety Classifier:  
   - `chrome://flags/#text-safety-classifier`: **Disabled**  

### **Verifying Installation**  
1. Open Chrome DevTools and run the following command to initialize the AI model:  
   ```javascript
   await ai.languageModel.create();
Verify that the model is available:
javascript
Copy code
(await window.ai.languageModel.capabilities()).available
If the output is 'readily', you're all set!

# Impact 🌍
Anuvad addresses key challenges in the translation space by:

- 🏋️ Empowering Users: Provides translation capabilities even without internet access.
- 🔒 Enhancing Privacy: All translations happen on-device, ensuring sensitive data remains secure.
- 📡 Improving Accessibility: Allows users in remote areas with limited connectivity to access translation services.

# Scalability 📈
Anuvad can scale across various use cases, such as:

- 🧳 Personal Use: Offline translation for travelers, students, and language learners.
- 💼 Business Applications: Instant translations during meetings, conferences, or client interactions.
- 🏛️ Government & NGOs: Providing translation services in remote areas without reliable internet access.

# Business Relevance 🤝
With its offline-first, privacy-focused approach, Anuvad aligns with:

- 📜 Data Privacy Regulations: Ensures compliance with laws like GDPR by keeping translations on-device.
- 🏢 Enterprise Use: Offers a secure alternative for sensitive business communications.
- 🌏 Emerging Markets: Serves regions with limited internet infrastructure, tapping into a vast, underserved user base.

# Future Scope 🚀
Anuvad's development roadmap includes:

- 🌐 Support for Additional Languages: Expanding language options to cater to a broader audience.
- 🎙️ Voice-to-Text Customization: Enhancing voice input accuracy with regional dialect support.
- 🔗 Integration with Other Platforms: Extending compatibility beyond Chrome to mobile and desktop applications.
- 📈 AI Model Updates: Leveraging future versions of the Gemini Nano model for improved translation accuracy and speed.

# Testing 
## Enable Required Chrome Flags
To access the AI capabilities needed for **Anuvad**, enable the following flags in Chrome:

1. **Enable Prompt API for Gemini Nano**:
   - Open Chrome and navigate to:  
     `chrome://flags/#prompt-api-for-gemini-nano`  
   - Set it to **Enabled**.

2. **Enable Optimization Guide On-Device Model**:
   - Open Chrome and navigate to:  
     `chrome://flags/#optimization-guide-on-device-model`  
   - Set it to **Enabled BypassPrefRequirement**.

3. **Disable Text Safety Classifier**:
   - Open Chrome and navigate to:  
     `chrome://flags/#text-safety-classifier`  
   - Set it to **Disabled**.

4. **Download the Optimization Guide Model**:
   - Navigate to:  
     `chrome://components/`  
   - Find **Optimization Guide On Device Model** and click **Update** to download the required model.

---

### 3. Verify Model Availability

1. Open **Chrome DevTools**:  
   Press `Ctrl + Shift + I` (Windows) or `Cmd + Shift + I` (Mac).

2. In the **Console**, run the following command:
   ```javascript
   await ai.languageModel.create();
