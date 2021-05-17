# rofi_et

rofi_et is a rofi script with features to aid you with English.

![preview](./assets/preview.gif)

## Features

- [x] Spellcheck and suggestions (offline, based on a wordlist)
- [x] Define (online, based on wordnik.com)
- [x] Synonyms (online, based on bighugelabs.com)
- [x] Antonyms (online, based on bighugelabs.com)
- [x] Abbreviations (online, based on Abbreviations.com)

## Dependencies

> The installation script won't install the dependencies for you because I don't know the package names on distros other than Arch

- `rofi` (of course) from `rofi` package on Arch
- `xclip` from `xclip` package on Arch => to copy selected spelling suggestion to clipboard
- `notify-send` from `libnotify` package on Arch => to notify you on copying a spelling suggestion to clipboard
- `agrep` from `tre` package on Arch => to do fuzzy searching in the wordlist to get spelling suggestions

## Installation

1. clone this repo => `git clone https://github.com/PlankCipher/rofi_et.git`
2. cd into the cloned repo directory
3. run `install.sh` => `./install.sh`
4. Voila 🎉

> You will be asked to enter your password for sudo to move the executable to `/sbin/rofi_et` so that it's accessible from anywhere

## Usage

![usage](./assets/usage.png)

## Credits

- I got `words_alpha` wordlist from [this](https://github.com/dwyl/english-words) repo.
- [wordnik.com](https://www.wordnik.com/) is used to get definitions.
- [abbreviations.com](https://www.abbreviations.com) is used to get what abbreviations stand for.
- [bighugelabs.com](https://words.bighugelabs.com) is used to get synonyms and antonyms.

## Contributions

Contributions are very welcome.
