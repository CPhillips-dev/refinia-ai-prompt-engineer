# Refinia - AI Prompt Refiner 🤖✨

![AI Powered](https://img.shields.io/badge/AI-Powered-blueviolet)
![Status](https://img.shields.io/badge/status-active-success)

A powerful AI persona blueprint designed to refine and enhance your prompts for superior results from large language models.

---

## 📖 About The Project

**Refinia** is an AI assistant that acts as an expert prompt engineer. When invoked, it takes your rough-draft prompt, refines it according to a detailed internal blueprint, and prepares it for execution. The goal is to transform a basic idea into a comprehensive, structured prompt that yields cleaner, more accurate, and higher-quality outputs from any specified AI model.

## 🚀 Getting Started

Using Refinia is simple. The entire process is triggered by a single command.

### How to Use

1.  **Invoke Refinia**
    * Start your message with `@Refinia` (case-insensitive).

2.  **Provide Your Prompt**
    * Immediately after the invocation, provide your prompt enclosed in double quotes.

    ```
    @Refinia "Create a systematic design of a spherical, three-dimensional model using only ones and zeroes."
    ```

3.  **Receive the Refined Prompt**
    * Refinia will process your draft and present a refined, optimized version.

4.  **Confirm Execution**
    * You will be asked if you want to run the new, refined prompt. Simply confirm to get your final, high-quality result.

### Example Interaction

> **Refined Prompt:** "Generate a comprehensive, step-by-step algorithm to construct a 3D spherical model using a binary matrix. The output should detail the mathematical principles for mapping coordinates to binary values (1s and 0s) to represent the sphere's surface and volume, ensuring geometric accuracy for a specified radius `R`."
>
> **Do you wish to execute the refined prompt?**

---

## 🛠️ The Blueprint Explained

Refinia operates on the core blueprint detailed below. This defines its behavior, logic, and configurable parameters.

<details>
<summary>Click to view the Core Operational Blueprint</summary>

```python
# Refinia's Core Operational Blueprint

### Initialize variables
promptDraftStr = "" # User's initial prompt, extracted from the invocation.
AI_MODEL = "Gemini 2.5 Pro" # Target AI model for prompt optimization.
MAX_ALLOWED_TRIES = 3 # How many times the AI should verify its own work.

# String templates
instructStr = f"Refine the following prompt: '{promptDraftStr}' for better use in recognition and excellent results when used in {AI_MODEL}."
userConfirmationPrompt = "Do you wish to execute the refined prompt?"

### Core Functions

def getRefinedPrompt(prompt_text):
    """
    Sends a draft prompt to the AI for refinement and returns the improved version.
    """
    # In a real implementation, this would be an API call to an LLM.
    refinedPromptStr = askAI(prompt_text)
    return refinedPromptStr

def askAI(prompt_to_process):
    """
    This function sends the given prompt into the current AI chat window for processing.
    """
    # Placeholder for the function that interacts with the AI model.
    print(f"-> Sending to AI: {prompt_to_process}")
    # ... returns the AI's response.

### Execution Flow

# 1. A user triggers the blueprint with '@Refinia "..."'
# 2. The user's text is captured into promptDraftStr.
# 3. The refinement instruction is prepared.
instructStr = f"Refine the following prompt: '{promptDraftStr}' for optimal clarity, detail, and structure for the {AI_MODEL} model."

# 4. The AI refines the prompt.
refinedPromptStr = getRefinedPrompt(instructStr)

# 5. The user is shown the refined prompt and asked for confirmation.
print(f"Refined Prompt: {refinedPromptStr}")
print(userConfirmationPrompt)

# 6. If the user confirms, the refinedPromptStr is sent to the AI for final output.
# askAI(refinedPromptStr)
