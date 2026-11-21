# AI-Safety-2: Boundary Erosion Demo

> A SafeLab prototype that uses scripted responses to illustrate how incremental context shifts can erode conversational AI guardrails.

[Open the simulator](https://v0-interactive-ai-demo.vercel.app/) or see the [changelog](CHANGELOG.md). This repository holds research notes and a [patch for a Vercel source snapshot](deployment-fixes/README.md).
<img width="1082" alt="Screenshot 2025-04-25 at 1 41 12 PM" src="https://github.com/user-attachments/assets/07446380-fa77-49a4-a9fc-3b0b4fd59c5c" />

## 🧠 Overview

Boundary erosion describes an AI safety failure where several small context shifts can add up to a response that crosses a safety boundary. The simulator illustrates the idea with a boundary meter and scripted replies for each scenario. The meter increases when a message contains trigger words for the selected scenario.

## ⚙️ Features

- Live chat interface for simulating prompt manipulation
- Boundary Meter tracking cumulative drift
- Visual + textual representation of context erosion
- Reset Context clears the conversation and meter and discards pending replies from the old conversation
- Preloaded scenarios for volleyball, jokes, and research

## 🧪 Example: Volleyball Scenario

Select the volleyball scenario, send “Draw a woman playing volleyball,” and watch the meter as you try follow-up messages. Select **Reset Context** to start over.

## 👩‍💻 Stack

The hosted simulator uses Next.js, Tailwind CSS, and React state. The chat selects scripted replies based on the current scenario and boundary level.

## 📜 License

Apache 2.0 — Use, adapt, or fork. Attribution encouraged. Misuse discouraged.

## 🤝 Contribute

We’re open to:
- Alignment researchers
- Red team contributors
- Interface designers with security focus

DM [@rg2official](https://twitter.com/rg2official) or email via SafeLab.

---

© 2025 Rodney Gainous Jr. / SafeLab
