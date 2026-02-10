# QuizDrop

A lightweight quiz app for parents who want to quiz their kids at home. Upload any question set as JSON, pick topics, and go. No accounts, no internet, no install — just open and drop.

Created by **Manu Balasree**

## Quick Start

1. Open **`quiz.html`** in any browser (double-click the file)
2. Drop a JSON question file onto the upload area
3. Pick topics, set question count and timer
4. Hit **Start Quiz**

## Sample Question Sets

The `samples/` folder includes ready-to-use question sets you can upload right away:

| File | Questions | Topics | Best For |
|---|---|---|---|
| `general-knowledge.json` | 100 | 10 (science, history, geography, etc.) | General study & curiosity building |

Just upload any of these to get started. You can also create your own — see the format below.

## Features

- **Upload any question set** — drop a JSON file and start quizzing
- **Topic filtering** — select specific topics to focus each session
- **Configurable length** — quiz on 5, 10, 20, or all questions
- **Optional timer** — 30s, 60s, 90s, or 2 min per question (or untimed)
- **Shuffle mode** — randomize question order each time
- **Instant feedback** — correct/wrong shown immediately with an explanation
- **Score breakdown by topic** — see which areas need more review
- **Retry wrong answers** — one-click to drill only the ones missed
- **Drag & drop** — drop a JSON file onto the upload area
- **Works offline** — no server or internet needed
- **Flexible options** — supports 2–6 answer choices per question

## Creating Your Own Questions

Create a `.json` file in this format:

```json
{
  "title": "Quiz Title",
  "description": "Short subtitle",
  "author": "Your Name",
  "questions": [
    {
      "id": 1,
      "question": "Question text here",
      "options": ["Choice A", "Choice B", "Choice C", "Choice D"],
      "answer": 0,
      "topic": "Topic Name",
      "explanation": "Brief explanation of the correct answer"
    }
  ]
}
```

**Field reference:**

| Field | Required | Description |
|---|---|---|
| `question` | Yes | The question text |
| `options` | Yes | Array of 2–6 answer choices |
| `answer` | Yes | Index of the correct option (0 = first, 1 = second, etc.) |
| `topic` | No | Topic name for grouping and filtering (defaults to "General") |
| `explanation` | No | Shown after answering — great for reinforcing learning |
| `title` | No | Top-level field — sets the quiz title in the header |
| `description` | No | Top-level field — sets the subtitle in the header |

## Tips for Parents

- **Start small** — 10-question sessions work better than marathon 100-question runs
- **Let them pick topics** — giving kids control over what they study increases engagement
- **Use the timer sparingly** — untimed is fine for learning; add a timer when they want a challenge
- **Retry wrong answers** — the "Retry Wrong Answers" button is the most valuable feature for retention
- **Make your own sets** — the JSON format is simple enough to write by hand or generate with AI

## Project Structure

```
quizdrop/
├── quiz.html                        # The app (open this)
├── README.md
├── LICENSE
└── samples/
    ├── general-knowledge.json       # 100 GK questions for middle schoolers
```

## License

This project is licensed under [CC BY 4.0](https://creativecommons.org/licenses/by/4.0/).
