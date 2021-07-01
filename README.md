# et

A CLI/rofi/dmenu script with features to aid you with English.

## Preview

### rofi_et

![rofi_et](./assets/rofi_et.gif)

### dmenu_et

![dmenu_et](./assets/dmenu_et.gif)

## Features

- [x] Spellcheck and suggestions (offline, based on a wordlist)
- [x] Define (online, based on wordnik.com)
- [x] Synonyms (online, based on bighugelabs.com)
- [x] Antonyms (online, based on bighugelabs.com)
- [x] Abbreviations (online, based on Abbreviations.com)
- [ ] Pronunciation (online, TBD)

## Dependencies

> The installation script won't install the dependencies for you because I don't know the package names on distros other than Arch

- `rofi` or `dmenu`
- `xclip` from `xclip` package on Arch => to copy selected spelling suggestion to clipboard
- `notify-send` from `libnotify` package on Arch => to notify you on copying a spelling suggestion to clipboard
- `agrep` from `tre` package on Arch => to do fuzzy searching in the wordlist to get spelling suggestions

## Installation

1. clone this repo => `git clone https://github.com/PlankCipher/rofi_et.git`
2. cd into the cloned repo directory
3. run `install.sh` => `./install.sh`
4. Voila 🎉

> You will be asked to enter your password for sudo to move the executables to `/sbin/` so that they're accessible from anywhere

## Usage

### et

```man
Usage: et OPTION [WORD]

Options:
  -abr or --abbreviations
    print what WORD might stand for from abbreviations.com. (WORD is required for this option)

  -ant or --antonyms
    print antonyms for WORD from bighugelabs.com. (WORD is required for this option)

  -def or --define
    print definitions for WORD from wordnik.com if correctly spelled, otherwise print spell suggestions. (WORD is required for this option)

  -spl or --spell
    print spell suggestions for WORD from wordlist if not spelled correctly (exits with 1 as exit code), otherwise print a message indicating that WORD is spelled correctly. (WORD is required for this option)

  -syn or --synonyms
    print synonyms for WORD from bighugelabs.com. (WORD is required for this option)

  -h or --help
    print this help message and exit
```

### rofi_et or dmenu_et

![usage](./assets/usage.png)

## Credits

- I got `words_alpha` wordlist from [this](https://github.com/dwyl/english-words) repo.
- [wordnik.com](https://www.wordnik.com/) is used to get definitions.
- [abbreviations.com](https://www.abbreviations.com) is used to get what abbreviations stand for.
- [bighugelabs.com](https://words.bighugelabs.com) is used to get synonyms and antonyms.

## Contributions

Contributions are very welcome.
