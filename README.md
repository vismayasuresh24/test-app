# Quiz CLI

An interactive command-line quiz game for learning JavaScript, Node.js, and general programming concepts. Choose a topic, answer multiple-choice questions, review explanations, and see your score—all from your terminal.

## Features

- Three quiz categories: JavaScript Basics, Node.js Fundamentals, and General Programming.
- Choose to answer all available questions or a shorter 3- or 5-question round (when the category has enough questions).
- Shuffled question order, numbered answer choices, and a visual progress bar.
- Immediate answer feedback with explanations and a review of incorrect answers at the end.
- Score summary with performance messages, plus an option to play again.
- Colorized terminal output using built-in ANSI escape codes; no third-party runtime dependencies.

## Requirements

- [Node.js](https://nodejs.org/) 18.0.0 or later.
- A terminal that supports interactive input. ANSI color and Unicode rendering depend on terminal support.

## Getting started

The Node.js project files are in the `test-app/` directory. From the repository root, enter that directory and start the quiz:

```sh
cd test-app
npm start
```

Follow the prompts to choose a category and question count. Enter the number corresponding to an answer, and press Enter when prompted to continue. At the end of a round, choose whether to play again.

Alternatively, run the entry point directly from `test-app/`:

```sh
node index.js
```

## Running tests

The project defines a test script using Node's built-in test runner:

```sh
cd test-app
npm test
```

This runs `node --test`. The repository currently does not include a dedicated test-file suite, so the command may report that no tests were found.

## Project structure

```text
.
├── README.md
└── test-app/
    ├── index.js              # Application entry point and quiz flow
    ├── package.json          # Project metadata and npm scripts
    ├── data/
    │   └── questions.json    # Categories, questions, options, answers, explanations
    └── src/
        ├── colors.js         # ANSI terminal styling helpers
        ├── input.js          # Readline prompts and selection helpers
        └── quiz.js           # Quiz state, scoring, feedback, and results
```

## How it works

1. `index.js` loads category and question data from `data/questions.json` and presents the interactive menu.
2. The selected questions are passed to the `Quiz` class in `src/quiz.js`, which shuffles them and manages progress, answers, and score.
3. The helpers in `src/input.js` collect and validate numbered choices using Node.js's built-in `readline` module.
4. `src/colors.js` applies terminal styles without external dependencies. After the final question, the game displays results and any incorrect answers for review.

Question answers are stored as zero-based indexes into each question's `options` array. To add or edit quiz content, update the corresponding category and question entries in `test-app/data/questions.json`, keeping each question's `options`, `answer`, and optional `explanation` consistent.

## Learning topics

This project is also a small example of modern JavaScript and Node.js techniques, including ES modules, async/await and Promises, file-system operations, readline-based input, classes, array methods, destructuring, template literals, and error handling.

## Dependencies

There are no external packages listed in `package.json`. The application uses Node.js built-in modules, including `node:fs/promises`, `node:path`, `node:url`, and `node:readline`.

## License

The `test-app/package.json` declares the project license as MIT. See the repository for license terms.
