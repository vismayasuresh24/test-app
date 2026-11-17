# Quiz CLI

An interactive command-line quiz game for learning JavaScript, Node.js, and general programming concepts. The application runs in Node.js and uses built-in modules only.

## Features

- Three quiz categories: JavaScript Basics, Node.js Fundamentals, and General Programming
- Choose a category and answer all available questions
- Questions are shuffled for each quiz
- Immediate answer feedback, explanations, progress display, and final score summary
- Review incorrect answers after completing a quiz
- Option to start another quiz without restarting the application
- Colorized terminal output using ANSI escape codes

## Requirements

- Node.js 18.0.0 or later
- A terminal that supports interactive input

No third-party npm dependencies are required.

## Getting started

Clone the repository and enter the project directory:

```sh
git clone https://github.com/vismayasuresh24/test-app.git
cd test-app/test-app
```

Start the quiz:

```sh
npm start
```

You can also run it directly with Node.js:

```sh
node index.js
```

Follow the prompts to select a category, choose the number of questions when available, and enter the number corresponding to your answer. Press Enter between questions and choose whether to play again at the end.

## Project structure

```text
test-app/
├── data/
│   └── questions.json   # Categories, questions, answers, and explanations
├── src/
│   ├── colors.js        # ANSI terminal color helpers
│   ├── input.js         # Interactive input and selection helpers
│   └── quiz.js          # Quiz state, question flow, and results
├── index.js             # Application entry point
└── package.json         # Project metadata and npm scripts
```

## Questions and categories

Quiz content is stored in `data/questions.json`, grouped under `categories`. Each category has a display name and a list of questions. A question includes its prompt, an `options` array, the zero-based index of the correct option in `answer`, and an optional `explanation`.

To add content, edit the JSON while preserving this structure. The game offers all questions and, when the category has enough questions, options to play a shorter quiz.

## Development

The project uses JavaScript ES modules and Node.js built-in APIs. Run the test script with:

```sh
npm test
```

## License

This project declares the MIT license in `package.json`.
