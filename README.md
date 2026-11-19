# Quiz CLI

An interactive command-line quiz game for practicing JavaScript, Node.js, and general programming knowledge. Choose a category, answer multiple-choice questions, and review your score and missed answers. The app is built with Node.js and uses only built-in modules.

## Features

- Three quiz categories: JavaScript Basics, Node.js Fundamentals, and General Programming.
- Choose to answer all questions in a category or a shorter set of three or five questions when available.
- Questions are shuffled for each quiz.
- Immediate feedback, explanations, a progress bar, and a final score.
- Review incorrect answers at the end of a quiz.
- Colorized terminal output using ANSI escape codes, with no third-party dependencies.
- Option to play another round without restarting the program.

## Requirements

- Node.js 18 or later
- npm (included with Node.js)

## Getting started

Clone the repository and enter the application directory:

```sh
git clone https://github.com/vismayasuresh24/test-app.git
cd test-app/test-app
```

There are no external packages to install. Start the quiz with:

```sh
npm start
```

Follow the interactive prompts to select a category and question count. Enter the number shown beside an option to answer. Press Enter when prompted to continue. At the end, choose whether to play again.

You can also launch the entry point directly:

```sh
node index.js
```

## Testing

Run the project's Node.js test command from the `test-app` directory:

```sh
npm test
```

The command runs Node's built-in test runner (`node --test`). No test files are currently listed in the repository.

## Project structure

```text
.
├── README.md
└── test-app/
    ├── index.js              # CLI startup, question loading, and game loop
    ├── package.json          # Scripts, metadata, and Node.js requirement
    ├── data/
    │   └── questions.json    # Quiz categories, questions, answers, and explanations
    └── src/
        ├── colors.js         # ANSI terminal color helpers
        ├── input.js          # Readline prompts and selection helpers
        └── quiz.js           # Quiz state, question handling, and results
```

## How it works

`index.js` loads the question data from `data/questions.json`, presents category and question-count choices, and runs the interactive session. The `Quiz` class in `src/quiz.js` shuffles the selected questions, records answers, tracks progress and score, and displays results. User input is handled asynchronously with Node's built-in `readline` module in `src/input.js`; terminal styling is provided by `src/colors.js`.

Quiz content is maintained in `test-app/data/questions.json`. Each category has a display name and a list of questions. Questions provide answer options, a zero-based index identifying the correct answer, and an optional explanation. When adding questions, ensure the `answer` index points to the correct entry in `options`.

## Technologies

- JavaScript with ES modules
- Node.js built-in modules: `node:fs/promises`, `node:path`, `node:url`, and `node:readline`
- Node.js built-in test runner
- ANSI escape codes for terminal colors

## License

The package metadata declares the project license as MIT. Refer to the repository's license file (if present) for the authoritative license terms.
