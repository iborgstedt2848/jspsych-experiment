# Lexical Decision Task (Word vs. Non-Word)

A browser-based **lexical decision experiment** built with [jsPsych](https://www.jspsych.org/) for my Cognitive Science Research Methods class. Participants see a string of letters and decide, as quickly as possible, whether it is a real English word or not. Accuracy and response times are recorded for each trial.

## Research question

Lexical decision tasks are a standard way to study how people access words in memory. Here, participants judge words related to a common theme (travel) alongside scrambled non-words made from the same letters, and we measure how quickly and accurately they respond to each.

## Design

| Component | Details |
|-----------|---------|
| Task | Lexical decision (word / non-word) |
| Stimuli | 20 letter strings: 10 real words and 10 non-words |
| Words | travel, plane, luggage, passport, vacation, country, abroad, departure, arrival, international |
| Non-words | Anagrams of each word (e.g. *vaterl*, *lapne*, *lgagegu*), so each non-word matches its word in length and letter content |
| Repetitions | Each stimulus is shown 5 times (100 trials total) |
| Order | Fully randomized |
| Fixation | "+" shown before each stimulus for a random duration (250-2000 ms, in 250 ms steps) |
| Responses | **T** = word, **F** = non-word |

### Variables

- **Independent variable:** stimulus type (word vs. non-word)
- **Dependent variables:** response time (ms) and accuracy (correct/incorrect)

## Procedure

1. Welcome screen
2. Instructions (press **T** for a word, **F** for a non-word)
3. 100 test trials, each a fixation cross followed by a letter string that stays on screen until a response
4. Debrief screen showing the participant's accuracy (%) and mean response time on correct trials

## Data

Each trial records:

- `task`: `fixation` or `response`
- `stimulus`: the letter string shown
- `response`: the key pressed
- `correct_response`: the key that was correct (`t` or `f`)
- `correct`: whether the response was correct
- `rt`: response time in milliseconds

When the experiment ends, the full dataset is displayed on the page (`jsPsych.data.displayData()`). The experiment does not currently save data to a server, so copy or export the displayed data if you want to keep it for analysis.

## Running the experiment

1. Download or clone this repository.
2. Open the `.html` file in a modern web browser (Chrome, Firefox, Safari, or Edge).
3. Follow the on-screen instructions.

An internet connection is needed because jsPsych is loaded from a CDN (unpkg).

## Built with

- [jsPsych 7.3.4](https://www.jspsych.org/)
- `@jspsych/plugin-html-keyboard-response` 1.1.3
- Plain HTML and JavaScript (no build step)

## Possible extensions

- Add real words unrelated to travel to compare themed and unthemed words
- Match words and non-words on word frequency and length
- Add practice trials
- Save data to a server or download it as a CSV
- Add a demographic questionnaire and consent form

## Author
Isabelle Borgstedt and COGS-219 Research Methods
Spring 2024

