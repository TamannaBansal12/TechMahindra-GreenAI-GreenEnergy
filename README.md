# TechMahindra-GreenAI & Green Energy
Agentic AI for Deploying Green AI in Business Workflows

Goal:
Build an AI system (agent) that works with business tools like CRMs or ERPs 
and helps replace heavy AI models with lighter, more energy-efficient 
ones — without hurting performance.

 Steps of Development
 1.Pick Common AI Use Cases
   1. Choose 2–3 tasks often used in businesses:
      1. Email classification
      2. Text summarization
      3. Sentiment analysis
         
   2.Analyze Energy Usage of Current Tools
      1. Measure how much energy these AI tools consume.
      2. Tools like CodeCarbon or model benchmarks can help estimate this.
      
   3.Build the Smart Agent
      1. Use LangChain to design an agent that:
          1. Understands the business task
          2. Suggests or replaces models with greener options (e.g., distilled 
or quantized models)

   4.Integrate into Workflow
      1. Use tools like Zapier or Make to connect the agent with CRM/ERP 
systems.
      2. Simulate workflows where AI tasks happen (e.g., auto-summarize 
customer emails).

   5.Test and Report Improvements
      1. Show how the new model:
          1. Performs on the task
          2. Saves compute and energy
          3. Keeps accuracy at a usable level
          
   6.Build a Dashboard
      1. Use Streamlit to display:
          1. Current vs. optimized energy usage
          2. Suggested model swaps
          3. Impact over time

![TechStack](https://github.com/user-attachments/assets/926d01bd-2376-410e-a113-94ff98efb16c)

Solution & Evaluation

The system incorporates pre-trained models sourced from HuggingFace's Model Hub, focusing on those that are distilled or quantized to maintain high efficiency without significantly compromising summarization quality.
•	Dynamic Model Selection Strategy:
The core innovation of this system is its dynamic agent that selects a summarization model based on input characteristics and efficiency goals. This allows real-time decision-making for optimal carbon and performance trade-offs.
o	t5-small: Chosen for very short texts due to its minimal compute footprint.
o	distilbart-cnn-12-6: Balances performance and efficiency for medium-sized texts.
o	facebook/bart-large-cnn: Used selectively for long and complex texts, only when the additional cost is justified by a significant gain in performance.

•	Static Model Baseline:
For comparison, a static pipeline using only distilbart-cnn-12-6 is implemented. This reflects common business usage where simplicity is prioritized but may lead to inefficiencies when handling varied input types.


![System Architecture](https://github.com/user-attachments/assets/7afc056a-0ad3-47ed-ab60-5bcacbe19217)

![image](https://github.com/user-attachments/assets/75ec4158-446f-43d2-9902-a8efe2e669ce)

Energy Efficiency and Emission Savings
One of the strongest justifications for the dynamic model lies in its energy efficiency. Since the agent selects models based on text length and emission profile:
•	Tasks that used t5-small saw emissions drop by up to 65% compared to using distilbart for the same task.
•	Overall, dynamic routing saved ~35–40% of total emissions over a fixed static pipeline across the dataset.

![image](https://github.com/user-attachments/assets/7f18abc3-fe05-48ec-8fec-0447d6c54fe2)

![image](https://github.com/user-attachments/assets/5220ffb6-c8ad-4696-9fcb-3dcba3d5c161)

![image](https://github.com/user-attachments/assets/ba19ec2d-074c-4e62-acc3-c52f005f88c0)

