# 🤖 Multi-Agent AI Article Generator with CrewAI

A production-ready multi-agent AI system built with **CrewAI** that demonstrates how multiple specialized AI agents collaborate to research, write, and edit high-quality articles.

This project showcases modern CrewAI best practices using the latest stable APIs and a Hugging Face-hosted Llama 3.1 model.

---

## 🚀 Features

- 📝 AI Content Planner
  - Researches a topic
  - Creates a structured content outline

- ✍️ AI Content Writer
  - Converts the outline into a complete article
  - Produces coherent, well-organized content

- 🔍 AI Editor
  - Improves grammar
  - Enhances readability
  - Removes repetition
  - Refines structure and clarity

- ⚙️ Sequential multi-agent workflow using CrewAI

- 🤖 Powered by:
  - CrewAI
  - Hugging Face Inference Router
  - Meta Llama 3.1 8B Instruct

---

# Project Architecture

```
               User Topic
                    │
                    ▼
         ┌────────────────────┐
         │ Content Planner    │
         └────────────────────┘
                    │
                    ▼
         ┌────────────────────┐
         │ Content Writer     │
         └────────────────────┘
                    │
                    ▼
         ┌────────────────────┐
         │ Editor             │
         └────────────────────┘
                    │
                    ▼
            Final Article
```

---

# Tech Stack

- Python
- CrewAI 1.15.2
- CrewAI Tools 1.15.2
- Hugging Face Router
- Meta Llama 3.1 8B Instruct
- Jupyter Notebook

---

# Installation

Clone the repository.

```bash
git clone https://github.com/yourusername/multi-agent-article-generator.git

cd multi-agent-article-generator
```

Install the required packages.

```bash
pip install -U crewai==1.15.2 crewai-tools==1.15.2
pip install -U "crewai[litellm]"
```

---

# API Key Setup

This project uses the Hugging Face Router.

Create a Hugging Face access token from:

https://huggingface.co/settings/tokens

Then either:

```python
import os

os.environ["HUGGINGFACE_API_KEY"] = "your_api_key"
```

or enter it when prompted in the notebook.

---

# Running the Project

Open the notebook.

```
Multi_Agent.ipynb
```

Run each cell in order.

The workflow is:

1. Configure the LLM
2. Create the agents
3. Create the tasks
4. Build the Crew
5. Execute the workflow

Example:

```python
result = await crew.kickoff_async(
    inputs={
        "topic": "Artificial Intelligence"
    }
)
```

---

# Example Topics

Try generating articles about:

- Artificial Intelligence
- Climate Change
- Cybersecurity
- Machine Learning
- Blockchain
- Renewable Energy
- Robotics
- Data Science
- Quantum Computing

---

# Multi-Agent Workflow

### 1. Content Planner

Responsible for:

- Researching the topic
- Identifying key concepts
- Creating an organized outline

---

### 2. Content Writer

Responsible for:

- Writing the full article
- Following the planner's outline
- Producing informative content

---

### 3. Editor

Responsible for:

- Grammar correction
- Improving readability
- Ensuring logical flow
- Removing redundant content
- Producing the final polished article

---

# Project Structure

```
.
├── Multi_Agent.ipynb
├── README.md
└── requirements.txt (optional)
```

---

# Example Output

Input:

```
Topic:
The Future of Generative AI
```

Output:

- Research Plan
- Complete Article
- Professionally Edited Final Version

---

# Learning Objectives

This project demonstrates:

- Multi-Agent AI Systems
- CrewAI Architecture
- Agent Collaboration
- Sequential Task Execution
- LLM Integration
- Prompt Engineering
- AI Content Generation

---

# Future Improvements

- Web search integration
- PDF export
- Blog publishing
- Memory-enabled agents
- Fact-checking agent
- Citation generation
- Streamlit interface
- RAG integration
- Human approval workflow

---

# Requirements

- Python 3.10+
- CrewAI 1.15.2
- CrewAI Tools 1.15.2
- Hugging Face API Key

---

# License

This project is intended for educational purposes and demonstrates modern multi-agent AI workflows using CrewAI.

---

# Acknowledgements

- CrewAI
- Hugging Face
- Meta AI (Llama 3.1)
