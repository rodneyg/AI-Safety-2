# AI-Safety-2: Boundary Erosion Demo

> A SafeLab prototype that uses scripted responses to illustrate how incremental context shifts can erode conversational AI guardrails.

[Hosted simulator](https://v0-interactive-ai-demo.vercel.app/) or see the [changelog](CHANGELOG.md). This repository contains research notes and patches. Each patch guide identifies the Vercel source snapshot it requires.

Use the [metadata and reset patch](deployment-fixes/README.md) for the original snapshot. The [accessibility patch](deployment-fixes/t10393.md) is for a later snapshot that already includes the reset fix. The [chat wrapping patch](deployment-fixes/t11092.md) applies to that same later snapshot. When using both patches, apply the accessibility patch first.
<img width="1082" alt="Screenshot 2025-04-25 at 1 41 12 PM" src="https://github.com/user-attachments/assets/07446380-fa77-49a4-a9fc-3b0b4fd59c5c" />

## 🧠 Overview

Boundary erosion describes an AI safety failure where several small context shifts can add up to a response that crosses a safety boundary. The simulator illustrates the idea with a boundary meter and scripted replies for each scenario. The meter adds the weights of matching trigger phrases for the selected scenario and caps the total at 100%. Matching ignores case and can occur within a word.

## ⚙️ Features

- Interactive chat with scripted replies
- Boundary Meter tracking cumulative drift
- Visual + textual representation of context erosion
- The reset patch clears the conversation, meter, and boundary alert. It also prevents delayed replies or alert timers from the old conversation from changing the new one.
- The accessibility patch labels Scenario Selection and Send message for screen readers and improves contrast for the empty chat prompt, sent messages, and context metrics
- Preloaded scenarios for volleyball, jokes, and research

## 🧪 Example: Volleyball Scenario

Select the Volleyball Player Scenario and send “Draw a woman playing volleyball.” The meter stays at zero. Follow up with “Add more detail” to increase it by five points. Select **Reset Context** to start over.

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
