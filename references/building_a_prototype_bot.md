# Building a Prototype: Customer Support Bot

## Introduction: Empowering Customer Support with AI-Driven Chatbots
Welcome to this hands-on lesson where we will build a functional prototype of a customer support chatbot. In today's competitive landscape, exceptional customer service is paramount. AI-powered chatbots offer a scalable and efficient way to handle customer inquiries, resolve issues, and provide instant support. This lesson bridges the gap between theoretical prompt engineering concepts and practical application by guiding you through the development of a customer support bot. We will leverage the power of prompt engineering to design intelligent conversational flows, manage context, and integrate with basic user interfaces. By the end of this session, you will have a working prototype and a deeper understanding of how to apply prompt engineering to solve real-world business challenges, develop end-to-end AI solutions, and integrate AI models into existing workflows. This practical experience will also equip you to evaluate the impact of prompt engineering on project outcomes.

**Learning Objectives:**
*   Design effective prompts for handling Frequently Asked Questions (FAQs) and resolving customer issues.
*   Implement mechanisms for managing conversation history to maintain context.
*   Integrate the chatbot prototype with a simple user interface for interaction.
*   Develop strategies for handling customer support escalations to human agents.
*   Understand the iterative process of testing and refining chatbot prompts.
*   Considerations for using real-world data in chatbot development.

This lesson directly supports the module's learning objectives by providing a tangible project that demonstrates the application of prompt engineering in a business context. You will gain practical skills in building AI-powered solutions and integrating them into a functional prototype. The hands-on nature of this lesson will solidify your understanding of how prompt engineering can be a powerful tool for enhancing customer support operations.

## Section 1: Designing Prompts for FAQs and Issue Resolution
The foundation of any effective chatbot lies in its ability to understand and respond to user queries accurately and helpfully. For a customer support bot, this means meticulously crafting prompts that can address common questions and guide users through problem-solving steps. This section focuses on the art and science of designing prompts that are both comprehensive and context-aware, ensuring the chatbot provides relevant and actionable information.

### What are Prompts for FAQs and Issue Resolution?
Prompts in this context are the instructions and examples given to the AI model to elicit specific types of responses. For FAQs, prompts are designed to retrieve pre-defined answers based on keywords or intent. For issue resolution, prompts guide the AI to ask clarifying questions, diagnose problems, and suggest solutions. The goal is to create a conversational flow that mimics a helpful human support agent.

### Why are they Important?
Well-designed prompts are crucial for several reasons:
*   **Accuracy:** They ensure the chatbot provides correct information, reducing customer frustration.
*   **Efficiency:** They enable quick resolution of common issues, freeing up human agents for complex cases.
*   **User Experience:** They contribute to a smooth, natural, and helpful conversational experience.
*   **Brand Consistency:** They help maintain a consistent tone and messaging across all customer interactions.

### How to Implement: Designing Effective Prompts
The process involves several key steps:
1.  **Identify Common Queries:** Analyze historical support data (tickets, chat logs, emails) to identify the most frequent questions and recurring issues. Categorize these into FAQs and distinct problem types.
2.  **Define Bot Persona and Tone:** Decide on the chatbot's personality – friendly, professional, empathetic, etc. This will influence the language and style of your prompts.
3.  **Craft FAQ Prompts:** For FAQs, the prompt might look like this: "User asks: [User's question]. Provide the most relevant answer from the following knowledge base: [Knowledge Base Snippets]. If the question is not covered, state that you cannot find the answer." The key is to provide the AI with the context (user question) and the resources (knowledge base) to find the answer.
4.  **Develop Issue Resolution Prompts:** For troubleshooting, prompts need to guide the AI through a diagnostic process. This often involves a series of questions. Example: "User reports an issue: [User's problem description]. Ask clarifying questions to diagnose the root cause. Start by asking about [specific aspect of the problem]. If the user provides information, use it to ask the next relevant question. Aim to guide the user towards a solution."
5.  **Incorporate Examples (Few-Shot Learning):** Providing a few examples of user queries and desired chatbot responses within the prompt can significantly improve performance. This helps the AI understand the expected format and style of interaction.
6.  **Specify Output Format:** Clearly define how the chatbot should respond. For instance, "Respond in a concise, easy-to-understand manner. If providing steps, use numbered lists."
7.  **Handle Ambiguity and Out-of-Scope Queries:** Design prompts that instruct the bot on how to handle questions it cannot answer or that are outside its domain. This might involve politely stating limitations or offering to connect the user to a human agent.

### Real-world Examples and Scenarios:
Consider a telecommunications company's support bot. Common FAQs might include questions about billing cycles, data plans, or service outages. Issue resolution prompts could guide users through troubleshooting internet connectivity problems, setting up new devices, or resolving mobile app errors. For instance, a prompt for internet troubleshooting might start with: "User is experiencing slow internet. Ask the user to restart their modem and router. Then, ask if they have tried connecting via a wired connection. Based on their response, guide them to the next troubleshooting step."

The effectiveness of these prompts directly impacts the chatbot's utility. Investing time in their design and refinement is paramount for building a successful customer support solution.

## Section 2: Implementing Conversation History Management
A truly intelligent chatbot doesn't just respond to individual messages; it remembers the context of the ongoing conversation. This ability to maintain and utilize conversation history is critical for providing a natural, coherent, and personalized user experience. Without it, the chatbot would repeatedly ask for information the user has already provided, leading to frustration and inefficiency.

### What is Conversation History Management?
Conversation history management refers to the process of storing, retrieving, and utilizing previous turns in a dialogue between a user and a chatbot. This includes user inputs, chatbot responses, and any relevant metadata (like timestamps or user IDs). The AI model then uses this historical context to understand the current user query in relation to what has already been discussed.

### Why is it Important?
Effective conversation history management is vital for:
*   **Contextual Understanding:** It allows the chatbot to understand pronouns (e.g., 'it', 'that'), follow-up questions, and references to previous statements.
*   **Personalization:** By remembering user preferences or past issues, the chatbot can offer more tailored support.
*   **Reduced Redundancy:** Users don't have to repeat themselves, leading to a smoother and more efficient interaction.
*   **Complex Task Completion:** For multi-step processes or troubleshooting, remembering previous steps is essential.
*   **Improved AI Performance:** Providing the AI with conversational context can lead to more accurate and relevant responses.

### How to Implement: Strategies and Techniques
Implementing conversation history management typically involves a combination of backend logic and prompt engineering:
*   **Storing Conversation Turns:** Each user message and bot response pair needs to be stored. This can be done in memory for short-term sessions or in a database (like SQL, NoSQL, or even a simple file) for longer-term persistence.
*   **Context Window Limits:** Language models have a maximum token limit (context window) they can process at once. Sending the entire history of a long conversation will eventually exceed this limit.
*   **Truncation/Sliding Window:** Only send the most recent *N* turns of the conversation to the model. This is the simplest approach but can lose long-term context.
*   **Summarization:** Use another prompt to periodically summarize the older parts of the conversation. Send the summary along with the most recent turns. This retains key information while saving tokens.

## Section 3: Integrating with a Basic User Interface
To make our chatbot prototype truly functional, we need to connect the backend logic (where prompts are formatted, AI models are called, and conversation history is managed) to a front-end interface that the user sees and interacts with. This interface could be a web page, a mobile app, a messaging platform (like Slack or Teams), or, in our case, a simple command-line application.

### Why is it Important?
*   **Accessibility:** Allows users to easily input queries and receive responses.
*   **Testing and Iteration:** Provides a platform to test the chatbot's performance with real user inputs and gather feedback for prompt refinement.
*   **Demonstration:** Enables showcasing the chatbot's capabilities to stakeholders.
*   **User Experience:** A well-designed UI enhances the overall user experience, making the interaction intuitive and pleasant.

### How to Implement: A Python CLI Prototype
We will build a basic Python script that:
1.  Initializes the conversation history.
2.  Enters a loop to continuously prompt the user for input.
3.  Sends the user's input, along with the conversation history, to the AI model.
4.  Receives the AI's response.
5.  Updates the conversation history with both the user's input and the AI's response.
6.  Displays the AI's response to the user.
7.  Includes a mechanism to exit the loop.

**Prerequisites:**
*   Python installed on your system.
*   The `openai` Python library installed (`pip install openai`). You'll need an OpenAI API key.

**Python Code Structure:**

```python
import openai
import os

# --- Configuration ---
# Ensure you have your OpenAI API key set as an environment variable
# export OPENAI_API_KEY='your-api-key'
openai.api_key = os.getenv('OPENAI_API_KEY')

# --- Conversation Management ---
conversation_history = [
    {"role": "system", "content": "You are a helpful customer support assistant. Respond concisely and professionally."}
]

def add_message(role, content):
    conversation_history.append({'role': role, 'content': content})

def get_recent_history(max_turns=5):
    # Returns the last 'max_turns' user/assistant message pairs, plus the system message
    # We need to account for the system message and ensure we don't exceed token limits
    # For simplicity, we'll take the system message and the last N pairs.
    # A more robust solution would involve token counting.
    history_to_send = [conversation_history[0]] # Start with system message
    user_assistant_pairs = []
    
    for msg in conversation_history[1:]:
        user_assistant_pairs.append(msg)
        if len(user_assistant_pairs) == 2: # One user, one assistant message
            if len(history_to_send) + len(user_assistant_pairs) <= max_turns * 2 + 1: # +1 for system message
                history_to_send.extend(user_assistant_pairs)
            user_assistant_pairs = []
            
    # Add any remaining messages if the loop didn't complete a pair
    if user_assistant_pairs:
        if len(history_to_send) + len(user_assistant_pairs) <= max_turns * 2 + 1:
            history_to_send.extend(user_assistant_pairs)
            
    return history_to_send

# --- AI Interaction Function ---
def get_ai_response(user_input):
    add_message('user', user_input)
    
    # Get context, ensuring we don't overload the model's context window
    # Adjust max_turns based on your model's token limit and desired history depth
    context = get_recent_history(max_turns=10)
    
    try:
        response = openai.ChatCompletion.create(
            model="gpt-3.5-turbo", # Or gpt-4 if available
            messages=context
        )
        ai_message = response.choices[0].message['content'].strip()
        add_message('assistant', ai_message)
        return ai_message
    except Exception as e:
        print(f"Error communicating with OpenAI API: {e}")
        return "I'm sorry, I encountered an error. Please try again later."

# --- Main Chat Loop ---
def run_chatbot():
    print("Customer Support Bot: Hello! How can I assist you today? (Type 'quit' to exit)")
    while True:
        user_input = input("You: ")
        if user_input.lower() == 'quit':
            print("Customer Support Bot: Goodbye! Have a great day.")
            break
            
        bot_response = get_ai_response(user_input)
        print(f"Customer Support Bot: {bot_response}")

# --- Run the chatbot ---
if __name__ == "__main__":
    run_chatbot()
```

**Explanation of the Code:**
*   **Configuration:** Sets up the OpenAI API key. It's best practice to load this from environment variables for security.
*   **`conversation_history`:** A list that stores all messages. It starts with a system message defining the bot's role.

## Section 4: Strategies for Handling Escalations
Even the most sophisticated AI chatbots will encounter situations they cannot resolve. This could be due to a highly complex issue, a lack of access to specific data, or a user who is frustrated and demands to speak with a human. A robust customer support strategy must include clear and seamless escalation paths to human agents.

### Why is Escalation Management Important?
*   **Customer Satisfaction:** Prevents users from getting stuck in loops or receiving unhelpful automated responses.
*   **Issue Resolution:** Ensures complex problems are addressed by individuals with the necessary expertise and authority.
*   **Agent Efficiency:** By handling routine inquiries, the AI ensures human agents are only brought in when their skills are truly needed, optimizing their workload.
*   **Trust and Reliability:** Demonstrates that the company values the customer's problem and provides a safety net when automation falls short.

### Strategies for Effective Escalation:
*   **Explicit User Requests:** The most straightforward trigger is when a user explicitly asks for a human. Keywords like "agent", "human", "representative", or "escalate" should immediately trigger the process.
*   **AI Confidence Thresholds:** If the AI model returns a low confidence score for its intended response, or if it struggles to understand the user's intent after multiple clarifying questions, it should default to escalation.
*   **Sentiment Analysis:** Monitoring the tone of the user's messages. If the sentiment turns highly negative or frustrated, preemptive escalation can diffuse a tense situation.
*   **Complexity Triggers:** Certain predefined topics (e.g., security breaches, major account changes, legal inquiries) might be pre-programmed to always trigger an escalation.

### The Escalation Process:
1.  **Acknowledge and Inform:** When an escalation is triggered, the chatbot should clearly inform the user that they are being transferred and provide an estimated wait time if possible.
2.  **Transfer Context:** Crucially, the chatbot should pass the relevant conversation history and any gathered information (user ID, issue description, troubleshooting steps taken) to the human agent. This prevents the user from having to repeat themselves.
3.  **Implementation:** This context can be passed via API calls to a CRM system, a ticketing system, or directly into the agent's chat interface.
4.  **Seamless Handoff:** The transition should be as smooth as possible. The user should feel like they are continuing the conversation with a knowledgeable representative, not starting over.

**Python Implementation Snippet (Conceptual):**

```python
def check_for_escalation(user_input, conversation_history):
    # Simple keyword-based detection
    keywords = ['human', 'agent', 'representative', 'talk to someone']
    if any(keyword in user_input.lower() for keyword in keywords):
        return True
    
    # More advanced: check if AI is stuck or sentiment is negative
    # This would require more complex logic or additional AI calls (e.g., sentiment analysis)
    return False

def initiate_escalation(conversation_history):
    print("Customer Support Bot: I understand you need further assistance. Please wait a moment while I connect you to a human agent.")
    
    # In a real system, you would:
    # 1. Log the conversation history to a ticketing system.
    # 2. Notify an agent queue.
    # 3. Potentially provide an estimated wait time.
    # For this prototype, we'll just simulate the message.
    
    return "Escalation initiated. A human agent will be with you shortly."

# --- Inside the main chat loop (run_chatbot function) ---
# ... after getting user_input ...
        
        if check_for_escalation(user_input, conversation_history):
            escalation_message = initiate_escalation(conversation_history)
            print(f"Customer Support Bot: {escalation_message}")
            # Optionally, break the loop or transition to an agent-waiting state
            # For this prototype, we'll just inform the user and let them quit or continue
        else:
            bot_response = get_ai_response(user_input)
            print(f"Customer Support Bot: {bot_response}")

# ... rest of the loop ...
```

### Real-world Examples and Scenarios:
A user is trying to dispute a charge on their credit card. The chatbot can handle initial information gathering (transaction details, date), but when the user expresses strong disagreement or provides complex reasons, the chatbot recognizes this as a situation requiring human judgment and initiates an escalation. The entire chat log, including the user's dispute reason and the chatbot's attempts to clarify, is then sent to a specialized billing agent.

Another scenario: a user is trying to set up a complex enterprise software integration. The chatbot can guide through basic setup steps, but if the user encounters a highly specific configuration error or asks about advanced API usage, the chatbot offers to connect them to a technical support engineer who can provide in-depth assistance.

Implementing a seamless escalation process is key to a customer-centric AI support strategy, ensuring that users always have access to the right level of support when they need it.

## Section 5: Testing and Iterating on Prompts
Building a chatbot is not a one-time task; it's an iterative process. The effectiveness of your chatbot hinges on the quality of its prompts. Continuous testing and refinement of these prompts are essential to improve accuracy, enhance user experience, and adapt to evolving customer needs. This section focuses on the methodologies and best practices for testing and iterating on your chatbot prompts.

### What is Prompt Testing and Iteration?
Prompt testing involves systematically evaluating how well your prompts elicit the desired responses from the AI model. Iteration is the subsequent process of modifying and improving these prompts based on the insights gained from testing. This cycle of test-refine-test is fundamental to developing a high-performing AI application.

### Why is it Important?
*   **Accuracy and Relevance:** Ensures the chatbot provides correct and pertinent information.
*   **Robustness:** Helps identify and fix edge cases, ambiguities, and failure points in the AI's responses.
*   **User Experience:** Improves the naturalness, helpfulness, and overall satisfaction of the user interaction.
*   **Efficiency:** Reduces instances of incorrect answers, unnecessary escalations, or repetitive questions.
*   **Adaptability:** Allows the chatbot to handle new types of queries or adapt to changes in products, services, or policies.

### How to Implement: A Structured Approach to Testing
A systematic approach to testing and iteration involves several key stages:
1.  **Define Test Cases:** Create a comprehensive set of test cases that cover various scenarios:
    *   **Common FAQs:** Verify that standard questions are answered correctly.
    *   **Edge Cases:** Test unusual phrasing, typos, or slightly ambiguous queries.
    *   **Complex Queries:** Assess how the bot handles multi-part questions or nuanced issues.
    *   **Escalation Triggers:** Ensure that requests for human assistance are correctly identified.
    *   **Out-of-Scope Queries:** Check that the bot gracefully handles questions it's not designed to answer.
    *   **Conversational Flow:** Test multi-turn interactions to ensure context is maintained.
2.  **Establish Evaluation Metrics:** How will you measure success?
    *   **Accuracy:** Percentage of correct answers.
    *   **Relevance:** How well the response addresses the user's intent.
    *   **Completeness:** Whether the response provides all necessary information.
    *   **Conciseness:** Avoidance of overly verbose or redundant answers.
    *   **Tone:** Consistency with the defined bot persona.
    *   **Task Completion Rate:** For issue resolution, the percentage of issues successfully resolved by the bot.
    *   **Escalation Rate:** The frequency of unnecessary escalations.
3.  **Execute Tests:** Use your prototype (the Python CLI script) or a dedicated testing framework to run through your test cases. Record the user input, the AI's response, and your evaluation against the metrics.
4.  **Analyze Results:** Review the test results to identify patterns of failure or areas for improvement.
    *   **Common Issues:** Are there specific types of questions the bot consistently gets wrong?
    *   **Ambiguous Prompts:** Do certain prompts lead to unpredictable or incorrect outputs?
    *   **Context Loss:** Does the bot forget previous information in longer conversations?
5.  **Iterate on Prompts:** Based on the analysis, modify your prompts. This could involve:
    *   **Rewording:** Clarifying instructions or providing better examples.
    *   **Adding Constraints:** Specifying output formats or response lengths.
    *   **Adjusting Few-Shot Examples:** Providing more relevant or diverse examples.
    *   **Refining System Messages:** Enhancing the bot's persona or instructions.
    *   **Improving Context Management:** Adjusting the `max_turns` in `get_recent_history` or exploring summarization techniques.
6.  **Re-test:** After modifying prompts, re-run the relevant test cases to verify that the changes have had the desired effect and haven't introduced new problems.

### Hands-on Component: Testing Your Prototype
1.  **Prepare Test Cases:** Think of 5-10 specific questions or scenarios for your customer support bot. Include a mix of FAQs, troubleshooting requests, and perhaps a request to speak to a human.
2.  **Run the Python Script:** Execute your `customer_support_bot.py` script.
3.  **Input Test Cases:** Enter your prepared test cases one by one.
4.  **Record Observations:** For each input, note down:
    *   The exact user input.
    *   The bot's response.
    *   Whether the response was accurate, helpful, and appropriate.
    *   Any issues observed (e.g., irrelevant answer, repetition, failure to escalate).
5.  **Analyze and Refine:** Review your observations. If you notice a pattern (e.g., the bot struggles with questions about pricing), consider how you might adjust the prompts in the `conversation_history` initialization or within the `get_ai_response` function (though modifying the core prompts requires editing the script directly). For instance, if the bot isn't clear about pricing, you might add a more specific instruction in the system message: "When asked about pricing, clearly state the different tiers and what is included in each."
6.  **Re-test:** After making hypothetical prompt adjustments (or actual code changes if you're comfortable), re-run the problematic test cases to see if the responses have improved.

### Real-world Examples and Scenarios:
A company launches a new product feature. Initially, the chatbot might not handle questions about it well. Through testing, they discover users are asking specific questions about compatibility. They then iterate on the prompts, adding information about compatibility to the knowledge base snippets used in prompt construction or refining the system message to guide the AI on how to answer such queries. This iterative process ensures the chatbot remains a valuable resource as the product evolves.

Another example: A bank notices its chatbot frequently escalates queries about account closures, even when the user is just asking for information. By analyzing these interactions, they realize the prompt needs to better differentiate between asking *how* to close an account versus *wanting* to close an account immediately. They refine the prompt to guide the AI to provide information first, only escalating if the user explicitly states their intent to close.

Prompt testing and iteration are not optional; they are integral to delivering a high-quality AI-powered customer support experience.

## Section 6: Real-World Data Considerations for Chatbots
While we've focused on prompt engineering with general knowledge and simulated interactions, building a truly effective customer support chatbot for a specific organization requires careful consideration of real-world data. This data is the lifeblood of a specialized chatbot, enabling it to provide accurate, relevant, and context-aware support tailored to the organization's products, services, and customer base.

### What is Real-World Data in Chatbot Development?
Real-world data refers to the actual information generated by a company and its customers. This includes:
*   **Knowledge Bases:** FAQs, product manuals, troubleshooting guides, policy documents.
*   **Customer Interaction Logs:** Transcripts of past chat sessions, email support threads, call center notes.
*   **Product Catalogs:** Information about available products, services, pricing, and specifications.
*   **User Account Information:** (With appropriate privacy controls) Details about customer accounts, order history, service plans.
*   **Website Content:** Information available on the company's website.

### Why is it Important?
Leveraging real-world data is crucial for:
*   **Domain Specificity:** AI models are trained on vast general datasets, but they lack specific knowledge about your company's unique offerings and procedures. Real-world data bridges this gap.
*   **Accuracy and Relevance:** Ensures the chatbot provides answers that are specific to your business, not generic information.
*   **Personalization:** Enables the chatbot to access user-specific information (e.g., order status, account details) for tailored support.
*   **Efficiency:** Reduces the need for the AI to guess or provide overly general answers, leading to faster resolutions.
*   **Trust and Credibility:** Customers are more likely to trust a chatbot that demonstrates knowledge of their specific situation and company.

### How to Integrate Real-World Data: Techniques and Strategies
Several techniques can be employed to integrate real-world data into your chatbot:

1.  **Retrieval-Augmented Generation (RAG):** This is a powerful technique where the chatbot first retrieves relevant information from a knowledge base (your real-world data) and then uses that information to generate a response.
    *   **Process:**
        *   **Indexing:** Your knowledge base documents are processed and stored in a searchable format, often using vector embeddings in a vector database.
        *   **Retrieval:** When a user asks a question, the system searches the vector database for the most relevant document snippets.
        *   **Augmentation:** These retrieved snippets are then included in the prompt sent to the LLM.
        *   **Generation:** The LLM uses the provided snippets and its general knowledge to formulate a coherent and contextually relevant answer.
2.  **Fine-tuning (Less Common for Prompt Engineering Focus):** While prompt engineering is our primary focus, fine-tuning an LLM on your specific data can create a model highly specialized for your domain. However, this is more resource-intensive and complex than RAG.
3.  **API Integrations:** For dynamic data (like order status or account details), the chatbot needs to integrate with your company's internal APIs.
    *   **Process:** When the chatbot identifies a need for specific user data, it makes a call to the relevant internal API, retrieves the information, and then uses it to formulate a response or guide the user.
    *   **Prompt Engineering:** Prompts need to instruct the AI on when and how to request data from these APIs (often through function calling capabilities offered by LLM providers).
4.  **Structured Data Prompts:** For product information or pricing, you can embed structured data (like JSON or tables) directly into prompts or use RAG to retrieve it.

**Python Implementation Considerations (Conceptual):**
Integrating RAG typically involves libraries like LangChain or LlamaIndex, which abstract away much of the complexity of embedding, indexing, and retrieval. For API integrations, you would use standard Python libraries like `requests`.

```python
# Conceptual example using a hypothetical RAG system and API call
# Assume 'rag_system' is an initialized RAG object that can search your knowledge base
# Assume 'api_client' can interact with your company's internal APIs

def get_informed_ai_response(user_input, conversation_history, rag_system, api_client):
    # 1. Retrieve relevant documents from knowledge base
    relevant_docs = rag_system.search(user_input)
    
    # 2. Check if user data is needed (e.g., order status)
    data_request = None
    if "order status" in user_input.lower():
        # Extract order ID if possible, or ask user for it
        order_id = extract_order_id(user_input) # Placeholder function
        if order_id:
            try:
                order_info = api_client.get_order_status(order_id)
                data_request = f"Order Status: {order_info}"
            except Exception as e:
                data_request = "Could not retrieve order status at this time."
        else:
            data_request = "Please provide your order ID."
            
    # 3. Construct prompt with retrieved docs and any API data
    context_snippets = "\n".join([doc['content'] for doc in relevant_docs])
    prompt_messages = [
        {"role": "system", "content": "You are a customer support assistant. Use the provided context and information to answer the user's query accurately."}
    ]
    
    # Add conversation history...
    prompt_messages.extend(conversation_history[1:]) # Exclude system message from history
    
    # Add current user input, augmented with retrieved docs and API data
    augmented_user_input = f"{user_input}\n\nContext:\n{context_snippets}\n{data_request if data_request else ''}"
    prompt_messages.append({"role": "user", "content": augmented_user_input})
    
    # 4. Call LLM API
    try:
        response = openai.ChatCompletion.create(
            model="gpt-3.5-turbo",
            messages=prompt_messages
        )
        ai_message = response.choices[0].message['content'].strip()
        return ai_message
    except Exception as e:
        print(f"Error communicating with OpenAI API: {e}")
        return "I'm sorry, I encountered an error. Please try again later."

# Placeholder functions
def extract_order_id(text):
    # Implement logic to extract order ID from text
    return None

class MockAPIService:
    def get_order_status(self, order_id):
        # Simulate API call
        return "Shipped"

# Example usage within run_chatbot:
# rag = RAGSystem(knowledge_base='path/to/your/kb')
# api = MockAPIService() # Replace with actual API client
# bot_response = get_informed_ai_response(user_input, conversation_history, rag, api)
```

### Real-world Examples and Scenarios:
An e-commerce chatbot needs to answer questions about product availability, shipping times, and return policies. Using RAG, it can access product descriptions and FAQs. If a user asks, "When will my order arrive?", the chatbot, integrated with the company's order management system API, can retrieve the specific order's status and provide an accurate delivery estimate.

A software company's chatbot can access technical documentation via RAG to answer questions about API usage. If a user encounters an error code, the chatbot can search its knowledge base for that specific error code and provide troubleshooting steps. If the issue persists, it can then use API integration to check the user's service plan or system logs for more context before escalating.

Integrating real-world data transforms a generic chatbot into a powerful, specialized tool that significantly enhances customer support efficiency and satisfaction.

## Section 7: Hands-On Component: Building and Testing Your Chatbot Prototype
Now it's time to consolidate your learning by building and testing a functional prototype of the customer support chatbot. This section guides you through the practical steps of implementing the core components discussed in the previous sections using Python.

**Objective:** To create a working command-line chatbot that can handle basic customer support queries, manage conversation history, and provide a foundation for further development.

**Steps:**
1.  **Set Up Your Environment:**
    *   Ensure you have Python installed.
    *   Install the OpenAI Python library: `pip install openai`
    *   Obtain your OpenAI API key and set it as an environment variable (e.g., `export OPENAI_API_KEY='your-api-key'`).
2.  **Develop the Core Chatbot Script:**
    *   Combine the code snippets from Section 3 (Integrating with a Simple User Interface) into a single Python file. Let's call it `customer_support_bot.py`.

```python
import openai
import os

# --- Configuration ---
openai.api_key = os.getenv('OPENAI_API_KEY')
if not openai.api_key:
    raise ValueError("OpenAI API key not found. Please set the OPENAI_API_KEY environment variable.")

# --- Conversation Management ---
# Initialize with a system message defining the bot's persona and task
conversation_history = [
    {"role": "system", "content": "You are a helpful and friendly customer support assistant for a fictional tech company. Your goal is to answer user questions about products, services, and common troubleshooting steps. If you cannot answer a question or the user expresses significant frustration, offer to connect them to a human agent. Respond concisely."}
]

def add_message(role, content):
    conversation_history.append({'role': role, 'content': content})

def get_recent_history(max_turns=8):
    # Returns the last 'max_turns' user/assistant message pairs, plus the system message.
    # This is a simplified approach. A real-world app would use token counting.
    history_to_send = [conversation_history[0]] # Always include system message
    
    # Collect user and assistant messages in pairs
    message_pairs = []
    for msg in conversation_history[1:]:
        message_pairs.append(msg)
        if len(message_pairs) == 2: # A pair consists of user + assistant message
            if len(history_to_send) + len(message_pairs) <= max_turns * 2 + 1: # +1 for system message
                history_to_send.extend(message_pairs)
            message_pairs = []
    
    # Add any remaining messages if the last turn wasn't a full pair
    if message_pairs:
        if len(history_to_send) + len(message_pairs) <= max_turns * 2 + 1:
            history_to_send.extend(message_pairs)
            
    return history_to_send

# --- AI Interaction Function ---
def get_ai_response(user_input):
    add_message('user', user_input)
    
    context = get_recent_history(max_turns=8) # Adjust max_turns as needed
    
    try:
        response = openai.ChatCompletion.create(
            model="gpt-3.5-turbo", # Use a suitable model like gpt-3.5-turbo or gpt-4
            messages=context
        )
        ai_message = response.choices[0].message['content'].strip()
        add_message('assistant', ai_message)
        return ai_message
    except openai.error.RateLimitError:
        error_msg = "API rate limit exceeded. Please wait a moment and try again."
        add_message('assistant', error_msg)
        return error_msg
    except openai.error.AuthenticationError:
        error_msg = "Authentication failed. Please check your API key."
        add_message('assistant', error_msg)
        return error_msg
    except Exception as e:
        print(f"An unexpected error occurred: {e}")
        error_msg = "I apologize, but I encountered an internal error. Please try again later."
        add_message('assistant', error_msg)
        return error_msg

# --- Escalation Logic (Simplified) ---
def check_for_escalation(user_input):
    keywords = ['human', 'agent', 'representative', 'talk to someone', 'speak to an agent']
    return any(keyword in user_input.lower() for keyword in keywords)

def initiate_escalation():
    escalation_response = "I understand you need further assistance. Please wait a moment while I connect you to a human agent. For now, I will end this chat."
    add_message('assistant', escalation_response)
    return escalation_response

# --- Main Chat Loop ---
def run_chatbot():
    print("\n=====================================")
    print(" TechCo Support Bot Activated ")
    print("=====================================")
    print("Bot: Hello! I'm your virtual assistant for TechCo. How can I help you today? (Type 'quit' to exit)")
    
    while True:
        user_input = input("You: ")
        if user_input.lower() == 'quit':
            print("Bot: Goodbye! Thank you for contacting TechCo Support.")
            break
        
        if check_for_escalation(user_input):
            bot_response = initiate_escalation()
            print(f"Bot: {bot_response}")
            break # End chat after escalation offer
        
        bot_response = get_ai_response(user_input)
        print(f"Bot: {bot_response}")

# --- Run the chatbot ---
if __name__ == "__main__":
    run_chatbot()
```

3.  **Run the Chatbot:**
    *   Open your terminal or command prompt, navigate to the directory where you saved `customer_support_bot.py`, and run the script: `python customer_support_bot.py`
    *   You should see the welcome message from the bot.
4.  **Test with Sample Queries:**
    *   Interact with your chatbot. Try the following types of queries:
    *   **FAQs:** "What are your return policies?", "How do I reset my password?", "What are the specifications of the new X1 laptop?"
    *   **Troubleshooting:** "My internet is not working.", "The software keeps crashing.", "How do I set up my new device?"
    *   **Contextual Queries:** Ask a follow-up question after an initial query. For example, after asking about returns, ask "What is the timeframe for returns?"
    *   **Escalation Request:** "I need to speak to a human agent.", "This is too complicated, I need more help."
    *   **Out-of-Scope Queries:** "What's the weather like today?", "Tell me a joke."
5.  **Observe and Analyze:**
    *   Pay close attention to the bot's responses:
    *   Are the answers accurate and relevant to TechCo (as defined in the system prompt)?
    *   Does the bot maintain context across multiple turns?
    *   Does it handle escalation requests appropriately?
    *   How does it respond to questions outside its scope?
6.  **Iterate and Refine (Optional but Recommended):**
    *   Based on your observations, you can refine the chatbot:
    *   **Modify the System Prompt:** Edit the `conversation_history[0]['content']` in the script to provide clearer instructions, a different persona, or more specific guidance on handling certain query types. For example, you could add: "When asked about product features, focus on benefits and technical specifications."
    *   **Adjust `max_turns`:** Experiment with the `max_turns` parameter in the `get_recent_history` function to control how much conversation history is sent to the API. A higher number preserves more context but increases API costs and latency.
    *   **Add More Specific Prompts:** For very common issues, you could implement logic to detect specific keywords and construct more tailored prompts before sending them to the AI.

This hands-on exercise provides a tangible outcome and reinforces the practical application of prompt engineering principles in building a functional AI prototype.

## Summary and Next Steps: Mastering AI Chatbot Development
In this comprehensive lesson, we've journeyed from understanding the fundamentals of prompt design for customer support to building and testing a functional AI chatbot prototype. You've learned how to craft prompts for FAQs and issue resolution, manage conversation history for coherent dialogues, integrate with a simple user interface, handle escalations to human agents, and consider the critical role of real-world data. The hands-on component allowed you to bring these concepts to life by creating and interacting with your own Python-based chatbot.

**Key Takeaways:**
*   **Prompt Engineering is Foundational:** The quality of your prompts directly dictates the performance and usefulness of your AI chatbot.
*   **Context is King:** Effective conversation history management is essential for natural and efficient user interactions.
*   **Human Escalation is Crucial:** A well-defined escalation path ensures customer needs are met, even beyond AI capabilities.
*   **Iteration is Key:** Continuous testing and refinement of prompts are vital for optimizing chatbot performance.
*   **Real-World Data Powers Specialization:** Integrating domain-specific data (via RAG or APIs) transforms generic AI into a powerful business tool.
*   **Practical Application Builds Confidence:** Building prototypes solidifies understanding and demonstrates the tangible impact of prompt engineering.

**Best Practices and Pro Tips:**
*   **Start Simple, Then Scale:** Begin with a clear scope and gradually add complexity.
*   **Document Your Prompts:** Keep a record of your prompts, their purpose, and their performance.
*   **Monitor and Analyze:** Regularly review chatbot interactions to identify areas for improvement.
*   **User Feedback is Gold:** Actively solicit and incorporate user feedback into your iteration cycle.
*   **Security First:** Be mindful of data privacy and security, especially when handling sensitive customer information or integrating with internal systems.
*   **Choose the Right Model:** Select AI models appropriate for your task and budget.

**Preparation for the Next Lesson: Project: Content Generation Pipeline**
Our next module dives into automating content creation. To prepare, reflect on how the principles of prompt engineering, context management, and iterative refinement you've applied today can be adapted for generating written content. Consider:
*   What kind of inputs would a content generation AI need?
*   How would you structure prompts to guide the AI in creating different types of content (e.g., blog posts, articles, marketing copy)?
*   What are the challenges in ensuring factual accuracy and maintaining a consistent brand voice in AI-generated content?
*   How might you chain prompts together to create a more complex content generation workflow?

Think about how you might design a prompt that asks the AI to generate an outline for a blog post on a given topic, and then another prompt to flesh out each section of that outline. This forward-thinking will help you hit the ground running in our next project.

**Practice Exercises:**
*   **Enhance Your Chatbot:** Try adding more specific prompts to your `customer_support_bot.py` script. For example, create a simple function to detect if a user is asking about "shipping" and then prepend a specific instruction to the prompt sent to the AI, like: "The user is asking about shipping. Provide information on standard shipping times and costs."
*   **Explore RAG Concepts:** Research libraries like LangChain or LlamaIndex and explore their documentation on setting up a basic RAG pipeline. While you don't need to implement it fully now, understanding the concepts will be beneficial.
*   **Analyze Real Chat Logs:** If you have access to anonymized customer support chat logs, review them to identify common patterns, user intents, and areas where a chatbot could be most effective.

By mastering these foundational skills in building and refining AI chatbots, you are well-equipped to tackle more complex AI projects, including the content generation pipeline we will explore next.
