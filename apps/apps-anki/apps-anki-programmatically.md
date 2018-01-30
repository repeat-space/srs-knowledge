How do I write scripts and programs which deal with Anki data files?
The list below contains experience reports and notes how to do this.

## Articles

- https://www.reddit.com/r/Anki/comments/6qxeuh/anki_scripting_101_automate_your_flashcards/

- https://www.juliensobczak.com/tell/2016/12/26/anki-scripting.html
- https://github.com/julien-sobczak/anki-scripting

- http://ojisanseiuchi.com/2016/03/12/anki-tool-low-level-manipulation-of-Anki-databases/
- http://ojisanseiuchi.com/2017/12/02/Accessing-the-Anki-database-with-Python-Working-with-a-specific-deck/
- http://ojisanseiuchi.com/2017/12/03/Anki-database-adventures-Counting-notes-by-model-type/
- http://ojisanseiuchi.com/2017/12/01/Working-with-the-Anki-database-on-mac-OS/
- http://ojisanseiuchi.com/2017/11/03/Process-automation-in-building-Anki-vocabulary-cards/
- http://ojisanseiuchi.com/2017/09/06/More-Javascript-with-Anki/

## Use Anki sources directly

```sh
$ mkdir app && cd app
$ git clone https://github.com/dae/anki.git
$ pip3 install -r anki/requirements.txt
$ touch main.py
```

```py
# main.py
import sys
import re
import os

sys.path.append(os.path.dirname(os.path.realpath(__file__)) + '/anki')
from anki import Collection as aopen

collection = aopen(os.environ['HOME'] +
                   '/.local/share/Anki2/User 1/collection.anki2')  # linux

for deck in collection.decks.all():
    print(deck['name'])
```

```sh
$ python3 main.py # prints all decks
```

## Python

- https://github.com/glutanimate/anki-cli-remote
- https://github.com/kerrickstaley/genanki
- https://github.com/coffeemug/ankify
- https://github.com/WillForan/anki-cli

## JavaScript

- https://github.com/repeat-space/anki-apkg-export
- https://github.com/fasiha/fuzzy-anki

## Golang

- https://github.com/flimzy/anki
- https://github.com/kovetskiy/ankictl
- https://github.com/seletskiy/runki

## Rust

- https://github.com/kerrickstaley/hsk_flashcards
