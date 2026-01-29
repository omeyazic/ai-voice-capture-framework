# ai-voice-capture-framework
A structured framework for capturing an individual's unique writing voice, thought patterns, and stylistic preferences into a portable text file. This enables consistent AI persona imitation across different models.  Based on the methodology described by Ruben Hassid in "I am just a text file" (https://ruben.substack.com/p/i-am-just-a-text-file).


# Voice Capture Framework

A structured framework for capturing an individual's unique writing voice, thought patterns, and stylistic preferences into a portable text file. This enables consistent AI persona imitation across different models.

Based on the methodology and core prompt described by **Ruben Hassid** in the article ["I am just a text file"](https://ruben.substack.com/p/i-am-just-a-text-file).

## Core Philosophy

This project is built on a simple but powerful premise: your unique "voice"—the patterns, preferences, and boundaries that define how you think and write—can be systematically captured. The goal is not to create a rigid checklist, but to provide an AI with the **context of your taste**, moving it from generating generic outputs to producing content that genuinely resonates with your style.

As Ruben describes, *"Taste isn't what you like, but what you reject."* This framework is designed to help you articulate those rejections with precision.

##  How It Works

The process is an adaptive interview between you and a capable Large Language Model (LLM).

1.  **The Interview**: You provide an LLM (like Claude) with the structured prompt. It acts as a "Taste Interviewer," asking you 100 probing questions across seven key categories of your voice and style.
2.  **Dynamic Q&A**: The AI does not use a fixed list. It generates questions in real-time, diving deeper into your interesting answers and pushing for specificity, creating a truly personalized interview.
3.  **Profile Generation**: After the 100th answer, the AI compiles all your responses into a comprehensive, well-structured Markdown (`.md`) document—your **Voice Profile**.
4.  **Portable Usage**: This `.md` file becomes a portable context file. You can upload it to any AI chat session (Claude, ChatGPT, etc.) and instruct the model to "read this first." The AI will then generate text that aligns with the captured voice.

## Repository Structure

```
voice-capture-framework/
│
├── prompts/
│   └── taste_interview_prompt.md  # The core 100-question interview prompt
│
├── examples/
│   ├── sample_voice_profile.md    # An example output (anonymous)
│   └── ruben_hassid_profile.md    # A distilled profile based on the article's author
│
├── notes/
│   ├── methodology_notes.md       # Insights on the process & philosophy
│   └── implementation_tips.md     # Practical advice for running your interview
│
├── tools/
│   └── profile_validator.py       # (Optional) A simple script to check profile structure
│
└── README.md                      # This file
```

## Quick Start Guide

### Prerequisites
*   Access to an LLM with a large context window and good instruction-following capabilities (e.g., **Claude 3.5 Sonnet/Opus** via [claude.ai](https://claude.ai) is highly recommended, as used in the original article).
*   **1.5 - 2 hours** of focused time for the interview.

### Steps
1.  **Copy the Prompt**: Navigate to `/prompts/taste_interview_prompt.md` and copy the entire text.
2.  **Start a New Chat**: In your chosen AI platform, start a new chat. For best results, use a "document" or "project" feature if available.
3.  **Paste and Begin**: Paste the full prompt and send it. The AI will introduce itself as the Taste Interviewer and ask the first question.
4.  **Answer Thoroughly**: Engage with the process. Be specific, use examples, and let the AI guide you. Remember: specificity is key.
5.  **Compile Your Profile**: After the 100th answer, the AI will generate your Voice Profile in Markdown format. Save this as `[your_name]_voice_profile.md`.
6.  **Use Your Voice**: To use it, upload this file at the start of a new AI chat and give an instruction like: "Please read my voice profile first, then help me draft a blog post about..."

## Best Practices & Tips

*   **Embrace Specificity**: Vague answers lead to a generic profile. If you say "I like clear writing," be prepared for the AI to ask, "*Clear how? Give me an example of clear vs. unclear from your work.*"
*   **Think in Boundaries**: Focus as much on what you **never** do (e.g., "I never start emails with 'I hope this email finds you well'") as on what you prefer.
*   **It's a Living Document**: Your voice evolves. Re-run the interview periodically or manually edit your `.md` file to add new preferences or insights.
*   **Spirit Over Letter**: When using the profile, instruct the AI to capture the *spirit* of your voice, not to follow every rule slavishly. Natural variation is human.
*   **Start Small**: For your first test, try creating a profile just for a specific context (e.g., "Professional Email Voice" or "Technical Blogging Voice").

## Important Considerations

*   **Time Investment**: This is a deep, reflective exercise. Allocate sufficient time and mental energy.
*   **The "Uncanny Valley"**: Output may sometimes feel like a slightly "off" imitation. Use your profile as a first draft generator, not a final-word producer.
*   **Authenticity**: Relying solely on an AI clone risks diluting your genuine creative voice. Use this as a tool for augmentation, not replacement.
*   **Ethical Use**: This framework is intended for capturing **your own** voice. Using it to imitate others without their explicit consent is strongly discouraged.

## Example Output

Check the `examples/` directory to see what a generated Voice Profile looks like. `sample_voice_profile.md` shows a generic example, while `ruben_hassid_profile.md` distills key voice elements from the original article's author.

## Future Ideas & Contributing

This is a starting point. Potential future expansions include:
*   Adapters for different LLMs (GPT, Gemini, etc.).
*   A web interface to guide users through the interview.
*   Tools to analyze and compare voice profiles.
*   Extensions for specific domains (corporate tone, fictional character voice, etc.).

Contributions, ideas, and discussions are welcome! Please open an Issue or Pull Request.

## Credits & Attribution

The core concept, methodology, and original prompt structure are the work of **Ruben Hassid**. This repository is a curated implementation and extension of the ideas presented in his seminal article:
*   **Article**: ["I am just a text file"](https://ruben.substack.com/p/i-am-just-a-text-file)
*   **Author**: Ruben Hassid

This project is intended for educational and practical experimentation. It is not officially affiliated with Ruben Hassid or Substack.

---

*“I am just a text file. And now anyone can think & write like me.”* – Ruben Hassid
