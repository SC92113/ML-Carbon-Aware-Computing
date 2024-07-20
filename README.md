# ML-Carbon-Aware-Computing

### 🛠️ This project is supported by [DeepLearning.AI](https://www.deeplearning.ai/) and [Google Cloud](https://cloud.google.com/).

### 🎯 Goal
- **Perform low carbon training by using real time carbon intensity**

  1. Set up Google Cloud account
  2. Initialize Vertex AI application
  3. Set up training environment and import libraries
  4. Load Electricity Map carbon intensity API
  5. Select a training location with lowest carbon intensity
     - Method 1: Select a training location based on public carbon intensity reference page
     - Method 2: Define a cleanest function to select a training location from the region list by API
  5. Define task.py
  6. Define storage bucket
  7. Define custom training job
  8. Train model
  9. Delete storage bucket

- **Quick access to notebook: here**

### 💡 Key concepts in the project

- **Carbon emission formula**
  - Amount of carbon used in machine learning workload = Carbon intensity * Amount of Energy used in machine learning workload

- **Energy used in machine learning lifecycle**
  - Hardware
    - CPU, GPU, data center
  - Training
    - Pre-training, fine-tuning
  - Inference
    - Serve and interact with users in real time

- **Carbon aware solutions**
  - Compute in low carbon regions which have renewable energy sources (refer to notebook)
    - Factors to be considered when selecting low carbon training locations
      - Cost
      - Security
      - Performance latency
  - Compute in the time with most renewable energy generated
  - Choose cloud provider with low power usage effectiveness (PUE)/ internal energy consumption of data center
    - e.g. Google has multiple data centers around the world showing Carbon Free Energy Percentage (CFE%) for user references
  - Choose efficient hardware such as GPU and TPU
  - Compute with special purposes through model pretraining/ model resizing

- **API call of Electricity Map**
  - Carbon intensity and power breakdown request of a training location in one step

### 📚 References
- Electricity Map global carbon intensity: [Global carbon intensity (real time)](https://app.electricitymaps.com/map)
- Electricity Map API portal: [Free personal tier API](https://api-portal.electricitymaps.com/)
- Google Cloud region picker: [Region picker](https://cloud.withgoogle.com/region-picker/?_ga=2.35602913.1900645210.1721376901-275758419.1721116042&_gac=1.18114251.1721116042.CjwKCAjwtNi0BhA1EiwAWZaANCLZ8IKpUZPtW7lXpRlVVzAxdVYIcl4WIDGgmZ1absGbuyxsrl_qihoCG5MQAvD_BwE&_gl=1*1014ysf*_ga*Mjc1NzU4NDE5LjE3MjExMTYwNDI.*_ga_WH2QY8WWF5*MTcyMTM3NjkwMS4yLjEuMTcyMTM3NjkwNi41NS4wLjA.)
- Google Cloud global carbon intensity: [Global carbon intensity (by batch)](https://cloud.google.com/about/locations#americas)
- Google Cloud Vertex AI services: [Vertex AI](https://cloud.google.com/generative-ai-studio?utm_source=google&utm_medium=cpc&utm_campaign=japac-SG-all-en-dr-SKWS-all-all-trial-DSA-dr-1605216&utm_content=text-ad-none-none-DEV_c-CRE_655856180858-ADGP_Hybrid+%7C+SKWS+-+BRO+%7C+DSA+-All+Webpages-KWID_39700076131768290-dsa-1456167871416&userloc_9061591-network_g&utm_term=KW_&gad_source=1&gclid=CjwKCAjwnei0BhB-EiwAA2xuBjJZ-_1bJZ_qzmYnpLXxYPODCDMqgW6E3YAddmZEx_uyvKtS5bc2OhoCYhAQAvD_BwE&gclsrc=aw.ds&hl=en)
- Alternative of energy data API: [WattTime Data API (V3)](https://docs.watttime.org/)

### 🔎 Research papers
  - [Power_Hungry_Processing_Watts_Driving_the_Cost_of_AI_Deployment.pdf](https://github.com/SC92113/ML-Carbon-Aware-Computing/blob/83d61dd6cadd68b0c9e06208c0ddbd2c2b5b0dae/Power_Hungry_Processing_Watts_Driving_the_Cost_of_AI_Deployment.pdf)
  - [Measuring_the_Carbon_Intensity_of_AI_in_Cloud_Instances.pdf](https://github.com/SC92113/ML-Carbon-Aware-Computing/blob/83d61dd6cadd68b0c9e06208c0ddbd2c2b5b0dae/Measuring_the_Carbon_Intensity_of_AI_in_Cloud_Instances.pdf)
  - [Making_AI_Less_Thirsty_Uncovering_and_Addressing_the_Secret_Water_Footprint_of AI_Models.pdf](https://github.com/SC92113/ML-Carbon-Aware-Computing/blob/83d61dd6cadd68b0c9e06208c0ddbd2c2b5b0dae/Making_AI_Less_Thirsty_Uncovering_and_Addressing_the_Secret_Water_Footprint_of%20AI_Models.pdf)
