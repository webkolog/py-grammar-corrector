# PY Grammar Corrector

[![License: MIT](https://img.shields.io/badge/License-MIT-yellow.svg)](https://opensource.org/licenses/MIT)
[![Python: 3.6+](https://img.shields.io/badge/Python-3.6+-blue.svg)](https://www.python.org/downloads/)
[![CI: GitHub Actions](https://img.shields.io/badge/CI-GitHub%20Actions-brightgreen.svg)](https://github.com/webkolog/py-system-information/actions)

**Version:** 1.0

**Created Date:** 2026-07-18

**Last Updated:** 2026-07-27

**Compatibility:** Python 3.6+

**Created By:** Ali Candan ([@webkolog](https://github.com/webkolog))

**Website:** [http://webkolog.net](http://webkolog.net)

**Copyright:** (c) 2026 Ali Candan

**License:** MIT License ([http://mit-license.org](http://mit-license.org))

---

**PY Grammar Corrector** is a lightweight, TextBlob-powered Python command-line utility designed to easily correct spelling and basic grammatical errors in English text sentences. It takes user input in real time and leverages natural language processing to output the most accurate variation of the sentence.

## Installation

### Prerequisites
Make sure you have Python 3.6 or higher installed on your system.

### 1. Clone the Repository
```bash
git clone [https://github.com/webkolog/py-grammar-corrector.git](https://github.com/webkolog/py-grammar-corrector.git)
cd py-grammar-corrector

```

### 2. Install Dependencies

This project relies on the `TextBlob` library. You can install it using `pip`:

```bash
pip install textblob

```

*Note: TextBlob might require downloading its default NLTK corpora during the first run. If prompted, you can download them by running:*

```bash
python -m textblob.download_corpora

```

## Usage

Simply execute the main script `py-grammar-corrector.py` using Python:

```bash
python py-grammar-corrector.py

```

### How It Works

1. The application prompts you to enter a sentence via the command line.
2. It processes the text through a dedicated grammar correction function using TextBlob's `.correct()` method.
3. It prints out the refined, corrected version instantly.

## Code Overview

The script contains a modular configuration that makes it straightforward to integrate into larger text processing projects:

```python
from textblob import TextBlob

def correct_grammar(text):
    """
    Analyzes the input text and returns a grammatically/spelling-corrected string.
    """
    blob = TextBlob(text)
    corrected_text = str(blob.correct())
    return corrected_text

if __name__ == "__main__":
    text = input("Enter your Sentence: ")
    corrected_text = correct_grammar(text)
    print(f"Corrected: {corrected_text}")

```

## Example Usages

### Example 1: Basic Typos

* **Input:** `Enter your Sentence:` I havv a gud ideea.
* **Output:** `Corrected:` I have a good idea.

### Example 2: Common Grammar & Spelling Shifts

* **Input:** `Enter your Sentence:` The keybord is broken.
* **Output:** `Corrected:` The keyboard is broken.

## Dependencies

* **Python 3.6+**
* **TextBlob Library** (Handles tokenization, spelling correction, and NLP parsing)

## License

This project is open-source software licensed under the [MIT license](https://mit-license.org/).

```text
MIT License

Copyright (c) 2026 Ali Candan

Permission is hereby granted, free of charge, to any person obtaining a copy
of this software and associated documentation files (the "Software"), to deal
in the Software without restriction, including without limitation the rights
to use, copy, modify, merge, publish, distribute, sublicense, and/or sell
copies of the Software, and to permit persons to whom the Software is
furnished to do so, subject to the following conditions:

The above copyright notice and this permission notice shall be included in all
copies or substantial portions of the Software.

THE SOFTWARE IS PROVIDED "AS IS", WITHOUT WARRANTY OF ANY KIND, EXPRESS OR
IMPLIED, INCLUDING BUT NOT LIMITED TO THE WARRANTIES OF MERCHANTABILITY,
FITNESS FOR A PARTICULAR PURPOSE AND NONINFRINGEMENT. IN NO EVENT SHALL THE
AUTHORS OR COPYRIGHT HOLDERS BE LIABLE FOR ANY CLAIM, DAMAGES OR OTHER
LIABILITY, WHETHER IN AN ACTION OF CONTRACT, TORT OR OTHERWISE, ARISING FROM,
OUT OF OR IN CONNECTION WITH THE SOFTWARE OR THE USE OR OTHER DEALINGS IN THE
SOFTWARE.

```

## Contributing

Contributions are welcome! If you find any bugs, want to add automated tests, or have suggestions for improvements, please feel free to open an issue or submit a pull request on the GitHub repository.

## Support

For any questions or support regarding **PY Grammar Corrector**, you can refer to the project's GitHub repository issues or contact the author directly via [Webkolog](http://webkolog.net).
