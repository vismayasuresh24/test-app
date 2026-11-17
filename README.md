# quiz-cli

An interactive command-line quiz game for learning JavaScript and general programming concepts. The project is located in the `test-app/` directory of this repository.

## Features

- Choose from three quiz categories: JavaScript Basics, Node.js Fundamentals, and General Programming.
- Select how many questions to answer.
- Answer multiple-choice questions in the terminal.
- See explanations, quiz progress, and a final score with performance feedback.
- Review incorrect answers.
- Choose whether to play again.

Questions and answer explanations are stored in `data/questions.json`.

## Technology Stack

- **Node.js** with ECMAScript modules
- **Node.js built-in modules:** `node:fs/promises`, `node:url`, `node:path`, and `readline`
- **npm scripts** for starting the application and running tests
- **External dependencies:** None are listed in `package.json`

## Project Structure

```text
.
├── README.md
└── test-app/
    ├── data/
    │   └── questions.json  # Quiz categories, questions, answers, and explanations
    ├── index.js            # CLI entry point and quiz/replay flow
    ├── package.json        # Project metadata, Node requirement, and npm scripts
    └── src/
        ├── colors.js       # ANSI terminal styling helpers
        ├── input.js        # Interactive prompts and input helpers
        └── quiz.js         # Question selection, scoring, feedback, and review
```

## Prerequisites

- Node.js **18.0.0 or later**
- npm, included with Node.js

## Installation and Setup

The application files are in `test-app/`, so run project commands from that directory:

```bash
cd test-app
```

There are no external npm dependencies listed in the project manifest. No separate dependency installation is required to run the application.

## How to Run

From the `test-app/` directory:

```bash
npm start
```

This runs `node index.js` and starts the interactive quiz in the terminal.

## Usage

1. Start the application with `npm start`.
2. Follow the terminal prompts to select a quiz category and question count.
3. Answer the multiple-choice questions.
4. Review your score and any incorrect answers.
5. Use the replay prompt if you want to start another quiz.

The available categories and questions are defined in `data/questions.json`.

## Environment Configuration

No environment variables or configuration files are identified in the retrieved repository information.

## API

This is a command-line application. No API endpoints or server configuration are identified.

## Tests

The package defines this test script:

```bash
npm test
```

It invokes Node.js’s built-in test runner with `node --test`. No test files were listed in the retrieved repository information, so the presence of dedicated tests is not confirmed.

## Troubleshooting

- **Commands do not find the project files:** Change into the nested project directory first: `cd test-app`.
- **The application cannot start:** Confirm that Node.js is version 18 or later.
- **The quiz exits with an error:** The entry point catches errors and exits with status code `1`. Review the terminal output for the error details.
- **Interactive prompts do not work as expected:** Run the application in an interactive terminal, since it uses terminal input prompts.

## Contributing

No contribution guidelines were found in the retrieved repository information. If you submit a change, keep it consistent with the existing Node.js project structure and update the relevant source or question data. Run the available check with `npm test` from `test-app/` and describe what you changed.

## License

`package.json` identifies the project license as **MIT**. A separate license file was not present in the retrieved repository information.
