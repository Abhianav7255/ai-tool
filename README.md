# Spellchecker Python Script

This Python script corrects the spelling in a given sentence using the `SpellChecker` library. It identifies and fixes misspelled words, providing a corrected version of the input sentence.

---

## Features

- Automatically detects misspelled words.
- Suggests the most likely correct spelling for each word.
- Processes the input sentence and returns a corrected version.

---

## Prerequisites

Ensure the following are installed:

- Python 3.x
- `pyspellchecker` library

### Installing `pyspellchecker`

Install the `pyspellchecker` library using pip:

```bash
pip install pyspellchecker
```

---

## Script Code

```python
from spellchecker import SpellChecker

def correct_sentence(sentence):
    spell = SpellChecker()
    words = sentence.split()  # Convert the sentence into individual words
    corrected_words = [spell.correction(word) for word in words]
    corrected_sentence = " ".join(corrected_words)
    return corrected_sentence

misspelled_sentence = str(input("Enter the sentence: "))
corrected_sentence = correct_sentence(misspelled_sentence)
print(f"Misspelled Sentence: {misspelled_sentence}")
print(f"Corrected Sentence: {corrected_sentence}")
```

---

## Usage

1. **Run the Script:** Execute the Python script in your terminal or IDE.
2. **Input a Sentence:** Enter a sentence with potential spelling errors.
3. **View Corrected Output:** The script will display the original and corrected sentences.

### Example

**Input:**
```plaintext
Enter the sentence: Ths is a smple sentnce
```

**Output:**
```plaintext
Misspelled Sentence: Ths is a smple sentnce
Corrected Sentence: The is a simple sentence
```

---

## File Structure

```plaintext
project-directory
├── spellchecker_script.py   # Main Python script
```

---

## Contributing

Contributions are welcome! Feel free to fork the repository and submit pull requests for improvements or additional features.

---

## License

This project is licensed under the MIT License. See the [LICENSE](LICENSE) file for details.

---

## Author

**Abhinav Kumar(https://github.com/Abhianav7255)**

---

## Notes

- This script uses the `pyspellchecker` library, which supports basic spellchecking and corrections. For advanced use cases, consider integrating with more sophisticated NLP libraries like `spaCy` or `TextBlob`.
