<div align="center">
  <h1>et</h1>

  <a href="https://ko-fi.com/Y8Y4HZ5S3" target="_blank">
    <img src="https://ko-fi.com/img/githubbutton_sm.svg" alt="Buy Me a Coffee at ko-fi.com" />
  </a>

  <br>
  <br>

A CLI/rofi/dmenu script with features to aid you with English.

</div>

## Preview

### rofi_et

![rofi_et](./assets/rofi_et.gif)

### dmenu_et

![dmenu_et](./assets/dmenu_et.gif)

## Features

- [x] Spellcheck and suggestions (offline, based on a wordlist)
- [x] Define (online, based on [wordnik.com](https://wordnik.com))
- [x] Synonyms (online, based on [bighugelabs.com](https://bighugelabs.com))
- [x] Antonyms (online, based on [bighugelabs.com](https://bighugelabs.com))
- [x] Abbreviations (online, based on [abbreviations.com](https://abbreviations.com))
- [x] Pronunciation (online, based on [wordnik.com](https://wordnik.com) and [dictionaryapi.dev](https://dictionaryapi.dev))

## Dependencies

> The installation script won't install the dependencies for you because I don't know the package names on distros other than Arch

- `rofi` or `dmenu`
- `xclip` from the `xclip` package (X) or `wl-copy` from the `wl-clipboard` (Wayland) package on Arch => to copy selected spelling suggestion to clipboard
- `notify-send` from `libnotify` package on Arch => to notify you on copying a spelling suggestion to clipboard
- `agrep` from `tre` package on Arch => to do fuzzy searching in the wordlist to get spelling suggestions
- `sox` from `sox` package on Arch => to play pronunciation

## Installation

1. clone this repo => `git clone https://github.com/PlankCipher/et.git`
2. cd into the cloned repo directory
3. run `install.sh` => `./install.sh`
4. Voila 🎉

> You will be asked to enter your password for sudo to move the executables to `/sbin/` so that they're accessible from anywhere

## Included

- et (simple underlying cli tool, run `et -h` for help)
- rofi_et (a rofi menu for et, run `rofi_et` then `help` for help)
- rofi_et_mode (a rofi custom mode for et, run `rofi -modes 'et:rofi_et_mode,drun,window' -show et` then `help` for help)
- dmenu_et (a dmenu script for et, run `dmenu_et` and then `help` for help)

## Usage

### et

```man
Usage: et OPTION...

Options:
  -abr, --abbreviations <abr>
    Print what <abr> might stand for from abbreviations.com.

  -ant, --antonyms <word>
    Print antonyms for <word> from bighugelabs.com.

  -def, --define <word>
    Print definitions for <word> from wordnik.com if correctly spelled, otherwise print spell suggestions.

  -pro, --pronounce <word>
    Play pronunciation of <word>.

    Defaults to American English pronunciation (listed as macmillan in sources list) from wordnik.com (which in turn depends on macmillandictionary). Other pronunciation sources/accents (from dictionaryapi.dev) can be listed with -lst|--list-sources and specified with -src|--source (must come after -pro|--pronounce).

  -lst, --list-sources <word>
    List available pronunciation sources/accents for <word>.

  -src, --source <source>
    Specify the <source> to use for pronunciation. This option must come after -pro|--pronounce.

  -spl, --spell <word>
    Print spell suggestions for <word> from wordlist if not spelled correctly (exits with 1 as exit code), otherwise print a message indicating that <word> is spelled correctly.

  -syn, --synonyms <word>
    Print synonyms for <word> from bighugelabs.com.

  -h, --help
    Print this help message and exit
```

### rofi_et, rofi_et_mode, or dmenu_et

![usage](./assets/usage.png)

## Credits

- I got `words_alpha` wordlist from [this](https://github.com/dwyl/english-words) repo.
- [wordnik.com](https://www.wordnik.com) is used to get definitions and pronunciations.
- [abbreviations.com](https://www.abbreviations.com) is used to get what abbreviations stand for.
- [bighugelabs.com](https://words.bighugelabs.com) is used to get synonyms and antonyms.
- [dictionaryapi.dev](https://dictionaryapi.dev) is used to get pronunciations.

## Contributions

Contributions are very welcome.
