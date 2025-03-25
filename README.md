# Enterprise-Customer-Support-System
# Customer Support Chatbot

## Overview
This project is a **Customer Support Chatbot** that leverages **LangChain, FAISS, and Groq's Llama 3 model** to assist users with product-related inquiries. The chatbot provides answers to frequently asked questions (FAQs), troubleshooting guidance, and general product information by retrieving relevant knowledge from indexed product files.

## Features
- **Product Knowledge Base**: Stores product details, FAQs, and troubleshooting instructions.
- **Fast Information Retrieval**: Uses **FAISS** for vector-based search.
- **Memory Retention**: Tracks conversation history for contextual responses.
- **AI-Powered Responses**: Uses **Llama 3 from Groq** for natural language understanding and generation.
- **Structured JSON Output**: Provides a detailed response with relevant context, FAQs, and troubleshooting steps.

## Dependencies
Make sure you have the following dependencies installed:

```bash
pip install faiss-cpu langchain langchain-community langchain-groq transformers sentence-transformers
```

## Setup Instructions
1. **Clone the Repository**:
   ```bash
   git clone https://github.com/your-repo/customer-support-chatbot.git
   cd customer-support-chatbot
   ```
2. **Set Up API Key**:
   - The chatbot requires a Groq API key.


## Example Usage Scenarios
### Scenario 1: Asking for Product Setup Instructions
**User:** "How do I connect my SmartSpeaker X100 to WiFi?"

**Chatbot Response:**
```json
{
  "query": "How do I connect my SmartSpeaker X100 to WiFi?",
  "context": "To connect your SmartSpeaker X100 to WiFi, open the mobile app, navigate to settings, select 'Network', and follow on-screen instructions.",
  "response": "To connect your SmartSpeaker X100, open the app, go to settings, select WiFi, and enter credentials.",
  "faq_answer": "You can connect the SmartSpeaker X100 by opening the app, going to settings, and selecting 'WiFi setup'.",
  "troubleshooting": "Ensure your router is turned on, move closer to the router, and restart the device."
}
```

### Scenario 2: Troubleshooting an Issue
**User:** "My SmartSpeaker X100 won't turn on. What should I do?"

**Chatbot Response:**
```json
{
  "query": "My SmartSpeaker X100 won't turn on. What should I do?",
  "context": "If your SmartSpeaker X100 does not turn on, check if it's plugged into a power source. Try a different power adapter.",
  "response": "Ensure your SmartSpeaker X100 is plugged in. If the issue persists, try a different power adapter.",
  "faq_answer": "Check the power source and adapter connection. If the problem continues, contact support.",
  "troubleshooting": "Unplug the device for 30 seconds, plug it back in, and press the power button."
}
```
